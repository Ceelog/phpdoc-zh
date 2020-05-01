SR
--

PHP code
--------

``` php
<?php
/*
 * Shift bits of value1 to the right value2 steps (each step means "divide by two")
 * opcode number: 7
 */
echo 8 >> 2;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | SR     |       |     | \~0    | 8,2      |
|      | 1   | ECHO   |       |     |        | \~0      |
| 7    | 2   | RETURN |       |     |        | 1        |
