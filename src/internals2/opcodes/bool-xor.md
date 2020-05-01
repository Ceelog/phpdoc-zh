BOOL\_XOR
---------

PHP code
--------

``` php
<?php
/*
 * Boolean (logical) xor of value1
 * opcode number: 14
 */
echo 1 xor 2;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op        | fetch | ext | return | operands |
|------|-----|-----------|-------|-----|--------|----------|
| 6    | 0   | BOOL\_XOR |       |     | \~0    | 1,2      |
|      | 1   | ECHO      |       |     |        | \~0      |
| 7    | 2   | RETURN    |       |     |        | 1        |
