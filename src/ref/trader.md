trader\_acos
============

Vector Trigonometric ACos

### 说明

<span class="type">array</span> <span
class="methodname">trader\_acos</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> )

Calculates the arc cosine for each value in `real` and returns the
resulting array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_ad
==========

Chaikin A/D Line

### 说明

<span class="type">array</span> <span
class="methodname">trader\_ad</span> ( <span class="methodparam"><span
class="type">array</span> `$high`</span> , <span
class="methodparam"><span class="type">array</span> `$low`</span> ,
<span class="methodparam"><span class="type">array</span>
`$close`</span> , <span class="methodparam"><span
class="type">array</span> `$volume`</span> )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`volume`  
成交量，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_add
===========

Vector Arithmetic Add

### 说明

<span class="type">array</span> <span
class="methodname">trader\_add</span> ( <span class="methodparam"><span
class="type">array</span> `$real0`</span> , <span
class="methodparam"><span class="type">array</span> `$real1`</span> )

Calculates the vector addition of `real0` to `real1` and returns the
resulting vector.

### 参数

`real0`  
浮点数数组。

`real1`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_adosc
=============

Chaikin A/D Oscillator

### 说明

<span class="type">array</span> <span
class="methodname">trader\_adosc</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
, <span class="methodparam"><span class="type">array</span>
`$close`</span> , <span class="methodparam"><span
class="type">array</span> `$volume`</span> \[, <span
class="methodparam"><span class="type">int</span> `$fastPeriod`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$slowPeriod`</span> \]\] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`volume`  
成交量，浮点数数组。

`fastPeriod`  
Number of period for the fast MA. Valid range from 2 to 100000.

`slowPeriod`  
Number of period for the slow MA. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_adx
===========

Average Directional Movement Index

### 说明

<span class="type">array</span> <span
class="methodname">trader\_adx</span> ( <span class="methodparam"><span
class="type">array</span> `$high`</span> , <span
class="methodparam"><span class="type">array</span> `$low`</span> ,
<span class="methodparam"><span class="type">array</span>
`$close`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_adxr
============

Average Directional Movement Index Rating

### 说明

<span class="type">array</span> <span
class="methodname">trader\_adxr</span> ( <span class="methodparam"><span
class="type">array</span> `$high`</span> , <span
class="methodparam"><span class="type">array</span> `$low`</span> ,
<span class="methodparam"><span class="type">array</span>
`$close`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_apo
===========

Absolute Price Oscillator

### 说明

<span class="type">array</span> <span
class="methodname">trader\_apo</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$fastPeriod`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$slowPeriod`</span> \[, <span class="methodparam"><span
class="type">int</span> `$mAType`</span> \]\]\] )

### 参数

`real`  
浮点数数组。

`fastPeriod`  
Number of period for the fast MA. Valid range from 2 to 100000.

`slowPeriod`  
Number of period for the slow MA. Valid range from 2 to 100000.

`mAType`  
Type of Moving Average.
<a href="/trader/constants.html" class="link">TRADER_MA_TYPE_*</a>
series of constants should be used.

### 返回值

Returns an array with calculated data or false on failure.

trader\_aroon
=============

Aroon

### 说明

<span class="type">array</span> <span
class="methodname">trader\_aroon</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_aroonosc
================

Aroon Oscillator

### 说明

<span class="type">array</span> <span
class="methodname">trader\_aroonosc</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_asin
============

Vector Trigonometric ASin

### 说明

<span class="type">array</span> <span
class="methodname">trader\_asin</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> )

Calculates the arc sine for each value in `real` and returns the
resulting array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_atan
============

Vector Trigonometric ATan

### 说明

<span class="type">array</span> <span
class="methodname">trader\_atan</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> )

Calculates the arc tangent for each value in `real` and returns the
resulting array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_atr
===========

Average True Range

### 说明

<span class="type">array</span> <span
class="methodname">trader\_atr</span> ( <span class="methodparam"><span
class="type">array</span> `$high`</span> , <span
class="methodparam"><span class="type">array</span> `$low`</span> ,
<span class="methodparam"><span class="type">array</span>
`$close`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_avgprice
================

Average Price

### 说明

<span class="type">array</span> <span
class="methodname">trader\_avgprice</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_bbands
==============

Bollinger Bands

### 说明

<span class="type">array</span> <span
class="methodname">trader\_bbands</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \[, <span class="methodparam"><span
class="type">float</span> `$nbDevUp`</span> \[, <span
class="methodparam"><span class="type">float</span> `$nbDevDn`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$mAType`</span> \]\]\]\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

`nbDevUp`  
Deviation multiplier for upper band. Valid range from
<a href="/trader/constants.html#" class="link">TRADER_REAL_MIN</a> to
<a href="/trader/constants.html#" class="link">TRADER_REAL_MAX</a>.

`nbDevDn`  
Deviation multiplier for lower band. Valid range from
<a href="/trader/constants.html#" class="link">TRADER_REAL_MIN</a> to
<a href="/trader/constants.html#" class="link">TRADER_REAL_MAX</a>.

`mAType`  
Type of Moving Average.
<a href="/trader/constants.html" class="link">TRADER_MA_TYPE_*</a>
series of constants should be used.

### 返回值

Returns an array with calculated data or false on failure.

trader\_beta
============

Beta

### 说明

