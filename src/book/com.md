COM and .Net (Windows)
======================

**目录**

-   [简介](/intro/com.html)
-   [安装／配置](/com/setup.html)
    -   [需求](/com/setup.html#需求)
    -   [安装](/com/setup.html#安装)
    -   [运行时配置](/com/setup.html#运行时配置)
    -   [资源类型](/com/setup.html#资源类型)
-   [预定义常量](/com/constants.html)
-   [Errors and error handling](/com/error-handling.html)
-   [范例](/com/examples.html)
    -   [For Each](/com/examples.html#For%20Each)
    -   [Arrays and Array-style COM
        properties](/com/examples.html#Arrays%20and%20Array-style%20COM%20properties)
-   [com](/class/com.html) — The com class
    -   [com::\_\_construct](/class/com.html#com::__construct) — com
        class constructor
-   [dotnet](/class/dotnet.html) — The dotnet class
    -   [dotnet::\_\_construct](/class/dotnet.html#dotnet::__construct)
        — dotnet class constructor
-   [variant](/class/variant.html) — variant class
    -   [variant::\_\_construct](/class/variant.html#variant::__construct)
        — variant class constructor
-   [COMPersistHelper](/class/compersisthelper.html) — The
    COMPersistHelper class
    -   [COMPersistHelper::\_\_construct](/class/compersisthelper.html#COMPersistHelper::__construct)
        — Construct a COMPersistHelper object
    -   [COMPersistHelper::GetCurFileName](/class/compersisthelper.html#COMPersistHelper::GetCurFileName)
        — Get current filename
    -   [COMPersistHelper::GetMaxStreamSize](/class/compersisthelper.html#COMPersistHelper::GetMaxStreamSize)
        — Get maximum stream size
    -   [COMPersistHelper::InitNew](/class/compersisthelper.html#COMPersistHelper::InitNew)
        — Initialize object to default state
    -   [COMPersistHelper::LoadFromFile](/class/compersisthelper.html#COMPersistHelper::LoadFromFile)
        — Load object from file
    -   [COMPersistHelper::LoadFromStream](/class/compersisthelper.html#COMPersistHelper::LoadFromStream)
        — Load object from stream
    -   [COMPersistHelper::SaveToFile](/class/compersisthelper.html#COMPersistHelper::SaveToFile)
        — Save object to file
    -   [COMPersistHelper::SaveToStream](/class/compersisthelper.html#COMPersistHelper::SaveToStream)
        — Save object to stream
-   [com\_exception](/class/com-exception.html) — The com\_exception
    class
-   [COM 函数](/ref/com.html)
    -   [com\_create\_guid](/ref/com.html#com_create_guid) — Generate a
        globally unique identifier (GUID)
    -   [com\_event\_sink](/ref/com.html#com_event_sink) — Connect
        events from a COM object to a PHP object
    -   [com\_get\_active\_object](/ref/com.html#com_get_active_object)
        — Returns a handle to an already running instance of a COM
        object
    -   [com\_load\_typelib](/ref/com.html#com_load_typelib) — 装载一个
        Typelib
    -   [com\_message\_pump](/ref/com.html#com_message_pump) — Process
        COM messages, sleeping for up to timeoutms milliseconds
    -   [com\_print\_typeinfo](/ref/com.html#com_print_typeinfo) — Print
        out a PHP class definition for a dispatchable interface
    -   [variant\_abs](/ref/com.html#variant_abs) — Returns the absolute
        value of a variant
    -   [variant\_add](/ref/com.html#variant_add) — "Adds" two variant
        values together and returns the result
    -   [variant\_and](/ref/com.html#variant_and) — Performs a bitwise
        AND operation between two variants
    -   [variant\_cast](/ref/com.html#variant_cast) — Convert a variant
        into a new variant object of another type
    -   [variant\_cat](/ref/com.html#variant_cat) — Concatenates two
        variant values together and returns the result
    -   [variant\_cmp](/ref/com.html#variant_cmp) — Compares two
        variants
    -   [variant\_date\_from\_timestamp](/ref/com.html#variant_date_from_timestamp)
        — Returns a variant date representation of a Unix timestamp
    -   [variant\_date\_to\_timestamp](/ref/com.html#variant_date_to_timestamp)
        — Converts a variant date/time value to Unix timestamp
    -   [variant\_div](/ref/com.html#variant_div) — Returns the result
        from dividing two variants
    -   [variant\_eqv](/ref/com.html#variant_eqv) — Performs a bitwise
        equivalence on two variants
    -   [variant\_fix](/ref/com.html#variant_fix) — Returns the integer
        portion of a variant
    -   [variant\_get\_type](/ref/com.html#variant_get_type) — Returns
        the type of a variant object
    -   [variant\_idiv](/ref/com.html#variant_idiv) — Converts variants
        to integers and then returns the result from dividing them
    -   [variant\_imp](/ref/com.html#variant_imp) — Performs a bitwise
        implication on two variants
    -   [variant\_int](/ref/com.html#variant_int) — Returns the integer
        portion of a variant
    -   [variant\_mod](/ref/com.html#variant_mod) — Divides two variants
        and returns only the remainder
    -   [variant\_mul](/ref/com.html#variant_mul) — Multiplies the
        values of the two variants
    -   [variant\_neg](/ref/com.html#variant_neg) — Performs logical
        negation on a variant
    -   [variant\_not](/ref/com.html#variant_not) — Performs bitwise not
        negation on a variant
    -   [variant\_or](/ref/com.html#variant_or) — Performs a logical
        disjunction on two variants
    -   [variant\_pow](/ref/com.html#variant_pow) — Returns the result
        of performing the power function with two variants
    -   [variant\_round](/ref/com.html#variant_round) — Rounds a variant
        to the specified number of decimal places
    -   [variant\_set\_type](/ref/com.html#variant_set_type) — Convert a
        variant into another type "in-place"
    -   [variant\_set](/ref/com.html#variant_set) — Assigns a new value
        for a variant object
    -   [variant\_sub](/ref/com.html#variant_sub) — Subtracts the value
        of the right variant from the left variant value
    -   [variant\_xor](/ref/com.html#variant_xor) — Performs a logical
        exclusion on two variants

简介
----

The com class allows you to instantiate an OLE compatible COM object and
call its methods and access its properties.

类摘要
------

**com**

<span class="ooclass"> class **com** </span> <span class="ooclass">
<span class="modifier">extends</span> **variant** </span> {

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$module_name`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$server_name`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$codepage`<span class="initializer"> =
CP\_ACP</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$typelib`</span> \]\]\] )

}

Overloaded Methods
------------------

The returned object is an overloaded object, which means that PHP does
not see any fixed methods as it does with regular classes; instead, any
property or method accesses are passed through to COM.

PHP will automatically detect methods that accept parameters by
reference, and will automatically convert regular PHP variables to a
form that can be passed by reference. This means that you can call the
method very naturally; you needn't go to any extra effort in your code.

com examples
------------

**示例 \#1 com example (1)**

``` php
<?php
// starting word
$word = new com("word.application") or die("Unable to instantiate Word");
echo "Loaded Word, version {$word->Version}\n";

//bring it to front
$word->Visible = 1;

//open an empty document
$word->Documents->Add();

//do some weird stuff
$word->Selection->TypeText("This is a test...");
$word->Documents[1]->SaveAs("Useless test.doc");

//closing word
$word->Quit();

//free the object
$word = null;
?>
```

**示例 \#2 com example (2)**

``` php
<?php

$conn = new com("ADODB.Connection") or die("Cannot start ADO");
$conn->Open("Provider=SQLOLEDB; Data Source=localhost;
Initial Catalog=database; User ID=user; Password=password");

$rs = $conn->Execute("SELECT * FROM sometable");    // Recordset

$num_columns = $rs->Fields->Count();
echo $num_columns . "\n";

for ($i=0; $i < $num_columns; $i++) {
    $fld[$i] = $rs->Fields($i);
}

$rowcount = 0;
while (!$rs->EOF) {
    for ($i=0; $i < $num_columns; $i++) {
        echo $fld[$i]->value . "\t";
    }
    echo "\n";
    $rowcount++;            // increments rowcount
    $rs->MoveNext();
}

$rs->Close();
$conn->Close();

$rs = null;
$conn = null;

?>
```

com::\_\_construct
==================

com class constructor

### 说明

<span class="methodname">com::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$module_name`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$server_name`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$codepage`<span class="initializer"> =
CP\_ACP</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$typelib`</span> \]\]\] )

Constructs a new com object.

### 参数

`module_name`  
<span class="simpara"> Can be a ProgID, Class ID or Moniker that names
the component to load. </span> <span class="simpara"> A ProgID is
typically the application or DLL name, followed by a period, followed by
the object name. e.g: *Word.Application*. </span> <span class="simpara">
A Class ID is the UUID that uniquely identifies a given class. </span>
<span class="simpara"> A Moniker is a special form of naming, similar in
concept to a URL scheme, that identifies a resource and specifies how it
should be loaded. As an example, you could load up Word and get an
object representing a word document by specifying the full path to the
word document as the module name, or you can use *LDAP:* as a moniker to
use the ADSI interface to LDAP. </span>

`server_name`  
<span class="simpara"> The name of the DCOM server on which the
component should be loaded and run. If **`NULL`**, the object is run
using the default for the application. The default is typically to run
it on the local machine, although the administrator might have
configured the application to launch on a different machine. </span>
<span class="simpara"> If you specify a non-**`NULL`** value for server,
PHP will refuse to load the object unless the
<a href="/com/setup.html#" class="xref"></a> configuration option is set
to **`TRUE`**. </span>

If `server_name` is an array, it should contain the following elements
(case sensitive!). Note that they are all optional (although you need to
specify both Username and Password together); if you omit the Server
setting, the default server will be used (as mentioned above), and the
instantiation of the object will not be affected by the
<a href="/com/setup.html#" class="xref"></a> directive.

| key      | type    | description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Server   | string  | The name of the server.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Username | string  | The username to connect as.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Password | string  | The password for *Username*.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Domain   | string  | The domain of *server*.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Flags    | integer | One or more of the following constants, logically OR'd together: **`CLSCTX_INPROC_SERVER`**, **`CLSCTX_INPROC_HANDLER`**, **`CLSCTX_LOCAL_SERVER`**, **`CLSCTX_REMOTE_SERVER`**, **`CLSCTX_SERVER`** and **`CLSCTX_ALL`**. The default value if not specified here is **`CLSCTX_SERVER`** if you also omit *Server*, or **`CLSCTX_REMOTE_SERVER`** if you do specify a server. You should consult the Microsoft documentation for CoCreateInstance for more information on the meaning of these constants; you will typically never have to use them. |

`codepage`  
<span class="simpara"> Specifies the codepage that is used to convert
strings to unicode-strings and vice versa. The conversion is applied
whenever a PHP string is passed as a parameter or returned from a method
of this COM object. The code page is sticky, which means that it will
propagate to objects and variants returned from the object. </span>
<span class="simpara"> Possible values are **`CP_ACP`** (use system
default ANSI code page - the default if this parameter is omitted),
**`CP_MACCP`**, **`CP_OEMCP`**, **`CP_SYMBOL`**, **`CP_THREAD_ACP`**
(use codepage/locale set for the current executing thread),
**`CP_UTF7`** and **`CP_UTF8`**. You may also use the number for a given
codepage; consult the Microsoft documentation for more details on
codepages and their numeric values. </span>

简介
----

The dotnet class allows you to instantiate a class from a .Net assembly
and call its methods and access its properties, if the class and the
methods and properties are
<a href="https://docs.microsoft.com/dotnet/api/system.runtime.interopservices.comvisibleattribute" class="link external">» visible to COM</a>.

Neither instantiating static classes nor calling static methods is
supported.

Some .Net classes do not implement IDispatch, so while they can be
instantiated, calling methods or accessing properties on these classes
is not supported.

> **Note**:
>
> You need to install the .Net runtime on your web server to take
> advantage of this feature.

> **Note**:
>
> .Net framework 4.0 and later are not supported by the <span
> class="classname">dotnet</span> class. If assemblies have been
> registered with **regasm.exe**, the classes can be instantiated as
> <span class="classname">com</span> objects, though.

类摘要
------

**dotnet**

<span class="ooclass"> class **dotnet** </span> <span class="ooclass">
<span class="modifier">extends</span> **variant** </span> {

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$assembly_name`</span> , <span class="methodparam"><span
class="type">string</span> `$class_name`</span> \[, <span
class="methodparam"><span class="type">int</span> `$codepage`<span
class="initializer"> = CP\_ACP</span></span> \] )

}

Overloaded Methods
------------------

The returned object is an overloaded object, which means that PHP does
not see any fixed methods as it does with regular classes; instead, any
property or method accesses are passed through to COM and from there to
DOTNET. In other words, the .Net object is mapped through the COM
interoperability layer provided by the .Net runtime.

Once you have created a dotnet object, PHP treats it identically to any
other COM object; all the same rules apply.

dotnet examples
---------------

**示例 \#1 dotnet example**

``` php
<?php
$stack = new dotnet("mscorlib", "System.Collections.Stack");
$stack->Push(".Net");
$stack->Push("Hello ");
echo $stack->Pop() . $stack->Pop();
?>
```

dotnet::\_\_construct
=====================

dotnet class constructor

### 说明

<span class="methodname">dotnet::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$assembly_name`</span> , <span class="methodparam"><span
class="type">string</span> `$class_name`</span> \[, <span
class="methodparam"><span class="type">int</span> `$codepage`<span
class="initializer"> = CP\_ACP</span></span> \] )

Constructs a new dotnet object.

### 参数

`assembly_name`  
<span class="simpara"> Specifies which assembly should be loaded.
</span>

`class_name`  
<span class="simpara"> Specifices which class in that assembly to
instantiate. </span>

`codepage`  
<span class="simpara"> Codepage to use for unicode string
transformations; see the <a href="/class/com.html" class="xref">com</a>
class for more details on code pages. </span>

简介
----

The VARIANT is COM's equivalent of the PHP zval; it is a structure that
can contain a value with a range of different possible types. The
variant class provided by the COM extension allows you to have more
control over the way that PHP passes values to and from COM.

类摘要
------

**variant**

<span class="ooclass"> class **variant** </span> {

/\* 方法 \*/

<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$value`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$type`<span
class="initializer"> = VT\_EMPTY</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$codepage`<span
class="initializer"> = CP\_ACP</span></span> \]\]\] )

}

variant examples
----------------

**示例 \#1 variant example**

``` php
<?php
$v = new variant(42);
print "The type is " . variant_get_type($v) . "<br/>";
print "The value is " . $v . "<br/>";
?>
```

> **Note**:
>
> When returning a value or fetching a variant property, the variant is
> converted to a PHP value only when there is a direct mapping between
> the types that would not result in a loss of information. In all other
> cases, the result is returned as an instance of the variant class. You
> can force PHP to convert or evaluate the variant as a PHP native type
> by using a casting operator explicitly, or implicitly casting to a
> string by <span class="function">print</span>ing it. You may use the
> wide range of variant functions to perform arithmetic operations on
> variants without forcing a conversion or risking a loss of data.

See also <span class="function">variant\_get\_type</span>.

variant::\_\_construct
======================

variant class constructor

### 说明

<span class="methodname">variant::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$value`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$type`<span
class="initializer"> = VT\_EMPTY</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$codepage`<span
class="initializer"> = CP\_ACP</span></span> \]\]\] )

Constructs a new variant object.

### 参数

`value`  
<span class="simpara"> Initial value. If omitted, or set to **`NULL`**
an VT\_EMPTY object is created. </span>

`type`  
<span class="simpara"> Specifies the content type of the variant object.
Possible values are one of the **`VT_XXX`**
<a href="/com/constants.html" class="xref">预定义常量</a>. </span> <span
class="simpara"> PHP can detect parameters passed by reference
automatically; they do not even need to be passed as variant objects.
</span> <span class="simpara"> Consult the MSDN library for additional
information on the VARIANT type. </span>

`codepage`  
<span class="simpara"> Specifies the codepage that is used to convert
strings to unicode. See the parameter of the same name in the
<a href="/class/com.html" class="xref">com</a> class for more
information. </span>

简介
----

<span class="classname">COMPersistHelper</span> improves the
interoperability of COM and PHP with regard to the `php.ini` directive
<a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>,
and stream
<a href="/language/types/resource.html" class="link">资源(resource)</a>s.

类摘要
------

**COMPersistHelper**

<span class="ooclass"> <span class="modifier">final</span> class
**COMPersistHelper** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">variant</span> `$com_object`<span
class="initializer"> = **`NULL`**</span></span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GetCurFileName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GetMaxStreamSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">InitNew</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">LoadFromFile</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">LoadFromStream</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SaveToFile</span> (\[ <span
class="methodparam"><span class="type">string</span> `$filename`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$remember`<span
class="initializer"> = **`TRUE`**</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SaveToStream</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
)

}

COMPersistHelper::\_\_construct
===============================

Construct a COMPersistHelper object

### 说明

<span class="modifier">public</span> <span
class="methodname">COMPersistHelper::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">variant</span> `$com_object`<span
class="initializer"> = **`NULL`**</span></span> \] )

Constructs a persistence helper object, usually associated with a
`com_object`.

### 参数

`com_object`  
<span class="simpara"> A COM object which implements <span
class="interfacename">IDispatch</span>. To be able to successfully call
any of <span class="classname">COMPersistHelper</span>'s methods, the
object has to implement <span class="interfacename">IPersistFile</span>,
<span class="interfacename">IPersistStream</span> and/or <span
class="interfacename">IPersistStreamInit</span>. </span> <span
class="simpara"> Passing **`NULL`** as `com_object` is only useful if
the object is to be loaded from a stream by calling <span
class="methodname">COMPersistHelper::LoadFromStream</span>. </span>

COMPersistHelper::GetCurFileName
================================

Get current filename

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">COMPersistHelper::GetCurFileName</span> ( <span
class="methodparam">void</span> )

Retrieves the current name of the file associated with the object.

### 参数

此函数没有参数。

### 返回值

Returns the current name of the file associated with the object.

### 错误／异常

A <span class="classname">com\_exception</span> is thrown if the
associated object does not implement the COM interface <span
class="interfacename">IPersistFile</span>, or when calling the <span
class="methodname">IPersistFile::GetCurFile</span> method failed.

COMPersistHelper::GetMaxStreamSize
==================================

Get maximum stream size

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">COMPersistHelper::GetMaxStreamSize</span> ( <span
class="methodparam">void</span> )

Retrieves the size of the stream (in bytes) needed to save the object.

### 参数

此函数没有参数。

### 返回值

Returns the size of the stream (in bytes) needed to save the object.

### 错误／异常

A <span class="classname">com\_exception</span> is thrown if the
associated object does neither implement the COM interface <span
class="interfacename">IPersistStream</span> nor <span
class="interfacename">IPersistStreamInit</span>, or when calling the
<span class="methodname">IPersistStream::GetSizeMax</span> method
failed.

COMPersistHelper::InitNew
=========================

Initialize object to default state

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">COMPersistHelper::InitNew</span> ( <span
class="methodparam">void</span> )

Initializes an object to a default state.

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

A <span class="classname">com\_exception</span> is thrown if the
associated object does not implement the COM interface <span
class="interfacename">IPersistStreamInit</span>, or when calling its
<span class="methodname">IPersistStreamInit::Init</span> method failed.

COMPersistHelper::LoadFromFile
==============================

Load object from file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">COMPersistHelper::LoadFromFile</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \] )

Opens the specified file and initializes an object from the file
contents.

### 参数

`path`  
<span class="simpara"> The name of the file from which to load the
object. </span>

`flags`  
<span class="simpara"> The access mode to be used when opening the file.
Possible values are taken from the
<a href="https://docs.microsoft.com/en-us/windows/win32/stg/stgm-constants" class="link external">» STGM enumeration</a>.
The method can treat this value as a suggestion, adding more restrictive
permissions if necessary. If `flags` is *0*, the implementation is
supposed to open the file using whatever default permissions are used
when a user opens the file. </span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

A <span class="classname">com\_exception</span> is thrown if the
associated object does not implement the COM interface <span
class="interfacename">IPersistFile</span>, or when calling the <span
class="methodname">IPersistFile::Load</span> method failed.

COMPersistHelper::LoadFromStream
================================

Load object from stream

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">COMPersistHelper::LoadFromStream</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
)

Initializes an object from the stream where it was saved previously.

### 参数

`stream`  
<span class="simpara"> The stream
<a href="/language/types/resource.html" class="link">资源(resource)</a>
from which to load the object. </span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

A <span class="classname">com\_exception</span> is thrown if the
associated object does not implement the COM interface <span
class="interfacename">IPersistStream</span>, or when calling the <span
class="methodname">IPersistStream::Load</span> method failed.

COMPersistHelper::SaveToFile
============================

Save object to file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">COMPersistHelper::SaveToFile</span> (\[ <span
class="methodparam"><span class="type">string</span> `$filename`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$remember`<span
class="initializer"> = **`TRUE`**</span></span> \]\] )

Saves a copy of the object to the specified file.

### 参数

`filename`  
<span class="simpara"> The name of the file to which to save the object.
</span>

`remember`  
<span class="simpara"> Indicates whether the `filename` parameter is to
be used as the current working file. If **`TRUE`**, `filename` becomes
the current file and the object is supposed to clear its dirty flag
after the save. If **`FALSE`**, this save operation is a "Save A Copy As
..." operation. In this case, the current file is unchanged and the
object is not supposed to clear its dirty flag. </span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

A <span class="classname">com\_exception</span> is thrown if the
associated object does not implement the COM interface <span
class="interfacename">IPersistFile</span>, or when calling the <span
class="methodname">IPersistFile::Save</span> method failed.

### 范例

**示例 \#1 Basic <span
class="methodname">COMPersistHelper::saveToFile</span> Usage**

``` php
<?php
$word = new COM('Word.Application');
$doc = $word->Documents->Add();
$ph = new COMPersistHelper($doc);
$ph->SaveToFile('C:\\Users\\cmb\\Documents\\my.docx');
$word->Quit();
?>
```

COMPersistHelper::SaveToStream
==============================

Save object to stream

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">COMPersistHelper::SaveToStream</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
)

Saves an object to the specified stream.

### 参数

`stream`  
<span class="simpara"> The stream
<a href="/language/types/resource.html" class="link">资源(resource)</a>
to which to save the object. </span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

A <span class="classname">com\_exception</span> is thrown if the
associated object does neither implement the COM interface <span
class="interfacename">IPersistStream</span> nor <span
class="interfacename">IPersistStreamInit</span>, or when calling the
<span class="methodname">IPersistStream::Save</span> method failed.

简介
----

类摘要
------

**com\_exception**

<span class="ooclass"> class **com\_exception** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> <span class="oointerface">implements <span
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
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}
