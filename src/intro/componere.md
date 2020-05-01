Componere <sub>(latin,\ English:\ compose)</sub> targets production
environments and provides an API for composition of classes, monkey
patching, and casting.

##### Composition:

<span class="classname">Componere\\Definition</span> is used to define
(or redefine) a class at runtime; The class can then be registered, and
in the case of redefinition it replaces the original class for as long
as the <span class="classname">Componere\\Definition</span> exists.

<span class="modifier">public</span> <span
class="methodname">Componere\\Definition::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="methodname">Componere\\Definition::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$parent`</span> )

<span class="modifier">public</span> <span
class="methodname">Componere\\Definition::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">array</span>
`$interfaces`</span> )

<span class="modifier">public</span> <span
class="methodname">Componere\\Definition::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$parent`</span> , <span class="methodparam"><span
class="type">array</span> `$interfaces`</span> )

##### Patching:

<span class="classname">Componere\\Patch</span> is used to change the
class of a specific instance of an object at runtime; Upon application
the patch will remain applied for as long as the <span
class="classname">Componere\\Patch</span> exists, and can be reverted
explicitly.

<span class="modifier">public</span> <span
class="methodname">Componere\\Patch::\_\_construct</span> ( <span
class="methodparam"><span class="type">object</span> `$instance`</span>
)

<span class="modifier">public</span> <span
class="methodname">Componere\\Patch::\_\_construct</span> ( <span
class="methodparam"><span class="type">object</span> `$instance`</span>
, <span class="methodparam"><span class="type">array</span>
`$interfaces`</span> )

##### Casting:

<span class="classname">Componere\\</span> casting functions can cast
among user defined compatible types; Where compatible means <span
class="classname">Type</span> is sub or super to the type of `object`.

<span class="type">Type</span> <span
class="methodname">Componere\\cast</span> ( <span
class="methodparam"><span class="type">Type</span> `$type`</span> ,
<span class="methodparam"> `$object`</span> )

<span class="type">Type</span> <span
class="methodname">Componere\\cast\_by\_ref</span> ( <span
class="methodparam"><span class="type">Type</span> `$type`</span> ,
<span class="methodparam"> `$object`</span> )
