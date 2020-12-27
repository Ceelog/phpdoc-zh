stream\_bucket\_append
======================

Append bucket to brigade

### 说明

<span class="type">void</span> <span
class="methodname">stream\_bucket\_append</span> ( <span
class="methodparam"><span class="type">resource</span> `$brigade`</span>
, <span class="methodparam"><span class="type">object</span>
`$bucket`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

stream\_bucket\_make\_writeable
===============================

Return a bucket object from the brigade for operating on

### 说明

<span class="type">object</span> <span
class="methodname">stream\_bucket\_make\_writeable</span> ( <span
class="methodparam"><span class="type">resource</span> `$brigade`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

stream\_bucket\_new
===================

Create a new bucket for use on the current stream

### 说明

<span class="type">object</span> <span
class="methodname">stream\_bucket\_new</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
, <span class="methodparam"><span class="type">string</span>
`$buffer`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

stream\_bucket\_prepend
=======================

Prepend bucket to brigade

### 说明

<span class="type">void</span> <span
class="methodname">stream\_bucket\_prepend</span> ( <span
class="methodparam"><span class="type">resource</span> `$brigade`</span>
, <span class="methodparam"><span class="type">object</span>
`$bucket`</span> )

This function can be called to prepend a bucket to a bucket brigade. It
is typically called from <span
class="methodname">php\_user\_filter::filter</span>.

### 参数

`brigade`  
`brigade` is a resource pointing to a *bucket brigade* which contains
one or more *bucket* objects.

`bucket`  
A bucket object.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">stream\_bucket\_prepend</span>
examples**

``` php
<?php

class foo extends php_user_filter {
  protected $calls = 0;
  public function filter($in, $out, &$consumed, $closing) {
    while ($bucket = stream_bucket_make_writeable($in)) {
      $consumed += $bucket->datalen;
      if ($this->calls++ == 2) {
        // This bucket will appear again before any other bucket.
        stream_bucket_prepend($in, $bucket);
      }
    }
    return PSFS_FEED_ME;
  }
}
stream_filter_register('test', 'foo');
print  file_get_contents('php://filter/read=test/resource=foo');
?>
```

stream\_context\_create
=======================

创建资源流上下文

### 说明

<span class="type">resource</span> <span
class="methodname">stream\_context\_create</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$params`</span> \]\] )

创建并返回一个资源流上下文，该资源流中包含了 `options`
中提前设定的所有参数的值。

### 参数

`options`  
必须是一个二维关联数组，格式如下：*$arr\['wrapper'\]\['option'\] =
$value* 。

默认是一个空数组。

`params`  
必须是 *$arr\['parameter'\] = $value* 格式的关联数组。 请参考
<a href="/context.html" class="link">context parameters</a>
里的标准资源流参数列表。

### 返回值

上下文资源流，类型为 <span class="type">resource</span> 。

### 更新日志

| 版本  | 说明                       |
|-------|----------------------------|
| 5.3.0 | 增加了可选参数 `params` 。 |

### 范例

**示例 \#1 使用 <span class="function">stream\_context\_create</span>**

``` php
<?php
$opts = array(
  'http'=>array(
    'method'=>"GET",
    'header'=>"Accept-language: en\r\n" .
              "Cookie: foo=bar\r\n"
  )
);

$context = stream_context_create($opts);

/* Sends an http request to www.example.com
   with additional headers shown above */
$fp = fopen('http://www.example.com', 'r', false, $context);
fpassthru($fp);
fclose($fp);
?>
```

### 参见

-   <span class="function">stream\_context\_set\_option</span>
-   Listing of supported wrappers
    (<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>)
-   Context options
    (<a href="/context.html" class="xref">上下文（Context）选项和参数</a>)

stream\_context\_get\_default
=============================

Retrieve the default stream context

### 说明

<span class="type">resource</span> <span
class="methodname">stream\_context\_get\_default</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`</span> \]
)

Returns the default stream context which is used whenever file
operations (<span class="function">fopen</span>, <span
class="function">file\_get\_contents</span>, etc...) are called without
a context parameter. Options for the default context can optionally be
specified with this function using the same syntax as <span
class="function">stream\_context\_create</span>.

### 参数

`options`  
<span class="simpara"> `options` must be an associative array of
associative arrays in the format *$arr\['wrapper'\]\['option'\] =
$value*. </span>

> **Note**:
>
> As of PHP 5.3.0, the <span
> class="function">stream\_context\_set\_default</span> function can be
> used to set the default context.

### 返回值

A stream context <span class="type">resource</span>.

### 范例

**示例 \#1 Using <span
class="function">stream\_context\_get\_default</span>**

``` php
<?php
$default_opts = array(
  'http'=>array(
    'method'=>"GET",
    'header'=>"Accept-language: en\r\n" .
              "Cookie: foo=bar",
    'proxy'=>"tcp://10.54.1.39:8000"
  )
);


$alternate_opts = array(
  'http'=>array(
    'method'=>"POST",
    'header'=>"Content-type: application/x-www-form-urlencoded\r\n" .
              "Content-length: " . strlen("baz=bomb"),
    'content'=>"baz=bomb"
  )
);

$default = stream_context_get_default($default_opts);
$alternate = stream_context_create($alternate_opts);

/* Sends a regular GET request to proxy server at 10.54.1.39
 * For www.example.com using context options specified in $default_opts
 */
readfile('http://www.example.com');

/* Sends a POST request directly to www.example.com
 * Using context options specified in $alternate_opts
 */
readfile('http://www.example.com', false, $alternate);

?>
```

### 参见

-   <span class="function">stream\_context\_create</span>
-   Listing of supported wrappers with context options
    (<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>).

stream\_context\_get\_options
=============================

获取资源流/数据包/上下文的参数

### 说明

<span class="type">array</span> <span
class="methodname">stream\_context\_get\_options</span> ( <span
class="methodparam"><span class="type">resource</span>
`$stream_or_context`</span> )

返回指定资源流或者上下文的数组参数。

### 参数

`stream_or_context`  
获取参数信息的 <span class="type">stream</span> 或者 <span
class="type">context</span> 。

### 返回值

返回一个包含有原参数的关联数组。

### 范例

**示例 \#1 <span class="function">stream\_context\_get\_options</span>
的例子**

``` php
<?php
$params = array("method" => "POST");

stream_context_get_default(array("http" => $params));

var_dump(stream_context_get_options(stream_context_get_default()));

?>
```

以上例程的输出类似于：

    array(1) {
      ["http"]=>
      array(1) {
        ["method"]=>
        string(4) "POST"
      }
    }

stream\_context\_get\_params
============================

Retrieves parameters from a context

### 说明

<span class="type">array</span> <span
class="methodname">stream\_context\_get\_params</span> ( <span
class="methodparam"><span class="type">resource</span>
`$stream_or_context`</span> )

Retrieves parameter and options information from the stream or context.

### 参数

`stream_or_context`  
A stream <span class="type">resource</span> or a
<a href="/context.html" class="link">context</a> <span
class="type">resource</span>

### 返回值

Returns an associate array containing all context options and
parameters.

### 范例

**示例 \#1 <span class="function">stream\_context\_get\_params</span>
example**

Basic usage example

``` php
<?php
$ctx = stream_context_create();
$params = array("notification" => "stream_notification_callback");
stream_context_set_params($ctx, $params);

var_dump(stream_context_get_params($ctx));
?>
```

以上例程的输出类似于：

    array(2) {
      ["notification"]=>
      string(28) "stream_notification_callback"
      ["options"]=>
      array(0) {
      }
    }

### 参见

-   <span class="function">stream\_context\_set\_option</span>
-   <span class="function">stream\_context\_set\_params</span>

stream\_context\_set\_default
=============================

Set the default stream context

### 说明

<span class="type">resource</span> <span
class="methodname">stream\_context\_set\_default</span> ( <span
class="methodparam"><span class="type">array</span> `$options`</span> )

Set the default stream context which will be used whenever file
operations (<span class="function">fopen</span>, <span
class="function">file\_get\_contents</span>, etc...) are called without
a context parameter. Uses the same syntax as <span
class="function">stream\_context\_create</span>.

### 参数

`options`  
The options to set for the default context.

> **Note**:
>
> `options` must be an associative array of associative arrays in the
> format *$arr\['wrapper'\]\['option'\] = $value*.

### 返回值

Returns the default stream context.

### 范例

**示例 \#1 <span class="function">stream\_context\_set\_default</span>
example**

``` php
<?php
$default_opts = array(
  'http'=>array(
    'method'=>"GET",
    'header'=>"Accept-language: en\r\n" .
              "Cookie: foo=bar",
    'proxy'=>"tcp://10.54.1.39:8000"
  )
);

$default = stream_context_set_default($default_opts);

/* Sends a regular GET request to proxy server at 10.54.1.39
 * For www.example.com using context options specified in $default_opts
 */
readfile('http://www.example.com');
?>
```

### 参见

-   <span class="function">stream\_context\_create</span>
-   <span class="function">stream\_context\_get\_default</span>
-   Listing of supported wrappers with context options
    (<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>).

stream\_context\_set\_option
============================

对资源流、数据包或者上下文设置参数

### 说明

