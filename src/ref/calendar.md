cal\_days\_in\_month
====================

返回某个历法中某年中某月的天数

### 说明

<span class="type">int</span> <span
class="methodname">cal\_days\_in\_month</span> ( <span
class="methodparam"><span class="type">int</span> `$calendar`</span> ,
<span class="methodparam"><span class="type">int</span> `$month`</span>
, <span class="methodparam"><span class="type">int</span> `$year`</span>
)

该函数返回特定`历法`中的某`年`中的某`月`的天数。

### 参数

`calendar`  
用来计算的某个历法

`month`  
选定历法中的某月

`year`  
选定历法中的某年

### 返回值

指定历法中选定的某月的天数。

### 范例

**示例 \#1 <span class="function">cal\_days\_in\_month</span> example**

``` php
<?php
$num = cal_days_in_month(CAL_GREGORIAN, 8, 2003); // 31
echo "There was $num days in August 2003";
?>
```

cal\_from\_jd
=============

转换Julian Day计数到一个支持的历法。

### 说明

<span class="type">array</span> <span
class="methodname">cal\_from\_jd</span> ( <span
class="methodparam"><span class="type">int</span> `$jd`</span> , <span
class="methodparam"><span class="type">int</span> `$calendar`</span> )

<span class="function">cal\_from\_jd</span>函数根据给定的Julian
day的`jd`
天数转换成特定历法`calendar`中的日期。`calendar`支持的值有**`CAL_GREGORIAN`**，**`CAL_JULIAN`**，**`CAL_JEWISH`**
和**`CAL_FRENCH`**。

### 参数

`jd`  
一个Julian day天数的整数数字

`calendar`  
要转换成的历法

### 返回值

返回一个数组，包含的历法信息有月，日，年，星期，星期的缩写和全写，月份的缩写和全写，日期的形式是“月/日/年”。

### 范例

**示例 \#1 <span class="function">cal\_from\_jd</span> example**

``` php
<?php
$today = unixtojd(mktime(0, 0, 0, 8, 16, 2003));
print_r(cal_from_jd($today, CAL_GREGORIAN));
?>
```

以上例程会输出：

    Array
    (
        [date] => 8/16/2003
        [month] => 8
        [day] => 16
        [year] => 2003
        [dow] => 6
        [abbrevdayname] => Sat
        [dayname] => Saturday
        [abbrevmonth] => Aug
        [monthname] => August
    )

### 参见

-   <span class="function">cal\_to\_jd</span>
-   <span class="function">jdtofrench</span>
-   <span class="function">jdtogregorian</span>
-   <span class="function">jdtojewish</span>
-   <span class="function">jdtojulian</span>
-   <span class="function">jdtounix</span>

cal\_info
=========

返回选定历法的信息

### 说明

<span class="type">array</span> <span
class="methodname">cal\_info</span> (\[ <span class="methodparam"><span
class="type">int</span> `$calendar`<span class="initializer"> =
-1</span></span> \] )

<span class="function">cal\_info</span>返回选定 `calendar`的作息。

历法信息以一个数组的形式返回，包含的元素有*历法名称*，*历法代码*，*月份*，*月份的缩写*和*单月的最多天数*。作为参数的`calendar`历法名字可以有：

-   <span class="simpara"> 0 or **`CAL_GREGORIAN`** - Gregorian Calendar
    </span>
-   <span class="simpara"> 1 or **`CAL_JULIAN`** - Julian Calendar
    </span>
-   <span class="simpara"> 2 or **`CAL_JEWISH`** - Jewish Calendar
    </span>
-   <span class="simpara"> 3 or **`CAL_FRENCH`** - French Revolutionary
    Calendar </span>

如果没有指定参数`calendar`，所支持的所有历法将以数组形式返回。

### 参数

`calendar`  
返回信息所指定的历法名称，如果没有指定历法，将返回所有历法。

### 返回值

### 更新日志

