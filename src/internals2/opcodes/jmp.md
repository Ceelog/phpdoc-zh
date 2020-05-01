JMP
---

PHP code
--------

``` php
<?php 
/*
 * Unconditonally jump to the address
 * opcode number: 42
 */
$foo = false;
while(!$foo) {
    $foo = true;
}
?>
```

PHP opcodes
-----------

Function name: (null)

compiled vars: !0 = $foo

| line | \#  | op        | fetch | ext | return | operands  |
|------|-----|-----------|-------|-----|--------|-----------|
| 6    | 0   | ASSIGN    |       |     |        | !0, false |
| 7    | 1   | BOOL\_NOT |       |     | \~1    | !0        |
|      | 2   | JMPZ      |       |     |        | \~1, -\>5 |
| 8    | 3   | ASSIGN    |       |     |        | !0, true  |
| 9    | 4   | JMP       |       |     |        | -\>1      |
| 11   | 5   | RETURN    |       |     |        | 1         |
