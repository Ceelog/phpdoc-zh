checkdate
=========

验证一个格里高里日期

### 说明

<span class="type">bool</span> <span class="methodname">checkdate</span>
( <span class="methodparam"><span class="type">int</span>
`$month`</span> , <span class="methodparam"><span
class="type">int</span> `$day`</span> , <span class="methodparam"><span
class="type">int</span> `$year`</span> )

检查由参数构成的日期的合法性。如果每个参数都正确定义了则会被认为是有效的。

### 参数

`month`  
month 的值是从 1 到 12。

`day`  
`Day` 的值在给定的 `month`
所应该具有的天数范围之内，闰年已经考虑进去了。

`year`  
year 的值是从 1 到 32767。

### 返回值

如果给出的日期有效则返回 **`TRUE`**，否则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">checkdate</span> 例子**

``` php
<?php
var_dump(checkdate(12, 31, 2000));
var_dump(checkdate(2, 29, 2001));
?>
```

以上例程会输出：

    bool(true)
    bool(false)

### 参见

-   <span class="function">mktime</span>
-   <span class="function">strtotime</span>

date\_add
=========

别名 <span class="methodname">DateTime::add</span>

### 说明

此函数是该函数的别名： <span class="methodname">DateTime::add</span>

date\_create\_from\_format
==========================

别名 <span class="methodname">DateTime::createFromFormat</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTime::createFromFormat</span>

date\_create\_immutable\_from\_format
=====================================

别名 <span class="methodname">DateTimeImmutable::createFromFormat</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTimeImmutable::createFromFormat</span>

date\_create\_immutable
=======================

别名 <span class="methodname">DateTimeImmutable::\_\_construct</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTimeImmutable::\_\_construct</span>

date\_create
============

别名 <span class="methodname">DateTime::\_\_construct</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTime::\_\_construct</span>

date\_date\_set
===============

别名 <span class="methodname">DateTime::setDate</span>

### 说明

此函数是该函数的别名： <span class="methodname">DateTime::setDate</span>

date\_default\_timezone\_get
============================

取得一个脚本中所有日期时间函数所使用的默认时区

### 说明

<span class="type">string</span> <span
class="methodname">date\_default\_timezone\_get</span> ( <span
class="methodparam">void</span> )

本函数返回默认时区，使用如下“假定”的顺序：

-   用 <span class="function">date\_default\_timezone\_set</span>
    函数设定的时区（如果设定了的话）

-   *仅仅*在 PHP 5.4.0 之前： `TZ` 环境变量（如果非空）

-   <a href="/datetime/setup.html#" class="link">date.timezone</a>
    配置选项（如果设定了的话）

-   *仅仅*在 PHP 5.4.0 之前： 查询操作系统主机
    (如果操作系统支持并允许)。 This uses an algorithm that has to
    *guess* the timezone. This is by no means going to work correctly
    for every situation. A warning is shown when this stage is reached.
    Do not rely on it to be guessed correctly, and set
    <a href="/datetime/setup.html#" class="link">date.timezone</a> to
    the correct timezone instead.

-   如果以上选择都不成功， <span
    class="methodname">date\_default\_timezone\_get</span> 会则返回
    *UTC* 的默认时区。

### 返回值

返回一个 <span class="type">string</span>。

### 更新日志

| 版本  | 说明                                                 |
|-------|------------------------------------------------------|
| 5.4.0 | 不再使用 *TZ* 来推测时区。                           |
| 5.4.0 | 不再根据操作系统的信息来推测时区，因为这是不可靠的。 |

### 范例

**示例 \#1 获取默认时区**

``` php
<?php
date_default_timezone_set('Europe/London');

if (date_default_timezone_get()) {
    echo 'date_default_timezone_set: ' . date_default_timezone_get() . '<br />';
}

if (ini_get('date.timezone')) {
    echo 'date.timezone: ' . ini_get('date.timezone');
}

?>
```

以上例程的输出类似于：

    date_default_timezone_set: Europe/London
    date.timezone: Europe/London

**示例 \#2 获取一个时区的简写**

``` php
<?php
date_default_timezone_set('America/Los_Angeles');
echo date_default_timezone_get() . ' => ' . date('e') . ' => ' . date('T');
?>
```

以上例程会输出：

    America/Los_Angeles => America/Los_Angeles => PST

### 参见

-   <span class="function">date\_default\_timezone\_set</span>
-   <a href="/timezones.html" class="xref">所支持的时区列表</a>

date\_default\_timezone\_set
============================

设定用于一个脚本中所有日期时间函数的默认时区

### 说明

<span class="type">bool</span> <span
class="methodname">date\_default\_timezone\_set</span> ( <span
class="methodparam"><span class="type">string</span>
`$timezone_identifier`</span> )

<span class="function">date\_default\_timezone\_set</span>
设定用于所有日期时间函数的默认时区。

> **Note**:
>
> 自 PHP 5.1.0
> 起（此版本日期时间函数被重写了），如果时区不合法则每个对日期时间函数的调用都会产生一条
> **`E_NOTICE`** 级别的错误信息，如果使用系统设定或 `TZ`
> 环境变量则还会产生 **`E_STRICT`** 级别的信息。

除了用此函数，你还可以通过 INI 设置
<a href="/datetime/setup.html#" class="link">date.timezone</a>
来设置默认时区。

### 参数

`timezone_identifier`  
时区标识符，例如 *UTC* 或
*Europe/Lisbon*。合法标识符列表见<a href="/timezones.html" class="xref">所支持的时区列表</a>。

### 返回值

如果 `timezone_identifier` 参数无效则返回 **`FALSE`**，否则返回
**`TRUE`**。

### 范例

**示例 \#1 获取默认时区**

``` php
<?php
date_default_timezone_set('America/Los_Angeles');

$script_tz = date_default_timezone_get();

if (strcmp($script_tz, ini_get('date.timezone'))){
    echo 'Script timezone differs from ini-set timezone.';
} else {
    echo 'Script timezone and ini-set timezone match.';
}
?>
```

### 更新日志

| 版本  | 说明                                               |
|-------|----------------------------------------------------|
| 5.3.0 | 现在会抛出 **`E_WARNING`** 而不是 **`E_STRICT`**。 |
| 5.1.2 | 本版本开始验证 `timezone_identifier` 参数。        |

### 参见

-   <span class="function">date\_default\_timezone\_get</span>
-   <a href="/timezones.html" class="xref">所支持的时区列表</a>

date\_diff
==========

别名 <span class="methodname">DateTime::diff</span>

### 说明

此函数是该函数的别名： <span class="methodname">DateTime::diff</span>

date\_format
============

别名 <span class="methodname">DateTime::format</span>

### 说明

此函数是该函数的别名： <span class="methodname">DateTime::format</span>

date\_get\_last\_errors
=======================

别名 <span class="methodname">DateTime::getLastErrors</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTime::getLastErrors</span>

date\_interval\_create\_from\_date\_string
==========================================

别名 <span class="methodname">DateInterval::createFromDateString</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateInterval::createFromDateString</span>

date\_interval\_format
======================

别名 <span class="methodname">DateInterval::format</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateInterval::format</span>

date\_isodate\_set
==================

别名 <span class="methodname">DateTime::setISODate</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTime::setISODate</span>

date\_modify
============

别名 <span class="methodname">DateTime::modify</span>

### 说明

此函数是该函数的别名： <span class="methodname">DateTime::modify</span>

date\_offset\_get
=================

别名 <span class="methodname">DateTime::getOffset</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTime::getOffset</span>

date\_parse\_from\_format
=========================

Get info about given date formatted according to the specified format

### 说明

<span class="type">array</span> <span
class="methodname">date\_parse\_from\_format</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> ,
<span class="methodparam"><span class="type">string</span>
`$date`</span> )

Returns associative array with detailed info about given date.

### 参数

`format`  
Format accepted by <span
class="function">DateTime::createFromFormat</span>.

`date`  
String representing the date.

### 返回值

Returns associative array with detailed info about given date.

### 更新日志

| 版本  | 说明                                                                                                                                             |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.2.0 | The *zone* element of the returned array represents seconds instead of minutes now, and its sign is inverted. For instance *-120* is now *7200*. |

### 范例

**示例 \#1 <span class="function">date\_parse\_from\_format</span>
example**

``` php
<?php
$date = "6.1.2009 13:00+01:00";
print_r(date_parse_from_format("j.n.Y H:iP", $date));
?>
```

以上例程会输出：

    Array
    (
        [year] => 2009
        [month] => 1
        [day] => 6
        [hour] => 13
        [minute] => 0
        [second] => 0
        [fraction] => 
        [warning_count] => 0
        [warnings] => Array
            (
            )

        [error_count] => 0
        [errors] => Array
            (
            )

        [is_localtime] => 1
        [zone_type] => 1
        [zone] => 3600
        [is_dst] => 
    )

### 参见

-   <span class="function">DateTime::createFromFormat</span>
-   <span class="function">checkdate</span>

date\_parse
===========

Returns associative array with detailed info about given date

### 说明

<span class="type">array</span> <span
class="methodname">date\_parse</span> ( <span class="methodparam"><span
class="type">string</span> `$date`</span> )

### 参数

`date`  
Date in format accepted by <span class="function">strtotime</span>.

### 返回值

Returns <span class="type">array</span> with information about the
parsed date on success 或者在失败时返回 **`FALSE`**.

### 错误／异常

In case the date format has an error, the element 'errors' will contains
the error messages.

### 更新日志

| 版本  | 说明                                                                                                                                             |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.2.0 | The *zone* element of the returned array represents seconds instead of minutes now, and its sign is inverted. For instance *-120* is now *7200*. |

### 范例

**示例 \#1 A <span class="function">date\_parse</span> example**

``` php
<?php
print_r(date_parse("2006-12-12 10:00:00.5"));
?>
```

以上例程会输出：

    Array
    (
        [year] => 2006
        [month] => 12
        [day] => 12
        [hour] => 10
        [minute] => 0
        [second] => 0
        [fraction] => 0.5
        [warning_count] => 0
        [warnings] => Array()
        [error_count] => 0
        [errors] => Array()
        [is_localtime] => 
    )

<a href="/datetime/formats.html#Relative%20Formats" class="link">Relative formats</a>
do not influence the values parsed from absolute formats, but are parsed
into the "relative" element.

**示例 \#2 <span class="function">date\_parse</span> with relative
formats**

``` php
<?php
print_r(date_parse("2006-12-12 10:00:00.5 +1 week +1 hour"));
?>
```

以上例程会输出：

    Array
    (
        [year] => 2006
        [month] => 12
        [day] => 12
        [hour] => 10
        [minute] => 0
        [second] => 0
        [fraction] => 0.5
        [warning_count] => 0
        [warnings] => Array
            (
            )

        [error_count] => 0
        [errors] => Array
            (
            )

        [is_localtime] =>
        [relative] => Array
            (
                [year] => 0
                [month] => 0
                [day] => 7
                [hour] => 1
                [minute] => 0
                [second] => 0
            )

    )

### 参见

-   <span class="function">checkdate</span>
-   <span class="function">getdate</span>

date\_sub
=========

别名 <span class="methodname">DateTime::sub</span>

### 说明

此函数是该函数的别名： <span class="methodname">DateTime::sub</span>

date\_sun\_info
===============

Returns an array with information about sunset/sunrise and twilight
begin/end

### 说明

<span class="type">array</span> <span
class="methodname">date\_sun\_info</span> ( <span
class="methodparam"><span class="type">int</span> `$time`</span> , <span
class="methodparam"><span class="type">float</span> `$latitude`</span> ,
<span class="methodparam"><span class="type">float</span>
`$longitude`</span> )

### 参数

`time`  
Timestamp.

`latitude`  
Latitude in degrees.

`longitude`  
Longitude in degrees.

### 返回值

Returns array on success 或者在失败时返回 **`FALSE`**. The structure of
the array is detailed in the following list:

