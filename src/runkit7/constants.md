预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`RUNKIT7_IMPORT_FUNCTIONS`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit7\_import</span>
flag indicating that normal functions should be imported from the
specified file. </span>

**`RUNKIT7_IMPORT_CLASS_METHODS`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit7\_import</span>
flag indicating that class methods should be imported from the specified
file. </span>

**`RUNKIT7_IMPORT_CLASS_CONSTS`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit7\_import</span>
flag indicating that class constants should be imported from the
specified file. </span>

**`RUNKIT7_IMPORT_CLASS_PROPS`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit7\_import</span>
flag indicating that class standard properties should be imported from
the specified file. </span>

**`RUNKIT7_IMPORT_CLASS_STATIC_PROPS`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit7\_import</span>
flag indicating that class static properties should be imported from the
specified file. Available since Runkit 1.0.1. </span>

**`RUNKIT7_IMPORT_CLASSES`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit7\_import</span>
flag representing a bitwise OR of the **`RUNKIT7_IMPORT_CLASS_*`**
constants. </span>

**`RUNKIT7_IMPORT_OVERRIDE`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit7\_import</span>
flag indicating that if any of the imported functions, methods,
constants, or properties already exist, they should be replaced with the
new definitions. If this flag is not set, then any imported definitions
which already exist will be discarded. </span>

**`RUNKIT7_ACC_RETURN_REFERENCE`** (<span class="type">integer</span>)  
<span class="simpara"> Include this flag to make the function or method
being created or redeclared return a reference. </span>

**`RUNKIT7_ACC_PUBLIC`** (<span class="type">integer</span>)  
<span class="simpara"> Flag for <span
class="function">runkit7\_method\_add</span> and <span
class="function">runkit7\_method\_redefine</span> to make the method
public. </span>

**`RUNKIT7_ACC_PROTECTED`** (<span class="type">integer</span>)  
<span class="simpara"> Flag for <span
class="function">runkit7\_method\_add</span> and <span
class="function">runkit7\_method\_redefine</span> to make the method
protected. </span>

**`RUNKIT7_ACC_PRIVATE`** (<span class="type">integer</span>)  
<span class="simpara"> Flag for <span
class="function">runkit7\_method\_add</span> and <span
class="function">runkit7\_method\_redefine</span> to make the method
private. </span>

**`RUNKIT7_ACC_STATIC`** (<span class="type">integer</span>)  
<span class="simpara"> Flag for <span
class="function">runkit7\_method\_add</span> and <span
class="function">runkit7\_method\_redefine</span> to make the method
static. </span>

**`RUNKIT7_FEATURE_MANIPULATION`** (<span class="type">integer</span>)  
<span class="simpara"> Equal to 1 if runtime manipulation is enabled,
and 0 otherwise. </span>

**`RUNKIT7_FEATURE_SUPERGLOBALS`** (<span class="type">integer</span>)  
<span class="simpara"> Equal to 1 if custom superglobals are enabled,
and 0 otherwise. </span>

**`RUNKIT7_FEATURE_SANDBOX`** (<span class="type">integer</span>)  
<span class="simpara"> Always 0, it's impractical to implement the
sandbox feature in php 7. </span>
