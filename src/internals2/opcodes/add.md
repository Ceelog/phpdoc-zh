ADD
---

PHP code
--------

``` php
<?php
/*
 * Adds "value1" to "value2" and stores the result into "result".
 * opcode number: 1
 */
echo 1 + 2;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | ADD    |       |     | \~0    | 1,2      |
|      | 1   | ECHO   |       |     |        | \~0      |
| 7    | 2   | RETURN |       |     |        | 1        |
