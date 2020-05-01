JMPZNZ
------

PHP code
--------

``` php
<?php
/*
 * Jump to the address given in the operands if the value is zero;
 * jump to the address given in extended data if nonzero.
 * opcode number: 45
 */
for($i=0; $i<3; $i++){ 
    echo "hi";
}
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$i

| line | \#  | op          | fetch | ext | return | operands |
|------|-----|-------------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN      |       |     |        | !0,0     |
|      | 1   | IS\_SMALLER |       |     | \~1    | !0,3     |
|      | 2   | JMPZNZ      |       | 6   |        | \~1,-\>8 |
|      | 3   | POST\_INC   |       |     | \~2    | !0       |
|      | 4   | FREE        |       |     |        | \~2      |
|      | 5   | JMP         |       |     |        | -\>1     |
| 7    | 6   | ECHO        |       |     |        | 'hi'     |
| 8    | 7   | JMP         |       |     |        | -\>3     |
| 9    | 8   | RETURN      |       |     |        | 1        |
