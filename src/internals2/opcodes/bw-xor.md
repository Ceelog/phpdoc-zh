BW\_XOR
-------

PHP code
--------

``` php
<?php
/*
 * Bit-wise xor of value1 and value2
 * opcode number: 11
 */
echo 1^2;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op      | fetch | ext | return | operands |
|------|-----|---------|-------|-----|--------|----------|
| 6    | 0   | BW\_XOR |       |     | \~0    | 1,2      |
|      | 1   | ECHO    |       |     |        | \~0      |
| 7    | 2   | RETURN  |       |     |        | 1        |
