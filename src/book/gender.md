Determine gender of firstnames
==============================

**目录**

-   [简介](/intro/gender.html)
-   [安装／配置](/gender/setup.html)
    -   [安装](/gender/setup.html#安装)
-   [范例](/gender/examples.html)
    -   [Usage example.](/gender/examples.html#Usage%20example.)
-   [Gender\\Gender](/class/gender.html) — The Gender\\Gender class
    -   [Gender\\Gender::connect](/class/gender.html#Gender\Gender::connect)
        — Connect to an external name dictionary
    -   [Gender\\Gender::\_\_construct](/class/gender.html#Gender\Gender::__construct)
        — Construct the Gender object
    -   [Gender\\Gender::country](/class/gender.html#Gender\Gender::country)
        — Get textual country representation
    -   [Gender\\Gender::get](/class/gender.html#Gender\Gender::get) —
        Get gender of a name
    -   [Gender\\Gender::isNick](/class/gender.html#Gender\Gender::isNick)
        — Check if the name0 is an alias of the name1
    -   [Gender\\Gender::similarNames](/class/gender.html#Gender\Gender::similarNames)
        — Get similar names

简介
----

类摘要
------

**Gender\\Gender**

<span class="ooclass"> class **Gender\\Gender** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::IS_FEMALE` <span class="initializer"> = 70</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::IS_MOSTLY_FEMALE` <span class="initializer"> =
102</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::IS_MALE` <span class="initializer"> = 77</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::IS_MOSTLY_MALE` <span class="initializer"> = 109</span>
;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::IS_UNISEX_NAME` <span class="initializer"> = 63</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::IS_A_COUPLE` <span class="initializer"> = 67</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::NAME_NOT_FOUND` <span class="initializer"> = 32</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::ERROR_IN_NAME` <span class="initializer"> = 69</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::ANY_COUNTRY` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::BRITAIN` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::IRELAND` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::USA` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::SPAIN` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::PORTUGAL` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::ITALY` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::MALTA` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::FRANCE` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::BELGIUM` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::LUXEMBOURG` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::NETHERLANDS` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::GERMANY` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::EAST_FRISIA` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::AUSTRIA` <span class="initializer"> = 14</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::SWISS` <span class="initializer"> = 15</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::ICELAND` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::DENMARK` <span class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::NORWAY` <span class="initializer"> = 18</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::SWEDEN` <span class="initializer"> = 19</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::FINLAND` <span class="initializer"> = 20</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::ESTONIA` <span class="initializer"> = 21</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::LATVIA` <span class="initializer"> = 22</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::LITHUANIA` <span class="initializer"> = 23</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::POLAND` <span class="initializer"> = 24</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::CZECH_REP` <span class="initializer"> = 25</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::SLOVAKIA` <span class="initializer"> = 26</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::HUNGARY` <span class="initializer"> = 27</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::ROMANIA` <span class="initializer"> = 28</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::BULGARIA` <span class="initializer"> = 29</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::BOSNIA` <span class="initializer"> = 30</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::CROATIA` <span class="initializer"> = 31</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::KOSOVO` <span class="initializer"> = 32</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::MACEDONIA` <span class="initializer"> = 33</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::MONTENEGRO` <span class="initializer"> = 34</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::SERBIA` <span class="initializer"> = 35</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::SLOVENIA` <span class="initializer"> = 36</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::ALBANIA` <span class="initializer"> = 37</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::GREECE` <span class="initializer"> = 38</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::RUSSIA` <span class="initializer"> = 39</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::BELARUS` <span class="initializer"> = 40</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::MOLDOVA` <span class="initializer"> = 41</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::UKRAINE` <span class="initializer"> = 42</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::ARMENIA` <span class="initializer"> = 43</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::AZERBAIJAN` <span class="initializer"> = 44</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::GEORGIA` <span class="initializer"> = 45</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::KAZAKH_UZBEK` <span class="initializer"> = 46</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::TURKEY` <span class="initializer"> = 47</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::ARABIA` <span class="initializer"> = 48</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::ISRAEL` <span class="initializer"> = 49</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::CHINA` <span class="initializer"> = 50</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::INDIA` <span class="initializer"> = 51</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::JAPAN` <span class="initializer"> = 52</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Gender\Gender::KOREA` <span class="initializer"> = 53</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">connect</span> ( <span
class="methodparam"><span class="type">string</span> `$dsn`</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$dsn`</span> \] )

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">false</span></span> <span
class="methodname">country</span> ( <span class="methodparam"><span
class="type">int</span> `$country`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">get</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> \[, <span
class="methodparam"><span class="type">int</span> `$country`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">isNick</span> ( <span class="methodparam"><span
class="type">string</span> `$name0`</span> , <span
class="methodparam"><span class="type">string</span> `$name1`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$country`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">similarNames</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$country`</span> \] )

}

预定义常量
----------

**`Gender\Gender::IS_FEMALE`**  

**`Gender\Gender::IS_MOSTLY_FEMALE`**  

**`Gender\Gender::IS_MALE`**  

**`Gender\Gender::IS_MOSTLY_MALE`**  

**`Gender\Gender::IS_UNISEX_NAME`**  

**`Gender\Gender::IS_A_COUPLE`**  

**`Gender\Gender::NAME_NOT_FOUND`**  

**`Gender\Gender::ERROR_IN_NAME`**  

**`Gender\Gender::ANY_COUNTRY`**  

**`Gender\Gender::BRITAIN`**  

**`Gender\Gender::IRELAND`**  

**`Gender\Gender::USA`**  

**`Gender\Gender::SPAIN`**  

**`Gender\Gender::PORTUGAL`**  

**`Gender\Gender::ITALY`**  

**`Gender\Gender::MALTA`**  

**`Gender\Gender::FRANCE`**  

**`Gender\Gender::BELGIUM`**  

**`Gender\Gender::LUXEMBOURG`**  

**`Gender\Gender::NETHERLANDS`**  

**`Gender\Gender::GERMANY`**  

**`Gender\Gender::EAST_FRISIA`**  

**`Gender\Gender::AUSTRIA`**  

**`Gender\Gender::SWISS`**  

**`Gender\Gender::ICELAND`**  

**`Gender\Gender::DENMARK`**  

**`Gender\Gender::NORWAY`**  

**`Gender\Gender::SWEDEN`**  

**`Gender\Gender::FINLAND`**  

**`Gender\Gender::ESTONIA`**  

**`Gender\Gender::LATVIA`**  

**`Gender\Gender::LITHUANIA`**  

**`Gender\Gender::POLAND`**  

**`Gender\Gender::CZECH_REP`**  

**`Gender\Gender::SLOVAKIA`**  

**`Gender\Gender::HUNGARY`**  

**`Gender\Gender::ROMANIA`**  

**`Gender\Gender::BULGARIA`**  

**`Gender\Gender::BOSNIA`**  

**`Gender\Gender::CROATIA`**  

**`Gender\Gender::KOSOVO`**  

**`Gender\Gender::MACEDONIA`**  

**`Gender\Gender::MONTENEGRO`**  

**`Gender\Gender::SERBIA`**  

**`Gender\Gender::SLOVENIA`**  

**`Gender\Gender::ALBANIA`**  

**`Gender\Gender::GREECE`**  

**`Gender\Gender::RUSSIA`**  

**`Gender\Gender::BELARUS`**  

**`Gender\Gender::MOLDOVA`**  

**`Gender\Gender::UKRAINE`**  

**`Gender\Gender::ARMENIA`**  

**`Gender\Gender::AZERBAIJAN`**  

**`Gender\Gender::GEORGIA`**  

**`Gender\Gender::KAZAKH_UZBEK`**  

**`Gender\Gender::TURKEY`**  

**`Gender\Gender::ARABIA`**  

**`Gender\Gender::ISRAEL`**  

**`Gender\Gender::CHINA`**  

**`Gender\Gender::INDIA`**  

**`Gender\Gender::JAPAN`**  

**`Gender\Gender::KOREA`**  

Gender\\Gender::connect
=======================

Connect to an external name dictionary

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Gender\\Gender::connect</span> ( <span
class="methodparam"><span class="type">string</span> `$dsn`</span> )

Connect to an external name dictionary. Currently only streams are
supported.

### 参数

`dsn`  
DSN to open.

### 返回值

Boolean as success of failure.

Gender\\Gender::\_\_construct
=============================

Construct the Gender object

### 说明

<span class="modifier">public</span> <span
class="methodname">Gender\\Gender::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$dsn`</span> \] )

Create a Gender object optionally connecting to an external name
dictionary. When no external database was given, compiled in data will
be used.

### 参数

`dsn`  
DSN to open.

### 返回值

Gender\\Gender::country
=======================

Get textual country representation

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">false</span></span> <span
class="methodname">Gender\\Gender::country</span> ( <span
class="methodparam"><span class="type">int</span> `$country`</span> )

Returns the textual representation of a country from a Gender class
constant.

### 参数

`country`  
A country ID specified by a <span
class="classname">Gender\\Gender</span> class constant.

### 返回值

Returns an array with the short and full names of the country on success
或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 Using <span
class="methodname">Gender\\Gender::country</span>**

``` php
$gender = new Gender\Gender;
var_dump($gender->country(Gender\Gender::BRITAIN));
```

以上例程会输出：

    array(2) {
      'country_short' =>
      string(2) "UK"
      'country' =>
      string(13) "Great Britain"
    }

Gender\\Gender::get
===================

Get gender of a name

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Gender\\Gender::get</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$country`</span> \] )

Get the gender of the name in a particular country.

### 参数

`name`  
Name to check.

`country`  
Country id identified by Gender class constant.

### 返回值

Returns gender of the name.

Gender\\Gender::isNick
======================

Check if the name0 is an alias of the name1

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Gender\\Gender::isNick</span> ( <span
class="methodparam"><span class="type">string</span> `$name0`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name1`</span> \[, <span class="methodparam"><span
class="type">int</span> `$country`</span> \] )

Check whether the name0 is a nick of the name1.

### 参数

`name0`  
Name to check.

`name1`  
Name to check.

`country`  
Country id identified by Gender class constant. If ommited ANY\_COUNTRY
is used.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

Gender\\Gender::similarNames
============================

Get similar names

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Gender\\Gender::similarNames</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$country`</span> \] )

Get similar names for the given name and country.

### 参数

`name`  
Name to check.

`country`  
Country id identified by Gender class constant. If ommited ANY\_COUNTRY
is used.

### 返回值

Returns an array with the similar names found.