| 版本      | 说明                                                 |
|-----------|------------------------------------------------------|
| Since 5.0 | 参数`calendar`作为可选项，缺省时默认值为"所有历法"。 |

### 范例

**示例 \#1 <span class="function">cal\_info</span> example**

``` php
<?php
$info = cal_info(0);
print_r($info);
?>
```

以上例程会输出：

    Array
    (
        [months] => Array
            (
                [1] => January
                [2] => February
                [3] => March
                [4] => April
                [5] => May
                [6] => June
                [7] => July
                [8] => August
                [9] => September
                [10] => October
                [11] => November
                [12] => December
            )

        [abbrevmonths] => Array
            (
                [1] => Jan
                [2] => Feb
                [3] => Mar
                [4] => Apr
                [5] => May
                [6] => Jun
                [7] => Jul
                [8] => Aug
                [9] => Sep
                [10] => Oct
                [11] => Nov
                [12] => Dec
            )

        [maxdaysinmonth] => 31
        [calname] => Gregorian
        [calsymbol] => CAL_GREGORIAN
    )

cal\_to\_jd
===========

从一个支持的历法转变为Julian Day计数。

### 说明

<span class="type">int</span> <span
class="methodname">cal\_to\_jd</span> ( <span class="methodparam"><span
class="type">int</span> `$calendar`</span> , <span
class="methodparam"><span class="type">int</span> `$month`</span> ,
<span class="methodparam"><span class="type">int</span> `$day`</span> ,
<span class="methodparam"><span class="type">int</span> `$year`</span> )

<span
class="function">cal\_to\_jd</span>函数从一个给定的历法日期计算出Julian天数，支持的历法有
**`CAL_GREGORIAN`**，**`CAL_JULIAN`**，**`CAL_JEWISH`**和**`CAL_FRENCH`**。

### 参数

`calendar`  
选定的历法，可以是**`CAL_GREGORIAN`**，**`CAL_JULIAN`**，**`CAL_JEWISH`**或**`CAL_FRENCH`**中的某一个。

`month`  
数字形式的月份，根据选定的`calendar`历法来确定范围。

`day`  
数字形式的日期，根据选定的`calendar`历法来确定范围。

`year`  
数字形式的年份，根据选定的`calendar`历法来确定范围。

### 返回值

一个Julian天数。

### 参见

-   <span class="function">cal\_from\_jd</span>
-   <span class="function">frenchtojd</span>
-   <span class="function">gregoriantojd</span>
-   <span class="function">jewishtojd</span>
-   <span class="function">juliantojd</span>
-   <span class="function">unixtojd</span>

easter\_date
============

得到指定年份的复活节午夜时的Unix时间戳。

### 说明

<span class="type">int</span> <span
class="methodname">easter\_date</span> (\[ <span
class="methodparam"><span class="type">int</span> `$year`</span> \] )

返回指定年份的复活节午夜时的Unix时间戳。

**Warning**

如果给定的年份超出Unix时间戳的范围（比如1970年以前或2037年以后），该函数将返回一个警告。

复活节的日期是由尼西亚议会在AD325年确定的为每年春分月圆后的第一个星期日。春分一般是在3月21日，这就简化为只要计算满月的日期和紧挨的星期日的日期。这里所用的算法是在532年由Dionysius
Exiguus所介绍的，参考了Julian历法和Gregorian历法这两个历法来提高精确度。（在1753年以前用Julian历法计算，该历法是一个以19年为周期来确定月亮的相位的历法。在1753年以后用Gregorian历法计算，该历法由Clavius和Lilius发明，由Pope
Gregory 8世在1582年推广）

### 参数

`year`  
1970年至2037年之间的数字形式的年份。

### 返回值

复活节日期的Unix时间戳。

### 更新日志

| 版本        | 说明                                 |
|-------------|--------------------------------------|
| Since 4.3.0 | `year`参数可选，缺省的默认值是当年。 |

### 范例

**示例 \#1 <span class="function">easter\_date</span> example**