*sunrise*  
<span class="simpara"> The time of the sunrise (zenith angle = 90°35').
</span>

*sunset*  
<span class="simpara"> The time of the sunset (zenith angle = 90°35').
</span>

*transit*  
<span class="simpara"> The time when the sun is at its zenith, i.e. has
reached its topmost point. </span>

*civil\_twilight\_begin*  
<span class="simpara"> The start of the civil dawn (zenith angle = 96°).
It ends at *sunrise*. </span>

*civil\_twilight\_end*  
<span class="simpara"> The end of the civil dusk (zenith angle = 96°).
It starts at *sunset*. </span>

*nautical\_twilight\_begin*  
<span class="simpara"> The start of the nautical dawn (zenith angle =
102°). It ends at *civil\_twilight\_begin*. </span>

*nautical\_twilight\_end*  
<span class="simpara"> The end of the nautical dusk (zenith angle =
102°). It starts at *civil\_twilight\_end*. </span>

*astronomical\_twilight\_begin*  
<span class="simpara"> The start of the astronomical dawn (zenith angle
= 108°). It ends at *nautical\_twilight\_begin*. </span>

*astronomical\_twilight\_end*  
<span class="simpara"> The end of the astronomical dusk (zenith angle =
108°). It starts at *nautical\_twilight\_end*. </span>

The values of the array elements are either UNIX timestamps, **`FALSE`**
if the sun is below the respective zenith for the whole day, or
**`TRUE`** if the sun is above the respective zenith for the whole day.

### 更新日志

| 版本  | 说明                                                      |
|-------|-----------------------------------------------------------|
| 5.2.2 | The order of `latitude` and `longitude` has been swapped. |

### 范例

**示例 \#1 A <span class="function">date\_sun\_info</span> example**

``` php
<?php
$sun_info = date_sun_info(strtotime("2006-12-12"), 31.7667, 35.2333);
foreach ($sun_info as $key => $val) {
    echo "$key: " . date("H:i:s", $val) . "\n";
}
?>
```

以上例程会输出：

    sunrise: 05:52:11
    sunset: 15:41:21
    transit: 10:46:46
    civil_twilight_begin: 05:24:08
    civil_twilight_end: 16:09:24
    nautical_twilight_begin: 04:52:25
    nautical_twilight_end: 16:41:06
    astronomical_twilight_begin: 04:21:32
    astronomical_twilight_end: 17:12:00

**示例 \#2 Polar night**

``` php
<?php
var_dump(date_sun_info(strtotime("2017-12-21"), 90, 0));
?>
```

以上例程会输出：

    array(9) {
      ["sunrise"]=>
      bool(false)
      ["sunset"]=>
      bool(false)
      ["transit"]=>
      int(1513857490)
      ["civil_twilight_begin"]=>
      bool(false)
      ["civil_twilight_end"]=>
      bool(false)
      ["nautical_twilight_begin"]=>
      bool(false)
      ["nautical_twilight_end"]=>
      bool(false)
      ["astronomical_twilight_begin"]=>
      bool(false)
      ["astronomical_twilight_end"]=>
      bool(false)
    }

**示例 \#3 Midnight sun**

``` php
<?php
var_dump(date_sun_info(strtotime("2017-06-21"), 90, 0));
?>
```

以上例程会输出：

    array(9) {
      ["sunrise"]=>
      bool(true)
      ["sunset"]=>
      bool(true)
      ["transit"]=>
      int(1498046510)
      ["civil_twilight_begin"]=>
      bool(true)
      ["civil_twilight_end"]=>
      bool(true)
      ["nautical_twilight_begin"]=>
      bool(true)
      ["nautical_twilight_end"]=>
      bool(true)
      ["astronomical_twilight_begin"]=>
      bool(true)
      ["astronomical_twilight_end"]=>
      bool(true)
    }

### 参见

-   <span class="function">date\_sunrise</span>
-   <span class="function">date\_sunset</span>

date\_sunrise
=============

返回给定的日期与地点的日出时间

### 说明

<span class="type">mixed</span> <span
class="methodname">date\_sunrise</span> ( <span
class="methodparam"><span class="type">int</span> `$timestamp`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$format`<span class="initializer"> =
SUNFUNCS\_RET\_STRING</span></span> \[, <span class="methodparam"><span
class="type">float</span> `$latitude`<span class="initializer"> =
ini\_get("date.default\_latitude")</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$longitude`<span
class="initializer"> = ini\_get("date.default\_longitude")</span></span>
\[, <span class="methodparam"><span class="type">float</span>
`$zenith`<span class="initializer"> =
ini\_get("date.sunrise\_zenith")</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$gmt_offset`<span
class="initializer"> = 0</span></span> \]\]\]\]\] )

<span class="function">date\_sunrise</span> 返回给定的日期（以
`timestamp` 指定）与地点的日出时间。

### 参数

`timestamp`  
取 `timestamp`所在日期的日出时间。

`format`  
| 常量                     | 说明                                                        | 取值举例    |
|--------------------------|-------------------------------------------------------------|-------------|
| SUNFUNCS\_RET\_STRING    | 以 <span class="type">string</span> 格式返回结果            | 16:46       |
| SUNFUNCS\_RET\_DOUBLE    | 以 <span class="type">float</span> 格式返回结果             | 16.78243132 |
| SUNFUNCS\_RET\_TIMESTAMP | 以 <span class="type">integer</span> 格式（时间戳）返回结果 | 1095034606  |

`latitude`  
默认是指北纬。因此如果要指定南纬，必须传递一个负值。 参见
*date.default\_latitude*。

`longitude`  
默认是指东经。因此如果要指定西经，必须传递一个负值。 参见
*date.default\_longitude*。

`zenith`  
默认： *date.sunrise\_zenith*。

`gmtoffset`  
单位是小时。

### 返回值

按指定格式 `format` 返回的日出时间， 或者在失败时返回 **`FALSE`**。

### 错误／异常

在每 次调用日期/时间函数时，如果时区无效则会引发 **`E_NOTICE`**
错误，如果使用系统设定值或 `TZ` 环境变量，则会引发 **`E_STRICT`** 或
**`E_WARNING`** 消息。参见 <span
class="function">date\_default\_timezone\_set</span>。

### 更新日志

| 版本  | 说明                                                 |
|-------|------------------------------------------------------|
| 5.1.0 | 现在发布 **`E_STRICT`** 和 **`E_NOTICE`** 时区错误。 |

### 范例

**示例 \#1 <span class="function">date\_sunrise</span> 例子**

``` php
<?php

/* 计算葡萄牙里斯本的日出时间
Latitude:  北纬 38.4 度
Longitude: 西经 9 度
Zenith ~= 90
offset: +1 GMT
*/

echo date("D M d Y"). ', sunrise time : ' .date_sunrise(time(), SUNFUNCS_RET_STRING, 38.4, -9, 90, 1);

?>
```

以上例程的输出类似于：

    Mon Dec 20 2004, sunrise time : 08:54

### 参见

-   <span class="function">date\_sunset</span>

date\_sunset
============

返回给定的日期与地点的日落时间

### 说明

<span class="type">mixed</span> <span
class="methodname">date\_sunset</span> ( <span class="methodparam"><span
class="type">int</span> `$timestamp`</span> \[, <span
class="methodparam"><span class="type">int</span> `$format`<span
class="initializer"> = SUNFUNCS\_RET\_STRING</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$latitude`<span
class="initializer"> = ini\_get("date.default\_latitude")</span></span>
\[, <span class="methodparam"><span class="type">float</span>
`$longitude`<span class="initializer"> =
ini\_get("date.default\_longitude")</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$zenith`<span
class="initializer"> = ini\_get("date.sunset\_zenith")</span></span> \[,
<span class="methodparam"><span class="type">float</span>
`$gmt_offset`<span class="initializer"> = 0</span></span> \]\]\]\]\] )

<span class="function">date\_sunset</span> 返回给定的日期（以
`timestamp` 指定）与地点的日落时间。

### 参数

`timestamp`  
返回给定的日期（以 `timestamp` 指定）的日落时间。

`format`  
| 常量                     | 说明                                                        | 取值举例    |
|--------------------------|-------------------------------------------------------------|-------------|
| SUNFUNCS\_RET\_STRING    | 以 <span class="type">string</span> 格式返回结果            | 16:46       |
| SUNFUNCS\_RET\_DOUBLE    | 以 <span class="type">float</span> 格式返回结果             | 16.78243132 |
| SUNFUNCS\_RET\_TIMESTAMP | 以 <span class="type">integer</span> 格式（时间戳）返回结果 | 1095034606  |

`latitude`  
默认是指北纬。因此如果要指定南纬，必须传递一个负值。参见：
*date.default\_latitude*。

`longitude`  
默认是指东经。因此如果要指定西经，必须传递一个负值。参见：
*date.default\_longitude*

`zenith`  
默认： *date.sunset\_zenith*。

`gmtoffset`  
单位是小时。

### 错误／异常

在每 次调用日期/时间函数时，如果时区无效则会引发 **`E_NOTICE`**
错误，如果使用系统设定值或 `TZ` 环境变量，则会引发 **`E_STRICT`** 或
**`E_WARNING`** 消息。参见 <span
class="function">date\_default\_timezone\_set</span>。

### 更新日志

| 版本  | 说明                                                 |
|-------|------------------------------------------------------|
| 5.1.0 | 现在发布 **`E_STRICT`** 和 **`E_NOTICE`** 时区错误。 |

### 返回值

用指定的格式 `format` 返回日落时间， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">date\_sunset</span> 例子**

``` php
<?php

/* calculate the sunset time for Lisbon, Portugal
Latitude: 38.4 North
Longitude: 9 West
Zenith ~= 90
offset: +1 GMT
*/

echo date("D M d Y"). ', sunset time : ' .date_sunset(time(), SUNFUNCS_RET_STRING, 38.4, -9, 90, 1);

?>
```

以上例程的输出类似于：

    Mon Dec 20 2004, sunset time : 18:13

### 参见

-   <span class="function">date\_sunrise</span>

date\_time\_set
===============

别名 <span class="methodname">DateTime::setTime</span>

### 说明

此函数是该函数的别名： <span class="methodname">DateTime::setTime</span>

date\_timestamp\_get
====================

别名 <span class="methodname">DateTime::getTimestamp</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTime::getTimestamp</span>

date\_timestamp\_set
====================

别名 <span class="methodname">DateTime::setTimestamp</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTime::setTimestamp</span>

date\_timezone\_get
===================

别名 <span class="methodname">DateTime::getTimezone</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTime::getTimezone</span>

date\_timezone\_set
===================

别名 <span class="methodname">DateTime::setTimezone</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTime::setTimezone</span>

date
====

格式化一个本地时间／日期

### 说明

<span class="type">string</span> <span class="methodname">date</span> (
<span class="methodparam"><span class="type">string</span>
`$format`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timestamp`</span> \] )

返回将整数 `timestamp`
按照给定的格式字串而产生的字符串。如果没有给出时间戳则使用本地当前时间。换句话说，`timestamp`
是可选的，默认值为 <span class="function">time</span>。

**小贴士**

自 PHP 5.1.1
起有几个有用的<a href="/datetime/constants.html" class="link">常量</a>可用作标准的日期／时间格式来指定
`format` 参数。

**小贴士**

自 PHP 5.1 起在 `$_SERVER['REQUEST_TIME']`
中保存了发起该请求时刻的时间戳。

> **Note**:
>
> 有效的时间戳典型范围是格林威治时间 1901 年 12 月 13 日 20:45:54 到
> 2038 年 1 月 19 日 03:14:07。（此范围符合 32
> 位有符号整数的最小值和最大值）。不过在 PHP 5.1
> 之前此范围在某些系统（如 Windows）中限制为从 1970 年 1 月 1 日到 2038
> 年 1 月 19 日。

> **Note**:
>
> 要将字符串表达的时间转换成时间戳，应该使用 <span
> class="function">strtotime</span>。此外一些数据库有一些函数将其时间格式转换成时间戳（例如
> MySQL 的
> <a href="http://dev.mysql.com/doc/mysql/en/date-and-time-functions.html" class="link external">» UNIX_TIMESTAMP</a>
> 函数）。

|     `format` 字符    | 说明                                                                                                                                                                                                                  | 返回值例子                                                                                                             |
|:--------------------:|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
|         *日*         | ---                                                                                                                                                                                                                   | ---                                                                                                                    |
|          *d*         | 月份中的第几天，有前导零的 2 位数字                                                                                                                                                                                   | *01* 到 *31*                                                                                                           |
|          *D*         | 星期中的第几天，文本表示，3 个字母                                                                                                                                                                                    | *Mon* 到 *Sun*                                                                                                         |
|          *j*         | 月份中的第几天，没有前导零                                                                                                                                                                                            | *1* 到 *31*                                                                                                            |
| *l*（“L”的小写字母） | 星期几，完整的文本格式                                                                                                                                                                                                | *Sunday* 到 *Saturday*                                                                                                 |
|          *N*         | ISO-8601 格式数字表示的星期中的第几天（PHP 5.1.0 新加）                                                                                                                                                               | *1*（表示星期一）到 *7*（表示星期天）                                                                                  |
|          *S*         | 每月天数后面的英文后缀，2 个字符                                                                                                                                                                                      | *st*，*nd*，*rd* 或者 *th*。可以和 *j* 一起用                                                                          |
|          *w*         | 星期中的第几天，数字表示                                                                                                                                                                                              | *0*（表示星期天）到 *6*（表示星期六）                                                                                  |
|          *z*         | 年份中的第几天                                                                                                                                                                                                        | *0* 到 *365*                                                                                                           |
|        *星期*        | ---                                                                                                                                                                                                                   | ---                                                                                                                    |
|          *W*         | ISO-8601 格式年份中的第几周，每周从星期一开始（PHP 4.1.0 新加的）                                                                                                                                                     | 例如：*42*（当年的第 42 周）                                                                                           |
|         *月*         | ---                                                                                                                                                                                                                   | ---                                                                                                                    |
|          *F*         | 月份，完整的文本格式，例如 January 或者 March                                                                                                                                                                         | *January* 到 *December*                                                                                                |
|          *m*         | 数字表示的月份，有前导零                                                                                                                                                                                              | *01* 到 *12*                                                                                                           |
|          *M*         | 三个字母缩写表示的月份                                                                                                                                                                                                | *Jan* 到 *Dec*                                                                                                         |
|          *n*         | 数字表示的月份，没有前导零                                                                                                                                                                                            | *1* 到 *12*                                                                                                            |
|          *t*         | 指定的月份有几天                                                                                                                                                                                                      | *28* 到 *31*                                                                                                           |
|         *年*         | ---                                                                                                                                                                                                                   | ---                                                                                                                    |
|          *L*         | 是否为闰年                                                                                                                                                                                                            | 如果是闰年为 *1*，否则为 *0*                                                                                           |
|          *o*         | ISO-8601 格式年份数字。这和 *Y* 的值相同，只除了如果 ISO 的星期数（*W*）属于前一年或下一年，则用那一年。（PHP 5.1.0 新加）                                                                                            | Examples: *1999* or *2003*                                                                                             |
|          *Y*         | 4 位数字完整表示的年份                                                                                                                                                                                                | 例如：*1999* 或 *2003*                                                                                                 |
|          *y*         | 2 位数字表示的年份                                                                                                                                                                                                    | 例如：*99* 或 *03*                                                                                                     |
|        *时间*        | ---                                                                                                                                                                                                                   | ---                                                                                                                    |
|          *a*         | 小写的上午和下午值                                                                                                                                                                                                    | *am* 或 *pm*                                                                                                           |
|          *A*         | 大写的上午和下午值                                                                                                                                                                                                    | *AM* 或 *PM*                                                                                                           |
|          *B*         | Swatch Internet 标准时                                                                                                                                                                                                | *000* 到 *999*                                                                                                         |
|          *g*         | 小时，12 小时格式，没有前导零                                                                                                                                                                                         | *1* 到 *12*                                                                                                            |
|          *G*         | 小时，24 小时格式，没有前导零                                                                                                                                                                                         | *0* 到 *23*                                                                                                            |
|          *h*         | 小时，12 小时格式，有前导零                                                                                                                                                                                           | *01* 到 *12*                                                                                                           |
|          *H*         | 小时，24 小时格式，有前导零                                                                                                                                                                                           | *00* 到 *23*                                                                                                           |
|          *i*         | 有前导零的分钟数                                                                                                                                                                                                      | *00* 到 *59*\>                                                                                                         |
|          *s*         | 秒数，有前导零                                                                                                                                                                                                        | *00* 到 *59*\>                                                                                                         |
|          *u*         | 毫秒 （PHP 5.2.2 新加）。需要注意的是 <span class="function">date</span> 函数总是返回 *000000* 因为它只接受 <span class="type">integer</span> 参数， 而 <span class="methodname">DateTime::format</span> 才支持毫秒。 | 示例: *654321*                                                                                                         |
|        *时区*        | ---                                                                                                                                                                                                                   | ---                                                                                                                    |
|          *e*         | 时区标识（PHP 5.1.0 新加）                                                                                                                                                                                            | 例如：*UTC*，*GMT*，*Atlantic/Azores*                                                                                  |
|          *I*         | 是否为夏令时                                                                                                                                                                                                          | 如果是夏令时为 *1*，否则为 *0*                                                                                         |
|          *O*         | 与格林威治时间相差的小时数                                                                                                                                                                                            | 例如：*+0200*                                                                                                          |
|          *P*         | 与格林威治时间（GMT）的差别，小时和分钟之间有冒号分隔（PHP 5.1.3 新加）                                                                                                                                               | 例如：*+02:00*                                                                                                         |
|          *T*         | 本机所在的时区                                                                                                                                                                                                        | 例如：*EST*，*MDT*（【译者注】在 Windows 下为完整文本格式，例如“Eastern Standard Time”，中文版会显示“中国标准时间”）。 |
|          *Z*         | 时差偏移量的秒数。UTC 西边的时区偏移量总是负的，UTC 东边的时区偏移量总是正的。                                                                                                                                        | *-43200* 到 *43200*                                                                                                    |
|  *完整的日期／时间*  | ---                                                                                                                                                                                                                   | ---                                                                                                                    |
|          *c*         | ISO 8601 格式的日期（PHP 5 新加）                                                                                                                                                                                     | 2004-02-12T15:19:21+00:00                                                                                              |
|          *r*         | RFC 822 格式的日期                                                                                                                                                                                                    | 例如：*Thu, 21 Dec 2000 16:01:07 +0200*                                                                                |
|          *U*         | 从 Unix 纪元（January 1 1970 00:00:00 GMT）开始至今的秒数                                                                                                                                                             | 参见 <span class="function">time</span>                                                                                |

格式字串中不能被识别的字符将原样显示。*Z* 格式在使用 <span
class="function">gmdate</span> 时总是返回 *0*。

**示例 \#1 <span class="function">date</span> 例子**

``` php
<?php
// 设定要用的默认时区。自 PHP 5.1 可用
date_default_timezone_set('UTC');


// 输出类似：Monday
echo date("l");

// 输出类似：Monday 15th of August 2005 03:12:46 PM
echo date('l dS \of F Y h:i:s A');

// 输出：July 1, 2000 is on a Saturday
echo "July 1, 2000 is on a " . date("l", mktime(0, 0, 0, 7, 1, 2000));

/* 在格式参数中使用常量 */
// 输出类似：Wed, 25 Sep 2013 15:28:57 -0700
echo date(DATE_RFC2822);

// 输出类似：2000-07-01T00:00:00+00:00
echo date(DATE_ATOM, mktime(0, 0, 0, 7, 1, 2000));
?>
```

在格式字串中的字符前加上反斜线来转义可以避免它被按照上表解释。如果加上反斜线后的字符本身就是一个特殊序列，那还要转义反斜线。

**示例 \#2 在 <span class="function">date</span> 中转义字符**

``` php
<?php
// prints something like: Wednesday the 15th
echo date("l \\t\h\e jS");
?>
```

可以把 <span class="function">date</span> 和 <span
class="function">mktime</span> 函数结合使用来得到未来或过去的日期。

**示例 \#3 <span class="function">date</span> 和 <span
class="function">mktime</span> 例子**

``` php
<?php
$tomorrow  = mktime(0, 0, 0, date("m")  , date("d")+1, date("Y"));
$lastmonth = mktime(0, 0, 0, date("m")-1, date("d"),   date("Y"));
$nextyear  = mktime(0, 0, 0, date("m"),   date("d"),   date("Y")+1);
?>
```

> **Note**:
>
> 由于夏令时的缘故，这种方法比简单地在时间戳上加减一天或者一个月的秒数更可靠。

一些使用 <span class="function">date</span>
格式化日期的例子。注意要转义所有其它的字符，因为目前有特殊含义的字符会产生不需要的结果，而其余字符在
PHP 将来的版本中可能会被用上。当转义时，注意用单引号以避免类似 \\n
的字符变成了换行符。

**示例 \#4 <span class="function">date</span> 格式举例**

``` php
<?php
// 假定今天是：March 10th, 2001, 5:16:18 pm
$today = date("F j, Y, g:i a");                 // March 10, 2001, 5:16 pm
$today = date("m.d.y");                         // 03.10.01
$today = date("j, n, Y");                       // 10, 3, 2001
$today = date("Ymd");                           // 20010310
$today = date('h-i-s, j-m-y, it is w Day z ');  // 05-16-17, 10-03-01, 1631 1618 6 Fripm01
$today = date('\i\t \i\s \t\h\e jS \d\a\y.');   // It is the 10th day.
$today = date("D M j G:i:s T Y");               // Sat Mar 10 15:16:08 MST 2001
$today = date('H:m:s \m \i\s\ \m\o\n\t\h');     // 17:03:17 m is month
$today = date("H:i:s");                         // 17:16:17
$today = date("Y-m-d H:i:s");                   // 2001-03-10 17:16:18 （MySQL DATETIME 格式）
?>
```

要格式化其它语种的日期，应该用 <span class="function">setlocale</span>
和 <span class="function">strftime</span> 函数来代替 <span
class="function">date</span>。

参见 <span class="function">getlastmod</span>，<span
class="function">gmdate</span>，<span
class="function">mktime</span>，<span class="function">strftime</span>
和 <span class="function">time</span>。

### 参数

`format`  
输出的日期 <span class="type">string</span> 格式。 参见下文中的
格式化选项。 同时，还可以使用
<a href="/class/datetimeinterface.html#预定义常量" class="link">预定义日期常量</a>
，例如：常量 **`DATE_RSS`** 表示格式化字符串 *'D, d M Y H:i:s'*。

|    `format` 字符    | 描述                                                                                                                                                                                                                   | 返回值示例                                           |
|:-------------------:|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
|         *天*        | ---                                                                                                                                                                                                                    | ---                                                  |
|         *d*         | 一个月中的第几天，有前导 0 的 2 位数字                                                                                                                                                                                 | 从 *01* 到 *31*                                      |
|         *D*         | 3 个字符表示的星期几                                                                                                                                                                                                   | 从 *Mon* 到 *Sun*                                    |
|         *j*         | 一个月中的第几天，无前导 0                                                                                                                                                                                             | 从 *1* 到 *31*                                       |
| *l* (lowercase 'L') | 星期几，英文全称                                                                                                                                                                                                       | 从 *Sunday* 到 *Saturday*                            |
|         *N*         | ISO-8601 规定的数字表示的星期几（PHP 5.1.0 新加 ）                                                                                                                                                                     | 从 *1* （表示星期一）到 *7* （表示星期日）           |
|         *S*         | 一个月中的第几天，带有 2 个字符表示的英语序数词。                                                                                                                                                                      | *st*， *nd*， *rd* 或者 *th*。 可以和 *j* 联合使用。 |
|         *w*         | 数字表示的星期几                                                                                                                                                                                                       | 从 *0* （星期日） 到 *6* （星期六）                  |
|         *z*         | 一年中的第几天，从 0 开始计数                                                                                                                                                                                          | 从 *0* 到 *365*                                      |
|         *周*        | ---                                                                                                                                                                                                                    | ---                                                  |
|         *W*         | ISO-8601 规范的一年中的第几周，周一视为一周开始。（PHP 4.1.0 新加）                                                                                                                                                    | 示例： *42* （本年第42周）                           |
|         *月*        | ---                                                                                                                                                                                                                    | ---                                                  |
|         *F*         | 月份英文全拼，例如：January 或 March                                                                                                                                                                                   | 从 *January* 到 *December*                           |
|         *m*         | 带有 0 前导的数字表示的月份                                                                                                                                                                                            | 从 *01* 到 *12*                                      |
|         *M*         | 3 个字符表示的月份的英文简拼                                                                                                                                                                                           | 从 *Jan* 到 *Dec*                                    |
|         *n*         | 月份的数字表示，无前导 0                                                                                                                                                                                               | *1* through *12*                                     |
|         *t*         | 给定月份中包含多少天                                                                                                                                                                                                   | 从 *28* 到 *31*                                      |
|         *年*        | ---                                                                                                                                                                                                                    | ---                                                  |
|         *L*         | 是否为闰年                                                                                                                                                                                                             | 如果是闰年，则返回 *1*，反之返回 *0*。               |
|         *o*         | ISO-8601 规范的年份，同 *Y* 格式。有一种情况除外：当 ISO 的周数（*W*）属于前一年或者后一年时，会返回前一年或者后一年的年份数字表达。 属于前一年或者后一年时，会返回前一年或者后一年的年份数字表达。 （PHP 5.1.0 新加） | 示例：*1999* 或 *2003*                               |
|         *Y*         | 4 位数字的年份                                                                                                                                                                                                         | 示例：*1999* 或 *2003*                               |
|         *y*         | 2 位数字的年份                                                                                                                                                                                                         | 示例： *99* 或 *03*                                  |
|        *时间*       | ---                                                                                                                                                                                                                    | ---                                                  |
|         *a*         | 上午还是下午，2 位小写字符                                                                                                                                                                                             | *am* 或 *pm*                                         |
|         *A*         | 上午还是下午，2 位大写字符                                                                                                                                                                                             | *AM* 或 *PM*                                         |
|         *B*         | 斯沃琪因特网时间                                                                                                                                                                                                       | 从 *000* 到 *999*                                    |
|         *g*         | 小时，12时制，无前导 0                                                                                                                                                                                                 | 从 *1* 到 *12*                                       |
|         *G*         | 小时，24时制，无前导 0                                                                                                                                                                                                 | 从 *0* 到 *23*                                       |
|         *h*         | 小时，12时制，有前导 0 的 2 位数字                                                                                                                                                                                     | 从 *01* 到 *12*                                      |
|         *H*         | 小时，24时制，有前导 0 的 2 位数字                                                                                                                                                                                     | *00* through *23*                                    |
|         *i*         | 分钟，有前导 0 的 2 位数字                                                                                                                                                                                             | 从 *00* 到 *59*                                      |
|         *s*         | 秒，有前导 0 的 2 位数字                                                                                                                                                                                               | 从 *00* 到 *59*                                      |
|         *u*         | 毫秒 （PHP 5.2.2 新加）                                                                                                                                                                                                | 示例： *654321*                                      |
|        *时区*       | ---                                                                                                                                                                                                                    | ---                                                  |
|         *e*         | 时区标识（PHP 5.1.0 新加）                                                                                                                                                                                             | 示例: *UTC*, *GMT*, *Atlantic/Azores*                |
|  *I* （大写字母 i） | 是否夏令时                                                                                                                                                                                                             | 如果是夏令时则返回 *1*，反之返回 *0*。               |
|         *O*         | 和格林威治时间（GMT）的时差，以小时为单位                                                                                                                                                                              | 示例： *+0200*                                       |
|         *P*         | 和格林威治时间（GMT）的时差，包括小时和分钟，小时和分钟之间使用冒号（:）分隔（PHP 5.1.3 新加）                                                                                                                         | 示例： *+02:00*                                      |
|         *T*         | 时区缩写                                                                                                                                                                                                               | 示例：*EST*, *MDT* ...                               |
|         *Z*         | 以秒为单位的时区偏移量。UTC 以西的时区返回负数，UTC 以东的时区返回正数。                                                                                                                                               | 从 *-43200* 到 *50400*                               |
|  *完整的日期/时间*  | ---                                                                                                                                                                                                                    | ---                                                  |
|         *c*         | ISO 8601 日期及时间（PHP 5 新加）                                                                                                                                                                                      | 2004-02-12T15:19:21+00:00                            |
|         *r*         | <a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC 2822</a> 格式的日期和时间                                                                                                                       | 示例：*Thu, 21 Dec 2000 16:01:07 +0200*              |
|         *U*         | 自 1970 年 1 月 1 日 0 时 0 分 0 秒（GMT 时间）以来的时间，以秒为单位                                                                                                                                                  | 参见<span class="function">time</span>               |

格式化字符串中的不可识别字符将原样输出。 当使用 <span
class="function">gmdate</span> 函数时， *Z* 格式永远返回 *0*。

> **Note**:
>
> 由于本函数仅接受 <span class="type">integer</span>
> 类型的时间戳参数，所以 *u* 格式仅在使用 <span
> class="function">date\_format</span> 函数并且使用 <span
> class="function">date\_create</span> 函数创建时间戳时才是有用的。

`timestamp`  
可选的 `timestamp` 参数是一个 <span class="type">integer</span> 的 Unix
时间戳，如未指定，参数值默认为当前本地时间。也就是说，其值默认为 <span
class="function">time</span> 的返回值。

### 返回值

返回格式化后的日期时间的字符串表达。 如果 `timestamp`
参数不是一个有效数值，则返回 **`FALSE`** 并引发 **`E_WARNING`**
级别的错误。

### 错误／异常

在每 次调用日期/时间函数时，如果时区无效则会引发 **`E_NOTICE`**
错误，如果使用系统设定值或 `TZ` 环境变量，则会引发 **`E_STRICT`** 或
**`E_WARNING`** 消息。参见 <span
class="function">date\_default\_timezone\_set</span>。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                       |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.1.0 | 时间戳的有效取值范围为 GMT 时间的 1901 年 12 月 13 日至 GMT 时间的 2038 年 1 月 19 日。 （32 位有符号整数的取值范围）。 但是，在 PHP 5.1.0 之前的版本，在某些系统（例如 Windows）上有效取值范围为 1970 年 1 月 1 日至 2038 年 1 月 19 日。 |
| 5.1.0 | 现在发布 **`E_STRICT`** 和 **`E_NOTICE`** 时区错误。                                                                                                                                                                                       |
| 5.1.1 | `format` 参数标准的可用日期/时间格式常量见： <a href="/datetime/constants.html" class="link">常量</a>                                                                                                                                      |

### 范例

**示例 \#5 <span class="function">date</span> 函数示例**

``` php
<?php
// 设置默认时区。PHP 5.1 之后版本可用
date_default_timezone_set('UTC');


// 输出类似： Monday
echo date("l");

// 输出类似：Monday 8th of August 2005 03:12:46 PM
echo date('l jS \of F Y h:i:s A');

// 输出：July 1, 2000 is on a Saturday
echo "July 1, 2000 is on a " . date("l", mktime(0, 0, 0, 7, 1, 2000));

/* 使用格式常量 */
// 输出类似： Mon, 15 Aug 2005 15:12:46 UTC
echo date(DATE_RFC822);

// 输出类似：2000-07-01T00:00:00+00:00
echo date(DATE_ATOM, mktime(0, 0, 0, 7, 1, 2000));
?>
```

可以使用反斜线进行转义来阻止函数解析格式字符串中的可识别字符。
如果反斜线和要转义的字符连在一起依然是一个有效的字符序列，那么需要对
反斜线再次进行转义。

**示例 \#6 对 <span class="function">date</span>
函数中的格式字符串进行转义**

``` php
<?php
// 输出类似： Wednesday the 15th
echo date('l \t\h\e jS');
?>
```

可以联合使用 <span class="function">date</span> 和 <span
class="function">mktime</span> 函数 来构造之前或者之后的日期时间。

**示例 \#7 <span class="function">date</span> 和 <span
class="function">mktime</span> 联合使用示例**

``` php
<?php
$tomorrow  = mktime(0, 0, 0, date("m")  , date("d")+1, date("Y"));
$lastmonth = mktime(0, 0, 0, date("m")-1, date("d"),   date("Y"));
$nextyear  = mktime(0, 0, 0, date("m"),   date("d"),   date("Y")+1);
?>
```

> **Note**:
>
> 由于存在夏令时时间， 所以此方案相对于直接在时间戳上加/减秒数
> 要更加可靠。

<span class="function">date</span> 函数格式化的一些示例。
需要注意的是，即使是对于当前来说并不具有特殊含义的字符，
也要像对待具有特殊含义的字符那样进行转义，以避免函数返回非预期的值。
因为可能在将来的 PHP 版本中，这些字符会被赋予特殊的含义。
进行转义的时候，请确保使用单引号，以避免 \\n 被解释为换行符号。

**示例 \#8 <span class="function">date</span> 函数格式化**

``` php
<?php
// 假设今天是 2001 年 3 月 10 日下午 5 点 16 分 18 秒，
// 并且位于山区标准时间（MST）时区

$today = date("F j, Y, g:i a");                 // March 10, 2001, 5:16 pm
$today = date("m.d.y");                         // 03.10.01
$today = date("j, n, Y");                       // 10, 3, 2001
$today = date("Ymd");                           // 20010310
$today = date('h-i-s, j-m-y, it is w Day');     // 05-16-18, 10-03-01, 1631 1618 6 Satpm01
$today = date('\i\t \i\s \t\h\e jS \d\a\y.');   // it is the 10th day.
$today = date("D M j G:i:s T Y");               // Sat Mar 10 17:16:18 MST 2001
$today = date('H:m:s \m \i\s\ \m\o\n\t\h');     // 17:03:18 m is month
$today = date("H:i:s");                         // 17:16:18
?>
```

如果需要将日期时间格式化为其他语言，你应该使用 <span
class="function">setlocale</span> 和 <span
class="function">strftime</span> 函数 来替代 <span
class="function">date</span> 函数。

### 注释

> **Note**:
>
> 使用 <span class="function">strtotime</span>
> 函数将一个字符串表达的日期时间转换为时间戳。
> 另外，一些数据库产品也提供了将日期时间格式转换为时间戳的函数。 （例如
> MySQL 中的
> <a href="http://dev.mysql.com/doc/mysql/en/date-and-time-functions.html" class="link external">» UNIX_TIMESTAMP</a>
> 函数）。

**小贴士**

从 PHP 5.1 版本开始，请求的开始时间可以从变量 `$_SERVER['REQUEST_TIME']`
中获取。

### 参见

-   <span class="function">gmdate</span>
-   <span class="function">idate</span>
-   <span class="function">getdate</span>
-   <span class="function">getlastmod</span>
-   <span class="function">mktime</span>
-   <span class="function">strftime</span>
-   <span class="function">time</span>
-   <span class="function">strtotime</span>
-   <a href="/class/datetimeinterface.html#预定义常量" class="link">预定义的日期时间常量</a>

getdate
=======

取得日期／时间信息

### 说明

<span class="type">array</span> <span class="methodname">getdate</span>
(\[ <span class="methodparam"><span class="type">int</span>
`$timestamp`<span class="initializer"> = time()</span></span> \] )

返回一个根据 `timestamp` 得出的包含有日期信息的关联数组 <span
class="type">array</span>。如果没有给出时间戳则认为是当前本地时间。

### 参数

`timestamp`  
可选的 `timestamp` 参数是一个 <span class="type">integer</span> 的 Unix
时间戳，如未指定，参数值默认为当前本地时间。也就是说，其值默认为 <span
class="function">time</span> 的返回值。

### 返回值

返回一个根据 `timestamp` 得出的包含有日期信息的关联数组 <span
class="type">array</span>。 返回的关联数组中的键名单元有以下几个：

| 键名        | 说明                                                                                                                               | 返回值例子                                           |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| *"seconds"* | 秒的数字表示                                                                                                                       | *0* 到 *59*                                          |
| *"minutes"* | 分钟的数字表示                                                                                                                     | *0* 到 *59*                                          |
| *"hours"*   | 小时的数字表示                                                                                                                     | *0* 到 *23*                                          |
| *"mday"*    | 月份中第几天的数字表示                                                                                                             | *1* 到 *31*                                          |
| *"wday"*    | 星期中第几天的数字表示                                                                                                             | *0* (周日) 到 *6* (周六)                             |
| *"mon"*     | 月份的数字表示                                                                                                                     | *1* 到 *12*                                          |
| *"year"*    | 4 位数字表示的完整年份                                                                                                             | 比如： *1999* 或 *2003*                              |
| *"yday"*    | 一年中第几天的数字表示                                                                                                             | *0* 到 *365*                                         |
| *"weekday"* | 星期几的完整文本表示                                                                                                               | *Sunday* 到 *Saturday*                               |
| *"month"*   | 月份的完整文本表示，比如 January 或 March                                                                                          | *January* 到 *December*                              |
| *0*         | 自从 Unix 纪元开始至今的秒数，和 <span class="function">time</span> 的返回值以及用于 <span class="function">date</span> 的值类似。 | 系统相关，典型值为从 *-2147483648* 到 *2147483647*。 |

### 范例

**示例 \#1 <span class="function">getdate</span> 例子**

``` php
<?php
$today = getdate();
print_r($today);
?>
```

以上例程的输出类似于：

    Array
    (
        [seconds] => 40
        [minutes] => 58
        [hours]   => 21
        [mday]    => 17
        [wday]    => 2
        [mon]     => 6
        [year]    => 2003
        [yday]    => 167
        [weekday] => Tuesday
        [month]   => June
        [0]       => 1055901520
    )

### 参见

-   <span class="function">date</span>
-   <span class="function">idate</span>
-   <span class="function">localtime</span>
-   <span class="function">time</span>
-   <span class="function">setlocale</span>

gettimeofday
============

取得当前时间

### 说明

<span class="type">mixed</span> <span
class="methodname">gettimeofday</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$return_float`<span
class="initializer"> = false</span></span> \] )

本函数是 gettimeofday(2)
的接口。返回一个关联数组，包含有系统调用返回的数据。

### 参数

`return_float`  
当其设为 **`TRUE`** 时，会返回一个浮点数而不是一个数组。

### 返回值

默认返回一个 <span class="type">array</span>。如果 `return_float`
设置了则会返回一个 <span class="type">float</span>。

数组中的键为：

-   <span class="simpara"> "sec" - 自 Unix 纪元起的秒数 </span>
-   <span class="simpara"> "usec" - 微秒数 </span>
-   <span class="simpara"> "minuteswest" - 格林威治向西的分钟数 </span>
-   <span class="simpara"> "dsttime" - 夏令时修正的类型 </span>

### 更新日志

| 版本  | 说明                        |
|-------|-----------------------------|
| 5.1.0 | 增加了参数 `return_float`。 |

### 范例

**示例 \#1 <span class="function">gettimeofday</span> 例子**

``` php
<?php
print_r(gettimeofday());

echo gettimeofday(true);
?>
```

以上例程的输出类似于：

    Array
    (
        [sec] => 1073504408
        [usec] => 238215
        [minuteswest] => 0
        [dsttime] => 1
    )

    1073504408.23910

gmdate
======

格式化一个 GMT/UTC 日期／时间

### 说明

<span class="type">string</span> <span class="methodname">gmdate</span>
( <span class="methodparam"><span class="type">string</span>
`$format`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timestamp`</span> \] )

同 <span class="function">date</span>
函数完全一样，只除了返回的时间是格林威治标准时（GMT）。例如当在中国（GMT
+0800）运行以下程序时，第一行显示“Jan 01 2000 00:00:00”而第二行显示“Dec
31 1999 16:00:00”。

**示例 \#1 <span class="function">gmdate</span> 例子**

``` php
<?php
echo date("M d Y H:i:s", mktime (0,0,0,1,1,2000));
echo gmdate("M d Y H:i:s", mktime (0,0,0,1,1,2000));
?>
```

> **Note**:
>
> 在 PHP 5.1.0 之前，负的时间戳（1970 年之前的日期）在某些系统下（例如
> Windows）不能工作。

参见 <span class="function">date</span>，<span
class="function">mktime</span>，<span class="function">gmmktime</span>
和 <span class="function">strftime</span>。

gmmktime
========

取得 GMT 日期的 UNIX 时间戳

### 说明

<span class="type">int</span> <span class="methodname">gmmktime</span>
(\[ <span class="methodparam"><span class="type">int</span>
`$hour`</span> \[, <span class="methodparam"><span
class="type">int</span> `$minute`</span> \[, <span
class="methodparam"><span class="type">int</span> `$second`</span> \[,
<span class="methodparam"><span class="type">int</span> `$month`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$day`</span> \[, <span class="methodparam"><span
class="type">int</span> `$year`</span> \[, <span
class="methodparam"><span class="type">int</span> `$is_dst`</span>
\]\]\]\]\]\]\] )

和 <span class="function">mktime</span>
完全一样，只除了返回值是格林威治标准时的时间戳。

参数总是表示 GMT 日期，因此 `is_dst` 对结果没有影响。

和 <span class="function">mktime</span>
一样，参数可以从右到左依次空着，空着的参数会被设为相应的当前 GMT 值。

> **Note**:
>
> 自 5.1.0 起，`is_dst` 参数被废弃。因此应该用新的时区处理特性。

> **Note**: <span class="simpara"> <span
> class="function">gmmktime</span> 内部使用了 <span
> class="function">mktime</span>，因此只有转换成本地时间也合法的时间才能用在其中。
> so only times valid in derived local time can be used. </span>

**示例 \#1 <span class="function">gmmktime</span> 在 Windows 中的边界**

``` php
<?php
gmmktime(0, 0, 0, 1, 1, 1970); // 在 GMT 和西方合法，在东方不合法
?>
```

参见 <span class="function">mktime</span>，<span
class="function">date</span> 和 <span class="function">time</span>。

gmstrftime
==========

根据区域设置格式化 GMT/UTC 时间／日期

### 说明

<span class="type">string</span> <span
class="methodname">gmstrftime</span> ( <span class="methodparam"><span
class="type">string</span> `$format`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timestamp`</span> \]
)

和 <span class="function">strftime</span>
的行为相同，只除了返回时间是格林威治标准时（GMT）。例如，当在东部标准时（EST，GMT
-500）运行时，下面第一行显示“Dec 31 1998 20:00:00”，而第二行显示“Jan 01
1999 01:00:00”。

**示例 \#1 <span class="function">gmstrftime</span> 例子**

``` php
<?php
setlocale(LC_TIME, 'en_US');
echo strftime("%b %d %Y %H:%M:%S", mktime (20,0,0,12,31,98))."\n";
echo gmstrftime("%b %d %Y %H:%M:%S", mktime (20,0,0,12,31,98))."\n";
?>
```

参见 <span class="function">strftime</span>。

idate
=====

将本地时间日期格式化为整数

### 说明

<span class="type">int</span> <span class="methodname">idate</span> (
<span class="methodparam"><span class="type">string</span>
`$format`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timestamp`</span> \] )

根据给定的格式字符对 `timestamp` 格式化并返回数字结果。`timestamp`
为可选项，默认值为本地当前时间，即 <span class="function">time</span>
的值。

和 <span class="function">date</span> 不同，<span
class="function">idate</span> 只接受一个字符作为 `format` 参数。

| `format` 字符 | 说明                                                                                                  |
|---------------|-------------------------------------------------------------------------------------------------------|
| *B*           | Swatch Beat/Internet Time                                                                             |
| *d*           | 月份中的第几天                                                                                        |
| *h*           | 小时（12 小时格式）                                                                                   |
| *H*           | 小时（24 小时格式）                                                                                   |
| *i*           | 分钟                                                                                                  |
| *I*           | 如果启用夏时制则返回 *1*，否则返回 *0*                                                                |
| *L*           | 如果是闰年则返回 *1*，否则返回 *0*                                                                    |
| *m*           | 月份的数字                                                                                            |
| *s*           | 秒数                                                                                                  |
| *t*           | 本月的总天数                                                                                          |
| *U*           | 自 Unix 纪元（January 1 1970 00:00:00 GMT）起的秒数——这和 <span class="function">time</span> 作用相同 |
| *w*           | 星期中的第几天（星期天是 *0*）                                                                        |
| *W*           | ISO-8601 格式年份中的第几个星期，每星期从星期一开始                                                   |
| *y*           | 年份（1 或 2 位数字——见下面说明）                                                                     |
| *Y*           | 年份（4 位数字）                                                                                      |
| *z*           | 年份中的第几天                                                                                        |
| *Z*           | 以秒为单位的时区偏移量                                                                                |

> **Note**:
>
> 因为 <span class="function">idate</span> 总是返回 <span
> class="type">integer</span>，不能以“0”开头，因此 <span
> class="function">idate</span>
> 可能会返回比用户期望中要少的数字。见下面例子：

``` php
<?php
$timestamp = strtotime('1st January 2004'); //1072915200

// 下面以两位数字格式显示年份，但是因为
// 以“0”打头，因此只会显示“4”
echo idate('y', $timestamp);
?>
```

参见 <span class="function">date</span> 和 <span
class="function">time</span>。

localtime
=========

取得本地时间

### 说明

<span class="type">array</span> <span
class="methodname">localtime</span> (\[ <span class="methodparam"><span
class="type">int</span> `$timestamp`<span class="initializer"> =
time()</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$is_associative`<span class="initializer"> =
false</span></span> \]\] )

<span class="function">localtime</span> 函数返回一个数组，其结构和 C
函数调用返回的完全一样。

### 参数

`timestamp`  
可选的 `timestamp` 参数是一个 <span class="type">integer</span> 的 Unix
时间戳，如未指定，参数值默认为当前本地时间。也就是说，其值默认为 <span
class="function">time</span> 的返回值。

`is_associative`  
如果设为 **`FALSE`**
或未提供则返回的是普通的数字索引数组。如果该参数设为 **`TRUE`** 则 <span
class="function">localtime</span> 函数返回包含有所有从 C 的 localtime
函数调用所返回的不同单元的关联数组。关联数组中不同的键名为：

-   <span class="simpara"> "tm\_sec" - 秒数， *0* 到 *59* </span>
-   <span class="simpara"> "tm\_min" - 分钟数， *0* 到 *59* </span>
-   <span class="simpara"> "tm\_hour" - 小时， *0* 到 *23* </span>
-   <span class="simpara"> "tm\_mday" - 月份中的第几日， *1* 到 *31*
    </span>
-   <span class="simpara"> "tm\_mon" - 年份中的第几个月， *0* (Jan) 到
    *11* (Dec) </span>
-   <span class="simpara"> "tm\_year" - 年份，从 1900 开始 </span>
-   <span class="simpara"> "tm\_wday" - 星期中的第几天， *0* (Sun) 到
    *6* (Sat) </span>
-   <span class="simpara"> "tm\_yday" - 一年中的第几天， *0* 到 *365*
    </span>
-   <span class="simpara"> "tm\_isdst" - 夏令时当前是否生效？ </span>
    <span class="simpara"> 如果是生效的是正数， *0*
    代表未生效，负数代表未知。 </span>

### 错误／异常

在每 次调用日期/时间函数时，如果时区无效则会引发 **`E_NOTICE`**
错误，如果使用系统设定值或 `TZ` 环境变量，则会引发 **`E_STRICT`** 或
**`E_WARNING`** 消息。参见 <span
class="function">date\_default\_timezone\_set</span>。

### 更新日志

| 版本  | 说明                                                 |
|-------|------------------------------------------------------|
| 5.1.0 | 现在发布 **`E_STRICT`** 和 **`E_NOTICE`** 时区错误。 |

### 范例

**示例 \#1 <span class="function">localtime</span> 例子**

``` php
<?php
$localtime = localtime();
$localtime_assoc = localtime(time(), true);
print_r($localtime);
print_r($localtime_assoc);
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => 24
        [1] => 3
        [2] => 19
        [3] => 3
        [4] => 3
        [5] => 105
        [6] => 0
        [7] => 92
        [8] => 1
    )

    Array
    (
        [tm_sec] => 24
        [tm_min] => 3
        [tm_hour] => 19
        [tm_mday] => 3
        [tm_mon] => 3
        [tm_year] => 105
        [tm_wday] => 0
        [tm_yday] => 92
        [tm_isdst] => 1
    )

### 参见

-   <span class="function">getdate</span>

microtime
=========

返回当前 Unix 时间戳和微秒数

### 说明

<span class="type">mixed</span> <span
class="methodname">microtime</span> (\[ <span class="methodparam"><span
class="type">bool</span> `$get_as_float`</span> \] )

<span class="function">microtime</span> 当前 Unix
时间戳以及微秒数。本函数仅在支持 gettimeofday()
系统调用的操作系统下可用。

如果调用时不带可选参数，本函数以 "msec sec" 的格式返回一个字符串，其中
sec 是自 Unix 纪元（0:00:00 January 1, 1970 GMT）起到现在的秒数，msec
是微秒部分。字符串的两部分都是以秒为单位返回的。

如果给出了 `get_as_float` 参数并且其值等价于 **`TRUE`**，<span
class="function">microtime</span> 将返回一个浮点数。

> **Note**: <span class="simpara"> `get_as_float` 参数是 PHP 5.0.0
> 新加的。 </span>

**示例 \#1 用 <span class="function">microtime</span> 对脚本的运行计时**

``` php
<?php
/**
 * Simple function to replicate PHP 5 behaviour
 */
function microtime_float()
{
    list($usec, $sec) = explode(" ", microtime());
    return ((float)$usec + (float)$sec);
}

$time_start = microtime_float();

// Sleep for a while
usleep(100);

$time_end = microtime_float();
$time = $time_end - $time_start;

echo "Did nothing in $time seconds\n";
?>
```

参见 <span class="function">time</span>。

mktime
======

取得一个日期的 Unix 时间戳

### 说明

<span class="type">int</span> <span class="methodname">mktime</span> (\[
<span class="methodparam"><span class="type">int</span> `$hour`<span
class="initializer"> = date("H")</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$minute`<span
class="initializer"> = date("i")</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$second`<span
class="initializer"> = date("s")</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$month`<span
class="initializer"> = date("n")</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$day`<span
class="initializer"> = date("j")</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$year`<span
class="initializer"> = date("Y")</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$is_dst`<span
class="initializer"> = -1</span></span> \]\]\]\]\]\]\] )

根据给出的参数返回 Unix 时间戳。时间戳是一个长整数，包含了从 Unix
纪元（January 1 1970 00:00:00 GMT）到给定时间的秒数。

参数可以从右向左省略，任何省略的参数会被设置成本地日期和时间的当前值。

### 注释

> **Note**:
>
> As of PHP 5.1, when called with no arguments, <span
> class="function">mktime</span> throws an **`E_STRICT`** notice: use
> the <span class="function">time</span> function instead.

### 参数

`hour`  
小时数。 The number of the hour relative to the start of the day
determined by `month`, `day` and `year`. Negative values reference the
hour before midnight of the day in question. Values greater than 23
reference the appropriate hour in the following day(s).

`minute`  
分钟数。 The number of the minute relative to the start of the `hour`.
Negative values reference the minute in the previous hour. Values
greater than 59 reference the appropriate minute in the following
hour(s).

`second`  
秒数（一分钟之内）。 The number of seconds relative to the start of the
`minute`. Negative values reference the second in the previous minute.
Values greater than 59 reference the appropriate second in the following
minute(s).

`month`  
月份数。 The number of the month relative to the end of the previous
year. Values 1 to 12 reference the normal calendar months of the year in
question. Values less than 1 (including negative values) reference the
months in the previous year in reverse order, so 0 is December, -1 is
November, etc. Values greater than 12 reference the appropriate month in
the following year(s).

`day`  
天数。 The number of the day relative to the end of the previous month.
Values 1 to 28, 29, 30 or 31 (depending upon the month) reference the
normal days in the relevant month. Values less than 1 (including
negative values) reference the days in the previous month, so 0 is the
last day of the previous month, -1 is the day before that, etc. Values
greater than the number of days in the relevant month reference the
appropriate day in the following month(s).

`year`  
年份数，可以是两位或四位数字，0-69 对应于 2000-2069，70-100 对应于
1970-2000。在如今系统中普遍把 time\_t 作为一个 32
位有符号整数的情况下，`year` 的合法范围是 1901 到 2038
之间，不过此限制自 PHP 5.1.0 起已被克服了。

`is_dst`  
本参数可以设为 1，表示正处于夏时制时间（DST），0 表示不是夏时制，或者
-1（默认值）表示不知道是否是夏时制。如果未知，PHP
会尝试自己搞明白。这可能产生不可预知（但并非不正确）的结果。如果 PHP
运行的系统中启用了 DST 或者 `is_dst` 设为 1，某些时间是无效的。例如 DST
自 2:00 生效，则所有处于 2:00 到 3:00 之间的时间都无效，<span
class="function">mktime</span>
会返回一个未定义（通常为负）的值。某些系统（例如 Solaris 8）的 DST
在午夜生效，则 DST 生效当天的 0:30 会被计算为前一天的 23:30。

> **Note**:
>
> 自 PHP 5.1.0 起，本参数已被废弃。应该使用新的时区处理特性来替代。

> **Note**:
>
> PHP 7.0.0 起，此参数已经被移除。

### 返回值

<span class="function">mktime</span> 根据给出的参数返回 Unix
时间戳。如果参数非法，本函数返回 **`FALSE`**（在 PHP 5.1 之前返回
*-1*）。

### 错误／异常

在每 次调用日期/时间函数时，如果时区无效则会引发 **`E_NOTICE`**
错误，如果使用系统设定值或 `TZ` 环境变量，则会引发 **`E_STRICT`** 或
**`E_WARNING`** 消息。参见 <span
class="function">date\_default\_timezone\_set</span>。

### 更新日志

| 版本  | 说明                                                                                                                                                           |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.0.0 | `is_dst`参数已经被移除。                                                                                                                                       |
| 5.3.0 | <span class="function">mktime</span> now throws **`E_DEPRECATED`** notice if the `is_dst` parameter is used.                                                   |
| 5.1.0 | `is_dst` 参数被废弃。出错时函数返回 **`FALSE`** 而不再是 *-1*。修正了本函数可以接受年月日参数全为零。                                                          |
| 5.1.0 | When called with no arguments, <span class="function">mktime</span> throws **`E_STRICT`** notice. Use the <span class="function">time</span> function instead. |
| 5.1.0 | 现在发布 **`E_STRICT`** 和 **`E_NOTICE`** 时区错误。                                                                                                           |

### 范例

**示例 \#1 基本例子**

``` php
<?php
// Set the default timezone to use. Available as of PHP 5.1
date_default_timezone_set('UTC');

// Prints: July 1, 2000 is on a Saturday
echo "July 1, 2000 is on a " . date("l", mktime(0, 0, 0, 7, 1, 2000));

// Prints something like: 2006-04-05T01:02:03+00:00
echo date('c', mktime(1, 2, 3, 4, 5, 2006));
?>
```

**示例 \#2 <span class="function">mktime</span> 例子**

<span class="function">mktime</span>
在做日期计算和验证方面很有用，它会自动计算超出范围的输入的正确值。例如下面例子中每一行都会产生字符串
"Jan-01-1998"。

``` php
<?php
echo date("M-d-Y", mktime(0, 0, 0, 12, 32, 1997));
echo date("M-d-Y", mktime(0, 0, 0, 13, 1, 1997));
echo date("M-d-Y", mktime(0, 0, 0, 1, 1, 1998));
echo date("M-d-Y", mktime(0, 0, 0, 1, 1, 98));
?>
```

**示例 \#3 下个月的最后一天**

任何给定月份的最后一天都可以被表示为下个月的第 "0" 天，而不是 -1
天。下面两个例子都会产生字符串 "The last day in Feb 2000 is: 29"。

``` php
<?php
$lastday = mktime(0, 0, 0, 3, 0, 2000);
echo strftime("Last day in Feb 2000 is: %d", $lastday);
$lastday = mktime(0, 0, 0, 4, -31, 2000);
echo strftime("Last day in Feb 2000 is: %d", $lastday);
?>
```

### 注释

**Caution**

在 PHP 5.1.0 之前，在任何已知 Windows
版本以及一些其它系统下不支持负的时间戳。因此年份的有效范围限制为 1970 到
2038。

### 参见

-   <span class="function">checkdate</span>
-   <span class="function">gmmktime</span>
-   <span class="function">date</span>
-   <span class="function">time</span>

strftime
========

根据区域设置格式化本地时间／日期

### 说明

<span class="type">string</span> <span
class="methodname">strftime</span> ( <span class="methodparam"><span
class="type">string</span> `$format`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timestamp`<span
class="initializer"> = time()</span></span> \] )

