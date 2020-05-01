Runkit\_Sandbox
===============

Runkit Sandbox Class -- PHP Virtual Machine

### 说明

Instantiating the <span class="classname">Runkit\_Sandbox</span> class
creates a new thread with its own scope and program stack. Using a set
of options passed to the constructor, this environment may be restricted
to a subset of what the primary interpreter can do and provide a safer
environment for executing user supplied code.

> **Note**: <span class="simpara">沙箱支持（是 <span
> class="function">runkit\_lint</span>，<span
> class="function">runkit\_lint\_file</span> 函数，与 <span
> class="classname">Runkit\_Sandbox</span> 类所必需）仅可用于 PHP 5.1.0
> 或 PHP 5.0 的特别修补版本，并需启用线程安全。更多信息可参见 runkit
> 包中的 `README` 文件。</span>

### Constructor

<span class="type">void</span> <span
class="methodname">Runkit\_Sandbox::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`</span> \]
)

`options` is an associative array containing any combination of the
special ini options listed below.

`safe_mode`  
If the outer script which is instantiating the <span
class="classname">Runkit\_Sandbox</span> class is configured with
*safe\_mode = off*, then safe\_mode may be turned on for the sandbox
environment. This setting can not be used to disable *safe\_mode* when
it's already enabled in the outer script.

`safe_mode_gid`  
If the outer script which is instantiating the <span
class="classname">Runkit\_Sandbox</span> class is configured with
*safe\_mode\_gid = on*, then safe\_mode\_gid may be turned off for the
sandbox environment. This setting can not be used to enable
*safe\_mode\_gid* when it's already disabled in the outer script.

`safe_mode_include_dir`  
If the outer script which is instantiating the <span
class="classname">Runkit\_Sandbox</span> class is configured with a
*safe\_mode\_include\_dir*, then a new safe\_mode\_include\_dir may be
set for sandbox environments below the currently defined value.
safe\_mode\_include\_dir may also be cleared to indicate that the bypass
feature is disabled. If safe\_mode\_include\_dir was blank in the outer
script, but safe\_mode was not enabled, then any arbitrary
safe\_mode\_include\_dir may be set while turning safe\_mode on.

`open_basedir`  
`open_basedir` may be set to any path below the current setting of
*open\_basedir*. If *open\_basedir* is not set within the global scope,
then it is assumed to be the root directory and may be set to any
location.

`allow_url_fopen`  
Like `safe_mode`, this setting can only be made more restrictive, in
this case by setting it to **`FALSE`** when it is previously set to
**`TRUE`**

`disable_functions`  
Comma separated list of functions to disable within the sandbox
sub-interpreter. This list need not contain the names of the currently
disabled functions, they will remain disabled whether listed here or
not.

`disable_classes`  
Comma separated list of classes to disable within the sandbox
sub-interpreter. This list need not contain the names of the currently
disabled classes, they will remain disabled whether listed here or not.

`runkit.superglobal`  
Comma separated list of variables to be treated as superglobals within
the sandbox sub-interpreter. These variables will be used in addition to
any variables defined internally or through the global
runkit.superglobal setting.

`runkit.internal_override`  
Ini option *runkit.internal\_override* may be disabled (but not
re-enabled) within sandboxes.

**示例 \#1 Instantiating a restricted sandbox**

``` php
<?php
$options = array(
  'safe_mode'=>true,
  'open_basedir'=>'/var/www/users/jdoe/',
  'allow_url_fopen'=>'false',
  'disable_functions'=>'exec,shell_exec,passthru,system',
  'disable_classes'=>'myAppClass');
$sandbox = new Runkit_Sandbox($options);
/* Non-protected ini settings may set normally */
$sandbox->ini_set('html_errors',true);
?>
```

### Accessing Variables

All variables in the global scope of the sandbox environment are
accessible as properties of the sandbox object. The first thing to note
is that because of the way memory between these two threads is managed,
object and resource variables can not currently be exchanged between
interpreters. Additionally, all arrays are deep copied and any
references will be lost. This also means that references between
interpreters are not possible.

**示例 \#2 Working with variables in a sandbox**

``` php
<?php
$sandbox = new Runkit_Sandbox();

$sandbox->foo = 'bar';
$sandbox->eval('echo "$foo\n"; $bar = $foo . "baz";');
echo "{$sandbox->bar}\n";
if (isset($sandbox->foo)) unset($sandbox->foo);
$sandbox->eval('var_dump(isset($foo));');
?>
```

以上例程会输出：

    bar
    barbaz
    bool(false)

### Calling PHP Functions

Any function defined within the sandbox may be called as a method on the
sandbox object. This also includes a few pseudo-function language
constructs: <span class="function">eval</span>, <span
class="function">include</span>, <span
class="function">include\_once</span>, <span
class="function">require</span>, <span
class="function">require\_once</span>, <span
class="function">echo</span>, <span class="function">print</span>, <span
class="function">die</span>, and <span class="function">exit</span>.

**示例 \#3 Calling sandbox functions**

``` php
<?php
$sandbox = new Runkit_Sandbox();