<span class="type">array</span> <span
class="methodname">trader\_beta</span> ( <span class="methodparam"><span
class="type">array</span> `$real0`</span> , <span
class="methodparam"><span class="type">array</span> `$real1`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`real0`  
浮点数数组。

`real1`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_bop
===========

Balance Of Power

### 说明

<span class="type">array</span> <span
class="methodname">trader\_bop</span> ( <span class="methodparam"><span
class="type">array</span> `$open`</span> , <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
, <span class="methodparam"><span class="type">array</span>
`$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cci
===========

Commodity Channel Index

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cci</span> ( <span class="methodparam"><span
class="type">array</span> `$high`</span> , <span
class="methodparam"><span class="type">array</span> `$low`</span> ,
<span class="methodparam"><span class="type">array</span>
`$close`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdl2crows
=================

Two Crows

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdl2crows</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdl3blackcrows
======================

Three Black Crows

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdl3blackcrows</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdl3inside
==================

Three Inside Up/Down

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdl3inside</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdl3linestrike
======================

Three-Line Strike

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdl3linestrike</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdl3outside
===================

Three Outside Up/Down

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdl3outside</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdl3starsinsouth
========================

Three Stars In The South

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdl3starsinsouth</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdl3whitesoldiers
=========================

Three Advancing White Soldiers

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdl3whitesoldiers</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlabandonedbaby
========================

Abandoned Baby

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlabandonedbaby</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> \[, <span
class="methodparam"><span class="type">float</span>
`$penetration`</span> \] )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`penetration`  
一个烛台渗入到另一个烛台的百分比。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdladvanceblock
=======================

Advance Block

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdladvanceblock</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlbelthold
===================

Belt-hold

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlbelthold</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlbreakaway
====================

Breakaway

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlbreakaway</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlclosingmarubozu
==========================

Closing Marubozu

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlclosingmarubozu</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlconcealbabyswall
===========================

Concealing Baby Swallow

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlconcealbabyswall</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlcounterattack
========================

Counterattack

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlcounterattack</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdldarkcloudcover
=========================

Dark Cloud Cover

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdldarkcloudcover</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> \[, <span
class="methodparam"><span class="type">float</span>
`$penetration`</span> \] )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`penetration`  
一个烛台渗入到另一个烛台的百分比。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdldoji
===============

Doji

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdldoji</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdldojistar
===================

Doji Star

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdldojistar</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdldragonflydoji
========================

Dragonfly Doji

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdldragonflydoji</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlengulfing
====================

Engulfing Pattern

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlengulfing</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdleveningdojistar
==========================

Evening Doji Star

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdleveningdojistar</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> \[, <span
class="methodparam"><span class="type">float</span>
`$penetration`</span> \] )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`penetration`  
一个烛台渗入到另一个烛台的百分比。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdleveningstar
======================

Evening Star

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdleveningstar</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> \[, <span
class="methodparam"><span class="type">float</span>
`$penetration`</span> \] )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`penetration`  
一个烛台渗入到另一个烛台的百分比。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlgapsidesidewhite
===========================

Up/Down-gap side-by-side white lines

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlgapsidesidewhite</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlgravestonedoji
=========================

Gravestone Doji

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlgravestonedoji</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlhammer
=================

Hammer

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlhammer</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlhangingman
=====================

Hanging Man

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlhangingman</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlharami
=================

Harami Pattern

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlharami</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlharamicross
======================

Harami Cross Pattern

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlharamicross</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlhighwave
===================

High-Wave Candle

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlhighwave</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlhikkake
==================

Hikkake Pattern

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlhikkake</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlhikkakemod
=====================

Modified Hikkake Pattern

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlhikkakemod</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlhomingpigeon
=======================

Homing Pigeon

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlhomingpigeon</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlidentical3crows
==========================

Identical Three Crows

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlidentical3crows</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlinneck
=================

In-Neck Pattern

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlinneck</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlinvertedhammer
=========================

Inverted Hammer

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlinvertedhammer</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlkicking
==================

Kicking

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlkicking</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlkickingbylength
==========================

Kicking - bull/bear determined by the longer marubozu

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlkickingbylength</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlladderbottom
=======================

Ladder Bottom

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlladderbottom</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdllongleggeddoji
=========================

Long Legged Doji

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdllongleggeddoji</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdllongline
===================

Long Line Candle

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdllongline</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlmarubozu
===================

Marubozu

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlmarubozu</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlmatchinglow
======================

Matching Low

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlmatchinglow</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlmathold
==================

Mat Hold

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlmathold</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> \[, <span
class="methodparam"><span class="type">float</span>
`$penetration`</span> \] )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`penetration`  
一个烛台渗入到另一个烛台的百分比。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlmorningdojistar
==========================

Morning Doji Star

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlmorningdojistar</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> \[, <span
class="methodparam"><span class="type">float</span>
`$penetration`</span> \] )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`penetration`  
一个烛台渗入到另一个烛台的百分比。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlmorningstar
======================

Morning Star

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlmorningstar</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> \[, <span
class="methodparam"><span class="type">float</span>
`$penetration`</span> \] )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`penetration`  
一个烛台渗入到另一个烛台的百分比。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlonneck
=================

On-Neck Pattern

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlonneck</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlpiercing
===================

Piercing Pattern

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlpiercing</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlrickshawman
======================

Rickshaw Man

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlrickshawman</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlrisefall3methods
===========================

Rising/Falling Three Methods

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlrisefall3methods</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlseparatinglines
==========================

Separating Lines

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlseparatinglines</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlshootingstar
=======================

Shooting Star

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlshootingstar</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlshortline
====================

Short Line Candle

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlshortline</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlspinningtop
======================

Spinning Top

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlspinningtop</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlstalledpattern
=========================

Stalled Pattern

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlstalledpattern</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlsticksandwich
========================

Stick Sandwich

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlsticksandwich</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdltakuri
=================

Takuri (Dragonfly Doji with very long lower shadow)

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdltakuri</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdltasukigap
====================

Tasuki Gap

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdltasukigap</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlthrusting
====================

Thrusting Pattern

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlthrusting</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdltristar
==================

Tristar Pattern

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdltristar</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlunique3river
=======================

Unique 3 River

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlunique3river</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlupsidegap2crows
==========================

Upside Gap Two Crows

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlupsidegap2crows</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cdlxsidegap3methods
===========================

Upside/Downside Gap Three Methods

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cdlxsidegap3methods</span> ( <span
class="methodparam"><span class="type">array</span> `$open`</span> ,
<span class="methodparam"><span class="type">array</span> `$high`</span>
, <span class="methodparam"><span class="type">array</span>
`$low`</span> , <span class="methodparam"><span
class="type">array</span> `$close`</span> )

### 参数

`open`  
开盘价，浮点数数组。

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_ceil
============

Vector Ceil

### 说明

<span class="type">array</span> <span
class="methodname">trader\_ceil</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> )

Calculates the next highest integer for each value in `real` and returns
the resulting array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cmo
===========

Chande Momentum Oscillator

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cmo</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_correl
==============

Pearson's Correlation Coefficient (r)

### 说明

<span class="type">array</span> <span
class="methodname">trader\_correl</span> ( <span
class="methodparam"><span class="type">array</span> `$real0`</span> ,
<span class="methodparam"><span class="type">array</span>
`$real1`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timePeriod`</span> \] )

### 参数

`real0`  
浮点数数组。

`real1`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_cos
===========

Vector Trigonometric Cos

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cos</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> )

Calculates the cosine for each value in `real` and returns the resulting
array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_cosh
============

Vector Trigonometric Cosh

### 说明

<span class="type">array</span> <span
class="methodname">trader\_cosh</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> )

Calculates the hyperbolic cosine for each value in `real` and returns
the resulting array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_dema
============

Double Exponential Moving Average

### 说明

<span class="type">array</span> <span
class="methodname">trader\_dema</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_div
===========

Vector Arithmetic Div

### 说明

<span class="type">array</span> <span
class="methodname">trader\_div</span> ( <span class="methodparam"><span
class="type">array</span> `$real0`</span> , <span
class="methodparam"><span class="type">array</span> `$real1`</span> )

Divides each value from `real0` by the corresponding value from `real1`
and returns the resulting array.

### 参数

`real0`  
浮点数数组。

`real1`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_dx
==========

Directional Movement Index

### 说明

<span class="type">array</span> <span
class="methodname">trader\_dx</span> ( <span class="methodparam"><span
class="type">array</span> `$high`</span> , <span
class="methodparam"><span class="type">array</span> `$low`</span> ,
<span class="methodparam"><span class="type">array</span>
`$close`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_ema
===========

Exponential Moving Average

### 说明

<span class="type">array</span> <span
class="methodname">trader\_ema</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_errno
=============

Get error code

### 说明

<span class="type">int</span> <span
class="methodname">trader\_errno</span> ( <span
class="methodparam">void</span> )

Get error code of the last operation.

### 返回值

Returns the error code identified by one of the
<a href="/trader/constants.html" class="link">TRADER_ERR_*</a>
constants.

trader\_exp
===========

Vector Arithmetic Exp

### 说明

<span class="type">array</span> <span
class="methodname">trader\_exp</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> )