返回用给定的格式字串对给出的 `timestamp`
进行格式输出后的字符串。如果没有给出时间戳则用当前的本地时间。月份和星期几以及其它和语言有关的字符串写法和用
<span class="function">setlocale</span> 设定的当前的区域有关。

可能不是所有的转换标记都被 C 库文件支持，这种情况下 PHP 的 <span
class="function">strftime</span>
也不支持。此外，不是所有的平台都支持负的时间戳，因此日期的范围可能限定在不早于
Unix 纪元。这意味着例如 %e, %T，%R 和 %D（可能更多）以及早于 *Jan 1,
1970* 的时间在 Windows，一些 Linux
发行版本，以及其它几个操作系统中无效。对于 Windows
系统，所支持的转换标记可在
<a href="http://msdn.microsoft.com/en-us/library/fe06s4ak.aspx" class="link external">» MSDN 网站</a>找到。

### 参数

`format`  
|       `格式`       | 描述                                                                                                                                                                        | 返回值示例                                                         |
|:------------------:|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
|        *日*        | ---                                                                                                                                                                         | ---                                                                |
|        *%a*        | 当前区域星期几的简写                                                                                                                                                        | *Sun* 到 *Sat*                                                     |
|        *%A*        | 当前区域星期几的全称                                                                                                                                                        | *Sunday* 到 *Saturday*                                             |
|        *%d*        | 月份中的第几天，十进制数字（范围从 01 到 31）                                                                                                                               | *01* 到 *31*                                                       |
|        *%e*        | 月份中的第几天，十进制数字，一位的数字前会加上一个空格（范围从 ' 1' 到 '31'） 在 Windows 上尚未按描述实现。更多信息见下方。                                                 | *1* 到 *31*                                                        |
|        *%j*        | 年份中的第几天，带前导零的三位十进制数（范围从 001 到 366）                                                                                                                 | *001* 到 *366*                                                     |
|        *%u*        | 符合 ISO-8601 星期几的十进制数表达 \[1,7\]，1 表示星期一                                                                                                                    | *1* (星期一) 到 *7* (星期日)                                       |
|        *%w*        | 星期中的第几天，星期天为 0                                                                                                                                                  | *0* (星期天) 到 *6* (星期六)                                       |
|        *周*        | ---                                                                                                                                                                         | ---                                                                |
|        *%U*        | 本年的第几周，从第一周的第一个星期天作为第一天开始                                                                                                                          | *13* (for the 13th full week of the year)                          |
|        *%V*        | %V - 本年第几周的 ISO-8601:1988 格式，范围从 01 到 53，第 1 周是本年第一个至少还有 4 天的星期，星期一作为每周的第一天。（用 %G 或者 %g 作为指定时间戳相应周数的年份组成。） | *01* 到 *53* (where 53 accounts for an overlapping week)           |
|        *%W*        | 本年的第几周数，从第一周的第一个星期一作为第一天开始                                                                                                                        | *46* (for the 46th week of the year beginning with a Monday)       |
|        *月*        | ---                                                                                                                                                                         | ---                                                                |
|        *%b*        | 当前区域月份的简写                                                                                                                                                          | *Jan* 到 *Dec*                                                     |
|        *%B*        | 当前区域月份的全称                                                                                                                                                          | *January* 到 *December*                                            |
|        *%h*        | 当前区域月份的简写（%b 的别名）                                                                                                                                             | *Jan* 到 *Dec*                                                     |
|        *%m*        | 两位数的月份                                                                                                                                                                | *01* (是一月份) 到 *12* (是十二月份)                               |
|        *年*        | ---                                                                                                                                                                         | ---                                                                |
|        *%C*        | 两位数显示世纪（年份除以 100，截成整数）                                                                                                                                    | *19* 是 20 世纪                                                    |
|        *%g*        | 2 位数的年份，符合 ISO-8601:1988 星期数（参见 %V）。和 %V 的格式和值一样，只除了如果 ISO 星期数属于前一年或者后一年，则使用那一年。                                         | 比如：2009年1月6日那一周是 *09*。                                  |
|        *%G*        | %g 的完整四位数版本                                                                                                                                                         | 比如：2009年1月3日那一周是 *2008*.                                 |
|        *%y*        | 两位数显示年份                                                                                                                                                              | 比如： *09* 是 2009，*79* 是 1979                                  |
|        *%Y*        | 四位数显示年份                                                                                                                                                              | 比如： *2038*                                                      |
|       *时间*       | ---                                                                                                                                                                         | ---                                                                |
|        *%H*        | 以 24 小时格式显示两位小时数                                                                                                                                                | *00* 到 *23*                                                       |
|        *%I*        | 以 12 小时格式显示两位小时数                                                                                                                                                | *01* 到 *12*                                                       |
| *%l（'L' 的小写）* | 以 12 小时格式显示小时数，单个数字前含空格                                                                                                                                  | *1* 到 *12*                                                        |
|        *%M*        | 两位的分钟数                                                                                                                                                                | *00* 到 *59*                                                       |
|        *%p*        | 指定时间的大写 “AM” 或 “PM”                                                                                                                                                 | 比如： 00:31 是 *AM* ，22:23 是*PM*                                |
|        *%P*        | 指定时间的小写 “am” 或 “pm”                                                                                                                                                 | 比如：00:31 是 *am* ，22:23 是*pm*                                 |
|        *%r*        | 和 "%I:%M:%S %p" 一样                                                                                                                                                       | 比如： 21:34:17 是 *09:34:17 PM*                                   |
|        *%R*        | 和 "%H:%M" 一样                                                                                                                                                             | 比如： 12:35 AM 是 *00:35*，4:44 PM 是 *16:44*                     |
|        *%S*        | 两位数字表示秒                                                                                                                                                              | *00* 到 *59*                                                       |
|        *%T*        | 和 "%H:%M:%S" 一样                                                                                                                                                          | 比如： 09:34:17 PM 是 *21:34:17*                                   |
|        *%X*        | 当前区域首选的时间表示法，不包括日期                                                                                                                                        | 例如： *03:59:16* 或 *15:59:16*                                    |
|        *%z*        | 从 UTC 的时区偏移 或 简写（由操作系统决定）                                                                                                                                 | 比如： 东部时间是 *-0500* 或 *EST*                                 |
|        *%Z*        | %z 没有给出的 UTC 的时区偏移 或 简写（由操作系统决定）                                                                                                                      | 比如： *-0500* 或 *EST* 是东部时间                                 |
|   *时间和日期戳*   | ---                                                                                                                                                                         | ---                                                                |
|        *%c*        | 当前区域首选的日期时间表达                                                                                                                                                  | 比如： 2009 年 2 月 5 日上午 12:45:10 是 *Tue Feb 5 00:45:10 2009* |
|        *%D*        | 和 "%m/%d/%y" 一样                                                                                                                                                          | 比如： 2009 年 2 月 5 日是 *02/05/09*                              |
|        *%F*        | Same as "%Y-%m-%d" (commonly used in database datestamps)                                                                                                                   | 比如：2009 年 2 月 5 日是 *2009-02-05*                             |
|        *%s*        | Unix纪元的时间戳（和 <span class="function">time</span> 函数一样）                                                                                                          | 比如： 1979 年 9 月 10 日上午 8 点 40 分 00 秒是 *305815200*       |
|        *%x*        | 当前区域首选的时间表示法，不包括时间                                                                                                                                        | 比如： 2009 年 2 月 5 日是 *02/05/09*                              |
|       *其他*       | ---                                                                                                                                                                         | ---                                                                |
|        *%n*        | 换行符("\\n")                                                                                                                                                               | ---                                                                |
|        *%t*        | Tab 字符("\\t")                                                                                                                                                             | ---                                                                |
|        *%%*        | 文字上的百分字符("%")                                                                                                                                                       | ---                                                                |

