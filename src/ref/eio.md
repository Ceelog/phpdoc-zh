eio\_busy
=========

Artificially increase load. Could be useful in tests, benchmarking

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_busy</span> ( <span class="methodparam"><span
class="type">int</span> `$delay`</span> \[, <span
class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_busy</span> artificially increases load
taking `delay` seconds to execute. May be used for debugging, or
benchmarking.

### 参数

`delay`  
Delay in seconds

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
This callback is called when all the group requests are done.

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_busy</span> returns request resource on
success or **`FALSE`** on error.

### 参见

-   <span class="function">eio\_nop</span>

eio\_cancel
===========

Cancels a request

### 说明

<span class="type">void</span> <span
class="methodname">eio\_cancel</span> ( <span class="methodparam"><span
class="type">resource</span> `$req`</span> )

<span class="function">eio\_cancel</span> cancels a request specified by
`req`

### 参数

`req`  
The request resource

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">eio\_cancel</span> example**

``` php
<?php
 /* Is called when eio_nop() finished */
 function my_nop_cb($data, $result) {
  echo "my_nop ", $data, "\n";
 }

// This eio_nop() call will be cancelled
$req = eio_nop(EIO_PRI_DEFAULT, "my_nop_cb", "1");
var_dump($req);
eio_cancel($req);

// This time eio_nop() will be processed
eio_nop(EIO_PRI_DEFAULT, "my_nop_cb", "2");

// Process requests
eio_event_loop();
?>
```

以上例程的输出类似于：

    resource(4) of type (EIO Request Descriptor)
    my_nop 2

### 参见

-   <span class="function">eio\_grp\_cancel</span>

eio\_chmod
==========

Change file/directory permissions

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_chmod</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">int</span> `$mode`</span> \[,
<span class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_chmod</span> changes file, or directory
permissions. The new permissions are specified by `mode`.

### 参数

`path`  
Path to the target file or directory

**Warning**
避免相对路径。

`mode`  
The new permissions. E.g. **`0644`**.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_chmod</span> returns request resource on
success or **`FALSE`** on error.

### 参见

-   <span class="function">eio\_chown</span>

eio\_chown
==========

Change file/directory permissions

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_chown</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">int</span> `$uid`</span> \[,
<span class="methodparam"><span class="type">int</span> `$gid`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\]\] )

Changes file, or directory permissions.

### 参数

`path`  
Path to file or directory.

**Warning**
避免相对路径。

`uid`  
User ID. Is ignored when equal to -1.

`gid`  
Group ID. Is ignored when equal to -1.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_chown</span> returns request resource on
success or **`FALSE`** on error.

### 参见

-   <span class="function">eio\_chmod</span>

eio\_close
==========