Calculates **`e`** raised to the power of each value in `real`. Returns
an array with the calculated data.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_floor
=============

Vector Floor

### 说明

<span class="type">array</span> <span
class="methodname">trader\_floor</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> )

Calculates the next lowest integer for each value in `real` and returns
the resulting array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_get\_compat
===================

Get compatibility mode

### 说明

<span class="type">int</span> <span
class="methodname">trader\_get\_compat</span> ( <span
class="methodparam">void</span> )

Get compatibility mode which affects the way calculations are done by
all the extension functions.

### 返回值

Returns the compatibility mode id which can be identified by
<a href="/trader/constants.html" class="link">TRADER_COMPATIBILITY_*</a>
series of constants.

trader\_get\_unstable\_period
=============================

Get unstable period

### 说明

<span class="type">int</span> <span
class="methodname">trader\_get\_unstable\_period</span> ( <span
class="methodparam"><span class="type">int</span> `$functionId`</span> )

Get unstable period factor for a particular function.

### 参数

`functionId`  
Function ID the factor to be read for.
<a href="/trader/constants.html" class="link">TRADER_FUNC_UNST_*</a>
series of constants should be used.

### 返回值

Returns the unstable period factor for the corresponding function.

trader\_ht\_dcperiod
====================

Hilbert Transform - Dominant Cycle Period

### 说明

<span class="type">array</span> <span
class="methodname">trader\_ht\_dcperiod</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> )

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_ht\_dcphase
===================

Hilbert Transform - Dominant Cycle Phase

### 说明

<span class="type">array</span> <span
class="methodname">trader\_ht\_dcphase</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> )

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_ht\_phasor
==================

Hilbert Transform - Phasor Components

### 说明

<span class="type">array</span> <span
class="methodname">trader\_ht\_phasor</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> )

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_ht\_sine
================

Hilbert Transform - SineWave

### 说明

<span class="type">array</span> <span
class="methodname">trader\_ht\_sine</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> )

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_ht\_trendline
=====================

Hilbert Transform - Instantaneous Trendline

### 说明

<span class="type">array</span> <span
class="methodname">trader\_ht\_trendline</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> )

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_ht\_trendmode
=====================

Hilbert Transform - Trend vs Cycle Mode

### 说明

<span class="type">array</span> <span
class="methodname">trader\_ht\_trendmode</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> )

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_kama
============

Kaufman Adaptive Moving Average

### 说明

<span class="type">array</span> <span
class="methodname">trader\_kama</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_linearreg\_angle
========================

Linear Regression Angle

### 说明

<span class="type">array</span> <span
class="methodname">trader\_linearreg\_angle</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_linearreg\_intercept
============================

Linear Regression Intercept

### 说明

<span class="type">array</span> <span
class="methodname">trader\_linearreg\_intercept</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_linearreg\_slope
========================

Linear Regression Slope

### 说明

<span class="type">array</span> <span
class="methodname">trader\_linearreg\_slope</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_linearreg
=================

Linear Regression

### 说明

<span class="type">array</span> <span
class="methodname">trader\_linearreg</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_ln
==========

Vector Log Natural

### 说明

<span class="type">array</span> <span
class="methodname">trader\_ln</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> )

Calculates the natural logarithm for each value in `real` and returns
the resulting array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_log10
=============

Vector Log10

### 说明

<span class="type">array</span> <span
class="methodname">trader\_log10</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> )

Calculates the base-10 logarithm for each value in `real` and returns
the resulting array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_ma
==========

Moving average

### 说明

<span class="type">array</span> <span
class="methodname">trader\_ma</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$mAType`</span> \]\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

`mAType`  
Type of Moving Average.
<a href="/trader/constants.html" class="link">TRADER_MA_TYPE_*</a>
series of constants should be used.

### 返回值

Returns an array with calculated data or false on failure.

trader\_macd
============

Moving Average Convergence/Divergence

### 说明

<span class="type">array</span> <span
class="methodname">trader\_macd</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$fastPeriod`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$slowPeriod`</span> \[, <span class="methodparam"><span
class="type">int</span> `$signalPeriod`</span> \]\]\] )

### 参数

`real`  
浮点数数组。

`fastPeriod`  
Number of period for the fast MA. Valid range from 2 to 100000.

`slowPeriod`  
Number of period for the slow MA. Valid range from 2 to 100000.

`signalPeriod`  
Smoothing for the signal line (nb of period). Valid range from 1
to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_macdext
===============

MACD with controllable MA type

### 说明

<span class="type">array</span> <span
class="methodname">trader\_macdext</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$fastPeriod`</span> \[, <span class="methodparam"><span
class="type">int</span> `$fastMAType`</span> \[, <span
class="methodparam"><span class="type">int</span> `$slowPeriod`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$slowMAType`</span> \[, <span class="methodparam"><span
class="type">int</span> `$signalPeriod`</span> \[, <span
class="methodparam"><span class="type">int</span> `$signalMAType`</span>
\]\]\]\]\]\] )

### 参数

`real`  
浮点数数组。

`fastPeriod`  
Number of period for the fast MA. Valid range from 2 to 100000.

`fastMAType`  
Type of Moving Average for fast MA.
<a href="/trader/constants.html" class="link">TRADER_MA_TYPE_*</a>
series of constants should be used.

`slowPeriod`  
Number of period for the slow MA. Valid range from 2 to 100000.

`slowMAType`  
Type of Moving Average for slow MA.
<a href="/trader/constants.html" class="link">TRADER_MA_TYPE_*</a>
series of constants should be used.

`signalPeriod`  
Smoothing for the signal line (nb of period). Valid range from 1
to 100000.

`signalMAType`  
Type of Moving Average for signal line.
<a href="/trader/constants.html" class="link">TRADER_MA_TYPE_*</a>
series of constants should be used.

### 返回值

Returns an array with calculated data or false on failure.

trader\_macdfix
===============

Moving Average Convergence/Divergence Fix 12/26

### 说明

<span class="type">array</span> <span
class="methodname">trader\_macdfix</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$signalPeriod`</span> \] )

### 参数

`real`  
浮点数数组。

`signalPeriod`  
Smoothing for the signal line (nb of period). Valid range from 1
to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_mama
============

MESA Adaptive Moving Average

### 说明

<span class="type">array</span> <span
class="methodname">trader\_mama</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">float</span> `$fastLimit`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$slowLimit`</span> \]\] )

### 参数

`real`  
浮点数数组。

`fastLimit`  
Upper limit use in the adaptive algorithm. Valid range from 0.01 to
0.99.

`slowLimit`  
Lower limit use in the adaptive algorithm. Valid range from 0.01 to
0.99.

### 返回值

Returns an array with calculated data or false on failure.

trader\_mavp
============

Moving average with variable period

### 说明

