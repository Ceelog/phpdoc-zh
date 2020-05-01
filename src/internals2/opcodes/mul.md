MUL
---

PHP code
--------

``` php
<?php
/*
 * Multiplys "value1" by "value2" and stores the result into "result".
 * opcode number: 3
 */
echo 2*3;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | MUL    |       |     | \~0    | 2,3      |
|      | 1   | ECHO   |       |     |        | \~0      |
| 7    | 2   | RETURN |       |     |        | 1        |