Close file

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_close</span> ( <span class="methodparam"><span
class="type">mixed</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_close</span> closes file specified by `fd`.

### 参数

`fd`  
Stream, Socket resource, or numeric file descriptor

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_close</span> returns request resource on
success or **`FALSE`** on error.

### 参见

-   <span class="function">eio\_open</span>

eio\_custom
===========

Execute custom request like any other *eio\_\** call

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_custom</span> ( <span class="methodparam"><span
class="type">callable</span> `$execute`</span> , <span
class="methodparam"><span class="type">int</span> `$pri`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`<span class="initializer"> =
NULL</span></span> \] )

<span class="function">eio\_custom</span> executes custom function
specified by `execute` processing it just like any other *eio\_\** call.

### 参数

`execute`  
Specifies the request function that should match the following
prototype:

          mixed execute(mixed data);
          

`callback` is event completion callback that should match the following
prototype:

          void callback(mixed data, mixed result);
          

`data` is the data passed to `execute` via `data` argument without
modifications `result` value returned by `execute`

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_custom</span> returns request resource on
success or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">eio\_custom</span> example**

``` php
<?php
/* Callback for the custom callback */
function my_custom_callback($data, $result) {
    var_dump($data);
    var_dump(count($result));
    var_dump($result['data_modified']);
    var_dump($result['result']);
}

/* The custom request */
function my_custom($data) {
    var_dump($data);

    $result  = array(
        'result'        => 1001,
        'data_modified' => "my custom data",
    );

    return $result;
}

$data = "my_custom_data";
$req = eio_custom("my_custom", EIO_PRI_DEFAULT, "my_custom_callback", $data);
var_dump($req);
eio_event_loop();
?>
```

以上例程的输出类似于：

    resource(4) of type (EIO Request Descriptor)
    string(14) "my_custom_data"
    string(14) "my_custom_data"
    int(2)
    string(14) "my custom data"
    int(1001)
     

eio\_dup2
=========

Duplicate a file descriptor

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_dup2</span> ( <span class="methodparam"><span
class="type">mixed</span> `$fd`</span> , <span class="methodparam"><span
class="type">mixed</span> `$fd2`</span> \[, <span
class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_dup2</span> duplicates file descriptor.

### 参数

`fd`  
Source stream, Socket resource, or numeric file descriptor

`fd2`  
Target stream, Socket resource, or numeric file descriptor

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_dup2</span> returns request resource on
success or **`FALSE`** on error.

eio\_event\_loop
================

Polls libeio until all requests proceeded

### 说明

<span class="type">bool</span> <span
class="methodname">eio\_event\_loop</span> ( <span
class="methodparam">void</span> )

<span class="function">eio\_event\_loop</span> polls libeio until all
requests proceeded.

### 参数

此函数没有参数。

### 返回值

<span class="function">eio\_event\_loop</span> returns **`TRUE`** on
success or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">eio\_event\_loop</span> example**

``` php
<?php
$temp_filename = "eio-temp-file.tmp";
touch($temp_filename);

/* Is called when eio_chmod() finished */
function my_chmod_callback($data, $result) {
    global $temp_filename;

    if ($result == 0 && !is_readable($temp_filename) && is_writable($temp_filename)) {
        echo "eio_chmod_ok";
    }

    @unlink($temp_filename);
}

eio_chmod($temp_filename, 0200, EIO_PRI_DEFAULT, "my_chmod_callback");
eio_event_loop();
?>
```

以上例程的输出类似于：

    eio_chmod_ok
     

### 参见

-   <span class="function">eio\_poll</span>

eio\_fallocate
==============

Allows the caller to directly manipulate the allocated disk space for a
file

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_fallocate</span> ( <span
class="methodparam"><span class="type">mixed</span> `$fd`</span> , <span
class="methodparam"><span class="type">int</span> `$mode`</span> , <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$length`</span>
\[, <span class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_fallocate</span> allows the caller to
directly manipulate the allocated disk space for the file specified by
`fd` file descriptor for the byte range starting at `offset` and
continuing for `length` bytes.

> **Note**: **File should be opened for writing**  
>
> **`EIO_O_CREAT`** should be logically *OR*'d with **`EIO_O_WRONLY`**,
> or **`EIO_O_RDWR`**

### 参数

`fd`  
Stream, Socket resource, or numeric file descriptor, e.g. returned by
<span class="function">eio\_open</span>.

`mode`  
Currently only one flag is supported for mode:
**`EIO_FALLOC_FL_KEEP_SIZE`** (the same as POSIX constant
**`FALLOC_FL_KEEP_SIZE`**).

`offset`  
Specifies start of the byte range.

`length`  
Specifies length the byte range.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_fallocate</span> returns request resource on
success or **`FALSE`** on error.

eio\_fchmod
===========

Change file permissions

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_fchmod</span> ( <span class="methodparam"><span
class="type">mixed</span> `$fd`</span> , <span class="methodparam"><span
class="type">int</span> `$mode`</span> \[, <span
class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_fchmod</span> changes permissions for the
file specified by `fd` file descriptor.

### 参数

`fd`  
Stream, Socket resource, or numeric file descriptor, e.g. returned by
<span class="function">eio\_open</span>.

`mode`  
The new permissions. E.g. 0644.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_fchmod</span> returns request resource on
success or **`FALSE`** on error.

### 参见

-   <span class="function">eio\_fchown</span>

eio\_fchown
===========

Change file ownership

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_fchown</span> ( <span class="methodparam"><span
class="type">mixed</span> `$fd`</span> , <span class="methodparam"><span
class="type">int</span> `$uid`</span> \[, <span
class="methodparam"><span class="type">int</span> `$gid`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\]\] )

<span class="function">eio\_fchown</span> changes ownership of the file
specified by `fd` file descriptor.

### 参数

`fd`  
Stream, Socket resource, or numeric file descriptor.

`uid`  
User ID. Is ignored when equal to -1.

`gid`  
Group ID. Is ignored when equal to -1.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 参见

-   <span class="function">eio\_fchmod</span>

eio\_fdatasync
==============

Synchronize a file's in-core state with storage device

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_fdatasync</span> ( <span
class="methodparam"><span class="type">mixed</span> `$fd`</span> \[,
<span class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_fdatasync</span> synchronizes a file's
in-core state with storage device.

### 参数

`fd`  
Stream, Socket resource, or numeric file descriptor, e.g. returned by
<span class="function">eio\_open</span>.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_fdatasync</span> returns request resource on
success or **`FALSE`** on error.

eio\_fstat
==========

Get file status

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_fstat</span> ( <span class="methodparam"><span
class="type">mixed</span> `$fd`</span> , <span class="methodparam"><span
class="type">int</span> `$pri`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`</span> \] )

<span class="function">eio\_fstat</span> returns file status information
in `result` argument of `callback`

### 参数

`fd`  
Stream, Socket resource, or numeric file descriptor.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_busy</span> returns request resource on
success or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">eio\_lstat</span> example**

``` php
<?php
// Create temporary file
$tmp_filename = dirname(__FILE__) ."/eio-file.tmp";
touch($tmp_filename);

/* Is called when eio_fstat() done */
function my_res_cb($data, $result) {
 // Should output array with stat info
 var_dump($result);

 if ($data['fd']) {
  // Close temporary file
  eio_close($data['fd']);
  eio_event_loop();
 }
 // Remove temporary file
 @unlink($data['file']);
}

/* Is called when eio_open() done */
function my_open_cb($data, $result) {
 // Prepare data for callback
 $d = array(
  'fd'  => $result,
  'file'=> $data
 );
 // Request stat info
 eio_fstat($result, EIO_PRI_DEFAULT, "my_res_cb", $d);
 // Process request(s)
 eio_event_loop();
}

// Open temporary file
eio_open($tmp_filename, EIO_O_RDONLY, NULL, EIO_PRI_DEFAULT,
  "my_open_cb", $tmp_filename);
eio_event_loop();
?>
```

以上例程的输出类似于：

    array(12) {
     ["st_dev"]=>
      int(2050)
      ["st_ino"]=>
      int(2489159)
      ["st_mode"]=>
      int(33188)
      ["st_nlink"]=>
      int(1)
      ["st_uid"]=>
      int(1000)
      ["st_gid"]=>
      int(100)
      ["st_rdev"]=>
      int(0)
      ["st_blksize"]=>
      int(4096)
      ["st_blocks"]=>
      int(0)
      ["st_atime"]=>
      int(1318239506)
      ["st_mtime"]=>
      int(1318239506)
      ["st_ctime"]=>
      int(1318239506)
    }

### 参见

-   <span class="function">eio\_lstat</span>
-   <span class="function">eio\_stat</span>

eio\_fstatvfs
=============

Get file system statistics

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_fstatvfs</span> ( <span
class="methodparam"><span class="type">mixed</span> `$fd`</span> , <span
class="methodparam"><span class="type">int</span> `$pri`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`</span> \] )

<span class="function">eio\_fstatvfs</span> returns file system
statistics in `result` of `callback`.

### 参数

`fd`  
A file descriptor of a file within the mounted file system.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_fstatvfs</span> returns request resource on
success or **`FALSE`** on error.

### 参见

-   <span class="function">eio\_statvfs</span>

eio\_fsync
==========

Synchronize a file's in-core state with storage device

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_fsync</span> ( <span class="methodparam"><span
class="type">mixed</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

Synchronize a file's in-core state with storage device

### 参数

`fd`  
Stream, Socket resource, or numeric file descriptor.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_fsync</span> returns request resource on
success or **`FALSE`** on error.

### 参见

-   <span class="function">eio\_sync</span>

eio\_ftruncate
==============

Truncate a file

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_ftruncate</span> ( <span
class="methodparam"><span class="type">mixed</span> `$fd`</span> \[,
<span class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\]\] )

<span class="function">eio\_ftruncate</span> causes a regular file
referenced by `fd` file descriptor to be truncated to precisely `length`
bytes.

### 参数

`fd`  
Stream, Socket resource, or numeric file descriptor.

`offset`  
Offset from beginning of the file

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_ftruncate</span> returns request resource on
success or **`FALSE`** on error.

### 参见

-   <span class="function">eio\_truncate</span>

eio\_futime
===========

Change file last access and modification times

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_futime</span> ( <span class="methodparam"><span
class="type">mixed</span> `$fd`</span> , <span class="methodparam"><span
class="type">float</span> `$atime`</span> , <span
class="methodparam"><span class="type">float</span> `$mtime`</span> \[,
<span class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_futime</span> changes file last access and
modification times.

### 参数

`fd`  
Stream, Socket resource, or numeric file descriptor, e.g. returned by
<span class="function">eio\_open</span>

`atime`  
Access time

`mtime`  
Modification time

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_futime</span> returns request resource on
success or **`FALSE`** on error.

### 参见

-   <span class="function">eio\_utime</span>

eio\_get\_event\_stream
=======================

Get stream representing a variable used in internal communications with
libeio

### 说明

<span class="type">mixed</span> <span
class="methodname">eio\_get\_event\_stream</span> ( <span
class="methodparam">void</span> )

<span class="function">eio\_get\_event\_stream</span> acquires stream
representing a variable used in internal communications with libeio.
Could be used to bind with some event loop provided by other PECL
extension, for example libevent.

### 参数

此函数没有参数。

### 返回值

<span class="function">eio\_get\_event\_stream</span> returns stream on
success; otherwise, **`NULL`**

### 范例

**示例 \#1 Using eio with libevent**

``` php
<?php
function my_eio_poll($fd, $events, $arg) {
    /* Some libevent regulation might go here .. */
    if (eio_nreqs()) {
        eio_poll();
    }
    /* .. and here */
}

function my_res_cb($d, $r) {
    var_dump($r); var_dump($d);
}

$base = event_base_new();
$event = event_new();

$fd = eio_get_event_stream();
var_dump($fd);

eio_nop(EIO_PRI_DEFAULT, "my_res_cb", "nop data");
eio_mkdir("/tmp/abc-eio-temp", 0750, EIO_PRI_DEFAULT, "my_res_cb", "mkdir data");
/* some other eio_* calls here ... */


// set event flags
event_set($event, $fd, EV_READ /*| EV_PERSIST*/, "my_eio_poll", array($event, $base));

// set event base 
event_base_set($event, $base);

// enable event
event_add($event);

// start event loop
event_base_loop($base);

/* The same will be available via buffered libevent interface */
?>
```

以上例程的输出类似于：

    int(3)
    int(0)
    string(8) "nop data"
    int(0)
    string(10) "mkdir data"

eio\_get\_last\_error
=====================

Returns string describing the last error associated with a request
resource

### 说明

<span class="type">string</span> <span
class="methodname">eio\_get\_last\_error</span> ( <span
class="methodparam"><span class="type">resource</span> `$req`</span> )

<span class="function">eio\_get\_last\_error</span> returns string
describing the last error associated with `req`.

### 参数

`req`  
The request resource

### 返回值

<span class="function">eio\_get\_last\_error</span> returns string
describing the last error associated with the request resource specified
by `req`.

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

eio\_grp\_add
=============

Adds a request to the request group

### 说明

<span class="type">void</span> <span
class="methodname">eio\_grp\_add</span> ( <span
class="methodparam"><span class="type">resource</span> `$grp`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$req`</span> )

<span class="function">eio\_grp\_add</span> adds a request to the
request group.

### 参数

`grp`  
The request group resource returned by <span
class="function">eio\_grp</span>

`req`  
The request resource

### 返回值

<span class="function">eio\_grp\_add</span> doesn't return a value.

### 范例

**示例 \#1 Grouping requests**

``` php
<?php
/*
 * Create a group request to open, read and close a file
 */

// Create temporary file and write some bytes to it
$temp_filename = dirname(__FILE__) ."/eio-file.tmp";
$fp = fopen($temp_filename, "w");
fwrite($fp, "some data");
fclose($fp);

/* Is called when the group requests are done */
function my_grp_done($data, $result) {
 var_dump($result == 0);
 @unlink($data);
}

/* Is called when eio_open() done */
function my_grp_file_opened_callback($data, $result) {
 global $grp;

 // $result should contain the file descriptor
 var_dump($result > 0);

 // Create eio_read() request and add it to the group
 // Pass file descriptor to the callback
 $req = eio_read($result, 4, 0,
   EIO_PRI_DEFAULT, "my_grp_file_read_callback", $result);
 eio_grp_add($grp, $req);
}

/* Is called when eio_read() done */
function my_grp_file_read_callback($data, $result) {
 global $grp;

 // Read bytes
 var_dump($result);

 // Create eio_close() request and add it to the group
 // $data should contain the file descriptor
 $req = eio_close($data);
 eio_grp_add($grp, $req);
}

// Create request group
$grp = eio_grp("my_grp_done", $temp_filename);
var_dump($grp);

// Create eio_open() request and add it to the group
$req = eio_open($temp_filename, EIO_O_RDWR | EIO_O_APPEND , NULL,
  EIO_PRI_DEFAULT, "my_grp_file_opened_callback", NULL);
eio_grp_add($grp, $req);

// Process requests
eio_event_loop();
?>
```

以上例程的输出类似于：

    resource(6) of type (EIO Group Descriptor)
    bool(true)
    string(4) "some"
    bool(true)

### 参见

-   <span class="function">eio\_grp</span>
-   <span class="function">eio\_grp\_cancel</span>
-   <span class="function">eio\_grp\_limit</span>

eio\_grp\_cancel
================

Cancels a request group

### 说明

<span class="type">void</span> <span
class="methodname">eio\_grp\_cancel</span> ( <span
class="methodparam"><span class="type">resource</span> `$grp`</span> )

<span class="function">eio\_grp\_cancel</span> cancels a group request
specified by `grp` request group resource.

### 参数

`grp`  
The request group resource returned by <span
class="function">eio\_grp</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">eio\_grp</span>
-   <span class="function">eio\_grp\_add</span>

eio\_grp\_limit
===============

Set group limit

### 说明

<span class="type">void</span> <span
class="methodname">eio\_grp\_limit</span> ( <span
class="methodparam"><span class="type">resource</span> `$grp`</span> ,
<span class="methodparam"><span class="type">int</span> `$limit`</span>
)

Limit number of requests in the request group.

### 参数

`grp`  
The request group resource.

`limit`  
Number of requests in the group.

### 返回值

没有返回值。

### 参见

-   <span class="function">eio\_grp\_add</span>

eio\_grp
========

Creates a request group

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_grp</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">string</span> `$data`<span
class="initializer"> = NULL</span></span> \] )

<span class="function">eio\_grp</span> creates a request group.

### 参数

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_grp</span> returns request group resource on
success or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">eio\_grp</span> example**

``` php
<?php
$temp_filename = dirname(__FILE__) ."/eio-file.tmp";
$fp = fopen($temp_filename, "w");
fwrite($fp, "some data");
fclose($fp);
$my_file_fd = NULL;

/* Is called when the group requests are done */
function my_grp_done($data, $result) {
 // Remove the file, if it still exists
 @unlink($data);
}

/* Is called when the temporary file is opened */
function my_grp_file_opened_callback($data, $result) {
 global $my_file_fd, $grp;

 $my_file_fd = $result;

 $req = eio_read($my_file_fd, 4, 0,
   EIO_PRI_DEFAULT, "my_grp_file_read_callback");
 eio_grp_add($grp, $req);
}

/* Is called when the file is read */
function my_grp_file_read_callback($data, $result) {
 global $my_file_fd, $grp;

 var_dump($result);

 // Create request to close the file
 $req = eio_close($my_file_fd);

 // Add request to the group
 eio_grp_add($grp, $req);
}

// Create request group
$grp = eio_grp("my_grp_done", $temp_filename);

// Create request
$req = eio_open($temp_filename, EIO_O_RDWR | EIO_O_APPEND , NULL,
  EIO_PRI_DEFAULT, "my_grp_file_opened_callback", NULL);

// Add request to the group
eio_grp_add($grp, $req);

// Process requests
eio_event_loop();
?>
```

以上例程的输出类似于：

    string(4) "some"

### 参见

-   <span class="function">eio\_grp\_cancel</span>
-   <span class="function">eio\_grp\_add</span>

eio\_init
=========

(Re-)initialize Eio

### 说明

<span class="type">void</span> <span class="methodname">eio\_init</span>
( <span class="methodparam">void</span> )

<span class="function">eio\_init</span> (re-)initializes Eio. It
allocates memory for internal structures of libeio and Eio itself. You
may call <span class="function">eio\_init</span> before using Eio
functions. Otherwise it will be called internally first time you invoke
an Eio function in a process.

**Warning**

本过时特性*将*肯定会在未来被*移除*。 Since Eio *1.1.0* <span
class="function">eio\_init</span> is deprecated. In Eio *1.0.0* because
of
<a href="http://pod.tst.eu/http://cvs.schmorp.de/libeio/eio.pod#FORK_SUPPORT" class="link external">» <em>libeio</em>'s restrictions</a>
you *must* call <span class="function">eio\_init</span> in child
process, if you fork one by any means. You have to avoid using Eio in
parent process, if you use it in childs.

### 参数

此函数没有参数。

### 返回值

没有返回值。

eio\_link
=========

Create a hardlink for file

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_link</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">string</span> `$new_path`</span>
\[, <span class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_link</span> creates a hardlink `new_path`
for a file specified by `path`.

### 参数

`path`  
Source file path.

`new_path`  
Target file path.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

### 范例

**示例 \#1 <span class="function">eio\_link</span> example**

``` php
<?php
$filename = dirname(__FILE__)."/symlink.dat";
touch($filename);
$link = dirname(__FILE__)."/symlink.link";
$hardlink = dirname(__FILE__)."/hardlink.link";

function my_hardlink_cb($data, $result) {
    global $link, $filename;
    var_dump(file_exists($data) && !is_link($data));
    @unlink($data);

    eio_symlink($filename, $link, EIO_PRI_DEFAULT, "my_symlink_cb", $link);
}

function my_symlink_cb($data, $result) {
    global $link, $filename;
    var_dump(file_exists($data) && is_link($data));

    if (!eio_readlink($data, EIO_PRI_DEFAULT, "my_readlink_cb", NULL)) {
        @unlink($link);
        @unlink($filename);
    }
}

function my_readlink_cb($data, $result) {
    global $filename, $link;
    var_dump($result);

    @unlink($link);
    @unlink($filename);
}

eio_link($filename, $hardlink, EIO_PRI_DEFAULT, "my_hardlink_cb", $hardlink);
eio_event_loop();
?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    string(%d) "%ssymlink.dat"

### 参见

-   <span class="function">eio\_symlink</span>

eio\_lstat
==========

Get file status

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_lstat</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">int</span> `$pri`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`<span class="initializer"> =
NULL</span></span> \] )

<span class="function">eio\_lstat</span> returns file status information
in `result` argument of `callback`

### 参数

`path`  
The file path

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_lstat</span> returns request resource on
success or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">eio\_lstat</span> example**

``` php
<?php
$tmp_filename = dirname(__FILE__). "/eio-file.tmp";
touch($tmp_filename);

function my_res_cb($data, $result) {
    var_dump($data);
    var_dump($result);
}

function my_open_cb($data, $result) {
    eio_close($result);
    eio_event_loop();

    @unlink($data);
}

eio_lstat($tmp_filename, EIO_PRI_DEFAULT, "my_res_cb", "eio_lstat");
eio_open($tmp_filename, EIO_O_RDONLY, NULL,
 EIO_PRI_DEFAULT, "my_open_cb", $tmp_filename);
eio_event_loop();
?>
```

以上例程的输出类似于：

    string(9) "eio_lstat"
    array(12) {
     ["st_dev"]=>
      int(2050)
      ["st_ino"]=>
      int(2099197)
      ["st_mode"]=>
      int(33188)
      ["st_nlink"]=>
      int(1)
      ["st_uid"]=>
      int(1000)
      ["st_gid"]=>
      int(100)
      ["st_rdev"]=>
      int(0)
      ["st_blksize"]=>
      int(4096)
      ["st_blocks"]=>
      int(0)
      ["st_atime"]=>
      int(1318235777)
      ["st_mtime"]=>
      int(1318235777)
      ["st_ctime"]=>
      int(1318235777)
    }

### 参见

-   <span class="function">eio\_stat</span>
-   <span class="function">eio\_fstat</span>

eio\_mkdir
==========

Create directory

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_mkdir</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">int</span> `$mode`</span> \[,
<span class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_mkdir</span> creates directory with
specified access `mode`.

### 参数

`path`  
Path for the new directory.

`mode`  
Access mode, e.g. 0755

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_mkdir</span> returns request resource on
success or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">eio\_mkdir</span> example**

``` php
<?php
$temp_dirname = "eio-temp-dir";

/* Is called when eio_mkdir() finishes */
function my_mkdir_callback($data, $result) {
 if ($result == 0 && is_dir($temp_dirname)
   && !is_readable($temp_dirname)
   && is_writable($temp_dirname)) {
  echo "eio_mkdir_ok";
 }

 // Remove directory
    if (file_exists($data))
        rmdir($temp_dirname);
}

// Create directory with access mode 0300
eio_mkdir($temp_dirname, 0300, EIO_PRI_DEFAULT, "my_mkdir_callback", $temp_dirname);
eio_event_loop();
?>
```

以上例程的输出类似于：

    eio_mkdir_ok

### 参见

-   <span class="function">eio\_rmdir</span>

eio\_mknod
==========

Create a special or ordinary file

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_mknod</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">int</span> `$mode`</span> , <span
class="methodparam"><span class="type">int</span> `$dev`</span> \[,
<span class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_mknod</span> creates ordinary or
special(often) file.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`path`  
Path for the new node(file).

`mode`  
Specifies both the permissions to use and the type of node to be
created. It should be a combination (using bitwise OR) of one of the
file types listed below and the permissions for the new node(e.g. 0640).
Possible file types are: **`EIO_S_IFREG`**(regular file),
**`EIO_S_IFCHR`**(character file), **`EIO_S_IFBLK`**(block special
file), **`EIO_S_IFIFO`**(FIFO - named pipe) and **`EIO_S_IFSOCK`**(UNIX
domain socket). To specify permissions *EIO\_S\_I\** constants could be
used.

`dev`  
If the file type is **`EIO_S_IFCHR`** or **`EIO_S_IFBLK`** then dev
specifies the major and minor numbers of the newly created device
special file. Otherwise `dev` ignored. See *mknod(2) man page for
details*.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_mknod</span> returns request resource on
success or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">eio\_mknod</span> example**

``` php
<?php
// FIFO name
$temp_filename = "/tmp/eio-temp-fifo";

/* Is called when eio_mknod() finishes */
function my_mknod_callback($data, $result) {
    $s = stat($data);
    var_dump($s);

    if ($result == 0) {
        echo "eio_mknod_ok";
    }

    @unlink($data);
}

eio_mknod($temp_filename, EIO_S_IFIFO, 0,
    EIO_PRI_DEFAULT, "my_mknod_callback", $temp_filename);
eio_event_loop();
?>
```

以上例程的输出类似于：

    array(26) {
      [0]=>
      int(17)
      [1]=>
      int(2337608)
      [2]=>
      int(4096)
      [3]=>
      int(1)
      [4]=>
      int(1000)
      [5]=>
      int(100)
      [6]=>
      int(0)
      [7]=>
      int(0)
      [8]=>
      int(1318241261)
      [9]=>
      int(1318241261)
      [10]=>
      int(1318241261)
      [11]=>
      int(4096)
      [12]=>
      int(0)
      ["dev"]=>
      int(17)
      ["ino"]=>
      int(2337608)
      ["mode"]=>
      int(4096)
      ["nlink"]=>
      int(1)
      ["uid"]=>
      int(1000)
      ["gid"]=>
      int(100)
      ["rdev"]=>
      int(0)
      ["size"]=>
      int(0)
      ["atime"]=>
      int(1318241261)
      ["mtime"]=>
      int(1318241261)
      ["ctime"]=>
      int(1318241261)
      ["blksize"]=>
      int(4096)
      ["blocks"]=>
      int(0)
    }
    eio_mknod_ok

### 参见

-   <span class="function">eio\_open</span>

eio\_nop
========

Does nothing, except go through the whole request cycle

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_nop</span> (\[ <span class="methodparam"><span
class="type">int</span> `$pri`<span class="initializer"> =
EIO\_PRI\_DEFAULT</span></span> \[, <span class="methodparam"><span
class="type">callable</span> `$callback`<span class="initializer"> =
NULL</span></span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`<span class="initializer"> =
NULL</span></span> \]\]\] )

<span class="function">eio\_nop</span> does nothing, except go through
the whole request cycle. Could be useful in debugging.

### 参数

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_nop</span> returns request resource on
success or **`FALSE`** on error.

### 参见

-   <span class="function">eio\_busy</span>

eio\_npending
=============

Returns number of finished, but unhandled requests

### 说明

<span class="type">int</span> <span
class="methodname">eio\_npending</span> ( <span
class="methodparam">void</span> )

<span class="function">eio\_npending</span> returns number of finished,
but unhandled requests

### 参数

此函数没有参数。

### 返回值

<span class="function">eio\_npending</span> returns number of finished,
but unhandled requests.

### 参见

-   <span class="function">eio\_nreqs</span>
-   <span class="function">eio\_nready</span>
-   <span class="function">eio\_nthreads</span>

eio\_nready
===========

Returns number of not-yet handled requests

### 说明

<span class="type">int</span> <span
class="methodname">eio\_nready</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

<span class="function">eio\_nready</span> returns number of not-yet
handled requests

### 参见

-   <span class="function">eio\_nreqs</span>
-   <span class="function">eio\_nready</span>
-   <span class="function">eio\_nthreads</span>

eio\_nreqs
==========

Returns number of requests to be processed

### 说明

<span class="type">int</span> <span class="methodname">eio\_nreqs</span>
( <span class="methodparam">void</span> )

<span class="function">eio\_nreqs</span> could be called in a custom
loop calling <span class="function">eio\_poll</span>.

### 参数

此函数没有参数。

### 返回值

<span class="function">eio\_nreqs</span> returns number of requests to
be processed.

### 范例

**示例 \#1 <span class="function">eio\_nreqs</span> example**

``` php
<?php
function res_cb($data, $result) {
    var_dump($data);
    var_dump($result);
}

eio_nop(EIO_PRI_DEFAULT, "res_cb", "1");
eio_nop(EIO_PRI_DEFAULT, "res_cb", "2");
eio_nop(EIO_PRI_DEFAULT, "res_cb", "3");

while (eio_nreqs()) {
    eio_poll();
}
?>
```

以上例程的输出类似于：

    string(1) "1"
    int(0)
    string(1) "3"
    int(0)
    string(1) "2"
    int(0)

### 参见

-   <span class="function">eio\_poll</span>
-   <span class="function">eio\_nready</span>

eio\_nthreads
=============

Returns number of threads currently in use

### 说明

<span class="type">int</span> <span
class="methodname">eio\_nthreads</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

<span class="function">eio\_nthreads</span> returns number of threads
currently in use.

### 参见

-   <span class="function">eio\_npending</span>
-   <span class="function">eio\_nready</span>
-   <span class="function">eio\_nreqs</span>
-   <span class="function">eio\_set\_max\_idle</span>
-   <span class="function">eio\_set\_max\_parallel</span>
-   <span class="function">eio\_set\_min\_parallel</span>

eio\_open
=========

Opens a file

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_open</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">int</span> `$flags`</span> ,
<span class="methodparam"><span class="type">int</span> `$mode`</span> ,
<span class="methodparam"><span class="type">int</span> `$pri`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`<span class="initializer"> =
NULL</span></span> \] )

<span class="function">eio\_open</span> opens file specified by `path`
in access mode `mode` with

### 参数

`path`  
Path of the file to be opened.

**Warning**
In some SAPIs(e.g. *PHP-FPM*) it could fail, if you don't specify full
path.

`flags`  
One of *EIO\_O\_\** constants, or their combinations. *EIO\_O\_\**
constants have the same meaning, as their corresponding *O\_\**
counterparts defined in *fnctl.h* C header file. Default is
**`EIO_O_RDWR`**.

`mode`  
One of *EIO\_S\_I\** constants, or their combination (via bitwise OR
operator). The constants have the same meaning as their *S\_I\**
counterparts defined in
<a href="http://pubs.opengroup.org/onlinepubs/9699919799/basedefs/sys_stat.h.html" class="link external">» sys/stat.h</a>
C header file. Required, if a file is created. Otherwise ignored.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_open</span> returns file descriptor in
`result` argument of `callback` on success; otherwise, `result` is equal
to **`-1`**.

### 范例

**示例 \#1 <span class="function">eio\_open</span> example**

``` php
<?php
$temp_filename = "eio-temp-file.tmp";

/* Is called when eio_close() finishes */
function my_close_cb($data, $result) {
 // Zero indicates success
    var_dump($result == 0);
 @unlink($data);
}

/* Is called when eio_open() finishes */
function my_file_opened_callback($data, $result) {
 // $result should contain the file descriptor
    var_dump($result > 0);

    if ($result > 0) {
  // Close the file
        eio_close($result, EIO_PRI_DEFAULT, "my_close_cb", $data);
        eio_event_loop();
    }
}

// Create new file for reading and writing
// Deny group and others to do anything with that file
eio_open($temp_filename, EIO_O_CREAT | EIO_O_RDWR, EIO_S_IRUSR | EIO_S_IWUSR,
  EIO_PRI_DEFAULT, "my_file_opened_callback", $temp_filename);
eio_event_loop();
?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)

### 参见

-   <span class="function">eio\_mknod</span>

eio\_poll
=========

Can be to be called whenever there are pending requests that need
finishing

### 说明

<span class="type">int</span> <span class="methodname">eio\_poll</span>
( <span class="methodparam">void</span> )

<span class="function">eio\_poll</span> can be used to implement special
event loop. For this <span class="function">eio\_nreqs</span> could be
used to test if there are unprocessed requests.

> **Note**:
>
> Applicable only when implementing userspace event loop.

### 参数

此函数没有参数。

### 返回值

If any request invocation returns a non-zero value, returns that value.
Otherwise, it returns **`0`**.

### 范例

**示例 \#1 <span class="function">eio\_poll</span> example**

``` php
<?php
function res_cb($data, $result) {
    var_dump($data);
    var_dump($result);
}

eio_nop(EIO_PRI_DEFAULT, "res_cb", "1");
eio_nop(EIO_PRI_DEFAULT, "res_cb", "2");
eio_nop(EIO_PRI_DEFAULT, "res_cb", "3");

while (eio_nreqs()) {
    // Some specific IPC or so
    eio_poll();
}
?>
```

以上例程的输出类似于：

    string(1) "1"
    int(0)
    string(1) "3"
    int(0)
    string(1) "2"
    int(0)

### 参见

-   <span class="function">eio\_nreqs</span>

eio\_read
=========

Read from a file descriptor at given offset

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_read</span> ( <span class="methodparam"><span
class="type">mixed</span> `$fd`</span> , <span class="methodparam"><span
class="type">int</span> `$length`</span> , <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$pri`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`<span class="initializer"> =
NULL</span></span> \] )

<span class="function">eio\_read</span> reads up to `length` bytes from
`fd` file descriptor at `offset`. The read bytes are stored in `result`
argument of `callback`.

### 参数

`fd`  
Stream, Socket resource, or numeric file descriptor

`length`  
Maximum number of bytes to read.

`offset`  
Offset within the file.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_read</span> stores read bytes in `result`
argument of `callback` function.

### 范例

**示例 \#1 <span class="function">eio\_read</span> example**

``` php
<?php
// Open a temporary file and write some bytes there
$temp_filename = "eio-temp-file.tmp";
$fp = fopen($temp_filename, "w");
fwrite($fp, "1234567890");
fclose($fp);

/* Is called when eio_read() is done */
function my_read_cb($data, $result) {
    global $temp_filename;

 // Output read bytes
    var_dump($result);

 // Close file
    eio_close($data);
    eio_event_loop();

 // Remove temporary file
    @unlink($temp_filename);
}

/* Is called when eio_open() is done */
function my_file_opened_callback($data, $result) {
 // $result should contain the file descriptor
    if ($result > 0) {
  // Read 5 bytes starting from third
        eio_read($result, 5, 2, EIO_PRI_DEFAULT, "my_read_cb", $result);
        eio_event_loop();
    } else {
  // eio_open() failed
        unlink($data);
    }
}

// Open the file for reading and writing
eio_open($temp_filename, EIO_O_RDWR, NULL,
    EIO_PRI_DEFAULT, "my_file_opened_callback", $temp_filename);
eio_event_loop();
?>
```

以上例程的输出类似于：

    string(5) "34567"

### 参见

-   <span class="function">eio\_open</span>
-   <span class="function">eio\_write</span>
-   <span class="function">eio\_close</span>
-   <span class="function">eio\_event\_loop</span>

eio\_readahead
==============

Perform file readahead into page cache

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_readahead</span> ( <span
class="methodparam"><span class="type">mixed</span> `$fd`</span> , <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$length`</span>
\[, <span class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_readahead</span> populates the page cache
with data from a file so that subsequent reads from that file will not
block on disk I/O. See *READAHEAD(2)* man page for details.

### 参数

`fd`  
Stream, Socket resource, or numeric file descriptor

`offset`  
Starting point from which data is to be read.

`length`  
Number of bytes to be read.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_readahead</span> returns request resource on
success or **`FALSE`** on error.

eio\_readdir
============

Reads through a whole directory

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_readdir</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">int</span> `$flags`</span> ,
<span class="methodparam"><span class="type">int</span> `$pri`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">string</span> `$data`<span class="initializer"> =
NULL</span></span> \] )

Reads through a whole directory(via the *opendir*, *readdir* and
*closedir* system calls) and returns either the names or an array in
`result` argument of `callback` function, depending on the `flags`
argument.

### 参数

`path`  
Directory path.

`flags`  
Combination of *EIO\_READDIR\_\** constants.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_readdir</span> returns request resource on
success, or **`FALSE`** on error. Sets `result` argument of `callback`
function according to `flags`:

**`EIO_READDIR_DENTS`** (<span class="type">int</span>)  
<span class="simpara"> <span class="function">eio\_readdir</span> flag.
If specified, the result argument of the callback becomes an array with
the following keys: *'names'* - array of directory names *'dents'* -
array of *struct eio\_dirent*-like arrays having the following keys
each: *'name'* - the directory name; *'type'* - one of *EIO\_DT\_\**
constants; *'inode'* - the inode number, if available, otherwise
unspecified; </span>

**`EIO_READDIR_DIRS_FIRST`** (<span class="type">int</span>)  
<span class="simpara"> When this flag is specified, the names will be
returned in an order where likely directories come first, in optimal
stat order. </span>

**`EIO_READDIR_STAT_ORDER`** (<span class="type">int</span>)  
<span class="simpara"> When this flag is specified, then the names will
be returned in an order suitable for *stat*'ing each one. When planning
to <span class="function">stat</span> all files in the given directory,
the returned order will likely be fastest. </span>

**`EIO_READDIR_FOUND_UNKNOWN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

Node types:

**`EIO_DT_UNKNOWN`** (<span class="type">int</span>)  
<span class="simpara"> Unknown node type(very common). Further <span
class="function">stat</span> needed. </span>

**`EIO_DT_FIFO`** (<span class="type">int</span>)  
<span class="simpara"> FIFO node type </span>

**`EIO_DT_CHR`** (<span class="type">int</span>)  
<span class="simpara"> Node type </span>

**`EIO_DT_MPC`** (<span class="type">int</span>)  
<span class="simpara"> Multiplexed char device (v7+coherent) node type
</span>

**`EIO_DT_DIR`** (<span class="type">int</span>)  
<span class="simpara"> Directory node type </span>

**`EIO_DT_NAM`** (<span class="type">int</span>)  
<span class="simpara"> Xenix special named file node type </span>

**`EIO_DT_BLK`** (<span class="type">int</span>)  
<span class="simpara"> Node type </span>

**`EIO_DT_MPB`** (<span class="type">int</span>)  
<span class="simpara"> Multiplexed block device (v7+coherent) </span>

**`EIO_DT_REG`** (<span class="type">int</span>)  
<span class="simpara"> Node type </span>

**`EIO_DT_NWK`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_DT_CMP`** (<span class="type">int</span>)  
<span class="simpara"> HP-UX network special node type </span>

**`EIO_DT_LNK`** (<span class="type">int</span>)  
<span class="simpara"> Link node type </span>

**`EIO_DT_SOCK`** (<span class="type">int</span>)  
<span class="simpara"> Socket node type </span>

**`EIO_DT_DOOR`** (<span class="type">int</span>)  
<span class="simpara"> Solaris door node type </span>

**`EIO_DT_WHT`** (<span class="type">int</span>)  
<span class="simpara"> Node type </span>

**`EIO_DT_MAX`** (<span class="type">int</span>)  
<span class="simpara"> Highest node type value </span>

### 范例

**示例 \#1 <span class="function">eio\_readdir</span> example**

``` php
<?php
/* Is called when eio_readdir() finishes */
function my_readdir_callback($data, $result) {
    echo __FUNCTION__, " called\n";
    echo "data: "; var_dump($data);
    echo "result: "; var_dump($result);
    echo "\n";
}

eio_readdir("/var/spool/news", EIO_READDIR_STAT_ORDER | EIO_READDIR_DIRS_FIRST,
  EIO_PRI_DEFAULT, "my_readdir_callback");
eio_event_loop();
?>
```

以上例程的输出类似于：

    my_readdir_callback called
    data: NULL
    result: array(2) {
     ["names"]=>
      array(7) {
       [0]=>
        string(7) "archive"
        [1]=>
        string(8) "articles"
        [2]=>
        string(8) "incoming"
        [3]=>
        string(7) "innfeed"
        [4]=>
        string(8) "outgoing"
        [5]=>
        string(8) "overview"
        [6]=>
        string(3) "tmp"
      }
     ["dents"]=>
      array(7) {
       [0]=>
        array(3)
        {
         ["name"]=>
          string(7)
          "archive"
          ["type"]=>
          int(4)
          ["inode"]=>
          int(393265)
        }
       [1]=>
        array(3)
        {
         ["name"]=>
          string(8)
          "articles"
          ["type"]=>
          int(4)
          ["inode"]=>
          int(393266)
        }
       [2]=>
        array(3)
        {
         ["name"]=>
          string(8)
          "incoming"
          ["type"]=>
          int(4)
          ["inode"]=>
          int(393267)
        }
       [3]=>
        array(3)
        {
         ["name"]=>
          string(7)
          "innfeed"
          ["type"]=>
          int(4)
          ["inode"]=>
          int(393269)
        }
       [4]=>
        array(3)
        {
         ["name"]=>
          string(8)
          "outgoing"
          ["type"]=>
          int(4)
          ["inode"]=>
          int(393270)
        }
       [5]=>
        array(3)
        {
         ["name"]=>
          string(8)
          "overview"
          ["type"]=>
          int(4)
          ["inode"]=>
          int(393271)
        }
       [6]=>
        array(3)
        {
         ["name"]=>
          string(3)
          "tmp"
          ["type"]=>
          int(4)
          ["inode"]=>
          int(393272)
        }
      }
    }

eio\_readlink
=============

Read value of a symbolic link

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_readlink</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">int</span> `$pri`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">string</span> `$data`<span class="initializer"> =
NULL</span></span> \] )

### 参数

`path`  
Source symbolic link path

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_readlink</span> returns request resource on
success or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">eio\_readlink</span> example**

``` php
<?php
$filename = dirname(__FILE__)."/symlink.dat";
touch($filename);
$link = dirname(__FILE__)."/symlink.link";
$hardlink = dirname(__FILE__)."/hardlink.link";

function my_hardlink_cb($data, $result) {
    global $link, $filename;
    var_dump(file_exists($data) && !is_link($data));
    @unlink($data);

    eio_symlink($filename, $link, EIO_PRI_DEFAULT, "my_symlink_cb", $link);
}

function my_symlink_cb($data, $result) {
    global $link, $filename;
    var_dump(file_exists($data) && is_link($data));

    if (!eio_readlink($data, EIO_PRI_DEFAULT, "my_readlink_cb", NULL)) {
        @unlink($link);
        @unlink($filename);
    }
}

function my_readlink_cb($data, $result) {
    global $filename, $link;
    var_dump($result);

    @unlink($link);
    @unlink($filename);
}

eio_link($filename, $hardlink, EIO_PRI_DEFAULT, "my_hardlink_cb", $hardlink);
eio_event_loop();
?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    string(16) "/tmp/symlink.dat"

### 参见

-   <span class="function">eio\_symlink</span>

eio\_realpath
=============

Get the canonicalized absolute pathname

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_realpath</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">int</span> `$pri`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">string</span> `$data`<span class="initializer"> =
NULL</span></span> \] )

<span class="function">eio\_realpath</span> returns the canonicalized
absolute pathname in `result` argument of `callback` function.

### 参数

`path`  
Short pathname

`pri`  

`callback`  

`data`  

### 返回值

### 范例

**示例 \#1 <span class="function">eio\_realpath</span> example**

``` php
<?php
var_dump(getcwd());

function my_realpath_allback($data, $result) {
    var_dump($result);
}

eio_realpath("../", EIO_PRI_DEFAULT, "my_realpath_allback");
eio_event_loop();
?>
```

以上例程的输出类似于：

    string(12) "/home/ruslan"
    string(5) "/home"

eio\_rename
===========

Change the name or location of a file

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_rename</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">string</span> `$new_path`</span>
\[, <span class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_rename</span> renames or moves a file to new
location.

### 参数

`path`  
Source path

`new_path`  
Target path

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_rename</span> returns request resource on
success or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">eio\_rename</span> example**

``` php
<?php
$filename = dirname(__FILE__)."/eio-temp-file.dat";
touch($filename);
$new_filename = dirname(__FILE__)."/eio-temp-file-new.dat";

function my_rename_cb($data, $result) {
    global $filename, $new_filename;

    if ($result == 0 && !file_exists($filename) && file_exists($new_filename)) {
        @unlink($new_filename);
        echo "eio_rename_ok";
    } else {
        @unlink($filename);
    }
}

eio_rename($filename, $new_filename, EIO_PRI_DEFAULT, "my_rename_cb", $filename);
eio_event_loop();
?>
```

以上例程的输出类似于：

    eio_rename_ok

eio\_rmdir
==========

Remove a directory

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_rmdir</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_rmdir</span> removes a directory.

### 参数

`path`  
Directory path

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_rmdir</span> returns request resource on
success or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">eio\_rmdir</span> example**

``` php
<?php
$temp_dirname = "eio-temp-dir";
mkdir($temp_dirname);

function my_rmdir_callback($data, $result) {
    if ($result == 0 && !file_exists($data)) {
        echo "eio_rmdir_ok";
    } else if (file_exists($data)) {
        rmdir($data);
    }
}


eio_rmdir($temp_dirname, EIO_PRI_DEFAULT, "my_rmdir_callback", $temp_dirname);
eio_event_loop();
?>
```

以上例程的输出类似于：

    eio_rmdir_ok

### 参见

-   <span class="function">eio\_mkdir</span>

eio\_seek
=========

Repositions the offset of the open file associated with the `fd`
argument to the argument `offset` according to the directive `whence`

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_seek</span> ( <span class="methodparam"><span
class="type">mixed</span> `$fd`</span> , <span class="methodparam"><span
class="type">int</span> `$offset`</span> , <span
class="methodparam"><span class="type">int</span> `$whence`</span> \[,
<span class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_seek</span> repositions the offset of the
open file associated with stream, Socket resource, or file descriptor
specified by `fd` to the argument `offset` according to the directive
`whence` as follows:

-   **`EIO_SEEK_SET`** - Set position equal to `offset` bytes.
-   **`EIO_SEEK_CUR`** - Set position to current location plus `offset`.
-   **`EIO_SEEK_END`** - Set position to end-of-file plus `offset`.

### 参数

`fd`  
Stream, Socket resource, or numeric file descriptor

`offset`  
Starting point from which data is to be read.

`length`  
Number of bytes to be read.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_seek</span> returns request resource on
success or **`FALSE`** on error.

eio\_sendfile
=============

Transfer data between file descriptors

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_sendfile</span> ( <span
class="methodparam"><span class="type">mixed</span> `$out_fd`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$in_fd`</span> , <span class="methodparam"><span
class="type">int</span> `$offset`</span> , <span
class="methodparam"><span class="type">int</span> `$length`</span> \[,
<span class="methodparam"><span class="type">int</span> `$pri`</span>
\[, <span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">string</span> `$data`</span> \]\]\] )

<span class="function">eio\_sendfile</span> copies data between one file
descriptor and another. See *SENDFILE(2)* man page for details.

### 参数

`out_fd`  
Output stream, Socket resource, or file descriptor. Should be opened for
writing.

`in_fd`  
Input stream, Socket resource, or file descriptor. Should be opened for
reading.

`offset`  
Offset within the source file.

`length`  
Number of bytes to copy.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_sendfile</span> returns request resource on
success or **`FALSE`** on error.

eio\_set\_max\_idle
===================

Set maximum number of idle threads

### 说明

<span class="type">void</span> <span
class="methodname">eio\_set\_max\_idle</span> ( <span
class="methodparam"><span class="type">int</span> `$nthreads`</span> )

### 参数

`nthreads`  
Number of idle threads.

### 返回值

没有返回值。

### 参见

-   <span class="function">eio\_nthreads</span>
-   <span class="function">eio\_set\_min\_parallel</span>
-   <span class="function">eio\_set\_max\_parallel</span>

eio\_set\_max\_parallel
=======================

Set maximum parallel threads

### 说明

<span class="type">void</span> <span
class="methodname">eio\_set\_max\_parallel</span> ( <span
class="methodparam"><span class="type">int</span> `$nthreads`</span> )

### 参数

`nthreads`  
Number of parallel threads

### 返回值

没有返回值。

### 参见

-   <span class="function">eio\_nthreads</span>
-   <span class="function">eio\_set\_max\_idle</span>
-   <span class="function">eio\_set\_min\_parallel</span>

eio\_set\_max\_poll\_reqs
=========================

Set maximum number of requests processed in a poll

### 说明

<span class="type">void</span> <span
class="methodname">eio\_set\_max\_poll\_reqs</span> ( <span
class="methodparam"><span class="type">int</span> `$nreqs`</span> )

### 参数

`nreqs`  
Number of requests

### 返回值

没有返回值。

eio\_set\_max\_poll\_time
=========================

Set maximum poll time

### 说明

<span class="type">void</span> <span
class="methodname">eio\_set\_max\_poll\_time</span> ( <span
class="methodparam"><span class="type">float</span> `$nseconds`</span> )

Polling stops, if poll took longer than `nseconds` seconds.

### 参数

`nseconds`  
Number of seconds

### 返回值

没有返回值。

eio\_set\_min\_parallel
=======================

Set minimum parallel thread number

### 说明

<span class="type">void</span> <span
class="methodname">eio\_set\_min\_parallel</span> ( <span
class="methodparam"><span class="type">string</span> `$nthreads`</span>
)

### 参数

`nthreads`  
Number of parallel threads.

### 返回值

没有返回值。

### 参见

-   <span class="function">eio\_nthreads</span>
-   <span class="function">eio\_set\_max\_idle</span>
-   <span class="function">eio\_set\_max\_parallel</span>

eio\_stat
=========

Get file status

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_stat</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">int</span> `$pri`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`<span class="initializer"> =
NULL</span></span> \] )

<span class="function">eio\_stat</span> returns file status information
in `result` argument of `callback`

### 参数

`path`  
The file path

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_stat</span> returns request resource on
success or **`FALSE`** on error. On success assigns `result` argument of
`callback` to an array.

### 范例

**示例 \#1 <span class="function">eio\_stat</span> example**

``` php
<?php
$tmp_filename = "eio-file.tmp";
touch($tmp_filename);

function my_res_cb($data, $result) {
    var_dump($data);
    var_dump($result);
}

function my_open_cb($data, $result) {
    eio_close($result);
    eio_event_loop();

    @unlink($data);
}

eio_stat($tmp_filename, EIO_PRI_DEFAULT, "my_res_cb", "eio_stat");
eio_open($tmp_filename, EIO_O_RDONLY, NULL,
 EIO_PRI_DEFAULT, "my_open_cb", $tmp_filename);
eio_event_loop();
?>
```

以上例程的输出类似于：

    string(8) "eio_stat"
    array(12) {
      ["st_dev"]=>
      int(2050)
      ["st_ino"]=>
      int(2489173)
      ["st_mode"]=>
      int(33188)
      ["st_nlink"]=>
      int(1)
      ["st_uid"]=>
      int(1000)
      ["st_gid"]=>
      int(100)
      ["st_rdev"]=>
      int(0)
      ["st_blksize"]=>
      int(4096)
      ["st_blocks"]=>
      int(0)
      ["st_atime"]=>
      int(1318250380)
      ["st_mtime"]=>
      int(1318250380)
      ["st_ctime"]=>
      int(1318250380)
    }

### 参见

-   <span class="function">eio\_lstat</span>
-   <span class="function">eio\_fstat</span>

eio\_statvfs
============

Get file system statistics

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_statvfs</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">int</span> `$pri`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`</span> \] )

<span class="function">eio\_statvfs</span> returns file system
statistics information in `result` argument of `callback`

### 参数

`path`  
Pathname of any file within the mounted file system

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_statvfs</span> returns request resource on
success or **`FALSE`** on error. On success assigns `result` argument of
`callback` to an array.

### 范例

**示例 \#1 <span class="function">eio\_statvfs</span> example**

``` php
<?php
$tmp_filename = '/tmp/eio-file.tmp';
touch($tmp_filename);

function my_statvfs_callback($data, $result) {
    var_dump($data);
    var_dump($result);

 @unlink($data);
}

eio_statvfs($tmp_filename, EIO_PRI_DEFAULT, "my_statvfs_callback", $tmp_filename);
eio_event_loop();
?>
```

以上例程的输出类似于：

    string(17) "/tmp/eio-file.tmp"
    array(11) {
      ["f_bsize"]=>
      int(4096)
      ["f_frsize"]=>
      int(4096)
      ["f_blocks"]=>
      int(262144)
      ["f_bfree"]=>
      int(262111)
      ["f_bavail"]=>
      int(262111)
      ["f_files"]=>
      int(1540815)
      ["f_ffree"]=>
      int(1540743)
      ["f_favail"]=>
      int(1540743)
      ["f_fsid"]=>
      int(0)
      ["f_flag"]=>
      int(4102)
      ["f_namemax"]=>
      int(255)
    }

eio\_symlink
============

Create a symbolic link

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_symlink</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">string</span> `$new_path`</span>
\[, <span class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_symlink</span> creates a symbolic link
`new_path` to `path`.

### 参数

`path`  
Source path

`new_path`  
Target path

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_symlink</span> returns request resource on
success or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">eio\_symlink</span> example**

``` php
<?php
$filename = dirname(__FILE__)."/symlink.dat";
touch($filename);
$link = dirname(__FILE__)."/symlink.link";

function my_symlink_cb($data, $result) {
    global $link, $filename;
    var_dump(file_exists($data) && is_link($data));

    if (!eio_readlink($data, EIO_PRI_DEFAULT, "my_readlink_cb", NULL)) {
        @unlink($link);
        @unlink($filename);
    }
}

function my_readlink_cb($data, $result) {
    global $filename, $link;
    var_dump($result);

    @unlink($link);
    @unlink($filename);
}

eio_symlink($filename, $link, EIO_PRI_DEFAULT, "my_symlink_cb", $link);
eio_event_loop();
?>
```

以上例程的输出类似于：

    bool(true)
    string(16) "/tmp/symlink.dat"

### 参见

-   <span class="function">eio\_link</span>

eio\_sync\_file\_range
======================

Sync a file segment with disk

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_sync\_file\_range</span> ( <span
class="methodparam"><span class="type">mixed</span> `$fd`</span> , <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$nbytes`</span>
, <span class="methodparam"><span class="type">int</span>
`$flags`</span> \[, <span class="methodparam"><span
class="type">int</span> `$pri`<span class="initializer"> =
EIO\_PRI\_DEFAULT</span></span> \[, <span class="methodparam"><span
class="type">callable</span> `$callback`<span class="initializer"> =
NULL</span></span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`<span class="initializer"> =
NULL</span></span> \]\]\] )

<span class="function">eio\_sync\_file\_range</span> permits fine
control when synchronizing the open file referred to by the file
descriptor `fd` with disk.

### 参数

`fd`  
File descriptor

`offset`  
The starting byte of the file range to be synchronized

`nbytes`  
Specifies the length of the range to be synchronized, in bytes. If
`nbytes` is zero, then all bytes from `offset` through to the end of
file are synchronized.

`flags`  
A bit-mask. Can include any of the following values:
**`EIO_SYNC_FILE_RANGE_WAIT_BEFORE`**, **`EIO_SYNC_FILE_RANGE_WRITE`**,
**`EIO_SYNC_FILE_RANGE_WAIT_AFTER`**. These flags have the same meaning
as their *SYNC\_FILE\_RANGE\_\** counterparts(see *SYNC\_FILE\_RANGE(2)*
man page).

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_sync\_file\_range</span> returns request
resource on success or **`FALSE`** on error.

eio\_sync
=========

Commit buffer cache to disk

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_sync</span> (\[ <span class="methodparam"><span
class="type">int</span> `$pri`<span class="initializer"> =
EIO\_PRI\_DEFAULT</span></span> \[, <span class="methodparam"><span
class="type">callable</span> `$callback`<span class="initializer"> =
NULL</span></span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`<span class="initializer"> =
NULL</span></span> \]\]\] )

### 参数

此函数没有参数。

### 返回值

<span class="function">eio\_sync</span> returns request resource on
success or **`FALSE`** on error.

eio\_syncfs
===========

Calls Linux' syncfs syscall, if available

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_syncfs</span> ( <span class="methodparam"><span
class="type">mixed</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

### 参数

`fd`  
File descriptor

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_syncfs</span> returns request resource on
success or **`FALSE`** on error.

eio\_truncate
=============

Truncate a file

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_truncate</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\]\] )

<span class="function">eio\_truncate</span> causes the regular file
named by `path` to be truncated to a size of precisely `length` bytes

### 参数

`path`  
File path

`offset`  
Offset from beginning of the file.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_busy</span> returns request resource on
success or **`FALSE`** on error.

### 参见

-   <span class="function">eio\_ftruncate</span>

eio\_unlink
===========

Delete a name and possibly the file it refers to

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_unlink</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\] )

<span class="function">eio\_unlink</span> deletes a name from the file
system.

### 参数

`path`  
Path to file

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_unlink</span> returns request resource on
success or **`FALSE`** on error.

eio\_utime
==========

Change file last access and modification times

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_utime</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">float</span> `$atime`</span> ,
<span class="methodparam"><span class="type">float</span>
`$mtime`</span> \[, <span class="methodparam"><span
class="type">int</span> `$pri`<span class="initializer"> =
EIO\_PRI\_DEFAULT</span></span> \[, <span class="methodparam"><span
class="type">callable</span> `$callback`<span class="initializer"> =
NULL</span></span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`<span class="initializer"> =
NULL</span></span> \]\]\] )

### 参数

`path`  
Path to the file.

`atime`  
Access time

`mtime`  
Modification time

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_utime</span> returns request resource on
success or **`FALSE`** on error.

### 参见

-   <span class="function">eio\_futime</span>

eio\_write
==========

Write to file

### 说明

<span class="type">resource</span> <span
class="methodname">eio\_write</span> ( <span class="methodparam"><span
class="type">mixed</span> `$fd`</span> , <span class="methodparam"><span
class="type">string</span> `$str`</span> \[, <span
class="methodparam"><span class="type">int</span> `$length`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$pri`<span
class="initializer"> = EIO\_PRI\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">callable</span> `$callback`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$data`<span
class="initializer"> = NULL</span></span> \]\]\]\]\] )