<span class="type">array</span> <span
class="methodname">trader\_mavp</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> , <span
class="methodparam"><span class="type">array</span> `$periods`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$minPeriod`</span> \[, <span class="methodparam"><span
class="type">int</span> `$maxPeriod`</span> \[, <span
class="methodparam"><span class="type">int</span> `$mAType`</span>
\]\]\] )

### 参数

`real`  
浮点数数组。

`periods`  
浮点数数组。

`minPeriod`  
Value less than minimum will be changed to Minimum period. Valid range
from 2 to 100000

`maxPeriod`  
Value higher than minimum will be changed to Maximum period. Valid range
from 2 to 100000

`mAType`  
Type of Moving Average.
<a href="/trader/constants.html" class="link">TRADER_MA_TYPE_*</a>
series of constants should be used.

### 返回值

Returns an array with calculated data or false on failure.

trader\_max
===========

Highest value over a specified period

### 说明

<span class="type">array</span> <span
class="methodname">trader\_max</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_maxindex
================

Index of highest value over a specified period

### 说明

<span class="type">array</span> <span
class="methodname">trader\_maxindex</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_medprice
================

Median Price

### 说明

<span class="type">array</span> <span
class="methodname">trader\_medprice</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
)

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_mfi
===========

Money Flow Index

### 说明

<span class="type">array</span> <span
class="methodname">trader\_mfi</span> ( <span class="methodparam"><span
class="type">array</span> `$high`</span> , <span
class="methodparam"><span class="type">array</span> `$low`</span> ,
<span class="methodparam"><span class="type">array</span>
`$close`</span> , <span class="methodparam"><span
class="type">array</span> `$volume`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`volume`  
成交量，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_midpoint
================

MidPoint over period

### 说明

<span class="type">array</span> <span
class="methodname">trader\_midpoint</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_midprice
================

Midpoint Price over period

### 说明

<span class="type">array</span> <span
class="methodname">trader\_midprice</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_min
===========

Lowest value over a specified period

### 说明

<span class="type">array</span> <span
class="methodname">trader\_min</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_minindex
================

Index of lowest value over a specified period

### 说明

<span class="type">array</span> <span
class="methodname">trader\_minindex</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_minmax
==============

Lowest and highest values over a specified period

### 说明

<span class="type">array</span> <span
class="methodname">trader\_minmax</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_minmaxindex
===================

Indexes of lowest and highest values over a specified period

### 说明

<span class="type">array</span> <span
class="methodname">trader\_minmaxindex</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_minus\_di
=================

Minus Directional Indicator

### 说明

<span class="type">array</span> <span
class="methodname">trader\_minus\_di</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
, <span class="methodparam"><span class="type">array</span>
`$close`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_minus\_dm
=================

Minus Directional Movement

### 说明

<span class="type">array</span> <span
class="methodname">trader\_minus\_dm</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_mom
===========

Momentum

### 说明

<span class="type">array</span> <span
class="methodname">trader\_mom</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_mult
============

Vector Arithmetic Mult

### 说明

<span class="type">array</span> <span
class="methodname">trader\_mult</span> ( <span class="methodparam"><span
class="type">array</span> `$real0`</span> , <span
class="methodparam"><span class="type">array</span> `$real1`</span> )

Calculates the vector dot product of `real0` with `real1` and returns
the resulting vector.

### 参数

`real0`  
浮点数数组。

`real1`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_natr
============

Normalized Average True Range

### 说明

<span class="type">array</span> <span
class="methodname">trader\_natr</span> ( <span class="methodparam"><span
class="type">array</span> `$high`</span> , <span
class="methodparam"><span class="type">array</span> `$low`</span> ,
<span class="methodparam"><span class="type">array</span>
`$close`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_obv
===========

On Balance Volume

### 说明

<span class="type">array</span> <span
class="methodname">trader\_obv</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> , <span
class="methodparam"><span class="type">array</span> `$volume`</span> )

### 参数

`real`  
浮点数数组。

`volume`  
成交量，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_plus\_di
================

Plus Directional Indicator

### 说明

<span class="type">array</span> <span
class="methodname">trader\_plus\_di</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
, <span class="methodparam"><span class="type">array</span>
`$close`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_plus\_dm
================

Plus Directional Movement

### 说明

<span class="type">array</span> <span
class="methodname">trader\_plus\_dm</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_ppo
===========

Percentage Price Oscillator

### 说明

<span class="type">array</span> <span
class="methodname">trader\_ppo</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$fastPeriod`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$slowPeriod`</span> \[, <span class="methodparam"><span
class="type">int</span> `$mAType`</span> \]\]\] )

### 参数

`real`  
浮点数数组。

`fastPeriod`  
Number of period for the fast MA. Valid range from 2 to 100000.

`slowPeriod`  
Number of period for the slow MA. Valid range from 2 to 100000.

`mAType`  
Type of Moving Average.
<a href="/trader/constants.html" class="link">TRADER_MA_TYPE_*</a>
series of constants should be used.

### 返回值

Returns an array with calculated data or false on failure.

trader\_roc
===========

Rate of change : ((price/prevPrice)-1)\*100

### 说明

<span class="type">array</span> <span
class="methodname">trader\_roc</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_rocp
============

Rate of change Percentage: (price-prevPrice)/prevPrice

### 说明

<span class="type">array</span> <span
class="methodname">trader\_rocp</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_rocr100
===============

Rate of change ratio 100 scale: (price/prevPrice)\*100

### 说明

<span class="type">array</span> <span
class="methodname">trader\_rocr100</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_rocr
============

Rate of change ratio: (price/prevPrice)

### 说明

<span class="type">array</span> <span
class="methodname">trader\_rocr</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_rsi
===========

Relative Strength Index

### 说明

<span class="type">array</span> <span
class="methodname">trader\_rsi</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_sar
===========

Parabolic SAR

### 说明

<span class="type">array</span> <span
class="methodname">trader\_sar</span> ( <span class="methodparam"><span
class="type">array</span> `$high`</span> , <span
class="methodparam"><span class="type">array</span> `$low`</span> \[,
<span class="methodparam"><span class="type">float</span>
`$acceleration`</span> \[, <span class="methodparam"><span
class="type">float</span> `$maximum`</span> \]\] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`acceleration`  
Acceleration Factor used up to the Maximum value. Valid range from 0 to
<a href="/trader/constants.html#" class="link">TRADER_REAL_MAX</a>.

`maximum`  
Acceleration Factor Maximum value. Valid range from 0 to
<a href="/trader/constants.html#" class="link">TRADER_REAL_MAX</a>.

### 返回值

Returns an array with calculated data or false on failure.

trader\_sarext
==============

Parabolic SAR - Extended

### 说明

<span class="type">array</span> <span
class="methodname">trader\_sarext</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$startValue`</span> \[, <span class="methodparam"><span
class="type">float</span> `$offsetOnReverse`</span> \[, <span
class="methodparam"><span class="type">float</span>
`$accelerationInitLong`</span> \[, <span class="methodparam"><span
class="type">float</span> `$accelerationLong`</span> \[, <span
class="methodparam"><span class="type">float</span>
`$accelerationMaxLong`</span> \[, <span class="methodparam"><span
class="type">float</span> `$accelerationInitShort`</span> \[, <span
class="methodparam"><span class="type">float</span>
`$accelerationShort`</span> \[, <span class="methodparam"><span
class="type">float</span> `$accelerationMaxShort`</span>
\]\]\]\]\]\]\]\] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`startValue`  
Start value and direction. 0 for Auto, \>0 for Long, \<0 for Short.
Valid range from
<a href="/trader/constants.html#" class="link">TRADER_REAL_MIN</a> to
<a href="/trader/constants.html#" class="link">TRADER_REAL_MAX</a>.