<span class="type">bool</span> <span
class="methodname">stream\_context\_set\_option</span> ( <span
class="methodparam"><span class="type">resource</span>
`$stream_or_context`</span> , <span class="methodparam"><span
class="type">string</span> `$wrapper`</span> , <span
class="methodparam"><span class="type">string</span> `$option`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="type">bool</span> <span
class="methodname">stream\_context\_set\_option</span> ( <span
class="methodparam"><span class="type">resource</span>
`$stream_or_context`</span> , <span class="methodparam"><span
class="type">array</span> `$options`</span> )

给指定的上下文设置参数。参数 `value` 是设置 `wrapper` 的 `option`
参数的值。

### 参数

`stream_or_context`  
需要添加参数的资源流或者上下文。

`options`  
添加给默认的上下文的参数。

> **Note**:
>
> `options` 必须是一个 *$arr\['wrapper'\]\['option'\] = $value*
> 格式二维关联数组 。
>
> 请参考
> <a href="/context.html" class="link">context options and parameters</a>
> 查看资源流参数列表。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

stream\_context\_set\_params
============================

Set parameters for a stream/wrapper/context

### 说明

<span class="type">bool</span> <span
class="methodname">stream\_context\_set\_params</span> ( <span
class="methodparam"><span class="type">resource</span> `$context`</span>
, <span class="methodparam"><span class="type">array</span>
`$params`</span> )

Sets parameters on the specified context.

### 参数

`context`  
The stream or context to apply the parameters too.

`params`  
An array of parameters to set.

> **Note**:
>
> `params` should be an associative array of the structure:
> *$params\['paramname'\] = "paramvalue";*.

### Supported parameters

| Parameters     | Purpose                                                                                                                                                                                                                                            |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *notification* | Name of user-defined callback function to be called whenever a stream triggers a notification. Only supported for <a href="/wrappers/http.html" class="link">http://</a> and <a href="/wrappers/ftp.html" class="link">ftp://</a> stream wrappers. |
| *options*      | Array of options as in <a href="/context.html" class="link">context options and parameters</a>.                                                                                                                                                    |

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">stream\_notification\_callback</span>

stream\_copy\_to\_stream
========================

Copies data from one stream to another

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">stream\_copy\_to\_stream</span> ( <span
class="methodparam"><span class="type">resource</span> `$source`</span>
, <span class="methodparam"><span class="type">resource</span>
`$dest`</span> \[, <span class="methodparam"><span
class="type">int</span> `$maxlength`<span class="initializer"> =
-1</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`<span class="initializer"> =
0</span></span> \]\] )

Makes a copy of up to `maxlength` bytes of data from the current
position (or from the `offset` position, if specified) in `source` to
`dest`. If `maxlength` is not specified, all remaining content in
`source` will be copied.

### 参数

`source`  
The source stream

`dest`  
The destination stream

`maxlength`  
Maximum bytes to copy

`offset`  
The offset where to start to copy data

### 返回值

Returns the total count of bytes copied, 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 A <span class="function">stream\_copy\_to\_stream</span>
example**

``` php
<?php
$src = fopen('http://www.example.com', 'r');
$dest1 = fopen('first1k.txt', 'w');
$dest2 = fopen('remainder.txt', 'w');

echo stream_copy_to_stream($src, $dest1, 1024) . " bytes copied to first1k.txt\n";
echo stream_copy_to_stream($src, $dest2) . " bytes copied to remainder.txt\n";

?>
```

### 参见

-   <span class="function">copy</span>

stream\_filter\_append
======================

Attach a filter to a stream

### 说明

<span class="type">resource</span> <span
class="methodname">stream\_filter\_append</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
, <span class="methodparam"><span class="type">string</span>
`$filtername`</span> \[, <span class="methodparam"><span
class="type">int</span> `$read_write`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$params`</span>
\]\] )

Adds `filtername` to the list of filters attached to `stream`.

### 参数

`stream`  
The target stream.

`filtername`  
The filter name.

`read_write`  
By default, <span class="function">stream\_filter\_append</span> will
attach the filter to the *read filter chain* if the file was opened for
reading (i.e. File Mode: *r*, and/or *+*). The filter will also be
attached to the *write filter chain* if the file was opened for writing
(i.e. File Mode: *w*, *a*, and/or *+*). **`STREAM_FILTER_READ`**,
**`STREAM_FILTER_WRITE`**, and/or **`STREAM_FILTER_ALL`** can also be
passed to the `read_write` parameter to override this behavior.

`params`  
This filter will be added with the specified `params` to the *end* of
the list and will therefore be called last during stream operations. To
add a filter to the beginning of the list, use <span
class="function">stream\_filter\_prepend</span>.

### 返回值

Returns a resource on success or **`false`** on failure. The resource
can be used to refer to this filter instance during a call to <span
class="function">stream\_filter\_remove</span>.

**`false`** is returned if `stream` is not a resource or if `filtername`
cannot be located.

### 范例

**示例 \#1 Controlling where filters are applied**

``` php
<?php
/* Open a test file for reading and writing */
$fp = fopen('test.txt', 'w+');

/* Apply the ROT13 filter to the
 * write filter chain, but not the
 * read filter chain */
stream_filter_append($fp, "string.rot13", STREAM_FILTER_WRITE);

/* Write a simple string to the file
 * it will be ROT13 transformed on the
 * way out */
fwrite($fp, "This is a test\n");

/* Back up to the beginning of the file */
rewind($fp);

/* Read the contents of the file back out.
 * Had the filter been applied to the
 * read filter chain as well, we would see
 * the text ROT13ed back to its original state */
fpassthru($fp);

fclose($fp);

/* Expected Output
   ---------------

Guvf vf n grfg

 */
?>
```

### 注释

> **Note**: **When using custom (user) filters**  
> <span class="simpara"> <span
> class="function">stream\_filter\_register</span> must be called first
> in order to register the desired user filter to `filtername`. </span>

> **Note**: <span class="simpara"> Stream data is read from resources
> (both local and remote) in chunks, with any unconsumed data kept in
> internal buffers. When a new filter is appended to a stream, data in
> the internal buffers is processed through the new filter at that time.
> This differs from the behavior of <span
> class="function">stream\_filter\_prepend</span>. </span>

> **Note**: <span class="simpara"> When a filter is added for read and
> write, two instances of the filter are created. <span
> class="function">stream\_filter\_append</span> must be called twice
> with **`STREAM_FILTER_READ`** and **`STREAM_FILTER_WRITE`** to get
> both filter resources. </span>

### 参见

-   <span class="function">stream\_filter\_register</span>
-   <span class="function">stream\_filter\_prepend</span>
-   <span class="function">stream\_get\_filters</span>

stream\_filter\_prepend
=======================

Attach a filter to a stream

### 说明

<span class="type">resource</span> <span
class="methodname">stream\_filter\_prepend</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
, <span class="methodparam"><span class="type">string</span>
`$filtername`</span> \[, <span class="methodparam"><span
class="type">int</span> `$read_write`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$params`</span>
\]\] )

Adds `filtername` to the list of filters attached to `stream`.

### 参数

`stream`  
The target stream.

`filtername`  
The filter name.

`read_write`  
By default, <span class="function">stream\_filter\_prepend</span> will
attach the filter to the *read filter chain* if the file was opened for
reading (i.e. File Mode: *r*, and/or *+*). The filter will also be
attached to the *write filter chain* if the file was opened for writing
(i.e. File Mode: *w*, *a*, and/or *+*). **`STREAM_FILTER_READ`**,
**`STREAM_FILTER_WRITE`**, and/or **`STREAM_FILTER_ALL`** can also be
passed to the `read_write` parameter to override this behavior. See
<span class="function">stream\_filter\_append</span> for an example of
using this parameter.

`params`  
This filter will be added with the specified `params` to the *beginning*
of the list and will therefore be called first during stream operations.
To add a filter to the end of the list, use <span
class="function">stream\_filter\_append</span>.

### 返回值

Returns a resource on success or **`false`** on failure. The resource
can be used to refer to this filter instance during a call to <span
class="function">stream\_filter\_remove</span>.

**`false`** is returned if `stream` is not a resource or if `filtername`
cannot be located.

### 注释

> **Note**: **When using custom (user) filters**  
> <span class="simpara"> <span
> class="function">stream\_filter\_register</span> must be called first
> in order to register the desired user filter to `filtername`. </span>

> **Note**: <span class="simpara"> Stream data is read from resources
> (both local and remote) in chunks, with any unconsumed data kept in
> internal buffers. When a new filter is prepended to a stream, data in
> the internal buffers, which has already been processed through other
> filters will *not* be reprocessed through the new filter at that time.
> This differs from the behavior of <span
> class="function">stream\_filter\_append</span>. </span>

> **Note**: <span class="simpara"> When a filter is added for read and
> write, two instances of the filter are created. <span
> class="function">stream\_filter\_prepend</span> must be called twice
> with **`STREAM_FILTER_READ`** and **`STREAM_FILTER_WRITE`** to get
> both filter resources. </span>

### 参见

-   <span class="function">stream\_filter\_register</span>
-   <span class="function">stream\_filter\_append</span>

stream\_filter\_register
========================

Register a user defined stream filter

### 说明

<span class="type">bool</span> <span
class="methodname">stream\_filter\_register</span> ( <span
class="methodparam"><span class="type">string</span>
`$filter_name`</span> , <span class="methodparam"><span
class="type">string</span> `$class`</span> )

<span class="function">stream\_filter\_register</span> allows you to
implement your own filter on any registered stream used with all the
other filesystem functions (such as <span class="function">fopen</span>,
<span class="function">fread</span> etc.).

### 参数

`filter_name`  
The filter name to be registered.

`class`  
To implement a filter, you need to define a class as an extension of
<span class="classname">php\_user\_filter</span> with a number of member
functions. When performing read/write operations on the stream to which
your filter is attached, PHP will pass the data through your filter (and
any other filters attached to that stream) so that the data may be
modified as desired. You must implement the methods exactly as described
in <span class="classname">php\_user\_filter</span> - doing otherwise
will lead to undefined behaviour.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

<span class="function">stream\_filter\_register</span> will return
**`false`** if the `filter_name` is already defined.

### 范例

**示例 \#1 Filter for capitalizing characters on `foo-bar.txt` stream**

The example below implements a filter named *strtoupper* on the
`foo-bar.txt` stream which will capitalize all letter characters written
to/read from that stream.

``` php
<?php

/* Define our filter class */
class strtoupper_filter extends php_user_filter {
  function filter($in, $out, &$consumed, $closing)
  {
    while ($bucket = stream_bucket_make_writeable($in)) {
      $bucket->data = strtoupper($bucket->data);
      $consumed += $bucket->datalen;
      stream_bucket_append($out, $bucket);
    }
    return PSFS_PASS_ON;
  }
}

/* Register our filter with PHP */
stream_filter_register("strtoupper", "strtoupper_filter")
    or die("Failed to register filter");

$fp = fopen("foo-bar.txt", "w");

/* Attach the registered filter to the stream just opened */
stream_filter_append($fp, "strtoupper");

fwrite($fp, "Line1\n");
fwrite($fp, "Word - 2\n");
fwrite($fp, "Easy As 123\n");

fclose($fp);

/* Read the contents back out
 */
readfile("foo-bar.txt");

?>
```

以上例程会输出：

    LINE1
    WORD - 2
    EASY AS 123

**示例 \#2 Registering a generic filter class to match multiple filter
names.**

``` php
<?php

/* Define our filter class */
class string_filter extends php_user_filter {
  var $mode;

  function filter($in, $out, &$consumed, $closing)
  {
    while ($bucket = stream_bucket_make_writeable($in)) {
      if ($this->mode == 1) {
        $bucket->data = strtoupper($bucket->data);
      } elseif ($this->mode == 0) {
        $bucket->data = strtolower($bucket->data);
      }

      $consumed += $bucket->datalen;
      stream_bucket_append($out, $bucket);
    }
    return PSFS_PASS_ON;
  }

  function onCreate()
  {
    if ($this->filtername == 'str.toupper') {
      $this->mode = 1;
    } elseif ($this->filtername == 'str.tolower') {
      $this->mode = 0;
    } else {
      /* Some other str.* filter was asked for,
         report failure so that PHP will keep looking */
      return false;
    }

    return true;
  }
}

/* Register our filter with PHP */
stream_filter_register("str.*", "string_filter")
    or die("Failed to register filter");

$fp = fopen("foo-bar.txt", "w");

/* Attach the registered filter to the stream just opened
   We could alternately bind to str.tolower here */
stream_filter_append($fp, "str.toupper");

fwrite($fp, "Line1\n");
fwrite($fp, "Word - 2\n");
fwrite($fp, "Easy As 123\n");

fclose($fp);

/* Read the contents back out
 */
readfile("foo-bar.txt");
?>
```

以上例程会输出：

    LINE1
    WORD - 2
    EASY AS 123

### 参见

-   <span class="function">stream\_wrapper\_register</span>
-   <span class="function">stream\_filter\_append</span>
-   <span class="function">stream\_filter\_prepend</span>

stream\_filter\_remove
======================

从资源流里移除某个过滤器

### 说明

<span class="type">bool</span> <span
class="methodname">stream\_filter\_remove</span> ( <span
class="methodparam"><span class="type">resource</span>
`$stream_filter`</span> )

移除之前通过 <span class="function">stream\_filter\_prepend</span> 或者
<span class="function">stream\_filter\_append</span>
添加到资源流里面的过滤器。
在移除之前，残留在过滤器内部缓冲区里的所有数据刷新到下一个过滤器。

### 参数

`stream_filter`  
需要被移除的资源流过滤器。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 动态地重新过滤一个资源流**

``` php
<?php
/* Open a test file for reading and writing */
$fp = fopen("test.txt", "rw");

$rot13_filter = stream_filter_append($fp, "string.rot13", STREAM_FILTER_WRITE);
fwrite($fp, "This is ");
stream_filter_remove($rot13_filter);
fwrite($fp, "a test\n");

rewind($fp);
fpassthru($fp);
fclose($fp);

?>
```

以上例程会输出：

    Guvf vf a test

### 参见

-   <span class="function">stream\_filter\_register</span>
-   <span class="function">stream\_filter\_append</span>
-   <span class="function">stream\_filter\_prepend</span>

stream\_get\_contents
=====================

读取资源流到一个字符串

### 说明

<span class="type">string</span> <span
class="methodname">stream\_get\_contents</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$maxlength`<span class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = -1</span></span> \]\] )

