MOD
---

PHP code
--------

``` php
<?php
/*
 * Makes the value of "result" congruent to "value1" modulo "value2".
 * opcode number: 5
 */
echo 6 % 3;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | MOD    |       |     | \~0    | 6,3      |
|      | 1   | ECHO   |       |     |        | \~0      |
| 7    | 2   | RETURN |       |     |        | 1        |