``` php
<?php

echo date("M-d-Y", easter_date(1999));        // Apr-04-1999
echo date("M-d-Y", easter_date(2000));        // Apr-23-2000
echo date("M-d-Y", easter_date(2001));        // Apr-15-2001

?>
```

### 参见

-   <span class="function">easter\_days</span> for calculating Easter
    before 1970 or after 2037

easter\_days
============

得到指定年份的3月21日到复活节之间的天数

### 说明

<span class="type">int</span> <span
class="methodname">easter\_days</span> (\[ <span
class="methodparam"><span class="type">int</span> `$year`</span> \[,
<span class="methodparam"><span class="type">int</span> `$method`<span
class="initializer"> = CAL\_EASTER\_DEFAULT</span></span> \]\] )

返回指定年份的3月21日到复活节之间的天数，如果没有指定年份，默认是当年。

这个函数可以用来代替<span
class="function">easter\_date</span>函数来计算Unix时间戳以外年份的复活节日期。（比如1970年以前或2037年以后）

复活节的日期是由尼西亚议会在AD325年确定的为每年春分月圆后的第一个星期日。春分一般是在3月21日，这就简化为只要计算满月的日期和紧挨的星期日的日期。这里所用的算法是在532年由Dionysius
Exiguus所介绍的，参考了Julian历法和Gregorian历法这两个历法来提高精确度。（在1753年以前用Julian历法计算，该历法是一个以19年为周期来确定月亮的相位的历法。在1753年以后用Gregorian历法计算，该历法由Clavius和Lilius发明，由Pope
Gregory 8世在1582年推广）

### 参数

`year`  
正数形式的年份

`method`  
当设置为**`CAL_EASTER_ROMAN`**时可以用Gregorian历法来计算1582－1752之间的复活节日期。更多可用的常量参考<a href="/calendar/constants.html" class="link">calendar constants</a>。

### 返回值

根据给定参数`year`年份而返回的3月21日至复活节的天数。

### 更新日志

| 版本        | 说明                                |
|-------------|-------------------------------------|
| Since 4.3.0 | 参数`year` 可选，缺省默认值是当年。 |
| Since 4.3.0 | 引入参数 `method`。                 |

### 范例

**示例 \#1 <span class="function">easter\_days</span> example**

``` php
<?php

echo easter_days(1999);        // 14, i.e. April 4
echo easter_days(1492);        // 32, i.e. April 22
echo easter_days(1913);        //  2, i.e. March 23

?>
```

### 参见

-   <span class="function">easter\_date</span>

FrenchToJD
==========

从一个French Republican历法的日期得到Julian Day计数。

### 说明

<span class="type">int</span> <span class="methodname">frenchtojd</span>
( <span class="methodparam"><span class="type">int</span>
`$month`</span> , <span class="methodparam"><span
class="type">int</span> `$day`</span> , <span class="methodparam"><span
class="type">int</span> `$year`</span> )

从一个French Republican历法的日期得到Julian Day计数。

年份所能用的范围是1到14（Gregorian历法的1792年9月22日到1806年9月22日）。

### 参数

`month`  
月份的范围是1到13。

`day`  
日期的范围是1到30。

`year`  
年份的范围是1到14。

### 返回值

返回指定french revolution日期的julian天数。

### 参见

-   <span class="function">jdtofrench</span>
-   <span class="function">cal\_to\_jd</span>

GregorianToJD
=============

转变一个Gregorian历法日期到Julian Day计数

### 说明

<span class="type">int</span> <span
class="methodname">gregoriantojd</span> ( <span
class="methodparam"><span class="type">int</span> `$month`</span> ,
<span class="methodparam"><span class="type">int</span> `$day`</span> ,
<span class="methodparam"><span class="type">int</span> `$year`</span> )

Gregorian历法的合理范围是4714 B.C. 至 9999 A.D.