与 <span class="function">file\_get\_contents</span> 一样，但是 <span
class="function">stream\_get\_contents</span>
是对一个已经打开的资源流进行操作，并将其内容写入一个字符串返回。
返回的内容取决于 `maxlength` 字节长度和 `offset` 指定的起始位置。

### 参数

`handle` (<span class="type">resource</span>)  
一个资源流（例如 <span class="function">fopen</span>
操作之后返回的结果）

`maxlength` (<span class="type">integer</span>)  
需要读取的最大的字节数。默认是-1（读取全部的缓冲数据）。

`offset` (<span class="type">integer</span>)  
在读取数据之前先查找指定的偏移量。如果这个数字是负数，就不进行查找，直接从当前位置开始读取。

### 返回值

返回一个字符串 或者在失败时返回 **`false`**.

### 更新日志

| 版本  | 说明                 |
|-------|----------------------|
| 5.1.0 | 增加参数 `offset` 。 |

### 范例

**示例 \#1 <span class="function">stream\_get\_contents</span> 例子**

``` php
<?php

if ($stream = fopen('http://www.example.com', 'r')) {
    // print all the page starting at the offset 10
    echo stream_get_contents($stream, -1, 10);

    fclose($stream);
}


if ($stream = fopen('http://www.example.net', 'r')) {
    // print the first 5 bytes
    echo stream_get_contents($stream, 5);

    fclose($stream);
}

?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">fgets</span>
-   <span class="function">fread</span>
-   <span class="function">fpassthru</span>

stream\_get\_filters
====================

获取已注册的数据流过滤器列表

### 说明

<span class="type">array</span> <span
class="methodname">stream\_get\_filters</span> ( <span
class="methodparam">void</span> )

获取当前运行系统中已注册的数据流过滤器列表。

### 返回值

返回一个包含所有有效的数据流过滤器名字的索引数组。

### 范例

**示例 \#1 使用 <span class="function">stream\_get\_filters</span>**

``` php
<?php
$streamlist = stream_get_filters();
print_r($streamlist);
?>
```

以上例程的输出类似于：

    Array (
      [0] => string.rot13
      [1] => string.toupper
      [2] => string.tolower
      [3] => string.base64
      [4] => string.quoted-printable
    )

### 参见

-   <span class="function">stream\_filter\_register</span>
-   <span class="function">stream\_get\_wrappers</span>

stream\_get\_line
=================

从资源流里读取一行直到给定的定界符

### 说明

<span class="type">string</span> <span
class="methodname">stream\_get\_line</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
, <span class="methodparam"><span class="type">int</span>
`$length`</span> \[, <span class="methodparam"><span
class="type">string</span> `$ending`</span> \] )

从给定的资源流里读取一行。

当读取到 `length` 个字节数就结束，或者当在读取的字符串中发现 `ending`
（*不*包含到返回值里）也结束，又或者遇到了 EOF
也结束（总之以上条件中哪个先出现就以哪个为准）。

这个函数与 <span class="function">fgets</span>
几乎是相同的，唯一的区别是在这个函数里面允许指定行尾的定界符，而不是使用标准的
\\n， \\r 还有 \\r\\n ，并且返回值中*不*包含定界符。（翻译注：也可以把
\\n 等作为定界符传入 `ending` ）

### 参数

`handle`  
一个有效的文件句柄。

`length`  
需要从句柄里读取的字节数。

`ending`  
可选参数，字符串定界符。

### 返回值

返回一个字符串，该字符串的内容根据 `length` 字节数从 `handle` 里读取。

如果发生错误，则返回 **`false`**.

### 参见

-   <span class="function">fread</span>
-   <span class="function">fgets</span>
-   <span class="function">fgetc</span>

stream\_get\_meta\_data
=======================

从封装协议文件指针中取得报头／元数据

### 说明

<span class="type">array</span> <span
class="methodname">stream\_get\_meta\_data</span> ( <span
class="methodparam"><span class="type">int</span> `$fp`</span> )

返回现有 `stream` 的信息。可以是任何通过 <span
class="function">fopen</span>，<span class="function">fsockopen</span>
和 <span class="function">pfsockopen</span>
建立的流。返回的数组包含以下项目：

-   `timed_out` (bool) - 如果在上次调用 <span
    class="function">fread</span> 或者 <span
    class="function">fgets</span> 中等待数据时流超时了则为 **`true`**。

-   `blocked` (bool) - 如果流处于阻塞 IO 模式时为 **`true`**。参见 <span
    class="function">stream\_set\_blocking</span>。

-   `eof` (bool) - 如果流到达文件末尾时为 **`true`**。注意对于 socket
    流甚至当 `unread_bytes` 为非零值时也可以为
    **`true`**。要测定是否有更多数据可读，用 <span
    class="function">feof</span> 替代读取本项目的值。

-   `unread_bytes` (int) - 当前在 PHP 自己的内部缓冲区中的字节数。

    > **Note**: <span class="simpara"> 不要在脚本中使用此值。 </span>

以下项目是 PHP 4.3 新加的：

-   `stream_type` (string) - 一个描述流底层实现的标注。

-   `wrapper_type` (string) -
    一个描述流的分层协议封装实现的标注。更多关于封装协议的信息见
    <a href="/wrappers.html" class="xref">支持的协议和封装协议</a>。

-   `wrapper_data` (mixed) -
    当前流附加的封装协议数据。更多封装协议及其数据的信息见
    <a href="/wrappers.html" class="xref">支持的协议和封装协议</a>。

-   `filters` (array) -
    包含有被叠加在当前流的任何过滤器名的数组。过滤器的文档见附录中的<a href="/filters.html" class="link">可用过滤器列表</a>。

> **Note**:
>
> 本函数是 PHP 4.3 引进的，在此版本之前，可以用 <span
> class="function">socket\_get\_status</span>
> 来取得前四个项目并且*仅能用于基于 socket 的流*。
>
> 在 PHP 4.3 及以后版本中，<span
> class="function">socket\_get\_status</span> 是本函数的别名。

> **Note**: <span class="simpara"> 本函数不能作用于通过
> <a href="/ref/sockets.html" class="link">Socket 扩展库</a>创建的流。
> </span>

以下项目为 PHP 5.0 新加：

-   `mode` (string) - 对当前流所要求的访问类型（见
    <a href="/ref/filesystem.html#fopen" class="link">fopen()</a>
    中的表格 1）。

-   `seekable` (bool) - 是否可以在当前流中定位。

-   `uri` (string) - 与当前流关联的 URI 或文件名。

stream\_get\_transports
=======================

获取已注册的套接字传输协议列表

### 说明

<span class="type">array</span> <span
class="methodname">stream\_get\_transports</span> ( <span
class="methodparam">void</span> )

返回一个包含当前运行系统中所有套接字传输协议名称的索引数组。

### 返回值

返回一个套接字传输协议名称的索引数组。

### 范例

**示例 \#1 使用 <span class="function">stream\_get\_transports</span>**

``` php
<?php
$xportlist = stream_get_transports();
print_r($xportlist);
?>
```

以上例程的输出类似于：

    Array (
      [0] => tcp
      [1] => udp
      [2] => unix
      [3] => udg
    )

### 参见

-   <span class="function">stream\_get\_filters</span>
-   <span class="function">stream\_get\_wrappers</span>

stream\_get\_wrappers
=====================

获取已注册的流类型

### 说明

<span class="type">array</span> <span
class="methodname">stream\_get\_wrappers</span> ( <span
class="methodparam">void</span> )

获取在当前运行系统中已经注册并可使用的流类型列表。

### 返回值

返回一个索引数组，该数组里包含了当前运行系统中可使用的流类型的名称。

### 范例

**示例 \#1 <span class="function">stream\_get\_wrappers</span> 例子**

``` php
<?php
print_r(stream_get_wrappers());
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => php
        [1] => file
        [2] => http
        [3] => ftp
        [4] => compress.bzip2
        [5] => compress.zlib
    )

**示例 \#2 检查一个流类型是否存在**

