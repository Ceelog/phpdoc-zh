预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`RUNKIT_IMPORT_FUNCTIONS`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit\_import</span> flag
indicating that normal functions should be imported from the specified
file. </span>

**`RUNKIT_IMPORT_CLASS_METHODS`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit\_import</span> flag
indicating that class methods should be imported from the specified
file. </span>

**`RUNKIT_IMPORT_CLASS_CONSTS`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit\_import</span> flag
indicating that class constants should be imported from the specified
file. Note that this flag is only meaningful in PHP versions 5.1.0 and
above. </span>

**`RUNKIT_IMPORT_CLASS_PROPS`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit\_import</span> flag
indicating that class standard properties should be imported from the
specified file. </span>

**`RUNKIT_IMPORT_CLASS_STATIC_PROPS`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit\_import</span> flag
indicating that class static properties should be imported from the
specified file. Available since Runkit 1.0.1. </span>

**`RUNKIT_IMPORT_CLASSES`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit\_import</span> flag
representing a bitwise OR of the **`RUNKIT_IMPORT_CLASS_*`** constants.
</span>

**`RUNKIT_IMPORT_OVERRIDE`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">runkit\_import</span> flag
indicating that if any of the imported functions, methods, constants, or
properties already exist, they should be replaced with the new
definitions. If this flag is not set, then any imported definitions
which already exist will be discarded. </span>

**`RUNKIT_ACC_PUBLIC`** (<span class="type">integer</span>)  
<span class="simpara"> PHP 5 specific flag to <span
class="function">runkit\_method\_add</span> and <span
class="function">runkit\_method\_redefine</span> </span>

**`RUNKIT_ACC_PROTECTED`** (<span class="type">integer</span>)  
<span class="simpara"> PHP 5 specific flag to <span
class="function">runkit\_method\_add</span> and <span
class="function">runkit\_method\_redefine</span> </span>

**`RUNKIT_ACC_PRIVATE`** (<span class="type">integer</span>)  
<span class="simpara"> PHP 5 specific flag to <span
class="function">runkit\_method\_add</span> and <span
class="function">runkit\_method\_redefine</span> </span>

**`RUNKIT_ACC_STATIC`** (<span class="type">integer</span>)  
<span class="simpara"> PHP 5 specific flag to <span
class="function">runkit\_method\_add</span> and <span
class="function">runkit\_method\_redefine</span>. Available since Runkit
1.0.1. </span>

**`CLASSKIT_ACC_PUBLIC`** (<span class="type">integer</span>)  
<span class="simpara"> PHP 5 specific flag to <span
class="function">classkit\_method\_add</span> Only defined when classkit
compatibility is enabled. </span>

**`CLASSKIT_ACC_PROTECTED`** (<span class="type">integer</span>)  
<span class="simpara"> PHP 5 specific flag to <span
class="function">classkit\_method\_add</span> Only defined when classkit
compatibility is enabled. </span>

**`CLASSKIT_ACC_PRIVATE`** (<span class="type">integer</span>)  
<span class="simpara"> PHP 5 specific flag to <span
class="function">classkit\_method\_add</span> Only defined when classkit
compatibility is enabled. </span>

**`CLASSKIT_AGGREGATE_OVERRIDE`** (<span class="type">integer</span>)  
<span class="simpara"> PHP 5 specific flag to <span
class="function">classkit\_import</span> Only defined when classkit
compatibility is enabled. </span>

**`RUNKIT_VERSION`** (<span class="type">string</span>)  
<span class="simpara"> Defined to the current version of the runkit
package. </span>

**`CLASSKIT_VERSION`** (<span class="type">string</span>)  
<span class="simpara"> Defined to the current version of the runkit
package. Only defined when classkit compatibility is enabled. </span>
