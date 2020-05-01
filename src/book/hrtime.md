High resolution timing
======================

**目录**

-   [简介](/intro/hrtime.html)
-   [安装／配置](/hrtime/setup.html)
    -   [安装](/hrtime/setup.html#安装)
-   [范例](/hrtime/examples.html)
    -   [Basic usage](/hrtime/examples.html#Basic%20usage)
-   [HRTime\\PerformanceCounter](/class/hrtime-performancecounter.html)
    — The HRTime\\PerformanceCounter class
    -   [HRTime\\PerformanceCounter::getFrequency](/class/hrtime-performancecounter.html#HRTime\PerformanceCounter::getFrequency)
        — Timer frequency in ticks per second
    -   [HRTime\\PerformanceCounter::getTicks](/class/hrtime-performancecounter.html#HRTime\PerformanceCounter::getTicks)
        — Current ticks from the system
    -   [HRTime\\PerformanceCounter::getTicksSince](/class/hrtime-performancecounter.html#HRTime\PerformanceCounter::getTicksSince)
        — Ticks elapsed since the given value
-   [HRTime\\StopWatch](/class/hrtime-stopwatch.html) — The
    HRTime\\StopWatch class
    -   [HRTime\\StopWatch::getElapsedTicks](/class/hrtime-stopwatch.html#HRTime\StopWatch::getElapsedTicks)
        — Get elapsed ticks for all intervals
    -   [HRTime\\StopWatch::getElapsedTime](/class/hrtime-stopwatch.html#HRTime\StopWatch::getElapsedTime)
        — Get elapsed time for all intervals
    -   [HRTime\\StopWatch::getLastElapsedTicks](/class/hrtime-stopwatch.html#HRTime\StopWatch::getLastElapsedTicks)
        — Get elapsed ticks for the last interval
    -   [HRTime\\StopWatch::getLastElapsedTime](/class/hrtime-stopwatch.html#HRTime\StopWatch::getLastElapsedTime)
        — Get elapsed time for the last interval
    -   [HRTime\\StopWatch::isRunning](/class/hrtime-stopwatch.html#HRTime\StopWatch::isRunning)
        — Whether the measurement is running
    -   [HRTime\\StopWatch::start](/class/hrtime-stopwatch.html#HRTime\StopWatch::start)
        — Start time measurement
    -   [HRTime\\StopWatch::stop](/class/hrtime-stopwatch.html#HRTime\StopWatch::stop)
        — Stop time measurement
-   [HRTime\\Unit](/class/hrtime-unit.html) — The HRTime\\Unit class

简介
----

类摘要
------

**HRTime\\PerformanceCounter**

<span class="ooclass"> class **HRTime\\PerformanceCounter** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getFrequency</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getTicks</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getTicksSince</span> ( <span
class="methodparam"><span class="type">int</span> `$start`</span> )

}

HRTime\\PerformanceCounter::getFrequency
========================================

Timer frequency in ticks per second

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">HRTime\\PerformanceCounter::getFrequency</span> (
<span class="methodparam">void</span> )

Returns the timer frequency in ticks per second. This value is constant
after the system start on almost any operating system.

### 参数

此函数没有参数。

### 返回值

Returns <span class="type">integer</span> indicating the timer
frequency.

HRTime\\PerformanceCounter::getTicks
====================================

Current ticks from the system

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">HRTime\\PerformanceCounter::getTicks</span> ( <span
class="methodparam">void</span> )

Returns the ticks count.

### 参数

此函数没有参数。

### 返回值

Returns <span class="type">integer</span> indicating the ticks count.

HRTime\\PerformanceCounter::getTicksSince
=========================================

Ticks elapsed since the given value

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">HRTime\\PerformanceCounter::getTicksSince</span> (
<span class="methodparam"><span class="type">int</span> `$start`</span>
)

Returns the ticks count elapsed since the given start value.

### 参数

`start`  
Starting ticks value.

### 返回值

Returns <span class="type">integer</span> indicating the ticks count.

简介
----

类摘要
------

**HRTime\\StopWatch**

<span class="ooclass"> class **HRTime\\StopWatch** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**HRTime\\PerformanceCounter** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getElapsedTicks</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">getElapsedTime</span> (\[ <span
class="methodparam"><span class="type">int</span> `$unit`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getLastElapsedTicks</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">getLastElapsedTime</span> (\[ <span
class="methodparam"><span class="type">int</span> `$unit`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isRunning</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">stop</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">HRTime\\PerformanceCounter::getFrequency</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">HRTime\\PerformanceCounter::getTicks</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">HRTime\\PerformanceCounter::getTicksSince</span> (
<span class="methodparam"><span class="type">int</span> `$start`</span>
)

}

HRTime\\StopWatch::getElapsedTicks
==================================

Get elapsed ticks for all intervals

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">HRTime\\StopWatch::getElapsedTicks</span> ( <span
class="methodparam">void</span> )

Get elapsed ticks for all the previously closed intervals.

### 参数

此函数没有参数。

### 返回值

Returns <span class="type">integer</span> indicating elapsed ticks.

HRTime\\StopWatch::getElapsedTime
=================================

Get elapsed time for all intervals

### 说明

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">HRTime\\StopWatch::getElapsedTime</span> (\[
<span class="methodparam"><span class="type">int</span> `$unit`</span>
\] )

Get elapsed time for all the previously closed intervals.

### 参数

`unit`  
Time unit represented by a HRTime\\Unit constant. Default is
HRTime\\Unit::SECOND.

### 返回值

Returns <span class="type">float</span> indicating elapsed time.

HRTime\\StopWatch::getLastElapsedTicks
======================================

Get elapsed ticks for the last interval

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">HRTime\\StopWatch::getLastElapsedTicks</span> ( <span
class="methodparam">void</span> )

Get elapsed ticks for the previously closed interval.

### 参数

此函数没有参数。

### 返回值

Returns <span class="type">integer</span> indicating elapsed ticks.

HRTime\\StopWatch::getLastElapsedTime
=====================================

Get elapsed time for the last interval

### 说明

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">HRTime\\StopWatch::getLastElapsedTime</span>
(\[ <span class="methodparam"><span class="type">int</span>
`$unit`</span> \] )

Get elapsed time for the previously closed interval.

### 参数

`unit`  
Time unit represented by a HRTime\\Unit constant. Default is
HRTime\\Unit::SECOND.

### 返回值

Returns <span class="type">float</span> indicating elapsed time.

HRTime\\StopWatch::isRunning
============================

Whether the measurement is running

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">HRTime\\StopWatch::isRunning</span> ( <span
class="methodparam">void</span> )

Reveals whether the measurement was started.

### 参数

此函数没有参数。

### 返回值

Returns <span class="type">boolean</span> indicating whetehr the
measurement is running.

HRTime\\StopWatch::start
========================

Start time measurement

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">HRTime\\StopWatch::start</span> ( <span
class="methodparam">void</span> )

Starts the time measurement. It has no effect if the measurement was
already started. The measurement will be continued if it was previously
stopped.

### 参数

此函数没有参数。

### 返回值

Returns void.

HRTime\\StopWatch::stop
=======================

Stop time measurement

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">HRTime\\StopWatch::stop</span> ( <span
class="methodparam">void</span> )

Stop the time measurement for the previously started interval.

### 参数

此函数没有参数。

### 返回值

Returns void.

简介
----

类摘要
------

**HRTime\\Unit**

<span class="ooclass"> class **HRTime\\Unit** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`HRTime\Unit::SECOND` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`HRTime\Unit::MILLISECOND` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`HRTime\Unit::MICROSECOND` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`HRTime\Unit::NANOSECOND` <span class="initializer"> = 3</span> ;

/\* 方法 \*/

}

预定义常量
----------

**`HRTime\Unit::SECOND`**  

**`HRTime\Unit::MILLISECOND`**  

**`HRTime\Unit::MICROSECOND`**  

**`HRTime\Unit::NANOSECOND`**  
