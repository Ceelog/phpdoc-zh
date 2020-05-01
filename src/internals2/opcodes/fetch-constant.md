FETCH\_CONSTANT
---------------

PHP code
--------

``` php
<?php
/*
 * Fetch the constant value bound to the specified name (name) and stores it into a variable (result).
 * opcode number: 99
 */
define("FOO", "something");
echo FOO;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op              | fetch | ext | return | operands    |
|------|-----|-----------------|-------|-----|--------|-------------|
| 6    | 0   | SEND\_VAL       |       |     |        | 'FOO'       |
|      | 1   | SEND\_VAL       |       |     |        | 'something' |
|      | 2   | DO\_FCALL       |       | 2   |        | 'define'    |
| 7    | 3   | FETCH\_CONSTANT |       |     | \~1    | 'FOO'       |
|      | 4   | ECHO            |       |     |        | \~1         |
| 8    | 5   | RETURN          |       |     |        | 1           |
