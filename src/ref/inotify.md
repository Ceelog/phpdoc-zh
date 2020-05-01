inotify\_add\_watch
===================

Add a watch to an initialized inotify instance

### 说明

<span class="type">int</span> <span
class="methodname">inotify\_add\_watch</span> ( <span
class="methodparam"><span class="type">resource</span>
`$inotify_instance`</span> , <span class="methodparam"><span
class="type">string</span> `$pathname`</span> , <span
class="methodparam"><span class="type">int</span> `$mask`</span> )

<span class="function">inotify\_add\_watch</span> adds a new watch or
modify an existing watch for the file or directory specified in
`pathname`.

Using <span class="function">inotify\_add\_watch</span> on a watched
object replaces the existing watch. Using the **`IN_MASK_ADD`** constant
adds (OR) events to the existing watch.

### 参数

`inotify_instance`  
<span class="function">inotify\_init</span>返回的资源

`pathname`  
File or directory to watch

`mask`  
Events to watch for. See
<a href="/inotify/constants.html" class="link">预定义常量</a>.

### 返回值

The return value is a unique (inotify instance wide) watch descriptor.

### 参见

-   <span class="function">inotify\_init</span>

inotify\_init
=============

Initialize an inotify instance

### 说明

<span class="type">resource</span> <span
class="methodname">inotify\_init</span> ( <span
class="methodparam">void</span> )

Initialize an inotify instance for use with <span
class="function">inotify\_add\_watch</span>

### 返回值

A stream resource or **`FALSE`** on error.

### 范例

**示例 \#1 Example usage of inotify**

``` php
<?php
// Open an inotify instance
$fd = inotify_init();

// Watch __FILE__ for metadata changes (e.g. mtime)
$watch_descriptor = inotify_add_watch($fd, __FILE__, IN_ATTRIB);

// generate an event
touch(__FILE__);

// Read events
$events = inotify_read($fd);
print_r($events);

// The following methods allows to use inotify functions without blocking on inotify_read():

// - Using stream_select() on $fd:
$read = array($fd);
$write = null;
$except = null;
stream_select($read,$write,$except,0);

// - Using stream_set_blocking() on $fd
stream_set_blocking($fd, 0);
inotify_read($fd); // Does no block, and return false if no events are pending

// - Using inotify_queue_len() to check if event queue is not empty
$queue_len = inotify_queue_len($fd); // If > 0, inotify_read() will not block

// Stop watching __FILE__ for metadata changes
inotify_rm_watch($fd, $watch_descriptor);

// Close the inotify instance
// This may have closed all watches if this was not already done
fclose($fd);

?>
```

以上例程的输出类似于：

    array(
      array(
        'wd' => 1,     // Equals $watch_descriptor
        'mask' => 4,   // IN_ATTRIB bit is set
        'cookie' => 0, // unique id to connect related events (e.g. 
                       // IN_MOVE_FROM and IN_MOVE_TO events)
        'name' => '',  // the name of a file (e.g. if we monitored changes
                       // in a directory)
      ),
    );

### 参见

-   <span class="function">inotify\_add\_watch</span>
-   <span class="function">inotify\_rm\_watch</span>
-   <span class="function">inotify\_queue\_len</span>
-   <span class="function">inotify\_read</span>
-   <span class="function">fclose</span>

inotify\_queue\_len
===================

Return a number upper than zero if there are pending events

### 说明

<span class="type">int</span> <span
class="methodname">inotify\_queue\_len</span> ( <span
class="methodparam"><span class="type">resource</span>
`$inotify_instance`</span> )

This function allows to know if <span
class="function">inotify\_read</span> will block or not. If a number
upper than zero is returned, there are pending events and <span
class="function">inotify\_read</span> will not block.

### 参数

`inotify_instance`  
<span class="function">inotify\_init</span>返回的资源

### 返回值

Returns a number upper than zero if there are pending events.

### 参见

-   <span class="function">inotify\_init</span>
-   <span class="function">stream\_select</span>
-   <span class="function">stream\_set\_blocking</span>

inotify\_read
=============

Read events from an inotify instance

### 说明

<span class="type">array</span> <span
class="methodname">inotify\_read</span> ( <span
class="methodparam"><span class="type">resource</span>
`$inotify_instance`</span> )

Read inotify events from an inotify instance.

### 参数

`inotify_instance`  
<span class="function">inotify\_init</span>返回的资源

### 返回值

An array of inotify events or **`FALSE`** if no events was pending and
`inotify_instance` is non-blocking. Each event is an array with the
following keys:

-   wd is a watch descriptor returned by <span
    class="function">inotify\_add\_watch</span>
-   mask is a bit mask of
    <a href="/inotify/constants.html" class="link">events</a>
-   cookie is a unique id to connect related events (e.g.
    **`IN_MOVE_FROM`** and **`IN_MOVE_TO`**)
-   name is the name of a file (e.g. if a file was modified in a watched
    directory)

### 参见

-   <span class="function">inotify\_init</span>
-   <span class="function">stream\_select</span>
-   <span class="function">stream\_set\_blocking</span>
-   <span class="function">inotify\_queue\_len</span>

inotify\_rm\_watch
==================

Remove an existing watch from an inotify instance

### 说明

<span class="type">bool</span> <span
class="methodname">inotify\_rm\_watch</span> ( <span
class="methodparam"><span class="type">resource</span>
`$inotify_instance`</span> , <span class="methodparam"><span
class="type">int</span> `$watch_descriptor`</span> )

<span class="function">inotify\_rm\_watch</span> removes the watch
`watch_descriptor` from the inotify instance `inotify_instance`.

### 参数

`inotify_instance`  
<span class="function">inotify\_init</span>返回的资源

`watch_descriptor`  
Watch to remove from the instance

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">inotify\_init</span>

**目录**

-   [inotify\_add\_watch](/ref/inotify.html#inotify_add_watch) — Add a
    watch to an initialized inotify instance
-   [inotify\_init](/ref/inotify.html#inotify_init) — Initialize an
    inotify instance
-   [inotify\_queue\_len](/ref/inotify.html#inotify_queue_len) — Return
    a number upper than zero if there are pending events
-   [inotify\_read](/ref/inotify.html#inotify_read) — Read events from
    an inotify instance
-   [inotify\_rm\_watch](/ref/inotify.html#inotify_rm_watch) — Remove an
    existing watch from an inotify instance
