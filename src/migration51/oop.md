Class and object changes
------------------------

-   <a href="/migration51/oop.html#migration51.oop-functions" class="link"><em>instanceof</em>, <em>is_a()</em>, <em>is_subclass_of()</em> and <em>catch</em></a>

-   <a href="/migration51/oop.html#migration51.oop-methods" class="link">Abstract private methods</a>

-   <a href="/migration51/oop.html#migration51.oop-modifiers" class="link">Access modifiers in interfaces</a>

-   <a href="/migration51/oop.html#migration51.oop-inheritance" class="link">Changes in inheritance rules</a>

-   <a href="/migration51/oop.html#migration51.oop-constants" class="link">Class constants</a>

*instanceof*, *is\_a()*, *is\_subclass\_of()* and *catch*
---------------------------------------------------------

In PHP 5.0, *is\_a()* was deprecated and replaced by the *instanceof*
operator. There were some issues with the initial implementation of
*instanceof*, which relied on *\_\_autoload()* to search for missing
classes. If the class was not present, *instanceof* would throw a fatal
**`E_ERROR`** due to the failure of *\_\_autoload()* to discover that
class. The same behaviour occurred in the *catch* operator and the
*is\_subclass\_of()* function, for the same reason.

None of these functions or operators call *\_\_autoload()* in PHP 5.1.x,
and the *class\_exists()* workarounds used in code written for PHP
5.0.x, while not problematic in any way, are no longer necessary.

Abstract private methods
------------------------

Abstract private methods were supported between PHP 5.0.0 and PHP 5.0.4,
but were then disallowed on the grounds that the behaviours of *private*
and *abstract* are mutually exclusive.

Access modifiers in interfaces
------------------------------

Under PHP 5.0, function declarations in interfaces were treated in
exactly the same way as function declarations in classes. This has not
been the case since October 2004, at which point only the *public*
access modifier was allowed in interface function declarations. Since
April 2005 - which pre-dates the PHP 5.0b1 release - the *static*
modifier has also been allowed. However, the *protected* and *private*
modifiers will now throw an **`E_ERROR`**, as will *abstract*. Note that
this change should not affect your existing code, as none of these
modifiers makes sense in the context of interfaces anyway.

Changes in inheritance rules
----------------------------

Under PHP 5.0, it was possible to have a function declaration in a
derived class that did not match the declaration of the same function in
the base class, e.g.

This code will cause an **`E_STRICT`** error to be emitted under PHP
5.1.x.

``` php
<?php
class Base {
    function &return_by_ref() {
        $r = 1;
        return $r;
    }
}

class Derived extends Base {
    function return_by_ref() {
        return 1;
    }
}
?>
```

Class constants
---------------

Under PHP 5.0.x, the following code was valid:

Under PHP 5.1.x, redefinition of a class constant will throw a fatal
**`E_ERROR`**.

``` php
<?php
class test {
    const foobar = 'foo';
    const foobar = 'bar';
}

?>
```
