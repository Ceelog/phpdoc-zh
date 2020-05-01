字符串过滤器
------------

每个过滤器都正如其名字暗示的那样工作并与内置的 PHP
字符串函数的行为相对应。对于指定过滤器的更多信息，请参考该函数的手册页。

*string.rot13*（自 PHP 4.3.0 起）使用此过滤器等同于用 <span
class="function">str\_rot13</span>函数处理所有的流数据。

**示例 \#1 string.rot13**

``` php
<?php
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'string.rot13');
fwrite($fp, "This is a test.\n");
/* Outputs:  Guvf vf n grfg.   */
?>
```

*string.toupper*（自 PHP 5.0.0 起）使用此过滤器等同于用 <span
class="function">strtoupper</span>函数处理所有的流数据。

**示例 \#2 string.toupper**

``` php
<?php
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'string.toupper');
fwrite($fp, "This is a test.\n");
/* Outputs:  THIS IS A TEST.   */
?>
```

*string.tolower*（自 PHP 5.0.0 起）使用此过滤器等同于用 <span
class="function">strtolower</span>函数处理所有的流数据。

**示例 \#3 string.tolower**

``` php
<?php
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'string.tolower');
fwrite($fp, "This is a test.\n");
/* Outputs:  this is a test.   */
?>
```