虽然这个函数可以处理4714
B.C.以前的日期，但是没有意义。Gregorian历法直到1582年10年15日（或是Julian历法的1582年10月5日）才被发明，很久以后一些国家也没有接受它。比如，英国是在1752年开始使用Gregorian历法，苏联是在1918年，希腊是在1923年，大部分的欧洲国家使用Julian历法。

### 参数

`month`  
月份的范围是 1（January）到 12（December）。

`day`  
日期的范围是 1到 31。

`year`  
年份的范围是 -4714 到 9999。

### 返回值

给定gregorian历法日期的julian天数。

### 范例

**示例 \#1 Calendar functions**

``` php
<?php
$jd = GregorianToJD(10, 11, 1970);
echo "$jd\n";
$gregorian = JDToGregorian($jd);
echo "$gregorian\n";
?>
```

### 参见

-   <span class="function">jdtogregorian</span>
-   <span class="function">cal\_to\_jd</span>

JDDayOfWeek
===========

返回星期的日期

### 说明

<span class="type">mixed</span> <span
class="methodname">jddayofweek</span> ( <span class="methodparam"><span
class="type">int</span> `$julianday`</span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = CAL\_DOW\_DAYNO</span></span> \] )

返回星期的日期，根据模式不同可能是字符串或是整数。

### 参数

`julianday`  
一个julian天数。

`mode`  
| Mode     | Meaning                                  |
|----------|------------------------------------------|
| 0 (默认) | 返回数字形式(0=Sunday, 1=Monday, etc)    |
| 1        | 返回字符串形式 (English-Gregorian)       |
| 2        | 返回缩写形式的字符串 (English-Gregorian) |

### 返回值

数字或字符串形式的星期数。

JDMonthName
===========

返回月份的名称

### 说明

<span class="type">string</span> <span
class="methodname">jdmonthname</span> ( <span class="methodparam"><span
class="type">int</span> `$julianday`</span> , <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

返回一个月份名称的字符串，`mode`参数指定使用哪种历法和月份名称的形式。

| Mode | Meaning                 | Values                                                                                                                         |
|------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| 0    | Gregorian - abbreviated | Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec                                                                     |
| 1    | Gregorian               | January, February, March, April, May, June, July, August, September, October, November, December                               |
| 2    | Julian - abbreviated    | Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec                                                                     |
| 3    | Julian                  | January, February, March, April, May, June, July, August, September, October, November, December                               |
| 4    | Jewish                  | Tishri, Heshvan, Kislev, Tevet, Shevat, AdarI, AdarII, Nisan, Iyyar, Sivan, Tammuz, Av, Elul                                   |
| 5    | French Republican       | Vendemiaire, Brumaire, Frimaire, Nivose, Pluviose, Ventose, Germinal, Floreal, Prairial, Messidor, Thermidor, Fructidor, Extra |

### 参数

`jday`  
用来计算的julian天数

`calendar`  
历法的月份的名字

### 返回值

根据指定的julian天数和`calendar`历法参数而得到月份的名称。

JDToFrench
==========

转变一个Julian Day计数到French Republican历法的日期

### 说明

<span class="type">string</span> <span
class="methodname">jdtofrench</span> ( <span class="methodparam"><span
class="type">int</span> `$juliandaycount`</span> )

转变一个Julian Day计数到French Republican历法的日期。

### 参数

`julianday`  
一个julian天数

### 返回值

以"月/日/年"形式的french revolution日期

### 参见

-   <span class="function">frenchtojd</span>
-   <span class="function">cal\_from\_jd</span>

JDToGregorian
=============

转变一个Julian Day计数为Gregorian历法日期

### 说明

<span class="type">string</span> <span
class="methodname">jdtogregorian</span> ( <span
class="methodparam"><span class="type">int</span> `$julianday`</span> )

转变一个julian天数为gregorian历法的“月/日/年”形式的日期

### 参数

`julianday`  
一个julian天数

### 返回值

“月/日/年”形式的gregorian日期

### 参见

-   <span class="function">gregoriantojd</span>
-   <span class="function">cal\_from\_jd</span>

jdtojewish
==========

转换一个julian天数为Jewish历法的日期

### 说明

<span class="type">string</span> <span
class="methodname">jdtojewish</span> ( <span class="methodparam"><span
class="type">int</span> `$juliandaycount`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$hebrew`<span
class="initializer"> = false</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$fl`<span
class="initializer"> = 0</span></span> \]\] )

