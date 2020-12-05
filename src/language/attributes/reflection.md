Reading Attributes with the Reflection API
------------------------------------------

To access attributes from classes, methods, functions, parameters,
properties and class constants, the Reflection API provides the method
<span class="function">getAttributes</span> on each of the corresponding
Reflection objects. This method returns an array of <span
class="classname">ReflectionAttribute</span> instances that can be
queried for attribute name, arguments and to instantiate an instance of
the represented attribute.

This separation of reflected attribute representation from actual
instance increases control of the programmer to handle errors regarding
missing attribute classes, mistyped or missing arguments. Only after
calling <span class="function">newInstance</span>, objects of the
attribute class are instantiated and the correct matching of arguments
is validated, not earlier.

**示例 \#1 Reading Attributes using Reflection API**

``` php
<?php

#[Attribute]
class MyAttribute
{
    public $value;

    public function __construct($value)
    {
        $this->value = $value;
    }
}

#[MyAttribute(value: 1234)]
class Thing
{
}

function dumpAttributeData($reflection) {
    $attributes = $reflection->getAttributes();

    foreach ($attributes as $attribute) {
       var_dump($attribute->getName());
       var_dump($attribute->getArguments());
       var_dump($attribute->newInstance());
    }
}

dumpAttributeData(new ReflectionClass(Thing::class));
/*
string(11) "MyAttribute"
array(1) {
  ["value"]=>
  int(1234)
}
object(MyAttribute)#3 (1) {
  ["value"]=>
  int(1234)
}
*/
```

Instead of iterating all attributes on the reflection instance, only
those of a particular attribute class can be retrieved by passing the
searched attribute class name as argument.

**示例 \#2 Reading Specific Attributes using Reflection API**

``` php
<?php

function dumpMyAttributeData($reflection) {
    $attributes = $reflection->getAttributes(MyAttribute::class);

    foreach ($attributes as $attribute) {
       var_dump($attribute->getName());
       var_dump($attribute->getArguments());
       var_dump($attribute->newInstance());
    }
}

dumpAttributeData(new ReflectionClass(Thing::class));
```