``` php
<?php
// check for the existence of the bzip2 stream wrapper
if (in_array('compress.bzip2', stream_get_wrappers())) {
    echo 'compress.bzip2:// support enabled.';
} else {
    echo 'compress.bzip2:// support not enabled.';
}
?>
```

### 参见

-   <span class="function">stream\_wrapper\_register</span>

stream\_is\_local
=================

Checks if a stream is a local stream

### 说明

<span class="type">bool</span> <span
class="methodname">stream\_is\_local</span> ( <span
class="methodparam"><span class="type"><span
class="type">resource</span><span class="type">string</span></span>
`$stream`</span> )

Checks if a stream, or a URL, is a local one or not.

### 参数

`stream`  
The stream <span class="type">resource</span> or URL to check.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">stream\_is\_local</span> example**

Basic usage example.

``` php
<?php
var_dump(stream_is_local("http://example.com"));
var_dump(stream_is_local("/etc"));
?>
```

以上例程的输出类似于：

    bool(false)
    bool(true)

stream\_isatty
==============

Check if a stream is a TTY

### 说明

<span class="type">bool</span> <span
class="methodname">stream\_isatty</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
)

Determines if stream `stream` refers to a valid terminal type device.
This is a more portable version of <span
class="function">posix\_isatty</span>, since it works on Windows systems
too.

### 参数

`stream`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">stream\_isatty</span> example**

This command can be used to determine if a standard output / standard
error stream is redirected to a file.

``` sh
php -r "var_export(stream_isatty(STDERR));"
```

以上例程的输出类似于：

  
true  

``` sh
php -r "var_export(stream_isatty(STDERR));" 2>output.txt
```

以上例程的输出类似于：

  
false  

stream\_notification\_callback
==============================

A callback function for the *notification* context parameter

### 说明

<span class="type">void</span> <span class="methodname"><span
class="replaceable">stream\_notification\_callback</span></span> ( <span
class="methodparam"><span class="type">int</span>
`$notification_code`</span> , <span class="methodparam"><span
class="type">int</span> `$severity`</span> , <span
class="methodparam"><span class="type">string</span> `$message`</span> ,
<span class="methodparam"><span class="type">int</span>
`$message_code`</span> , <span class="methodparam"><span
class="type">int</span> `$bytes_transferred`</span> , <span
class="methodparam"><span class="type">int</span> `$bytes_max`</span> )

A <span class="type">callable</span> function, used by the
<a href="/context/params.html#context.params.notification" class="link">notification context parameter</a>,
called during an event.

> **Note**:
>
> This is *not* a real function, only a prototype of how the function
> should be.

### 参数

`notification_code`  
One of the **`STREAM_NOTIFY_*`** notification constants.

`severity`  
One of the **`STREAM_NOTIFY_SEVERITY_*`** notification constants.

`message`  
Passed if a descriptive message is available for the event.

`message_code`  
Passed if a descriptive message code is available for the event.

The meaning of this value is dependent on the specific wrapper in use.

`bytes_transferred`  
If applicable, the `bytes_transferred` will be populated.

`bytes_max`  
If applicable, the `bytes_max` will be populated.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">stream\_notification\_callback</span>
example**

``` php
<?php
function stream_notification_callback($notification_code, $severity, $message, $message_code, $bytes_transferred, $bytes_max) {

    switch($notification_code) {
        case STREAM_NOTIFY_RESOLVE:
        case STREAM_NOTIFY_AUTH_REQUIRED:
        case STREAM_NOTIFY_COMPLETED:
        case STREAM_NOTIFY_FAILURE:
        case STREAM_NOTIFY_AUTH_RESULT:
            var_dump($notification_code, $severity, $message, $message_code, $bytes_transferred, $bytes_max);
            /* Ignore */
            break;

        case STREAM_NOTIFY_REDIRECTED:
            echo "Being redirected to: ", $message;
            break;

        case STREAM_NOTIFY_CONNECT:
            echo "Connected...";
            break;

        case STREAM_NOTIFY_FILE_SIZE_IS:
            echo "Got the filesize: ", $bytes_max;
            break;

        case STREAM_NOTIFY_MIME_TYPE_IS:
            echo "Found the mime-type: ", $message;
            break;

        case STREAM_NOTIFY_PROGRESS:
            echo "Made some progress, downloaded ", $bytes_transferred, " so far";
            break;
    }
    echo "\n";
}

$ctx = stream_context_create();
stream_context_set_params($ctx, array("notification" => "stream_notification_callback"));

file_get_contents("http://php.net/contact", false, $ctx);
?>
```

以上例程的输出类似于：

    Connected...
    Found the mime-type: text/html; charset=utf-8
    Being redirected to: http://no.php.net/contact
    Connected...
    Got the filesize: 0
    Found the mime-type: text/html; charset=utf-8
    Being redirected to: http://no.php.net/contact.php
    Connected...
    Got the filesize: 4589
    Found the mime-type: text/html;charset=utf-8
    Made some progress, downloaded 0 so far
    Made some progress, downloaded 0 so far
    Made some progress, downloaded 0 so far
    Made some progress, downloaded 1440 so far
    Made some progress, downloaded 2880 so far
    Made some progress, downloaded 4320 so far
    Made some progress, downloaded 5760 so far
    Made some progress, downloaded 6381 so far
    Made some progress, downloaded 7002 so far

**示例 \#2 Simple progressbar for commandline download client**

``` php
<?php
function usage($argv) {
    echo "Usage:\n";
    printf("\tphp %s <http://example.com/file> <localfile>\n", $argv[0]);
    exit(1);
}

function stream_notification_callback($notification_code, $severity, $message, $message_code, $bytes_transferred, $bytes_max) {
    static $filesize = null;

    switch($notification_code) {
    case STREAM_NOTIFY_RESOLVE:
    case STREAM_NOTIFY_AUTH_REQUIRED:
    case STREAM_NOTIFY_COMPLETED:
    case STREAM_NOTIFY_FAILURE:
    case STREAM_NOTIFY_AUTH_RESULT:
        /* Ignore */
        break;

    case STREAM_NOTIFY_REDIRECTED:
        echo "Being redirected to: ", $message, "\n";
        break;

    case STREAM_NOTIFY_CONNECT:
        echo "Connected...\n";
        break;

    case STREAM_NOTIFY_FILE_SIZE_IS:
        $filesize = $bytes_max;
        echo "Filesize: ", $filesize, "\n";
        break;

    case STREAM_NOTIFY_MIME_TYPE_IS:
        echo "Mime-type: ", $message, "\n";
        break;

    case STREAM_NOTIFY_PROGRESS:
        if ($bytes_transferred > 0) {
            if (!isset($filesize)) {
                printf("\rUnknown filesize.. %2d kb done..", $bytes_transferred/1024);
            } else {
                $length = (int)(($bytes_transferred/$filesize)*100);
                printf("\r[%-100s] %d%% (%2d/%2d kb)", str_repeat("=", $length). ">", $length, ($bytes_transferred/1024), $filesize/1024);
            }
        }
        break;
    }
}

isset($argv[1], $argv[2]) or usage($argv);

$ctx = stream_context_create();
stream_context_set_params($ctx, array("notification" => "stream_notification_callback"));

$fp = fopen($argv[1], "r", false, $ctx);
if (is_resource($fp) && file_put_contents($argv[2], $fp)) {
    echo "\nDone!\n";
    exit(0);
}

$err = error_get_last();
echo "\nErrrrrorr..\n", $err["message"], "\n";
exit(1);
?>
```

Executing the example above with: *php -n fetch.php
http://no2.php.net/get/php-5-LATEST.tar.bz2/from/this/mirror
php-latest.tar.bz2* will output something similar too:

    Connected...
    Mime-type: text/html; charset=utf-8
    Being redirected to: http://no2.php.net/distributions/php-5.2.5.tar.bz2
    Connected...
    Filesize: 7773024
    Mime-type: application/octet-stream
    [========================================>                                                           ] 40% (3076/7590 kb)

### 参见

-   <a href="/context/params.html" class="xref">Context 参数</a>

stream\_register\_wrapper
=========================

别名 <span class="function">stream\_wrapper\_register</span>

### 说明

此函数是该函数的别名： <span
class="function">stream\_wrapper\_register</span>.

stream\_resolve\_include\_path
==============================

Resolve filename against the include path

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">stream\_resolve\_include\_path</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

Resolve `filename` against the include path according to the same rules
as <span class="function">fopen</span>/<span
class="function">include</span>.

### 参数

`filename`  
The filename to resolve.

### 返回值

Returns a <span class="type">string</span> containing the resolved
absolute filename, 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">stream\_resolve\_include\_path</span>
example**

Basic usage example.

``` php
<?php
var_dump(stream_resolve_include_path("test.php"));
?>
```

以上例程的输出类似于：

    string(22) "/var/www/html/test.php"

stream\_select
==============

Runs the equivalent of the select() system call on the given arrays of
streams with a timeout specified by tv\_sec and tv\_usec

### 说明

<span class="type">int</span> <span
class="methodname">stream\_select</span> ( <span
class="methodparam"><span class="type">array</span> `&$read`</span> ,
<span class="methodparam"><span class="type">array</span>
`&$write`</span> , <span class="methodparam"><span
class="type">array</span> `&$except`</span> , <span
class="methodparam"><span class="type">int</span> `$tv_sec`</span> \[,
<span class="methodparam"><span class="type">int</span> `$tv_usec`<span
class="initializer"> = 0</span></span> \] )

The <span class="function">stream\_select</span> function accepts arrays
of streams and waits for them to change status. Its operation is
equivalent to that of the <span class="function">socket\_select</span>
function except in that it acts on streams.

### 参数

`read`  
The streams listed in the `read` array will be watched to see if
characters become available for reading (more precisely, to see if a
read will not block - in particular, a stream resource is also ready on
end-of-file, in which case an <span class="function">fread</span> will
return a zero length string).

`write`  
The streams listed in the `write` array will be watched to see if a
write will not block.

`except`  
The streams listed in the `except` array will be watched for high
priority exceptional ("out-of-band") data arriving.

> **Note**:
>
> When <span class="function">stream\_select</span> returns, the arrays
> `read`, `write` and `except` are modified to indicate which stream
> resource(s) actually changed status. The original keys of the <span
> class="type">array</span>s are preserved.

`tv_sec`  
The `tv_sec` and `tv_usec` together form the *timeout* parameter,
`tv_sec` specifies the number of seconds while `tv_usec` the number of
microseconds. The `timeout` is an upper bound on the amount of time that
<span class="function">stream\_select</span> will wait before it
returns. If `tv_sec` and `tv_usec` are both set to *0*, <span
class="function">stream\_select</span> will not wait for data - instead
it will return immediately, indicating the current status of the
streams.

