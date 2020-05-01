范例
====

**示例 \#1 Simple timers**

``` php
<?php
// Create and start timer firing after 2 seconds
$w1 = new EvTimer(2, 0, function () {
    echo "2 seconds elapsed\n";
});

// Create and launch timer firing after 2 seconds repeating each second
// until we manually stop it
$w2 = new EvTimer(2, 1, function ($w) {
    echo "is called every second, is launched after 2 seconds\n";
    echo "iteration = ", Ev::iteration(), PHP_EOL;

    // Stop the watcher after 5 iterations
    Ev::iteration() == 5 and $w->stop();
    // Stop the watcher if further calls cause more than 10 iterations
    Ev::iteration() >= 10 and $w->stop();
});

// Create stopped timer. It will be inactive until we start it ourselves
$w_stopped = EvTimer::createStopped(10, 5, function($w) {
    echo "Callback of a timer created as stopped\n";

    // Stop the watcher after 2 iterations
    Ev::iteration() >= 2 and $w->stop();
});

// Loop until Ev::stop() is called or all of watchers stop
Ev::run();

// Start and look if it works
$w_stopped->start();
echo "Run single iteration\n";
Ev::run(Ev::RUN_ONCE);

echo "Restart the second watcher and try to handle the same events, but don't block\n";
$w2->again();
Ev::run(Ev::RUN_NOWAIT);

$w = new EvTimer(10, 0, function() {});
echo "Running a blocking loop\n";
Ev::run();
echo "END\n";
?>
```

以上例程的输出类似于：

    2 seconds elapsed
    is called every second, is launched after 2 seconds
    iteration = 1
    is called every second, is launched after 2 seconds
    iteration = 2
    is called every second, is launched after 2 seconds
    iteration = 3
    is called every second, is launched after 2 seconds
    iteration = 4
    is called every second, is launched after 2 seconds
    iteration = 5
    Run single iteration
    Callback of a timer created as stopped
    Restart the second watcher and try to handle the same events, but don't block
    Running a blocking loop
    is called every second, is launched after 2 seconds
    iteration = 8
    is called every second, is launched after 2 seconds
    iteration = 9
    is called every second, is launched after 2 seconds
    iteration = 10
    END

**示例 \#2 Periodic timer. Tick each 10.5 seconds**

``` php
<?php
$w = new EvPeriodic(0., 10.5, NULL, function ($w, $revents) {
    echo time(), PHP_EOL;
});

Ev::run();
?>
```

**示例 \#3 Periodic timer. Use reschedule callback**

``` php
<?php
// Tick each 10.5 seconds

function reschedule_cb ($watcher, $now) {
    return $now + (10.5. - fmod($now, 10.5));
}

$w = new EvPeriodic(0., 0., "reschedule_cb", function ($w, $revents) {
    echo time(), PHP_EOL;
});

Ev::run();
?>
```

**示例 \#4 Periodic timer. Tick every 10.5 seconds starting at now**

``` php
<?php
// Tick every 10.5 seconds starting at now
$w = new EvPeriodic(fmod(Ev::now(), 10.5), 10.5, NULL, function ($w, $revents) {
    echo time(), PHP_EOL;
});

Ev::run();
?>
```

**示例 \#5 Wait until STDIN is readable**

``` php
<?php
// Wait until STDIN is readable
$w = new EvIo(STDIN, Ev::READ, function ($watcher, $revents) {
    echo "STDIN is readable\n";
});

Ev::run(Ev::RUN_ONCE);
?>
```

**示例 \#6 Use some async I/O to access a socket**

``` php
<?php
/* Use some async I/O to access a socket */

// `sockets' extension still logs warnings
// for EINPROGRESS, EAGAIN/EWOULDBLOCK etc.
error_reporting(E_ERROR);

$e_nonblocking = array (/*EAGAIN or EWOULDBLOCK*/11, /*EINPROGRESS*/115);

// Get the port for the WWW service
$service_port = getservbyname('www', 'tcp');

// Get the IP address for the target host
$address = gethostbyname('google.co.uk');

// Create a TCP/IP socket
$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);
if ($socket === FALSE) {
    echo "socket_create() failed: reason: "
        .socket_strerror(socket_last_error()) . "\n";
}

// Set O_NONBLOCK flag
socket_set_nonblock($socket);

// Abort on timeout
$timeout_watcher = new EvTimer(10.0, 0., function () use ($socket) {
    socket_close($socket);
    Ev::stop(Ev::BREAK_ALL);
});

