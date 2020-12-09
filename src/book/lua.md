Lua
===

**目录**

-   [简介](/intro/lua.html)
-   [安装／配置](/lua/setup.html)
    -   [需求](/lua/setup.html#需求)
    -   [安装](/lua/setup.html#安装)
    -   [运行时配置](/lua/setup.html#运行时配置)
    -   [资源类型](/lua/setup.html#资源类型)
-   [Lua](/class/lua.html) — Lua类
    -   [Lua::assign](/class/lua.html#Lua::assign) —
        将一个php变量赋值给Lua
    -   [Lua::call](/class/lua.html#Lua::call) — 调用Lua函数
    -   [Lua::\_\_construct](/class/lua.html#Lua::__construct) — Lua
        构造方法
    -   [Lua::eval](/class/lua.html#Lua::eval) — 将字符串当做Lua代码执行
    -   [Lua::getVersion](/class/lua.html#Lua::getVersion) — 获取Lua版本
    -   [Lua::include](/class/lua.html#Lua::include) — 解析Lua脚本文件
    -   [Lua::registerCallback](/class/lua.html#Lua::registerCallback) —
        向Lua中注册php函数
-   [LuaClosure](/class/luaclosure.html) — LuaClosure类
    -   [LuaClosure::\_\_invoke](/class/luaclosure.html#LuaClosure::__invoke)
        — 调用luaclosure

简介
----

类摘要
------

**Lua**

<span class="ooclass"> class **Lua** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">string</span>
`Lua::LUA_VERSION` <span class="initializer"> = Lua 5.1.4</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">assign</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">call</span> ( <span class="methodparam"><span
class="type">callable</span> `$lua_func`</span> \[, <span
class="methodparam"><span class="type">array</span> `$args`</span> \[,
<span class="methodparam"><span class="type">int</span> `$use_self`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">\_\_call</span> ( <span
class="methodparam"><span class="type">callable</span>
`$lua_func`</span> \[, <span class="methodparam"><span
class="type">array</span> `$args`</span> \[, <span
class="methodparam"><span class="type">int</span> `$use_self`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$lua_script_file`<span class="initializer"> = NULL</span></span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">eval</span> ( <span class="methodparam"><span
class="type">string</span> `$statements`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getVersion</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">include</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">registerCallback</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$function`</span> )

}

预定义常量
----------

**`Lua::LUA_VERSION`**  

Lua::assign
===========

将一个php变量赋值给Lua

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Lua::assign</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

`value`  

### 返回值

赋值成功返回`$this`否则返回**`null`**

### 范例

**示例 \#1 <span class="function">Lua::assign</span>示例**

``` php
<?php
$lua = new Lua();
$lua->assign("php_var", array(1=>1, 2, 3)); //lua table index begin with 1
$lua->eval(<<<CODE
    print(php_var);
CODE
);
?>
```

以上例程会输出：

    Array
     (
         [1] => 1
         [2] => 2
         [3] => 3
     )

Lua::call
=========

Lua::\_\_call
=============

调用Lua函数

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Lua::call</span> ( <span
class="methodparam"><span class="type">callable</span>
`$lua_func`</span> \[, <span class="methodparam"><span
class="type">array</span> `$args`</span> \[, <span
class="methodparam"><span class="type">int</span> `$use_self`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Lua::\_\_call</span> ( <span
class="methodparam"><span class="type">callable</span>
`$lua_func`</span> \[, <span class="methodparam"><span
class="type">array</span> `$args`</span> \[, <span
class="methodparam"><span class="type">int</span> `$use_self`<span
class="initializer"> = 0</span></span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`lua_func`  
lua中的函数名。

`args`  
向Lua函数传入的参数。

`use_self`  
是否使用*self*。

### 返回值

返回调用函数的结果，参数错误返回**`null`** ，其它错误返回**`false`**。

### 范例

**示例 \#1 <span class="function">Lua::call</span>示例**

``` php
<?php
$lua = new Lua();
$lua->eval(<<<CODE
    function dummy(foo, bar)
        print(foo, ",", bar)
    end
CODE
);
$lua->call("dummy", array("Lua", "geiliable\n"));
$lua->dummy("Lua", "geiliable"); // __call()
var_dump($lua->call(array("table", "concat"), array(array(1=>1, 2=>2, 3=>3), "-")));
?>
```

以上例程会输出：

    Lua,geiliable
    Lua,geiliable
    string(5) "1-2-3"

### 参见

-   <a href="/language/oop5/overloading.html#object.call" class="link">__call()</a>

Lua::\_\_construct
==================

Lua 构造方法

### 说明

<span class="modifier">public</span> <span
class="methodname">Lua::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$lua_script_file`<span class="initializer"> = NULL</span></span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`lua_script_file`  

### 返回值

Lua::eval
=========

将字符串当做Lua代码执行

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Lua::eval</span> ( <span
class="methodparam"><span class="type">string</span>
`$statements`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`statements`  

### 返回值

返回运行结果，参数错误返回**`null`** ，其它错误返回**`false`**。

### 范例

**示例 \#1 <span class="function">Lua::eval</span>示例**

``` php
<?php
$lua = new Lua();
$lua->eval(<<<CODE
    print(2);
CODE
);
?>
```

以上例程会输出：

    2

Lua::getVersion
===============

获取Lua版本

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Lua::getVersion</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

返回 `Lua::LUA_VERSION`。

Lua::include
============

解析Lua脚本文件

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Lua::include</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`file`  

### 返回值

返回脚本文件运行结果，参数错误返回**`null`** ，其它错误返回**`false`**。

Lua::registerCallback
=====================

向Lua中注册php函数

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Lua::registerCallback</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$function`</span> )

向Lua注册php函数，函数名为"$name"

### 参数

`name`  

`function`  
一个有效的PHP回调函数

### 返回值

成功返回`$this`，参数错误返回**`null`** ，其它错误返回**`false`**。

### 范例

**示例 \#1 <span class="function">Lua::registerCallback</span>示例**

``` php
<?php
$lua = new Lua();
$lua->registerCallback("echo", "var_dump");
$lua->eval(<<<CODE
    echo({1, 2, 3});
CODE
);
?>
```

以上例程会输出：

    array(3) {
      [1]=>
      float(1)
      [2]=>
      float(2)
      [3]=>
      float(3)
    }

简介
----

LuaClosure是对LUA\_TFUNCTION的封装类，可以作为调用Lua函数的返回值。

类摘要
------

**LuaClosure**

<span class="ooclass"> class **LuaClosure** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_invoke</span> ( <span
class="methodparam"><span class="type">mixed</span> `$arg`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$...`</span>
\] )

}

LuaClosure::\_\_invoke
======================

调用luaclosure

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">LuaClosure::\_\_invoke</span> ( <span
class="methodparam"><span class="type">mixed</span> `$arg`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$...`</span>
\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`arg`  

`...`  

### 返回值

### 范例

**示例 \#1 <span class="function">LuaClosure::\_\_invoke</span>示例**

``` php
<?php
$lua = new Lua();
$closure = $lua->eval(<<<CODE
    return (function ()
        print("hello world")
    end)
CODE
);

$lua->call($closure);
/* after PHP 5.3 */
$closure();
?>
```

以上例程会输出：

    hello worldhello world
