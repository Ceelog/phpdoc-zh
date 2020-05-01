FAQ: things you need to know about namespaces
---------------------------------------------

This FAQ is split into two sections: common questions, and some
specifics of implementation that are helpful to understand fully.

First, the common questions.

1.  <span class="simpara">
    <a href="/language/namespaces/faq.html#language.namespaces.faq.shouldicare" class="link">If I don't use namespaces, should I care about any of this?</a>
    </span>
2.  <span class="simpara">
    <a href="/language/namespaces/faq.html#language.namespaces.faq.globalclass" class="link">How do I use internal or global classes in a namespace?</a>
    </span>
3.  <span class="simpara">
    <a href="/language/namespaces/faq.html#language.namespaces.faq.innamespace" class="link">How do I use namespaces classes functions, or constants in their own namespace?</a>
    </span>
4.  <span class="simpara">
    <a href="/language/namespaces/faq.html#language.namespaces.faq.full" class="link">How does a name like <em>\my\name</em> or <em>\name</em> resolve?</a>
    </span>
5.  <span class="simpara">
    <a href="/language/namespaces/faq.html#language.namespaces.faq.qualified" class="link">How does a name like <em>my\name</em> resolve?</a>
    </span>
6.  <span class="simpara">
    <a href="/language/namespaces/faq.html#language.namespaces.faq.shortname1" class="link">How does an unqualified class name like <em>name</em> resolve?</a>
    </span>
7.  <span class="simpara">
    <a href="/language/namespaces/faq.html#language.namespaces.faq.shortname2" class="link">How does an unqualified function name or unqualified constant name like <em>name</em> resolve?</a>
    </span>

There are a few implementation details of the namespace implementations
that are helpful to understand.

1.  <span class="simpara">
    <a href="/language/namespaces/faq.html#language.namespaces.faq.conflict" class="link">Import names cannot conflict with classes defined in the same file.</a>
    </span>
2.  <span class="simpara">
    <a href="/language/namespaces/faq.html#language.namespaces.faq.nested" class="link">Nested namespaces are not allowed.</a>
    </span>
3.  <span class="simpara">
    <a href="/language/namespaces/faq.html#language.namespaces.faq.nofuncconstantuse" class="link">Neither functions nor constants can be imported via the <em>use</em> statement.</a>
    </span>
4.  <span class="simpara">
    <a href="/language/namespaces/faq.html#language.namespaces.faq.quote" class="link">Dynamic namespace names (quoted identifiers) should escape backslash.</a>
    </span>
5.  <span class="simpara">
    <a href="/language/namespaces/faq.html#language.namespaces.faq.constants" class="link">Undefined Constants referenced using any backslash die with fatal error</a>
    </span>
6.  <span class="simpara">
    <a href="/language/namespaces/faq.html#language.namespaces.faq.builtinconst" class="link">Cannot override special constants NULL, TRUE, FALSE, ZEND_THREAD_SAFE or ZEND_DEBUG_BUILD</a>
    </span>

### If I don't use namespaces, should I care about any of this?

No. Namespaces do not affect any existing code in any way, or any
as-yet-to-be-written code that does not contain namespaces. You can
write this code if you wish:

**示例 \#1 Accessing global classes outside a namespace**

``` php
<?php
$a = new \stdClass;
```

This is functionally equivalent to:

**示例 \#2 Accessing global classes outside a namespace**

``` php
<?php
$a = new stdClass;
```

### How do I use internal or global classes in a namespace?

**示例 \#3 Accessing internal classes in namespaces**

``` php
<?php
namespace foo;
$a = new \stdClass;

function test(\ArrayObject $typehintexample = null) {}

$a = \DirectoryIterator::CURRENT_AS_FILEINFO;

// extending an internal or global class
class MyException extends \Exception {}
?>
```

### How do I use namespaces classes, functions, or constants in their own namespace?

**示例 \#4 Accessing internal classes, functions or constants in
namespaces**

``` php
<?php
namespace foo;

class MyClass {}

// using a class from the current namespace as a type hint
function test(MyClass $typehintexample = null) {}
// another way to use a class from the current namespace as a type hint
function test(\foo\MyClass $typehintexample = null) {}

// extending a class from the current namespace
class Extended extends MyClass {}

// accessing a global function
$a = \globalfunc();

// accessing a global constant
$b = \INI_ALL;
?>
```

### How does a name like *\\my\\name* or *\\name* resolve?

Names that begin with a *\\* always resolve to what they look like, so
*\\my\\name* is in fact *my\\name*, and *\\Exception* is *Exception*.

**示例 \#5 Fully Qualified names**

``` php
<?php
namespace foo;
$a = new \my\name(); // instantiates "my\name" class
echo \strlen('hi'); // calls function "strlen"
$a = \INI_ALL; // $a is set to the value of constant "INI_ALL"
?>
```

### How does a name like *my\\name* resolve?

Names that contain a backslash but do not begin with a backslash like
*my\\name* can be resolved in 2 different ways.

If there is an import statement that aliases another name to *my*, then
the import alias is applied to the *my* in *my\\name*.

Otherwise, the current namespace name is prepended to *my\\name*.