echo $sandbox->str_replace('a','f','abc');
?>
```

以上例程会输出：

    fbc

When passing arguments to a sandbox function, the arguments are taken
from the outer instance of PHP. If you wish to pass arguments from the
sandbox's scope, be sure to access them as properties of the sandbox
object as illustrated above.

**示例 \#4 Passing arguments to sandbox functions**

``` php
<?php
$sandbox = new Runkit_Sandbox();

$foo = 'bar';
$sandbox->foo = 'baz';
echo $sandbox->str_replace('a',$foo,'a');
echo $sandbox->str_replace('a',$sandbox->foo,'a');
?>
```

以上例程会输出：

    bar
    baz

### Changing Sandbox Settings

As of runkit version 0.5, certain Sandbox settings may be modified on
the fly using ArrayAccess syntax. Some settings, such as `active` are
read-only and meant to provide status information. Other settings, such
as `output_handler` may be set and read much like a normal array offset.
Future settings may be write-only, however no such settings currently
exist.

| Setting           | Type                                          | Purpose                                                                                                                                                                                                                                                                                                                                 | Default              |
|-------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| *active*          | <span class="type">Boolean</span> (Read Only) | **`TRUE`** if the Sandbox is still in a usable state, **`FALSE`** if the request is in bailout due to a call to die(), exit(), or because of a fatal error condition.                                                                                                                                                                   | **`TRUE`** (Initial) |
| *output\_handler* | <span class="type">Callback</span>            | When set to a valid callback, all output generated by the Sandbox instance will be processed through the named function. Sandbox output handlers follow the same calling conventions as the system-wide output handler.                                                                                                                 | None                 |
| *parent\_access*  | <span class="type">Boolean</span>             | May the sandbox use instances of the <span class="classname">Runkit\_Sandbox\_Parent</span> class? Must be enabled for other <span class="classname">Runkit\_Sandbox\_Parent</span> related settings to work.                                                                                                                           | **`FALSE`**          |
| *parent\_read*    | <span class="type">Boolean</span>             | May the sandbox read variables in its parent's context?                                                                                                                                                                                                                                                                                 | **`FALSE`**          |
| *parent\_write*   | <span class="type">Boolean</span>             | May the sandbox modify variables in its parent's context?                                                                                                                                                                                                                                                                               | **`FALSE`**          |
| *parent\_eval*    | <span class="type">Boolean</span>             | May the sandbox evaluate arbitrary code in its parent's context? *DANGEROUS*                                                                                                                                                                                                                                                            | **`FALSE`**          |
| *parent\_include* | <span class="type">Boolean</span>             | May the sandbox include php code files in its parent's context? *DANGEROUS*                                                                                                                                                                                                                                                             | **`FALSE`**          |
| *parent\_echo*    | <span class="type">Boolean</span>             | May the sandbox echo data in its parent's context effectively bypassing its own output\_handler?                                                                                                                                                                                                                                        | **`FALSE`**          |
| *parent\_call*    | <span class="type">Boolean</span>             | May the sandbox call functions in its parent's context?                                                                                                                                                                                                                                                                                 | **`FALSE`**          |
| *parent\_die*     | <span class="type">Boolean</span>             | May the sandbox kill its own parent? (And thus itself)                                                                                                                                                                                                                                                                                  | **`FALSE`**          |
| *parent\_scope*   | <span class="type">Integer</span>             | What scope will parental property access look at? 0 == Global scope, 1 == Calling scope, 2 == Scope preceding calling scope, 3 == The scope before that, etc..., etc...                                                                                                                                                                 | *0* (Global)         |
| *parent\_scope*   | <span class="type">String</span>              | When *parent\_scope* is set to a string value, it refers to a named array variable in the global scope. If the named variable does not exist at the time of access it will be created as an empty array. If the variable exists but it not an array, a dummy array will be created containing a reference to the named global variable. |                      |

Runkit\_Sandbox\_Parent
=======================

Runkit Anti-Sandbox Class

### 说明

<span class="type">void</span> <span
class="methodname">Runkit\_Sandbox\_Parent::\_\_construct</span> ( <span
class="methodparam">void</span> )

Instantiating the <span class="classname">Runkit\_Sandbox\_Parent</span>
class from within a sandbox environment created from the <span
class="classname">Runkit\_Sandbox</span> class provides some
(controlled) means for a sandbox child to access its parent.

> **Note**: <span class="simpara">沙箱支持（是 <span
> class="function">runkit\_lint</span>，<span
> class="function">runkit\_lint\_file</span> 函数，与 <span
> class="classname">Runkit\_Sandbox</span> 类所必需）仅可用于 PHP 5.1.0
> 或 PHP 5.0 的特别修补版本，并需启用线程安全。更多信息可参见 runkit
> 包中的 `README` 文件。</span>

In order for any of the <span
class="classname">Runkit\_Sandbox\_Parent</span> features to function.
Support must be enabled on a per-sandbox basis by enabling the
*parent\_access* flag from the parent's context.

**示例 \#1 Working with variables in a sandbox**

``` php
<?php
$sandbox = new Runkit_Sandbox();
$sandbox['parent_access'] = true;
?>
```

### Accessing the Parent's Variables

Just as with sandbox variable access, a sandbox parent's variables may
be read from and written to as properties of the <span
class="classname">Runkit\_Sandbox\_Parent</span> class. Read access to
parental variables may be enabled with the *parent\_read* setting (in
addition to the base *parent\_access* setting). Write access, in turn,
is enabled through the *parent\_write* setting.

Unlike sandbox child variable access, the variable scope is not limited
to globals only. By setting the *parent\_scope* setting to an
appropriate integer value, other scopes in the active call stack may be
inspected instead. A value of 0 (Default) will direct variable access at
the global scope. 1 will point variable access at whatever variable
scope was active at the time the current block of sandbox code was
executed. Higher values progress back through the functions that called
the functions that led to the sandbox executing code that tried to
access its own parent's variables.

**示例 \#2 Accessing parental variables**

``` php
<?php
$php = new Runkit_Sandbox();
$php['parent_access'] = true;
$php['parent_read'] = true;

