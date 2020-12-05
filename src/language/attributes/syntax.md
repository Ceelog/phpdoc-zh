Attribute syntax
----------------

There are several parts to the attributes syntax. First, attribute
declaration are always enclosed with a starting *\#\[* and a
corresponding ending *\]*. Inside, one or many attributes are listed,
seperated by comma. The attribute name is an unqualified, qualified or
fully-qualified name as described in
<a href="/language/namespaces/basics.html" class="link">Using Namespaces Basics</a>.
Arguments to the attribute are optional, but are enclosed in the usual
parenthesis *()*. Arguments to attributes can only be literal values or
constant expressions. Both positional and named arguments syntax can be
used.

Attribute names and their arguments are resolved to a class and the
arguments are passed to its constructor, when an instance of the
attribute is requested through the Reflection API. As such a class
should be introduced for each attribute.

**示例 \#1 Attribute Syntax**

``` php
<?php
// a.php
namespace MyExample;

use Attribute;

#[Attribute]
class MyAttribute
{
    const VALUE = 'value';

    private $value;

    public function __construct($value = null)
    {
        $this->value = $value;
    }
}

// b.php

namespace Another;

use MyExample\MyAttribute;

#[MyAttribute]
#[\MyExample\MyAttribute]
#[MyAttribute(1234)]
#[MyAttribute(value: 1234)]
#[MyAttribute(MyAttribute::VALUE)]
#[MyAttribute(array("key" => "value"))]
#[MyAttribute(100 + 200)]
class Thing
{
}

#[MyAttribute(1234), MyAttribute(5678)]
class AnotherThing
{
}
```