**示例 \#6 Qualified names**

``` php
<?php
namespace foo;
use blah\blah as foo;

$a = new my\name(); // instantiates "foo\my\name" class
foo\bar::name(); // calls static method "name" in class "blah\blah\bar"
my\bar(); // calls function "foo\my\bar"
$a = my\BAR; // sets $a to the value of constant "foo\my\BAR"
?>
```

### How does an unqualified class name like *name* resolve?

Class names that do not contain a backslash like *name* can be resolved
in 2 different ways.

If there is an import statement that aliases another name to *name*,
then the import alias is applied.

Otherwise, the current namespace name is prepended to *name*.

**示例 \#7 Unqualified class names**

``` php
<?php
namespace foo;
use blah\blah as foo;

$a = new name(); // instantiates "foo\name" class
foo::name(); // calls static method "name" in class "blah\blah"
?>
```

### How does an unqualified function name or unqualified constant name like *name* resolve?

Function or constant names that do not contain a backslash like *name*
can be resolved in 2 different ways.

First, the current namespace name is prepended to *name*.

Finally, if the constant or function *name* does not exist in the
current namespace, a global constant or function *name* is used if it
exists.

**示例 \#8 Unqualified function or constant names**

``` php
<?php
namespace foo;
use blah\blah as foo;

const FOO = 1;

function my() {}
function foo() {}
function sort(&$a)
{
    sort($a);
    $a = array_flip($a);
    return $a;
}

my(); // calls "foo\my"
$a = strlen('hi'); // calls global function "strlen" because "foo\strlen" does not exist
$arr = array(1,3,2);
$b = sort($arr); // calls function "foo\sort"
$c = foo(); // calls function "foo\foo" - import is not applied

$a = FOO; // sets $a to value of constant "foo\FOO" - import is not applied
$b = INI_ALL; // sets $b to value of global constant "INI_ALL"
?>
```

### Import names cannot conflict with classes defined in the same file.

The following script combinations are legal:

file1.php

``` php
<?php
namespace my\stuff;
class MyClass {}
?>
```

another.php

``` php
<?php
namespace another;
class thing {}
?>
```

file2.php

``` php
<?php
namespace my\stuff;
include 'file1.php';
include 'another.php';

use another\thing as MyClass;
$a = new MyClass; // instantiates class "thing" from namespace another
?>
```

There is no name conflict, even though the class *MyClass* exists within
the *my\\stuff* namespace, because the MyClass definition is in a
separate file. However, the next example causes a fatal error on name
conflict because MyClass is defined in the same file as the use
statement.

``` php
<?php
namespace my\stuff;
use another\thing as MyClass;
class MyClass {} // fatal error: MyClass conflicts with import statement
$a = new MyClass;
?>
```

### Nested namespaces are not allowed.

PHP does not allow nesting namespaces

``` php
<?php
namespace my\stuff {
    namespace nested {
        class foo {}
    }
}
?>
```

However, it is easy to simulate nested namespaces like so:

``` php
<?php
namespace my\stuff\nested {
    class foo {}
}
?>
```

### Neither functions nor constants can be imported via the *use* statement.

The only elements that are affected by *use* statements are namespaces
and class names. In order to shorten a long constant or function, import
its containing namespace

``` php
<?php
namespace mine;
use ultra\long\ns\name;

$a = name\CONSTANT;
name\func();
?>
```

### Dynamic namespace names (quoted identifiers) should escape backslash

It is very important to realize that because the backslash is used as an
escape character within strings, it should always be doubled when used
inside a string. Otherwise there is a risk of unintended consequences:

**示例 \#9 Dangers of using namespaced names inside a double-quoted
string**

``` php
<?php
$a = new "dangerous\name"; // \n is a newline inside double quoted strings!
$obj = new $a;

$a = new 'not\at\all\dangerous'; // no problems here.
$obj = new $a;
?>
```

Inside a single-quoted string, the backslash escape sequence is much
safer to use, but it is still recommended practice to escape backslashes
in all strings as a best practice.

### Undefined Constants referenced using any backslash die with fatal error

Any undefined constant that is unqualified like *FOO* will produce a
notice explaining that PHP assumed *FOO* was the value of the constant.
Any constant, qualified or fully qualified, that contains a backslash
will produce a fatal error if not found.

**示例 \#10 Undefined constants**

``` php
<?php
namespace bar;
$a = FOO; // produces notice - undefined constants "FOO" assumed "FOO";
$a = \FOO; // fatal error, undefined namespace constant FOO
$a = Bar\FOO; // fatal error, undefined namespace constant bar\Bar\FOO
$a = \Bar\FOO; // fatal error, undefined namespace constant Bar\FOO
?>
```

### Cannot override special constants NULL, TRUE, FALSE, ZEND\_THREAD\_SAFE or ZEND\_DEBUG\_BUILD

Any attempt to define a namespaced constant that is a special, built-in
constant results in a fatal error

**示例 \#11 Undefined constants**

``` php
<?php
namespace bar;
const NULL = 0; // fatal error;
const true = 'stupid'; // also fatal error;
// etc.
?>
```