// Make HEAD request when the socket is writable
$write_watcher = new EvIo($socket, Ev::WRITE, function ($w)
    use ($socket, $timeout_watcher, $e_nonblocking)
{
    // Stop timeout watcher
    $timeout_watcher->stop();
    // Stop write watcher
    $w->stop();

    $in = "HEAD / HTTP/1.1\r\n";
    $in .= "Host: google.co.uk\r\n";
    $in .= "Connection: Close\r\n\r\n";

    if (!socket_write($socket, $in, strlen($in))) {
        trigger_error("Failed writing $in to socket", E_USER_ERROR);
    }

    $read_watcher = new EvIo($socket, Ev::READ, function ($w, $re)
        use ($socket, $e_nonblocking)
    {
        // Socket is readable. recv() 20 bytes using non-blocking mode
        $ret = socket_recv($socket, $out, 20, MSG_DONTWAIT);

        if ($ret) {
            echo $out;
        } elseif ($ret === 0) {
            // All read
            $w->stop();
            socket_close($socket);
            return;
        }

        // Caught EINPROGRESS, EAGAIN, or EWOULDBLOCK
        if (in_array(socket_last_error(), $e_nonblocking)) {
            return;
        }

        $w->stop();
        socket_close($socket);
    });

    Ev::run();
});

$result = socket_connect($socket, $address, $service_port);

Ev::run();
?>
```

以上例程的输出类似于：

    HTTP/1.1 301 Moved Permanently
    Location: http://www.google.co.uk/
    Content-Type: text/html; charset=UTF-8
    Date: Sun, 23 Dec 2012 16:08:27 GMT
    Expires: Tue, 22 Jan 2013 16:08:27 GMT
    Cache-Control: public, max-age=2592000
    Server: gws
    Content-Length: 221
    X-XSS-Protection: 1; mode=block
    X-Frame-Options: SAMEORIGIN
    Connection: close

**示例 \#7 Embedding one loop into another**

``` php
<?php
/*
* Try to get an embeddable event loop and embed it into the default event loop.
* If it is impossible, use the default
* loop. The default loop is stored in $loop_hi, while the embeddable loop is
* stored in $loop_lo(which is $loop_hi in the case no embeddable loop can be
* used).
*
* Sample translated to PHP
* http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#Examples_CONTENT-9
*/
$loop_hi = EvLoop::defaultLoop();
$loop_lo = NULL;
$embed   = NULL;

/*
* See if there is a chance of getting one that works
* (flags' value of 0 means autodetection)
*/
$loop_lo = Ev::embeddableBackends() & Ev::recommendedBackends()
    ? new EvLoop(Ev::embeddableBackends() & Ev::recommendedBackends())
    : 0;

if ($loop_lo) {
    $embed = new EvEmbed($loop_lo, function () {});
} else {
    $loop_lo = $loop_hi;
}
?>
```

**示例 \#8 Embedding loop created with kqueue backend into the default
loop**

``` php
<?php
/*
* Check if kqueue is available but not recommended and create a kqueue backend
* for use with sockets (which usually work with any kqueue implementation).
* Store the kqueue/socket-only event loop in loop_socket. (One might optionally
* use EVFLAG_NOENV, too)
*
* Example borrowed from
* http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#Examples_CONTENT-9
*/
$loop        = EvLoop::defaultLoop();
$socket_loop = NULL;
$embed       = NULL;

if (Ev::supportedBackends() & ~Ev::recommendedBackends() & Ev::BACKEND_KQUEUE) {
    if (($socket_loop = new EvLoop(Ev::BACKEND_KQUEUE))) {
        $embed = new EvEmbed($loop);
    }
}

if (!$socket_loop) {
    $socket_loop = $loop;
}

// Now use $socket_loop for all sockets, and $loop for anything else
?>
```

**示例 \#9 Handle SIGTERM signal**

``` php
<?php
$w = new EvSignal(SIGTERM, function ($watcher) {
    echo "SIGTERM received\n";
    $watcher->stop();
});

Ev::run();
?>
```

**示例 \#10 Monitor changes of /var/log/messages**

``` php
<?php
// Use 10 second update interval.
$w = new EvStat("/var/log/messages", 8, function ($w) {
    echo "/var/log/messages changed\n";

    $attr = $w->attr();

    if ($attr['nlink']) {
        printf("Current size: %ld\n", $attr['size']);
        printf("Current atime: %ld\n", $attr['atime']);
        printf("Current mtime: %ld\n", $attr['mtime']);
    } else {
        fprintf(STDERR, "`messages` file is not there!");
        $w->stop();
    }
});

Ev::run();
?>
```

**示例 \#11 Monotor changes of /var/log/messages. Avoid missing updates
by means of one second delay**

``` php
<?php
$timer = EvTimer::createStopped(0., 1.02, function ($w) {
    $w->stop();

    $stat = $w->data;

    // 1 second after the most recent change of the file
    printf("Current size: %ld\n", $stat->attr()['size']);
});

$stat = new EvStat("/var/log/messages", 0., function () use ($timer) {
    // Reset timer watcher
    $timer->again();
});

$timer->data = $stat;

Ev::run();
?>
```

**示例 \#12 Process status changes**

``` php
<?php
$pid = pcntl_fork();

if ($pid == -1) {
    fprintf(STDERR, "pcntl_fork failed\n");
} elseif ($pid) {
    $w = new EvChild($pid, FALSE, function ($w, $revents) {
        $w->stop();

        printf("Process %d exited with status %d\n", $w->rpid, $w->rstatus);
    });

    Ev::run();

    // Protect against Zombies
    pcntl_wait($status);
} else {
    //Forked child
    exit(2);
}
?>
```
