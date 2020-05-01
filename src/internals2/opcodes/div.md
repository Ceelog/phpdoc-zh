DIV
---

PHP code
--------

``` php
<?php
/*
 * Divides "value1" by "value2" and stores the result into "result".
 * opcode number: 4
 */
echo 6/3;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | DIV    |       |     | \~0    | 6,3      |
|      | 1   | ECHO   |       |     |        | \~0      |
| 7    | 2   | RETURN |       |     |        | 1        |