`offsetOnReverse`  
Percent offset added/removed to initial stop on short/long reversal.
Valid range from 0 to
<a href="/trader/constants.html#" class="link">TRADER_REAL_MAX</a>.

`accelerationInitLong`  
Acceleration Factor initial value for the Long direction. Valid range
from 0 to
<a href="/trader/constants.html#" class="link">TRADER_REAL_MAX</a>.

`accelerationLong`  
Acceleration Factor for the Long direction. Valid range from 0 to
<a href="/trader/constants.html#" class="link">TRADER_REAL_MAX</a>.

`accelerationMaxLong`  
Acceleration Factor maximum value for the Long direction. Valid range
from 0 to
<a href="/trader/constants.html#" class="link">TRADER_REAL_MAX</a>.

`accelerationInitShort`  
Acceleration Factor initial value for the Short direction. Valid range
from 0 to
<a href="/trader/constants.html#" class="link">TRADER_REAL_MAX</a>.

`accelerationShort`  
Acceleration Factor for the Short direction. Valid range from 0 to
<a href="/trader/constants.html#" class="link">TRADER_REAL_MAX</a>.

`accelerationMaxShort`  
Acceleration Factor maximum value for the Short direction. Valid range
from 0 to
<a href="/trader/constants.html#" class="link">TRADER_REAL_MAX</a>.

### 返回值

Returns an array with calculated data or false on failure.

trader\_set\_compat
===================

Set compatibility mode

### 说明

<span class="type">void</span> <span
class="methodname">trader\_set\_compat</span> ( <span
class="methodparam"><span class="type">int</span> `$compatId`</span> )

Set compatibility mode which will affect the way calculations are done
by all the extension functions.

### 参数

`compatId`  
Compatibility Id.
<a href="/trader/constants.html" class="link">TRADER_COMPATIBILITY_*</a>
series of constants should be used.

### 返回值

没有返回值。

trader\_set\_unstable\_period
=============================

Set unstable period

### 说明

<span class="type">void</span> <span
class="methodname">trader\_set\_unstable\_period</span> ( <span
class="methodparam"><span class="type">int</span> `$functionId`</span> ,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> )

Influences unstable period factor for functions, which are sensible to
it. More information about unstable periods can be found on the
<a href="http://ta-lib.org/d_api/ta_setunstableperiod.html" class="link external">» TA-Lib</a>
API documentation page.

### 参数

`functionId`  
Function ID the factor should be set for.
<a href="/trader/constants.html" class="link">TRADER_FUNC_UNST_*</a>
constant series can be used to affect the corresponding function.

`timePeriod`  
Unstable period value.

### 返回值

没有返回值。

trader\_sin
===========

Vector Trigonometric Sin

### 说明

<span class="type">array</span> <span
class="methodname">trader\_sin</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> )

Calculates the sine for each value in `real` and returns the resulting
array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_sinh
============

Vector Trigonometric Sinh

### 说明

<span class="type">array</span> <span
class="methodname">trader\_sinh</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> )

Calculates the hyperbolic sine for each value in `real` and returns the
resulting array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_sma
===========

Simple Moving Average

### 说明

<span class="type">array</span> <span
class="methodname">trader\_sma</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_sqrt
============

Vector Square Root

### 说明

<span class="type">array</span> <span
class="methodname">trader\_sqrt</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> )

Calculates the square root of each value in `real` and returns the
resulting array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_stddev
==============

Standard Deviation

### 说明

<span class="type">array</span> <span
class="methodname">trader\_stddev</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \[, <span class="methodparam"><span
class="type">float</span> `$nbDev`</span> \]\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

`nbDev`  

### 返回值

Returns an array with calculated data or false on failure.

trader\_stoch
=============

Stochastic

### 说明

<span class="type">array</span> <span
class="methodname">trader\_stoch</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
, <span class="methodparam"><span class="type">array</span>
`$close`</span> \[, <span class="methodparam"><span
class="type">int</span> `$fastK_Period`</span> \[, <span
class="methodparam"><span class="type">int</span> `$slowK_Period`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$slowK_MAType`</span> \[, <span class="methodparam"><span
class="type">int</span> `$slowD_Period`</span> \[, <span
class="methodparam"><span class="type">int</span> `$slowD_MAType`</span>
\]\]\]\]\] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`fastK_Period`  
Time period for building the Fast-K line. Valid range from 1 to 100000.

`slowK_Period`  
Smoothing for making the Slow-K line. Valid range from 1 to 100000,
usually set to 3.

`slowK_MAType`  
Type of Moving Average for Slow-K.
<a href="/trader/constants.html" class="link">TRADER_MA_TYPE_*</a>
series of constants should be used.

`slowD_Period`  
Smoothing for making the Slow-D line. Valid range from 1 to 100000.

`slowD_MAType`  
Type of Moving Average for Slow-D.
<a href="/trader/constants.html" class="link">TRADER_MA_TYPE_*</a>
series of constants should be used.

### 返回值

Returns an array with calculated data or false on failure.

trader\_stochf
==============

Stochastic Fast

### 说明

<span class="type">array</span> <span
class="methodname">trader\_stochf</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
, <span class="methodparam"><span class="type">array</span>
`$close`</span> \[, <span class="methodparam"><span
class="type">int</span> `$fastK_Period`</span> \[, <span
class="methodparam"><span class="type">int</span> `$fastD_Period`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$fastD_MAType`</span> \]\]\] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`fastK_Period`  
Time period for building the Fast-K line. Valid range from 1 to 100000.

`fastD_Period`  
Smoothing for making the Fast-D line. Valid range from 1 to 100000,
usually set to 3.

`fastD_MAType`  
Type of Moving Average for Fast-D.
<a href="/trader/constants.html" class="link">TRADER_MA_TYPE_*</a>
series of constants should be used.

### 返回值

Returns an array with calculated data or false on failure.

trader\_stochrsi
================

Stochastic Relative Strength Index

### 说明

<span class="type">array</span> <span
class="methodname">trader\_stochrsi</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \[, <span class="methodparam"><span
class="type">int</span> `$fastK_Period`</span> \[, <span
class="methodparam"><span class="type">int</span> `$fastD_Period`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$fastD_MAType`</span> \]\]\]\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

`fastK_Period`  
Time period for building the Fast-K line. Valid range from 1 to 100000.

`fastD_Period`  
Smoothing for making the Fast-D line. Valid range from 1 to 100000,
usually set to 3.

`fastD_MAType`  
Type of Moving Average for Fast-D.
<a href="/trader/constants.html" class="link">TRADER_MA_TYPE_*</a>
series of constants should be used.

### 返回值

Returns an array with calculated data or false on failure.

trader\_sub
===========

Vector Arithmetic Subtraction

### 说明

<span class="type">array</span> <span
class="methodname">trader\_sub</span> ( <span class="methodparam"><span
class="type">array</span> `$real0`</span> , <span
class="methodparam"><span class="type">array</span> `$real1`</span> )

Calculates the vector subtraction of `real1` from `real0` and returns
the resulting vector.

### 参数

`real0`  
浮点数数组。

`real1`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_sum
===========

Summation

### 说明

<span class="type">array</span> <span
class="methodname">trader\_sum</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_t3
==========

Triple Exponential Moving Average (T3)

### 说明

<span class="type">array</span> <span
class="methodname">trader\_t3</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$vFactor`</span> \]\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

`vFactor`  
成交量因子。有效值从 0 到 1。

### 返回值

Returns an array with calculated data or false on failure.

trader\_tan
===========

Vector Trigonometric Tan

### 说明

<span class="type">array</span> <span
class="methodname">trader\_tan</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> )