If `tv_sec` is **`null`** <span class="function">stream\_select</span>
can block indefinitely, returning only when an event on one of the
watched streams occurs (or if a signal interrupts the system call).

**Warning**
Using a timeout value of *0* allows you to instantaneously poll the
status of the streams, however, it is NOT a good idea to use a *0*
timeout value in a loop as it will cause your script to consume too much
CPU time.

It is much better to specify a timeout value of a few seconds, although
if you need to be checking and running other code concurrently, using a
timeout value of at least *200000* microseconds will help reduce the CPU
usage of your script.

Remember that the timeout value is the maximum time that will elapse;
<span class="function">stream\_select</span> will return as soon as the
requested streams are ready for use.

`tv_usec`  
See `tv_sec` description.

### 返回值

On success <span class="function">stream\_select</span> returns the
number of stream resources contained in the modified arrays, which may
be zero if the timeout expires before anything interesting happens. On
error **`false`** is returned and a warning raised (this can happen if
the system call is interrupted by an incoming signal).

### 范例

**示例 \#1 <span class="function">stream\_select</span> Example**

This example checks to see if data has arrived for reading on either
`$stream1` or `$stream2`. Since the timeout value is *0* it will return
immediately:

``` php
<?php
/* Prepare the read array */
$read   = array($stream1, $stream2);
$write  = NULL;
$except = NULL;
if (false === ($num_changed_streams = stream_select($read, $write, $except, 0))) {
    /* Error handling */
} elseif ($num_changed_streams > 0) {
    /* At least on one of the streams something interesting happened */
}
?>
```

### 注释

> **Note**:
>
> Due to a limitation in the current Zend Engine it is not possible to
> pass a constant modifier like **`null`** directly as a parameter to a
> function which expects this parameter to be passed by reference.
> Instead use a temporary variable or an expression with the leftmost
> member being a temporary variable:
>
> ``` php
> <?php
> $e = NULL;
> stream_select($r, $w, $e, 0);
> ?>
> ```

> **Note**:
>
> Be sure to use the *===* operator when checking for an error. Since
> the <span class="function">stream\_select</span> may return 0 the
> comparison with *==* would evaluate to **`true`**:
>
> ``` php
> <?php
> $e = NULL;
> if (false === stream_select($r, $w, $e, 0)) {
>     echo "stream_select() failed\n";
> }
> ?>
> ```

> **Note**:
>
> If you read/write to a stream returned in the arrays be aware that
> they do not necessarily read/write the full amount of data you have
> requested. Be prepared to even only be able to read/write a single
> byte.

> **Note**:
>
> Some streams (like *zlib*) cannot be selected by this function.

> **Note**: **Windows compatibility**  
>
> Use of <span class="function">stream\_select</span> on file
> descriptors returned by <span class="function">proc\_open</span> will
> fail and return **`false`** under Windows.
>
> **`STDIN`** from a console changes status as soon as *any* input
> events are available, but reading from the stream may still block.

### 参见

-   <span class="function">stream\_set\_blocking</span>

stream\_set\_blocking
=====================

为资源流设置阻塞或者阻塞模式

### 说明

<span class="type">bool</span> <span
class="methodname">stream\_set\_blocking</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
, <span class="methodparam"><span class="type">bool</span>
`$mode`</span> )

为 `stream` 设置阻塞或者阻塞模。

此函数适用于支持非阻塞模式的任何资源流（常规文件，套接字资源流等）。

### 参数

`stream`  
资源流。

`mode`  
如果 `mode` 为 **`false`**，资源流将会被转换为非阻塞模式；如果是
**`true`**，资源流将会被转换为阻塞模式。 该参数的设置将会影响到像 <span
class="function">fgets</span> 和 <span class="function">fread</span>
这样的函数从资源流里读取数据。 在非阻塞模式下，调用 <span
class="function">fgets</span>
总是会立即返回；而在阻塞模式下，将会一直等到从资源流里面获取到数据才能返回。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 注释

> **Note**:
>
> 该函数之前叫作 <span class="function">set\_socket\_blocking</span>
> 后来又叫做 <span class="function">socket\_set\_blocking</span>
> ，但是这种用法都已经被废弃。

> **Note**:
>
> 在 Windows 系统上，这对本地文件没有影响。Windows
> 不支持本地文件的非阻塞 IO。

### 参见

-   <span class="function">stream\_select</span>

stream\_set\_chunk\_size
========================

设置资源流区块大小

### 说明

<span class="type">int</span> <span
class="methodname">stream\_set\_chunk\_size</span> ( <span
class="methodparam"><span class="type">resource</span> `$fp`</span> ,
<span class="methodparam"><span class="type">int</span>
`$chunk_size`</span> )

设置资源流区块大小。

### 参数

`fp`  
目标资源流。

`chunk_size`  
想设置的新的区块大小。

### 返回值

成功的情况下返回资源流之前的区块大小。

如果 `chunk_size` 比 1 小或者比 **`PHP_INT_MAX`** 还大，就将返回
**`false`** 。

### 错误／异常

当 `chunk_size` 比 1 小或者比 **`PHP_INT_MAX`** 还大的时候将会产生一个
**`E_WARNING`** 级别的错误。

stream\_set\_read\_buffer
=========================

Set read file buffering on the given stream

### 说明

<span class="type">int</span> <span
class="methodname">stream\_set\_read\_buffer</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
, <span class="methodparam"><span class="type">int</span> `$size`</span>
)

Sets the read buffer. It's the equivalent of <span
class="function">stream\_set\_write\_buffer</span>, but for read
operations.

### 参数

`stream`  
The file pointer.

`size`  
The number of bytes to buffer. If `size` is 0 then read operations are
unbuffered. This ensures that all reads with <span
class="function">fread</span> are completed before other processes are
allowed to read from that input stream.

### 返回值

Returns 0 on success, or another value if the request cannot be honored.

### 参见

-   <span class="function">stream\_set\_write\_buffer</span>

stream\_set\_timeout
====================

Set timeout period on a stream

### 说明

<span class="type">bool</span> <span
class="methodname">stream\_set\_timeout</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
, <span class="methodparam"><span class="type">int</span>
`$seconds`</span> \[, <span class="methodparam"><span
class="type">int</span> `$microseconds`<span class="initializer"> =
0</span></span> \] )

Sets the timeout value on `stream`, expressed in the sum of `seconds`
and `microseconds`.

When the stream times out, the 'timed\_out' key of the array returned by
<span class="function">stream\_get\_meta\_data</span> is set to
**`true`**, although no error/warning is generated.

### 参数

`stream`  
The target stream.

`seconds`  
The seconds part of the timeout to be set.

`microseconds`  
The microseconds part of the timeout to be set.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">stream\_set\_timeout</span> example**

``` php
<?php
$fp = fsockopen("www.example.com", 80);
if (!$fp) {
    echo "Unable to open\n";
} else {

    fwrite($fp, "GET / HTTP/1.0\r\n\r\n");
    stream_set_timeout($fp, 2);
    $res = fread($fp, 2000);

    $info = stream_get_meta_data($fp);
    fclose($fp);

    if ($info['timed_out']) {
        echo 'Connection timed out!';
    } else {
        echo $res;
    }

}
?>
```

### 注释

> **Note**:
>
> This function doesn't work with advanced operations like <span
> class="function">stream\_socket\_recvfrom</span>, use <span
> class="function">stream\_select</span> with timeout parameter instead.

This function was previously called as <span
class="function">set\_socket\_timeout</span> and later <span
class="function">socket\_set\_timeout</span> but this usage is
deprecated.

### 参见

-   <span class="function">fsockopen</span>
-   <span class="function">fopen</span>

stream\_set\_write\_buffer
==========================

Sets write file buffering on the given stream

### 说明

<span class="type">int</span> <span
class="methodname">stream\_set\_write\_buffer</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
, <span class="methodparam"><span class="type">int</span>
`$buffer`</span> )

Sets the buffering for write operations on the given `stream` to
`buffer` bytes.

### 参数

`stream`  
The file pointer.

`buffer`  
The number of bytes to buffer. If `buffer` is 0 then write operations
are unbuffered. This ensures that all writes with <span
class="function">fwrite</span> are completed before other processes are
allowed to write to that output stream.

### 返回值

Returns 0 on success, or another value if the request cannot be honored.

### 范例

**示例 \#1 <span class="function">stream\_set\_write\_buffer</span>
example**

The following example demonstrates how to use <span
class="function">stream\_set\_write\_buffer</span> to create an
unbuffered stream.

``` php
<?php
$fp = fopen($file, "w");
if ($fp) {
  if (stream_set_write_buffer($fp, 0) !== 0) {
      // changing the buffering failed
  }
  fwrite($fp, $output);
  fclose($fp);
}
?>
```

### 参见

-   <span class="function">fopen</span>
-   <span class="function">fwrite</span>

stream\_socket\_accept
======================

接受由 <span class="function">stream\_socket\_server</span>
创建的套接字连接

### 说明

<span class="type">resource</span> <span
class="methodname">stream\_socket\_accept</span> ( <span
class="methodparam"><span class="type">resource</span>
`$server_socket`</span> \[, <span class="methodparam"><span
class="type">float</span> `$timeout`<span class="initializer"> =
ini\_get("default\_socket\_timeout")</span></span> \[, <span
class="methodparam"><span class="type">string</span> `&$peername`</span>
\]\] )

接受由 <span class="function">stream\_socket\_server</span>
创建的套接字连接。

### 参数

`server_socket`  
需要接受的服务器创建的套接字连接。

`timeout`  
覆盖默认的套接字接受的超时时限。输入的时间需以秒为单位。

`peername`  
如果包含该参数并且是可以从选中的传输数据中获取到，则将被设置给连接中的客户端主机的名称（地址）（怕出入很大，附带上原文：Will
be set to the name (address) of the client which connected, if included
and available from the selected transport.）

> **Note**:
>
> 也可以之后通过 <span class="function">stream\_socket\_get\_name</span>
> 来确定。

### 返回值

返回接受套接之后的资源流 或者在失败时返回 **`false`**。

### 注释

**Warning**

该函数不能被用于 UDP 套接字。可以使用 <span
class="function">stream\_socket\_recvfrom</span> 和 <span
class="function">stream\_socket\_sendto</span> 来取而代之。

### 参见

-   <span class="function">stream\_socket\_server</span>
-   <span class="function">stream\_socket\_get\_name</span>
-   <span class="function">stream\_set\_blocking</span>
-   <span class="function">stream\_set\_timeout</span>
-   <span class="function">fgets</span>
-   <span class="function">fgetss</span>
-   <span class="function">fwrite</span>
-   <span class="function">fclose</span>
-   <span class="function">feof</span>
-   <a href="/ref/curl.html" class="xref">cURL 函数</a>