$test = "Global";

$php->eval('$PARENT = new Runkit_Sandbox_Parent;');

$php['parent_scope'] = 0;
one();

$php['parent_scope'] = 1;
one();

$php['parent_scope'] = 2;
one();

$php['parent_scope'] = 3;
one();

$php['parent_scope'] = 4;
one();

$php['parent_scope'] = 5;
one();

function one() {
    $test = "one()";
    two();
}

function two() {
    $test = "two()";
    three();
}

function three() {
    $test = "three()";
    $GLOBALS['php']->eval('var_dump($PARENT->test);');
}
?>
```

以上例程会输出：

    string(6) "Global"
    string(7) "three()"
    string(5) "two()"
    string(5) "one()"
    string(6) "Global"
    string(6) "Global"

### Calling the Parent's Functions

Just as with sandbox access, a sandbox may access its parents functions
providing that the proper settings have been enabled. Enabling
*parent\_call* will allow the sandbox to call all functions available to
the parent scope. Language constructs are each controlled by their own
setting: <span class="function">print</span> and <span
class="function">echo</span> are enabled with *parent\_echo*. <span
class="function">die</span> and <span class="function">exit</span> are
enabled with *parent\_die*. <span class="function">eval</span> is
enabled with *parent\_eval* while <span class="function">include</span>,
<span class="function">include\_once</span>, <span
class="function">require</span>, and <span
class="function">require\_once</span> are enabled through
*parent\_include*.

runkit\_class\_adopt
====================

Convert a base class to an inherited class, add ancestral methods when
appropriate

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_class\_adopt</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$parentname`</span> )

### 参数

`classname`  
Name of class to be adopted

`parentname`  
Parent class which child class is extending

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 A <span class="function">runkit\_class\_adopt</span>
example**

``` php
<?php
class myParent {
  function parentFunc() {
    echo "Parent Function Output\n";
  }
}

class myChild {
}

runkit_class_adopt('myChild','myParent');
myChild::parentFunc();
?>
```

以上例程会输出：

    Parent Function Output

### 参见

-   <span class="function">runkit\_class\_emancipate</span>

runkit\_class\_emancipate
=========================

Convert an inherited class to a base class, removes any method whose
scope is ancestral

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_class\_emancipate</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
)

### 参数

`classname`  
Name of class to emancipate

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 A <span class="function">runkit\_class\_emancipate</span>
example**

``` php
<?php
class myParent {
  function parentFunc () {
    echo "Parent Function Output\n";
  }
}
class myChild extends myParent {
}

myChild::parentFunc();
runkit_class_emancipate('myChild');
myChild::parentFunc();
?>
```

以上例程会输出：

    Parent Function Output
    Fatal error: Call to undefined function:  parentFunc() in example.php on line 12

### 参见

-   <span class="function">runkit\_class\_adopt</span>

runkit\_constant\_add
=====================