<span class="function">eio\_write</span> writes up to `length` bytes
from `str` at `offset` offset from the beginning of the file.

### 参数

`fd`  
Stream, Socket resource, or numeric file descriptor, e.g. returned by
<span class="function">eio\_open</span>

`str`  
Source string

`length`  
Maximum number of bytes to write.

`offset`  
Offset from the beginning of file.

`pri`  
请求的优先级：**`EIO_PRI_DEFAULT`**，**`EIO_PRI_MIN`**，**`EIO_PRI_MAX`**
或 **`NULL`**。如果是 **`NULL`**，`pri` 将设为 **`EIO_PRI_DEFAULT`**。

`callback`  
`callback` 函数在请求完成时被调用。其应匹配一下原型：

``` php
void callback(mixed $data, int $result[, resource $req]);
```

`data`  
传递给请求的用户数据。

`result`  
针对请求的结果的值。通常是相应的系统调用返回的值。

`req`  
可选的请求资源，可被 <span class="function">eio\_get\_last\_error</span>
之类的函数使用。

`data`  
Arbitrary variable passed to `callback`.

### 返回值

<span class="function">eio\_write</span> returns request resource on
success or **`FALSE`** on error.

### 参见

-   <span class="function">eio\_open</span>

**目录**

-   [eio\_busy](/ref/eio.html#eio_busy) — Artificially increase load.
    Could be useful in tests, benchmarking
-   [eio\_cancel](/ref/eio.html#eio_cancel) — Cancels a request
-   [eio\_chmod](/ref/eio.html#eio_chmod) — Change file/directory
    permissions
-   [eio\_chown](/ref/eio.html#eio_chown) — Change file/directory
    permissions
-   [eio\_close](/ref/eio.html#eio_close) — Close file
-   [eio\_custom](/ref/eio.html#eio_custom) — Execute custom request
    like any other eio\_\* call
-   [eio\_dup2](/ref/eio.html#eio_dup2) — Duplicate a file descriptor
-   [eio\_event\_loop](/ref/eio.html#eio_event_loop) — Polls libeio
    until all requests proceeded
-   [eio\_fallocate](/ref/eio.html#eio_fallocate) — Allows the caller to
    directly manipulate the allocated disk space for a file
-   [eio\_fchmod](/ref/eio.html#eio_fchmod) — Change file permissions
-   [eio\_fchown](/ref/eio.html#eio_fchown) — Change file ownership
-   [eio\_fdatasync](/ref/eio.html#eio_fdatasync) — Synchronize a file's
    in-core state with storage device
-   [eio\_fstat](/ref/eio.html#eio_fstat) — Get file status
-   [eio\_fstatvfs](/ref/eio.html#eio_fstatvfs) — Get file system
    statistics
-   [eio\_fsync](/ref/eio.html#eio_fsync) — Synchronize a file's in-core
    state with storage device
-   [eio\_ftruncate](/ref/eio.html#eio_ftruncate) — Truncate a file
-   [eio\_futime](/ref/eio.html#eio_futime) — Change file last access
    and modification times
-   [eio\_get\_event\_stream](/ref/eio.html#eio_get_event_stream) — Get
    stream representing a variable used in internal communications with
    libeio
-   [eio\_get\_last\_error](/ref/eio.html#eio_get_last_error) — Returns
    string describing the last error associated with a request resource
-   [eio\_grp\_add](/ref/eio.html#eio_grp_add) — Adds a request to the
    request group
-   [eio\_grp\_cancel](/ref/eio.html#eio_grp_cancel) — Cancels a request
    group
-   [eio\_grp\_limit](/ref/eio.html#eio_grp_limit) — Set group limit
-   [eio\_grp](/ref/eio.html#eio_grp) — Creates a request group
-   [eio\_init](/ref/eio.html#eio_init) — (Re-)initialize Eio
-   [eio\_link](/ref/eio.html#eio_link) — Create a hardlink for file
-   [eio\_lstat](/ref/eio.html#eio_lstat) — Get file status
-   [eio\_mkdir](/ref/eio.html#eio_mkdir) — Create directory
-   [eio\_mknod](/ref/eio.html#eio_mknod) — Create a special or ordinary
    file
-   [eio\_nop](/ref/eio.html#eio_nop) — Does nothing, except go through
    the whole request cycle
-   [eio\_npending](/ref/eio.html#eio_npending) — Returns number of
    finished, but unhandled requests
-   [eio\_nready](/ref/eio.html#eio_nready) — Returns number of not-yet
    handled requests
-   [eio\_nreqs](/ref/eio.html#eio_nreqs) — Returns number of requests
    to be processed
-   [eio\_nthreads](/ref/eio.html#eio_nthreads) — Returns number of
    threads currently in use
-   [eio\_open](/ref/eio.html#eio_open) — Opens a file
-   [eio\_poll](/ref/eio.html#eio_poll) — Can be to be called whenever
    there are pending requests that need finishing
-   [eio\_read](/ref/eio.html#eio_read) — Read from a file descriptor at
    given offset
-   [eio\_readahead](/ref/eio.html#eio_readahead) — Perform file
    readahead into page cache
-   [eio\_readdir](/ref/eio.html#eio_readdir) — Reads through a whole
    directory
-   [eio\_readlink](/ref/eio.html#eio_readlink) — Read value of a
    symbolic link
-   [eio\_realpath](/ref/eio.html#eio_realpath) — Get the canonicalized
    absolute pathname
-   [eio\_rename](/ref/eio.html#eio_rename) — Change the name or
    location of a file
-   [eio\_rmdir](/ref/eio.html#eio_rmdir) — Remove a directory
-   [eio\_seek](/ref/eio.html#eio_seek) — Repositions the offset of the
    open file associated with the fd argument to the argument offset
    according to the directive whence
-   [eio\_sendfile](/ref/eio.html#eio_sendfile) — Transfer data between
    file descriptors
-   [eio\_set\_max\_idle](/ref/eio.html#eio_set_max_idle) — Set maximum
    number of idle threads
-   [eio\_set\_max\_parallel](/ref/eio.html#eio_set_max_parallel) — Set
    maximum parallel threads
-   [eio\_set\_max\_poll\_reqs](/ref/eio.html#eio_set_max_poll_reqs) —
    Set maximum number of requests processed in a poll
-   [eio\_set\_max\_poll\_time](/ref/eio.html#eio_set_max_poll_time) —
    Set maximum poll time
-   [eio\_set\_min\_parallel](/ref/eio.html#eio_set_min_parallel) — Set
    minimum parallel thread number
-   [eio\_stat](/ref/eio.html#eio_stat) — Get file status
-   [eio\_statvfs](/ref/eio.html#eio_statvfs) — Get file system
    statistics
-   [eio\_symlink](/ref/eio.html#eio_symlink) — Create a symbolic link
-   [eio\_sync\_file\_range](/ref/eio.html#eio_sync_file_range) — Sync a
    file segment with disk
-   [eio\_sync](/ref/eio.html#eio_sync) — Commit buffer cache to disk
-   [eio\_syncfs](/ref/eio.html#eio_syncfs) — Calls Linux' syncfs
    syscall, if available
-   [eio\_truncate](/ref/eio.html#eio_truncate) — Truncate a file
-   [eio\_unlink](/ref/eio.html#eio_unlink) — Delete a name and possibly
    the file it refers to
-   [eio\_utime](/ref/eio.html#eio_utime) — Change file last access and
    modification times
-   [eio\_write](/ref/eio.html#eio_write) — Write to file