stream\_socket\_client
======================

Open Internet or Unix domain socket connection

### 说明

<span class="type">resource</span> <span
class="methodname">stream\_socket\_client</span> ( <span
class="methodparam"><span class="type">string</span>
`$remote_socket`</span> \[, <span class="methodparam"><span
class="type">int</span> `&$errno`</span> \[, <span
class="methodparam"><span class="type">string</span> `&$errstr`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$timeout`<span class="initializer"> =
ini\_get("default\_socket\_timeout")</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = STREAM\_CLIENT\_CONNECT</span></span> \[, <span
class="methodparam"><span class="type">resource</span> `$context`</span>
\]\]\]\]\] )

Initiates a stream or datagram connection to the destination specified
by `remote_socket`. The type of socket created is determined by the
transport specified using standard URL formatting: *transport://target*.
For Internet Domain sockets (AF\_INET) such as TCP and UDP, the *target*
portion of the `remote_socket` parameter should consist of a hostname or
IP address followed by a colon and a port number. For Unix domain
sockets, the `target` portion should point to the socket file on the
filesystem.

> **Note**:
>
> The stream will by default be opened in blocking mode. You can switch
> it to non-blocking mode by using <span
> class="function">stream\_set\_blocking</span>.

### 参数

`remote_socket`  
Address to the socket to connect to.

`errno`  
Will be set to the system level error number if connection fails.

`errstr`  
Will be set to the system level error message if the connection fails.

`timeout`  
Number of seconds until the *connect()* system call should timeout.

> **Note**: <span class="simpara"> This parameter only applies when not
> making asynchronous connection attempts. </span>

> **Note**:
>
> To set a timeout for reading/writing data over the socket, use the
> <span class="function">stream\_set\_timeout</span>, as the `timeout`
> only applies while making connecting the socket.

`flags`  
Bitmask field which may be set to any combination of connection flags.
Currently the select of connection flags is limited to
**`STREAM_CLIENT_CONNECT`** (default), **`STREAM_CLIENT_ASYNC_CONNECT`**
and **`STREAM_CLIENT_PERSISTENT`**.

`context`  
A valid context resource created with <span
class="function">stream\_context\_create</span>.

### 返回值

On success a stream resource is returned which may be used together with
the other file functions (such as <span class="function">fgets</span>,
<span class="function">fgetss</span>, <span
class="function">fwrite</span>, <span class="function">fclose</span>,
and <span class="function">feof</span>), **`false`** on failure.

### 错误／异常

On failure the `errno` and `errstr` arguments will be populated with the
actual system level error that occurred in the system-level *connect()*
call. If the value returned in `errno` is *0* and the function returned
**`false`**, it is an indication that the error occurred before the
*connect()* call. This is most likely due to a problem initializing the
socket. Note that the `errno` and `errstr` arguments will always be
passed by reference.

### 范例

**示例 \#1 <span class="function">stream\_socket\_client</span>
example**

``` php
<?php
$fp = stream_socket_client("tcp://www.example.com:80", $errno, $errstr, 30);
if (!$fp) {
    echo "$errstr ($errno)<br />\n";
} else {
    fwrite($fp, "GET / HTTP/1.0\r\nHost: www.example.com\r\nAccept: */*\r\n\r\n");
    while (!feof($fp)) {
        echo fgets($fp, 1024);
    }
    fclose($fp);
}
?>
```

**示例 \#2 Using UDP connection**

Retrieving the day and time from the UDP service "daytime" (port 13) on
localhost.

``` php
<?php
$fp = stream_socket_client("udp://127.0.0.1:13", $errno, $errstr);
if (!$fp) {
    echo "ERROR: $errno - $errstr<br />\n";
} else {
    fwrite($fp, "\n");
    echo fread($fp, 26);
    fclose($fp);
}
?>
```

### 注释

**Warning**

UDP sockets will sometimes appear to have opened without an error, even
if the remote host is unreachable. The error will only become apparent
when you read or write data to/from the socket. The reason for this is
because UDP is a "connectionless" protocol, which means that the
operating system does not try to establish a link for the socket until
it actually needs to send or receive data.

> **Note**: <span class="simpara">当指定数值型的 IPv6 地址（例如
> *fe80::1*）时必须用方括号将 IP 围起来——例如，
> *tcp://\[fe80::1\]:80*。</span>

> **Note**:
>
> Depending on the environment, the Unix domain or the optional connect
> timeout may not be available. A list of available transports can be
> retrieved using <span class="function">stream\_get\_transports</span>.
> See
> <a href="/transports.html" class="xref">所支持的套接字传输器（Socket Transports）列表</a>
> for a list of built in transports.

### 参见

-   <span class="function">stream\_socket\_server</span>
-   <span class="function">stream\_set\_blocking</span>
-   <span class="function">stream\_set\_timeout</span>
-   <span class="function">stream\_select</span>
-   <span class="function">fgets</span>
-   <span class="function">fgetss</span>
-   <span class="function">fwrite</span>
-   <span class="function">fclose</span>
-   <span class="function">feof</span>
-   <a href="/ref/curl.html" class="xref">cURL 函数</a>

stream\_socket\_enable\_crypto
==============================

Turns encryption on/off on an already connected socket

### 说明

<span class="type">mixed</span> <span
class="methodname">stream\_socket\_enable\_crypto</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
, <span class="methodparam"><span class="type">bool</span>
`$enable`</span> \[, <span class="methodparam"><span
class="type">int</span> `$crypto_type`</span> \[, <span
class="methodparam"><span class="type">resource</span>
`$session_stream`</span> \]\] )

Enable or disable encryption on the stream.

Once the crypto settings are established, cryptography can be turned on
and off dynamically by passing **`true`** or **`false`** in the `enable`
parameter.

### 参数

`stream`  
The stream resource.

`enable`  
Enable/disable cryptography on the stream.

`crypto_type`  
Setup encryption on the stream. Valid methods are

-   <span class="simpara">**`STREAM_CRYPTO_METHOD_SSLv2_CLIENT`**</span>
-   <span class="simpara">**`STREAM_CRYPTO_METHOD_SSLv3_CLIENT`**</span>
-   <span
    class="simpara">**`STREAM_CRYPTO_METHOD_SSLv23_CLIENT`**</span>
-   <span class="simpara">**`STREAM_CRYPTO_METHOD_ANY_CLIENT`**</span>
-   <span class="simpara">**`STREAM_CRYPTO_METHOD_TLS_CLIENT`**</span>
-   <span
    class="simpara">**`STREAM_CRYPTO_METHOD_TLSv1_0_CLIENT`**</span>
-   <span
    class="simpara">**`STREAM_CRYPTO_METHOD_TLSv1_1_CLIENT`**</span>
-   <span
    class="simpara">**`STREAM_CRYPTO_METHOD_TLSv1_2_CLIENT`**</span>
-   <span class="simpara">**`STREAM_CRYPTO_METHOD_SSLv2_SERVER`**</span>
-   <span class="simpara">**`STREAM_CRYPTO_METHOD_SSLv3_SERVER`**</span>
-   <span
    class="simpara">**`STREAM_CRYPTO_METHOD_SSLv23_SERVER`**</span>
-   <span class="simpara">**`STREAM_CRYPTO_METHOD_ANY_SERVER`**</span>
-   <span class="simpara">**`STREAM_CRYPTO_METHOD_TLS_SERVER`**</span>
-   <span
    class="simpara">**`STREAM_CRYPTO_METHOD_TLSv1_0_SERVER`**</span>
-   <span
    class="simpara">**`STREAM_CRYPTO_METHOD_TLSv1_1_SERVER`**</span>
-   <span
    class="simpara">**`STREAM_CRYPTO_METHOD_TLSv1_2_SERVER`**</span>

If omitted, the *crypto\_method* context option on the stream's SSL
context will be used instead.

`session_stream`  
Seed the stream with settings from `session_stream`.

### 返回值

Returns **`true`** on success, **`false`** if negotiation has failed or
*0* if there isn't enough data and you should try again (only for
non-blocking sockets).

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                                                                                                      |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.6.0 | Introduce **`STREAM_CRYPTO_METHOD_ANY_CLIENT`**, **`STREAM_CRYPTO_METHOD_TLSv1_0_CLIENT`**, **`STREAM_CRYPTO_METHOD_TLSv1_1_CLIENT`**, **`STREAM_CRYPTO_METHOD_TLSv1_2_CLIENT`**, **`STREAM_CRYPTO_METHOD_ANY_SERVER`**, **`STREAM_CRYPTO_METHOD_TLSv1_0_SERVER`**, **`STREAM_CRYPTO_METHOD_TLSv1_1_SERVER`**, **`STREAM_CRYPTO_METHOD_TLSv1_2_SERVER`**. |
| 5.6.0 | The `crypto_type` is now optional.                                                                                                                                                                                                                                                                                                                        |

### 范例

**示例 \#1 <span class="function">stream\_socket\_enable\_crypto</span>
example**

``` php
<?php
$fp = stream_socket_client("tcp://myproto.example.com:31337", $errno, $errstr, 30);
if (!$fp) {
    die("Unable to connect: $errstr ($errno)");
}

/* Turn on encryption for login phase */
stream_socket_enable_crypto($fp, true, STREAM_CRYPTO_METHOD_SSLv23_CLIENT);
fwrite($fp, "USER god\r\n");
fwrite($fp, "PASS secret\r\n");

/* Turn off encryption for the rest */
stream_socket_enable_crypto($fp, false);

while ($motd = fgets($fp)) {
    echo $motd;
}

fclose($fp);
?>
```

以上例程的输出类似于：

### 参见

-   <a href="/ref/openssl.html" class="xref">OpenSSL 函数</a>
-   <a href="/transports.html" class="xref">所支持的套接字传输器（Socket Transports）列表</a>

stream\_socket\_get\_name
=========================

获取本地或者远程的套接字名称

### 说明

<span class="type">string</span> <span
class="methodname">stream\_socket\_get\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
, <span class="methodparam"><span class="type">bool</span>
`$want_peer`</span> )

返回给定的本地或者远程套接字连接的名称。

### 参数

`handle`  
需要获取其名称的套接字连接。

`want_peer`  
如果设置为 **`true`** ，那么将返回 *remote* 套接字连接名称；如果设置为
**`false`** 则返回 *local* 套接字连接名称。

### 返回值

套接字连接的名称。

### 参见

-   <span class="function">stream\_socket\_accept</span>

stream\_socket\_pair
====================

创建一对完全一样的网络套接字连接流

### 说明

<span class="type">array</span> <span
class="methodname">stream\_socket\_pair</span> ( <span
class="methodparam"><span class="type">int</span> `$domain`</span> ,
<span class="methodparam"><span class="type">int</span> `$type`</span> ,
<span class="methodparam"><span class="type">int</span>
`$protocol`</span> )

<span class="function">stream\_socket\_pair</span>
创建一对完全一样的网络套接字连接，这个函数通常会被用在进程间通信(Inter-Process
Communication)

### 参数

`domain`  
使用的协议族： **`STREAM_PF_INET`**, **`STREAM_PF_INET6`** or
**`STREAM_PF_UNIX`**

`type`  
通信类型: **`STREAM_SOCK_DGRAM`**, **`STREAM_SOCK_RAW`**,
**`STREAM_SOCK_RDM`**, **`STREAM_SOCK_SEQPACKET`** or
**`STREAM_SOCK_STREAM`**

`protocol`  
使用的传输协议: **`STREAM_IPPROTO_ICMP`**, **`STREAM_IPPROTO_IP`**,
**`STREAM_IPPROTO_RAW`**, **`STREAM_IPPROTO_TCP`** or
**`STREAM_IPPROTO_UDP`**

> **Note**: <span class="simpara"> Please consult the
> <a href="/stream/constants.html" class="link">Streams constant list</a>
> for further details on each constant. </span>

### 返回值

如果成功将返回一个<span
class="type">数组</span>包括了两个socket资源，错误时返回**`false`**

### 更新日志

| 版本  | 说明                        |
|-------|-----------------------------|
| 5.3.0 | 这个函数在windows平台不可用 |

### 范例

**示例 \#1 A <span class="function">stream\_socket\_pair</span>
example**

This example shows the basic usage of <span
class="function">stream\_socket\_pair</span> in Inter-Process
Comunication.

``` php
<?php

$sockets = stream_socket_pair(STREAM_PF_UNIX, STREAM_SOCK_STREAM, STREAM_IPPROTO_IP);
$pid     = pcntl_fork();

if ($pid == -1) {
     die('could not fork');

} else if ($pid) {
     /* parent */
    fclose($sockets[0]);

    fwrite($sockets[1], "child PID: $pid\n");
    echo fgets($sockets[1]);

    fclose($sockets[1]);

} else {
    /* child */
    fclose($sockets[1]);

    fwrite($sockets[0], "message from child\n");
    echo fgets($sockets[0]);

    fclose($sockets[0]);
}

?>
```

以上例程的输出类似于：

    child PID: 1378
    message from child

stream\_socket\_recvfrom
========================

Receives data from a socket, connected or not

### 说明

<span class="type">string</span> <span
class="methodname">stream\_socket\_recvfrom</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
, <span class="methodparam"><span class="type">int</span>
`$length`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">string</span> `&$address`</span> \]\] )

<span class="function">stream\_socket\_recvfrom</span> accepts data from
a remote socket up to `length` bytes.

### 参数

`socket`  
The remote socket.

`length`  
The number of bytes to receive from the `socket`.

`flags`  
The value of `flags` can be any combination of the following:

|                   |                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`STREAM_OOB`**  | Process OOB (*out-of-band*) data.                                                                                                                                                                       |
| **`STREAM_PEEK`** | Retrieve data from the socket, but do not consume the buffer. Subsequent calls to <span class="function">fread</span> or <span class="function">stream\_socket\_recvfrom</span> will see the same data. |

`address`  
If `address` is provided it will be populated with the address of the
remote socket.

### 返回值

Returns the read data, as a string

### 范例

**示例 \#1 <span class="function">stream\_socket\_recvfrom</span>
example**

``` php
<?php
/* Open a server socket to port 1234 on localhost */
$server = stream_socket_server('tcp://127.0.0.1:1234');

/* Accept a connection */
$socket = stream_socket_accept($server);

/* Grab a packet (1500 is a typical MTU size) of OOB data */
echo "Received Out-Of-Band: '" . stream_socket_recvfrom($socket, 1500, STREAM_OOB) . "'\n";

/* Take a peek at the normal in-band data, but don't consume it. */
echo "Data: '" . stream_socket_recvfrom($socket, 1500, STREAM_PEEK) . "'\n";

/* Get the exact same packet again, but remove it from the buffer this time. */
echo "Data: '" . stream_socket_recvfrom($socket, 1500) . "'\n";

/* Close it up */
fclose($socket);
fclose($server);
?>
```

### 注释

> **Note**:
>
> If a message received is longer than the `length` parameter, excess
> bytes may be discarded depending on the type of socket the message is
> received from (such as UDP).

> **Note**:
>
> Calls to <span class="function">stream\_socket\_recvfrom</span> on
> socket-based streams, after calls to buffer-based stream functions
> (like <span class="function">fread</span> or <span
> class="function">stream\_get\_line</span>) read data directly from the
> socket and bypass the stream buffer.

### 参见

-   <span class="function">stream\_socket\_sendto</span>
-   <span class="function">stream\_socket\_client</span>
-   <span class="function">stream\_socket\_server</span>

stream\_socket\_sendto
======================

Sends a message to a socket, whether it is connected or not

### 说明

<span class="type">int</span> <span
class="methodname">stream\_socket\_sendto</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
, <span class="methodparam"><span class="type">string</span>
`$data`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$address`</span> \]\] )

