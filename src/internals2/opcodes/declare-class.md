DECLARE\_CLASS
--------------

PHP code
--------

``` php
<?php
/*
 * Declare a class with the name of class-name as the implementation specified by ID.
 * opcode number: 139
 */
class A {
    function methodA(){
        echo "hello world";
    }
}
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | NOP    |       |     |        |          |
| 11   | 1   | RETURN |       |     |        | 1        |

Function name: methodA

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands      |
|------|-----|--------|-------|-----|--------|---------------|
| 8    | 0   | ECHO   |       |     |        | 'hello+world' |
| 9    | 1   | RETURN |       |     |        | null          |