转换一个julian天数为Jewish历法的日期。

### 参数

`julianday`  
一个julian天数

`hebrew`  
如果参数 `hebrew`设置为 **`TRUE`**，参数`fl`可用于希伯莱语的格式。

`fl`  
可用的格式有： **`CAL_JEWISH_ADD_ALAFIM_GERESH`**,
**`CAL_JEWISH_ADD_ALAFIM`**, **`CAL_JEWISH_ADD_GERESHAYIM`**.

### 返回值

以“月/日/年”的格式显示jewish日期。

### 更新日志

| 版本  | 说明                   |
|-------|------------------------|
| 5.0.0 | 增加了参数 `fl`。      |
| 4.3.0 | 增加了参数 `hebrew` 。 |

### 范例

**示例 \#1 <span class="function">jdtojewish</span> Example**

``` php
<?php
echo jdtojewish(gregoriantojd(10, 8, 2002), true,
       CAL_JEWISH_ADD_GERESHAYIM + CAL_JEWISH_ADD_ALAFIM + CAL_JEWISH_ADD_ALAFIM_GERESH); 
?>
```

### 参见

-   <span class="function">jewishtojd</span>
-   <span class="function">cal\_from\_jd</span>

JDToJulian
==========

转变一个Julian Day计数到Julian历法的日期

### 说明

<span class="type">string</span> <span
class="methodname">jdtojulian</span> ( <span class="methodparam"><span
class="type">int</span> `$julianday`</span> )

转变一个Julian Day计数到以“月/日/年”形式显示的Julian历法的日期。

### 参数

`julianday`  
一个julian天数

### 返回值

以“月/日/年”形式显示的Julian历法的日期

### 参见

-   <span class="function">juliantojd</span>
-   <span class="function">cal\_from\_jd</span>

jdtounix
========

转变Julian Day计数为一个Unix时间戳

### 说明

<span class="type">int</span> <span class="methodname">jdtounix</span> (
<span class="methodparam"><span class="type">int</span> `$jday`</span> )

这个函数根据给定的julian天数返回一个Unix时间戳，或如果参数`jday`不在Unix时间（Gregorian历法的1970年至2037年，或2440588
\<= `jday` \<= 2465342）范围内返回 **`FALSE`**
。返回的时间是本地时间（不是GMT）。

### 参数

`jday`  
一个在 2440588 到 2465342 之间的julian天数

### 返回值

指定的julian天数的开始时的时间戳。

### 参见

-   <span class="function">unixtojd</span>

JewishToJD
==========

转变一个Jewish历法的日期为一个Julian Day计数

### 说明

<span class="type">int</span> <span class="methodname">jewishtojd</span>
( <span class="methodparam"><span class="type">int</span>
`$month`</span> , <span class="methodparam"><span
class="type">int</span> `$day`</span> , <span class="methodparam"><span
class="type">int</span> `$year`</span> )

尽管这个函数可以处理1（3761
B.C.）以前的年份，但这是没有意义的。Jewish历法被用了几千年，但早期的时候一个月的开始没有固定的准则，通常是观察到一个新月后定为一个月份的开始。

### 参数

`month`  
在1到13之间的月份

`day`  
在1到30日之间的日子

`year`  
在1到9999之间的年份

### 返回值

指定的jewish历法的日期的julian天数。

### 参见

-   <span class="function">jdtojewish</span>
-   <span class="function">cal\_to\_jd</span>

JulianToJD
==========

转变一个Julian历法的日期为Julian Day计数

### 说明

