Declaring Attribute Classes
---------------------------

While not strictly required it is recommended to create an actual class
for every attribute. In the most simple case only an empty class is
needed with the *\#\[Attribute\]* attribute declared that can be
imported from the global namespace with a use statement.

**示例 \#1 Using target specification to restrict where attributes can
be used**

``` php
<?php

namespace Example;

use Attribute;

#[Attribute]
class MyAttribute
{
}
```

To restrict the type of declaration an attribute can be assigned to, a
bitmask can be passed as the first argument to the *\#\[Attribute\]*
declaration.

**示例 \#2 Simple Attribute Class**

``` php
<?php

namespace Example;

use Attribute;

#[Attribute(Attribute::TARGET_METHOD | Attribute::TARGET_FUNCTION)]
class MyAttribute
{
}
```

Declaring <span class="classname">MyAttribute</span> on another type
will now throw an exception during the call to <span
class="function">ReflectionAttribute::newInstance</span>

By default an attribute can only be used once per declaration. If the
attribute should be repeatable on declarations it must be specified as
part of the bitmask to the *\#\[Attribute\]* declaration.

**示例 \#3 Using IS\_REPEATBLE to allow attribute on a declaration
multiple times**

``` php
<?php

namespace Example;

use Attribute;

#[Attribute(Attribute::TARGET_METHOD | Attribute::TARGET_FUNCTION | Attribute::IS_REPEATABLE)]
class MyAttribute
{
}
```
