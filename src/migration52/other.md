Other Enhancements
------------------

-   <span class="simpara"> Improved memory manager and increased default
    memory limit. </span> <span class="simpara"> The new memory manager
    allocates less memory and works faster than the previous
    incarnation. It allocates memory from the system in large blocks,
    and then manages the heap by itself. The *memory\_limit* value in
    `php.ini` is checked, not for each *emalloc()* call (as before), but
    for actual blocks requested from the system. This means that
    *memory\_limit* is far more accurate than it used to be, since the
    old memory manager didn't calculate all the memory overhead used by
    the *malloc* library. </span> <span class="simpara"> Thanks to this
    new-found accuracy memory usage may appear to have increased,
    although actually it has not. To accommodate this apparent increase,
    the default *memory\_limit* setting was also increased - from 8 to
    16 megabytes. </span>
-   <span class="simpara"> Added support for constructors in interfaces
    to force constructor signature checks in implementations. </span>
    <span class="simpara"> Starting with PHP 5.2.0, interfaces can have
    constructors. However, if you choose to declare a constructor in an
    interface, each class implementing that interface MUST include a
    constructor with a signature matching that of the base interface
    constructor. By 'signature' we mean the parameter and return type
    definitions, including any type hints and including whether the data
    is passed by reference or by value. </span>