<span class="type">int</span> <span class="methodname">juliantojd</span>
( <span class="methodparam"><span class="type">int</span>
`$month`</span> , <span class="methodparam"><span
class="type">int</span> `$day`</span> , <span class="methodparam"><span
class="type">int</span> `$year`</span> )

Julian历法的合理年份为 4713 B.C. 到 9999 A.D.

尽管这个函数也可以处理4713 B.C.以前的日期，但是没有意义。这个历法是在46
B.C.创立，但是到了8
A.D.还没有稳定，可能直到第4世纪才最终完善。而且，每年的开始也不相同，不是所有的国家都认定January为第一个月份的。

**Caution**

记住，当今世界最广泛使用的历法是Gregorian历法，函数<span
class="function">gregoriantojd</span>可以转变日期为Julian Day计数。

### 参数

`month`  
月份的范围从 1 (January) 到 12 ( December)

`day`  
日期的范围从 1 到 31

`year`  
年份的范围从 -4713 到 9999

### 返回值

指定julian历法中的日期所对应的julian天数。

### 参见

-   <span class="function">jdtojulian</span>
-   <span class="function">cal\_to\_jd</span>

unixtojd
========

转变Unix时间戳为Julian Day计数

### 说明

<span class="type">int</span> <span class="methodname">unixtojd</span>
(\[ <span class="methodparam"><span class="type">int</span>
`$timestamp`<span class="initializer"> = time()</span></span> \] )

根据指定的Unix时间戳`timestamp`，返回Julian天数。如果没有指定时间戳则返回当前日期的天数。

### 参数

`timestamp`  
一个用于转变的时间戳。

### 返回值

一个julian天数。

### 参见

-   <span class="function">jdtounix</span>

**目录**

-   [cal\_days\_in\_month](/ref/calendar.html#cal_days_in_month) —
    返回某个历法中某年中某月的天数
-   [cal\_from\_jd](/ref/calendar.html#cal_from_jd) — 转换Julian
    Day计数到一个支持的历法。
-   [cal\_info](/ref/calendar.html#cal_info) — 返回选定历法的信息
-   [cal\_to\_jd](/ref/calendar.html#cal_to_jd) —
    从一个支持的历法转变为Julian Day计数。
-   [easter\_date](/ref/calendar.html#easter_date) —
    得到指定年份的复活节午夜时的Unix时间戳。
-   [easter\_days](/ref/calendar.html#easter_days) —
    得到指定年份的3月21日到复活节之间的天数
-   [FrenchToJD](/ref/calendar.html#FrenchToJD) — 从一个French
    Republican历法的日期得到Julian Day计数。
-   [GregorianToJD](/ref/calendar.html#GregorianToJD) —
    转变一个Gregorian历法日期到Julian Day计数
-   [JDDayOfWeek](/ref/calendar.html#JDDayOfWeek) — 返回星期的日期
-   [JDMonthName](/ref/calendar.html#JDMonthName) — 返回月份的名称
-   [JDToFrench](/ref/calendar.html#JDToFrench) — 转变一个Julian
    Day计数到French Republican历法的日期
-   [JDToGregorian](/ref/calendar.html#JDToGregorian) — 转变一个Julian
    Day计数为Gregorian历法日期
-   [jdtojewish](/ref/calendar.html#jdtojewish) —
    转换一个julian天数为Jewish历法的日期
-   [JDToJulian](/ref/calendar.html#JDToJulian) — 转变一个Julian
    Day计数到Julian历法的日期
-   [jdtounix](/ref/calendar.html#jdtounix) — 转变Julian
    Day计数为一个Unix时间戳
-   [JewishToJD](/ref/calendar.html#JewishToJD) —
    转变一个Jewish历法的日期为一个Julian Day计数
-   [JulianToJD](/ref/calendar.html#JulianToJD) —
    转变一个Julian历法的日期为Julian Day计数
-   [unixtojd](/ref/calendar.html#unixtojd) — 转变Unix时间戳为Julian
    Day计数
