预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

The following opcodes are defined as constants by uopz before 5.0.0:

**`ZEND_EXIT`** (<span class="type">integer</span>)  
<span class="simpara"> Invoked by exit() and die(), receives no
arguments. Return boolean **`TRUE`** to exit, **`FALSE`** to continue
</span>

**`ZEND_NEW`** (<span class="type">integer</span>)  
<span class="simpara"> Invoked by object construction, receives the
class of object being created as the only argument </span>

**`ZEND_THROW`** (<span class="type">integer</span>)  
<span class="simpara"> Invoked by the throw construct, receives the
class of exception being thrown as the only argument </span>

**`ZEND_FETCH_CLASS`** (<span class="type">integer</span>)  
<span class="simpara"> Invoked upon composure, receives the class the
name of the class being fetched as the only argument </span>

**`ZEND_ADD_TRAIT`** (<span class="type">integer</span>)  
<span class="simpara"> Invoked upon composure, receives the class the
trait is being added to as the first argument, and the name of the trait
as the second argument </span>

**`ZEND_ADD_INTERFACE`** (<span class="type">integer</span>)  
<span class="simpara"> Invoked upon composure, receives the class the
interface is being added to as the first argument, and the name of the
interface as the second argument </span>

**`ZEND_INSTANCEOF`** (<span class="type">integer</span>)  
<span class="simpara"> Invoked by instanceof operator, receives the
object being verified as the first argument, and the name of the class
which that object should be as the second argument </span>

The following constants control the VM's behaviour after a user handler
is invoked, be extremely careful! These constants are removed as of uopz
5.0.0.

**`ZEND_USER_OPCODE_CONTINUE`** (<span class="type">integer</span>)  
<span class="simpara"> Advance 1 opcode and continuue </span>

**`ZEND_USER_OPCODE_ENTER`** (<span class="type">integer</span>)  
<span class="simpara"> Enter into new op\_array without recursion
</span>

**`ZEND_USER_OPCODE_LEAVE`** (<span class="type">integer</span>)  
<span class="simpara"> Return to calling op\_array within the same
executor </span>

**`ZEND_USER_OPCODE_DISPATCH`** (<span class="type">integer</span>)  
<span class="simpara"> Dispatch to original opcode handler </span>

**`ZEND_USER_OPCODE_DISPATCH_TO`** (<span class="type">integer</span>)  
<span class="simpara"> Dispatch to a specific handler (OR'd with ZEND
opcode constant) </span>

**`ZEND_USER_OPCODE_RETURN`** (<span class="type">integer</span>)  
<span class="simpara"> Exit from executor (return from function) </span>

The following modifiers are registered as constants by uopz

**`ZEND_ACC_PUBLIC`** (<span class="type">integer</span>)  
<span class="simpara"> Mark function as public, the default </span>

**`ZEND_ACC_PROTECTED`** (<span class="type">integer</span>)  
<span class="simpara"> Mark function as protected </span>

**`ZEND_ACC_PRIVATE`** (<span class="type">integer</span>)  
<span class="simpara"> Mark function as private </span>

**`ZEND_ACC_STATIC`** (<span class="type">integer</span>)  
<span class="simpara"> Mark function as static </span>

**`ZEND_ACC_FINAL`** (<span class="type">integer</span>)  
<span class="simpara"> Mark function as final </span>

**`ZEND_ACC_ABSTRACT`** (<span class="type">integer</span>)  
<span class="simpara"> Mark function as abstract </span>

**`ZEND_ACC_CLASS`** (<span class="type">integer</span>)  
<span class="simpara"> Dummy registered for consistency, the default
kind of class entry. Removed as of uopz 5.0.0. </span>

**`ZEND_ACC_INTERFACE`** (<span class="type">integer</span>)  
<span class="simpara"> Mark class as interface. Removed as of uopz
5.0.0. </span>

**`ZEND_ACC_TRAIT`** (<span class="type">integer</span>)  
<span class="simpara"> Mark class as trait. Removed as of uopz 5.0.0.
</span>

**`ZEND_ACC_FETCH`** (<span class="type">integer</span>)  
<span class="simpara"> Used for getting flags only. Removed as of uopz
5.0.0. </span>