Sends the specified `data` through the `socket`.

### 参数

`socket`  
The socket to send `data` to.

`data`  
The data to be sent.

`flags`  
The value of `flags` can be any combination of the following:

|                  |                                 |
|------------------|---------------------------------|
| **`STREAM_OOB`** | Process OOB (out-of-band) data. |

`address`  
The address specified when the socket stream was created will be used
unless an alternate address is specified in `address`.

If specified, it must be in dotted quad (or \[ipv6\]) format.

### 返回值

Returns a result code, as an integer.

### 范例

**示例 \#1 <span class="function">stream\_socket\_sendto</span>
Example**

``` php
<?php
/* Open a socket to port 1234 on localhost */
$socket = stream_socket_client('tcp://127.0.0.1:1234');

/* Send ordinary data via ordinary channels. */
fwrite($socket, "Normal data transmit.");

/* Send more data out of band. */
stream_socket_sendto($socket, "Out of Band data.", STREAM_OOB);

/* Close it up */
fclose($socket);
?>
```

### 参见

-   <span class="function">stream\_socket\_recvfrom</span>
-   <span class="function">stream\_socket\_client</span>
-   <span class="function">stream\_socket\_server</span>

stream\_socket\_server
======================

Create an Internet or Unix domain server socket

### 说明

<span class="type">resource</span> <span
class="methodname">stream\_socket\_server</span> ( <span
class="methodparam"><span class="type">string</span>
`$local_socket`</span> \[, <span class="methodparam"><span
class="type">int</span> `&$errno`</span> \[, <span
class="methodparam"><span class="type">string</span> `&$errstr`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> = STREAM\_SERVER\_BIND \|
STREAM\_SERVER\_LISTEN</span></span> \[, <span class="methodparam"><span
class="type">resource</span> `$context`</span> \]\]\]\] )

Creates a stream or datagram socket on the specified `local_socket`.

This function only creates a socket, to begin accepting connections use
<span class="function">stream\_socket\_accept</span>.

### 参数

`local_socket`  
The type of socket created is determined by the transport specified
using standard URL formatting: *transport://target*.

For Internet Domain sockets (**`AF_INET`**) such as TCP and UDP, the
*target* portion of the `remote_socket` parameter should consist of a
hostname or IP address followed by a colon and a port number. For Unix
domain sockets, the *target* portion should point to the socket file on
the filesystem.

Depending on the environment, Unix domain sockets may not be available.
A list of available transports can be retrieved using <span
class="function">stream\_get\_transports</span>. See
<a href="/transports.html" class="xref">所支持的套接字传输器（Socket Transports）列表</a>
for a list of bulitin transports.

`errno`  
If the optional `errno` and `errstr` arguments are present they will be
set to indicate the actual system level error that occurred in the
system-level *socket()*, *bind()*, and *listen()* calls. If the value
returned in `errno` is *0* and the function returned **`false`**, it is
an indication that the error occurred before the *bind()* call. This is
most likely due to a problem initializing the socket. Note that the
`errno` and `errstr` arguments will always be passed by reference.

`errstr`  
See `errno` description.

`flags`  
A bitmask field which may be set to any combination of socket creation
flags.

> **Note**:
>
> For UDP sockets, you must use **`STREAM_SERVER_BIND`** as the `flags`
> parameter.

`context`  

### 返回值

Returns the created stream, or **`false`** on error.

### 范例

**示例 \#1 Using TCP server sockets**

``` php
<?php
$socket = stream_socket_server("tcp://0.0.0.0:8000", $errno, $errstr);
if (!$socket) {
  echo "$errstr ($errno)<br />\n";
} else {
  while ($conn = stream_socket_accept($socket)) {
    fwrite($conn, 'The local time is ' . date('n/j/Y g:i a') . "\n");
    fclose($conn);
  }
  fclose($socket);
}
?>
```

The example below shows how to act as a time server which can respond to
time queries as shown in an example on <span
class="function">stream\_socket\_client</span>.

> **Note**: <span class="simpara"> Most systems require root access to
> create a server socket on a port below 1024. </span>

**示例 \#2 Using UDP server sockets**

``` php
<?php
$socket = stream_socket_server("udp://127.0.0.1:1113", $errno, $errstr, STREAM_SERVER_BIND);
if (!$socket) {
    die("$errstr ($errno)");
}

do {
    $pkt = stream_socket_recvfrom($socket, 1, 0, $peer);
    echo "$peer\n";
    stream_socket_sendto($socket, date("D M j H:i:s Y\r\n"), 0, $peer);
} while ($pkt !== false);

?>
```

### 注释

> **Note**: <span class="simpara">当指定数值型的 IPv6 地址（例如
> *fe80::1*）时必须用方括号将 IP 围起来——例如，
> *tcp://\[fe80::1\]:80*。</span>

### 参见

-   <span class="function">stream\_socket\_client</span>
-   <span class="function">stream\_set\_blocking</span>
-   <span class="function">stream\_set\_timeout</span>
-   <span class="function">fgets</span>
-   <span class="function">fgetss</span>
-   <span class="function">fwrite</span>
-   <span class="function">fclose</span>
-   <span class="function">feof</span>
-   <a href="/ref/curl.html" class="link">Curl extension</a>