这个参数的最大长度是 1023 个字符。

**Warning**
尽管 ISO 9889:1999（当前的 C 标准）明确指出一周从星期一开始，但是 Sun
Solaris 的一周似乎从星期天开始并作为 1。所以 %u
的结果也许不会和手册里描述得一样。

**Warning**
*仅针对 Windows：*这个函数里 *%e* 修饰符修饰符还不能支持 Windows。
为了得到这个值可以用 *%\#d*
修饰符来代替。下例说明了如何写一个跨平台支持的函数。

**Warning**
*仅针对 Mac OS X：*这个函数里 *%P* 修饰符还不能支持 Mac OS X。

`timestamp`  
可选的 `timestamp` 参数是一个 <span class="type">integer</span> 的 Unix
时间戳，如未指定，参数值默认为当前本地时间。也就是说，其值默认为 <span
class="function">time</span> 的返回值。

### 返回值

根据指定的 `timestamp` 或未给出 timestamp 是使用当前本地时间， 返回
`format` 格式化的字符。 月份、星期名和其他与语言相关的字符串遵守 <span
class="function">setlocale</span> 设置的当前区域设置。

### 错误／异常

在每 次调用日期/时间函数时，如果时区无效则会引发 **`E_NOTICE`**
错误，如果使用系统设定值或 `TZ` 环境变量，则会引发 **`E_STRICT`** 或
**`E_WARNING`** 消息。参见 <span
class="function">date\_default\_timezone\_set</span>。

