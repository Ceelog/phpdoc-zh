CONCAT
------

PHP code
--------

``` php
<?php
/*
 * Concats string values string1 and string2
 * opcode number: 8
 */
echo "hello" . "world";
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands        |
|------|-----|--------|-------|-----|--------|-----------------|
| 6    | 0   | CONCAT |       |     | \~0    | 'hello','world' |
|      | 1   | ECHO   |       |     |        | \~0             |
| 7    | 2   | RETURN |       |     |        | 1               |