Calculates the tangent for each value in `real` and returns the
resulting array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_tanh
============

Vector Trigonometric Tanh

### 说明

<span class="type">array</span> <span
class="methodname">trader\_tanh</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> )

Calculates the hyperbolic tangent for each value in `real` and returns
the resulting array.

### 参数

`real`  
浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_tema
============

Triple Exponential Moving Average

### 说明

<span class="type">array</span> <span
class="methodname">trader\_tema</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_trange
==============

True Range

### 说明

<span class="type">array</span> <span
class="methodname">trader\_trange</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
, <span class="methodparam"><span class="type">array</span>
`$close`</span> )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_trima
=============

Triangular Moving Average

### 说明

<span class="type">array</span> <span
class="methodname">trader\_trima</span> ( <span
class="methodparam"><span class="type">array</span> `$real`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timePeriod`</span> \] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_trix
============

1-day Rate-Of-Change (ROC) of a Triple Smooth EMA

### 说明

<span class="type">array</span> <span
class="methodname">trader\_trix</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_tsf
===========

Time Series Forecast

### 说明

<span class="type">array</span> <span
class="methodname">trader\_tsf</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_typprice
================

Typical Price

### 说明

<span class="type">array</span> <span
class="methodname">trader\_typprice</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
, <span class="methodparam"><span class="type">array</span>
`$close`</span> )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_ultosc
==============

Ultimate Oscillator

### 说明

<span class="type">array</span> <span
class="methodname">trader\_ultosc</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
, <span class="methodparam"><span class="type">array</span>
`$close`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timePeriod1`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod2`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timePeriod3`</span> \]\]\] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`timePeriod1`  
Number of bars for 1st period. Valid range from 1 to 100000.

`timePeriod2`  
Number of bars for 2nd period. Valid range from 1 to 100000.

`timePeriod3`  
Number of bars for 3rd period. Valid range from 1 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_var
===========

Variance

### 说明

<span class="type">array</span> <span
class="methodname">trader\_var</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$nbDev`</span> \]\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

`nbDev`  

### 返回值

Returns an array with calculated data or false on failure.

trader\_wclprice
================

Weighted Close Price

### 说明

<span class="type">array</span> <span
class="methodname">trader\_wclprice</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
, <span class="methodparam"><span class="type">array</span>
`$close`</span> )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

### 返回值

Returns an array with calculated data or false on failure.

trader\_willr
=============

Williams' %R

### 说明

<span class="type">array</span> <span
class="methodname">trader\_willr</span> ( <span
class="methodparam"><span class="type">array</span> `$high`</span> ,
<span class="methodparam"><span class="type">array</span> `$low`</span>
, <span class="methodparam"><span class="type">array</span>
`$close`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timePeriod`</span> \] )

### 参数

`high`  
高价，浮点数数组。

`low`  
低价，浮点数数组。

`close`  
收盘价，浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

trader\_wma
===========

Weighted Moving Average

### 说明