由于输出依赖于 C 库，所以一些转换标记并不被支持。 在 Windows
上，使用未知的转换标记将导致 5 **`E_WARNING`** 信息，并返回
**`FALSE`**。 在其他的操作系统上，你可能不能得到任何 **`E_WARNING`**
信息， 并且可能输出未经转换的转换标记。

### 更新日志

| 版本  | 说明                                                 |
|-------|------------------------------------------------------|
| 5.1.0 | 现在发布 **`E_STRICT`** 和 **`E_NOTICE`** 时区错误。 |

### 范例

如果你的系统里安装了各自的语言环境则下例能够正常运行。

**示例 \#1 <span class="function">strftime</span> 区域的例子**

``` php
<?php
setlocale(LC_TIME, "C");
echo strftime("%A");
setlocale(LC_TIME, "fi_FI");
echo strftime(" in Finnish is %A,");
setlocale(LC_TIME, "fr_FR");
echo strftime(" in French %A and");
setlocale(LC_TIME, "de_DE");
echo strftime(" in German %A.\n");
?>
```

**示例 \#2 ISO 8601:1988 week number example**

``` php
<?php
/*     December 2002 / January 2003
ISOWk  M   Tu  W   Thu F   Sa  Su
----- ----------------------------
51     16  17  18  19  20  21  22
52     23  24  25  26  27  28  29
1      30  31   1   2   3   4   5
2       6   7   8   9  10  11  12
3      13  14  15  16  17  18  19   */

// 输出： 12/28/2002 - %V,%G,%Y = 52,2002,2002
echo "12/28/2002 - %V,%G,%Y = " . strftime("%V,%G,%Y", strtotime("12/28/2002")) . "\n";

// 输出： 12/30/2002 - %V,%G,%Y = 1,2003,2002
echo "12/30/2002 - %V,%G,%Y = " . strftime("%V,%G,%Y", strtotime("12/30/2002")) . "\n";

// 输出： 1/3/2003 - %V,%G,%Y = 1,2003,2003
echo "1/3/2003 - %V,%G,%Y = " . strftime("%V,%G,%Y",strtotime("1/3/2003")) . "\n";

// 输出： 1/10/2003 - %V,%G,%Y = 2,2003,2003
echo "1/10/2003 - %V,%G,%Y = " . strftime("%V,%G,%Y",strtotime("1/10/2003")) . "\n";



/*     December 2004 / January 2005
ISOWk  M   Tu  W   Thu F   Sa  Su
----- ----------------------------
51     13  14  15  16  17  18  19
52     20  21  22  23  24  25  26
53     27  28  29  30  31   1   2
1       3   4   5   6   7   8   9
2      10  11  12  13  14  15  16   */

// 输出： 12/23/2004 - %V,%G,%Y = 52,2004,2004
echo "12/23/2004 - %V,%G,%Y = " . strftime("%V,%G,%Y",strtotime("12/23/2004")) . "\n";

// 输出： 12/31/2004 - %V,%G,%Y = 53,2004,2004
echo "12/31/2004 - %V,%G,%Y = " . strftime("%V,%G,%Y",strtotime("12/31/2004")) . "\n";

// 输出： 1/2/2005 - %V,%G,%Y = 53,2004,2005
echo "1/2/2005 - %V,%G,%Y = " . strftime("%V,%G,%Y",strtotime("1/2/2005")) . "\n";

// 输出： 1/3/2005 - %V,%G,%Y = 1,2005,2005
echo "1/3/2005 - %V,%G,%Y = " . strftime("%V,%G,%Y",strtotime("1/3/2005")) . "\n";

?>
```