Similar to define(), but allows defining in class definitions as well

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_constant\_add</span> ( <span
class="methodparam"><span class="type">string</span> `$constname`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

### 参数

`constname`  
Name of constant to declare. Either a string to indicate a global
constant, or *classname::constname* to indicate a class constant.

`value`  
NULL, Bool, Long, Double, String, or Resource value to store in the new
constant.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">define</span>
-   <span class="function">runkit\_constant\_redefine</span>
-   <span class="function">runkit\_constant\_remove</span>

runkit\_constant\_redefine
==========================

Redefine an already defined constant

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_constant\_redefine</span> ( <span
class="methodparam"><span class="type">string</span> `$constname`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$newvalue`</span> )

### 参数

`constname`  
Constant to redefine. Either string indicating global constant, or
*classname::constname* indicating class constant.

`newvalue`  
New value to assign to constant.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">runkit\_constant\_add</span>
-   <span class="function">runkit\_constant\_remove</span>

runkit\_constant\_remove
========================

Remove/Delete an already defined constant

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_constant\_remove</span> ( <span
class="methodparam"><span class="type">string</span> `$constname`</span>
)

### 参数

`constname`  
Name of constant to remove. Either a string indicating a global
constant, or *classname::constname* indicating a class constant.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">define</span>
-   <span class="function">runkit\_constant\_add</span>
-   <span class="function">runkit\_constant\_redefine</span>

runkit\_function\_add
=====================

Add a new function, similar to <span
class="function">create\_function</span>

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_function\_add</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
, <span class="methodparam"><span class="type">string</span>
`$arglist`</span> , <span class="methodparam"><span
class="type">string</span> `$code`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$return_by_reference`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$doc_comment`<span class="initializer"> =
**`NULL`**</span></span> \]\] )

<span class="type">bool</span> <span
class="methodname">runkit\_function\_add</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
, <span class="methodparam"><span class="type">Closure</span>
`$closure`</span> \[, <span class="methodparam"><span
class="type">string</span> `$doc_comment`<span class="initializer"> =
**`NULL`**</span></span> \] )

### 参数

`funcname`  
Name of function to be created

`arglist`  
Comma separated argument list

`code`  
Code making up the function

`closure`  
A <span class="classname">closure</span> that defines the function.

`return_by_reference`  
Whether the function should return by reference.

`doc_comment`  
The doc comment of the function.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本         | 说明                                                                             |
|--------------|----------------------------------------------------------------------------------|
| runkit 1.0.4 | An alternative syntax expecting a `closure` has been added.                      |
| runkit 1.0.4 | The optional parameters `return_by_reference` and `doc_comment` have been added. |

### 范例

**示例 \#1 A <span class="function">runkit\_function\_add</span>
example**

``` php
<?php
runkit_function_add('testme','$a,$b','echo "The value of a is $a\n"; echo "The value of b is $b\n";');
testme(1,2);
?>
```

以上例程会输出：

    The value of a is 1
    The value of b is 2

### 参见

-   <span class="function">create\_function</span>
-   <span class="function">runkit\_function\_redefine</span>
-   <span class="function">runkit\_function\_copy</span>
-   <span class="function">runkit\_function\_rename</span>
-   <span class="function">runkit\_function\_remove</span>
-   <span class="function">runkit\_method\_add</span>

runkit\_function\_copy
======================

Copy a function to a new function name

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_function\_copy</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
, <span class="methodparam"><span class="type">string</span>
`$targetname`</span> )

### 参数

`funcname`  
Name of existing function

`targetname`  
Name of new function to copy definition to

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 A <span class="function">runkit\_function\_copy</span>
example**

``` php
<?php
function original() {
  echo "In a function\n";
}
runkit_function_copy('original','duplicate');
original();
duplicate();
?>
```

以上例程会输出：

    In a function
    In a function

### 参见

-   <span class="function">runkit\_function\_add</span>
-   <span class="function">runkit\_function\_redefine</span>
-   <span class="function">runkit\_function\_rename</span>
-   <span class="function">runkit\_function\_remove</span>

runkit\_function\_redefine
==========================

Replace a function definition with a new implementation

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_function\_redefine</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
, <span class="methodparam"><span class="type">string</span>
`$arglist`</span> , <span class="methodparam"><span
class="type">string</span> `$code`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$return_by_reference`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$doc_comment`<span class="initializer"> =
**`NULL`**</span></span> \]\] )

<span class="type">bool</span> <span
class="methodname">runkit\_function\_redefine</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
, <span class="methodparam"><span class="type">Closure</span>
`$closure`</span> \[, <span class="methodparam"><span
class="type">string</span> `$doc_comment`<span class="initializer"> =
**`NULL`**</span></span> \] )

> **Note**: <span
> class="simpara">默认情况下，仅在用户空间可删除，重命名，或者修改函数。为了覆盖内部函数，必须启用
> `php.ini` 中的 *runkit.internal\_override* 设置。</span>

### 参数

`funcname`  
Name of function to redefine

`arglist`  
New list of arguments to be accepted by function

`code`  
New code implementation

`closure`  
A <span class="classname">closure</span> that defines the function.

`return_by_reference`  
Whether the function should return by reference.

`doc_comment`  
The doc comment of the function.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本         | 说明                                                                             |
|--------------|----------------------------------------------------------------------------------|
| runkit 1.0.4 | An alternative syntax expecting a `closure` has been added.                      |
| runkit 1.0.4 | The optional parameters `return_by_reference` and `doc_comment` have been added. |

### 范例

**示例 \#1 A <span class="function">runkit\_function\_redefine</span>
example**

``` php
<?php
function testme() {
  echo "Original Testme Implementation\n";
}
testme();
runkit_function_redefine('testme','','echo "New Testme Implementation\n";');
testme();
?>
```

以上例程会输出：

    Original Testme Implementation
    New Testme Implementation

### 参见

-   <span class="function">runkit\_function\_add</span>
-   <span class="function">runkit\_function\_copy</span>
-   <span class="function">runkit\_function\_rename</span>
-   <span class="function">runkit\_function\_remove</span>
-   <span class="function">runkit\_method\_redefine</span>

runkit\_function\_remove
========================

Remove a function definition

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_function\_remove</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
)

> **Note**: <span
> class="simpara">默认情况下，仅在用户空间可删除，重命名，或者修改函数。为了覆盖内部函数，必须启用
> `php.ini` 中的 *runkit.internal\_override* 设置。</span>

### 参数

`funcname`  
Name of function to be deleted

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">runkit\_function\_add</span>
-   <span class="function">runkit\_function\_copy</span>
-   <span class="function">runkit\_function\_redefine</span>
-   <span class="function">runkit\_function\_rename</span>

runkit\_function\_rename
========================

Change a function's name

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_function\_rename</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
, <span class="methodparam"><span class="type">string</span>
`$newname`</span> )

> **Note**: <span
> class="simpara">默认情况下，仅在用户空间可删除，重命名，或者修改函数。为了覆盖内部函数，必须启用
> `php.ini` 中的 *runkit.internal\_override* 设置。</span>

### 参数

`funcname`  
Current function name

`newname`  
New function name

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">runkit\_function\_add</span>
-   <span class="function">runkit\_function\_copy</span>
-   <span class="function">runkit\_function\_redefine</span>
-   <span class="function">runkit\_function\_remove</span>

runkit\_import
==============

Process a PHP file importing function and class definitions, overwriting
where appropriate

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_import</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> =
RUNKIT\_IMPORT\_CLASS\_METHODS</span></span> \] )

Similar to <span class="function">include</span> however any code
residing outside of a function or class is simply ignored. Additionally,
depending on the value of `flags`, any functions or classes which
already exist in the currently running environment may be automatically
overwritten by their new definitions.

### 参数

`filename`  
Filename to import function and class definitions from

`flags`  
Bitwise OR of the
<a href="/runkit/constants.html" class="link"><em>RUNKIT_IMPORT_*</em> family of constants</a>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">runkit\_import</span> example**

``` php
<?php
// import classes entirely
runkit_import('myfile.inc', RUNKIT_IMPORT_CLASSES);

/* import classes, but not imports their static properties
   (RUNKIT_IMPORT_CLASS_STATIC_PROPS is available since 1.0.1) */
runkit_import('myfile.inc', RUNKIT_IMPORT_CLASSES & ~RUNKIT_IMPORT_CLASS_STATIC_PROPS);

/* import only static properties of classes
   (RUNKIT_IMPORT_CLASS_STATIC_PROPS is available since 1.0.1) */
runkit_import('myfile.inc', RUNKIT_IMPORT_CLASS_STATIC_PROPS);
?>
```

runkit\_lint\_file
==================

Check the PHP syntax of the specified file

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_lint\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

The <span class="function">runkit\_lint\_file</span> function performs a
syntax (lint) check on the specified filename testing for scripting
errors. This is similar to using php -l from the commandline.

> **Note**: <span class="simpara">沙箱支持（是 <span
> class="function">runkit\_lint</span>，<span
> class="function">runkit\_lint\_file</span> 函数，与 <span
> class="classname">Runkit\_Sandbox</span> 类所必需）仅可用于 PHP 5.1.0
> 或 PHP 5.0 的特别修补版本，并需启用线程安全。更多信息可参见 runkit
> 包中的 `README` 文件。</span>

### 参数

`filename`  
File containing PHP Code to be lint checked

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">runkit\_lint</span>

runkit\_lint
============

Check the PHP syntax of the specified php code

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_lint</span> ( <span class="methodparam"><span
class="type">string</span> `$code`</span> )

The <span class="function">runkit\_lint</span> function performs a
syntax (lint) check on the specified php code testing for scripting
errors. This is similar to using *php -l* from the command line except
<span class="function">runkit\_lint</span> accepts actual code rather
than a filename.

> **Note**: <span class="simpara">沙箱支持（是 <span
> class="function">runkit\_lint</span>，<span
> class="function">runkit\_lint\_file</span> 函数，与 <span
> class="classname">Runkit\_Sandbox</span> 类所必需）仅可用于 PHP 5.1.0
> 或 PHP 5.0 的特别修补版本，并需启用线程安全。更多信息可参见 runkit
> 包中的 `README` 文件。</span>

### 参数

`code`  
PHP Code to be lint checked

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">runkit\_lint\_file</span>

runkit\_method\_add
===================

Dynamically adds a new method to a given class

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_method\_add</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> , <span class="methodparam"><span
class="type">string</span> `$args`</span> , <span
class="methodparam"><span class="type">string</span> `$code`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = RUNKIT\_ACC\_PUBLIC</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$doc_comment`<span
class="initializer"> = **`NULL`**</span></span> \]\] )