<span class="type">array</span> <span
class="methodname">trader\_wma</span> ( <span class="methodparam"><span
class="type">array</span> `$real`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timePeriod`</span>
\] )

### 参数

`real`  
浮点数数组。

`timePeriod`  
Number of period. Valid range from 2 to 100000.

### 返回值

Returns an array with calculated data or false on failure.

**目录**

-   [trader\_acos](/ref/trader.html#trader_acos) — Vector Trigonometric
    ACos
-   [trader\_ad](/ref/trader.html#trader_ad) — Chaikin A/D Line
-   [trader\_add](/ref/trader.html#trader_add) — Vector Arithmetic Add
-   [trader\_adosc](/ref/trader.html#trader_adosc) — Chaikin A/D
    Oscillator
-   [trader\_adx](/ref/trader.html#trader_adx) — Average Directional
    Movement Index
-   [trader\_adxr](/ref/trader.html#trader_adxr) — Average Directional
    Movement Index Rating
-   [trader\_apo](/ref/trader.html#trader_apo) — Absolute Price
    Oscillator
-   [trader\_aroon](/ref/trader.html#trader_aroon) — Aroon
-   [trader\_aroonosc](/ref/trader.html#trader_aroonosc) — Aroon
    Oscillator
-   [trader\_asin](/ref/trader.html#trader_asin) — Vector Trigonometric
    ASin
-   [trader\_atan](/ref/trader.html#trader_atan) — Vector Trigonometric
    ATan
-   [trader\_atr](/ref/trader.html#trader_atr) — Average True Range
-   [trader\_avgprice](/ref/trader.html#trader_avgprice) — Average Price
-   [trader\_bbands](/ref/trader.html#trader_bbands) — Bollinger Bands
-   [trader\_beta](/ref/trader.html#trader_beta) — Beta
-   [trader\_bop](/ref/trader.html#trader_bop) — Balance Of Power
-   [trader\_cci](/ref/trader.html#trader_cci) — Commodity Channel Index
-   [trader\_cdl2crows](/ref/trader.html#trader_cdl2crows) — Two Crows
-   [trader\_cdl3blackcrows](/ref/trader.html#trader_cdl3blackcrows) —
    Three Black Crows
-   [trader\_cdl3inside](/ref/trader.html#trader_cdl3inside) — Three
    Inside Up/Down
-   [trader\_cdl3linestrike](/ref/trader.html#trader_cdl3linestrike) —
    Three-Line Strike
-   [trader\_cdl3outside](/ref/trader.html#trader_cdl3outside) — Three
    Outside Up/Down
-   [trader\_cdl3starsinsouth](/ref/trader.html#trader_cdl3starsinsouth)
    — Three Stars In The South
-   [trader\_cdl3whitesoldiers](/ref/trader.html#trader_cdl3whitesoldiers)
    — Three Advancing White Soldiers
-   [trader\_cdlabandonedbaby](/ref/trader.html#trader_cdlabandonedbaby)
    — Abandoned Baby
-   [trader\_cdladvanceblock](/ref/trader.html#trader_cdladvanceblock) —
    Advance Block
-   [trader\_cdlbelthold](/ref/trader.html#trader_cdlbelthold) —
    Belt-hold
-   [trader\_cdlbreakaway](/ref/trader.html#trader_cdlbreakaway) —
    Breakaway
-   [trader\_cdlclosingmarubozu](/ref/trader.html#trader_cdlclosingmarubozu)
    — Closing Marubozu
-   [trader\_cdlconcealbabyswall](/ref/trader.html#trader_cdlconcealbabyswall)
    — Concealing Baby Swallow
-   [trader\_cdlcounterattack](/ref/trader.html#trader_cdlcounterattack)
    — Counterattack
-   [trader\_cdldarkcloudcover](/ref/trader.html#trader_cdldarkcloudcover)
    — Dark Cloud Cover
-   [trader\_cdldoji](/ref/trader.html#trader_cdldoji) — Doji
-   [trader\_cdldojistar](/ref/trader.html#trader_cdldojistar) — Doji
    Star
-   [trader\_cdldragonflydoji](/ref/trader.html#trader_cdldragonflydoji)
    — Dragonfly Doji
-   [trader\_cdlengulfing](/ref/trader.html#trader_cdlengulfing) —
    Engulfing Pattern
-   [trader\_cdleveningdojistar](/ref/trader.html#trader_cdleveningdojistar)
    — Evening Doji Star
-   [trader\_cdleveningstar](/ref/trader.html#trader_cdleveningstar) —
    Evening Star
-   [trader\_cdlgapsidesidewhite](/ref/trader.html#trader_cdlgapsidesidewhite)
    — Up/Down-gap side-by-side white lines
-   [trader\_cdlgravestonedoji](/ref/trader.html#trader_cdlgravestonedoji)
    — Gravestone Doji
-   [trader\_cdlhammer](/ref/trader.html#trader_cdlhammer) — Hammer
-   [trader\_cdlhangingman](/ref/trader.html#trader_cdlhangingman) —
    Hanging Man
-   [trader\_cdlharami](/ref/trader.html#trader_cdlharami) — Harami
    Pattern
-   [trader\_cdlharamicross](/ref/trader.html#trader_cdlharamicross) —
    Harami Cross Pattern
-   [trader\_cdlhighwave](/ref/trader.html#trader_cdlhighwave) —
    High-Wave Candle
-   [trader\_cdlhikkake](/ref/trader.html#trader_cdlhikkake) — Hikkake
    Pattern
-   [trader\_cdlhikkakemod](/ref/trader.html#trader_cdlhikkakemod) —
    Modified Hikkake Pattern
-   [trader\_cdlhomingpigeon](/ref/trader.html#trader_cdlhomingpigeon) —
    Homing Pigeon
-   [trader\_cdlidentical3crows](/ref/trader.html#trader_cdlidentical3crows)
    — Identical Three Crows
-   [trader\_cdlinneck](/ref/trader.html#trader_cdlinneck) — In-Neck
    Pattern
-   [trader\_cdlinvertedhammer](/ref/trader.html#trader_cdlinvertedhammer)
    — Inverted Hammer
-   [trader\_cdlkicking](/ref/trader.html#trader_cdlkicking) — Kicking
-   [trader\_cdlkickingbylength](/ref/trader.html#trader_cdlkickingbylength)
    — Kicking - bull/bear determined by the longer marubozu
-   [trader\_cdlladderbottom](/ref/trader.html#trader_cdlladderbottom) —
    Ladder Bottom
-   [trader\_cdllongleggeddoji](/ref/trader.html#trader_cdllongleggeddoji)
    — Long Legged Doji
-   [trader\_cdllongline](/ref/trader.html#trader_cdllongline) — Long
    Line Candle
-   [trader\_cdlmarubozu](/ref/trader.html#trader_cdlmarubozu) —
    Marubozu
-   [trader\_cdlmatchinglow](/ref/trader.html#trader_cdlmatchinglow) —
    Matching Low
-   [trader\_cdlmathold](/ref/trader.html#trader_cdlmathold) — Mat Hold
-   [trader\_cdlmorningdojistar](/ref/trader.html#trader_cdlmorningdojistar)
    — Morning Doji Star
-   [trader\_cdlmorningstar](/ref/trader.html#trader_cdlmorningstar) —
    Morning Star
-   [trader\_cdlonneck](/ref/trader.html#trader_cdlonneck) — On-Neck
    Pattern
-   [trader\_cdlpiercing](/ref/trader.html#trader_cdlpiercing) —
    Piercing Pattern
-   [trader\_cdlrickshawman](/ref/trader.html#trader_cdlrickshawman) —
    Rickshaw Man
-   [trader\_cdlrisefall3methods](/ref/trader.html#trader_cdlrisefall3methods)
    — Rising/Falling Three Methods
-   [trader\_cdlseparatinglines](/ref/trader.html#trader_cdlseparatinglines)
    — Separating Lines
-   [trader\_cdlshootingstar](/ref/trader.html#trader_cdlshootingstar) —
    Shooting Star
-   [trader\_cdlshortline](/ref/trader.html#trader_cdlshortline) — Short
    Line Candle
-   [trader\_cdlspinningtop](/ref/trader.html#trader_cdlspinningtop) —
    Spinning Top
-   [trader\_cdlstalledpattern](/ref/trader.html#trader_cdlstalledpattern)
    — Stalled Pattern
-   [trader\_cdlsticksandwich](/ref/trader.html#trader_cdlsticksandwich)
    — Stick Sandwich
-   [trader\_cdltakuri](/ref/trader.html#trader_cdltakuri) — Takuri
    (Dragonfly Doji with very long lower shadow)
-   [trader\_cdltasukigap](/ref/trader.html#trader_cdltasukigap) —
    Tasuki Gap
-   [trader\_cdlthrusting](/ref/trader.html#trader_cdlthrusting) —
    Thrusting Pattern
-   [trader\_cdltristar](/ref/trader.html#trader_cdltristar) — Tristar
    Pattern
-   [trader\_cdlunique3river](/ref/trader.html#trader_cdlunique3river) —
    Unique 3 River
-   [trader\_cdlupsidegap2crows](/ref/trader.html#trader_cdlupsidegap2crows)
    — Upside Gap Two Crows
-   [trader\_cdlxsidegap3methods](/ref/trader.html#trader_cdlxsidegap3methods)
    — Upside/Downside Gap Three Methods
-   [trader\_ceil](/ref/trader.html#trader_ceil) — Vector Ceil
-   [trader\_cmo](/ref/trader.html#trader_cmo) — Chande Momentum
    Oscillator
-   [trader\_correl](/ref/trader.html#trader_correl) — Pearson's
    Correlation Coefficient (r)
-   [trader\_cos](/ref/trader.html#trader_cos) — Vector Trigonometric
    Cos
-   [trader\_cosh](/ref/trader.html#trader_cosh) — Vector Trigonometric
    Cosh
-   [trader\_dema](/ref/trader.html#trader_dema) — Double Exponential
    Moving Average
-   [trader\_div](/ref/trader.html#trader_div) — Vector Arithmetic Div
-   [trader\_dx](/ref/trader.html#trader_dx) — Directional Movement
    Index
-   [trader\_ema](/ref/trader.html#trader_ema) — Exponential Moving
    Average
-   [trader\_errno](/ref/trader.html#trader_errno) — Get error code
-   [trader\_exp](/ref/trader.html#trader_exp) — Vector Arithmetic Exp
-   [trader\_floor](/ref/trader.html#trader_floor) — Vector Floor
-   [trader\_get\_compat](/ref/trader.html#trader_get_compat) — Get
    compatibility mode
-   [trader\_get\_unstable\_period](/ref/trader.html#trader_get_unstable_period)
    — Get unstable period
-   [trader\_ht\_dcperiod](/ref/trader.html#trader_ht_dcperiod) —
    Hilbert Transform - Dominant Cycle Period
-   [trader\_ht\_dcphase](/ref/trader.html#trader_ht_dcphase) — Hilbert
    Transform - Dominant Cycle Phase
-   [trader\_ht\_phasor](/ref/trader.html#trader_ht_phasor) — Hilbert
    Transform - Phasor Components
-   [trader\_ht\_sine](/ref/trader.html#trader_ht_sine) — Hilbert
    Transform - SineWave
-   [trader\_ht\_trendline](/ref/trader.html#trader_ht_trendline) —
    Hilbert Transform - Instantaneous Trendline
-   [trader\_ht\_trendmode](/ref/trader.html#trader_ht_trendmode) —
    Hilbert Transform - Trend vs Cycle Mode
-   [trader\_kama](/ref/trader.html#trader_kama) — Kaufman Adaptive
    Moving Average
-   [trader\_linearreg\_angle](/ref/trader.html#trader_linearreg_angle)
    — Linear Regression Angle
-   [trader\_linearreg\_intercept](/ref/trader.html#trader_linearreg_intercept)
    — Linear Regression Intercept
-   [trader\_linearreg\_slope](/ref/trader.html#trader_linearreg_slope)
    — Linear Regression Slope
-   [trader\_linearreg](/ref/trader.html#trader_linearreg) — Linear
    Regression
-   [trader\_ln](/ref/trader.html#trader_ln) — Vector Log Natural
-   [trader\_log10](/ref/trader.html#trader_log10) — Vector Log10
-   [trader\_ma](/ref/trader.html#trader_ma) — Moving average
-   [trader\_macd](/ref/trader.html#trader_macd) — Moving Average
    Convergence/Divergence
-   [trader\_macdext](/ref/trader.html#trader_macdext) — MACD with
    controllable MA type
-   [trader\_macdfix](/ref/trader.html#trader_macdfix) — Moving Average
    Convergence/Divergence Fix 12/26
-   [trader\_mama](/ref/trader.html#trader_mama) — MESA Adaptive Moving
    Average
-   [trader\_mavp](/ref/trader.html#trader_mavp) — Moving average with
    variable period
-   [trader\_max](/ref/trader.html#trader_max) — Highest value over a
    specified period
-   [trader\_maxindex](/ref/trader.html#trader_maxindex) — Index of
    highest value over a specified period
-   [trader\_medprice](/ref/trader.html#trader_medprice) — Median Price
-   [trader\_mfi](/ref/trader.html#trader_mfi) — Money Flow Index
-   [trader\_midpoint](/ref/trader.html#trader_midpoint) — MidPoint over
    period
-   [trader\_midprice](/ref/trader.html#trader_midprice) — Midpoint
    Price over period
-   [trader\_min](/ref/trader.html#trader_min) — Lowest value over a
    specified period
-   [trader\_minindex](/ref/trader.html#trader_minindex) — Index of
    lowest value over a specified period
-   [trader\_minmax](/ref/trader.html#trader_minmax) — Lowest and
    highest values over a specified period
-   [trader\_minmaxindex](/ref/trader.html#trader_minmaxindex) — Indexes
    of lowest and highest values over a specified period
-   [trader\_minus\_di](/ref/trader.html#trader_minus_di) — Minus
    Directional Indicator
-   [trader\_minus\_dm](/ref/trader.html#trader_minus_dm) — Minus
    Directional Movement
-   [trader\_mom](/ref/trader.html#trader_mom) — Momentum
-   [trader\_mult](/ref/trader.html#trader_mult) — Vector Arithmetic
    Mult
-   [trader\_natr](/ref/trader.html#trader_natr) — Normalized Average
    True Range
-   [trader\_obv](/ref/trader.html#trader_obv) — On Balance Volume
-   [trader\_plus\_di](/ref/trader.html#trader_plus_di) — Plus
    Directional Indicator
-   [trader\_plus\_dm](/ref/trader.html#trader_plus_dm) — Plus
    Directional Movement
-   [trader\_ppo](/ref/trader.html#trader_ppo) — Percentage Price
    Oscillator
-   [trader\_roc](/ref/trader.html#trader_roc) — Rate of change :
    ((price/prevPrice)-1)\*100
-   [trader\_rocp](/ref/trader.html#trader_rocp) — Rate of change
    Percentage: (price-prevPrice)/prevPrice
-   [trader\_rocr100](/ref/trader.html#trader_rocr100) — Rate of change
    ratio 100 scale: (price/prevPrice)\*100
-   [trader\_rocr](/ref/trader.html#trader_rocr) — Rate of change ratio:
    (price/prevPrice)
-   [trader\_rsi](/ref/trader.html#trader_rsi) — Relative Strength Index
-   [trader\_sar](/ref/trader.html#trader_sar) — Parabolic SAR
-   [trader\_sarext](/ref/trader.html#trader_sarext) — Parabolic SAR -
    Extended
-   [trader\_set\_compat](/ref/trader.html#trader_set_compat) — Set
    compatibility mode
-   [trader\_set\_unstable\_period](/ref/trader.html#trader_set_unstable_period)
    — Set unstable period
-   [trader\_sin](/ref/trader.html#trader_sin) — Vector Trigonometric
    Sin
-   [trader\_sinh](/ref/trader.html#trader_sinh) — Vector Trigonometric
    Sinh
-   [trader\_sma](/ref/trader.html#trader_sma) — Simple Moving Average
-   [trader\_sqrt](/ref/trader.html#trader_sqrt) — Vector Square Root
-   [trader\_stddev](/ref/trader.html#trader_stddev) — Standard
    Deviation
-   [trader\_stoch](/ref/trader.html#trader_stoch) — Stochastic
-   [trader\_stochf](/ref/trader.html#trader_stochf) — Stochastic Fast
-   [trader\_stochrsi](/ref/trader.html#trader_stochrsi) — Stochastic
    Relative Strength Index
-   [trader\_sub](/ref/trader.html#trader_sub) — Vector Arithmetic
    Subtraction
-   [trader\_sum](/ref/trader.html#trader_sum) — Summation
-   [trader\_t3](/ref/trader.html#trader_t3) — Triple Exponential Moving
    Average (T3)
-   [trader\_tan](/ref/trader.html#trader_tan) — Vector Trigonometric
    Tan
-   [trader\_tanh](/ref/trader.html#trader_tanh) — Vector Trigonometric
    Tanh
-   [trader\_tema](/ref/trader.html#trader_tema) — Triple Exponential
    Moving Average
-   [trader\_trange](/ref/trader.html#trader_trange) — True Range
-   [trader\_trima](/ref/trader.html#trader_trima) — Triangular Moving
    Average
-   [trader\_trix](/ref/trader.html#trader_trix) — 1-day Rate-Of-Change
    (ROC) of a Triple Smooth EMA
-   [trader\_tsf](/ref/trader.html#trader_tsf) — Time Series Forecast
-   [trader\_typprice](/ref/trader.html#trader_typprice) — Typical Price
-   [trader\_ultosc](/ref/trader.html#trader_ultosc) — Ultimate
    Oscillator
-   [trader\_var](/ref/trader.html#trader_var) — Variance
-   [trader\_wclprice](/ref/trader.html#trader_wclprice) — Weighted
    Close Price
-   [trader\_willr](/ref/trader.html#trader_willr) — Williams' %R
-   [trader\_wma](/ref/trader.html#trader_wma) — Weighted Moving Average