**示例 \#3 *%e* 修改器跨平台兼容的例子**

``` php
<?php

// Jan 1: results in: '%e%1%' (%%, e, %%, %e, %%)
$format = '%%e%%%e%%';

// Check for Windows to find and replace the %e 
// modifier correctly
if (strtoupper(substr(PHP_OS, 0, 3)) == 'WIN') {
    $format = preg_replace('#(?<!%)((?:%%)*)%e#', '</refsect1>%#d', $format);
}

echo strftime($format);
?>
```

**示例 \#4 显示所有已知和未知的格式**

``` php
<?php
// Describe the formats.
$strftimeFormats = array(
    'A' => 'A full textual representation of the day',
    'B' => 'Full month name, based on the locale',
    'C' => 'Two digit representation of the century (year divided by 100, truncated to an integer)',
    'D' => 'Same as "%m/%d/%y"',
    'E' => '',
    'F' => 'Same as "%Y-%m-%d"',
    'G' => 'The full four-digit version of %g',
    'H' => 'Two digit representation of the hour in 24-hour format',
    'I' => 'Two digit representation of the hour in 12-hour format',
    'J' => '',
    'K' => '',
    'L' => '',
    'M' => 'Two digit representation of the minute',
    'N' => '',
    'O' => '',
    'P' => 'lower-case "am" or "pm" based on the given time',
    'Q' => '',
    'R' => 'Same as "%H:%M"',
    'S' => 'Two digit representation of the second',
    'T' => 'Same as "%H:%M:%S"',
    'U' => 'Week number of the given year, starting with the first Sunday as the first week',
    'V' => 'ISO-8601:1988 week number of the given year, starting with the first week of the year with at least 4 weekdays, with Monday being the start of the week',
    'W' => 'A numeric representation of the week of the year, starting with the first Monday as the first week',
    'X' => 'Preferred time representation based on locale, without the date',
    'Y' => 'Four digit representation for the year',
    'Z' => 'The time zone offset/abbreviation option NOT given by %z (depends on operating system)',
    'a' => 'An abbreviated textual representation of the day',
    'b' => 'Abbreviated month name, based on the locale',
    'c' => 'Preferred date and time stamp based on local',
    'd' => 'Two-digit day of the month (with leading zeros)',
    'e' => 'Day of the month, with a space preceding single digits',
    'f' => '',
    'g' => 'Two digit representation of the year going by ISO-8601:1988 standards (see %V)',
    'h' => 'Abbreviated month name, based on the locale (an alias of %b)',
    'i' => '',
    'j' => 'Day of the year, 3 digits with leading zeros',
    'k' => '',
    'l' => 'Hour in 12-hour format, with a space preceeding single digits',
    'm' => 'Two digit representation of the month',
    'n' => 'A newline character ("\n")',
    'o' => '',
    'p' => 'UPPER-CASE "AM" or "PM" based on the given time',
    'q' => '',
    'r' => 'Same as "%I:%M:%S %p"',
    's' => 'Unix Epoch Time timestamp',
    't' => 'A Tab character ("\t")',
    'u' => 'ISO-8601 numeric representation of the day of the week',
    'v' => '',
    'w' => 'Numeric representation of the day of the week',
    'x' => 'Preferred date representation based on locale, without the time',
    'y' => 'Two digit representation of the year',
    'z' => 'Either the time zone offset from UTC or the abbreviation (depends on operating system)',
    '%' => 'A literal percentage character ("%")',
);

// Results.
$strftimeValues = array();

// Evaluate the formats whilst suppressing any errors.
foreach($strftimeFormats as $format => $description){
    if (False !== ($value = @strftime("%{$format}"))){
        $strftimeValues[$format] = $value;
    }
}

// Find the longest value.
$maxValueLength = 2 + max(array_map('strlen', $strftimeValues));

// Report known formats.
foreach($strftimeValues as $format => $value){
    echo "Known format   : '{$format}' = ", str_pad("'{$value}'", $maxValueLength), " ( {$strftimeFormats[$format]} )\n";
}

// Report unknown formats.
foreach(array_diff_key($strftimeFormats, $strftimeValues) as $format => $description){
    echo "Unknown format : '{$format}'   ", str_pad(' ', $maxValueLength), ($description ? " ( {$description} )" : ''), "\n";
}
?>
```

