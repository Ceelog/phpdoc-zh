SeasLog
=======

**目录**

-   [简介](/intro/seaslog.html)
-   [安装／配置](/seaslog/setup.html)
    -   [需求](/seaslog/setup.html#需求)
    -   [安装](/seaslog/setup.html#安装)
    -   [运行时配置](/seaslog/setup.html#运行时配置)
    -   [资源类型](/seaslog/setup.html#资源类型)
-   [预定义常量](/seaslog/constants.html)
-   [范例](/seaslog/examples.html)
-   [Seaslog 函数](/ref/seaslog.html)
    -   [seaslog\_get\_author](/ref/seaslog.html#seaslog_get_author) —
        获取 SeasLog 作者
    -   [seaslog\_get\_version](/ref/seaslog.html#seaslog_get_version) —
        获取 SeasLog 的版本
-   [SeasLog](/class/seaslog.html) — The SeasLog class
    -   [SeasLog::alert](/class/seaslog.html#SeasLog::alert) — 记录
        alert 日志
    -   [SeasLog::analyzerCount](/class/seaslog.html#SeasLog::analyzerCount)
        — Get log count by level, log\_path and key\_word
    -   [SeasLog::analyzerDetail](/class/seaslog.html#SeasLog::analyzerDetail)
        — Get log detail by level, log\_path, key\_word, start, limit,
        order
    -   [SeasLog::closeLoggerStream](/class/seaslog.html#SeasLog::closeLoggerStream)
        — Manually release stream flow from logger
    -   [SeasLog::\_\_construct](/class/seaslog.html#SeasLog::__construct)
        — Description
    -   [SeasLog::critical](/class/seaslog.html#SeasLog::critical) —
        记录 critical 日志
    -   [SeasLog::debug](/class/seaslog.html#SeasLog::debug) — 记录
        debug 日志
    -   [SeasLog::\_\_destruct](/class/seaslog.html#SeasLog::__destruct)
        — Description
    -   [SeasLog::emergency](/class/seaslog.html#SeasLog::emergency) —
        记录 emergency 日志
    -   [SeasLog::error](/class/seaslog.html#SeasLog::error) — 记录
        error 日志
    -   [SeasLog::flushBuffer](/class/seaslog.html#SeasLog::flushBuffer)
        — 将日志缓存刷新到介质中，文件介质，或者发送到远端的 TCP/UDP
        服务地址。
    -   [SeasLog::getBasePath](/class/seaslog.html#SeasLog::getBasePath)
        — 获得 SeasLog 根目录
    -   [SeasLog::getBuffer](/class/seaslog.html#SeasLog::getBuffer) —
        获取内存中的日志缓存数组
    -   [SeasLog::getBufferEnabled](/class/seaslog.html#SeasLog::getBufferEnabled)
        — Determin if buffer enabled
    -   [SeasLog::getDatetimeFormat](/class/seaslog.html#SeasLog::getDatetimeFormat)
        — 获取 SeasLog 日期格式
    -   [SeasLog::getLastLogger](/class/seaslog.html#SeasLog::getLastLogger)
        — 获得 SeasLog 最近的一次 Logger 名称
    -   [SeasLog::getRequestID](/class/seaslog.html#SeasLog::getRequestID)
        — 获得当前 SeasLog 中用于区分请求的 request\_id
    -   [SeasLog::getRequestVariable](/class/seaslog.html#SeasLog::getRequestVariable)
        — Get SeasLog request variable
    -   [SeasLog::info](/class/seaslog.html#SeasLog::info) — Record info
        log information
    -   [SeasLog::log](/class/seaslog.html#SeasLog::log) —
        公共的日志记录函数
    -   [SeasLog::notice](/class/seaslog.html#SeasLog::notice) — 记录
        notice 日志
    -   [SeasLog::setBasePath](/class/seaslog.html#SeasLog::setBasePath)
        — 设置 SeasLog 根目录
    -   [SeasLog::setDatetimeFormat](/class/seaslog.html#SeasLog::setDatetimeFormat)
        — 设置 SeasLog 日期格式
    -   [SeasLog::setLogger](/class/seaslog.html#SeasLog::setLogger) —
        设置 SeasLog 的 Logger 名
    -   [SeasLog::setRequestID](/class/seaslog.html#SeasLog::setRequestID)
        — 设置可以由 SeasLog 用于区分请求的 request\_id
    -   [SeasLog::setRequestVariable](/class/seaslog.html#SeasLog::setRequestVariable)
        — Manually set SeasLog request variable
    -   [SeasLog::warning](/class/seaslog.html#SeasLog::warning) —
        Record warning log information

简介
----

类摘要
------

**SeasLog**

<span class="ooclass"> class **SeasLog** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">alert</span> ( <span class="methodparam"><span
class="type">string</span> `$message`</span> \[, <span
class="methodparam"><span class="type">array</span> `$content`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$logger`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">analyzerCount</span> ( <span
class="methodparam"><span class="type">string</span> `$level`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$log_path`</span> \[, <span class="methodparam"><span
class="type">string</span> `$key_word`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">analyzerDetail</span> ( <span
class="methodparam"><span class="type">string</span> `$level`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$log_path`</span> \[, <span class="methodparam"><span
class="type">string</span> `$key_word`</span> \[, <span
class="methodparam"><span class="type">int</span> `$start`</span> \[,
<span class="methodparam"><span class="type">int</span> `$limit`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$order`</span> \]\]\]\]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">closeLoggerStream</span> ( <span
class="methodparam"><span class="type">int</span> `$model`</span> ,
<span class="methodparam"><span class="type">string</span>
`$logger`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">critical</span> ( <span class="methodparam"><span
class="type">string</span> `$message`</span> \[, <span
class="methodparam"><span class="type">array</span> `$content`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$logger`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">debug</span> ( <span class="methodparam"><span
class="type">string</span> `$message`</span> \[, <span
class="methodparam"><span class="type">array</span> `$content`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$logger`</span> \]\] )

<span class="modifier">public</span> <span
class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">emergency</span> ( <span class="methodparam"><span
class="type">string</span> `$message`</span> \[, <span
class="methodparam"><span class="type">array</span> `$content`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$logger`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">error</span> ( <span class="methodparam"><span
class="type">string</span> `$message`</span> \[, <span
class="methodparam"><span class="type">array</span> `$content`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$logger`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">flushBuffer</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Seaslog::getBasePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getBuffer</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">getBufferEnabled</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getDatetimeFormat</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getLastLogger</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getRequestID</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">getRequestVariable</span> ( <span
class="methodparam"><span class="type">int</span> `$key`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">info</span> ( <span class="methodparam"><span
class="type">string</span> `$message`</span> \[, <span
class="methodparam"><span class="type">array</span> `$content`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$logger`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">log</span> ( <span class="methodparam"><span
class="type">string</span> `$level`</span> \[, <span
class="methodparam"><span class="type">string</span> `$message`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">string</span> `$logger`</span> \]\]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">notice</span> ( <span class="methodparam"><span
class="type">string</span> `$message`</span> \[, <span
class="methodparam"><span class="type">array</span> `$content`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$logger`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">setBasePath</span> ( <span class="methodparam"><span
class="type">string</span> `$base_path`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">setDatetimeFormat</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">setLogger</span> ( <span class="methodparam"><span
class="type">string</span> `$logger`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">setRequestID</span> ( <span class="methodparam"><span
class="type">string</span> `$request_id`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">setRequestVariable</span> ( <span
class="methodparam"><span class="type">int</span> `$key`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">warning</span> ( <span class="methodparam"><span
class="type">string</span> `$message`</span> \[, <span
class="methodparam"><span class="type">array</span> `$content`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$logger`</span> \]\] )

}

SeasLog::alert
==============

记录 alert 日志

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::alert</span> ( <span
class="methodparam"><span class="type">string</span> `$message`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">string</span> `$logger`</span> \]\] )

记录 alert 日志

> **Note**:
>
> "ALERT" -必须立即采取行动的紧急事件 需要立即通知相关人员紧急修复。

### 参数

`message`  
日志的消息

`content`  
"消息"包含占位符，实现用 content 数组中的值替换这些占位符。 例如'消息'是
\`log info from {NAME}\`, '内容'是 \`array('NAME' =\> neeke)\`，
日志信息是 \`log info from neeke\`

`logger`  
当函数调用 SeasLog::setLogger() 时，就像临时 logger
一样，在第三个参数中使用这个"logger"。 如果 \`logger\` 为NULL 或
""，那么 SeasLog 将使用由 <span
class="methodname">SeasLog::setLogger</span>设置的最新日志记录程序。

### 返回值

记录日志信息成功返回 TRUE，失败返回 FALSE。

### 范例

**示例 \#1 <span class="function">SeasLog::alert</span>例子**

``` php
<?php

var_dump(SeasLog::alert('log message'));

//with content
var_dump(SeasLog::alert('log message from {NAME}',array('NAME' => 'neeke')));

//with tmp logger
var_dump(SeasLog::alert('log message from {NAME}',array('NAME' => 'neeke'),'tmp_logger'));

var_dump(SeasLog::getBuffer());

?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    bool(true)
    array(2) {
      ["/var/log/www/default/20180707.log"]=>
      array(2) {
        [0]=>
        string(81) "2018-07-07 11:45:49 | ALERT | 73263 | 5b40376d1067c | 1530935149.68 | log message
    "
        [1]=>
        string(92) "2018-07-07 11:45:49 | ALERT | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
      ["/var/log/www/tmp_logger/20180707.log"]=>
      array(1) {
        [0]=>
        string(92) "2018-07-07 11:45:49 | ALERT | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
    }

### 参见

-   <a href="/seaslog/setup.html#Seaslog%20内置变量表" class="link">seaslog.default_template</a>
-   <span class="methodname">SeasLog::debug</span>
-   <span class="methodname">SeasLog::info</span>
-   <span class="methodname">SeasLog::notice</span>
-   <span class="methodname">SeasLog::warning</span>
-   <span class="methodname">SeasLog::error</span>
-   <span class="methodname">SeasLog::critical</span>
-   <span class="methodname">SeasLog::emergency</span>
-   <span class="methodname">SeasLog::log</span>

SeasLog::analyzerCount
======================

Get log count by level, log\_path and key\_word

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">SeasLog::analyzerCount</span> ( <span
class="methodparam"><span class="type">string</span> `$level`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$log_path`</span> \[, <span class="methodparam"><span
class="type">string</span> `$key_word`</span> \]\] )

\`SeasLog\` get count value of \`grep -ai '{level}' \| grep -aic
'{key\_word}'\` use system pipe and return to PHP (array or int).

### 参数

`level`  
String. The log information level.

`log_path`  
String. The log information path.

`key_word`  
String. The search key word for log information.

### 返回值

If \`level\` is SEASLOG\_ALL or Empty, return all levels count as
\`array\`. If \`level\` is SEASLOG\_INFO or the other level, return
count as \`int\`.

### 范例

**示例 \#1 <span class="function">SeasLog::analyzerCount</span>
example**

``` php
<?php

$countResult1 = SeasLog::analyzerCount();

//with `level`
$countResult2 = SeasLog::analyzerCount(SEASLOG_DEBUG);

//with `level` and `log_path`
$countResult3 = SeasLog::analyzerCount(SEASLOG_ERROR,date('Ymd',time()));

//with `level` and `key_word`
$countResult4 = SeasLog::analyzerCount(SEASLOG_DEBUG,NULL,'accessToken');

var_dump($countResult1,$countResult2,$countResult3,$countResult4);

?>
```

以上例程的输出类似于：

    array(8) {
      ["DEBUG"]=>
      int(180)
      ["INFO"]=>
      int(214)
      ["NOTICE"]=>
      int(0)
      ["WARNING"]=>
      int(0)
      ["ERROR"]=>
      int(228)
      ["CRITICAL"]=>
      int(244)
      ["ALERT"]=>
      int(1)
      ["EMERGENCY"]=>
      int(0)
    }

    int(180)

    int(228)

    int(29)

### 参见

-   <span class="methodname">SeasLog::analyzerDetail</span>

SeasLog::analyzerDetail
=======================

Get log detail by level, log\_path, key\_word, start, limit, order

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">SeasLog::analyzerDetail</span> ( <span
class="methodparam"><span class="type">string</span> `$level`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$log_path`</span> \[, <span class="methodparam"><span
class="type">string</span> `$key_word`</span> \[, <span
class="methodparam"><span class="type">int</span> `$start`</span> \[,
<span class="methodparam"><span class="type">int</span> `$limit`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$order`</span> \]\]\]\]\] )

\`SeasLog\` get results of \`grep -ai '{level}' \| grep -ai
'{key\_word}' \| sed -n '{start},{limit}'p\` use system pipe and return
array to PHP.

### 参数

`level`  
String. The log information level.

`log_path`  
String. The log information path.

`key_word`  
String. The search key word for log information.

`start`  
Int. Default is \`1\`.

`limit`  
Int. Default is \`20\`.

`order`  
Int. Default is
<a href="/seaslog/constants.html#" class="link">SEASLOG_DETAIL_ORDER_ASC</a>.
See also:

-   <a href="/seaslog/constants.html#" class="link">SEASLOG_DETAIL_ORDER_ASC</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_DETAIL_ORDER_DESC</a>

### 返回值

Return results as array.

> **Note**:
>
> When \`start\`,\`limit\` is not NULL and in Windows, SeasLog will
> threw exception with message 'Param start and limit don't support
> Windows'.

### 范例

**示例 \#1 <span class="function">SeasLog::analyzerDetail</span>
example**

``` php
<?php

$result1 = SeasLog::analyzerDetail(SEASLOG_ERROR);

//with `logger` and `key_word`
$result2 = SeasLog::analyzerDetail(SEASLOG_ERROR,'test/logger/','neeke');

//with `start` and `limit`
$result3 = SeasLog::analyzerDetail(SEASLOG_ERROR,'test/logger/','neeke',1,2);

var_dump($result1,$result2,$result3);
?>
```

以上例程的输出类似于：

    array(20) {
      [0]=>
      string(93) "2018-07-09 12:52:53 | ERROR | 12247 | 5b42ea2580e51 | 1531111973.528 | log message from neeke"
      [1]=>
      string(93) "2018-07-09 12:52:54 | ERROR | 12256 | 5b42ea26d6657 | 1531111974.878 | log message from neeke"
      [2]=>
      string(93) "2018-07-09 12:52:55 | ERROR | 12265 | 5b42ea277b8d4 | 1531111975.506 | log message from neeke"
      [3]=>
      string(104) "2018-07-09 12:52:55 | ERROR | 12274 | 5b42ea27db5dc | 1531111975.898 | log message from the other people"
    ...
    }

    array(3) {
      [0]=>
      string(93) "2018-07-09 12:52:53 | ERROR | 12247 | 5b42ea2580e51 | 1531111973.528 | log message from neeke"
      [1]=>
      string(93) "2018-07-09 12:52:54 | ERROR | 12256 | 5b42ea26d6657 | 1531111974.878 | log message from neeke"
      [2]=>
      string(93) "2018-07-09 12:52:55 | ERROR | 12265 | 5b42ea277b8d4 | 1531111975.506 | log message from neeke"
    }

    array(2) {
      [0]=>
      string(93) "2018-07-09 12:52:53 | ERROR | 12247 | 5b42ea2580e51 | 1531111973.528 | log message from neeke"
      [1]=>
      string(93) "2018-07-09 12:52:54 | ERROR | 12256 | 5b42ea26d6657 | 1531111974.878 | log message from neeke"
    }

### 参见

-   <span class="methodname">SeasLog::analyzerCount</span>

SeasLog::closeLoggerStream
==========================

Manually release stream flow from logger

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::closeLoggerStream</span> ( <span
class="methodparam"><span class="type">int</span> `$model`</span> ,
<span class="methodparam"><span class="type">string</span>
`$logger`</span> )

Manually release stream flow from logger. SeasLog caches the stream
handle opened by the log logger to save the overhead of creating a
stream. The handle will be automatically released at the end of the
request. If in CLI mode, the process will also automatically release
when it exits. Or you can use the following functions to manually
release(manually release function needs to update SeasLog 1.8.6 or
updated version).

### 参数

`model`  
Constant int.

-   <a href="/seaslog/constants.html#" class="link">SEASLOG_CLOSE_LOGGER_STREAM_MOD_ALL</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_CLOSE_LOGGER_STREAM_MOD_ASSIGN</a>

`logger`  
The logger name.

### 返回值

Return TRUE on released stream flow success, FALSE on failure.

### 范例

**示例 \#1 <span class="methodname">SeasLog::closeLoggerStream</span>
example**

``` php
<?php

var_dump(SeasLog::closeLoggerStream());
var_dump(SeasLog::closeLoggerStream(SEASLOG_CLOSE_LOGGER_STREAM_MOD_ALL));
var_dump(SeasLog::closeLoggerStream(SEASLOG_CLOSE_LOGGER_STREAM_MOD_ASSIGN, 'logger_name'));

?>
```

以上例程的输出类似于：


    bool(true)
    bool(true)
    bool(true)

### 参见

-   <span class="methodname">SeasLog::setLogger</span>
-   <span class="methodname">SeasLog::getLastLogger</span>

SeasLog::\_\_construct
======================

Description

### 说明

<span class="modifier">public</span> <span
class="methodname">SeasLog::\_\_construct</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 范例

**示例 \#1 <span class="function">SeasLog::\_\_construct</span>
example**

``` php
<?php

/* ... */

?>
```

以上例程的输出类似于：

    ...

SeasLog::critical
=================

记录 critical 日志

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::critical</span> ( <span
class="methodparam"><span class="type">string</span> `$message`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">string</span> `$logger`</span> \]\] )

记录 critical 日志

> **Note**:
>
> "CRITICAL" - 紧急情况、需要立刻进行修复、程序组件不可用

### 参数

`message`  
日志的消息

`content`  
"消息"包含占位符，实现用 content 数组中的值替换这些占位符。 例如'消息'是
\`log info from {NAME}\`, '内容'是 \`array('NAME' =\> neeke)\`，
日志信息是 \`log info from neeke\`

`logger`  
当函数调用 SeasLog::setLogger() 时，就像临时 logger
一样，在第三个参数中使用这个"logger"。 如果 \`logger\` 为NULL 或
""，那么SeasLog将使用由 <span
class="methodname">SeasLog::setLogger</span>设置的最新日志记录程序。

### 返回值

记录日志信息成功返回 TRUE，失败返回 FALSE。

### 范例

**示例 \#1 <span class="function">SeasLog::critical</span> example**

``` php
<?php

var_dump(SeasLog::critical('log message'));

//with content
var_dump(SeasLog::critical('log message from {NAME}',array('NAME' => 'neeke')));

//with tmp logger
var_dump(SeasLog::critical('log message from {NAME}',array('NAME' => 'neeke'),'tmp_logger'));

var_dump(SeasLog::getBuffer());

?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    bool(true)
    array(2) {
      ["/var/log/www/default/20180707.log"]=>
      array(2) {
        [0]=>
        string(81) "2018-07-07 11:45:49 | CRITICAL | 73263 | 5b40376d1067c | 1530935149.68 | log message
    "
        [1]=>
        string(92) "2018-07-07 11:45:49 | CRITICAL | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
      ["/var/log/www/tmp_logger/20180707.log"]=>
      array(1) {
        [0]=>
        string(92) "2018-07-07 11:45:49 | CRITICAL | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
    }

### 参见

-   <a href="/seaslog/setup.html#Seaslog%20内置变量表" class="link">seaslog.default_template</a>
-   <span class="methodname">SeasLog::debug</span>
-   <span class="methodname">SeasLog::info</span>
-   <span class="methodname">SeasLog::notice</span>
-   <span class="methodname">SeasLog::warning</span>
-   <span class="methodname">SeasLog::error</span>
-   <span class="methodname">SeasLog::alert</span>
-   <span class="methodname">SeasLog::emergency</span>
-   <span class="methodname">SeasLog::log</span>

SeasLog::debug
==============

记录 debug 日志

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::debug</span> ( <span
class="methodparam"><span class="type">string</span> `$message`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">string</span> `$logger`</span> \]\] )

记录debug日志

> **Note**:
>
> "DEBUG" - debug 信息、细粒度信息事件

### 参数

`message`  
日志的消息

`content`  
"消息"包含占位符，实现用 content 数组中的值替换这些占位符。 例如'消息'是
\`log info from {NAME}\`, '内容'是 \`array('NAME' =\> neeke)\`，
日志信息是 \`log info from neeke\`

`logger`  
当函数调用 SeasLog::setLogger() 时，就像临时 logger
一样，在第三个参数中使用这个"logger"。 如果 \`logger\` 为NULL 或
""，那么 SeasLog 将使用由 <span
class="methodname">SeasLog::setLogger</span>设置的最新日志记录程序。

### 返回值

记录日志信息成功返回 TRUE，失败返回 FALSE。

### 范例

**示例 \#1 <span class="function">SeasLog::debug</span> example**

``` php
<?php

var_dump(SeasLog::debug('log message'));

//with content
var_dump(SeasLog::debug('log message from {NAME}',array('NAME' => 'neeke')));

//with tmp logger
var_dump(SeasLog::debug('log message from {NAME}',array('NAME' => 'neeke'),'tmp_logger'));

var_dump(SeasLog::getBuffer());

?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    bool(true)
    array(2) {
      ["/var/log/www/default/20180707.log"]=>
      array(2) {
        [0]=>
        string(81) "2018-07-07 11:45:49 | DEBUG | 73263 | 5b40376d1067c | 1530935149.68 | log message
    "
        [1]=>
        string(92) "2018-07-07 11:45:49 | DEBUG | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
      ["/var/log/www/tmp_logger/20180707.log"]=>
      array(1) {
        [0]=>
        string(92) "2018-07-07 11:45:49 | DEBUG | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
    }

### 参见

-   <a href="/seaslog/setup.html#Seaslog%20内置变量表" class="link">seaslog.default_template</a>
-   <span class="methodname">SeasLog::info</span>
-   <span class="methodname">SeasLog::notice</span>
-   <span class="methodname">SeasLog::warning</span>
-   <span class="methodname">SeasLog::error</span>
-   <span class="methodname">SeasLog::critical</span>
-   <span class="methodname">SeasLog::alert</span>
-   <span class="methodname">SeasLog::emergency</span>
-   <span class="methodname">SeasLog::log</span>

SeasLog::\_\_destruct
=====================

Description

### 说明

<span class="modifier">public</span> <span
class="methodname">SeasLog::\_\_destruct</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

### 范例

**示例 \#1 <span class="function">SeasLog::\_\_destruct</span> example**

``` php
<?php

/* ... */

?>
```

以上例程的输出类似于：

    ...

SeasLog::emergency
==================

记录 emergency 日志

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::emergency</span> ( <span
class="methodparam"><span class="type">string</span> `$message`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">string</span> `$logger`</span> \]\] )

记录 emergency 日志

> **Note**:
>
> "EMERGENCY" - 系统不可用。

### 参数

`message`  
日志的消息

`content`  
"消息"包含占位符，实现用 content 数组中的值替换这些占位符。 例如'消息'是
\`log info from {NAME}\`, '内容'是 \`array('NAME' =\> neeke)\`，
日志信息是 \`log info from neeke\`

`logger`  
当函数调用 SeasLog::setLogger() 时，就像临时 logger
一样，在第三个参数中使用这个"logger"。 如果 \`logger\` 为 NULL 或
""，那么 SeasLog 将使用由 <span
class="methodname">SeasLog::setLogger</span>设置的最新 Logger。

### 返回值

记录日志信息成功返回 TRUE，失败返回 FALSE。

### 范例

**示例 \#1 <span class="function">SeasLog::emergency</span> example**

``` php
<?php

var_dump(SeasLog::emergency('log message'));

//with content
var_dump(SeasLog::emergency('log message from {NAME}',array('NAME' => 'neeke')));

//with tmp logger
var_dump(SeasLog::emergency('log message from {NAME}',array('NAME' => 'neeke'),'tmp_logger'));

var_dump(SeasLog::getBuffer());

?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    bool(true)
    array(2) {
      ["/var/log/www/default/20180707.log"]=>
      array(2) {
        [0]=>
        string(81) "2018-07-07 11:45:49 | EMERGENCY | 73263 | 5b40376d1067c | 1530935149.68 | log message
    "
        [1]=>
        string(92) "2018-07-07 11:45:49 | EMERGENCY | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
      ["/var/log/www/tmp_logger/20180707.log"]=>
      array(1) {
        [0]=>
        string(92) "2018-07-07 11:45:49 | EMERGENCY | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
    }

### 参见

-   <a href="/seaslog/setup.html#Seaslog%20内置变量表" class="link">seaslog.default_template</a>
-   <span class="methodname">SeasLog::debug</span>
-   <span class="methodname">SeasLog::info</span>
-   <span class="methodname">SeasLog::notice</span>
-   <span class="methodname">SeasLog::warning</span>
-   <span class="methodname">SeasLog::error</span>
-   <span class="methodname">SeasLog::critical</span>
-   <span class="methodname">SeasLog::alert</span>
-   <span class="methodname">SeasLog::log</span>

SeasLog::error
==============

记录 error 日志

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::error</span> ( <span
class="methodparam"><span class="type">string</span> `$message`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">string</span> `$logger`</span> \]\] )

记录 error 日志

> **Note**:
>
> "ERROR" -
> 运行时出现的错误、不必要立即进行修复、不影响整个逻辑的运行、需要记录并做检测

### 参数

`message`  
日志的消息

`content`  
"消息"包含占位符，实现用 content 数组中的值替换这些占位符。 例如'消息'是
\`log info from {NAME}\`, '内容'是 \`array('NAME' =\> neeke)\`，
日志信息是 \`log info from neeke\`

`logger`  
当函数调用 SeasLog::setLogger() 时，就像临时 logger
一样，在第三个参数中使用这个"logger"。 如果 \`logger\` 为NULL 或
""，那么 SeasLog 将使用由 <span
class="methodname">SeasLog::setLogger</span>设置的最新日志记录程序。

### 返回值

记录日志信息成功返回 TRUE，失败返回 FALSE。

### 范例

**示例 \#1 <span class="function">SeasLog::error</span> example**

``` php
<?php

var_dump(SeasLog::error('log message'));

//with content
var_dump(SeasLog::error('log message from {NAME}',array('NAME' => 'neeke')));

//with tmp logger
var_dump(SeasLog::error('log message from {NAME}',array('NAME' => 'neeke'),'tmp_logger'));

var_dump(SeasLog::getBuffer());

?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    bool(true)
    array(2) {
      ["/var/log/www/default/20180707.log"]=>
      array(2) {
        [0]=>
        string(81) "2018-07-07 11:45:49 | ERROR | 73263 | 5b40376d1067c | 1530935149.68 | log message
    "
        [1]=>
        string(92) "2018-07-07 11:45:49 | ERROR | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
      ["/var/log/www/tmp_logger/20180707.log"]=>
      array(1) {
        [0]=>
        string(92) "2018-07-07 11:45:49 | ERROR | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
    }

### 参见

-   <a href="/seaslog/setup.html#Seaslog%20内置变量表" class="link">seaslog.default_template</a>
-   <span class="methodname">SeasLog::debug</span>
-   <span class="methodname">SeasLog::info</span>
-   <span class="methodname">SeasLog::notice</span>
-   <span class="methodname">SeasLog::warning</span>
-   <span class="methodname">SeasLog::critical</span>
-   <span class="methodname">SeasLog::alert</span>
-   <span class="methodname">SeasLog::emergency</span>
-   <span class="methodname">SeasLog::log</span>

SeasLog::flushBuffer
====================

将日志缓存刷新到介质中，文件介质，或者发送到远端的 TCP/UDP 服务地址。

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::flushBuffer</span> ( <span
class="methodparam">void</span> )

将日志缓存按照
<a href="/seaslog/setup.html#" class="link">seaslog.appender</a>
刷新到介质： 文件介质，或发送到远端的 TCP/UDP 服务地址。

> **Note**:
>
> 同时请留意：
> <a href="/seaslog/setup.html#" class="link">seaslog.appender_retry</a>
> <a href="/seaslog/setup.html#" class="link">seaslog.remote_host</a>
> <a href="/seaslog/setup.html#" class="link">seaslog.remote_port</a>

### 参数

此函数没有参数。

### 返回值

刷新成功返回 TRUE，失败返回 FALSE。

### 范例

**示例 \#1 <span class="function">SeasLog::flushBuffer</span> example**

``` php
<?php

SeasLog::info('info log');
SeasLog::debug('debug log');
var_dump(SeasLog::getBuffer());
var_dump(SeasLog::flushBuffer());
var_dump(SeasLog::getBuffer());

?>
```

以上例程的输出类似于：

    array(1) {
      ["/var/log/www/default/20180707.log"]=>
      array(2) {
        [0]=>
        string(79) "2018-07-07 10:47:58 | INFO | 71910 | 5b4029ded6009 | 1530931678.877 | info log
    "
        [1]=>
        string(81) "2018-07-07 10:47:58 | DEBUG | 71910 | 5b4029ded6009 | 1530931678.877 | debug log
    "
      }
    }
    bool(true)
    array(0) {
    }

### 参见

-   <a href="/seaslog/setup.html#" class="link">seaslog.use_buffer</a>
-   <a href="/seaslog/setup.html#" class="link">seaslog.buffer_size</a>
-   <a href="/seaslog/setup.html#" class="link">seaslog.buffer_disabled_in_cli</a>
-   <span class="methodname">SeasLog::getBufferEnabled</span>
-   <span class="methodname">SeasLog::getBuffer</span>

SeasLog::getBasePath
====================

获得 SeasLog 根目录

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Seaslog::getBasePath</span> ( <span
class="methodparam">void</span> )

使用函数 <span class="methodname">SeasLog::getBasePath</span> 可以获得在
php.ini(seaslog.ini)
中设置的<a href="/seaslog/setup.html#" class="link">seaslog.default_basepath</a>。

如果使用函数 <span
class="methodname">Seaslog::setBasePath</span>，将改变函数取值。

### 参数

此函数没有参数。

### 返回值

Return
<a href="/seaslog/setup.html#" class="link">seaslog.default_basepath</a>
as string.

### 范例

**示例 \#1 <span class="methodname">SeasLog::getBasePath</span>
example**

``` php
<?php

var_dump(SeasLog::getBasePath());

?>
```

以上例程的输出类似于：

    string(12) "/var/log/www"

SeasLog::getBuffer
==================

获取内存中的日志缓存数组

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">SeasLog::getBuffer</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

以 Array 形式返回内存中的日志缓存。

### 范例

**示例 \#1 <span class="function">SeasLog::getBuffer</span> example**

``` php
<?php

var_dump(SeasLog::info('info log'));
var_dump(SeasLog::debug('debug log'));
var_dump(SeasLog::getBuffer());

?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    array(1) {
      ["/var/log/www/default/20180707.log"]=>
      array(2) {
        [0]=>
        string(79) "2018-07-07 10:43:32 | INFO | 71785 | 5b4028d4c58d5 | 1530931412.810 | info log
    "
        [1]=>
        string(81) "2018-07-07 10:43:32 | DEBUG | 71785 | 5b4028d4c58d5 | 1530931412.810 | debug log
    "
      }
    }

### 参见

-   <a href="/seaslog/setup.html#" class="link">seaslog.use_buffer</a>
-   <a href="/seaslog/setup.html#" class="link">seaslog.buffer_size</a>
-   <a href="/seaslog/setup.html#" class="link">seaslog.buffer_disabled_in_cli</a>
-   <span class="methodname">SeasLog::getBufferEnabled</span>
-   <span class="methodname">SeasLog::flushBuffer</span>

SeasLog::getBufferEnabled
=========================

Determin if buffer enabled

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::getBufferEnabled</span> ( <span
class="methodparam">void</span> )

Result join
<a href="/seaslog/setup.html#" class="link">seaslog.use_buffer</a> and
<a href="/seaslog/setup.html#" class="link">seaslog.buffer_disabled_in_cli</a>.

### 参数

此函数没有参数。

### 返回值

Return TRUE on
<a href="/seaslog/setup.html#" class="link">seaslog.use_buffer</a> is
true. If switch
<a href="/seaslog/setup.html#" class="link">seaslog.buffer_disabled_in_cli</a>
on, and running in cli, seaslog.use\_buffer setting will be discarded,
Seaslog write to the Data Store IMMEDIATELY.

### 范例

**示例 \#1 <span class="function">SeasLog::getBufferEnabled</span>
example**

``` php
<?php

var_dump(SeasLog::getBufferEnabled());

?>
```

以上例程的输出类似于：

    bool(false)

### 参见

-   <a href="/seaslog/setup.html#" class="link">seaslog.use_buffer</a>
-   <a href="/seaslog/setup.html#" class="link">seaslog.buffer_size</a>
-   <a href="/seaslog/setup.html#" class="link">seaslog.buffer_disabled_in_cli</a>
-   <span class="methodname">SeasLog::getBuffer</span>
-   <span class="methodname">SeasLog::flushBuffer</span>

SeasLog::getDatetimeFormat
==========================

获取 SeasLog 日期格式

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">SeasLog::getDatetimeFormat</span> ( <span
class="methodparam">void</span> )

获取 SeasLog 日期格式。 使用函数 <span
class="methodname">SeasLog::getDatetimeFormat</span> 将获取
php.ini(seaslog.ini) 配置的
<a href="/seaslog/setup.html#" class="link">seaslog.default_datetime_format</a>
值。

### 参数

此函数没有参数。

### 返回值

获取 SeasLog 配置中的
<a href="/seaslog/setup.html#" class="link">seaslog.default_datetime_format</a>
值。 使用函数 <span class="methodname">SeasLog::setDatetimeFormat</span>
将改变本函数的取值。

### 范例

**示例 \#1 <span class="function">SeasLog::getDatetimeFormat</span>
example**

``` php
<?php

var_dump(SeasLog::getDateTimeFormat());
var_dump(SeasLog::setDateTimeFormat('Ymd His'));
var_dump(SeasLog::getDateTimeFormat());

?>
```

以上例程的输出类似于：

    string(11) "Y-m-d H:i:s"
    bool(true)
    string(7) "Ymd His"

### 参见

-   <span class="methodname">SeasLog::setDatetimeFormat</span>

SeasLog::getLastLogger
======================

获得 SeasLog 最近的一次 Logger 名称

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">SeasLog::getLastLogger</span> ( <span
class="methodparam">void</span> )

使用函数 <span class="methodname">SeasLog::getLastLogger</span> 将获取
php.ini(seaslog.ini) 中配置的
<a href="/seaslog/setup.html#" class="link">seaslog.default_logger</a>
值。

### 参数

此函数没有参数。

### 返回值

使用函数 <span class="methodname">SeasLog::setLogger</span> 将改变函数
<span class="methodname">SeasLog::getLastLogger</span> 的取值。

### 范例

**示例 \#1 <span class="function">SeasLog::getLastLogger</span>
example**

``` php
<?php

var_dump(SeasLog::getLastLogger());
SeasLog::setLogger('theNewLogger');
var_dump(SeasLog::getLastLogger());
?>
```

以上例程的输出类似于：

    string(7) "default"
    string(12) "theNewLogger"

### 参见

-   <span class="methodname">SeasLog::setLogger</span>

SeasLog::getRequestID
=====================

获得当前 SeasLog 中用于区分请求的 request\_id

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">SeasLog::getRequestID</span> ( <span
class="methodparam">void</span> )

为了区分一个独立的请求，如果没有调用函数 <span
class="methodname">SeasLog::setRequestId</span> 进行指定，SeasLog
将会在请求初始化时，使用内置函数 \`static char \*get\_uniqid ()\`
生成一个 unique 值。

### 参数

此函数没有参数。

### 返回值

返回一个由内置函数 \`static char \*get\_uniqid ()\` 生成的、
或由用户调用函数 <span class="methodname">SeasLog::setRequestId</span>
指定的字符串。

### 范例

**示例 \#1 <span class="function">SeasLog::getRequestID</span> example**

``` php
<?php

var_dump(SeasLog::getRequestID());
var_dump(SeasLog::setRequestID('reqeust_id_test_'.time()))
var_dump(SeasLog::getRequestID());

?>
```

以上例程的输出类似于：

    string(13) "5b3f21a209519"
    bool(true)
    string(26) "reqeust_id_test_1530864034"

### 参见

-   <span class="methodname">SeasLog::setRequestID</span>
-   在 Seaslog 默认变量表中的 \`%Q\`
    <a href="/seaslog/setup.html#Seaslog%20内置变量表" class="link">/seaslog/setup.html#Seaslog 内置变量表</a>

SeasLog::getRequestVariable
===========================

Get SeasLog request variable

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::getRequestVariable</span> ( <span
class="methodparam"><span class="type">int</span> `$key`</span> )

Get SeasLog request variable.

### 参数

`key`  
Constant int.

-   <a href="/seaslog/constants.html#" class="link">SEASLOG_REQUEST_VARIABLE_DOMAIN_PORT</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_REQUEST_VARIABLE_REQUEST_URI</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_REQUEST_VARIABLE_REQUEST_METHOD</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_REQUEST_VARIABLE_CLIENT_IP</a>

### 返回值

Return request variable value on set success.

### 范例

**示例 \#1 <span class="methodname">SeasLog::getRequestVariable</span>
example**

``` php
<?php

$sDomainPort = 'domain:port';
$sRequestUri = 'uri';
$sRequestMethod = 'method';
$sClientIp = 'client_ip';

$iErrorKey = 1000;

$oSeasLog = new SeasLog();

var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_DOMAIN_PORT, $sDomainPort));
var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_URI, $sRequestUri));
var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_METHOD, $sRequestMethod));
var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_CLIENT_IP, $sClientIp));

var_dump($oSeasLog->setRequestVariable($iErrorKey,NULL));

var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_DOMAIN_PORT) == $sDomainPort);
var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_URI) == $sRequestUri);
var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_METHOD) == $sRequestMethod);
var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_CLIENT_IP) == $sClientIp);

var_dump($oSeasLog->getRequestVariable($iErrorKey));

?>
```

以上例程的输出类似于：


    bool(true)
    bool(true)
    bool(true)
    bool(true)
    bool(false)
    bool(true)
    bool(true)
    bool(true)
    bool(true)
    bool(false)

### 参见

-   <span class="methodname">SeasLog::setRequestVariable</span>

SeasLog::info
=============

Record info log information

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::info</span> ( <span
class="methodparam"><span class="type">string</span> `$message`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">string</span> `$logger`</span> \]\] )

记录 info 日志

> **Note**:
>
> "INFO" - 重要事件、强调应用程序的运行过程。

### 参数

`message`  
The log message.

`content`  
"消息"包含占位符，实现用 content 数组中的值替换这些占位符。 例如'消息'是
\`log info from {NAME}\`, '内容'是 \`array('NAME' =\> neeke)\`，
日志信息是 \`log info from neeke\`

`logger`  
当函数调用 SeasLog::setLogger() 时，就像临时 logger
一样，在第三个参数中使用这个"logger"。 如果 \`logger\` 为NULL 或
""，那么 SeasLog 将使用由 <span
class="methodname">SeasLog::setLogger</span>设置的最新日志记录程序。

### 返回值

记录日志信息成功返回 TRUE，失败返回 FALSE。

### 范例

**示例 \#1 <span class="function">SeasLog::info</span> example**

``` php
<?php

var_dump(SeasLog::info('log message'));

//with content
var_dump(SeasLog::info('log message from {NAME}',array('NAME' => 'neeke')));

//with tmp logger
var_dump(SeasLog::info('log message from {NAME}',array('NAME' => 'neeke'),'tmp_logger'));

var_dump(SeasLog::getBuffer());

?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    bool(true)
    array(2) {
      ["/var/log/www/default/20180707.log"]=>
      array(2) {
        [0]=>
        string(81) "2018-07-07 11:45:49 | INFO | 73263 | 5b40376d1067c | 1530935149.68 | log message
    "
        [1]=>
        string(92) "2018-07-07 11:45:49 | INFO | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
      ["/var/log/www/tmp_logger/20180707.log"]=>
      array(1) {
        [0]=>
        string(92) "2018-07-07 11:45:49 | INFO | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
    }

### 参见

-   <a href="/seaslog/setup.html#Seaslog%20内置变量表" class="link">seaslog.default_template</a>
-   <span class="methodname">SeasLog::debug</span>
-   <span class="methodname">SeasLog::notice</span>
-   <span class="methodname">SeasLog::warning</span>
-   <span class="methodname">SeasLog::error</span>
-   <span class="methodname">SeasLog::critical</span>
-   <span class="methodname">SeasLog::alert</span>
-   <span class="methodname">SeasLog::emergency</span>
-   <span class="methodname">SeasLog::log</span>

SeasLog::log
============

公共的日志记录函数

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::log</span> ( <span class="methodparam"><span
class="type">string</span> `$level`</span> \[, <span
class="methodparam"><span class="type">string</span> `$message`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">string</span> `$logger`</span> \]\]\] )

公共的日志记录函数。可用于调用者扩展日志模板或级别。

### 参数

`level`  
可以使用以下预设级别：

-   <a href="/seaslog/constants.html#" class="link">SEASLOG_DEBUG</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_INFO</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_NOTICE</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_WARNING</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_ERROR</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_CRITICAL</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_ALERT</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_EMERGENCY</a>

或者你可以自助创建新的级别。

`message`  
日志消息

`content`  
"消息"包含占位符，实现用 content 数组中的值替换这些占位符。 例如'消息'是
\`log info from {NAME}\`, '内容'是 \`array('NAME' =\> neeke)\`，
日志信息是 \`log info from neeke\`

`logger`  
当函数调用 SeasLog::setLogger() 时，就像临时 logger
一样，在第三个参数中使用这个"logger"。 如果 \`logger\` 为 NULL 或
""，那么 SeasLog 将使用由 <span
class="methodname">SeasLog::setLogger</span>设置的最新 Logger。

### 返回值

记录日志信息成功返回 TRUE，失败返回 FALSE。

### 范例

**示例 \#1 <span class="function">SeasLog::log</span> example**

``` php
<?php

var_dump(SeasLog::log(SEASLOG_INFO,'info log'));
var_dump(SeasLog::getBuffer());

//create a new level self-help.
var_dump(SeasLog::log('MySelfLevel','info log'));
var_dump(SeasLog::getBuffer());

//with `content`
var_dump(SeasLog::log('MySelfLevel','info log {NAME}',array('NAME' => 'neeke')));
var_dump(SeasLog::getBuffer());

//with `logger`
var_dump(SeasLog::log('MySelfLevel','info log {NAME}',array('NAME' => 'neeke'),'tmp_logger'));
var_dump(SeasLog::getBuffer());


?>
```

以上例程的输出类似于：

    bool(true)
    array(1) {
      ["/var/log/www/default/20180707.log"]=>
      array(1) {
        [0]=>
        string(79) "2018-07-07 11:12:37 | INFO | 72427 | 5b402fa56a2ea | 1530933157.436 | info log
    "
      }
    }

    bool(true)
    array(1) {
      ["/var/log/www/default/20180707.log"]=>
      array(1) {
        [0]=>
        string(86) "2018-07-07 11:13:59 | MySelfLevel | 72470 | 5b402ff781c5e | 1530933239.532 | info log
    "
      }
    }

    bool(true)
    array(1) {
      ["/var/log/www/tmp_logger/20180707.log"]=>
      array(1) {
        [0]=>
        string(92) "2018-07-07 11:28:12 | MySelfLevel | 72833 | 5b40334ce6a2f | 1530934092.946 | info log neeke
    "
      }
    }

    bool(true)
    array(1) {
      ["/var/log/www/default/20180707.log"]=>
      array(1) {
        [0]=>
        string(86) "2018-07-07 11:20:12 | INFO | 72616 | 5b40316c3641e | 1530933612.222 | info log neeke
    "
      }
    }

### 参见

-   <a href="/seaslog/setup.html#Seaslog%20内置变量表" class="link">seaslog.default_template</a>
-   <span class="methodname">SeasLog::debug</span>
-   <span class="methodname">SeasLog::info</span>
-   <span class="methodname">SeasLog::notice</span>
-   <span class="methodname">SeasLog::warning</span>
-   <span class="methodname">SeasLog::error</span>
-   <span class="methodname">SeasLog::critical</span>
-   <span class="methodname">SeasLog::alert</span>
-   <span class="methodname">SeasLog::emergency</span>

SeasLog::notice
===============

记录 notice 日志

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::notice</span> ( <span
class="methodparam"><span class="type">string</span> `$message`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">string</span> `$logger`</span> \]\] )

记录 notice 日志。

> **Note**:
>
> "NOTICE" - 一般重要性事件、执行过程中较 INFO 级别更为重要的信息。

### 参数

`message`  
日志的消息

`content`  
"消息"包含占位符，实现用 content 数组中的值替换这些占位符。 例如'消息'是
\`log info from {NAME}\`, '内容'是 \`array('NAME' =\> neeke)\`，
日志信息是 \`log info from neeke\`

`logger`  
当函数调用 SeasLog::setLogger() 时，就像临时 logger
一样，在第三个参数中使用这个"logger"。 如果 \`logger\` 为 NULL 或
""，那么 SeasLog 将使用由 <span
class="methodname">SeasLog::setLogger</span>设置的最新 Logger。

### 返回值

记录日志信息成功返回 TRUE，失败返回 FALSE。

### 范例

**示例 \#1 <span class="function">SeasLog::notice</span> example**

``` php
<?php

var_dump(SeasLog::notice('log message'));

//with content
var_dump(SeasLog::notice('log message from {NAME}',array('NAME' => 'neeke')));

//with tmp logger
var_dump(SeasLog::notice('log message from {NAME}',array('NAME' => 'neeke'),'tmp_logger'));

var_dump(SeasLog::getBuffer());

?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    bool(true)
    array(2) {
      ["/var/log/www/default/20180707.log"]=>
      array(2) {
        [0]=>
        string(81) "2018-07-07 11:45:49 | NOTICE | 73263 | 5b40376d1067c | 1530935149.68 | log message
    "
        [1]=>
        string(92) "2018-07-07 11:45:49 | NOTICE | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
      ["/var/log/www/tmp_logger/20180707.log"]=>
      array(1) {
        [0]=>
        string(92) "2018-07-07 11:45:49 | NOTICE | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
    }

### 参见

-   <a href="/seaslog/setup.html#Seaslog%20内置变量表" class="link">seaslog.default_template</a>
-   <span class="methodname">SeasLog::debug</span>
-   <span class="methodname">SeasLog::info</span>
-   <span class="methodname">SeasLog::warning</span>
-   <span class="methodname">SeasLog::error</span>
-   <span class="methodname">SeasLog::critical</span>
-   <span class="methodname">SeasLog::alert</span>
-   <span class="methodname">SeasLog::emergency</span>
-   <span class="methodname">SeasLog::log</span>

SeasLog::setBasePath
====================

设置 SeasLog 根目录

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::setBasePath</span> ( <span
class="methodparam"><span class="type">string</span> `$base_path`</span>
)

设置 SeasLog 根目录。

### 参数

`base_path`  
String.

### 返回值

设置根目录成功返回 TRUE，失败返回 FALSE。

### 范例

**示例 \#1 <span class="methodname">SeasLog::setBasePath</span>
example**

``` php
<?php

/* ... */

?>
```

以上例程的输出类似于：

    ...

SeasLog::setDatetimeFormat
==========================

设置 SeasLog 日期格式

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::setDatetimeFormat</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> )

设置 SeasLog 日期格式。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`format`  
字符串。比如 \`Y-m-d H:i:s\` 或者 \`Ymd His\`。查看函数 <span
class="function">date</span> 的第一个参数 \`format\`。

### 返回值

Return TRUE on setted datetime format success, FALSE on failure.

### 范例

**示例 \#1 <span class="function">SeasLog::setDatetimeFormat</span>
example**

``` php
<?php

var_dump(SeasLog::setDateTimeFormat('Ymd His'));

?>
```

以上例程的输出类似于：

    bool(true)

### 参见

-   <span class="methodname">SeasLog::getDateTimeFormat</span>

SeasLog::setLogger
==================

设置 SeasLog 的 Logger 名

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::setLogger</span> ( <span
class="methodparam"><span class="type">string</span> `$logger`</span> )

使用函数 <span class="methodname">SeasLog::setLogger</span> 将改变函数
<span class="methodname">SeasLog::getLastLogger</span> 的取值。
这意味着，SeasLog 将会把日志信息记录在该 Logger 下。

### 参数

`logger`  
Logger name.

### 返回值

设置 Logger 成功（在存储介质为文件时将创建目录或文件）返回
TRUE，失败返回 FALSE。

### 范例

**示例 \#1 <span class="function">SeasLog::setLogger</span> example**

``` php
<?php

var_dump(SeasLog::setLogger('testModule/testLogger'));

?>
```

以上例程的输出类似于：

    bool(true)

### 参见

-   <span class="methodname">SeasLog::getLastLogger</span>

SeasLog::setRequestID
=====================

设置可以由 SeasLog 用于区分请求的 request\_id

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::setRequestID</span> ( <span
class="methodparam"><span class="type">string</span>
`$request_id`</span> )

为了区分一个独立的请求，如果没有调用函数 <span
class="methodname">SeasLog::setRequestId</span> 进行指定，SeasLog
将会在请求初始化时，使用内置函数 \`static char \*get\_uniqid ()\`
生成一个 unique 值。

### 参数

`request_id`  
String.

### 返回值

设置 request\_id 成功返回 TRUE，失败返回 FALSE。

### 范例

**示例 \#1 <span class="function">SeasLog::setRequestID</span> example**

``` php
<?php

var_dump(SeasLog::setRequestID(time() . rand()));

?>
```

以上例程的输出类似于：

    bool(true)

### 参见

-   <span class="methodname">SeasLog::getRequestID</span>

SeasLog::setRequestVariable
===========================

Manually set SeasLog request variable

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::setRequestVariable</span> ( <span
class="methodparam"><span class="type">int</span> `$key`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

Manually set SeasLog request variable.

### 参数

`key`  
Constant int.

-   <a href="/seaslog/constants.html#" class="link">SEASLOG_REQUEST_VARIABLE_DOMAIN_PORT</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_REQUEST_VARIABLE_REQUEST_URI</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_REQUEST_VARIABLE_REQUEST_METHOD</a>
-   <a href="/seaslog/constants.html#" class="link">SEASLOG_REQUEST_VARIABLE_CLIENT_IP</a>

`value`  
The request variable value.

### 返回值

Return TRUE on set success, FALSE on failure.

### 范例

**示例 \#1 <span class="methodname">SeasLog::setRequestVariable</span>
example**

``` php
<?php

$sDomainPort = 'domain:port';
$sRequestUri = 'uri';
$sRequestMethod = 'method';
$sClientIp = 'client_ip';

$iErrorKey = 1000;

$oSeasLog = new SeasLog();

var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_DOMAIN_PORT, $sDomainPort));
var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_URI, $sRequestUri));
var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_METHOD, $sRequestMethod));
var_dump($oSeasLog->setRequestVariable(SEASLOG_REQUEST_VARIABLE_CLIENT_IP, $sClientIp));

var_dump($oSeasLog->setRequestVariable($iErrorKey,NULL));

var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_DOMAIN_PORT) == $sDomainPort);
var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_URI) == $sRequestUri);
var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_REQUEST_METHOD) == $sRequestMethod);
var_dump($oSeasLog->getRequestVariable(SEASLOG_REQUEST_VARIABLE_CLIENT_IP) == $sClientIp);

var_dump($oSeasLog->getRequestVariable($iErrorKey));

?>
```

以上例程的输出类似于：


    bool(true)
    bool(true)
    bool(true)
    bool(true)
    bool(false)
    bool(true)
    bool(true)
    bool(true)
    bool(true)
    bool(false)

### 参见

-   <span class="methodname">SeasLog::getRequestVariable</span>

SeasLog::warning
================

Record warning log information

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">SeasLog::warning</span> ( <span
class="methodparam"><span class="type">string</span> `$message`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">string</span> `$logger`</span> \]\] )

Record warning log information.

> **Note**:
>
> "WARNING" -
> 出现了非错误性的异常信息、潜在异常信息、需要关注并且需要修复。

### 参数

`message`  
The log message.

`content`  
"消息"包含占位符，实现用 content 数组中的值替换这些占位符。 例如'消息'是
\`log info from {NAME}\`, '内容'是 \`array('NAME' =\> neeke)\`，
日志信息是 \`log info from neeke\`

`logger`  
当函数调用 SeasLog::setLogger() 时，就像临时 logger
一样，在第三个参数中使用这个"logger"。 如果 \`logger\` 为 NULL 或
""，那么 SeasLog 将使用由 <span
class="methodname">SeasLog::setLogger</span>设置的最新 Logger。

### 返回值

记录日志信息成功返回 TRUE，失败返回 FALSE。

### 范例

**示例 \#1 <span class="function">SeasLog::warning</span> example**

``` php
<?php

var_dump(SeasLog::warning('log message'));

//with content
var_dump(SeasLog::warning('log message from {NAME}',array('NAME' => 'neeke')));

//with tmp logger
var_dump(SeasLog::warning('log message from {NAME}',array('NAME' => 'neeke'),'tmp_logger'));

var_dump(SeasLog::getBuffer());

?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    bool(true)
    array(2) {
      ["/var/log/www/default/20180707.log"]=>
      array(2) {
        [0]=>
        string(81) "2018-07-07 11:45:49 | WARNING | 73263 | 5b40376d1067c | 1530935149.68 | log message
    "
        [1]=>
        string(92) "2018-07-07 11:45:49 | WARNING | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
      ["/var/log/www/tmp_logger/20180707.log"]=>
      array(1) {
        [0]=>
        string(92) "2018-07-07 11:45:49 | WARNING | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
    "
      }
    }

### 参见

-   <a href="/seaslog/setup.html#Seaslog%20内置变量表" class="link">seaslog.default_template</a>
-   <span class="methodname">SeasLog::debug</span>
-   <span class="methodname">SeasLog::info</span>
-   <span class="methodname">SeasLog::notice</span>
-   <span class="methodname">SeasLog::error</span>
-   <span class="methodname">SeasLog::critical</span>
-   <span class="methodname">SeasLog::alert</span>
-   <span class="methodname">SeasLog::emergency</span>
-   <span class="methodname">SeasLog::log</span>
