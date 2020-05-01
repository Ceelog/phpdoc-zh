Yaconf
======

**目录**

-   [简介](/intro/yaconf.html)
-   [安装／配置](/yaconf/setup.html)
    -   [需求](/yaconf/setup.html#需求)
    -   [安装](/yaconf/setup.html#安装)
    -   [运行时配置](/yaconf/setup.html#运行时配置)
    -   [资源类型](/yaconf/setup.html#资源类型)
-   [预定义常量](/yaconf/constants.html)
-   [Yaconf](/class/yaconf.html) — The Yaconf class
    -   [Yaconf::get](/class/yaconf.html#Yaconf::get) — Retrieve a item
    -   [Yaconf::has](/class/yaconf.html#Yaconf::has) — Determine if a
        item exists

简介
----

Yaconf is a configurations container, it parses INIT files, stores the
result in PHP when PHP is started, the result lives with the whole PHP
lifecycle.

类摘要
------

**Yaconf**

<span class="ooclass"> class **Yaconf** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">get</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> \[, <span
class="methodparam"><span class="type">mixed</span>
`$default_value`<span class="initializer"> = NULL</span></span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">has</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

}

Yaconf::get
===========

Retrieve a item

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">Yaconf::get</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> \[, <span
class="methodparam"><span class="type">mixed</span>
`$default_value`<span class="initializer"> = NULL</span></span> \] )

### 参数

`name`  
Configuration key, the key looks like "filename.key", or
"filename.sectionName,key".

`default_value`  
if the key doesn't exists, Yaconf::get will return this as result.

### 返回值

Returns configuration result(string or array) if the key exists, return
default\_value if not.

### 范例

**示例 \#1 <span class="function">INI</span>example**

``` ini
;filenmame foo.ini, placed in directory which is yaconf.directoy
[SectionA]
;key value pair
key=val
;hash[a]=val
hash.a=val
;arr[0]=val
arr.0=val
;or
arr[]=val

;SectionB inherits SectionA
[SectionB:SectionA]
;override configuration key in SectionA
key=new_val
```

以上例程的输出类似于：

    php7 -r 'var_dump(Yaconf::get("foo.SectionA.key"));'
    //string(3) "val"

    php7 -r 'var_dump(Yaconf::get("foo.SectionB.key"));'
    //string(7) "new_val"

    php7 -r 'var_dump(Yaconf::get("foo")["SectionA"]["hash"]);'
    //array(1)

Yaconf::has
===========

Determine if a item exists

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">Yaconf::has</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

### 参数

`name`  

### 返回值
