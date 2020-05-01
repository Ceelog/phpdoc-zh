The uopz - User Operations for Zend - extension exposes Zend Engine
functionality normally used at compilation and execution time in order
to allow modification of the internal structures that represent PHP
code, and for user code to interact with the VM.

uopz supports the following activities:

-   Overloading some opcodes including ZEND\_EXIT and ZEND\_NEW
-   Backup and restore functions and methods
-   Renaming functions and methods
-   Copying of functions and methods
-   Deletion of functions and methods
-   Redefinition of global and class constants
-   Deletion of global and class constants
-   Runtime composition and modification of classes

> **Note**:
>
> All of the activities supported are compatible with opcache
