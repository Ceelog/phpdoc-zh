SUB
---

PHP code
--------

``` php
<?php
/*
 * Subtracts "value2" from "value1" and stores the result into "result".
 * opcode number: 2
 */
echo 1-2;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | SUB    |       |     | \~0    | 1,2      |
|      | 1   | ECHO   |       |     |        | \~0      |
| 7    | 2   | RETURN |       |     |        | 1        |
