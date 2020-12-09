Weak References
===============

**目录**

-   [简介](/intro/weakref.html)
-   [安装／配置](/weakref/setup.html)
    -   [需求](/weakref/setup.html#需求)
    -   [安装](/weakref/setup.html#安装)
    -   [资源类型](/weakref/setup.html#资源类型)
-   [WeakRef](/class/weakref.html) — The WeakRef class
    -   [Weakref::acquire](/class/weakref.html#Weakref::acquire) —
        Acquires a strong reference on that object
    -   [Weakref::\_\_construct](/class/weakref.html#Weakref::__construct)
        — Constructs a new weak reference
    -   [Weakref::get](/class/weakref.html#Weakref::get) — Returns the
        object pointed to by the weak reference
    -   [Weakref::release](/class/weakref.html#Weakref::release) —
        Releases a previously acquired reference
    -   [Weakref::valid](/class/weakref.html#Weakref::valid) — Checks
        whether the object referenced still exists
-   [WeakMap](/class/weakmap.html) — The WeakMap class
    -   [WeakMap::\_\_construct](/class/weakmap.html#WeakMap::__construct)
        — Constructs a new map
    -   [WeakMap::count](/class/weakmap.html#WeakMap::count) — Counts
        the number of live entries in the map
    -   [WeakMap::current](/class/weakmap.html#WeakMap::current) —
        Returns the current value under iteration
    -   [WeakMap::key](/class/weakmap.html#WeakMap::key) — Returns the
        current key under iteration
    -   [WeakMap::next](/class/weakmap.html#WeakMap::next) — Advances to
        the next map element
    -   [WeakMap::offsetExists](/class/weakmap.html#WeakMap::offsetExists)
        — Checks whether a certain object is in the map
    -   [WeakMap::offsetGet](/class/weakmap.html#WeakMap::offsetGet) —
        Returns the value pointed to by a certain object
    -   [WeakMap::offsetSet](/class/weakmap.html#WeakMap::offsetSet) —
        Updates the map with a new key-value pair
    -   [WeakMap::offsetUnset](/class/weakmap.html#WeakMap::offsetUnset)
        — Removes an entry from the map
    -   [WeakMap::rewind](/class/weakmap.html#WeakMap::rewind) — Rewinds
        the iterator to the beginning of the map
    -   [WeakMap::valid](/class/weakmap.html#WeakMap::valid) — Returns
        whether the iterator is still on a valid map element

简介
----

The WeakRef class provides a gateway to objects without preventing the
garbage collector from freeing those objects. It also provides a way to
turn a weak reference into a strong one.

> **Note**:
>
> The class <span class="classname">WeakRef</span> is not to be confused
> with the class <span class="classname">WeakReference</span>.

类摘要
------

**WeakRef**

<span class="ooclass"> class **WeakRef** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">Weakref::\_\_construct</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Weakref::acquire</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">Weakref::get</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Weakref::release</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Weakref::valid</span> ( <span
class="methodparam">void</span> )

}

范例
----

**示例 \#1 <span class="classname">WeakRef</span> usage example**

``` php
<?php
class MyClass {
    public function __destruct() {
        echo "Destroying object!\n";
    }
}

$o1 = new MyClass;

$r1 = new WeakRef($o1);

if ($r1->valid()) {
    echo "Object still exists!\n";
    var_dump($r1->get());
} else {
    echo "Object is dead!\n";
}

unset($o1);

if ($r1->valid()) {
    echo "Object still exists!\n";
    var_dump($r1->get());
} else {
    echo "Object is dead!\n";
}
?>
```

以上例程会输出：

    Object still exists!
    object(MyClass)#1 (0) {
    }
    Destroying object!
    Object is dead!

Weakref::acquire
================

Acquires a strong reference on that object

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Weakref::acquire</span> ( <span
class="methodparam">void</span> )

Acquires a strong reference on that object, virtually turning the weak
reference into a strong one.

The <span class="classname">Weakref</span> instance maintains an
internal acquired counter to track outstanding strong references. If the
call to <span class="methodname">Weakref::acquire</span> is successful,
this counter will be incremented by one.

### 参数

此函数没有参数。

### 返回值

Returns **`true`** if the reference was valid and could be turned into a
strong reference, **`false`** otherwise.

### 范例

**示例 \#1 <span class="methodname">Weakref::acquire</span> example**

``` php
<?php
class MyClass {
    public function __destruct() {
        echo "Destroying object!\n";
    }
}

$o1 = new MyClass;

$r1 = new Weakref($o1);

$r1->acquire();

echo "Unsetting o1...\n";
unset($o1);

$o2 = $r1->get();

$r1->release();

echo "Unsetting o2...\n";
unset($o2);
?>
```

以上例程会输出：

    Unsetting o1...
    Unsetting o2...
    Destroying object!

**示例 \#2 Nested acquire/release example**

``` php
<?php
class MyClass {
    public function __destruct() {
        echo "Destroying object!\n";
    }
}

$o1 = new MyClass;

$r1 = new Weakref($o1);

echo "Acquiring...\n";
$r1->acquire();

echo "  Unsetting...\n";
unset($o1);

echo "  Acquiring...\n";
$r1->acquire();

echo "    Acquiring...\n";
$r1->acquire();

echo "    Releasing...\n";
$r1->release();

echo "  Releasing...\n";
$r1->release();

echo "Releasing...\n";
$r1->release();

?>
```

以上例程会输出：

    Acquiring...
      Unsetting...
      Acquiring...
        Acquiring...
        Releasing...
      Releasing...
    Releasing...
    Destroying object!

### 参见

-   <span class="methodname">Weakref::release</span>

Weakref::\_\_construct
======================

Constructs a new weak reference

### 说明

<span class="modifier">public</span> <span
class="methodname">Weakref::\_\_construct</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

Constructs a new weak reference.

### 参数

`object`  
The object to reference.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">Weakref::\_\_construct</span>
example**

``` php
<?php
class MyClass {
    public function __destruct() {
        echo "Destroying object!\n";
    }
}

$o1 = new MyClass;

$r1 = new Weakref($o1);

if ($r1->valid()) {
    echo "Object still exists!\n";
    var_dump($r1->get());
} else {
    echo "Object is dead!\n";
}

unset($o1);

if ($r1->valid()) {
    echo "Object still exists!\n";
    var_dump($r1->get());
} else {
    echo "Object is dead!\n";
}
?>
```

以上例程会输出：

    Object still exists!
    object(MyClass)#1 (0) {
    }
    Destroying object!
    Object is dead!

Weakref::get
============

Returns the object pointed to by the weak reference

### 说明

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">Weakref::get</span> ( <span
class="methodparam">void</span> )

Returns the object pointed to by the weak reference.

### 参数

此函数没有参数。

### 返回值

Returns the object if the reference is still valid, **`null`**
otherwise.

### 参见

-   <span class="methodname">Weakref::valid</span>

Weakref::release
================

Releases a previously acquired reference

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Weakref::release</span> ( <span
class="methodparam">void</span> )

Releases a previously acquired reference, potentially turning a strong
reference back into a weak reference.

The <span class="classname">Weakref</span> instance maintains an
internal acquired counter to track outstanding strong references. If the
call to <span class="methodname">Weakref::release</span> is successful,
this counter will be decremented by one. Once this counter reaches zero,
the strong reference is turned back into a weak reference.

### 参数

此函数没有参数。

### 返回值

Returns **`true`** if the reference was previously acquired and thus
could be released, **`false`** otherwise.

### 范例

**示例 \#1 <span class="methodname">Weakref::release</span> example**

``` php
<?php
class MyClass {
    public function __destruct() {
        echo "Destroying object!\n";
    }
}

$o1 = new MyClass;

$r1 = new Weakref($o1);

$r1->acquire();

echo "Unsetting o1...\n";
unset($o1);

$o2 = $r1->get();

$r1->release();

echo "Unsetting o2...\n";
unset($o2);
?>
```

以上例程会输出：

    Unsetting o1...
    Unsetting o2...
    Destroying object!

### 参见

-   <span class="methodname">Weakref::acquire</span>

Weakref::valid
==============

Checks whether the object referenced still exists

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Weakref::valid</span> ( <span
class="methodparam">void</span> )

Checks whether the object referenced still exists.

### 参数

此函数没有参数。

### 返回值

Returns **`true`** if the object still exists and is thus still
accessible via <span class="methodname">Weakref::get</span>, **`false`**
otherwise.

### 参见

-   <span class="methodname">Weakref::get</span>

简介
----

类摘要
------

**WeakMap**

<span class="ooclass"> class **WeakMap** </span> <span
class="oointerface">implements <span
class="interfacename">Countable</span> </span> <span
class="oointerface">, <span class="interfacename">ArrayAccess</span>
</span> <span class="oointerface">, <span
class="interfacename">Iterator</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">offsetExists</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">offsetGet</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetSet</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetUnset</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

范例
----

**示例 \#1 <span class="classname">Weakmap</span> usage example**

``` php
<?php
$wm = new WeakMap();

$o = new StdClass;

class A {
    public function __destruct() {
        echo "Dead!\n";
    }
}

$wm[$o] = new A;

var_dump(count($wm));
echo "Unsetting..\n";
unset($o);
echo "Done\n";
var_dump(count($wm));
```

以上例程会输出：

    int(1)
    Unsetting..
    Dead!
    Done
    int(0)

WeakMap::\_\_construct
======================

Constructs a new map

### 说明

<span class="modifier">public</span> <span
class="methodname">WeakMap::\_\_construct</span> ( <span
class="methodparam">void</span> )

Constructs a new map.

### 参数

此函数没有参数。

### 返回值

没有返回值。

WeakMap::count
==============

Counts the number of live entries in the map

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">WeakMap::count</span> ( <span
class="methodparam">void</span> )

Counts the number of live entries in the map.

### 参数

此函数没有参数。

### 返回值

Returns the number of live entries in the map.

WeakMap::current
================

Returns the current value under iteration

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">WeakMap::current</span> ( <span
class="methodparam">void</span> )

Returns the current value being iterated on in the map.

### 参数

此函数没有参数。

### 返回值

The value currently being iterated on.

WeakMap::key
============

Returns the current key under iteration

### 说明

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">WeakMap::key</span> ( <span
class="methodparam">void</span> )

Returns the object serving as key in the map, at the current iterating
position.

### 参数

此函数没有参数。

### 返回值

The object key currently being iterated.

WeakMap::next
=============

Advances to the next map element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">WeakMap::next</span> ( <span
class="methodparam">void</span> )

Advances to the next map element.

### 参数

此函数没有参数。

### 返回值

没有返回值。

WeakMap::offsetExists
=====================

Checks whether a certain object is in the map

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">WeakMap::offsetExists</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

Checks whether the passed object is referenced in the map.

### 参数

`object`  
Object to check for.

### 返回值

Returns **`true`** if the object is contained in the map, **`false`**
otherwise.

WeakMap::offsetGet
==================

Returns the value pointed to by a certain object

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">WeakMap::offsetGet</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

Returns the value pointed to by a certain object.

### 参数

`object`  
Some object contained as key in the map.

### 返回值

Returns the value associated to the object passed as argument,
**`null`** otherwise.

WeakMap::offsetSet
==================

Updates the map with a new key-value pair

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">WeakMap::offsetSet</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

Updates the map with a new key-value pair. If the key already existed in
the map, the old value is replaced with the new.

### 参数

`object`  
The object serving as key of the key-value pair.

`value`  
The arbitrary data serving as value of the key-value pair.

### 返回值

没有返回值。

WeakMap::offsetUnset
====================

Removes an entry from the map

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">WeakMap::offsetUnset</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

Removes an entry from the map.

### 参数

`object`  
The key object to remove from the map.

### 返回值

没有返回值。

WeakMap::rewind
===============

Rewinds the iterator to the beginning of the map

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">WeakMap::rewind</span> ( <span
class="methodparam">void</span> )

Rewinds the iterator to the beginning of the map.

### 参数

此函数没有参数。

### 返回值

没有返回值。

WeakMap::valid
==============

Returns whether the iterator is still on a valid map element

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">WeakMap::valid</span> ( <span
class="methodparam">void</span> )

Returns whether the iterator is still on a valid map element.

### 参数

此函数没有参数。

### 返回值

Returns **`true`** if the iterator is on a valid element that can be
accessed, **`false`** otherwise.