<span class="type">bool</span> <span
class="methodname">runkit\_method\_add</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> , <span class="methodparam"><span
class="type">Closure</span> `$closure`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = RUNKIT\_ACC\_PUBLIC</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$doc_comment`<span
class="initializer"> = **`NULL`**</span></span> \]\] )

### 参数

`classname`  
The class to which this method will be added

`methodname`  
The name of the method to add

`args`  
Comma-delimited list of arguments for the newly-created method

`code`  
The code to be evaluated when `methodname` is called

`closure`  
A <span class="classname">closure</span> that defines the method.

`flags`  
The type of method to create, can be **`RUNKIT_ACC_PUBLIC`**,
**`RUNKIT_ACC_PROTECTED`** or **`RUNKIT_ACC_PRIVATE`** optionally
combined via bitwise OR with **`RUNKIT_ACC_STATIC`** (since 1.0.1)

`doc_comment`  
The doc comment of the function.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本         | 说明                                                        |
|--------------|-------------------------------------------------------------|
| runkit 1.0.4 | An alternative syntax expecting a `closure` has been added. |
| runkit 1.0.4 | The optional parameter `doc_comment` has been added.        |

### 范例

**示例 \#1 <span class="function">runkit\_method\_add</span> example**

``` php
<?php
class Example {
    function foo() {
        echo "foo!\n";
    }
}

