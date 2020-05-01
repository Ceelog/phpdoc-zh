范例
====

**示例 \#1 面向对象风格**

``` php
<?php

$queue  = '/queue/foo';
$msg    = 'bar';

/* connection */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Connection failed: ' . $e->getMessage());
}

/* send a message to the queue 'foo' */
$stomp->send($queue, $msg);

/* subscribe to messages from the queue 'foo' */
$stomp->subscribe($queue);

/* read a frame */
$frame = $stomp->readFrame();

if ($frame->body === $msg) {
    var_dump($frame);

    /* acknowledge that the frame was received */
    $stomp->ack($frame);
}

/* close connection */
unset($stomp);

?>
```

以上例程的输出类似于：

    object(StompFrame)#2 (3) {
      ["command"]=>
      string(7) "MESSAGE"
      ["headers"]=>
      array(5) {
        ["message-id"]=>
        string(41) "ID:php.net-55293-1257226743606-4:2:-1:1:1"
        ["destination"]=>
        string(10) "/queue/foo"
        ["timestamp"]=>
        string(13) "1257226805828"
        ["expires"]=>
        string(1) "0"
        ["priority"]=>
        string(1) "0"
      }
      ["body"]=>
      string(3) "bar"
    }

**示例 \#2 过程化风格**

``` php
<?php

$queue  = '/queue/foo';
$msg    = 'bar';

/* connection */
$link = stomp_connect('ssl://localhost:61612');

/* check connection */
if (!$link) {
    die('Connection failed: ' . stomp_connect_error());
}

/* begin a transaction */
stomp_begin($link, 't1');

/* send a message to the queue 'foo' */
stomp_send($link, $queue, $msg, array('transaction' => 't1'));

/* commit a transaction */
stomp_commit($link, 't1');

/* subscribe to messages from the queue 'foo' */
stomp_subscribe($link, $queue);

/* read a frame */
$frame = stomp_read_frame($link);

if ($frame['body'] === $msg) {
    var_dump($frame);

    /* acknowledge that the frame was received */
    stomp_ack($link, $frame['headers']['message-id']);
}

/* close connection */
stomp_close($link);

?>
```

以上例程的输出类似于：

    array(3) {
      ["command"]=>
      string(7) "MESSAGE"
      ["body"]=>
      string(3) "bar"
      ["headers"]=>
      array(6) {
        ["transaction"]=>
        string(2) "t1"
        ["message-id"]=>
        string(41) "ID:php.net-55293-1257226743606-4:3:-1:1:1"
        ["destination"]=>
        string(10) "/queue/foo"
        ["timestamp"]=>
        string(13) "1257227037059"
        ["expires"]=>
        string(1) "0"
        ["priority"]=>
        string(1) "0"
      }
    }
