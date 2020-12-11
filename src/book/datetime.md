日期和时间
==========

**目录**

-   [简介](/intro/datetime.html)
-   [安装／配置](/datetime/setup.html)
    -   [需求](/datetime/setup.html#需求)
    -   [安装](/datetime/setup.html#安装)
    -   [运行时配置](/datetime/setup.html#运行时配置)
    -   [资源类型](/datetime/setup.html#资源类型)
-   [预定义常量](/datetime/constants.html)
-   [范例](/datetime/examples.html)
    -   [Date/Time
        Arithmetic](/datetime/examples.html#Date/Time%20Arithmetic)
-   [DateTime](/class/datetime.html) — DateTime 类
    -   [DateTime::add](/class/datetime.html#DateTime::add) — 给一个
        DateTime 对象增加一定量的天，月，年，小时，分钟 以及秒。
    -   [DateTime::\_\_construct](/class/datetime.html#DateTime::__construct)
        — 返回一个新的 DateTime 对象
    -   [DateTime::createFromFormat](/class/datetime.html#DateTime::createFromFormat)
        — 根据给定的格式解析日期时间字符串
    -   [DateTime::createFromImmutable](/class/datetime.html#DateTime::createFromImmutable)
        — Returns new DateTime object encapsulating the given
        DateTimeImmutable object
    -   [DateTime::createFromInterface](/class/datetime.html#DateTime::createFromInterface)
        — Returns new DateTime object encapsulating the given
        DateTimeInterface object
    -   [DateTime::getLastErrors](/class/datetime.html#DateTime::getLastErrors)
        — 获取警告和错误信息
    -   [DateTime::modify](/class/datetime.html#DateTime::modify) —
        修改日期时间对象的值
    -   [DateTime::\_\_set\_state](/class/datetime.html#DateTime::__set_state)
        — \_\_set\_state 魔术方法处理函数
    -   [DateTime::setDate](/class/datetime.html#DateTime::setDate) —
        设置 DateTime 对象的日期
    -   [DateTime::setISODate](/class/datetime.html#DateTime::setISODate)
        — 设置 ISO 日期
    -   [DateTime::setTime](/class/datetime.html#DateTime::setTime) —
        设置 DateTime 对象的时间
    -   [DateTime::setTimestamp](/class/datetime.html#DateTime::setTimestamp)
        — 以 Unix 时间戳的方式设置 DateTime 对象
    -   [DateTime::setTimezone](/class/datetime.html#DateTime::setTimezone)
        — 设置 DateTime 对象的时区
    -   [DateTime::sub](/class/datetime.html#DateTime::sub) — 对一个
        DateTime 对象减去一定量的 日、月、年、小时、分钟和秒。
-   [DateTimeImmutable](/class/datetimeimmutable.html) — The
    DateTimeImmutable class
    -   [DateTimeImmutable::add](/class/datetimeimmutable.html#DateTimeImmutable::add)
        — Adds an amount of days, months, years, hours, minutes and
        seconds
    -   [DateTimeImmutable::\_\_construct](/class/datetimeimmutable.html#DateTimeImmutable::__construct)
        — Returns new DateTimeImmutable object
    -   [DateTimeImmutable::createFromFormat](/class/datetimeimmutable.html#DateTimeImmutable::createFromFormat)
        — Parses a time string according to a specified format
    -   [DateTimeImmutable::createFromInterface](/class/datetimeimmutable.html#DateTimeImmutable::createFromInterface)
        — Returns new DateTimeImmutable object encapsulating the given
        DateTimeInterface object
    -   [DateTimeImmutable::createFromMutable](/class/datetimeimmutable.html#DateTimeImmutable::createFromMutable)
        — Returns new DateTimeImmutable object encapsulating the given
        DateTime object
    -   [DateTimeImmutable::getLastErrors](/class/datetimeimmutable.html#DateTimeImmutable::getLastErrors)
        — Returns the warnings and errors
    -   [DateTimeImmutable::modify](/class/datetimeimmutable.html#DateTimeImmutable::modify)
        — Creates a new object with modified timestamp
    -   [DateTimeImmutable::\_\_set\_state](/class/datetimeimmutable.html#DateTimeImmutable::__set_state)
        — The \_\_set\_state handler
    -   [DateTimeImmutable::setDate](/class/datetimeimmutable.html#DateTimeImmutable::setDate)
        — Sets the date
    -   [DateTimeImmutable::setISODate](/class/datetimeimmutable.html#DateTimeImmutable::setISODate)
        — Sets the ISO date
    -   [DateTimeImmutable::setTime](/class/datetimeimmutable.html#DateTimeImmutable::setTime)
        — Sets the time
    -   [DateTimeImmutable::setTimestamp](/class/datetimeimmutable.html#DateTimeImmutable::setTimestamp)
        — Sets the date and time based on a Unix timestamp
    -   [DateTimeImmutable::setTimezone](/class/datetimeimmutable.html#DateTimeImmutable::setTimezone)
        — Sets the time zone
    -   [DateTimeImmutable::sub](/class/datetimeimmutable.html#DateTimeImmutable::sub)
        — Subtracts an amount of days, months, years, hours, minutes and
        seconds
-   [DateTimeInterface](/class/datetimeinterface.html) — The
    DateTimeInterface interface
    -   [DateTime::diff](/class/datetimeinterface.html#DateTime::diff) —
        Returns the difference between two DateTime objects
    -   [DateTime::format](/class/datetimeinterface.html#DateTime::format)
        — Returns date formatted according to given format
    -   [DateTime::getOffset](/class/datetimeinterface.html#DateTime::getOffset)
        — Returns the timezone offset
    -   [DateTime::getTimestamp](/class/datetimeinterface.html#DateTime::getTimestamp)
        — Gets the Unix timestamp
    -   [DateTime::getTimezone](/class/datetimeinterface.html#DateTime::getTimezone)
        — Return time zone relative to given DateTime
    -   [DateTime::\_\_wakeup](/class/datetimeinterface.html#DateTime::__wakeup)
        — The \_\_wakeup handler
-   [DateTimeZone](/class/datetimezone.html) — The DateTimeZone class
    -   [DateTimeZone::\_\_construct](/class/datetimezone.html#DateTimeZone::__construct)
        — 创建新的DateTimeZone对象
    -   [DateTimeZone::getLocation](/class/datetimezone.html#DateTimeZone::getLocation)
        — 返回与时区相关的定位信息。
    -   [DateTimeZone::getName](/class/datetimezone.html#DateTimeZone::getName)
        — 返回时区名称。
    -   [DateTimeZone::getOffset](/class/datetimezone.html#DateTimeZone::getOffset)
        — 返回相对于 GMT 的时差。
    -   [DateTimeZone::getTransitions](/class/datetimezone.html#DateTimeZone::getTransitions)
        — Returns all transitions for the timezone
    -   [DateTimeZone::listAbbreviations](/class/datetimezone.html#DateTimeZone::listAbbreviations)
        — 返回一个包含 dst (夏令时)，时差和时区信息的关联数组。
    -   [DateTimeZone::listIdentifiers](/class/datetimezone.html#DateTimeZone::listIdentifiers)
        — 返回一个包含了所有时区标示符的索引数组。
-   [DateInterval](/class/dateinterval.html) — DateInterval 类
    -   [DateInterval::\_\_construct](/class/dateinterval.html#DateInterval::__construct)
        — Creates a new DateInterval object
    -   [DateInterval::createFromDateString](/class/dateinterval.html#DateInterval::createFromDateString)
        — Sets up a DateInterval from the relative parts of the string
    -   [DateInterval::format](/class/dateinterval.html#DateInterval::format)
        — Formats the interval
-   [DatePeriod](/class/dateperiod.html) — DatePeriod 类
    -   [DatePeriod::\_\_construct](/class/dateperiod.html#DatePeriod::__construct)
        — Creates a new DatePeriod object
    -   [DatePeriod::getDateInterval](/class/dateperiod.html#DatePeriod::getDateInterval)
        — Gets the interval
    -   [DatePeriod::getEndDate](/class/dateperiod.html#DatePeriod::getEndDate)
        — Gets the end date
    -   [DatePeriod::getRecurrences](/class/dateperiod.html#DatePeriod::getRecurrences)
        — Gets the number of recurrences
    -   [DatePeriod::getStartDate](/class/dateperiod.html#DatePeriod::getStartDate)
        — Gets the start date
-   [Date/Time 函数](/ref/datetime.html)
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
    -   [date\_get\_last\_errors](/ref/datetime.html#date_get_last_errors)
        — 别名 DateTime::getLastErrors
    -   [date\_interval\_create\_from\_date\_string](/ref/datetime.html#date_interval_create_from_date_string)
        — 别名 DateInterval::createFromDateString
    -   [date\_interval\_format](/ref/datetime.html#date_interval_format)
        — 别名 DateInterval::format
    -   [date\_isodate\_set](/ref/datetime.html#date_isodate_set) — 别名
        DateTime::setISODate
    -   [date\_modify](/ref/datetime.html#date_modify) — 别名
        DateTime::modify
    -   [date\_offset\_get](/ref/datetime.html#date_offset_get) — 别名
        DateTime::getOffset
    -   [date\_parse\_from\_format](/ref/datetime.html#date_parse_from_format)
        — Get info about given date formatted according to the specified
        format
    -   [date\_parse](/ref/datetime.html#date_parse) — Returns
        associative array with detailed info about given date/time
    -   [date\_sub](/ref/datetime.html#date_sub) — 别名 DateTime::sub
    -   [date\_sun\_info](/ref/datetime.html#date_sun_info) — Returns an
        array with information about sunset/sunrise and twilight
        begin/end
    -   [date\_sunrise](/ref/datetime.html#date_sunrise) —
        返回给定的日期与地点的日出时间
    -   [date\_sunset](/ref/datetime.html#date_sunset) —
        返回给定的日期与地点的日落时间
    -   [date\_time\_set](/ref/datetime.html#date_time_set) — 别名
        DateTime::setTime
    -   [date\_timestamp\_get](/ref/datetime.html#date_timestamp_get) —
        别名 DateTime::getTimestamp
    -   [date\_timestamp\_set](/ref/datetime.html#date_timestamp_set) —
        别名 DateTime::setTimestamp
    -   [date\_timezone\_get](/ref/datetime.html#date_timezone_get) —
        别名 DateTime::getTimezone
    -   [date\_timezone\_set](/ref/datetime.html#date_timezone_set) —
        别名 DateTime::setTimezone
    -   [date](/ref/datetime.html#date) — 格式化一个本地时间／日期
    -   [getdate](/ref/datetime.html#getdate) — 取得日期／时间信息
    -   [gettimeofday](/ref/datetime.html#gettimeofday) — 取得当前时间
    -   [gmdate](/ref/datetime.html#gmdate) — 格式化一个 GMT/UTC
        日期／时间
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
    -   [timezone\_name\_get](/ref/datetime.html#timezone_name_get) —
        别名 DateTimeZone::getName
    -   [timezone\_offset\_get](/ref/datetime.html#timezone_offset_get)
        — 别名 DateTimeZone::getOffset
    -   [timezone\_open](/ref/datetime.html#timezone_open) — 别名
        DateTimeZone::\_\_construct
    -   [timezone\_transitions\_get](/ref/datetime.html#timezone_transitions_get)
        — 别名 DateTimeZone::getTransitions
    -   [timezone\_version\_get](/ref/datetime.html#timezone_version_get)
        — Gets the version of the timezonedb
-   [Supported Date and Time Formats](/datetime/formats.html)
    -   [Time Formats](/datetime/formats.html#Time%20Formats)
    -   [Date Formats](/datetime/formats.html#Date%20Formats)
    -   [Compound Formats](/datetime/formats.html#Compound%20Formats)
    -   [Relative Formats](/datetime/formats.html#Relative%20Formats)
-   [所支持的时区列表](/timezones.html)
    -   [非洲](/timezones.html#非洲)
    -   [美洲](/timezones.html#美洲)
    -   [南极洲](/timezones.html#南极洲)
    -   [北极](/timezones.html#北极)
    -   [亚洲](/timezones.html#亚洲)
    -   [大西洋](/timezones.html#大西洋)
    -   [澳洲](/timezones.html#澳洲)
    -   [欧洲](/timezones.html#欧洲)
    -   [印度](/timezones.html#印度)
    -   [太平洋地区](/timezones.html#太平洋地区)
    -   [其他](/timezones.html#其他)

简介
----

日期和时间。

类摘要
------

**DateTime**

<span class="ooclass"> class **DateTime** </span> <span
class="oointerface">implements <span
class="interfacename">DateTimeInterface</span> </span> {

/\* 继承的常量 \*/

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::ATOM` <span class="initializer"> =
"Y-m-d\\TH:i:sP"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::COOKIE` <span class="initializer"> = "l, d-M-Y H:i:s
T"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::ISO8601` <span class="initializer"> =
"Y-m-d\\TH:i:sO"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC822` <span class="initializer"> = "D, d M y H:i:s
O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC850` <span class="initializer"> = "l, d-M-y H:i:s
T"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC1036` <span class="initializer"> = "D, d M y
H:i:s O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC1123` <span class="initializer"> = "D, d M Y
H:i:s O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC7231` <span class="initializer"> = "D, d M Y
H:i:s \\G\\M\\T"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC2822` <span class="initializer"> = "D, d M Y
H:i:s O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC3339` <span class="initializer"> =
"Y-m-d\\TH:i:sP"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC3339_EXTENDED` <span class="initializer"> =
"Y-m-d\\TH:i:s.vP"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RSS` <span class="initializer"> = "D, d M Y H:i:s
O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::W3C` <span class="initializer"> =
"Y-m-d\\TH:i:sP"</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$time`<span
class="initializer"> = "now"</span></span> \[, <span
class="methodparam"><span class="type">DateTimeZone</span>
`$timezone`<span class="initializer"> = **`null`**</span></span> \]\] )

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">add</span> ( <span class="methodparam"><span
class="type">DateInterval</span> `$interval`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">DateTime</span> <span
class="methodname">createFromFormat</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> ,
<span class="methodparam"><span class="type">string</span>
`$time`</span> \[, <span class="methodparam"><span
class="type">DateTimeZone</span> `$timezone`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">DateTime</span> <span
class="methodname">createFromImmutable</span> ( <span
class="methodparam"><span class="type">DateTimeImmutable</span>
`$object`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">DateTime</span> <span
class="methodname">createFromInterface</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$object`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getLastErrors</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">modify</span> ( <span class="methodparam"><span
class="type">string</span> `$modifier`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">DateTime</span> <span
class="methodname">\_\_set\_state</span> ( <span
class="methodparam"><span class="type">array</span> `$array`</span> )

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">setDate</span> ( <span
class="methodparam"><span class="type">int</span> `$year`</span> , <span
class="methodparam"><span class="type">int</span> `$month`</span> ,
<span class="methodparam"><span class="type">int</span> `$day`</span> )

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">setISODate</span> ( <span
class="methodparam"><span class="type">int</span> `$year`</span> , <span
class="methodparam"><span class="type">int</span> `$week`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$dayOfWeek`<span class="initializer"> = 1</span></span> \] )

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">setTime</span> ( <span
class="methodparam"><span class="type">int</span> `$hour`</span> , <span
class="methodparam"><span class="type">int</span> `$minute`</span> \[,
<span class="methodparam"><span class="type">int</span> `$second`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$microsecond`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">setTimestamp</span> ( <span
class="methodparam"><span class="type">int</span>
`$unixtimestamp`</span> )

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">setTimezone</span> ( <span
class="methodparam"><span class="type">DateTimeZone</span>
`$timezone`</span> )

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">sub</span> ( <span class="methodparam"><span
class="type">DateInterval</span> `$interval`</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">DateInterval</span><span class="type">false</span></span>
<span class="methodname">diff</span> ( <span class="methodparam"><span
class="type">DateTimeInterface</span> `$targetObject`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$absolute`<span
class="initializer"> = **`false`**</span></span> \] )

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">false</span></span> <span
class="methodname">format</span> ( <span class="methodparam"><span
class="type">string</span> `$format`</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">int</span><span class="type">false</span></span> <span
class="methodname">getOffset</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getTimestamp</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">DateTimeZone</span><span class="type">false</span></span>
<span class="methodname">getTimezone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_wakeup</span> ( <span
class="methodparam">void</span> )

}

更新日志
--------

| 版本   | 说明                                                                                                                                                                                                                              |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.2.0  | <span class="classname">DateTime</span> 的类常量现在定义在 <span class="classname">DateTimeInterface</span> 上。                                                                                                                  |
| 7.0.0  | 新增常量：<a href="/class/datetimeinterface.html#" class="link">DATE_RFC3339_EXTENDED</a> 和 <a href="/class/datetimeinterface.html#" class="link">DateTime::RFC3339_EXTENDED</a>。                                               |
| 5.5.0  | 实现 <span class="classname">DateTimeInterface</span> 接口。                                                                                                                                                                      |
| 5.4.24 | COOKIE 格式从 2 位数字表示年份（RFC 850） 修改为 4 位数字表示年份（RFC 1036）。                                                                                                                                                   |
| 5.2.2  | DateTime 对象进行比较操作（<a href="/language/operators/comparison.html" class="link">comparison operators</a>）的时候 可以正常工作了。 在之前的版本中，当使用 *==* 进行相等比较的时候， 所有的 DateTime 对象都会被视为是相等的。 |

DateTime::add
=============

date\_add
=========

给一个 DateTime 对象增加一定量的天，月，年，小时，分钟 以及秒。

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">DateTime::add</span> ( <span
class="methodparam"><span class="type">DateInterval</span>
`$interval`</span> )

过程化风格

<span class="type">DateTime</span> <span
class="methodname">date\_add</span> ( <span class="methodparam"><span
class="type">DateTime</span> `$object`</span> , <span
class="methodparam"><span class="type">DateInterval</span>
`$interval`</span> )

将给定的 <span class="classname">DateInterval</span> 对象 加到 <span
class="classname">DateTime</span> 对象上。

### 参数

`object`  
仅过程化风格：由 <span class="function">date\_create</span> 返回的 <span
class="classname">DateTime</span> 类型的对象。此函数会修改这个对象。

`interval`  
<span class="classname">DateInterval</span> 对象。

### 返回值

返回被修改的 DateTime 对象， 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">DateTime::add</span> 例程**

面向对象风格

``` php
<?php
$date = new DateTime('2000-01-01');
$date->add(new DateInterval('P10D'));
echo $date->format('Y-m-d') . "\n";
?>
```

过程化风格

``` php
<?php
$date = date_create('2000-01-01');
date_add($date, date_interval_create_from_date_string('10 days'));
echo date_format($date, 'Y-m-d');
?>
```

以上例程会输出：

    2000-01-11

**示例 \#2 Further <span class="function">DateTime::add</span> 例程**

``` php
<?php
$date = new DateTime('2000-01-01');
$date->add(new DateInterval('PT10H30S'));
echo $date->format('Y-m-d H:i:s') . "\n";

$date = new DateTime('2000-01-01');
$date->add(new DateInterval('P7Y5M4DT4H3M2S'));
echo $date->format('Y-m-d H:i:s') . "\n";
?>
```

以上例程会输出：

    2000-01-01 10:00:30
    2007-06-05 04:03:02

**示例 \#3 当在 DateTime 上加月的时候要注意**

``` php
<?php
$date = new DateTime('2000-12-31');
$interval = new DateInterval('P1M');

$date->add($interval);
echo $date->format('Y-m-d') . "\n";

$date->add($interval);
echo $date->format('Y-m-d') . "\n";
?>
```

以上例程会输出：

    2001-01-31
    2001-03-03

### 注释

在 PHP 5.2 的版本中， 也可以使用 <span
class="function">DateTime::modify</span> 方法来替代本方法。

### 参见

-   <span class="function">DateTime::sub</span>
-   <span class="function">DateTime::diff</span>
-   <span class="function">DateTime::modify</span>

DateTime::\_\_construct
=======================

date\_create
============

返回一个新的 DateTime 对象

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="methodname">DateTime::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$time`<span
class="initializer"> = "now"</span></span> \[, <span
class="methodparam"><span class="type">DateTimeZone</span>
`$timezone`<span class="initializer"> = **`null`**</span></span> \]\] )

过程化风格

<span class="type">DateTime</span> <span
class="methodname">date\_create</span> (\[ <span
class="methodparam"><span class="type">string</span> `$time`<span
class="initializer"> = "now"</span></span> \[, <span
class="methodparam"><span class="type">DateTimeZone</span>
`$timezone`<span class="initializer"> = **`null`**</span></span> \]\] )

返回一个新的 DateTime 对象。

### 参数

`time`  
日期/时间字符串。正确格式的说明详见
<a href="/datetime/formats.html" class="link">日期与时间格式</a>。

如果这个参数为字符串 *"now"* 表示获取当前时间。 如果同时指定了
`$timezone` 参数，那么获取指定时区的当前时间。

`timezone`  
<span class="classname">DateTimeZone</span> 对象， 表示要获取哪个时区的
`$time`。

如果省略了 `$timezone` 参数， 那么会使用当前时区。

> **Note**:
>
> 当 `$time` 参数是 UNIX 时间戳 （例如 *@946684800*），
> 或者已经包含时区信息 （例如 *2010-01-28T15:00:00+02:00*）的时候，
> `$timezone` 参数 和当前时区都将被忽略。

### 返回值

返回一个新的 DateTime 对象实例，或者在发生错误的时候返回
过程化风格在失败时返回 **`false`**。。

### 错误／异常

如果发生错误，会抛出 <span class="classname">Exception</span>。

### 更新日志

| 版本  | 说明                                                                                                                                           |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.1   | 微秒部分不再是 '00000' 了，而是真实的微秒数据。                                                                                                |
| 5.3.0 | 如果 `time` 参数不是一个有效的 <a href="/datetime/formats.html" class="link">日期/时间格式</a>， 会抛出异常。 在之前的版本中是会发出一个错误。 |

### 范例

**示例 \#1 <span class="function">DateTime::\_\_construct</span> 例程**

面向对象风格

``` php
<?php
try {
    $date = new DateTime('2000-01-01');
} catch (Exception $e) {
    echo $e->getMessage();
    exit(1);
}

echo $date->format('Y-m-d');
?>
```

过程化风格

``` php
<?php
$date = date_create('2000-01-01');
if (!$date) {
    $e = date_get_last_errors();
    foreach ($e['errors'] as $error) {
        echo "$error\n";
    }
    exit(1);
}

echo date_format($date, 'Y-m-d');
?>
```

以上例程会输出：

    2000-01-01

**示例 \#2 <span class="function">DateTime::\_\_construct</span>
的复杂用法**

``` php
<?php
// 指定时间，但是使用电脑的时区
$date = new DateTime('2000-01-01');
echo $date->format('Y-m-d H:i:sP') . "\n";

// 指定时间和时区
$date = new DateTime('2000-01-01', new DateTimeZone('Pacific/Nauru'));
echo $date->format('Y-m-d H:i:sP') . "\n";

// 使用当前时间以及电脑的时区
$date = new DateTime();
echo $date->format('Y-m-d H:i:sP') . "\n";

// 使用当前时间和指定的时区
$date = new DateTime(null, new DateTimeZone('Pacific/Nauru'));
echo $date->format('Y-m-d H:i:sP') . "\n";

// 使用 UNIX 时间戳作为时间，请注意这里的生成的 DateTime 对象对应的是 UTC 时区
$date = new DateTime('@946684800');
echo $date->format('Y-m-d H:i:sP') . "\n";

// 指定一个无效的时间，会自动对应到有效的时间
$date = new DateTime('2000-02-30');
echo $date->format('Y-m-d H:i:sP') . "\n";
?>
```

以上例程的输出类似于：

    2000-01-01 00:00:00-05:00
    2000-01-01 00:00:00+12:00
    2010-04-24 10:24:16-04:00
    2010-04-25 02:24:16+12:00
    2000-01-01 00:00:00+00:00
    2000-03-01 00:00:00-05:00

### 参见

-   <span class="function">DateTime::createFromFormat</span>
-   <span class="function">DateTimeZone::\_\_construct</span>
-   <a href="/datetime/formats.html" class="link">日期时间格式</a>
-   <a href="/datetime/setup.html#" class="link">date.timezone</a> ini
    设置
-   <span class="function">date\_default\_timezone\_set</span>
-   <span class="function">DateTime::getLastErrors</span>
-   <span class="function">checkdate</span>

DateTime::createFromFormat
==========================

date\_create\_from\_format
==========================

根据给定的格式解析日期时间字符串

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">DateTime</span> <span
class="methodname">DateTime::createFromFormat</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> ,
<span class="methodparam"><span class="type">string</span>
`$time`</span> \[, <span class="methodparam"><span
class="type">DateTimeZone</span> `$timezone`</span> \] )

过程化风格

<span class="type">DateTime</span> <span
class="methodname">date\_create\_from\_format</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> ,
<span class="methodparam"><span class="type">string</span>
`$time`</span> \[, <span class="methodparam"><span
class="type">DateTimeZone</span> `$timezone`</span> \] )

将 `time` 参数给定的日期时间字符串， 根据 `format` 参数给定的格式
解析为一个新的 DateTime 对象。

### 参数

`format`  
在解析日期时间字符串的时候使用的格式 <span class="type">string</span>。
参加下列的格式清单。 大部分格式和 <span class="function">date</span>
函数中的格式是一致的。

|              `format` 中的字符             | 解释                                                                                                                                      | 示例                                                                                                                                     |
|:------------------------------------------:|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
|                    *日*                    | ---                                                                                                                                       | ---                                                                                                                                      |
|                 *d* 和 *j*                 | 一个月中的第几天，2 位数字表示，有前导 0 或者无前导 0                                                                                     | *01* 到 *31* 或者 *1* 到 *31*                                                                                                            |
|                 *D* 和 *l*                 | 星期几的文字表示                                                                                                                          | *Mon* 到 *Sun* 或者 *Sunday* 到 *Saturday*                                                                                               |
|                     *S*                    | 2 个字母表示的一个月中的第几天（序数词）， 在进行解析的时候会被忽略                                                                       | *st*，*nd*，*rd* 或者 *th*。                                                                                                             |
|                     *z*                    | 一年中的第几天，从 0 开始                                                                                                                 | *0* 到 *365*                                                                                                                             |
|                    *月*                    | ---                                                                                                                                       | ---                                                                                                                                      |
|                 *F* 和 *M*                 | 文本表示的月份，例如 January 或者 Sept                                                                                                    | *January* 到 *December* 或者 *Jan* 到 *Dec*                                                                                              |
|                 *m* 和 *n*                 | 数值表示的月份，有前导 0 或者无前导 0                                                                                                     | *01* 到 *12* or *1* 到 *12*                                                                                                              |
|                    *年*                    | ---                                                                                                                                       | ---                                                                                                                                      |
|                     *Y*                    | 4 位数字表示的年                                                                                                                          | 例如：*1999* 或 *2003*                                                                                                                   |
|                     *y*                    | 2 位数字表示的年， 可用的范围是 1970 至 2069（不含）                                                                                      | 例如： *99* 或 *03* （表示 *1999* 和 *2003*）                                                                                            |
|                   *时间*                   | ---                                                                                                                                       | ---                                                                                                                                      |
|                 *a* 和 *A*                 | 上午、下午                                                                                                                                | *am* 或 *pm*                                                                                                                             |
|                 *g* and *h*                | 12 小时制的小时，有前导 0 或者无前导 0                                                                                                    | *1* 到 *12* 或者 *01* 到 *12*                                                                                                            |
|                 *G* 和 *H*                 | 24 小时制的小时，有前导 0 或者无前导 0                                                                                                    | *0* 到 *23* 或 *00* 到 *23*                                                                                                              |
|                     *i*                    | 分钟，有前导 0                                                                                                                            | *00* 到 *59*                                                                                                                             |
|                     *s*                    | 秒，有前导 0                                                                                                                              | *00* 到 *59*                                                                                                                             |
|                     *u*                    | 微秒，最多到 6 位数字                                                                                                                     | 示例：*45*，*654321*                                                                                                                     |
|                   *时区*                   | ---                                                                                                                                       | ---                                                                                                                                      |
|            *e*，*O*, *P* 和 *T*            | 时区名称，或者是以 UTC 时区为基准的小时偏移量， 或者是以 UTC 为基准的小时和分钟的偏移量， 小时和分钟之间用冒号（:）分隔。                 | 示例：*UTC*，*GMT*， *Atlantic/Azores* 或 *+0200* 或 *+02:00* 或 *EST*，*MDT*                                                            |
|             *完整的日期和时间*             | ---                                                                                                                                       | ---                                                                                                                                      |
|                     *U*                    | 从 Unix Epoch (January 1 1970 00:00:00 GMT) 开始计算的时间，以秒为单位                                                                    | 示例：*1292177455*                                                                                                                       |
|            *空白字符和分隔字符*            | ---                                                                                                                                       | ---                                                                                                                                      |
|                   （空格）                 | 一个空格字符或者一个 tab 字符                                                                                                             | 示例：                                                                                                                                   |
|                    *\#*                    | 可以是一下分隔符号中的任意一个： *;*， *:*，*/*，*.*， *,*，*-*，*(* 或 *)*                                                               | 示例：*/*                                                                                                                                |
| *;*， *:*，*/*，*.*， *,*，*-*，*(* 或 *)* | 特殊字符                                                                                                                                  | 示例：*-*                                                                                                                                |
|                     *?*                    | 随机字节                                                                                                                                  | 示例：*^* （需要注意的是， 对于 UTF-8 字符，可能会需要多个 *?*。 这种情况下，请使用 *\**）                                               |
|                    *\**                    | 随机字节，直到遇到下一个有效的分隔符号或者数值                                                                                            | 示例：使用 *Y-\*-d* 格式用来解析 *2009-aWord-08* 字符串的时候， *\** 会匹配 *aWord*                                                      |
|                     *!*                    | 将所有的字段（年、月、日、时、分、秒、微秒以及时区）重置到 Unix Epoch 时间。                                                              | 如果不使用 *!,* 格式， 那么所有的字段会被设置为系统当前的日期和时间。                                                                    |
|                    *\|*                    | 将尚未被解析的字段，也即格式字符串中未明确指定的字段 （年、月、日、时、分、秒、微秒以及时区） 重置到 Unix Epoch 时间。                    | *Y-m-d\|* 会解析日期时间字符串中的年、月和日， 但是对于时、分、秒字段会设置为 0.                                                         |
|                     *+*                    | 在格式字符串中使用这个格式表示字符， 并且所提供的日期时间字符串中包含除了格式字符之外的其他数据的话，不会发出一个错误，而是发出一个警告。 | 使用 <span class="methodname">DateTime::getLastErrors</span> 方法 来检测所给定的日期时间字符串中是否包含格式字符串指定的内容之外的数据。 |

如果在格式字符串中包含不可识别的字符，
那么会导致解析失败，并且在返回的结构中附加一个错误信息。 可以通过 <span
class="methodname">DateTime::getLastErrors</span>
来探查解析是否存在错误。

如果需要在格式字符串 `format` 参数中使用
上述表示格式的字符作为一个普通字符，请对其使用反斜线（*\\*）进行转义。

如果格式字符串参数 `format` 中不包含 *!* 字符， 那么没有在 `format`
参数中指明的字段， 在解析结果中将会被设置为系统当前时间对应的字段值。

如果格式字符串参数 `format` 包含了 *!* 字符， 那么没有在 `format`
参数中指明的字段， 以及在 *!* 左侧对应的字段， 在解析结果中将会被设置为
Unix epoch 时间对应的字段。

The Unix epoch 为 1970-01-01 00:00:00 UTC。

`time`  
用来表示日期时间的字符串。

`timezone`  
<span class="classname">DateTimeZone</span> 对象，
表示在解析日期时间字符串的时候需要使用的时区。

如果忽略 `timezone` 参数， 并且表示日期时间的字符串 `time`
中也不包含时区信息， 那么将会使用系统当前时区作为解析结果对象的时区。

> **Note**:
>
> 如果 `time` 参数 是 UNIX 时间戳格式（例如：*946684800*），
> 或者其中已经包含了时区信息（例如：*2010-01-28T15:00:00+02:00*）， 那么
> `timezone` 以及系统当前时区 都将会被忽略。

### 返回值

返回一个 DateTime 对象。 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                              |
|-------|---------------------------------------------------|
| 5.3.9 | 新增 `format` 格式字符串中对于 + 格式字符的支持。 |

### 范例

**示例 \#1 <span class="function">DateTime::createFromFormat</span>
例程**

面向对象风格

``` php
<?php
$date = DateTime::createFromFormat('j-M-Y', '15-Feb-2009');
echo $date->format('Y-m-d');
?>
```

过程化风格

``` php
<?php
$date = date_create_from_format('j-M-Y', '15-Feb-2009');
echo date_format($date, 'Y-m-d');
?>
```

以上例程会输出：

    2009-02-15

**示例 \#2 <span class="function">DateTime::createFromFormat</span>
的复杂用法**

``` php
<?php
echo 'Current time: ' . date('Y-m-d H:i:s') . "\n";

$format = 'Y-m-d';
$date = DateTime::createFromFormat($format, '2009-02-15');
echo "Format: $format; " . $date->format('Y-m-d H:i:s') . "\n";

$format = 'Y-m-d H:i:s';
$date = DateTime::createFromFormat($format, '2009-02-15 15:16:17');
echo "Format: $format; " . $date->format('Y-m-d H:i:s') . "\n";

$format = 'Y-m-!d H:i:s';
$date = DateTime::createFromFormat($format, '2009-02-15 15:16:17');
echo "Format: $format; " . $date->format('Y-m-d H:i:s') . "\n";

$format = '!d';
$date = DateTime::createFromFormat($format, '15');
echo "Format: $format; " . $date->format('Y-m-d H:i:s') . "\n";
?>
```

以上例程的输出类似于：

    Current time: 2010-04-23 10:29:35
    Format: Y-m-d; 2009-02-15 10:29:35
    Format: Y-m-d H:i:s; 2009-02-15 15:16:17
    Format: Y-m-!d H:i:s; 1970-01-15 15:16:17
    Format: !d; 1970-01-15 00:00:00

**示例 \#3 格式化字符串中包含了需要进行转义的字符**

``` php
<?php
echo DateTime::createFromFormat('H\h i\m s\s','23h 15m 03s')->format('H:i:s');
?>
```

以上例程的输出类似于：

    23:15:03

### 参见

-   <span class="function">DateTime::\_\_construct</span>
-   <span class="function">DateTime::getLastErrors</span>
-   <span class="function">checkdate</span>
-   <span class="function">strptime</span>

DateTime::createFromImmutable
=============================

Returns new DateTime object encapsulating the given DateTimeImmutable
object

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">DateTime</span> <span
class="methodname">DateTime::createFromImmutable</span> ( <span
class="methodparam"><span class="type">DateTimeImmutable</span>
`$object`</span> )

### 参数

`object`  
The immutable <span class="classname">DateTimeImmutable</span> object
that needs to be converted to a mutable version. This object is not
modified, but instead a new <span class="classname">DateTime</span>
object is created containing the same date, time, and timezone
information.

### 范例

**示例 \#1 Creating a mutable date time object**

``` php
<?php
$date = new DateTimeImmutable("2014-06-20 11:45 Europe/London");

$mutable = DateTime::createFromImmutable( $date );
?>
```

### 返回值

Returns a new <span class="classname">DateTime</span> instance.

DateTime::createFromInterface
=============================

Returns new DateTime object encapsulating the given DateTimeInterface
object

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">DateTime</span> <span
class="methodname">DateTime::createFromInterface</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$object`</span> )

### 参数

`object`  
The <span class="classname">DateTimeInterface</span> object that needs
to be converted to a mutable version. This object is not modified, but
instead a new <span class="classname">DateTime</span> object is created
containing the same date, time, and timezone information.

### 返回值

Returns a new <span class="classname">DateTime</span> instance.

### 范例

**示例 \#1 Creating a mutable date time object**

``` php
<?php
$date = new DateTimeImmutable("2014-06-20 11:45 Europe/London");

$mutable = DateTime::createFromInterface($date);

$date = new DateTime("2014-06-20 11:45 Europe/London");
$also_mutable = DateTime::createFromInterface($date);
?>
```

DateTime::getLastErrors
=======================

date\_get\_last\_errors
=======================

获取警告和错误信息

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">DateTime::getLastErrors</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">array</span> <span
class="methodname">date\_get\_last\_errors</span> ( <span
class="methodparam">void</span> )

返回在解析日期时间字符串的过程中发生的警告和错误信息。

### 参数

此函数没有参数。

### 返回值

返回一个数组，其中包含在解析日期时间字符串的过程中发生的警告和错误信息。

### 范例

**示例 \#1 <span class="function">DateTime::getLastErrors</span> 例程**

面向对象风格

``` php
<?php
try {
    $date = new DateTime('asdfasdf');
} catch (Exception $e) {
    // 仅出于演示的目的...
    print_r(DateTime::getLastErrors());

    // 实际的代码中你应该这样使用返回对象
    // echo $e->getMessage();
}
?>
```

过程化风格

``` php
<?php
$date = date_create('asdfasdf');
print_r(date_get_last_errors());
?>
```

以上例程会输出：

    Array
    (
       [warning_count] => 1
       [warnings] => Array
           (
               [6] => Double timezone specification
           )

       [error_count] => 1
       [errors] => Array
           (
               [0] => The timezone could not be found in the database
           )

    )

返回数组中的索引 6 和 0
表示在解析过程中，所提供的日期时间字符串中无法正确解析的字符位置。

DateTime::modify
================

date\_modify
============

修改日期时间对象的值

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">DateTime::modify</span> ( <span
class="methodparam"><span class="type">string</span> `$modifier`</span>
)

过程化风格

<span class="type">DateTime</span> <span
class="methodname">date\_modify</span> ( <span class="methodparam"><span
class="type">DateTime</span> `$object`</span> , <span
class="methodparam"><span class="type">string</span> `$modifier`</span>
)

修改一个日期时间对象的值。 支持 <span
class="function">DateTimeImmutable::\_\_construct</span>
函数所允许的字符串。

### 参数

`object`  
仅过程化风格：由 <span class="function">date\_create</span> 返回的 <span
class="classname">DateTime</span> 类型的对象。此函数会修改这个对象。

`modifier`  
日期/时间字符串。正确格式的说明详见
<a href="/datetime/formats.html" class="link">日期与时间格式</a>。

### 返回值

返回被修改的 DateTime 对象， 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">DateTime::modify</span> 例程**

面向对象风格

``` php
<?php
$date = new DateTime('2006-12-12');
$date->modify('+1 day');
echo $date->format('Y-m-d');
?>
```

过程化风格

``` php
<?php
$date = date_create('2006-12-12');
date_modify($date, '+1 day');
echo date_format($date, 'Y-m-d');
?>
```

以上例程会输出：

    2006-12-13

**示例 \#2 增加或者减少月份的时候需要注意**

``` php
<?php
$date = new DateTime('2000-12-31');

$date->modify('+1 month');
echo $date->format('Y-m-d') . "\n";

$date->modify('+1 month');
echo $date->format('Y-m-d') . "\n";
?>
```

以上例程会输出：

    2001-01-31
    2001-03-03

### 参见

-   <span class="function">strtotime</span>
-   <span class="function">DateTime::add</span>
-   <span class="function">DateTime::sub</span>
-   <span class="function">DateTime::setDate</span>
-   <span class="function">DateTime::setISODate</span>
-   <span class="function">DateTime::setTime</span>
-   <span class="function">DateTime::setTimestamp</span>

DateTime::\_\_set\_state
========================

\_\_set\_state 魔术方法处理函数

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">DateTime</span> <span
class="methodname">DateTime::\_\_set\_state</span> ( <span
class="methodparam"><span class="type">array</span> `$array`</span> )

<a href="/language/oop5/magic.html#object.set-state" class="link">__set_state()</a>
魔术方法处理函数。

### 参数

`array`  
用来初始化对象属性值的数组。

### 返回值

返回 DateTime 对象实例。

DateTime::setDate
=================

date\_date\_set
===============

设置 DateTime 对象的日期

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">DateTime::setDate</span> ( <span
class="methodparam"><span class="type">int</span> `$year`</span> , <span
class="methodparam"><span class="type">int</span> `$month`</span> ,
<span class="methodparam"><span class="type">int</span> `$day`</span> )

过程化风格

<span class="type">DateTime</span> <span
class="methodname">date\_date\_set</span> ( <span
class="methodparam"><span class="type">DateTime</span> `$object`</span>
, <span class="methodparam"><span class="type">int</span> `$year`</span>
, <span class="methodparam"><span class="type">int</span>
`$month`</span> , <span class="methodparam"><span
class="type">int</span> `$day`</span> )

设置 DateTime 对象的日期。

### 参数

`object`  
仅过程化风格：由 <span class="function">date\_create</span> 返回的 <span
class="classname">DateTime</span> 类型的对象。此函数会修改这个对象。

`year`  
年份。

`month`  
月份。

`day`  
日。

### 返回值

返回被修改的 DateTime 对象， 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">DateTime::setDate</span> 例程**

面向对象风格

``` php
<?php
$date = new DateTime();
$date->setDate(2001, 2, 3);
echo $date->format('Y-m-d');
?>
```

过程化风格

``` php
<?php
$date = date_create();
date_date_set($date, 2001, 2, 3);
echo date_format($date, 'Y-m-d');
?>
```

以上例程会输出：

    2001-02-03

**示例 \#2 超出范围的部分会向上一级增加**

``` php
<?php
$date = new DateTime();

$date->setDate(2001, 2, 28);
echo $date->format('Y-m-d') . "\n";

$date->setDate(2001, 2, 29);
echo $date->format('Y-m-d') . "\n";

$date->setDate(2001, 14, 3);
echo $date->format('Y-m-d') . "\n";
?>
```

以上例程会输出：

    2001-02-28
    2001-03-01
    2002-02-03

### 参见

-   <span class="function">DateTime::setISODate</span>
-   <span class="function">DateTime::setTime</span>

DateTime::setISODate
====================

date\_isodate\_set
==================

设置 ISO 日期

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">DateTime::setISODate</span> ( <span
class="methodparam"><span class="type">int</span> `$year`</span> , <span
class="methodparam"><span class="type">int</span> `$week`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$dayOfWeek`<span class="initializer"> = 1</span></span> \] )

过程化风格

<span class="type">DateTime</span> <span
class="methodname">date\_isodate\_set</span> ( <span
class="methodparam"><span class="type">DateTime</span> `$object`</span>
, <span class="methodparam"><span class="type">int</span> `$year`</span>
, <span class="methodparam"><span class="type">int</span> `$week`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$dayOfWeek`<span class="initializer"> = 1</span></span> \] )

以 ISO 8601 规范的格式设置日期，
使用周和日的偏移量作为参数，而不是使用月和日。

### 参数

`object`  
仅过程化风格：由 <span class="function">date\_create</span> 返回的 <span
class="classname">DateTime</span> 类型的对象。此函数会修改这个对象。

`year`  
年份。

`week`  
周。

`dayOfWeek`  
从周的第一天计算，日在一周内的偏移量。

### 返回值

返回被修改的 DateTime 对象， 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">DateTime::setISODate</span> 例程**

面向对象风格

``` php
<?php
$date = new DateTime();

$date->setISODate(2008, 2);
echo $date->format('Y-m-d') . "\n";

$date->setISODate(2008, 2, 7);
echo $date->format('Y-m-d') . "\n";
?>
```

过程化风格

``` php
<?php
$date = date_create();

date_isodate_set($date, 2008, 2);
echo date_format($date, 'Y-m-d') . "\n";

date_isodate_set($date, 2008, 2, 7);
echo date_format($date, 'Y-m-d') . "\n";
?>
```

以上例程会输出：

    2008-01-07
    2008-01-13

**示例 \#2 超出有效范围的部分，会加到上一级**

``` php
<?php
$date = new DateTime();

$date->setISODate(2008, 2, 7);
echo $date->format('Y-m-d') . "\n";

$date->setISODate(2008, 2, 8);
echo $date->format('Y-m-d') . "\n";

$date->setISODate(2008, 53, 7);
echo $date->format('Y-m-d') . "\n";
?>
```

以上例程会输出：

    2008-01-13
    2008-01-14
    2009-01-04

**示例 \#3 找出来某个周所属的月份**

``` php
<?php
$date = new DateTime();
$date->setISODate(2008, 14);
echo $date->format('n');
?>
```

以上例程会输出：

    3

### 参见

-   <span class="function">DateTime::setDate</span>
-   <span class="function">DateTime::setTime</span>

DateTime::setTime
=================

date\_time\_set
===============

设置 DateTime 对象的时间

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">DateTime::setTime</span> ( <span
class="methodparam"><span class="type">int</span> `$hour`</span> , <span
class="methodparam"><span class="type">int</span> `$minute`</span> \[,
<span class="methodparam"><span class="type">int</span> `$second`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$microsecond`<span
class="initializer"> = 0</span></span> \]\] )

过程化风格

<span class="type">DateTime</span> <span
class="methodname">date\_time\_set</span> ( <span
class="methodparam"><span class="type">DateTime</span> `$object`</span>
, <span class="methodparam"><span class="type">int</span> `$hour`</span>
, <span class="methodparam"><span class="type">int</span>
`$minute`</span> \[, <span class="methodparam"><span
class="type">int</span> `$second`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$microsecond`<span class="initializer"> =
0</span></span> \]\] )

设置 DateTime 对象的时间。

### 参数

`object`  
仅过程化风格：由 <span class="function">date\_create</span> 返回的 <span
class="classname">DateTime</span> 类型的对象。此函数会修改这个对象。

`hour`  
小时。

`minute`  
分钟。

`second`  
秒。

`microsecond`  
微秒。

### 返回值

返回被修改的 DateTime 对象， 或者在失败时返回 **`false`**.

### 更新日志

| 版本  | 说明                      |
|-------|---------------------------|
| 7.1.0 | 新增 `microsecond` 参数。 |

### 范例

**示例 \#1 <span class="function">DateTime::setTime</span> 例程**

面向对象风格

``` php
<?php
$date = new DateTime('2001-01-01');

$date->setTime(14, 55);
echo $date->format('Y-m-d H:i:s') . "\n";

$date->setTime(14, 55, 24);
echo $date->format('Y-m-d H:i:s') . "\n";
?>
```

过程化风格

``` php
<?php
$date = date_create('2001-01-01');

date_time_set($date, 14, 55);
echo date_format($date, 'Y-m-d H:i:s') . "\n";

date_time_set($date, 14, 55, 24);
echo date_format($date, 'Y-m-d H:i:s') . "\n";
?>
```

以上例程的输出类似于：

    2001-01-01 14:55:00
    2001-01-01 14:55:24

**示例 \#2 超出有效范围的部分会增加到上一级**

``` php
<?php
$date = new DateTime('2001-01-01');

$date->setTime(14, 55, 24);
echo $date->format('Y-m-d H:i:s') . "\n";

$date->setTime(14, 55, 65);
echo $date->format('Y-m-d H:i:s') . "\n";

$date->setTime(14, 65, 24);
echo $date->format('Y-m-d H:i:s') . "\n";

$date->setTime(25, 55, 24);
echo $date->format('Y-m-d H:i:s') . "\n";
?>
```

以上例程会输出：

    2001-01-01 14:55:24
    2001-01-01 14:56:05
    2001-01-01 15:05:24
    2001-01-02 01:55:24

### 参见

-   <span class="function">DateTime::setDate</span>
-   <span class="function">DateTime::setISODate</span>

DateTime::setTimestamp
======================

date\_timestamp\_set
====================

以 Unix 时间戳的方式设置 DateTime 对象

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">DateTime::setTimestamp</span> ( <span
class="methodparam"><span class="type">int</span>
`$unixtimestamp`</span> )

过程化风格

<span class="type">DateTime</span> <span
class="methodname">date\_timestamp\_set</span> ( <span
class="methodparam"><span class="type">DateTime</span> `$object`</span>
, <span class="methodparam"><span class="type">int</span>
`$unixtimestamp`</span> )

以 Unix 时间戳的方式设置 DateTime 对象的日期和时间。

### 参数

`object`  
仅过程化风格：由 <span class="function">date\_create</span> 返回的 <span
class="classname">DateTime</span> 类型的对象。此函数会修改这个对象。

`unixtimestamp`  
表示日期时间的 Unix 时间戳。

### 返回值

返回被修改的 DateTime 对象， 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">DateTime::setTimestamp</span> 例程**

面向对象风格

``` php
<?php
$date = new DateTime();
echo $date->format('U = Y-m-d H:i:s') . "\n";

$date->setTimestamp(1171502725);
echo $date->format('U = Y-m-d H:i:s') . "\n";
?>
```

过程化风格

``` php
<?php
$date = date_create();
echo date_format($date, 'U = Y-m-d H:i:s') . "\n";

date_timestamp_set($date, 1171502725);
echo date_format($date, 'U = Y-m-d H:i:s') . "\n";
?>
```

以上例程的输出类似于：

    1272508903 = 2010-04-28 22:41:43
    1171502725 = 2007-02-14 20:25:25

### 注释

PHP 5.2 之后的版本中， 可以使用 Unix 时间戳作为构造函数的参数生成新的
<span class="type">DateTime</span> 对象，例如：

**示例 \#2 PHP 5.2 之后的版本中，<span
class="function">DateTime::setTimestamp</span> 替代方案**

``` php
<?php
$ts = 1171502725;
$date = new DateTime("@$ts");
echo $date->format('U = Y-m-d H:i:s') . "\n";
?>
```

以上例程的输出类似于：

    1171502725 = 2007-02-14 20:25:25

### 参见

-   <span class="function">DateTime::getTimestamp</span>

DateTime::setTimezone
=====================

date\_timezone\_set
===================

设置 DateTime 对象的时区

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">DateTime::setTimezone</span> ( <span
class="methodparam"><span class="type">DateTimeZone</span>
`$timezone`</span> )

过程化风格

<span class="type">DateTime</span> <span
class="methodname">date\_timezone\_set</span> ( <span
class="methodparam"><span class="type">DateTime</span> `$object`</span>
, <span class="methodparam"><span class="type">DateTimeZone</span>
`$timezone`</span> )

设置 <span class="classname">DateTime</span> <span
class="type">object</span> 的时区。

### 参数

`object`  
仅过程化风格：由 <span class="function">date\_create</span> 返回的 <span
class="classname">DateTime</span> 类型的对象。此函数会修改这个对象。

`timezone`  
<span class="classname">DateTimeZone</span> 对象， 表示要设置为时区。

### 返回值

返回被修改的 DateTime 对象， 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">DateTime::setTimeZone</span> 例程**

面向对象风格

``` php
<?php
$date = new DateTime('2000-01-01', new DateTimeZone('Pacific/Nauru'));
echo $date->format('Y-m-d H:i:sP') . "\n";

$date->setTimezone(new DateTimeZone('Pacific/Chatham'));
echo $date->format('Y-m-d H:i:sP') . "\n";
?>
```

过程化风格

``` php
<?php
$date = date_create('2000-01-01', timezone_open('Pacific/Nauru'));
echo date_format($date, 'Y-m-d H:i:sP') . "\n";

date_timezone_set($date, timezone_open('Pacific/Chatham'));
echo date_format($date, 'Y-m-d H:i:sP') . "\n";
?>
```

以上例程会输出：

    2000-01-01 00:00:00+12:00
    2000-01-01 01:45:00+13:45

### 参见

-   <span class="function">DateTime::getTimezone</span>
-   <span class="function">DateTimeZone::\_\_construct</span>

DateTime::sub
=============

date\_sub
=========

对一个 DateTime 对象减去一定量的 日、月、年、小时、分钟和秒。

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">DateTime::sub</span> ( <span
class="methodparam"><span class="type">DateInterval</span>
`$interval`</span> )

过程化风格

<span class="type">DateTime</span> <span
class="methodname">date\_sub</span> ( <span class="methodparam"><span
class="type">DateTime</span> `$object`</span> , <span
class="methodparam"><span class="type">DateInterval</span>
`$interval`</span> )

<span class="classname">DateInterval</span> 对象，
表示要减去多少量的时间。

### 参数

`object`  
仅过程化风格：由 <span class="function">date\_create</span> 返回的 <span
class="classname">DateTime</span> 类型的对象。此函数会修改这个对象。

`interval`  
<span class="classname">DateInterval</span> 对象

### 返回值

返回被修改的 DateTime 对象， 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">DateTime::sub</span> 例程**

面向对象风格

``` php
<?php
$date = new DateTime('2000-01-20');
$date->sub(new DateInterval('P10D'));
echo $date->format('Y-m-d') . "\n";
?>
```

过程化风格

``` php
<?php
$date = date_create('2000-01-20');
date_sub($date, date_interval_create_from_date_string('10 days'));
echo date_format($date, 'Y-m-d');
?>
```

以上例程会输出：

    2000-01-10

**示例 \#2 Further <span class="function">DateTime::sub</span> 例程**

``` php
<?php
$date = new DateTime('2000-01-20');
$date->sub(new DateInterval('PT10H30S'));
echo $date->format('Y-m-d H:i:s') . "\n";

$date = new DateTime('2000-01-20');
$date->sub(new DateInterval('P7Y5M4DT4H3M2S'));
echo $date->format('Y-m-d H:i:s') . "\n";
?>
```

以上例程会输出：

    2000-01-19 13:59:30
    1992-08-15 19:56:58

**示例 \#3 减去一定量的月份的时候需要注意**

``` php
<?php
$date = new DateTime('2001-04-30');
$interval = new DateInterval('P1M');

$date->sub($interval);
echo $date->format('Y-m-d') . "\n";

$date->sub($interval);
echo $date->format('Y-m-d') . "\n";
?>
```

以上例程会输出：

    2001-03-30
    2001-03-02

### 注释

在 PHP 5.2 之后，可以使用 <span class="function">DateTime::modify</span>
作为替代。

### 参见

-   <span class="function">DateTime::add</span>
-   <span class="function">DateTime::diff</span>
-   <span class="function">DateTime::modify</span>

简介
----

Representation of date and time.

类摘要
------

**DateTimeImmutable**

<span class="ooclass"> class **DateTimeImmutable** </span> <span
class="oointerface">implements <span
class="interfacename">DateTimeInterface</span> </span> {

/\* 继承的常量 \*/

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::ATOM` <span class="initializer"> =
"Y-m-d\\TH:i:sP"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::COOKIE` <span class="initializer"> = "l, d-M-Y H:i:s
T"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::ISO8601` <span class="initializer"> =
"Y-m-d\\TH:i:sO"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC822` <span class="initializer"> = "D, d M y H:i:s
O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC850` <span class="initializer"> = "l, d-M-y H:i:s
T"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC1036` <span class="initializer"> = "D, d M y
H:i:s O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC1123` <span class="initializer"> = "D, d M Y
H:i:s O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC7231` <span class="initializer"> = "D, d M Y
H:i:s \\G\\M\\T"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC2822` <span class="initializer"> = "D, d M Y
H:i:s O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC3339` <span class="initializer"> =
"Y-m-d\\TH:i:sP"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC3339_EXTENDED` <span class="initializer"> =
"Y-m-d\\TH:i:s.vP"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RSS` <span class="initializer"> = "D, d M Y H:i:s
O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::W3C` <span class="initializer"> =
"Y-m-d\\TH:i:sP"</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$datetime`<span
class="initializer"> = "now"</span></span> \[, <span
class="methodparam"><span class="type">DateTimeZone</span>
`$timezone`<span class="initializer"> = **`null`**</span></span> \]\] )

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">add</span> ( <span class="methodparam"><span
class="type">DateInterval</span> `$interval`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">createFromFormat</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> ,
<span class="methodparam"><span class="type">string</span>
`$datetime`</span> \[, <span class="methodparam"><span
class="type">DateTimeZone</span> `$timezone`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">createFromInterface</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$object`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">createFromMutable</span> ( <span
class="methodparam"><span class="type">DateTime</span> `$object`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getLastErrors</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">DateTimeImmutable</span><span
class="type">false</span></span> <span class="methodname">modify</span>
( <span class="methodparam"><span class="type">string</span>
`$modifier`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">\_\_set\_state</span> ( <span
class="methodparam"><span class="type">array</span> `$array`</span> )

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">setDate</span> ( <span class="methodparam"><span
class="type">int</span> `$year`</span> , <span class="methodparam"><span
class="type">int</span> `$month`</span> , <span
class="methodparam"><span class="type">int</span> `$day`</span> )

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">setISODate</span> ( <span class="methodparam"><span
class="type">int</span> `$year`</span> , <span class="methodparam"><span
class="type">int</span> `$week`</span> \[, <span
class="methodparam"><span class="type">int</span> `$day`<span
class="initializer"> = 1</span></span> \] )

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">setTime</span> ( <span class="methodparam"><span
class="type">int</span> `$hour`</span> , <span class="methodparam"><span
class="type">int</span> `$minute`</span> \[, <span
class="methodparam"><span class="type">int</span> `$second`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$microsecond`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">setTimestamp</span> ( <span class="methodparam"><span
class="type">int</span> `$timestamp`</span> )

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">setTimezone</span> ( <span class="methodparam"><span
class="type">DateTimeZone</span> `$timezone`</span> )

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">sub</span> ( <span class="methodparam"><span
class="type">DateInterval</span> `$interval`</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">DateInterval</span><span class="type">false</span></span>
<span class="methodname">diff</span> ( <span class="methodparam"><span
class="type">DateTimeInterface</span> `$targetObject`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$absolute`<span
class="initializer"> = **`false`**</span></span> \] )

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">false</span></span> <span
class="methodname">format</span> ( <span class="methodparam"><span
class="type">string</span> `$format`</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">int</span><span class="type">false</span></span> <span
class="methodname">getOffset</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getTimestamp</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">DateTimeZone</span><span class="type">false</span></span>
<span class="methodname">getTimezone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_wakeup</span> ( <span
class="methodparam">void</span> )

}

DateTimeImmutable::add
======================

Adds an amount of days, months, years, hours, minutes and seconds

### 说明

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">DateTimeImmutable::add</span> ( <span
class="methodparam"><span class="type">DateInterval</span>
`$interval`</span> )

Like <span class="methodname">DateTime::add</span> but works with <span
class="classname">DateTimeImmutable</span>.

DateTimeImmutable::\_\_construct
================================

date\_create\_immutable
=======================

Returns new DateTimeImmutable object

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="methodname">DateTimeImmutable::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$datetime`<span
class="initializer"> = "now"</span></span> \[, <span
class="methodparam"><span class="type">DateTimeZone</span>
`$timezone`<span class="initializer"> = **`null`**</span></span> \]\] )

过程化风格

<span class="type">DateTimeImmutable</span> <span
class="methodname">date\_create\_immutable</span> (\[ <span
class="methodparam"><span class="type">string</span> `$datetime`<span
class="initializer"> = "now"</span></span> \[, <span
class="methodparam"><span class="type">DateTimeZone</span>
`$timezone`<span class="initializer"> = **`null`**</span></span> \]\] )

Like <span class="methodname">DateTime::\_\_construct</span> but works
with <span class="classname">DateTimeImmutable</span>.

DateTimeImmutable::createFromFormat
===================================

date\_create\_immutable\_from\_format
=====================================

Parses a time string according to a specified format

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">DateTimeImmutable::createFromFormat</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> ,
<span class="methodparam"><span class="type">string</span>
`$datetime`</span> \[, <span class="methodparam"><span
class="type">DateTimeZone</span> `$timezone`</span> \] )

过程化风格

<span class="type">DateTimeImmutable</span> <span
class="methodname">date\_create\_immutable\_from\_format</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> ,
<span class="methodparam"><span class="type">string</span>
`$datetime`</span> \[, <span class="methodparam"><span
class="type">DateTimeZone</span> `$timezone`</span> \] )

Like <span class="methodname">DateTime::createFromFormat</span> but
works with <span class="classname">DateTimeImmutable</span>.

DateTimeImmutable::createFromInterface
======================================

Returns new DateTimeImmutable object encapsulating the given
DateTimeInterface object

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">DateTimeImmutable::createFromInterface</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$object`</span> )

### 参数

`object`  
The <span class="classname">DateTimeInterface</span> object that needs
to be converted to an immutable version. This object is not modified,
but instead a new <span class="classname">DateTimeImmutable</span>
object is created containing the same date, time, and timezone
information.

### 返回值

Returns a new <span class="classname">DateTimeImmutable</span> instance.

### 范例

**示例 \#1 Creating an immutable date time object**

``` php
<?php
$date = new DateTime("2014-06-20 11:45 Europe/London");

$immutable = DateTimeImmutable::createFromInterface($date);

$date = new DateTimeImmutable("2014-06-20 11:45 Europe/London");
$also_immutable = DateTimeImmutable::createFromInterface($date);
?>
```

DateTimeImmutable::createFromMutable
====================================

Returns new DateTimeImmutable object encapsulating the given DateTime
object

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">DateTimeImmutable::createFromMutable</span> ( <span
class="methodparam"><span class="type">DateTime</span> `$object`</span>
)

### 参数

`object`  
The mutable <span class="classname">DateTime</span> object that you want
to convert to an immutable version. This object is not modified, but
instead a new <span class="classname">DateTimeImmutable</span> object is
created containing the same date time and timezone information.

### 范例

**示例 \#1 Creating an immutable date time object**

``` php
<?php
$date = new DateTime("2014-06-20 11:45 Europe/London");

$immutable = DateTimeImmutable::createFromMutable( $date );
?>
```

### 返回值

Returns a new <span class="classname">DateTimeImmutable</span> instance.

DateTimeImmutable::getLastErrors
================================

Returns the warnings and errors

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">DateTimeImmutable::getLastErrors</span> ( <span
class="methodparam">void</span> )

Like <span class="methodname">DateTime::getLastErrors</span> but works
with <span class="classname">DateTimeImmutable</span>.

DateTimeImmutable::modify
=========================

Creates a new object with modified timestamp

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">DateTimeImmutable</span><span
class="type">false</span></span> <span
class="methodname">DateTimeImmutable::modify</span> ( <span
class="methodparam"><span class="type">string</span> `$modifier`</span>
)

Creates a new <span class="type">DateTimeImmutable</span> object with
modified timestamp. The original object is not modified.

### 参数

`object`  
仅过程化风格：由 <span class="function">date\_create</span> 返回的 <span
class="classname">DateTime</span> 类型的对象。此函数会修改这个对象。

`modifier`  
日期/时间字符串。正确格式的说明详见
<a href="/datetime/formats.html" class="link">日期与时间格式</a>。

### 返回值

Returns the newly created object 或者在失败时返回 **`false`**.

DateTimeImmutable::\_\_set\_state
=================================

The \_\_set\_state handler

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">DateTimeImmutable::\_\_set\_state</span> ( <span
class="methodparam"><span class="type">array</span> `$array`</span> )

Like <span class="methodname">DateTime::\_\_set\_state</span> but works
with <span class="classname">DateTimeImmutable</span>.

DateTimeImmutable::setDate
==========================

Sets the date

### 说明

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">DateTimeImmutable::setDate</span> ( <span
class="methodparam"><span class="type">int</span> `$year`</span> , <span
class="methodparam"><span class="type">int</span> `$month`</span> ,
<span class="methodparam"><span class="type">int</span> `$day`</span> )

Like <span class="methodname">DateTime::setDate</span> but works with
<span class="classname">DateTimeImmutable</span>.

DateTimeImmutable::setISODate
=============================

Sets the ISO date

### 说明

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">DateTimeImmutable::setISODate</span> ( <span
class="methodparam"><span class="type">int</span> `$year`</span> , <span
class="methodparam"><span class="type">int</span> `$week`</span> \[,
<span class="methodparam"><span class="type">int</span> `$day`<span
class="initializer"> = 1</span></span> \] )

Like <span class="methodname">DateTime::setISODate</span> but works with
<span class="classname">DateTimeImmutable</span>.

DateTimeImmutable::setTime
==========================

Sets the time

### 说明

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">DateTimeImmutable::setTime</span> ( <span
class="methodparam"><span class="type">int</span> `$hour`</span> , <span
class="methodparam"><span class="type">int</span> `$minute`</span> \[,
<span class="methodparam"><span class="type">int</span> `$second`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$microsecond`<span
class="initializer"> = 0</span></span> \]\] )

Like <span class="methodname">DateTime::setTime</span> but works with
<span class="classname">DateTimeImmutable</span>.

DateTimeImmutable::setTimestamp
===============================

Sets the date and time based on a Unix timestamp

### 说明

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">DateTimeImmutable::setTimestamp</span> ( <span
class="methodparam"><span class="type">int</span> `$timestamp`</span> )

Like <span class="methodname">DateTime::setTimestamp</span> but works
with <span class="classname">DateTimeImmutable</span>.

DateTimeImmutable::setTimezone
==============================

Sets the time zone

### 说明

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">DateTimeImmutable::setTimezone</span> ( <span
class="methodparam"><span class="type">DateTimeZone</span>
`$timezone`</span> )

Like <span class="methodname">DateTime::setTimezone</span> but works
with <span class="classname">DateTimeImmutable</span>.

DateTimeImmutable::sub
======================

Subtracts an amount of days, months, years, hours, minutes and seconds

### 说明

<span class="modifier">public</span> <span
class="type">DateTimeImmutable</span> <span
class="methodname">DateTimeImmutable::sub</span> ( <span
class="methodparam"><span class="type">DateInterval</span>
`$interval`</span> )

Like <span class="methodname">DateTime::sub</span> but works with <span
class="classname">DateTimeImmutable</span>.

简介
----

DateTimeInterface 的意思是可以约束类型为 DateTime 或
DateTimeImmutable。此接口不能让用户自己的 class 去实现（implements）。

类摘要
------

**DateTimeInterface**

<span class="ooclass"> class **DateTimeInterface** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::ATOM` <span class="initializer"> =
"Y-m-d\\TH:i:sP"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::COOKIE` <span class="initializer"> = "l, d-M-Y H:i:s
T"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::ISO8601` <span class="initializer"> =
"Y-m-d\\TH:i:sO"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC822` <span class="initializer"> = "D, d M y H:i:s
O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC850` <span class="initializer"> = "l, d-M-y H:i:s
T"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC1036` <span class="initializer"> = "D, d M y
H:i:s O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC1123` <span class="initializer"> = "D, d M Y
H:i:s O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC7231` <span class="initializer"> = "D, d M Y
H:i:s \\G\\M\\T"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC2822` <span class="initializer"> = "D, d M Y
H:i:s O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC3339` <span class="initializer"> =
"Y-m-d\\TH:i:sP"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RFC3339_EXTENDED` <span class="initializer"> =
"Y-m-d\\TH:i:s.vP"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::RSS` <span class="initializer"> = "D, d M Y H:i:s
O"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`DateTimeInterface::W3C` <span class="initializer"> =
"Y-m-d\\TH:i:sP"</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type"><span
class="type">DateInterval</span><span class="type">false</span></span>
<span class="methodname">diff</span> ( <span class="methodparam"><span
class="type">DateTimeInterface</span> `$targetObject`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$absolute`<span
class="initializer"> = **`false`**</span></span> \] )

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">false</span></span> <span
class="methodname">format</span> ( <span class="methodparam"><span
class="type">string</span> `$format`</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">int</span><span class="type">false</span></span> <span
class="methodname">getOffset</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getTimestamp</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">DateTimeZone</span><span class="type">false</span></span>
<span class="methodname">getTimezone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_wakeup</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`DateTimeInterface::ATOM`**  
**`DATE_ATOM`**  
<span class="simpara"> Atom 格式（示例：2005-08-15T15:52:01+00:00）
</span>

**`DateTimeInterface::COOKIE`**  
**`DATE_COOKIE`**  
<span class="simpara"> HTTP Cookies 格式（示例：Monday, 15-Aug-2005
15:52:01 UTC） </span>

**`DateTimeInterface::ISO8601`**  
**`DATE_ISO8601`**  
<span class="simpara"> ISO-8601 格式（示例：2005-08-15T15:52:01+0000）
</span>

> **Note**: <span class="simpara"> 这种格式和 ISO-8601
> 的格式并不兼容，只是出于向后兼容的原因才保留的。 如果要使用和 ISO-8601
> 兼容的格式， 请使用 **`DateTime::ATOM`** 或 **`DATE_ATOM`** 两个常量。
> </span>

**`DateTimeInterface::RFC822`**  
**`DATE_RFC822`**  
<span class="simpara"> RFC 822 格式（示例：Mon, 15 Aug 05 15:52:01
+0000） </span>

**`DateTimeInterface::RFC850`**  
**`DATE_RFC850`**  
<span class="simpara"> RFC 850 格式（示例：Monday, 15-Aug-05 15:52:01
UTC） </span>

**`DateTimeInterface::RFC1036`**  
**`DATE_RFC1036`**  
<span class="simpara"> RFC 1036（示例：Mon, 15 Aug 05 15:52:01 +0000）
</span>

**`DateTimeInterface::RFC1123`**  
**`DATE_RFC1123`**  
<span class="simpara"> RFC 1123 格式（示例：Mon, 15 Aug 2005 15:52:01
+0000） </span>

**`DateTimeInterface::RFC7231`**  
**`DATE_RFC7231`**  
<span class="simpara"> RFC 7231 格式 (自 PHP 7.0.19 和 7.1.5 可用)
(示例：Sat, 30 Apr 2016 17:52:13 GMT) </span>

**`DateTimeInterface::RFC2822`**  
**`DATE_RFC2822`**  
<span class="simpara"> RFC 2822 格式（示例：Mon, 15 Aug 2005 15:52:01
+0000） </span>

**`DateTimeInterface::RFC3339`**  
**`DATE_RFC3339`**  
<span class="simpara"> 同 **`DATE_ATOM`**（自 PHP 5.1.3 版本可用）
</span>

**`DateTimeInterface::RFC3339_EXTENDED`**  
**`DATE_RFC3339_EXTENDED`**  
<span class="simpara"> RFC 3339 EXTENDED 格式（自 PHP 7.0.0
可用）（示例：2005-08-15T15:52:01.000+00:00） </span>

**`DateTimeInterface::RSS`**  
**`DATE_RSS`**  
<span class="simpara"> RSS（示例：Mon, 15 Aug 2005 15:52:01 +0000）
</span>

**`DateTimeInterface::W3C`**  
**`DATE_W3C`**  
<span class="simpara"> RSS 格式（示例：2005-08-15T15:52:01+00:00）
</span>

更新日志
--------

| 版本  | 说明                                                                                                                                  |
|-------|---------------------------------------------------------------------------------------------------------------------------------------|
| 7.2.0 | <span class="classname">DateTime</span> 的类常量现在定义在了 <span class="classname">DateTimeInterface</span> 上。                    |
| 5.5.8 | 尝试实现（implement）<span class="classname">DateTimeInterface</span> 时，会抛出严重错误。 之前此举不会产生错误，但这种做法是不对的。 |

DateTime::diff
==============

DateTimeImmutable::diff
=======================

DateTimeInterface::diff
=======================

date\_diff
==========

Returns the difference between two DateTime objects

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type"><span
class="type">DateInterval</span><span class="type">false</span></span>
<span class="methodname">DateTime::diff</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$targetObject`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$absolute`<span class="initializer"> =
**`false`**</span></span> \] )

<span class="modifier">public</span> <span class="type"><span
class="type">DateInterval</span><span class="type">false</span></span>
<span class="methodname">DateTimeImmutable::diff</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$targetObject`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$absolute`<span class="initializer"> =
**`false`**</span></span> \] )

<span class="modifier">public</span> <span class="type"><span
class="type">DateInterval</span><span class="type">false</span></span>
<span class="methodname">DateTimeInterface::diff</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$targetObject`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$absolute`<span class="initializer"> =
**`false`**</span></span> \] )

过程化风格

<span class="type"><span class="type">DateInterval</span><span
class="type">false</span></span> <span
class="methodname">date\_diff</span> ( <span class="methodparam"><span
class="type">DateTimeInterface</span> `$originObject`</span> , <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$targetObject`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$absolute`<span class="initializer"> =
**`false`**</span></span> \] )

Returns the difference between two <span
class="classname">DateTimeInterface</span> objects.

### 参数

`datetime`  
The date to compare to.

`absolute`  
Should the interval be forced to be positive?

### 返回值

The <span class="classname">DateInterval</span> object represents the
difference between the two dates 或者在失败时返回 **`false`**.

The return value more specifically represents the interval to apply to
the original object (`$this` or `$originObject`) to arrive at the
`$targetObject`. This process is not always reversible.

### 范例

**示例 \#1 <span class="function">DateTime::diff</span> example**

面向对象风格

``` php
<?php
$origin = new DateTime('2009-10-11');
$target = new DateTime('2009-10-13');
$interval = $origin->diff($target);
echo $interval->format('%R%a days');
?>
```

过程化风格

``` php
<?php
$origin = date_create('2009-10-11');
$target = date_create('2009-10-13');
$interval = date_diff($origin, $target);
echo $interval->format('%R%a days');
?>
```

以上例程会输出：

    +2 days

**示例 \#2 <span class="classname">DateTime</span> object comparison**

> **Note**:
>
> As of PHP 5.2.2, DateTime objects can be compared using
> <a href="/language/operators/comparison.html" class="link">comparison operators</a>.

``` php
<?php
$date1 = new DateTime("now");
$date2 = new DateTime("tomorrow");

var_dump($date1 == $date2);
var_dump($date1 < $date2);
var_dump($date1 > $date2);
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(false)

### 参见

-   <span class="function">DateInterval::format</span>
-   <span class="function">DateTime::add</span>
-   <span class="function">DateTime::sub</span>

DateTime::format
================

DateTimeImmutable::format
=========================

DateTimeInterface::format
=========================

date\_format
============

Returns date formatted according to given format

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">false</span></span> <span
class="methodname">DateTime::format</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">false</span></span> <span
class="methodname">DateTimeImmutable::format</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">false</span></span> <span
class="methodname">DateTimeInterface::format</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> )

过程化风格

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">date\_format</span> ( <span class="methodparam"><span
class="type">DateTimeInterface</span> `$object`</span> , <span
class="methodparam"><span class="type">string</span> `$format`</span> )

Returns date formatted according to given format.

### 参数

`object`  
仅为过程化风格：由 <span class="function">date\_create</span> 返回的
<span class="classname">DateTime</span> 类型的对象。

`format`  
The format of the outputted date <span class="type">string</span>. See
the formatting options below. There are also several
<a href="/class/datetimeinterface.html#预定义常量" class="link">predefined date constants</a>
that may be used instead, so for example **`DATE_RSS`** contains the
format string *'D, d M Y H:i:s'*.

|  `format` character | Description                                                                                                                                                                                                                                                                                                      | Example returned values                       |
|:-------------------:|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
|        *Day*        | ---                                                                                                                                                                                                                                                                                                              | ---                                           |
|         *d*         | Day of the month, 2 digits with leading zeros                                                                                                                                                                                                                                                                    | *01* to *31*                                  |
|         *D*         | A textual representation of a day, three letters                                                                                                                                                                                                                                                                 | *Mon* through *Sun*                           |
|         *j*         | Day of the month without leading zeros                                                                                                                                                                                                                                                                           | *1* to *31*                                   |
| *l* (lowercase 'L') | A full textual representation of the day of the week                                                                                                                                                                                                                                                             | *Sunday* through *Saturday*                   |
|         *N*         | ISO-8601 numeric representation of the day of the week                                                                                                                                                                                                                                                           | *1* (for Monday) through *7* (for Sunday)     |
|         *S*         | English ordinal suffix for the day of the month, 2 characters                                                                                                                                                                                                                                                    | *st*, *nd*, *rd* or *th*. Works well with *j* |
|         *w*         | Numeric representation of the day of the week                                                                                                                                                                                                                                                                    | *0* (for Sunday) through *6* (for Saturday)   |
|         *z*         | The day of the year (starting from 0)                                                                                                                                                                                                                                                                            | *0* through *365*                             |
|        *Week*       | ---                                                                                                                                                                                                                                                                                                              | ---                                           |
|         *W*         | ISO-8601 week number of year, weeks starting on Monday                                                                                                                                                                                                                                                           | Example: *42* (the 42nd week in the year)     |
|       *Month*       | ---                                                                                                                                                                                                                                                                                                              | ---                                           |
|         *F*         | A full textual representation of a month, such as January or March                                                                                                                                                                                                                                               | *January* through *December*                  |
|         *m*         | Numeric representation of a month, with leading zeros                                                                                                                                                                                                                                                            | *01* through *12*                             |
|         *M*         | A short textual representation of a month, three letters                                                                                                                                                                                                                                                         | *Jan* through *Dec*                           |
|         *n*         | Numeric representation of a month, without leading zeros                                                                                                                                                                                                                                                         | *1* through *12*                              |
|         *t*         | Number of days in the given month                                                                                                                                                                                                                                                                                | *28* through *31*                             |
|        *Year*       | ---                                                                                                                                                                                                                                                                                                              | ---                                           |
|         *L*         | Whether it's a leap year                                                                                                                                                                                                                                                                                         | *1* if it is a leap year, *0* otherwise.      |
|         *o*         | ISO-8601 week-numbering year. This has the same value as *Y*, except that if the ISO week number (*W*) belongs to the previous or next year, that year is used instead.                                                                                                                                          | Examples: *1999* or *2003*                    |
|         *Y*         | A full numeric representation of a year, 4 digits                                                                                                                                                                                                                                                                | Examples: *1999* or *2003*                    |
|         *y*         | A two digit representation of a year                                                                                                                                                                                                                                                                             | Examples: *99* or *03*                        |
|        *Time*       | ---                                                                                                                                                                                                                                                                                                              | ---                                           |
|         *a*         | Lowercase Ante meridiem and Post meridiem                                                                                                                                                                                                                                                                        | *am* or *pm*                                  |
|         *A*         | Uppercase Ante meridiem and Post meridiem                                                                                                                                                                                                                                                                        | *AM* or *PM*                                  |
|         *B*         | Swatch Internet time                                                                                                                                                                                                                                                                                             | *000* through *999*                           |
|         *g*         | 12-hour format of an hour without leading zeros                                                                                                                                                                                                                                                                  | *1* through *12*                              |
|         *G*         | 24-hour format of an hour without leading zeros                                                                                                                                                                                                                                                                  | *0* through *23*                              |
|         *h*         | 12-hour format of an hour with leading zeros                                                                                                                                                                                                                                                                     | *01* through *12*                             |
|         *H*         | 24-hour format of an hour with leading zeros                                                                                                                                                                                                                                                                     | *00* through *23*                             |
|         *i*         | Minutes with leading zeros                                                                                                                                                                                                                                                                                       | *00* to *59*                                  |
|         *s*         | Seconds with leading zeros                                                                                                                                                                                                                                                                                       | *00* through *59*                             |
|         *u*         | Microseconds. Note that <span class="function">date</span> will always generate *000000* since it takes an <span class="type">int</span> parameter, whereas <span class="methodname">DateTime::format</span> does support microseconds if <span class="classname">DateTime</span> was created with microseconds. | Example: *654321*                             |
|         *v*         | Milliseconds (added in PHP 7.0.0). Same note applies as for *u*.                                                                                                                                                                                                                                                 | Example: *654*                                |
|      *Timezone*     | ---                                                                                                                                                                                                                                                                                                              | ---                                           |
|         *e*         | Timezone identifier                                                                                                                                                                                                                                                                                              | Examples: *UTC*, *GMT*, *Atlantic/Azores*     |
|   *I* (capital i)   | Whether or not the date is in daylight saving time                                                                                                                                                                                                                                                               | *1* if Daylight Saving Time, *0* otherwise.   |
|         *O*         | Difference to Greenwich time (GMT) without colon between hours and minutes                                                                                                                                                                                                                                       | Example: *+0200*                              |
|         *P*         | Difference to Greenwich time (GMT) with colon between hours and minutes                                                                                                                                                                                                                                          | Example: *+02:00*                             |
|         *p*         | The same as *P*, but returns *Z* instead of *+00:00*                                                                                                                                                                                                                                                             | Example: *+02:00*                             |
|         *T*         | Timezone abbreviation                                                                                                                                                                                                                                                                                            | Examples: *EST*, *MDT* ...                    |
|         *Z*         | Timezone offset in seconds. The offset for timezones west of UTC is always negative, and for those east of UTC is always positive.                                                                                                                                                                               | *-43200* through *50400*                      |
|   *Full Date/Time*  | ---                                                                                                                                                                                                                                                                                                              | ---                                           |
|         *c*         | ISO 8601 date                                                                                                                                                                                                                                                                                                    | 2004-02-12T15:19:21+00:00                     |
|         *r*         | <a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC 2822</a> formatted date                                                                                                                                                                                                                   | Example: *Thu, 21 Dec 2000 16:01:07 +0200*    |
|         *U*         | Seconds since the Unix Epoch (January 1 1970 00:00:00 GMT)                                                                                                                                                                                                                                                       | See also <span class="function">time</span>   |

Unrecognized characters in the format string will be printed as-is. The
*Z* format will always return *0* when using <span
class="function">gmdate</span>.

> **Note**:
>
> Since this function only accepts <span class="type">int</span>
> timestamps the *u* format character is only useful when using the
> <span class="function">date\_format</span> function with user based
> timestamps created with <span class="function">date\_create</span>.

### 返回值

Returns the formatted date string on success 或者在失败时返回
**`false`**.

### 范例

**示例 \#1 <span class="function">DateTime::format</span> example**

面向对象风格

``` php
<?php
$date = new DateTime('2000-01-01');
echo $date->format('Y-m-d H:i:s');
?>
```

过程化风格

``` php
<?php
$date = date_create('2000-01-01');
echo date_format($date, 'Y-m-d H:i:s');
?>
```

以上例程会输出：

    2000-01-01 00:00:00

### 注释

This method does not use locales. All output is in English.

### 参见

-   <span class="function">date</span>

DateTime::getOffset
===================

DateTimeImmutable::getOffset
============================

DateTimeInterface::getOffset
============================

date\_offset\_get
=================

Returns the timezone offset

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type"><span
class="type">int</span><span class="type">false</span></span> <span
class="methodname">DateTime::getOffset</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">int</span><span class="type">false</span></span> <span
class="methodname">DateTimeImmutable::getOffset</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">int</span><span class="type">false</span></span> <span
class="methodname">DateTimeInterface::getOffset</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">date\_offset\_get</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$object`</span> )

Returns the timezone offset.

### 参数

`object`  
仅为过程化风格：由 <span class="function">date\_create</span> 返回的
<span class="classname">DateTime</span> 类型的对象。

### 返回值

Returns the timezone offset in seconds from UTC on success
或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">DateTime::getOffset</span> example**

面向对象风格

``` php
<?php
$winter = new DateTime('2010-12-21', new DateTimeZone('America/New_York'));
$summer = new DateTime('2008-06-21', new DateTimeZone('America/New_York'));

echo $winter->getOffset() . "\n";
echo $summer->getOffset() . "\n";
?>
```

过程化风格

``` php
<?php
$winter = date_create('2010-12-21', timezone_open('America/New_York'));
$summer = date_create('2008-06-21', timezone_open('America/New_York'));

echo date_offset_get($winter) . "\n";
echo date_offset_get($summer) . "\n";
?>
```

以上例程会输出：

    -18000
    -14400

Note: -18000 = -5 hours, -14400 = -4 hours.

DateTime::getTimestamp
======================

DateTimeImmutable::getTimestamp
===============================

DateTimeInterface::getTimestamp
===============================

date\_timestamp\_get
====================

Gets the Unix timestamp

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DateTime::getTimestamp</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DateTimeImmutable::getTimestamp</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DateTimeInterface::getTimestamp</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">date\_timestamp\_get</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$object`</span> )

Gets the Unix timestamp.

### 参数

此函数没有参数。

### 返回值

Returns the Unix timestamp representing the date.

### 范例

**示例 \#1 <span class="function">DateTime::getTimestamp</span>
example**

面向对象风格

``` php
<?php
$date = new DateTime();
echo $date->getTimestamp();
?>
```

过程化风格

``` php
<?php
$date = date_create();
echo date_timestamp_get($date);
?>
```

以上例程的输出类似于：

    1272509157

### 注释

Using *U* as the parameter to <span
class="function">DateTime::format</span> is an alternative when using
PHP 5.2.

### 参见

-   <span class="function">DateTime::setTimestamp</span>
-   <span class="function">DateTime::format</span>

DateTime::getTimezone
=====================

DateTimeImmutable::getTimezone
==============================

DateTimeInterface::getTimezone
==============================

date\_timezone\_get
===================

Return time zone relative to given DateTime

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type"><span
class="type">DateTimeZone</span><span class="type">false</span></span>
<span class="methodname">DateTime::getTimezone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">DateTimeZone</span><span class="type">false</span></span>
<span class="methodname">DateTimeImmutable::getTimezone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">DateTimeZone</span><span class="type">false</span></span>
<span class="methodname">DateTimeInterface::getTimezone</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type"><span class="type">DateTimeZone</span><span
class="type">false</span></span> <span
class="methodname">date\_timezone\_get</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$object`</span> )

Return time zone relative to given DateTime.

### 参数

`object`  
仅为过程化风格：由 <span class="function">date\_create</span> 返回的
<span class="classname">DateTime</span> 类型的对象。

### 返回值

Returns a <span class="classname">DateTimeZone</span> object on success
或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">DateTime::getTimezone</span> example**

面向对象风格

``` php
<?php
$date = new DateTime(null, new DateTimeZone('Europe/London'));
$tz = $date->getTimezone();
echo $tz->getName();
?>
```

过程化风格

``` php
<?php
$date = date_create(null, timezone_open('Europe/London'));
$tz = date_timezone_get($date);
echo timezone_name_get($tz);
?>
```

以上例程会输出：

    Europe/London

### 参见

-   <span class="function">DateTime::setTimezone</span>

DateTime::\_\_wakeup
====================

DateTimeImmutable::\_\_wakeup
=============================

DateTimeInterface::\_\_wakeup
=============================

The \_\_wakeup handler

### 说明

<span class="modifier">public</span> <span
class="methodname">DateTime::\_\_wakeup</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">DateTimeImmutable::\_\_wakeup</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">DateTimeInterface::\_\_wakeup</span> ( <span
class="methodparam">void</span> )

The
<a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>
handler.

### 参数

此函数没有参数。

### 返回值

Initializes a DateTime object.

简介
----

Representation of time zone.

类摘要
------

**DateTimeZone**

<span class="ooclass"> class **DateTimeZone** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::AFRICA` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::AMERICA` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::ANTARCTICA` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::ARCTIC` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::ASIA` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::ATLANTIC` <span class="initializer"> = 32</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::AUSTRALIA` <span class="initializer"> = 64</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::EUROPE` <span class="initializer"> = 128</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::INDIAN` <span class="initializer"> = 256</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::PACIFIC` <span class="initializer"> = 512</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::UTC` <span class="initializer"> = 1024</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::ALL` <span class="initializer"> = 2047</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::ALL_WITH_BC` <span class="initializer"> = 4095</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`DateTimeZone::PER_COUNTRY` <span class="initializer"> = 4096</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$timezone`</span>
)

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getLocation</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getOffset</span> ( <span class="methodparam"><span
class="type">DateTime</span> `$datetime`</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">false</span></span> <span
class="methodname">getTransitions</span> (\[ <span
class="methodparam"><span class="type">int</span> `$timestampBegin`<span
class="initializer"> = **`PHP_INT_MIN`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$timestampEnd`<span
class="initializer"> = **`PHP_INT_MAX`**</span></span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">listAbbreviations</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">listIdentifiers</span> (\[ <span
class="methodparam"><span class="type">int</span> `$what`<span
class="initializer"> = DateTimeZone::ALL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$country`<span
class="initializer"> = **`null`**</span></span> \]\] )

}

预定义常量
----------

**`DateTimeZone::AFRICA`**  
Africa time zones.

**`DateTimeZone::AMERICA`**  
America time zones.

**`DateTimeZone::ANTARCTICA`**  
Antarctica time zones.

**`DateTimeZone::ARCTIC`**  
Arctic time zones.

**`DateTimeZone::ASIA`**  
Asia time zones.

**`DateTimeZone::ATLANTIC`**  
Atlantic time zones.

**`DateTimeZone::AUSTRALIA`**  
Australia time zones.

**`DateTimeZone::EUROPE`**  
Europe time zones.

**`DateTimeZone::INDIAN`**  
Indian time zones.

**`DateTimeZone::PACIFIC`**  
Pacific time zones.

**`DateTimeZone::UTC`**  
UTC time zones.

**`DateTimeZone::ALL`**  
All time zones.

**`DateTimeZone::ALL_WITH_BC`**  
All time zones including backwards compatible.

**`DateTimeZone::PER_COUNTRY`**  
Time zones per country.

DateTimeZone::\_\_construct
===========================

timezone\_open
==============

创建新的DateTimeZone对象

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="methodname">DateTimeZone::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$timezone`</span>
)

过程化风格

<span class="type">DateTimeZone</span> <span
class="methodname">timezone\_open</span> ( <span
class="methodparam"><span class="type">string</span> `$timezone`</span>
)

创建新的DateTimeZone对象.

### 参数

`timezone`  
所支持的 <a href="/timezones.html" class="link">timezone names</a>之一.

### 返回值

成功时返回 <span class="classname">DateTimeZone</span>对象.
过程化风格在失败时返回 **`false`**。

### 错误／异常

如果提供的时区无效，此方法将抛出 <span
class="classname">Exception</span>异常.

### 范例

**示例 \#1 Catching errors when instantiating <span
class="classname">DateTimeZone</span>**

``` php
<?php
// Error handling by catching exceptions
$timezones = array('Europe/London', 'Mars/Phobos', 'Jupiter/Europa');

foreach ($timezones as $tz) {
    try {
        $mars = new DateTimeZone($tz);
    } catch(Exception $e) {
        echo $e->getMessage() . '<br />';
    }
}
?>
```

以上例程会输出：

    DateTimeZone::__construct() [datetimezone.--construct]: Unknown or bad timezone (Mars/Phobos)
    DateTimeZone::__construct() [datetimezone.--construct]: Unknown or bad timezone (Jupiter/Europa)

DateTimeZone::getLocation
=========================

timezone\_location\_get
=======================

返回与时区相关的定位信息。

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">DateTimeZone::getLocation</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">array</span> <span
class="methodname">timezone\_location\_get</span> ( <span
class="methodparam"><span class="type">DateTimeZone</span>
`$object`</span> )

返回与时区相关的定位信息，包括国家代码，纬度/经度和解释。

### 参数

` object`  
仅过程化风格：由 <span class="function">timezone\_open</span> 返回的
<span class="classname">DateTimeZone</span> 对象。

### 返回值

数组，包含与时区相关的定位信息。

### 范例

**示例 \#1 <span class="function">DateTimeZone::getLocation</span>
函数的范例：**

``` php
<?php
$tz = new DateTimeZone("Europe/Prague");
print_r($tz->getLocation());
print_r(timezone_location_get($tz));
?>
```

以上例程会输出：

    Array
    (
        [country_code] => CZ
        [latitude] => 50.08333
        [longitude] => 14.43333
        [comments] => 
    )
    Array
    (
        [country_code] => CZ
        [latitude] => 50.08333
        [longitude] => 14.43333
        [comments] => 
    )

DateTimeZone::getName
=====================

timezone\_name\_get
===================

返回时区名称。

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DateTimeZone::getName</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">timezone\_name\_get</span> ( <span
class="methodparam"><span class="type">DateTimeZone</span>
`$object`</span> )

返回时区名称。

### 参数

`object`  
<span class="classname">DateTimeZone</span>对象。

### 返回值

<a href="/timezones.html" class="link">时区名称</a>列表之一。

DateTimeZone::getOffset
=======================

timezone\_offset\_get
=====================

返回相对于 GMT 的时差。

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DateTimeZone::getOffset</span> ( <span
class="methodparam"><span class="type">DateTime</span>
`$datetime`</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">timezone\_offset\_get</span> ( <span
class="methodparam"><span class="type">DateTimeZone</span>
`$object`</span> , <span class="methodparam"><span
class="type">DateTime</span> `$datetime`</span> )

该函数返回 `datetime`日期 相对于 GMT 的时差。 GMT 时差是通过
DateTimeZone 对象的时区信息计算出来的。

### 参数

` object`  
仅过程化风格：由 <span class="function">timezone\_open</span> 返回的
<span class="classname">DateTimeZone</span> 对象。

`datetime`  
用来计算时差的日期对象。

### 返回值

成功时返回精确到秒的时差， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">DateTimeZone::getOffset</span> 例子**

``` php
<?php
// Create two timezone objects, one for Taipei (Taiwan) and one for
// Tokyo (Japan)
$dateTimeZoneTaipei = new DateTimeZone("Asia/Taipei");
$dateTimeZoneJapan = new DateTimeZone("Asia/Tokyo");

// Create two DateTime objects that will contain the same Unix timestamp, but
// have different timezones attached to them.
$dateTimeTaipei = new DateTime("now", $dateTimeZoneTaipei);
$dateTimeJapan = new DateTime("now", $dateTimeZoneJapan);

// Calculate the GMT offset for the date/time contained in the $dateTimeTaipei
// object, but using the timezone rules as defined for Tokyo
// ($dateTimeZoneJapan).
$timeOffset = $dateTimeZoneJapan->getOffset($dateTimeTaipei);

// Should show int(32400) (for dates after Sat Sep 8 01:00:00 1951 JST).
var_dump($timeOffset);
?>
```

DateTimeZone::getTransitions
============================

timezone\_transitions\_get
==========================

Returns all transitions for the timezone

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">false</span></span> <span
class="methodname">DateTimeZone::getTransitions</span> (\[ <span
class="methodparam"><span class="type">int</span> `$timestampBegin`<span
class="initializer"> = **`PHP_INT_MIN`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$timestampEnd`<span
class="initializer"> = **`PHP_INT_MAX`**</span></span> \]\] )

过程化风格

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">timezone\_transitions\_get</span> ( <span
class="methodparam"><span class="type">DateTimeZone</span>
`$object`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timestampBegin`<span class="initializer"> =
**`PHP_INT_MIN`**</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$timestampEnd`<span class="initializer"> =
**`PHP_INT_MAX`**</span></span> \]\] )

### 参数

` object`  
仅过程化风格：由 <span class="function">timezone\_open</span> 返回的
<span class="classname">DateTimeZone</span> 对象。

`timestampBegin`  
Begin timestamp.

`timestampEnd`  
End timestamp.

### 返回值

Returns a numerically indexed array of transition arrays on success,
或者在失败时返回 **`false`**.

| Key      | Type                             | Description                                  |
|----------|----------------------------------|----------------------------------------------|
| *ts*     | <span class="type">int</span>    | Unix timestamp                               |
| *time*   | <span class="type">string</span> | **`DateTimeInterface::ISO8601`** time string |
| *offset* | <span class="type">int</span>    | Offset to UTC in seconds                     |
| *isdst*  | <span class="type">bool</span>   | Whether daylight saving time is active       |
| *abbr*   | <span class="type">string</span> | Timezone abbreviation                        |

### 范例

**示例 \#1 A <span class="function">timezone\_transitions\_get</span>
example**

``` php
<?php
$timezone = new DateTimeZone("Europe/London");
$transitions = $timezone->getTransitions();
print_r(array_slice($transitions, 0, 3));
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => Array
            (
                [ts] => -9223372036854775808
                [time] => -292277022657-01-27T08:29:52+0000
                [offset] => 3600
                [isdst] => 1
                [abbr] => BST
            )

        [1] => Array
            (
                [ts] => -1691964000
                [time] => 1916-05-21T02:00:00+0000
                [offset] => 3600
                [isdst] => 1
                [abbr] => BST
            )

        [2] => Array
            (
                [ts] => -1680472800
                [time] => 1916-10-01T02:00:00+0000
                [offset] => 0
                [isdst] => 
                [abbr] => GMT
            )

    )

DateTimeZone::listAbbreviations
===============================

timezone\_abbreviations\_list
=============================

返回一个包含 dst (夏令时)，时差和时区信息的关联数组。

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">DateTimeZone::listAbbreviations</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">array</span> <span
class="methodname">timezone\_abbreviations\_list</span> ( <span
class="methodparam">void</span> )

### 返回值

成功，返回数组， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">timezone\_abbreviations\_list</span>
函数的范例：**

``` php
<?php
$timezone_abbreviations = DateTimeZone::listAbbreviations();
print_r($timezone_abbreviations["acst"]);
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => Array
            (
                [dst] => 1
                [offset] => -14400
                [timezone_id] => America/Porto_Acre
            )

        [1] => Array
            (
                [dst] => 1
                [offset] => -14400
                [timezone_id] => America/Eirunepe
            )

        [2] => Array
            (
                [dst] => 1
                [offset] => -14400
                [timezone_id] => America/Rio_Branco
            )

        [3] => Array
            (
                [dst] => 1
                [offset] => -14400
                [timezone_id] => Brazil/Acre
            )

    )

### 参见

-   <span class="function">timezone\_identifiers\_list</span>

DateTimeZone::listIdentifiers
=============================

timezone\_identifiers\_list
===========================

返回一个包含了所有时区标示符的索引数组。

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">DateTimeZone::listIdentifiers</span> (\[ <span
class="methodparam"><span class="type">int</span> `$what`<span
class="initializer"> = DateTimeZone::ALL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$country`<span
class="initializer"> = **`null`**</span></span> \]\] )

过程化风格

<span class="type">array</span> <span
class="methodname">timezone\_identifiers\_list</span> (\[ <span
class="methodparam"><span class="type">int</span> `$what`<span
class="initializer"> = DateTimeZone::ALL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$country`<span
class="initializer"> = **`null`**</span></span> \]\] )

### 参数

`what`  
<span class="classname">DateTimeZone</span> 类中的常量之一。

`country`  
由两个字母组成，ISO 3166-1 兼容的国家代码。

> **Note**: <span class="simpara"> 只有当 `what`
> 被设置为**`DateTimeZone::PER_COUNTRY`**时,该选项才会被使用。 </span>

### 返回值

成功，返回数组，失败则返回**`false`**.

### 更新日志

| 版本  | 说明                                  |
|-------|---------------------------------------|
| 5.3.0 | 添加可选的 `what` 和 `country` 参数。 |

### 范例

**示例 \#1 <span class="function">timezone\_identifiers\_list</span>
函数的范例：**

``` php
<?php
$timezone_identifiers = DateTimeZone::listIdentifiers();
for ($i=0; $i < 5; $i++) {
    echo "$timezone_identifiers[$i]\n";
}
?>
```

以上例程的输出类似于：

    Africa/Abidjan
    Africa/Accra
    Africa/Addis_Ababa
    Africa/Algiers
    Africa/Asmara

### 参见

-   <span class="function">timezone\_abbreviations\_list</span>

简介
----

表示一个时间周期的类。

一个时间周期表示固定量的时间（多少年，月，天，小时等），
也可以表示一个字符串格式的相对时间， 当表示相对时间的时候，字符串格式是
<span class="classname">DateTime</span> 类的构造函数所支持的格式。

类摘要
------

**DateInterval**

<span class="ooclass"> class **DateInterval** </span> {

/\* 属性 \*/

<span class="modifier">public</span> <span class="type">integer</span>
`$y` ;

<span class="modifier">public</span> <span class="type">integer</span>
`$m` ;

<span class="modifier">public</span> <span class="type">integer</span>
`$d` ;

<span class="modifier">public</span> <span class="type">integer</span>
`$h` ;

<span class="modifier">public</span> <span class="type">integer</span>
`$i` ;

<span class="modifier">public</span> <span class="type">integer</span>
`$s` ;

<span class="modifier">public</span> <span class="type">float</span>
`$f` ;

<span class="modifier">public</span> <span class="type">integer</span>
`$invert` ;

<span class="modifier">public</span> <span class="type">mixed</span>
`$days` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$duration`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">DateInterval</span>
<span class="methodname">createFromDateString</span> ( <span
class="methodparam"><span class="type">string</span> `$datetime`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">format</span> ( <span class="methodparam"><span
class="type">string</span> `$format`</span> )

}

属性
----

`y`  
多少年。

`m`  
多少月。

`d`  
多少天。

`h`  
多少小时。

`i`  
多少分钟。

`s`  
多少秒。

`f`  
多少微秒。

`invert`  
*1* 表示一个负的时间周期， *0* 表示一个正的时间周期。 请参见： <span
class="methodname">DateInterval::format</span>.

`days`  
如果 DateInterval 对象是由 <span class="function">DateTime::diff</span>
函数创建的， 那么它表示开始日期和结束日期之间包含了多少天。 否则，`days`
属性为 **`false`**。

在 PHP 5.4.20/5.5.4 之前版本中，此属性不会为 **`false`**， 而是 -99999。

更新日志
--------

| 版本  | 说明            |
|-------|-----------------|
| 7.1.0 | 增加 `f` 属性。 |

DateInterval::\_\_construct
===========================

Creates a new DateInterval object

### 说明

<span class="modifier">public</span> <span
class="methodname">DateInterval::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$duration`</span>
)

Creates a new DateInterval object.

### 参数

`duration`  
An interval specification.

The format starts with the letter *P*, for “period.” Each duration
period is represented by an integer value followed by a period
designator. If the duration contains time elements, that portion of the
specification is preceded by the letter *T*.

| Period Designator | Description                                                            |
|-------------------|------------------------------------------------------------------------|
| *Y*               | years                                                                  |
| *M*               | months                                                                 |
| *D*               | days                                                                   |
| *W*               | weeks. These get converted into days, so can not be combined with *D*. |
| *H*               | hours                                                                  |
| *M*               | minutes                                                                |
| *S*               | seconds                                                                |

Here are some simple examples. Two days is *P2D*. Two seconds is *PT2S*.
Six years and five minutes is *P6YT5M*.

> **Note**:
>
> The unit types must be entered from the largest scale unit on the left
> to the smallest scale unit on the right. So years before months,
> months before days, days before minutes, etc. Thus one year and four
> days must be represented as *P1Y4D*, not *P4D1Y*.

The specification can also be represented as a date time. A sample of
one year and four days would be *P0001-00-04T00:00:00*. But the values
in this format can not exceed a given period's roll-over-point (e.g.
*25* hours is invalid).

These formats are based on the
<a href="http://en.wikipedia.org/wiki/Iso8601#Durations" class="link external">» ISO 8601 duration specification</a>.

### 错误／异常

Throws an <span class="classname">Exception</span> when the `duration`
cannot be parsed as an interval.

### 范例

**示例 \#1 <span class="classname">DateInterval</span> example**

``` php
<?php

$interval = new DateInterval('P2Y4DT6H8M');
var_dump($interval);

?>
```

以上例程会输出：

    object(DateInterval)#1 (8) {
      ["y"]=>
      int(2)
      ["m"]=>
      int(0)
      ["d"]=>
      int(4)
      ["h"]=>
      int(6)
      ["i"]=>
      int(8)
      ["s"]=>
      int(0)
      ["invert"]=>
      int(0)
      ["days"]=>
      bool(false)
    }

### 参见

-   <span class="function">DateInterval::format</span>
-   <span class="function">DateTime::add</span>
-   <span class="function">DateTime::sub</span>
-   <span class="function">DateTime::diff</span>

DateInterval::createFromDateString
==================================

Sets up a DateInterval from the relative parts of the string

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">DateInterval</span>
<span class="methodname">DateInterval::createFromDateString</span> (
<span class="methodparam"><span class="type">string</span>
`$datetime`</span> )

Uses the normal date parsers and sets up a DateInterval from the
relative parts of the parsed string.

### 参数

`datetime`  
A date with relative parts. Specifically, the
<a href="/datetime/formats.html#Relative%20Formats" class="link">relative formats</a>
supported by the parser used for <span class="function">strtotime</span>
and <span class="classname">DateTime</span> will be used to construct
the DateInterval.

### 范例

**示例 \#1 Parsing valid date intervals**

``` php
<?php
// Each set of intervals is equal.
$i = new DateInterval('P1D');
$i = DateInterval::createFromDateString('1 day');

$i = new DateInterval('P2W');
$i = DateInterval::createFromDateString('2 weeks');

$i = new DateInterval('P3M');
$i = DateInterval::createFromDateString('3 months');

$i = new DateInterval('P4Y');
$i = DateInterval::createFromDateString('4 years');

$i = new DateInterval('P1Y1D');
$i = DateInterval::createFromDateString('1 year + 1 day');

$i = new DateInterval('P1DT12H');
$i = DateInterval::createFromDateString('1 day + 12 hours');

$i = new DateInterval('PT3600S');
$i = DateInterval::createFromDateString('3600 seconds');
?>
```

### 返回值

Returns a new <span class="classname">DateInterval</span> instance.

DateInterval::format
====================

Formats the interval

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DateInterval::format</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> )

Formats the interval.

### 参数

`format`  
| `format` character | Description                                                                                                   | Example values               |
|--------------------|---------------------------------------------------------------------------------------------------------------|------------------------------|
| *%*                | Literal *%*                                                                                                   | *%*                          |
| *Y*                | Years, numeric, at least 2 digits with leading 0                                                              | *01*, *03*                   |
| *y*                | Years, numeric                                                                                                | *1*, *3*                     |
| *M*                | Months, numeric, at least 2 digits with leading 0                                                             | *01*, *03*, *12*             |
| *m*                | Months, numeric                                                                                               | *1*, *3*, *12*               |
| *D*                | Days, numeric, at least 2 digits with leading 0                                                               | *01*, *03*, *31*             |
| *d*                | Days, numeric                                                                                                 | *1*, *3*, *31*               |
| *a*                | Total number of days as a result of a <span class="methodname">DateTime::diff</span> or *(unknown)* otherwise | *4*, *18*, *8123*            |
| *H*                | Hours, numeric, at least 2 digits with leading 0                                                              | *01*, *03*, *23*             |
| *h*                | Hours, numeric                                                                                                | *1*, *3*, *23*               |
| *I*                | Minutes, numeric, at least 2 digits with leading 0                                                            | *01*, *03*, *59*             |
| *i*                | Minutes, numeric                                                                                              | *1*, *3*, *59*               |
| *S*                | Seconds, numeric, at least 2 digits with leading 0                                                            | *01*, *03*, *57*             |
| *s*                | Seconds, numeric                                                                                              | *1*, *3*, *57*               |
| *F*                | Microseconds, numeric, at least 6 digits with leading 0                                                       | *007701*, *052738*, *428291* |
| *f*                | Microseconds, numeric                                                                                         | *7701*, *52738*, *428291*    |
| *R*                | Sign "*-*" when negative, "*+*" when positive                                                                 | *-*, *+*                     |
| *r*                | Sign "*-*" when negative, empty when positive                                                                 | *-*,                         |

### 返回值

Returns the formatted interval.

### 注释

> **Note**:
>
> The <span class="methodname">DateInterval::format</span> method does
> not recalculate carry over points in time strings nor in date
> segments. This is expected because it is not possible to overflow
> values like *"32 days"* which could be interpreted as anything from
> *"1 month and 4 days"* to *"1 month and 1 day"*.

### 更新日志

| 版本  | 说明                                          |
|-------|-----------------------------------------------|
| 7.1.0 | The *F* and *f* format characters were added. |

### 范例

**示例 \#1 <span class="classname">DateInterval</span> example**

``` php
<?php

$interval = new DateInterval('P2Y4DT6H8M');
echo $interval->format('%d days');

?>
```

以上例程会输出：

    4 days

**示例 \#2 <span class="classname">DateInterval</span> and carry over
points**

``` php
<?php

$interval = new DateInterval('P32D');
echo $interval->format('%d days');

?>
```

以上例程会输出：

    32 days

**示例 \#3 <span class="classname">DateInterval</span> and <span
class="methodname">DateTime::diff</span> with the %a and %d modifiers**

``` php
<?php

$january = new DateTime('2010-01-01');
$february = new DateTime('2010-02-01');
$interval = $february->diff($january);

// %a will output the total number of days.
echo $interval->format('%a total days')."\n";

// While %d will only output the number of days not already covered by the
// month.
echo $interval->format('%m month, %d days');

?>
```

以上例程会输出：

    31 total days
    1 month, 0 days

### 参见

-   <span class="methodname">DateTime::diff</span>

简介
----

DatePeriod 类表示一个时间周期。

一个时间周期可以用来在给定的一段时间之内， 以一定的时间间隔进行迭代。

类摘要
------

**DatePeriod**

<span class="ooclass"> class **DatePeriod** </span> <span
class="oointerface">implements <span
class="interfacename">Traversable</span> </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`DatePeriod::EXCLUDE_START_DATE` <span class="initializer"> = 1</span> ;

/\* 属性 \*/

<span class="modifier">public</span> <span class="type">integer</span>
`$recurrences` ;

<span class="modifier">public</span> <span class="type">boolean</span>
`$include_start_date` ;

<span class="modifier">public</span> <span
class="type">DateTimeInterface</span> `$start` ;

<span class="modifier">public</span> <span
class="type">DateTimeInterface</span> `$current` ;

<span class="modifier">public</span> <span
class="type">DateTimeInterface</span> `$end` ;

<span class="modifier">public</span> <span
class="type">DateInterval</span> `$interval` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$start`</span> , <span class="methodparam"><span
class="type">DateInterval</span> `$interval`</span> , <span
class="methodparam"><span class="type">int</span> `$recurrences`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`</span> \] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$start`</span> , <span class="methodparam"><span
class="type">DateInterval</span> `$interval`</span> , <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$end`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`</span> \] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$isostr`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`</span> \] )

<span class="modifier">public</span> <span
class="type">DateInterval</span> <span
class="methodname">getDateInterval</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">DateTimeInterface</span> <span
class="methodname">getEndDate</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getRecurrences</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">DateTimeInterface</span> <span
class="methodname">getStartDate</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`DatePeriod::EXCLUDE_START_DATE`**  
在 <span class="function">DatePeriod::\_\_construct</span>
构造函数中使用，表示不包含开始时间。

属性
----

`recurrences`  
如果通过显式的传入 *$recurrences* 来创建的 <span
class="classname">DatePeriod</span> 实例， 那么这个参数表示循环次数。
参见： <span class="methodname">DatePeriod::getRecurrences</span>。

`include_start_date`  
在循环过程中，是否包含开始时间。

`start`  
时间周期的开始时间。

`current`  
表示在时间周期内迭代的时候，当前的时间。

`end`  
时间周期的结束时间。

`interval`  
ISO 8601 格式的间隔。

更新日志
--------

| 版本           | 说明                                                                                           |
|----------------|------------------------------------------------------------------------------------------------|
| 5.3.27, 5.4.17 | 公开以下属性：`recurrences`， `include_start_date`，`start`， `current`，`end` 和 `interval`。 |

DatePeriod::\_\_construct
=========================

Creates a new DatePeriod object

### 说明

<span class="modifier">public</span> <span
class="methodname">DatePeriod::\_\_construct</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$start`</span> , <span class="methodparam"><span
class="type">DateInterval</span> `$interval`</span> , <span
class="methodparam"><span class="type">int</span> `$recurrences`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`</span> \] )

<span class="modifier">public</span> <span
class="methodname">DatePeriod::\_\_construct</span> ( <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$start`</span> , <span class="methodparam"><span
class="type">DateInterval</span> `$interval`</span> , <span
class="methodparam"><span class="type">DateTimeInterface</span>
`$end`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`</span> \] )

<span class="modifier">public</span> <span
class="methodname">DatePeriod::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$isostr`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`</span> \] )

Creates a new DatePeriod object.

### 参数

`start`  
The start date of the period.

`interval`  
The interval between recurrences within the period.

`recurrences`  
The number of recurrences.

`end`  
The end date of the period.

`isostr`  
An ISO 8601 repeating interval specification.

`options`  
Can be set to **`DatePeriod::EXCLUDE_START_DATE`** to exclude the start
date from the set of recurring dates within the period.

### 更新日志

| 版本  | 说明                                                                                                                               |
|-------|------------------------------------------------------------------------------------------------------------------------------------|
| 5.5.8 | `end` type changed to <span class="interfacename">DateTimeInterface</span>. Previously, <span class="classname">DateTime</span>.   |
| 5.5.0 | `start` type changed to <span class="interfacename">DateTimeInterface</span>. Previously, <span class="classname">DateTime</span>. |

### 范例

**示例 \#1 DatePeriod example**

``` php
<?php
$start = new DateTime('2012-07-01');
$interval = new DateInterval('P7D');
$end = new DateTime('2012-07-31');
$recurrences = 4;
$iso = 'R4/2012-07-01T00:00:00Z/P7D';

// All of these periods are equivalent.
$period = new DatePeriod($start, $interval, $recurrences);
$period = new DatePeriod($start, $interval, $end);
$period = new DatePeriod($iso);

// By iterating over the DatePeriod object, all of the
// recurring dates within that period are printed.
foreach ($period as $date) {
    echo $date->format('Y-m-d')."\n";
}
?>
```

以上例程会输出：

    2012-07-01
    2012-07-08
    2012-07-15
    2012-07-22
    2012-07-29

**示例 \#2 DatePeriod example with
**`DatePeriod::EXCLUDE_START_DATE`****

``` php
<?php
$start = new DateTime('2012-07-01');
$interval = new DateInterval('P7D');
$end = new DateTime('2012-07-31');

$period = new DatePeriod($start, $interval, $end,
                         DatePeriod::EXCLUDE_START_DATE);

// By iterating over the DatePeriod object, all of the
// recurring dates within that period are printed.
// Note that, in this case, 2012-07-01 is not printed.
foreach ($period as $date) {
    echo $date->format('Y-m-d')."\n";
}
?>
```

以上例程会输出：

    2012-07-08
    2012-07-15
    2012-07-22
    2012-07-29

### 注释

Unbound numbers of repetitions as specified by ISO 8601 section 4.5
"Recurring time interval" are not supported, i.e. neither passing
*"R/..."* as `isostr` nor passing **`null`** as `end` would work.

DatePeriod::getDateInterval
===========================

Gets the interval

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="type">DateInterval</span> <span
class="methodname">DatePeriod::getDateInterval</span> ( <span
class="methodparam">void</span> )

Gets a <span class="classname">DateInterval</span> <span
class="type">object</span> representing the interval used for the
period.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="classname">DateInterval</span> <span
class="type">object</span>

### 范例

**示例 \#1 <span class="methodname">DatePeriod::getDateInterval</span>
example**

``` php
<?php
$period = new DatePeriod('R7/2016-05-16T00:00:00Z/P1D');
$interval = $period->getDateInterval();
echo $interval->format('%d day');
?>
```

以上例程会输出：

    1 day

### 参见

-   <span class="methodname">DatePeriod::getStartDate</span>
-   <span class="methodname">DatePeriod::getEndDate</span>

DatePeriod::getEndDate
======================

Gets the end date

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="type">DateTimeInterface</span> <span
class="methodname">DatePeriod::getEndDate</span> ( <span
class="methodparam">void</span> )

Gets the end date of the period.

### 参数

此函数没有参数。

### 返回值

Returns **`null`** if the <span class="classname">DatePeriod</span> does
not have an end date. For example, when initialized with the
`recurrences` parameter, or the `isostr` parameter without an end date.

Returns a <span class="classname">DateTimeImmutable</span> <span
class="type">object</span> when the <span
class="classname">DatePeriod</span> is initialized with a <span
class="classname">DateTimeImmutable</span> <span
class="type">object</span> as the `end` parameter.

Returns a <span class="classname">DateTime</span> <span
class="type">object</span> otherwise.

### 范例

**示例 \#1 <span class="methodname">DatePeriod::getEndDate</span>
example**

``` php
<?php
$period = new DatePeriod(
    new DateTime('2016-05-16T00:00:00Z'),
    new DateInterval('P1D'),
    new DateTime('2016-05-20T00:00:00Z')
);
$start = $period->getEndDate();
echo $start->format(DateTime::ISO8601);
?>
```

以上例程会输出：

    2016-05-20T00:00:00+0000

**示例 \#2 <span class="methodname">DatePeriod::getEndDate</span>
without an end date**

``` php
<?php
$period = new DatePeriod(
    new DateTime('2016-05-16T00:00:00Z'),
    new DateInterval('P1D'),
    7
);
var_dump($period->getEndDate());
?>
```

以上例程会输出：

    NULL

### 参见

-   <span class="methodname">DatePeriod::getStartDate</span>
-   <span class="methodname">DatePeriod::getDateInterval</span>

DatePeriod::getRecurrences
==========================

Gets the number of recurrences

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DatePeriod::getRecurrences</span> ( <span
class="methodparam">void</span> )

Get the number of recurrences.

### 参数

此函数没有参数。

### 返回值

Returns the number of recurrences.

### 参见

-   <a href="/class/dateperiod.html#" class="link">DatePeriod::$recurrences</a>

DatePeriod::getStartDate
========================

Gets the start date

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="type">DateTimeInterface</span> <span
class="methodname">DatePeriod::getStartDate</span> ( <span
class="methodparam">void</span> )

Gets the start date of the period.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="classname">DateTimeImmutable</span> <span
class="type">object</span> when the <span
class="classname">DatePeriod</span> is initialized with a <span
class="classname">DateTimeImmutable</span> <span
class="type">object</span> as the `start` parameter.

Returns a <span class="classname">DateTime</span> <span
class="type">object</span> otherwise.

### 范例

**示例 \#1 <span class="methodname">DatePeriod::getStartDate</span>
example**

``` php
<?php
$period = new DatePeriod('R7/2016-05-16T00:00:00Z/P1D');
$start = $period->getStartDate();
echo $start->format(DateTime::ISO8601);
?>
```

以上例程会输出：

    2016-05-16T00:00:00+0000

### 参见

-   <span class="methodname">DatePeriod::getEndDate</span>
-   <span class="methodname">DatePeriod::getDateInterval</span>