// create an Example object
$e = new Example();

// Add a new public method
runkit_method_add(
    'Example',
    'add',
    '$num1, $num2',
    'return $num1 + $num2;',
    RUNKIT_ACC_PUBLIC
);

// add 12 + 4
echo $e->add(12, 4);
?>
```

以上例程会输出：

    16

### 参见

-   <span class="function">runkit\_method\_copy</span>
-   <span class="function">runkit\_method\_redefine</span>
-   <span class="function">runkit\_method\_remove</span>
-   <span class="function">runkit\_method\_rename</span>
-   <span class="function">runkit\_function\_add</span>

runkit\_method\_copy
====================

Copies a method from class to another

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_method\_copy</span> ( <span
class="methodparam"><span class="type">string</span> `$dClass`</span> ,
<span class="methodparam"><span class="type">string</span>
`$dMethod`</span> , <span class="methodparam"><span
class="type">string</span> `$sClass`</span> \[, <span
class="methodparam"><span class="type">string</span> `$sMethod`</span>
\] )

### 参数

`dClass`  
Destination class for copied method

`dMethod`  
Destination method name

`sClass`  
Source class of the method to copy

`sMethod`  
Name of the method to copy from the source class. If this parameter is
omitted, the value of `dMethod` is assumed.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">runkit\_method\_copy</span> example**

``` php
<?php
class Foo {
    function example() {
        return "foo!\n";
    }
}

class Bar {
    // initially, no methods
}

// copy the example() method from the Foo class to the Bar class, as baz()
runkit_method_copy('Bar', 'baz', 'Foo', 'example');

// output copied function
echo Bar::baz();
?>
```

以上例程会输出：

    foo!

### 参见

-   <span class="function">runkit\_method\_add</span>
-   <span class="function">runkit\_method\_redefine</span>
-   <span class="function">runkit\_method\_remove</span>
-   <span class="function">runkit\_method\_rename</span>
-   <span class="function">runkit\_function\_copy</span>

runkit\_method\_redefine
========================

Dynamically changes the code of the given method

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_method\_redefine</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> , <span class="methodparam"><span
class="type">string</span> `$args`</span> , <span
class="methodparam"><span class="type">string</span> `$code`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = RUNKIT\_ACC\_PUBLIC</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$doc_comment`<span
class="initializer"> = **`NULL`**</span></span> \]\] )

<span class="type">bool</span> <span
class="methodname">runkit\_method\_redefine</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> , <span class="methodparam"><span
class="type">Closure</span> `$closure`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = RUNKIT\_ACC\_PUBLIC</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$doc_comment`<span
class="initializer"> = **`NULL`**</span></span> \]\] )

> **Note**: <span
> class="simpara">此函数不能用来操作当前正常运行（或运行链上）的方法。</span>

### 参数

`classname`  
The class in which to redefine the method

`methodname`  
The name of the method to redefine

`args`  
Comma-delimited list of arguments for the redefined method

`code`  
The new code to be evaluated when `methodname` is called

`closure`  
A <span class="classname">closure</span> that defines the method.

`flags`  
The redefined method can be **`RUNKIT_ACC_PUBLIC`**,
**`RUNKIT_ACC_PROTECTED`** or **`RUNKIT_ACC_PRIVATE`** optionally
combined via bitwise OR with **`RUNKIT_ACC_STATIC`** (since 1.0.1)

`doc_comment`  
The doc comment of the function.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本         | 说明                                                        |
|--------------|-------------------------------------------------------------|
| runkit 1.0.4 | An alternative syntax expecting a `closure` has been added. |
| runkit 1.0.4 | The optional parameter `doc_comment` has been added.        |

### 范例

**示例 \#1 <span class="function">runkit\_method\_redefine</span>
example**

``` php
<?php
class Example {
    function foo() {
        return "foo!\n";
    }
}