以上例程的输出类似于：

    Known format   : 'A' = 'Friday'            ( A full textual representation of the day )
    Known format   : 'B' = 'December'          ( Full month name, based on the locale )
    Known format   : 'H' = '11'                ( Two digit representation of the hour in 24-hour format )
    Known format   : 'I' = '11'                ( Two digit representation of the hour in 12-hour format )
    Known format   : 'M' = '24'                ( Two digit representation of the minute )
    Known format   : 'S' = '44'                ( Two digit representation of the second )
    Known format   : 'U' = '48'                ( Week number of the given year, starting with the first Sunday as the first week )
    Known format   : 'W' = '48'                ( A numeric representation of the week of the year, starting with the first Monday as the first week )
    Known format   : 'X' = '11:24:44'          ( Preferred time representation based on locale, without the date )
    Known format   : 'Y' = '2010'              ( Four digit representation for the year )
    Known format   : 'Z' = 'GMT Standard Time' ( The time zone offset/abbreviation option NOT given by %z (depends on operating system) )
    Known format   : 'a' = 'Fri'               ( An abbreviated textual representation of the day )
    Known format   : 'b' = 'Dec'               ( Abbreviated month name, based on the locale )
    Known format   : 'c' = '12/03/10 11:24:44' ( Preferred date and time stamp based on local )
    Known format   : 'd' = '03'                ( Two-digit day of the month (with leading zeros) )
    Known format   : 'j' = '337'               ( Day of the year, 3 digits with leading zeros )
    Known format   : 'm' = '12'                ( Two digit representation of the month )
    Known format   : 'p' = 'AM'                ( UPPER-CASE "AM" or "PM" based on the given time )
    Known format   : 'w' = '5'                 ( Numeric representation of the day of the week )
    Known format   : 'x' = '12/03/10'          ( Preferred date representation based on locale, without the time )
    Known format   : 'y' = '10'                ( Two digit representation of the year )
    Known format   : 'z' = 'GMT Standard Time' ( Either the time zone offset from UTC or the abbreviation (depends on operating system) )
    Known format   : '%' = '%'                 ( A literal percentage character ("%") )
    Unknown format : 'C'                       ( Two digit representation of the century (year divided by 100, truncated to an integer) )
    Unknown format : 'D'                       ( Same as "%m/%d/%y" )
    Unknown format : 'E'
    Unknown format : 'F'                       ( Same as "%Y-%m-%d" )
    Unknown format : 'G'                       ( The full four-digit version of %g )
    Unknown format : 'J'
    Unknown format : 'K'
    Unknown format : 'L'
    Unknown format : 'N'
    Unknown format : 'O'
    Unknown format : 'P'                       ( lower-case "am" or "pm" based on the given time )
    Unknown format : 'Q'
    Unknown format : 'R'                       ( Same as "%H:%M" )
    Unknown format : 'T'                       ( Same as "%H:%M:%S" )
    Unknown format : 'V'                       ( ISO-8601:1988 week number of the given year, starting with the first week of the year with at least 4 weekdays, with Monday being the start of the week )
    Unknown format : 'e'                       ( Day of the month, with a space preceding single digits )
    Unknown format : 'f'
    Unknown format : 'g'                       ( Two digit representation of the year going by ISO-8601:1988 standards (see %V) )
    Unknown format : 'h'                       ( Abbreviated month name, based on the locale (an alias of %b) )
    Unknown format : 'i'
    Unknown format : 'k'
    Unknown format : 'l'                       ( Hour in 12-hour format, with a space preceeding single digits )
    Unknown format : 'n'                       ( A newline character ("\n") )
    Unknown format : 'o'
    Unknown format : 'q'
    Unknown format : 'r'                       ( Same as "%I:%M:%S %p" )
    Unknown format : 's'                       ( Unix Epoch Time timestamp )
    Unknown format : 't'                       ( A Tab character ("\t") )
    Unknown format : 'u'                       ( ISO-8601 numeric representation of the day of the week )
    Unknown format : 'v'

### 注释

> **Note**: <span class="simpara"> %G 和
> %V，如果数字编号系统未能充分理解，基于 ISO 8601:1988
> 的星期数可能得出未预期的结果。见上面的 %V 和以下的例子。 </span>

### 参见

-   <a href="http://strftime.net/" class="link external">» 在线 strftime() 格式设计工具</a>
-   <span class="function">setlocale</span>
-   <span class="function">mktime</span>
-   <span class="function">strptime</span>
-   <span class="function">gmstrftime</span>
-   <a href="http://www.opengroup.org/onlinepubs/007908799/xsh/strftime.html" class="link external">» Open Group specification of <span class="function">strftime</span></a>

strptime
========

解析由 <span class="function">strftime</span> 生成的日期／时间

### 说明

<span class="type">array</span> <span class="methodname">strptime</span>
( <span class="methodparam"><span class="type">string</span>
`$date`</span> , <span class="methodparam"><span
class="type">string</span> `$format`</span> )

<span class="function">strptime</span> 返回一个将 `date`
解析后的数组，如果出错返回 **`FALSE`**。

月份和星期几的名字以及其它与语种有关的字符串对应于 <span
class="function">setlocale</span>设定的当前区域（**`LC_TIME`**）。

### 参数

`date`（<span class="type">string</span>）  
被解析的字符串（例如从 <span class="function">strftime</span> 返回的）

`format`（<span class="type">string</span>）  
`date` 所使用的格式（例如同 <span class="function">strftime</span>
中所使用的相同）。

更多有关格式选项的信息见 <span class="function">strftime</span> 页面。

### 返回值

返回一个数组 或者在失败时返回 **`FALSE`**

| 键名     | 说明                                        |
|----------|---------------------------------------------|
| tm\_sec  | 当前分钟内的秒数（0-61）                    |
| tm\_min  | 当前小时内的分钟数（0-59）                  |
| tm\_hour | 午夜起的小时数（0-23）                      |
| tm\_mday | 月份中的第几天（1-31）                      |
| tm\_mon  | 自一月起过了几个月（0-11）                  |
| tm\_year | 自 1900 年起过了几年                        |
| tm\_wday | 自星期天起过了几天（0-6）                   |
| tm\_yday | 本年自一月一日起过了多少天（0-365）         |
| unparsed | `date` 中未能通过指定的 `format` 识别的部分 |

### 范例

**示例 \#1 <span class="function">strptime</span> 例子**

``` php
<?php
$format = '%d/%m/%Y %H:%M:%S';
$strf = strftime($format);

echo "$strf\n";

print_r(strptime($strf, $format));
?>
```

以上例程的输出类似于：

    03/10/2004 15:54:19

    Array
    (
        [tm_sec] => 19
        [tm_min] => 54
        [tm_hour] => 15
        [tm_mday] => 3
        [tm_mon] => 9
        [tm_year] => 104
        [tm_wday] => 0
        [tm_yday] => 276
        [unparsed] =>
    )

### 注释

> **Note**: <span class="simpara">此函数未在 Windows 平台下实现。</span>

> **Note**:
>
> Internally, this function calls the *strptime()* function provided by
> the system's C library. This function can exhibit noticeably different
> behaviour across different operating systems. The use of <span
> class="function">date\_parse\_from\_format</span>, which does not
> suffer from these issues, is recommended on PHP 5.3.0 and later.

> **Note**:
>
> *"tm\_sec"* includes any leap seconds (currently upto 2 a year). For
> more information on leap seconds, see the
> <a href="http://en.wikipedia.org/wiki/Leap_second" class="link external">» Wikipedia article on leap seconds</a>.

> **Note**:
>
> Prior to PHP 5.2.0, this function could return undefined behaviour.
> Notably, the *"tm\_sec"*, *"tm\_min"* and *"tm\_hour"* entries would
> return undefined values.

### 参见

-   <span class="function">checkdate</span>
-   <span class="function">strftime</span>
-   <span class="function">date\_parse\_from\_format</span>
-   <span class="function">DateTime::createFromFormat</span>

strtotime
=========

将任何字符串的日期时间描述解析为 Unix 时间戳

### 说明

<span class="type">int</span> <span class="methodname">strtotime</span>
( <span class="methodparam"><span class="type">string</span>
`$time`</span> \[, <span class="methodparam"><span
class="type">int</span> `$now`<span class="initializer"> =
time()</span></span> \] )

本函数预期接受一个包含美国英语日期格式的字符串并尝试将其解析为 Unix
时间戳（自 January 1 1970 00:00:00 GMT 起的秒数），其值相对于 `now`
参数给出的时间，如果没有提供此参数则用系统当前时间。

本函数将使用 `TZ` 环境变量（如果有的话）来计算时间戳。自 PHP 5.1.0
起有更容易的方法来定义时区用于所有的日期／时间函数。此过程在 <span
class="function">date\_default\_timezone\_get</span> 函数页面中有说明。

### 参数

`time`  
日期/时间字符串。正确格式的说明详见
<a href="/datetime/formats.html" class="link">日期与时间格式</a>。

`now`  
用来计算返回值的时间戳。

### 返回值

成功则返回时间戳，否则返回 **`FALSE`**。在 PHP 5.1.0
之前本函数在失败时返回 *-1*。

### 错误／异常

在每 次调用日期/时间函数时，如果时区无效则会引发 **`E_NOTICE`**
错误，如果使用系统设定值或 `TZ` 环境变量，则会引发 **`E_STRICT`** 或
**`E_WARNING`** 消息。参见 <span
class="function">date\_default\_timezone\_set</span>。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                                                                       |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0 | Prior to PHP 5.3.0, relative time formats supplied to the `time` argument of <span class="function">strtotime</span> such as *this week*, *previous week*, *last week*, and *next week* were interpreted to mean a 7 day period relative to the current date/time, rather than a week period of *Monday* through *Sunday*. |
| 5.3.0 | 在 PHP 5.3.0 之前， *24:00* 不是一个有效的格式，并且 <span class="function">strtotime</span> 会返回 **`FALSE`**。                                                                                                                                                                                                          |
| 5.2.7 | In PHP 5 prior to 5.2.7, requesting a given occurrence of a given weekday in a month where that weekday was the first day of the month would incorrectly add one week to the returned timestamp. This has been corrected in 5.2.7 and later versions.                                                                      |
| 5.1.0 | 失败时返回 **`FALSE`**，不再是 *-1*。                                                                                                                                                                                                                                                                                      |
| 5.1.0 | 现在发布 **`E_STRICT`** 和 **`E_NOTICE`** 时区错误。                                                                                                                                                                                                                                                                       |
| 5.0.2 | 在 PHP 5 中到 5.0.2 之前，*"now"* 和其它相对时间从今天午夜起错误计算了。这和正确从当前时间起计算的其它版本不同。                                                                                                                                                                                                           |
| 5.0.0 | Microseconds began to be allowed, but they are ignored.                                                                                                                                                                                                                                                                    |

