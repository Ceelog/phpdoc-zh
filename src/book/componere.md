Componere
=========

**目录**

-   [简介](/intro/componere.html)
-   [安装／配置](/componere/setup.html)
    -   [需求](/componere/setup.html#需求)
    -   [安装](/componere/setup.html#安装)
-   [Componere\\Abstract\\Definition](/class/componere-abstract-definition.html)
    — The Componere\\Abstract\\Definition class
    -   [Componere\\Abstract\\Definition::addInterface](/class/componere-abstract-definition.html#Componere\Abstract\Definition::addInterface)
        — Add Interface
    -   [Componere\\Abstract\\Definition::addMethod](/class/componere-abstract-definition.html#Componere\Abstract\Definition::addMethod)
        — Add Method
    -   [Componere\\Abstract\\Definition::addTrait](/class/componere-abstract-definition.html#Componere\Abstract\Definition::addTrait)
        — Add Trait
    -   [Componere\\Abstract\\Definition::getReflector](/class/componere-abstract-definition.html#Componere\Abstract\Definition::getReflector)
        — Reflection
-   [Componere\\Definition](/class/componere-definition.html) — The
    Componere\\Definition class
    -   [Componere\\Definition::\_\_construct](/class/componere-definition.html#Componere\Definition::__construct)
        — Definition Construction
    -   [Componere\\Definition::addConstant](/class/componere-definition.html#Componere\Definition::addConstant)
        — Add Constant
    -   [Componere\\Definition::addProperty](/class/componere-definition.html#Componere\Definition::addProperty)
        — Add Property
    -   [Componere\\Definition::register](/class/componere-definition.html#Componere\Definition::register)
        — Registration
    -   [Componere\\Definition::isRegistered](/class/componere-definition.html#Componere\Definition::isRegistered)
        — State Detection
    -   [Componere\\Definition::getClosure](/class/componere-definition.html#Componere\Definition::getClosure)
        — Get Closure
    -   [Componere\\Definition::getClosures](/class/componere-definition.html#Componere\Definition::getClosures)
        — Get Closures
-   [Componere\\Patch](/class/componere-patch.html) — The
    Componere\\Patch class
    -   [Componere\\Patch::\_\_construct](/class/componere-patch.html#Componere\Patch::__construct)
        — Patch Construction
    -   [Componere\\Patch::apply](/class/componere-patch.html#Componere\Patch::apply)
        — Application
    -   [Componere\\Patch::revert](/class/componere-patch.html#Componere\Patch::revert)
        — Reversal
    -   [Componere\\Patch::isApplied](/class/componere-patch.html#Componere\Patch::isApplied)
        — State Detection
    -   [Componere\\Patch::derive](/class/componere-patch.html#Componere\Patch::derive)
        — Patch Derivation
    -   [Componere\\Patch::getClosure](/class/componere-patch.html#Componere\Patch::getClosure)
        — Get Closure
    -   [Componere\\Patch::getClosures](/class/componere-patch.html#Componere\Patch::getClosures)
        — Get Closures
-   [Componere\\Method](/class/componere-method.html) — The
    Componere\\Method class
    -   [Componere\\Method::\_\_construct](/class/componere-method.html#Componere\Method::__construct)
        — Method Construction
    -   [Componere\\Method::setPrivate](/class/componere-method.html#Componere\Method::setPrivate)
        — Accessibility Modification
    -   [Componere\\Method::setProtected](/class/componere-method.html#Componere\Method::setProtected)
        — Accessibility Modification
    -   [Componere\\Method::setStatic](/class/componere-method.html#Componere\Method::setStatic)
        — Accessibility Modification
    -   [Componere\\Method::getReflector](/class/componere-method.html#Componere\Method::getReflector)
        — Reflection
-   [Componere\\Value](/class/componere-value.html) — The
    Componere\\Value class
    -   [Componere\\Value::\_\_construct](/class/componere-value.html#Componere\Value::__construct)
        — Value Construction
    -   [Componere\\Value::setPrivate](/class/componere-value.html#Componere\Value::setPrivate)
        — Accessibility Modification
    -   [Componere\\Value::setProtected](/class/componere-value.html#Componere\Value::setProtected)
        — Accessibility Modification
    -   [Componere\\Value::setStatic](/class/componere-value.html#Componere\Value::setStatic)
        — Accessibility Modification
    -   [Componere\\Value::isPrivate](/class/componere-value.html#Componere\Value::isPrivate)
        — Accessibility Detection
    -   [Componere\\Value::isProtected](/class/componere-value.html#Componere\Value::isProtected)
        — Accessibility Detection
    -   [Componere\\Value::isStatic](/class/componere-value.html#Componere\Value::isStatic)
        — Accessibility Detection
    -   [Componere\\Value::hasDefault](/class/componere-value.html#Componere\Value::hasDefault)
        — Value Interaction
-   [Componere 函数](/reference/componere.html)
    -   [Componere\\cast](/reference/componere.html#Componere\cast) —
        Casting
    -   [Componere\\cast\_by\_ref](/reference/componere.html#Componere\cast_by_ref)
        — Casting

简介
----

This final abstract represents a class entry, and should not be used by
the programmer.

类摘要
------

**Componere\\Abstract\\Definition**

<span class="ooclass"> <span class="modifier">final</span> <span
class="modifier">abstract</span> class
**Componere\\Abstract\\Definition** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">addInterface</span> ( <span class="methodparam"><span
class="type">string</span> `$interface`</span> )

<span class="modifier">public</span> <span
class="type">Definition</span> <span class="methodname">addMethod</span>
( <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">\\Componere\\Method</span> `$method`</span> )

<span class="modifier">public</span> <span
class="type">Definition</span> <span class="methodname">addTrait</span>
( <span class="methodparam"><span class="type">string</span>
`$trait`</span> )

<span class="modifier">public</span> <span
class="type">\\ReflectionClass</span> <span
class="methodname">getReflector</span> ( <span
class="methodparam">void</span> )

}

Componere\\Abstract\\Definition::addInterface
=============================================

Add Interface

### 说明

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">Componere\\Abstract\\Definition::addInterface</span>
( <span class="methodparam"><span class="type">string</span>
`$interface`</span> )

Shall implement the given interface on the current definition

### 参数

`interface`  
The case insensitive name of an interface

### 返回值

The current Definition

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if <span
class="type">Definition</span> was registered

Componere\\Abstract\\Definition::addMethod
==========================================

Add Method

### 说明

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">Componere\\Abstract\\Definition::addMethod</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">\\Componere\\Method</span> `$method`</span> )

Shall create or override a method on the current definition.

### 参数

`name`  
The case insensitive name for method

`method`  
<span class="type">\\Componere\\Method</span> not previously added to
another <span class="type">Definition</span>

### 返回值

The current Definition

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if <span
class="type">Definition</span> was registered

**Warning**

Shall throw <span class="type">RuntimeException</span> if Method was
added to another Definition

Componere\\Abstract\\Definition::addTrait
=========================================

Add Trait

### 说明

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">Componere\\Abstract\\Definition::addTrait</span> (
<span class="methodparam"><span class="type">string</span>
`$trait`</span> )

Shall use the given trait for the current definition

### 参数

`trait`  
The case insensitive name of a trait

### 返回值

The current Definition

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if <span
class="type">Definition</span> was registered

Componere\\Abstract\\Definition::getReflector
=============================================

Reflection

### 说明

<span class="modifier">public</span> <span
class="type">\\ReflectionClass</span> <span
class="methodname">Componere\\Abstract\\Definition::getReflector</span>
( <span class="methodparam">void</span> )

Shall create or return a ReflectionClass

### 返回值

A ReflectionClass for the current definition (cached)

简介
----

The Definition class allows the programmer to build and register a type
at runtime.

Should a Definition replace an existing class, the existing class will
be restored when the Definition is destroyed.

类摘要
------

**Componere\\Definition**

<span class="ooclass"> <span class="modifier">final</span> class
**Componere\\Definition** </span> <span class="ooclass"> <span
class="modifier">extends</span> **Componere\\Abstract\\Definition**
</span> {

/\* Constructors \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$parent`</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">array</span>
`$interfaces`</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$parent`</span> , <span class="methodparam"><span
class="type">array</span> `$interfaces`</span> )

/\* 方法 \*/

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">addConstant</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type">\\Componere\\Value</span>
`$value`</span> )

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">addProperty</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type">\\Componere\\Value</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">register</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isRegistered</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">\\Closure</span>
<span class="methodname">getClosure</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getClosures</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">Componere\\Abstract\\Definition::addInterface</span>
( <span class="methodparam"><span class="type">string</span>
`$interface`</span> )

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">Componere\\Abstract\\Definition::addMethod</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">\\Componere\\Method</span> `$method`</span> )

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">Componere\\Abstract\\Definition::addTrait</span> (
<span class="methodparam"><span class="type">string</span>
`$trait`</span> )

<span class="modifier">public</span> <span
class="type">\\ReflectionClass</span> <span
class="methodname">Componere\\Abstract\\Definition::getReflector</span>
( <span class="methodparam">void</span> )

}

Componere\\Definition::\_\_construct
====================================

Definition Construction

### 说明

<span class="modifier">public</span> <span
class="methodname">Componere\\Definition::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="methodname">Componere\\Definition::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$parent`</span> )

<span class="modifier">public</span> <span
class="methodname">Componere\\Definition::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">array</span>
`$interfaces`</span> )

<span class="modifier">public</span> <span
class="methodname">Componere\\Definition::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$parent`</span> , <span class="methodparam"><span
class="type">array</span> `$interfaces`</span> )

### 参数

`name`  
A case insensitive class name

`parent`  
A case insensitive class name

`interfaces`  
An array of case insensitive class names

### Exceptions

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if an
attempt is made to replace an internal class

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if an
attempt is made to replace an interface

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if an
attempt is made to replace a trait

**Warning**

Shall throw <span class="type">RuntimeException</span> if a class in
`interfaces` cannot be found

**Warning**

Shall throw <span class="type">RuntimeException</span> if an class in
`interfaces` is not an interface

Componere\\Definition::addConstant
==================================

Add Constant

### 说明

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">Componere\\Definition::addConstant</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">\\Componere\\Value</span>
`$value`</span> )

Shall declare a class constant on the current Definition

### 参数

`name`  
The case sensitive name for the constant

`value`  
The Value for the constant, must not be undefined or static

### 返回值

The current Definition

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if <span
class="type">Definition</span> was registered

**Warning**

Shall throw <span class="type">RuntimeException</span> if `name` is
already declared as a constant

**Warning**

Shall throw <span class="type">RuntimeException</span> if `value` is
static

**Warning**

Shall throw <span class="type">RuntimeException</span> if `value` is
undefined

Componere\\Definition::addProperty
==================================

Add Property

### 说明

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">Componere\\Definition::addProperty</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">\\Componere\\Value</span>
`$value`</span> )

Shall declare a class property on the current Definition

### 参数

`name`  
The case sensitive name for the property

`value`  
The default Value for the property

### 返回值

The current Definition

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if <span
class="type">Definition</span> was registered

**Warning**

Shall throw <span class="type">RuntimeException</span> if `name` is
already declared as a property

Componere\\Definition::register
===============================

Registration

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Componere\\Definition::register</span> ( <span
class="methodparam">void</span> )

Shall register the current Definition

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if <span
class="type">Definition</span> was registered

Componere\\Definition::isRegistered
===================================

State Detection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Componere\\Definition::isRegistered</span> (
<span class="methodparam">void</span> )

Shall detect the registration state of this Definition

### 返回值

Shall return true if this Definition is registered

Componere\\Definition::getClosure
=================================

Get Closure

### 说明

<span class="modifier">public</span> <span class="type">\\Closure</span>
<span class="methodname">Componere\\Definition::getClosure</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

Shall return a Closure for the method specified by name

### 参数

`name`  
The case insensitive name of the method

### 返回值

A Closure bound to the correct scope

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if <span
class="type">Definition</span> was registered

**Warning**

Shall throw <span class="type">RuntimeException</span> if `name` could
not be found

Componere\\Definition::getClosures
==================================

Get Closures

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Componere\\Definition::getClosures</span> (
<span class="methodparam">void</span> )

Shall return an array of Closures

### 返回值

Shall return all methods as an array of Closure objects bound to the
correct scope

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if <span
class="type">Definition</span> was registered

简介
----

The Patch class allows the programmer to change the type of an instance
at runtime without registering a new Definition

When a Patch is destroyed it is reverted, so that instances that were
patched during the lifetime of the Patch are restored to their formal
type.

类摘要
------

**Componere\\Patch**

<span class="ooclass"> <span class="modifier">final</span> class
**Componere\\Patch** </span> <span class="ooclass"> <span
class="modifier">extends</span> **Componere\\Abstract\\Definition**
</span> {

/\* Constructors \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">object</span> `$instance`</span>
)

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">object</span> `$instance`</span>
, <span class="methodparam"><span class="type">array</span>
`$interfaces`</span> )

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">apply</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">revert</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isApplied</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Patch</span>
<span class="methodname">derive</span> ( <span class="methodparam"><span
class="type">object</span> `$instance`</span> )

<span class="modifier">public</span> <span class="type">\\Closure</span>
<span class="methodname">getClosure</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getClosures</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">Componere\\Abstract\\Definition::addInterface</span>
( <span class="methodparam"><span class="type">string</span>
`$interface`</span> )

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">Componere\\Abstract\\Definition::addMethod</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">\\Componere\\Method</span> `$method`</span> )

<span class="modifier">public</span> <span
class="type">Definition</span> <span
class="methodname">Componere\\Abstract\\Definition::addTrait</span> (
<span class="methodparam"><span class="type">string</span>
`$trait`</span> )

<span class="modifier">public</span> <span
class="type">\\ReflectionClass</span> <span
class="methodname">Componere\\Abstract\\Definition::getReflector</span>
( <span class="methodparam">void</span> )

}

Componere\\Patch::\_\_construct
===============================

Patch Construction

### 说明

<span class="modifier">public</span> <span
class="methodname">Componere\\Patch::\_\_construct</span> ( <span
class="methodparam"><span class="type">object</span> `$instance`</span>
)

<span class="modifier">public</span> <span
class="methodname">Componere\\Patch::\_\_construct</span> ( <span
class="methodparam"><span class="type">object</span> `$instance`</span>
, <span class="methodparam"><span class="type">array</span>
`$interfaces`</span> )

### 参数

`instance`  
The target for this Patch

`interfaces`  
A case insensitive array of class names

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if a class in
`interfaces` cannot be found

**Warning**

Shall throw <span class="type">RuntimeException</span> if an class in
`interfaces` is not an interface

Componere\\Patch::apply
=======================

Application

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Componere\\Patch::apply</span> ( <span
class="methodparam">void</span> )

Shall apply the current patch

Componere\\Patch::revert
========================

Reversal

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Componere\\Patch::revert</span> ( <span
class="methodparam">void</span> )

Shall revert the current patch

Componere\\Patch::isApplied
===========================

State Detection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Componere\\Patch::isApplied</span> ( <span
class="methodparam">void</span> )

Componere\\Patch::derive
========================

Patch Derivation

### 说明

<span class="modifier">public</span> <span class="type">Patch</span>
<span class="methodname">Componere\\Patch::derive</span> ( <span
class="methodparam"><span class="type">object</span> `$instance`</span>
)

Shall derive a <span class="type">Patch</span> for the given `instance`

### 参数

`instance`  
The target for the derived Patch

### 返回值

<span class="type">Patch</span> for `instance` derived from the current
<span class="type">Patch</span>

### Exceptions

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if
`instance` is not compatible

Componere\\Patch::getClosure
============================

Get Closure

### 说明

<span class="modifier">public</span> <span class="type">\\Closure</span>
<span class="methodname">Componere\\Patch::getClosure</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Shall return a Closure for the method specified by name

### 参数

`name`  
The case insensitive name of the method

### 返回值

A Closure bound to the correct scope and object

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if `name` could
not be found

Componere\\Patch::getClosures
=============================

Get Closures

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Componere\\Patch::getClosures</span> ( <span
class="methodparam">void</span> )

Shall return an array of Closures

### 返回值

Shall return all methods as an array of Closure objects bound to the
correct scope and object

简介
----

A Method represents a function with modifiable accessibility flags

类摘要
------

**Componere\\Method**

<span class="ooclass"> <span class="modifier">final</span> class
**Componere\\Method** </span> {

/\* Constructor \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">\\Closure</span>
`$closure`</span> )

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">Method</span>
<span class="methodname">setPrivate</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Method</span>
<span class="methodname">setProtected</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Method</span>
<span class="methodname">setStatic</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">\\ReflectionMethod</span> <span
class="methodname">getReflector</span> ( <span
class="methodparam">void</span> )

}

Componere\\Method::\_\_construct
================================

Method Construction

### 说明

<span class="modifier">public</span> <span
class="methodname">Componere\\Method::\_\_construct</span> ( <span
class="methodparam"><span class="type">\\Closure</span>
`$closure`</span> )

### 参数

`closure`  

Componere\\Method::setPrivate
=============================

Accessibility Modification

### 说明

<span class="modifier">public</span> <span class="type">Method</span>
<span class="methodname">Componere\\Method::setPrivate</span> ( <span
class="methodparam">void</span> )

### 返回值

The current Method

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if access level
was previously set

Componere\\Method::setProtected
===============================

Accessibility Modification

### 说明

<span class="modifier">public</span> <span class="type">Method</span>
<span class="methodname">Componere\\Method::setProtected</span> ( <span
class="methodparam">void</span> )

### 返回值

The current Method

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if access level
was previously set

Componere\\Method::setStatic
============================

Accessibility Modification

### 说明

<span class="modifier">public</span> <span class="type">Method</span>
<span class="methodname">Componere\\Method::setStatic</span> ( <span
class="methodparam">void</span> )

### 返回值

The current Method

Componere\\Method::getReflector
===============================

Reflection

### 说明

<span class="modifier">public</span> <span
class="type">\\ReflectionMethod</span> <span
class="methodname">Componere\\Method::getReflector</span> ( <span
class="methodparam">void</span> )

Shall create or return a ReflectionMethod

### 返回值

A ReflectionMethod for the current method (cached)

简介
----

A Value represents a PHP variable of all types, including undefined

类摘要
------

**Componere\\Value**

<span class="ooclass"> <span class="modifier">final</span> class
**Componere\\Value** </span> {

/\* Constructor \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span class="methodparam">
`$default`</span> \] )

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">Value</span>
<span class="methodname">setPrivate</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Value</span>
<span class="methodname">setProtected</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Value</span>
<span class="methodname">setStatic</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isPrivate</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isProtected</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isStatic</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasDefault</span> ( <span
class="methodparam">void</span> )

}

Componere\\Value::\_\_construct
===============================

Value Construction

### 说明

<span class="modifier">public</span> <span
class="methodname">Componere\\Value::\_\_construct</span> (\[ <span
class="methodparam"> `$default`</span> \] )

### 参数

`default`  

### Exceptions

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if
`default` does not have a suitable value

Componere\\Value::setPrivate
============================

Accessibility Modification

### 说明

<span class="modifier">public</span> <span class="type">Value</span>
<span class="methodname">Componere\\Value::setPrivate</span> ( <span
class="methodparam">void</span> )

### 返回值

The current Value

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if access level
was previously set

Componere\\Value::setProtected
==============================

Accessibility Modification

### 说明

<span class="modifier">public</span> <span class="type">Value</span>
<span class="methodname">Componere\\Value::setProtected</span> ( <span
class="methodparam">void</span> )

### 返回值

The current Value

### Exceptions

**Warning**

Shall throw <span class="type">RuntimeException</span> if access level
was previously set

Componere\\Value::setStatic
===========================

Accessibility Modification

### 说明

<span class="modifier">public</span> <span class="type">Value</span>
<span class="methodname">Componere\\Value::setStatic</span> ( <span
class="methodparam">void</span> )

### 返回值

The current Value

Componere\\Value::isPrivate
===========================

Accessibility Detection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Componere\\Value::isPrivate</span> ( <span
class="methodparam">void</span> )

Componere\\Value::isProtected
=============================

Accessibility Detection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Componere\\Value::isProtected</span> ( <span
class="methodparam">void</span> )

Componere\\Value::isStatic
==========================

Accessibility Detection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Componere\\Value::isStatic</span> ( <span
class="methodparam">void</span> )

Componere\\Value::hasDefault
============================

Value Interaction

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Componere\\Value::hasDefault</span> ( <span
class="methodparam">void</span> )
