SPL Type Handling
=================

**目录**

-   [简介](/intro/spl-types.html)
-   [安装／配置](/spl-types/setup.html)
    -   [需求](/spl-types/setup.html#需求)
    -   [安装](/spl-types/setup.html#安装)
    -   [运行时配置](/spl-types/setup.html#运行时配置)
    -   [资源类型](/spl-types/setup.html#资源类型)
-   [SplType](/class/spltype.html) — The SplType class
    -   [SplType::\_\_construct](/class/spltype.html#SplType::__construct)
        — Creates a new value of some type
-   [SplInt](/class/splint.html) — The SplInt class
-   [SplFloat](/class/splfloat.html) — The SplFloat class
-   [SplEnum](/class/splenum.html) — The SplEnum class
    -   [SplEnum::getConstList](/class/splenum.html#SplEnum::getConstList)
        — Returns all consts (possible values) as an array
-   [SplBool](/class/splbool.html) — The SplBool class
-   [SplString](/class/splstring.html) — The SplString class

简介
----

Parent class for all SPL types.

类摘要
------

**SplType**

<span class="ooclass"> <span class="modifier">abstract</span> class
**SplType** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">NULL</span>
`SplType::__default` <span class="initializer"> = **`NULL`**</span> ;

/\* 方法 \*/

<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span>
`$initial_value`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$strict`</span> \]\] )

}

预定义常量
----------

**`SplType::__default`**  

SplType::\_\_construct
======================

Creates a new value of some type

### 说明

<span class="methodname">SplType::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span>
`$initial_value`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$strict`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`initial_value`  
Type and default value depends on the extension class.

`strict`  
Whether to set the object's strictness.

### 错误／异常

Throws an <span class="classname">UnexpectedValueException</span> if
incompatible type is given.

简介
----

The SplInt class is used to enforce strong typing of the integer type.

类摘要
------

**SplInt**

<span class="ooclass"> class **SplInt** </span> <span class="ooclass">
<span class="modifier">extends</span> **SplType** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`SplInt::__default` <span class="initializer"> = 0</span> ;

/\* 继承的方法 \*/

<span class="methodname">SplType::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span>
`$initial_value`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$strict`</span> \]\] )

}

预定义常量
----------

**`SplInt::__default`**  

范例
----

**示例 \#1 <span class="classname">SplInt</span> usage example**

``` php
<?php
$int = new SplInt(94);

try {
    $int = 'Try to cast a string value for fun';
} catch (UnexpectedValueException $uve) {
    echo $uve->getMessage() . PHP_EOL;
}

echo $int . PHP_EOL;
?>
```

以上例程会输出：

    Value not an integer
    94

简介
----

The SplFloat class is used to enforce strong typing of the float type.

类摘要
------

**SplFloat**

<span class="ooclass"> class **SplFloat** </span> <span class="ooclass">
<span class="modifier">extends</span> **SplType** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">float</span>
`SplFloat::__default` <span class="initializer"> = 0</span> ;

/\* 继承的方法 \*/

<span class="methodname">SplType::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span>
`$initial_value`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$strict`</span> \]\] )

}

预定义常量
----------

**`SplFloat::__default`**  

范例
----

**示例 \#2 <span class="classname">SplFloat</span> usage example**

``` php
<?php
$float = new SplFloat(3.154);
$newFloat = new SplFloat(3);

try {
    $float = 'Try to cast a string value for fun';
} catch (UnexpectedValueException $uve) {
    echo $uve->getMessage() . PHP_EOL;
}

echo $float . PHP_EOL;
echo $newFloat . PHP_EOL;
?>
```

以上例程会输出：

    Value not a float
    3.154
    3

简介
----

SplEnum gives the ability to emulate and create enumeration objects
natively in PHP.

类摘要
------

**SplEnum**

<span class="ooclass"> class **SplEnum** </span> <span class="ooclass">
<span class="modifier">extends</span> **SplType** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">NULL</span>
`SplEnum::__default` <span class="initializer"> = **`NULL`**</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getConstList</span> (\[ <span
class="methodparam"><span class="type">bool</span>
`$include_default`<span class="initializer"> = **`FALSE`**</span></span>
\] )

/\* 继承的方法 \*/

<span class="methodname">SplType::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span>
`$initial_value`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$strict`</span> \]\] )

}

预定义常量
----------

**`SplEnum::__default`**  

范例
----

**示例 \#3 <span class="classname">SplEnum</span> usage example**

``` php
<?php
class Month extends SplEnum {
    const __default = self::January;
    
    const January = 1;
    const February = 2;
    const March = 3;
    const April = 4;
    const May = 5;
    const June = 6;
    const July = 7;
    const August = 8;
    const September = 9;
    const October = 10;
    const November = 11;
    const December = 12;
}

echo new Month(Month::June) . PHP_EOL;

try {
    new Month(13);
} catch (UnexpectedValueException $uve) {
    echo $uve->getMessage() . PHP_EOL;
}
?>
```

以上例程会输出：

    6
    Value not a const in enum Month

SplEnum::getConstList
=====================

Returns all consts (possible values) as an array

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SplEnum::getConstList</span> (\[ <span
class="methodparam"><span class="type">bool</span>
`$include_default`<span class="initializer"> = **`FALSE`**</span></span>
\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`include_default`  
Whether to include *\_\_default* property.

### 返回值

### 范例

**示例 \#1 <span class="function">SplEnum::getConstList</span> example**

``` php
<?php
$bool = new SplBool;
var_dump($bool->getConstList(true));
?>
```

以上例程会输出：

    array(3) {
      ["__default"]=>
      bool(false)
      ["false"]=>
      bool(false)
      ["true"]=>
      bool(true)
    }

简介
----

The SplBool class is used to enforce strong typing of the bool type.

类摘要
------

**SplBool**

<span class="ooclass"> class **SplBool** </span> <span class="ooclass">
<span class="modifier">extends</span> **SplEnum** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">bool</span>
`SplBool::__default` <span class="initializer"> = **`FALSE`**</span> ;

<span class="modifier">const</span> <span class="type">bool</span>
`SplBool::false` <span class="initializer"> = **`FALSE`**</span> ;

<span class="modifier">const</span> <span class="type">bool</span>
`SplBool::true` <span class="initializer"> = **`TRUE`**</span> ;

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SplEnum::getConstList</span> (\[ <span
class="methodparam"><span class="type">bool</span>
`$include_default`<span class="initializer"> = **`FALSE`**</span></span>
\] )

}

预定义常量
----------

**`SplBool::__default`**  

**`SplBool::false`**  

**`SplBool::true`**  

范例
----

**示例 \#1 <span class="classname">SplBool</span> usage example**

``` php
<?php
$true = new SplBool(true);
if ($true) {
    echo "TRUE\n";
}

$false = new SplBool;
if ($false) {
    echo "FALSE\n";
}
?>
```

以上例程会输出：

    TRUE

简介
----

The SplString class is used to enforce strong typing of the string type.

类摘要
------

**SplString**

<span class="ooclass"> class **SplString** </span> <span
class="ooclass"> <span class="modifier">extends</span> **SplType**
</span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">string</span>
`SplString::__default` <span class="initializer"> = ''</span> ;

/\* 继承的方法 \*/

<span class="methodname">SplType::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span>
`$initial_value`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$strict`</span> \]\] )

}

预定义常量
----------

**`SplString::__default`**  

范例
----

**示例 \#2 <span class="classname">SplString</span> usage example**

``` php
<?php
$string = new SplString("Testing");

try {
    $string = array();
} catch (UnexpectedValueException $uve) {
    echo $uve->getMessage() . PHP_EOL;
}

var_dump($string);
echo $string; // Outputs "Testing"
?>
```

以上例程会输出：

    Value not a string
    object(SplString)#1 (1) {
      ["__default"]=>
      string(7) "Testing"
    }
    Testing