### 范例

**示例 \#1 <span class="function">strtotime</span> 例子**

``` php
<?php
echo strtotime("now"), "\n";
echo strtotime("10 September 2000"), "\n";
echo strtotime("+1 day"), "\n";
echo strtotime("+1 week"), "\n";
echo strtotime("+1 week 2 days 4 hours 2 seconds"), "\n";
echo strtotime("next Thursday"), "\n";
echo strtotime("last Monday"), "\n";
?>
```

**示例 \#2 失败检查**

``` php
<?php
$str = 'Not Good';

// previous to PHP 5.1.0 you would compare with -1, instead of false
if (($timestamp = strtotime($str)) === false) {
    echo "The string ($str) is bogus";
} else {
    echo "$str == " . date('l dS of F Y h:i:s A', $timestamp);
}
?>
```

### 注释

> **Note**:
>
> 如果给定的年份是两位数字的格式，则其值 0-69 表示 2000-2069，70-100
> 表示 1970-2000。 See the notes below for possible differences on 32bit
> systems (possible dates might end on 2038-01-19 03:14:07).

> **Note**:
>
> 有效的时间戳通常从 Fri, 13 Dec 1901 20:45:54 GMT 到 Tue, 19 Jan 2038
> 03:14:07 GMT（对应于 32 位有符号整数的最小值和最大值）。
>
> PHP 5.1.0
> 之前，不是所有的平台都支持负的时间戳，那么日记范围就被限制为不能早于
> Unix 纪元。这意味着在 1970 年 1 月 1 日之前的日期将不能用在
> Windows，一些 Linux 版本，以及几个其它的操作系统中。
>
> For 64-bit versions of PHP, the valid range of a timestamp is
> effectively infinite, as 64 bits can represent approximately 293
> billion years in either direction.

> **Note**:
>
> Dates in the *m/d/y* or *d-m-y* formats are disambiguated by looking
> at the separator between the various components: if the separator is a
> slash (*/*), then the American *m/d/y* is assumed; whereas if the
> separator is a dash (*-*) or a dot (*.*), then the European *d-m-y*
> format is assumed. If, however, the year is given in a two digit
> format and the separator is a dash (*-*, the date string is parsed as
> *y-m-d*.
>
> To avoid potential ambiguity, it's best to use ISO 8601 (*YYYY-MM-DD*)
> dates or <span class="methodname">DateTime::createFromFormat</span>
> when possible.

> **Note**:
>
> Using this function for mathematical operations is not advisable. It
> is better to use <span class="methodname">DateTime::add</span> and
> <span class="methodname">DateTime::sub</span> in PHP 5.3 and later, or
> <span class="methodname">DateTime::modify</span> in PHP 5.2.

### 参见

-   <a href="/datetime/formats.html" class="link">Date and Time Formats</a>
-   <span class="methodname">DateTime::createFromFormat</span>
-   <span class="function">checkdate</span>
-   <span class="function">strptime</span>

time
====

返回当前的 Unix 时间戳

### 说明

<span class="type">int</span> <span class="methodname">time</span> (
<span class="methodparam">void</span> )

返回自从 Unix 纪元（格林威治时间 1970 年 1 月 1 日
00:00:00）到当前时间的秒数。

### 范例

**示例 \#1 <span class="function">time</span> 例子**

``` php
<?php
$nextWeek = time() + (7 * 24 * 60 * 60);
                   // 7 days; 24 hours; 60 mins; 60 secs
echo 'Now:       '. date('Y-m-d') ."\n";
echo 'Next Week: '. date('Y-m-d', $nextWeek) ."\n";
// or using strtotime():
echo 'Next Week: '. date('Y-m-d', strtotime('+1 week')) ."\n";
?>
```

以上例程的输出类似于：

    Now:       2005-03-30
    Next Week: 2005-04-06
    Next Week: 2005-04-06

### 注释

**小贴士**

自 PHP 5.1 起在 `$_SERVER['REQUEST_TIME']`
中保存了发起该请求时刻的时间戳。

### 参见

-   <span class="function">date</span>
-   <span class="function">microtime</span>

timezone\_abbreviations\_list
=============================

别名 <span class="methodname">DateTimeZone::listAbbreviations</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTimeZone::listAbbreviations</span>

timezone\_identifiers\_list
===========================

别名 <span class="methodname">DateTimeZone::listIdentifiers</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTimeZone::listIdentifiers</span>

timezone\_location\_get
=======================

别名 <span class="methodname">DateTimeZone::getLocation</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTimeZone::getLocation</span>

timezone\_name\_from\_abbr
==========================

Returns the timezone name from abbreviation

### 说明

<span class="type">string</span> <span
class="methodname">timezone\_name\_from\_abbr</span> ( <span
class="methodparam"><span class="type">string</span> `$abbr`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$gmtOffset`<span class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$isdst`<span
class="initializer"> = -1</span></span> \]\] )

### 参数

`abbr`  
Time zone abbreviation.

`gmtOffset`  
Offset from GMT in seconds. Defaults to -1 which means that first found
time zone corresponding to `abbr` is returned. Otherwise exact offset is
searched and only if not found then the first time zone with any offset
is returned.

`isdst`  
Daylight saving time indicator. Defaults to -1, which means that whether
the time zone has daylight saving or not is not taken into consideration
when searching. If this is set to 1, then the `gmtOffset` is assumed to
be an offset with daylight saving in effect; if 0, then `gmtOffset` is
assumed to be an offset without daylight saving in effect. If `abbr`
doesn't exist then the time zone is searched solely by the `gmtOffset`
and `isdst`.

### 返回值

Returns time zone name on success 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 A <span class="function">timezone\_name\_from\_abbr</span>
example**

``` php
<?php
echo timezone_name_from_abbr("CET") . "\n";
echo timezone_name_from_abbr("", 3600, 0) . "\n";
?>
```

以上例程的输出类似于：

    Europe/Berlin
    Europe/Paris

### 参见

-   <span class="function">timezone\_abbreviations\_list</span>

timezone\_name\_get
===================

别名 <span class="methodname">DateTimeZone::getName</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTimeZone::getName</span>

timezone\_offset\_get
=====================

别名 <span class="methodname">DateTimeZone::getOffset</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTimeZone::getOffset</span>

timezone\_open
==============

别名 <span class="methodname">DateTimeZone::\_\_construct</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTimeZone::\_\_construct</span>

timezone\_transitions\_get
==========================

别名 <span class="methodname">DateTimeZone::getTransitions</span>

### 说明

此函数是该函数的别名： <span
class="methodname">DateTimeZone::getTransitions</span>

timezone\_version\_get
======================

Gets the version of the timezonedb

### 说明

<span class="type">string</span> <span
class="methodname">timezone\_version\_get</span> ( <span
class="methodparam">void</span> )

Returns the current version of the timezonedb.

### 返回值

Returns a <span class="type">string</span>.

### 范例

**示例 \#1 Getting the timezonedb version**

``` php
<?php
echo timezone_version_get();
?>
```

以上例程的输出类似于：

    2009.7

### 参见

-   <a href="/timezones.html" class="link">List of Supported Timezones</a>

**目录**

-   [checkdate](/ref/datetime.html#checkdate) — 验证一个格里高里日期
-   [date\_add](/ref/datetime.html#date_add) — 别名 DateTime::add
-   [date\_create\_from\_format](/ref/datetime.html#date_create_from_format)
    — 别名 DateTime::createFromFormat
-   [date\_create\_immutable\_from\_format](/ref/datetime.html#date_create_immutable_from_format)
    — 别名 DateTimeImmutable::createFromFormat
-   [date\_create\_immutable](/ref/datetime.html#date_create_immutable)
    — 别名 DateTimeImmutable::\_\_construct
-   [date\_create](/ref/datetime.html#date_create) — 别名
    DateTime::\_\_construct
-   [date\_date\_set](/ref/datetime.html#date_date_set) — 别名
    DateTime::setDate
-   [date\_default\_timezone\_get](/ref/datetime.html#date_default_timezone_get)
    — 取得一个脚本中所有日期时间函数所使用的默认时区
-   [date\_default\_timezone\_set](/ref/datetime.html#date_default_timezone_set)
    — 设定用于一个脚本中所有日期时间函数的默认时区
-   [date\_diff](/ref/datetime.html#date_diff) — 别名 DateTime::diff
-   [date\_format](/ref/datetime.html#date_format) — 别名
    DateTime::format
-   [date\_get\_last\_errors](/ref/datetime.html#date_get_last_errors) —
    别名 DateTime::getLastErrors
-   [date\_interval\_create\_from\_date\_string](/ref/datetime.html#date_interval_create_from_date_string)
    — 别名 DateInterval::createFromDateString
-   [date\_interval\_format](/ref/datetime.html#date_interval_format) —
    别名 DateInterval::format
-   [date\_isodate\_set](/ref/datetime.html#date_isodate_set) — 别名
    DateTime::setISODate
-   [date\_modify](/ref/datetime.html#date_modify) — 别名
    DateTime::modify
-   [date\_offset\_get](/ref/datetime.html#date_offset_get) — 别名
    DateTime::getOffset
-   [date\_parse\_from\_format](/ref/datetime.html#date_parse_from_format)
    — Get info about given date formatted according to the specified
    format
-   [date\_parse](/ref/datetime.html#date_parse) — Returns associative
    array with detailed info about given date
-   [date\_sub](/ref/datetime.html#date_sub) — 别名 DateTime::sub
-   [date\_sun\_info](/ref/datetime.html#date_sun_info) — Returns an
    array with information about sunset/sunrise and twilight begin/end
-   [date\_sunrise](/ref/datetime.html#date_sunrise) —
    返回给定的日期与地点的日出时间
-   [date\_sunset](/ref/datetime.html#date_sunset) —
    返回给定的日期与地点的日落时间
-   [date\_time\_set](/ref/datetime.html#date_time_set) — 别名
    DateTime::setTime
-   [date\_timestamp\_get](/ref/datetime.html#date_timestamp_get) — 别名
    DateTime::getTimestamp
-   [date\_timestamp\_set](/ref/datetime.html#date_timestamp_set) — 别名
    DateTime::setTimestamp
-   [date\_timezone\_get](/ref/datetime.html#date_timezone_get) — 别名
    DateTime::getTimezone
-   [date\_timezone\_set](/ref/datetime.html#date_timezone_set) — 别名
    DateTime::setTimezone
-   [date](/ref/datetime.html#date) — 格式化一个本地时间／日期
-   [getdate](/ref/datetime.html#getdate) — 取得日期／时间信息
-   [gettimeofday](/ref/datetime.html#gettimeofday) — 取得当前时间
-   [gmdate](/ref/datetime.html#gmdate) — 格式化一个 GMT/UTC 日期／时间
-   [gmmktime](/ref/datetime.html#gmmktime) — 取得 GMT 日期的 UNIX
    时间戳
-   [gmstrftime](/ref/datetime.html#gmstrftime) — 根据区域设置格式化
    GMT/UTC 时间／日期
-   [idate](/ref/datetime.html#idate) — 将本地时间日期格式化为整数
-   [localtime](/ref/datetime.html#localtime) — 取得本地时间
-   [microtime](/ref/datetime.html#microtime) — 返回当前 Unix
    时间戳和微秒数
-   [mktime](/ref/datetime.html#mktime) — 取得一个日期的 Unix 时间戳
-   [strftime](/ref/datetime.html#strftime) —
    根据区域设置格式化本地时间／日期
-   [strptime](/ref/datetime.html#strptime) — 解析由 strftime
    生成的日期／时间
-   [strtotime](/ref/datetime.html#strtotime) —
    将任何字符串的日期时间描述解析为 Unix 时间戳
-   [time](/ref/datetime.html#time) — 返回当前的 Unix 时间戳
-   [timezone\_abbreviations\_list](/ref/datetime.html#timezone_abbreviations_list)
    — 别名 DateTimeZone::listAbbreviations
-   [timezone\_identifiers\_list](/ref/datetime.html#timezone_identifiers_list)
    — 别名 DateTimeZone::listIdentifiers
-   [timezone\_location\_get](/ref/datetime.html#timezone_location_get)
    — 别名 DateTimeZone::getLocation
-   [timezone\_name\_from\_abbr](/ref/datetime.html#timezone_name_from_abbr)
    — Returns the timezone name from abbreviation
-   [timezone\_name\_get](/ref/datetime.html#timezone_name_get) — 别名
    DateTimeZone::getName
-   [timezone\_offset\_get](/ref/datetime.html#timezone_offset_get) —
    别名 DateTimeZone::getOffset
-   [timezone\_open](/ref/datetime.html#timezone_open) — 别名
    DateTimeZone::\_\_construct
-   [timezone\_transitions\_get](/ref/datetime.html#timezone_transitions_get)
    — 别名 DateTimeZone::getTransitions
-   [timezone\_version\_get](/ref/datetime.html#timezone_version_get) —
    Gets the version of the timezonedb
