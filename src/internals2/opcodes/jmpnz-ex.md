JMPNZ\_EX
---------

PHP code
--------

``` php
<?php
/*
 * Jump to the address if the xor of value1 and value2 is zero .. ???
 * opcode number: 47
 */
if(1^2) return;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op      | fetch | ext | return | operands |
|------|-----|---------|-------|-----|--------|----------|
| 6    | 0   | BW\_XOR |       |     | \~0    | 1,2      |
|      | 1   | JMPZ    |       |     |        | \~0,-\>4 |
|      | 2   | RETURN  |       |     |        | null     |
|      | 3   | JMP     |       |     |        | -\>4     |
| 7    | 4   | RETURN  |       |     |        | 1        |
