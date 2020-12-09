Foreign Function Interface
==========================

**目录**

-   [简介](/intro/ffi.html)
-   [安装／配置](/ffi/setup.html)
    -   [需求](/ffi/setup.html#需求)
    -   [安装](/ffi/setup.html#安装)
    -   [运行时配置](/ffi/setup.html#运行时配置)
    -   [资源类型](/ffi/setup.html#资源类型)
-   [预定义常量](/ffi/constants.html)
-   [范例](/ffi/examples.html)
    -   [Basic FFI usage](/ffi/examples.html#Basic%20FFI%20usage)
    -   [PHP Callbacks](/ffi/examples.html#PHP%20Callbacks)
    -   [A Complete PHP/FFI/preloading
        Example](/ffi/examples.html#A%20Complete%20PHP/FFI/preloading%20Example)
-   [FFI](/class/ffi.html) — Main interface to C code and data
    -   [FFI::addr](/class/ffi.html#FFI::addr) — Creates an unmanaged
        pointer to C data
    -   [FFI::alignof](/class/ffi.html#FFI::alignof) — Gets the
        alignment
    -   [FFI::arrayType](/class/ffi.html#FFI::arrayType) — Dynamically
        constructs a new C array type
    -   [FFI::cast](/class/ffi.html#FFI::cast) — Performs a C type cast
    -   [FFI::cdef](/class/ffi.html#FFI::cdef) — Creates a new FFI
        object
    -   [FFI::free](/class/ffi.html#FFI::free) — Releases an unmanaged
        data structure
    -   [FFI::isNull](/class/ffi.html#FFI::isNull) — Checks whether a
        FFI\\CData is a null pointer
    -   [FFI::load](/class/ffi.html#FFI::load) — Loads C declarations
        from a C header file
    -   [FFI::memcmp](/class/ffi.html#FFI::memcmp) — Compares memory
        areas
    -   [FFI::memcpy](/class/ffi.html#FFI::memcpy) — Copies one memory
        area to another
    -   [FFI::memset](/class/ffi.html#FFI::memset) — Fills a memory area
    -   [FFI::new](/class/ffi.html#FFI::new) — Creates a C data
        structure
    -   [FFI::scope](/class/ffi.html#FFI::scope) — Instantiates an FFI
        object with C declarations parsed during preloading
    -   [FFI::sizeof](/class/ffi.html#FFI::sizeof) — Gets the size of C
        data or types
    -   [FFI::string](/class/ffi.html#FFI::string) — Creates a PHP
        string from a memory area
    -   [FFI::type](/class/ffi.html#FFI::type) — Creates an FFI\\CType
        object from a C declaration
    -   [FFI::typeof](/class/ffi.html#FFI::typeof) — Gets the FFI\\CType
        of FFI\\CData
-   [FFI\\CData](/class/ffi-cdata.html) — C Data Handles
-   [FFI\\CType](/class/ffi-ctype.html) — C Type Handles
-   [FFI\\Exception](/class/ffi-exception.html) — FFI Exceptions
-   [FFI\\ParserException](/class/ffi-parserexception.html) — FFI Parser
    Exceptions

简介
----

Objects of this class are created by the factory methods <span
class="methodname">FFI::cdef</span>, <span
class="methodname">FFI::load</span> or <span
class="methodname">FFI::scope</span>. Defined C variables are made
available as properties of the FFI instance, and defined C functions are
made available as methods of the FFI instance. Declared C types can be
used to create new C data structures using <span
class="methodname">FFI::new</span> and <span
class="methodname">FFI::type</span>.

FFI definition parsing and shared library loading may take significant
time. It is not useful to do it on each HTTP request in a Web
environment. However, it is possible to preload FFI definitions and
libraries at PHP startup, and to instantiate FFI objects when necessary.
Header files may be extended with special *FFI\_SCOPE* defines (e.g.
`#define FFI_SCOPE "foo"”"`; the default scope is "C") and then loaded
by <span class="methodname">FFI::load</span> during preloading. This
leads to the creation of a persistent binding, that will be available to
all the following requests through <span
class="methodname">FFI::scope</span>. Refer to the
<a href="/ffi/examples.html#A%20Complete%20PHP/FFI/preloading%20Example" class="link">complete PHP/FFI/preloading example</a>
for details.

It is possible to preload more than one C header file into the same
scope.

类摘要
------

**FFI**

<span class="ooclass"> class **FFI** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI\\CData</span>
<span class="methodname">addr</span> ( <span class="methodparam"><span
class="type">FFI\\CData</span> `&$ptr`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">alignof</span> ( <span class="methodparam"><span
class="type">mixed</span> `&$ptr`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI\\CType</span>
<span class="methodname">arrayType</span> ( <span
class="methodparam"><span class="type">FFI\\CType</span> `$type`</span>
, <span class="methodparam"><span class="type">array </span>
`$dims`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI\\CData</span>
<span class="methodname">cast</span> ( <span class="methodparam"><span
class="type">mixed</span> `$type`</span> , <span
class="methodparam"><span class="type">FFI\\CData</span> `&$ptr`</span>
)

<span class="modifier">public</span> <span
class="type">FFI\\CData</span> <span class="methodname">cast</span> (
<span class="methodparam"><span class="type">mixed</span> `$type`</span>
, <span class="methodparam"><span class="type">FFI\\CData</span>
`&$ptr`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI</span> <span
class="methodname">cdef</span> (\[ <span class="methodparam"><span
class="type">string</span> `$code`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$lib`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">free</span> ( <span class="methodparam"><span
class="type">FFI\\CData</span> `&$ptr`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isNull</span> ( <span class="methodparam"><span
class="type">FFI\\CData</span> `&$ptr`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI</span> <span
class="methodname">load</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">memcmp</span> ( <span class="methodparam"><span
class="type">mixed</span> `&$ptr1`</span> , <span
class="methodparam"><span class="type">mixed</span> `&$ptr2`</span> ,
<span class="methodparam"><span class="type">int</span> `$size`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">memcpy</span> ( <span class="methodparam"><span
class="type">FFI\\CData</span> `&$dst`</span> , <span
class="methodparam"><span class="type">mixed </span> `&$src`</span> ,
<span class="methodparam"><span class="type">int</span> `$size`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">memset</span> ( <span class="methodparam"><span
class="type">FFI\\CData</span> `&$ptr`</span> , <span
class="methodparam"><span class="type">int</span> `$ch`</span> , <span
class="methodparam"><span class="type">int</span> `$size`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI\\CData</span>
<span class="methodname">new</span> ( <span class="methodparam"><span
class="type">mixed</span> `$type`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$owned`<span
class="initializer"> = **`true`**</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$persistent`<span
class="initializer"> = **`false`**</span></span> \]\] )

<span class="modifier">public</span> <span
class="type">FFI\\CData</span> <span class="methodname">new</span> (
<span class="methodparam"><span class="type">mixed</span> `$type`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$owned`<span class="initializer"> = **`true`**</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$persistent`<span
class="initializer"> = **`false`**</span></span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI</span> <span
class="methodname">scope</span> ( <span class="methodparam"><span
class="type">string</span> `$scope_name`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">sizeof</span> ( <span class="methodparam"><span
class="type">mixed</span> `&$ptr`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">string</span> ( <span class="methodparam"><span
class="type">FFI\\CData</span> `&$ptr`</span> \[, <span
class="methodparam"><span class="type">int</span> `$size`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI\\CType</span>
<span class="methodname">type</span> ( <span class="methodparam"><span
class="type">mixed</span> `$type`</span> )

<span class="modifier">public</span> <span
class="type">FFI\\CType</span> <span class="methodname">type</span> (
<span class="methodparam"><span class="type">mixed</span> `$type`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI\\CType</span>
<span class="methodname">typeof</span> ( <span class="methodparam"><span
class="type">FFI\\CData</span> `&$ptr`</span> )

}

FFI::addr
=========

Creates an unmanaged pointer to C data

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI\\CData</span>
<span class="methodname">FFI::addr</span> ( <span
class="methodparam"><span class="type">FFI\\CData</span> `&$ptr`</span>
)

Creates an unmanaged pointer to the C data represented by the given
<span class="classname">FFI\\CData</span>. The source `ptr` must survive
the resulting pointer. This function is mainly useful to pass arguments
to C functions by pointer.

### 参数

`ptr`  
The handle of the pointer to a C data structure.

### 返回值

Returns the freshly created <span class="classname">FFI\\CData</span>
object.

FFI::alignof
============

Gets the alignment

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">FFI::alignof</span> ( <span class="methodparam"><span
class="type">mixed</span> `&$ptr`</span> )

Gets the alignment of the given <span
class="classname">FFI\\CData</span> or <span
class="classname">FFI\\CType</span> object.

### 参数

`ptr`  
The handle of the C data or type.

### 返回值

Returns the alignment of the given <span
class="classname">FFI\\CData</span> or <span
class="classname">FFI\\CType</span> object.

FFI::arrayType
==============

Dynamically constructs a new C array type

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI\\CType</span>
<span class="methodname">FFI::arrayType</span> ( <span
class="methodparam"><span class="type">FFI\\CType</span> `$type`</span>
, <span class="methodparam"><span class="type">array </span>
`$dims`</span> )

Dynamically constructs a new C array type with elements of type defined
by `type`, and dimensions specified by `dims`. In the following example
`$t1` and `$t2` are equivalent array types:

``` php
<?php
$t1 = FFI::type("int[2][3]");
$t2 = FFI::arrayType(FFI::type("int"), [2, 3]);
?>
```

### 参数

`type`  
A valid C declaration as <span class="type">string</span>, or an
instance of <span class="classname">FFI\\CType</span> which has already
been created.

`dims`  
The dimensions of the type as <span class="type">array</span>.

### 返回值

Returns the freshly created <span class="classname">FFI\\CType</span>
object.

FFI::cast
=========

Performs a C type cast

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI\\CData</span>
<span class="methodname">FFI::cast</span> ( <span
class="methodparam"><span class="type">mixed</span> `$type`</span> ,
<span class="methodparam"><span class="type">FFI\\CData</span>
`&$ptr`</span> )

<span class="modifier">public</span> <span
class="type">FFI\\CData</span> <span class="methodname">FFI::cast</span>
( <span class="methodparam"><span class="type">mixed</span>
`$type`</span> , <span class="methodparam"><span
class="type">FFI\\CData</span> `&$ptr`</span> )

<span class="methodname">FFI::cast</span> creates a new <span
class="classname">FFI\\CData</span> object, that references the same C
data structure, but is associated with a different type. The resulting
object does not own the C data, and the source `ptr` must survive the
result. The C type may be specified as a <span
class="type">string</span> with any valid C type declaration or as <span
class="classname">FFI\\CType</span> object, created before. If this
method is called statically, it must only use predefined C type names
(e.g. *int*, *char*, etc.); if the method is called as instance method,
any type declared for the instance is allowed.

### 参数

`type`  
A valid C declaration as <span class="type">string</span>, or an
instance of <span class="classname">FFI\\CType</span> which has already
been created.

`ptr`  
The handle of the pointer to a C data structure.

### 返回值

Returns the freshly created <span class="classname">FFI\\CData</span>
object.

FFI::cdef
=========

Creates a new FFI object

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI</span> <span
class="methodname">FFI::cdef</span> (\[ <span class="methodparam"><span
class="type">string</span> `$code`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$lib`</span> \]\] )

Creates a new FFI object.

### 参数

`code`  
A string containing a sequence of declarations in regular C language
(types, structures, functions, variables, etc). Actually, this string
may be copy-pasted from C header files.

> **Note**:
>
> C preprocessor directives are not supported, i.e. `#include`,
> `#define` and CPP macros do not work.

`lib`  
The name of a shared library file, to be loaded and linked with the
definitions.

> **Note**:
>
> If `lib` is omitted, platforms supporting *RTLD\_DEFAULT* attempt to
> lookup symbols declared in `code` in the normal global scope. Other
> systems will fail to resolve these symbols.

### 返回值

Returns the freshly created <span class="classname">FFI</span> object.

FFI::free
=========

Releases an unmanaged data structure

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">FFI::free</span> ( <span class="methodparam"><span
class="type">FFI\\CData</span> `&$ptr`</span> )

Manually releases a previously created unmanaged data structure.

### 参数

`ptr`  
The handle of the unmanaged pointer to a C data structure.

### 返回值

没有返回值。

FFI::isNull
===========

Checks whether a FFI\\CData is a null pointer

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">FFI::isNull</span> ( <span class="methodparam"><span
class="type">FFI\\CData</span> `&$ptr`</span> )

Checks whether a FFI\\CData is a null pointer.

### 参数

`ptr`  
The handle of the pointer to a C data structure.

### 返回值

Returns whether a FFI\\CData is a null pointer.

FFI::load
=========

Loads C declarations from a C header file

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI</span> <span
class="methodname">FFI::load</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

Loads C declarations from a C header file. It is possible to specify
shared libraries that should be loaded, using special *FFI\_LIB* defines
in the loaded C header file.

### 参数

`filename`  
The name of a C header file.

C preprocessor directives are not supported, i.e. *\#include*,
*\#define* and CPP macros do not work, except for special cases listed
below.

The header file *should* contain a *\#define* statement for the
*FFI\_SCOPE* variable, e.g.: `#define FFI_SCOPE "MYLIB"`. Refer to the
<a href="/class/ffi.html#简介" class="link">class introduction</a> for
details.

The header file *may* contain a *\#define* statement for the *FFI\_LIB*
variable to specify the library it exposes. If it is a system library
only the file name is required, e.g.:
`#define FFI_LIB       "libc.so.6"`. If it is a custom library, a
relative path is required, e.g.: `#define FFI_LIB "./mylib.so"`.

### 返回值

Returns the freshly created <span class="classname">FFI</span> object.

### 参见

-   <span class="methodname">FFI::scope</span>

FFI::memcmp
===========

Compares memory areas

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">FFI::memcmp</span> ( <span class="methodparam"><span
class="type">mixed</span> `&$ptr1`</span> , <span
class="methodparam"><span class="type">mixed</span> `&$ptr2`</span> ,
<span class="methodparam"><span class="type">int</span> `$size`</span> )

Compares `size` bytes from the memory areas `ptr1` and `ptr2`. Both
`ptr1` and `ptr2` can be any native data structures (<span
class="classname">FFI\\CData</span>) or PHP <span
class="type">string</span>s.

### 参数

`ptr1`  
The start of one memory area.

`ptr2`  
The start of another memory area.

`size`  
The number of bytes to compare.

### 返回值

Returns \< *0* if the contents of the memory area starting at `ptr1` are
considered less than the contents of the memory area starting at `ptr2`,
\> *0* if the contents of the first memory area are considered greater
than the second, and *0* if they are equal.

FFI::memcpy
===========

Copies one memory area to another

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">FFI::memcpy</span> ( <span class="methodparam"><span
class="type">FFI\\CData</span> `&$dst`</span> , <span
class="methodparam"><span class="type">mixed </span> `&$src`</span> ,
<span class="methodparam"><span class="type">int</span> `$size`</span> )

Copies `size` bytes from the memory area `src` to the memory area `dst`.
Both `src` and `dst` can be any native data structures (<span
class="classname">FFI\\CData</span>) or PHP <span
class="type">string</span>s.

### 参数

`dst`  
The start of the memory area to copy to.

`src`  
The start of the memory area to copy from.

`size`  
The number of bytes to copy.

### 返回值

没有返回值。

FFI::memset
===========

Fills a memory area

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">FFI::memset</span> ( <span class="methodparam"><span
class="type">FFI\\CData</span> `&$ptr`</span> , <span
class="methodparam"><span class="type">int</span> `$ch`</span> , <span
class="methodparam"><span class="type">int</span> `$size`</span> )

Fills `size` bytes of the memory area pointed to by `ptr` with the given
byte `ch`.

### 参数

`ptr`  
The start of the memory area to fill.

`ch`  
The byte to fill with.

`size`  
The number of bytes to fill.

### 返回值

没有返回值。

FFI::new
========

Creates a C data structure

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI\\CData</span>
<span class="methodname">FFI::new</span> ( <span
class="methodparam"><span class="type">mixed</span> `$type`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$owned`<span
class="initializer"> = **`true`**</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$persistent`<span
class="initializer"> = **`false`**</span></span> \]\] )

<span class="modifier">public</span> <span
class="type">FFI\\CData</span> <span class="methodname">FFI::new</span>
( <span class="methodparam"><span class="type">mixed</span>
`$type`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$owned`<span class="initializer"> =
**`true`**</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$persistent`<span class="initializer"> =
**`false`**</span></span> \]\] )

Creates a native data structure of the given C type. If this method is
called statically, it must only use predefined C type names (e.g. *int*,
*char*, etc.); if the method is called as instance method, any type
declared for the instance is allowed.

### 参数

`type`  
`type` is a valid C declaration as <span class="type">string</span>, or
an instance of <span class="classname">FFI\\CType</span> which has
already been created.

`owned`  
Whether to create owned (i.e. managed) or unmanaged data. Managed data
lives together with the returned <span
class="classname">FFI\\CData</span> object, and is released when the
last reference to that object is released by regular PHP reference
counting or GC. Unmanaged data should be released by calling <span
class="methodname">FFI::free</span>, when no longer needed.

`persistent`  
Whether to allocate the C data structure permanently on the system heap
(using <span class="function">malloc</span>), or on the PHP request heap
(using <span class="function">emalloc</span>).

### 返回值

Returns the freshly created <span class="classname">FFI\\CData</span>
object.

FFI::scope
==========

Instantiates an FFI object with C declarations parsed during preloading

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI</span> <span
class="methodname">FFI::scope</span> ( <span class="methodparam"><span
class="type">string</span> `$scope_name`</span> )

Instantiates an FFI object with C declarations parsed during preloading.

The <span class="methodname">FFI::scope</span> method is safe to call
multiple times for the same scope. Multiple references to the same scope
may be loaded at the same time.

### 参数

`scope_name`  
The scope name defined by a special *FFI\_SCOPE* define.

### 返回值

Returns the freshly created <span class="classname">FFI</span> object.

### 参见

-   <span class="methodname">FFI::load</span>

FFI::sizeof
===========

Gets the size of C data or types

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">FFI::sizeof</span> ( <span class="methodparam"><span
class="type">mixed</span> `&$ptr`</span> )

Returns the size of the given <span class="classname">FFI\\CData</span>
or <span class="classname">FFI\\CType</span> object.

### 参数

`ptr`  
The handle of the C data or type.

### 返回值

The size of the memory area pointed at by `ptr`.

FFI::string
===========

Creates a PHP string from a memory area

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">FFI::string</span> ( <span class="methodparam"><span
class="type">FFI\\CData</span> `&$ptr`</span> \[, <span
class="methodparam"><span class="type">int</span> `$size`</span> \] )

Creates a PHP <span class="type">string</span> from `size` bytes of the
memory area pointed to by `ptr`.

### 参数

`ptr`  
The start of the memory area from which to create a <span
class="type">string</span>.

`size`  
The number of bytes to copy to the <span class="type">string</span>. If
`size` is omitted, `ptr` must be a zero terminated array of C *chars*.

### 返回值

The freshly created PHP <span class="type">string</span>.

FFI::type
=========

Creates an FFI\\CType object from a C declaration

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI\\CType</span>
<span class="methodname">FFI::type</span> ( <span
class="methodparam"><span class="type">mixed</span> `$type`</span> )

<span class="modifier">public</span> <span
class="type">FFI\\CType</span> <span class="methodname">FFI::type</span>
( <span class="methodparam"><span class="type">mixed</span>
`$type`</span> )

This function creates and returns a <span
class="classname">FFI\\CType</span> object for the given <span
class="type">string</span> containing a C type declaration. If this
method is called statically, it must only use predefined C type names
(e.g. *int*, *char*, etc.); if the method is called as instance method,
any type declared for the instance is allowed.

### 参数

`type`  
A valid C declaration as <span class="type">string</span>, or an
instance of <span class="classname">FFI\\CType</span> which has already
been created.

### 返回值

Returns the freshly created <span class="classname">FFI\\CType</span>
object.

FFI::typeof
===========

Gets the FFI\\CType of FFI\\CData

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">FFI\\CType</span>
<span class="methodname">FFI::typeof</span> ( <span
class="methodparam"><span class="type">FFI\\CData</span> `&$ptr`</span>
)

Gets the <span class="classname">FFI\\CType</span> object representing
the type of the given <span class="classname">FFI\\CData</span> object.

### 参数

`ptr`  
The handle of the pointer to a C data structure.

### 返回值

Returns the <span class="classname">FFI\\CType</span> object
representing the type of the given <span
class="classname">FFI\\CData</span> object.

简介
----

<span class="classname">FFI\\CData</span> objects can be used in a
number of ways as a regular PHP data:

-   <span class="simpara"> C data of scalar types can be read and
    assigned via the <span class="property">$cdata</span> property, e.g.
    `$x = FFI::new('int'); $x->cdata = 42;` </span>
-   <span class="simpara"> C struct and union fields can be accessed as
    regular PHP object property, e.g. `$cdata->field` </span>
-   <span class="simpara"> C array elements can be accessed as regular
    PHP array elements, e.g. `$cdata[$offset]` </span>
-   <span class="simpara"> C arrays can be iterated using
    <a href="/control-structures/foreach.html" class="link">foreach</a>
    statements. </span>
-   <span class="simpara"> C arrays can be used as arguments of <span
    class="function">count</span>. </span>
-   <span class="simpara"> C pointers can be dereferenced as arrays,
    e.g. `$cdata[0]` </span>
-   <span class="simpara"> C pointers can be compared using regular
    comparison operators (`<`, `<=`, `==`, `!=`, `>=`, `>`). </span>
-   <span class="simpara"> C pointers can be incremented and decremented
    using regular `+`/`-`/ `++`/`–-` operations, e.g. `$cdata += 5`
    </span>
-   <span class="simpara"> C pointers can be subtracted from another
    using regular `-` operations. </span>
-   <span class="simpara"> C pointers to functions can be called as a
    regular PHP closure, e.g. `$cdata()` </span>
-   <span class="simpara"> Any C data can be duplicated using the
    <a href="/language/oop5/cloning.html" class="link">clone</a>
    operator, e.g. `$cdata2 = clone $cdata;` </span>
-   <span class="simpara"> Any C data can be visualized using <span
    class="function">var\_dump</span>, <span
    class="function">print\_r</span>, etc. </span>

> **Note**: <span class="simpara"> Notable limitations are that <span
> class="classname">FFI\\CData</span> instances do not support <span
> class="function">isset</span>, <span class="function">empty</span> and
> <span class="function">unset</span>, and that wrapped C structs and
> unions do not implement <span
> class="interfacename">Traversable</span>. </span>

类摘要
------

**FFI\\CData**

<span class="ooclass"> class **FFI\\CData** </span> {

}

简介
----

类摘要
------

**FFI\\CType**

<span class="ooclass"> class **FFI\\CType** </span> {

}

简介
----

类摘要
------

**FFI\\Exception**

<span class="ooclass"> class **FFI\\Exception** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Error** </span>
<span class="oointerface">implements <span
class="interfacename">Throwable</span> </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Error::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Error::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Error::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Error::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Error::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Error::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

类摘要
------

**FFI\\ParserException**

<span class="ooclass"> class **FFI\\ParserException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**FFI\\Exception** </span> <span class="oointerface">implements <span
class="interfacename">Throwable</span> </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

}
