异常处理
========

**目录**

-   [扩展（extend） PHP
    内置的异常处理类](/language/exceptions/extending.html)

PHP 5 has an exception model similar to that of other programming
languages. An exception can be
<a href="/language/exceptions.html" class="link"><em>throw</em></a>n,
and caught
("<a href="/language/exceptions.html#language.exceptions.catch" class="link"><em>catch</em></a>ed")
within PHP. Code may be surrounded in a
<a href="/language/exceptions.html" class="link"><em>try</em></a> block,
to facilitate the catching of potential exceptions. Each
<a href="/language/exceptions.html" class="link"><em>try</em></a> must
have at least one corresponding
<a href="/language/exceptions.html#language.exceptions.catch" class="link"><em>catch</em></a>
or
<a href="/language/exceptions.html#language.exceptions.finally" class="link"><em>finally</em></a>
block.

The thrown object must be an instance of the <span
class="classname">Exception</span> class or a subclass of <span
class="classname">Exception</span>. Trying to throw an object that is
not will result in a PHP Fatal Error.

Multiple
<a href="/language/exceptions.html#language.exceptions.catch" class="link"><em>catch</em></a>
blocks can be used to catch different classes of exceptions. Normal
execution (when no exception is thrown within the
<a href="/language/exceptions.html" class="link"><em>try</em></a> block)
will continue after that last
<a href="/language/exceptions.html#language.exceptions.catch" class="link"><em>catch</em></a>
block defined in sequence. Exceptions can be
<a href="/language/exceptions.html" class="link"><em>throw</em></a>n (or
re-thrown) within a
<a href="/language/exceptions.html#language.exceptions.catch" class="link"><em>catch</em></a>
block.

When an exception is thrown, code following the statement will not be
executed, and PHP will attempt to find the first matching
<a href="/language/exceptions.html#language.exceptions.catch" class="link"><em>catch</em></a>
block. If an exception is not caught, a PHP Fatal Error will be issued
with an "*Uncaught Exception ...*" message, unless a handler has been
defined with <span class="function">set\_exception\_handler</span>.

In PHP 5.5 and later, a
<a href="/language/exceptions.html#language.exceptions.finally" class="link"><em>finally</em></a>
block may also be specified after or instead of
<a href="/language/exceptions.html#language.exceptions.catch" class="link"><em>catch</em></a>
blocks. Code within the
<a href="/language/exceptions.html#language.exceptions.finally" class="link"><em>finally</em></a>
block will always be executed after the
<a href="/language/exceptions.html" class="link"><em>try</em></a> and
<a href="/language/exceptions.html#language.exceptions.catch" class="link"><em>catch</em></a>
blocks, regardless of whether an exception has been thrown, and before
normal execution resumes.

> **Note**:
>
> Internal PHP functions mainly use
> <a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">Error reporting</a>,
> only modern
> <a href="/language/oop5.html" class="link">Object oriented</a>
> extensions use exceptions. However, errors can be simply translated to
> exceptions with
> <a href="/class/errorexception.html" class="link">ErrorException</a>.

**小贴士**

The
<a href="/intro/spl.html" class="link">Standard PHP Library (SPL)</a>
provides a good number of
<a href="/spl/exceptions.html" class="link">built-in exceptions</a>.

**示例 \#1 Throwing an Exception**

``` php
<?php
function inverse($x) {
    if (!$x) {
        throw new Exception('Division by zero.');
    }
    return 1/$x;
}

try {
    echo inverse(5) . "\n";
    echo inverse(0) . "\n";
} catch (Exception $e) {
    echo 'Caught exception: ',  $e->getMessage(), "\n";
}

// Continue execution
echo "Hello World\n";
?>
```

以上例程会输出：

    0.2
    Caught exception: Division by zero.
    Hello World

**示例 \#2 Exception handling with a *finally* block**

``` php
<?php
function inverse($x) {
    if (!$x) {
        throw new Exception('Division by zero.');
    }
    return 1/$x;
}

try {
    echo inverse(5) . "\n";
} catch (Exception $e) {
    echo 'Caught exception: ',  $e->getMessage(), "\n";
} finally {
    echo "First finally.\n";
}

try {
    echo inverse(0) . "\n";
} catch (Exception $e) {
    echo 'Caught exception: ',  $e->getMessage(), "\n";
} finally {
    echo "Second finally.\n";
}

// Continue execution
echo "Hello World\n";
?>
```

以上例程会输出：

    0.2
    First finally.
    Caught exception: Division by zero.
    Second finally.
    Hello World

**示例 \#3 Nested Exception**

``` php
<?php

class MyException extends Exception { }

class Test {
    public function testing() {
        try {
            try {
                throw new MyException('foo!');
            } catch (MyException $e) {
                // rethrow it
                throw $e;
            }
        } catch (Exception $e) {
            var_dump($e->getMessage());
        }
    }
}

$foo = new Test;
$foo->testing();

?>
```

以上例程会输出：

    string(4) "foo!"