// create an Example object
$e = new Example();

// output Example::foo() (before redefine)
echo "Before: " . $e->foo();

// Redefine the 'foo' method
runkit_method_redefine(
    'Example',
    'foo',
    '',
    'return "bar!\n";',
    RUNKIT_ACC_PUBLIC
);

// output Example::foo() (after redefine)
echo "After: " . $e->foo();
?>
```

以上例程会输出：

    Before: foo!
    After: bar!

### 参见

-   <span class="function">runkit\_method\_add</span>
-   <span class="function">runkit\_method\_copy</span>
-   <span class="function">runkit\_method\_remove</span>
-   <span class="function">runkit\_method\_rename</span>
-   <span class="function">runkit\_function\_redefine</span>

runkit\_method\_remove
======================

Dynamically removes the given method

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_method\_remove</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> )

> **Note**: <span
> class="simpara">此函数不能用来操作当前正常运行（或运行链上）的方法。</span>

### 参数

`classname`  
The class in which to remove the method

`methodname`  
The name of the method to remove

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">runkit\_method\_remove</span>
example**

``` php
<?php
class Example {
    function foo() {
        return "foo!\n";
    }

    function bar() {
        return "bar!\n";
    }
}

// Remove the 'foo' method
runkit_method_remove(
    'Example',
    'foo'
);

echo implode(' ', get_class_methods('Example'));

?>
```

以上例程会输出：

    bar

### 参见

-   <span class="function">runkit\_method\_add</span>
-   <span class="function">runkit\_method\_copy</span>
-   <span class="function">runkit\_method\_redefine</span>
-   <span class="function">runkit\_method\_rename</span>
-   <span class="function">runkit\_function\_remove</span>

runkit\_method\_rename
======================

Dynamically changes the name of the given method

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_method\_rename</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> , <span class="methodparam"><span
class="type">string</span> `$newname`</span> )

> **Note**: <span
> class="simpara">此函数不能用来操作当前正常运行（或运行链上）的方法。</span>

### 参数

`classname`  
The class in which to rename the method

`methodname`  
The name of the method to rename

`newname`  
The new name to give to the renamed method

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">runkit\_method\_rename</span>
example**

``` php
<?php
class Example {
    function foo() {
        return "foo!\n";
    }
}

// Rename the 'foo' method to 'bar'
runkit_method_rename(
    'Example',
    'foo',
    'bar'
);

// output renamed function
echo Example::bar();
?>
```

以上例程会输出：

    foo!

### 参见

-   <span class="function">runkit\_method\_add</span>
-   <span class="function">runkit\_method\_copy</span>
-   <span class="function">runkit\_method\_redefine</span>
-   <span class="function">runkit\_method\_remove</span>
-   <span class="function">runkit\_function\_rename</span>

runkit\_return\_value\_used
===========================

Determines if the current functions return value will be used

### 说明

<span class="type">bool</span> <span
class="methodname">runkit\_return\_value\_used</span> ( <span
class="methodparam">void</span> )

### 返回值

Returns **`TRUE`** if the function's return value is used by the calling
scope, otherwise **`FALSE`**

### 范例

**示例 \#1 <span class="function">runkit\_return\_value\_used</span>
example**

``` php
<?php
function foo() {
  var_dump(runkit_return_value_used());
}

foo();
$f = foo();
?>
```

以上例程会输出：

    bool(false)
    bool(true)

runkit\_sandbox\_output\_handler
================================

Specify a function to capture and/or process output from a runkit
sandbox

### 说明

<span class="type">mixed</span> <span
class="methodname">runkit\_sandbox\_output\_handler</span> ( <span
class="methodparam"><span class="type">object</span> `$sandbox`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$callback`</span> \] )

Ordinarily, anything output (such as with <span
class="function">echo</span> or <span class="function">print</span>)
will be output as though it were printed from the parent's scope. Using
<span class="function">runkit\_sandbox\_output\_handler</span> however,
output generated by the sandbox (including errors), can be captured by a
function outside of the sandbox.

> **Note**: <span class="simpara">沙箱支持（是 <span
> class="function">runkit\_lint</span>，<span
> class="function">runkit\_lint\_file</span> 函数，与 <span
> class="classname">Runkit\_Sandbox</span> 类所必需）仅可用于 PHP 5.1.0
> 或 PHP 5.0 的特别修补版本，并需启用线程安全。更多信息可参见 runkit
> 包中的 `README` 文件。</span>