stream\_socket\_shutdown
========================

Shutdown a full-duplex connection

### 说明

<span class="type">bool</span> <span
class="methodname">stream\_socket\_shutdown</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
, <span class="methodparam"><span class="type">int</span> `$mode`</span>
)

Shutdowns (partially or not) a full-duplex connection.

> **Note**:
>
> The associated buffer, or buffers, may or may not be emptied.

### 参数

`stream`  
An open stream (opened with <span
class="function">stream\_socket\_client</span>, for example)

`mode`  
One of the following constants: **`STREAM_SHUT_RD`** (disable further
receptions), **`STREAM_SHUT_WR`** (disable further transmissions) or
**`STREAM_SHUT_RDWR`** (disable further receptions and transmissions).

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 A <span class="function">stream\_socket\_shutdown</span>
example**

``` php
<?php

$server = stream_socket_server('tcp://127.0.0.1:1337');
$client = stream_socket_client('tcp://127.0.0.1:1337');

var_dump(fputs($client, "hello"));

stream_socket_shutdown($client, STREAM_SHUT_WR);
var_dump(fputs($client, "hello")); // doesn't work now

?>
```

以上例程的输出类似于：

    int(5)

    Notice: fputs(): send of 5 bytes failed with errno=32 Broken pipe in test.php on line 9
    int(0)

### 参见

-   <span class="function">fclose</span>

stream\_supports\_lock
======================

Tells whether the stream supports locking

### 说明

<span class="type">bool</span> <span
class="methodname">stream\_supports\_lock</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
)

Tells whether the stream supports locking through <span
class="function">flock</span>.

### 参数

`stream`  
The stream to check.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">flock</span>

stream\_wrapper\_register
=========================

注册一个用 PHP 类实现的 URL 封装协议

### 说明

<span class="type">bool</span> <span
class="methodname">stream\_wrapper\_register</span> ( <span
class="methodparam"><span class="type">string</span> `$protocol`</span>
, <span class="methodparam"><span class="type">string</span>
`$classname`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags` <span class="initializer"> =
0</span></span> \] )

允许用户实现自定义的协议处理器和流，用于所有其它的文件系统函数中（例如
<span class="function">fopen</span>，<span class="function">fread</span>
等）。

### 参数

`protocol`  
待注册的封装的名字。

`classname`  
实现了`protocol`的类名。

`flags`  
Should be set to **`STREAM_IS_URL`** if `protocol` is a URL protocol.
Default is 0, local stream.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

当 `protocol` 已经有处理者时，<span
class="function">stream\_wrapper\_register</span> 将返回**`false`**

### 更新日志

| 版本  | 说明               |
|-------|--------------------|
| 5.2.4 | 添加 `flags` 参数. |

### 范例

**示例 \#1 如何注册一个 stream wrapper**

``` php
<?php
$existed = in_array("var", stream_get_wrappers());
if ($existed) {
    stream_wrapper_unregister("var");
}
stream_wrapper_register("var", "VariableStream");
$myvar = "";

$fp = fopen("var://myvar", "r+");

fwrite($fp, "line1\n");
fwrite($fp, "line2\n");
fwrite($fp, "line3\n");

rewind($fp);
while (!feof($fp)) {
    echo fgets($fp);
}
fclose($fp);
var_dump($myvar);

if ($existed) {
    stream_wrapper_restore("var");
}

?>
```

以上例程会输出：

    line1
    line2
    line3
    string(18) "line1
    line2
    line3
    "

### 参见

-   The
    <a href="/class/streamwrapper.html" class="xref">streamWrapper</a>
    prototype class
-   <a href="/stream/examples.html#Example%20class%20registered%20as%20stream%20wrapper" class="xref"></a>
-   <span class="function">stream\_wrapper\_unregister</span>
-   <span class="function">stream\_wrapper\_restore</span>
-   <span class="function">stream\_get\_wrappers</span>

stream\_wrapper\_restore
========================

Restores a previously unregistered built-in wrapper

### 说明

<span class="type">bool</span> <span
class="methodname">stream\_wrapper\_restore</span> ( <span
class="methodparam"><span class="type">string</span> `$protocol`</span>
)

Restores a built-in wrapper previously unregistered with <span
class="function">stream\_wrapper\_unregister</span>.

### 参数

`protocol`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

stream\_wrapper\_unregister
===========================

Unregister a URL wrapper

### 说明

<span class="type">bool</span> <span
class="methodname">stream\_wrapper\_unregister</span> ( <span
class="methodparam"><span class="type">string</span> `$protocol`</span>
)

Allows you to disable an already defined stream wrapper. Once the
wrapper has been disabled you may override it with a user-defined
wrapper using <span class="function">stream\_wrapper\_register</span> or
reenable it later on with <span
class="function">stream\_wrapper\_restore</span>.

### 参数

`protocol`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

**目录**

-   [stream\_bucket\_append](/ref/stream.html#stream_bucket_append) —
    Append bucket to brigade
-   [stream\_bucket\_make\_writeable](/ref/stream.html#stream_bucket_make_writeable)
    — Return a bucket object from the brigade for operating on
-   [stream\_bucket\_new](/ref/stream.html#stream_bucket_new) — Create a
    new bucket for use on the current stream
-   [stream\_bucket\_prepend](/ref/stream.html#stream_bucket_prepend) —
    Prepend bucket to brigade
-   [stream\_context\_create](/ref/stream.html#stream_context_create) —
    创建资源流上下文
-   [stream\_context\_get\_default](/ref/stream.html#stream_context_get_default)
    — Retrieve the default stream context
-   [stream\_context\_get\_options](/ref/stream.html#stream_context_get_options)
    — 获取资源流/数据包/上下文的参数
-   [stream\_context\_get\_params](/ref/stream.html#stream_context_get_params)
    — Retrieves parameters from a context
-   [stream\_context\_set\_default](/ref/stream.html#stream_context_set_default)
    — Set the default stream context
-   [stream\_context\_set\_option](/ref/stream.html#stream_context_set_option)
    — 对资源流、数据包或者上下文设置参数
-   [stream\_context\_set\_params](/ref/stream.html#stream_context_set_params)
    — Set parameters for a stream/wrapper/context
-   [stream\_copy\_to\_stream](/ref/stream.html#stream_copy_to_stream) —
    Copies data from one stream to another
-   [stream\_filter\_append](/ref/stream.html#stream_filter_append) —
    Attach a filter to a stream
-   [stream\_filter\_prepend](/ref/stream.html#stream_filter_prepend) —
    Attach a filter to a stream
-   [stream\_filter\_register](/ref/stream.html#stream_filter_register)
    — Register a user defined stream filter
-   [stream\_filter\_remove](/ref/stream.html#stream_filter_remove) —
    从资源流里移除某个过滤器
-   [stream\_get\_contents](/ref/stream.html#stream_get_contents) —
    读取资源流到一个字符串
-   [stream\_get\_filters](/ref/stream.html#stream_get_filters) —
    获取已注册的数据流过滤器列表
-   [stream\_get\_line](/ref/stream.html#stream_get_line) —
    从资源流里读取一行直到给定的定界符
-   [stream\_get\_meta\_data](/ref/stream.html#stream_get_meta_data) —
    从封装协议文件指针中取得报头／元数据
-   [stream\_get\_transports](/ref/stream.html#stream_get_transports) —
    获取已注册的套接字传输协议列表
-   [stream\_get\_wrappers](/ref/stream.html#stream_get_wrappers) —
    获取已注册的流类型
-   [stream\_is\_local](/ref/stream.html#stream_is_local) — Checks if a
    stream is a local stream
-   [stream\_isatty](/ref/stream.html#stream_isatty) — Check if a stream
    is a TTY
-   [stream\_notification\_callback](/ref/stream.html#stream_notification_callback)
    — A callback function for the notification context parameter
-   [stream\_register\_wrapper](/ref/stream.html#stream_register_wrapper)
    — 别名 stream\_wrapper\_register
-   [stream\_resolve\_include\_path](/ref/stream.html#stream_resolve_include_path)
    — Resolve filename against the include path
-   [stream\_select](/ref/stream.html#stream_select) — Runs the
    equivalent of the select() system call on the given arrays of
    streams with a timeout specified by tv\_sec and tv\_usec
-   [stream\_set\_blocking](/ref/stream.html#stream_set_blocking) —
    为资源流设置阻塞或者阻塞模式
-   [stream\_set\_chunk\_size](/ref/stream.html#stream_set_chunk_size) —
    设置资源流区块大小
-   [stream\_set\_read\_buffer](/ref/stream.html#stream_set_read_buffer)
    — Set read file buffering on the given stream
-   [stream\_set\_timeout](/ref/stream.html#stream_set_timeout) — Set
    timeout period on a stream
-   [stream\_set\_write\_buffer](/ref/stream.html#stream_set_write_buffer)
    — Sets write file buffering on the given stream
-   [stream\_socket\_accept](/ref/stream.html#stream_socket_accept) —
    接受由 stream\_socket\_server 创建的套接字连接
-   [stream\_socket\_client](/ref/stream.html#stream_socket_client) —
    Open Internet or Unix domain socket connection
-   [stream\_socket\_enable\_crypto](/ref/stream.html#stream_socket_enable_crypto)
    — Turns encryption on/off on an already connected socket
-   [stream\_socket\_get\_name](/ref/stream.html#stream_socket_get_name)
    — 获取本地或者远程的套接字名称
-   [stream\_socket\_pair](/ref/stream.html#stream_socket_pair) —
    创建一对完全一样的网络套接字连接流
-   [stream\_socket\_recvfrom](/ref/stream.html#stream_socket_recvfrom)
    — Receives data from a socket, connected or not
-   [stream\_socket\_sendto](/ref/stream.html#stream_socket_sendto) —
    Sends a message to a socket, whether it is connected or not
-   [stream\_socket\_server](/ref/stream.html#stream_socket_server) —
    Create an Internet or Unix domain server socket
-   [stream\_socket\_shutdown](/ref/stream.html#stream_socket_shutdown)
    — Shutdown a full-duplex connection
-   [stream\_supports\_lock](/ref/stream.html#stream_supports_lock) —
    Tells whether the stream supports locking
-   [stream\_wrapper\_register](/ref/stream.html#stream_wrapper_register)
    — 注册一个用 PHP 类实现的 URL 封装协议
-   [stream\_wrapper\_restore](/ref/stream.html#stream_wrapper_restore)
    — Restores a previously unregistered built-in wrapper
-   [stream\_wrapper\_unregister](/ref/stream.html#stream_wrapper_unregister)
    — Unregister a URL wrapper