> **Note**: **Deprecated**  
>
> As of runkit version 0.5, this function is deprecated and is scheduled
> to be removed from the package prior to a 1.0 release. The output
> handler for a given Runkit\_Sandbox instance may be read/set using the
> array offset syntax shown on the
> <a href="/ref/runkit.html#Runkit_Sandbox" class="link">Runkit_Sandbox</a>
> class definition page.

### 参数

`sandbox`  
Object instance of Runkit\_Sandbox class on which to set output
handling.

`callback`  
Name of a function which expects one parameter. Output generated by
`sandbox` will be passed to this callback. Anything returned by the
callback will be displayed normally. If this parameter is not passed
then output handling will not be changed. If a non-truth value is
passed, output handling will be disabled and will revert to direct
display.

### 返回值

Returns the name of the previously defined output handler callback, or
**`FALSE`** if no handler was previously defined.

### 范例

**示例 \#1 Feeding output to a variable**

``` php
<?php
function capture_output($str) {
  $GLOBALS['sandbox_output'] .= $str;

  return '';
}

$sandbox_output = '';

$php = new Runkit_Sandbox();
runkit_sandbox_output_handler($php, 'capture_output');
$php->echo("Hello\n");
$php->eval('var_dump("Excuse me");');
$php->die("I lost myself.");
unset($php);

echo "Sandbox Complete\n\n";
echo $sandbox_output;
?>
```

以上例程会输出：

    Sandbox Complete

    Hello
    string(9) "Excuse me"
    I lost myself.

runkit\_superglobals
====================

Return numerically indexed array of registered superglobals

### 说明

<span class="type">array</span> <span
class="methodname">runkit\_superglobals</span> ( <span
class="methodparam">void</span> )

### 返回值

Returns a numerically indexed array of the currently registered
superglobals. i.e. \_GET, \_POST, \_REQUEST, \_COOKIE, \_SESSION,
\_SERVER, \_ENV, \_FILES

### 参见

-   <a href="/language/variables/scope.html" class="link">Variable Scope</a>

**目录**

-   [Runkit\_Sandbox](/ref/runkit.html#Runkit_Sandbox) — Runkit Sandbox
    Class -- PHP Virtual Machine
-   [Runkit\_Sandbox\_Parent](/ref/runkit.html#Runkit_Sandbox_Parent) —
    Runkit Anti-Sandbox Class
-   [runkit\_class\_adopt](/ref/runkit.html#runkit_class_adopt) —
    Convert a base class to an inherited class, add ancestral methods
    when appropriate
-   [runkit\_class\_emancipate](/ref/runkit.html#runkit_class_emancipate)
    — Convert an inherited class to a base class, removes any method
    whose scope is ancestral
-   [runkit\_constant\_add](/ref/runkit.html#runkit_constant_add) —
    Similar to define(), but allows defining in class definitions as
    well
-   [runkit\_constant\_redefine](/ref/runkit.html#runkit_constant_redefine)
    — Redefine an already defined constant
-   [runkit\_constant\_remove](/ref/runkit.html#runkit_constant_remove)
    — Remove/Delete an already defined constant
-   [runkit\_function\_add](/ref/runkit.html#runkit_function_add) — Add
    a new function, similar to create\_function
-   [runkit\_function\_copy](/ref/runkit.html#runkit_function_copy) —
    Copy a function to a new function name
-   [runkit\_function\_redefine](/ref/runkit.html#runkit_function_redefine)
    — Replace a function definition with a new implementation
-   [runkit\_function\_remove](/ref/runkit.html#runkit_function_remove)
    — Remove a function definition
-   [runkit\_function\_rename](/ref/runkit.html#runkit_function_rename)
    — Change a function's name
-   [runkit\_import](/ref/runkit.html#runkit_import) — Process a PHP
    file importing function and class definitions, overwriting where
    appropriate
-   [runkit\_lint\_file](/ref/runkit.html#runkit_lint_file) — Check the
    PHP syntax of the specified file
-   [runkit\_lint](/ref/runkit.html#runkit_lint) — Check the PHP syntax
    of the specified php code
-   [runkit\_method\_add](/ref/runkit.html#runkit_method_add) —
    Dynamically adds a new method to a given class
-   [runkit\_method\_copy](/ref/runkit.html#runkit_method_copy) — Copies
    a method from class to another
-   [runkit\_method\_redefine](/ref/runkit.html#runkit_method_redefine)
    — Dynamically changes the code of the given method
-   [runkit\_method\_remove](/ref/runkit.html#runkit_method_remove) —
    Dynamically removes the given method
-   [runkit\_method\_rename](/ref/runkit.html#runkit_method_rename) —
    Dynamically changes the name of the given method
-   [runkit\_return\_value\_used](/ref/runkit.html#runkit_return_value_used)
    — Determines if the current functions return value will be used
-   [runkit\_sandbox\_output\_handler](/ref/runkit.html#runkit_sandbox_output_handler)
    — Specify a function to capture and/or process output from a runkit
    sandbox
-   [runkit\_superglobals](/ref/runkit.html#runkit_superglobals) —
    Return numerically indexed array of registered superglobals
