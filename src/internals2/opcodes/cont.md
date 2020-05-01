CONT
----

PHP code
--------

``` php
<?php 
/*
 * Continue next iteration of current loop level
 * opcode number: 51
 */
$foo = false;
while(!$foo) {
    $foo = true;
    continue;
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
| 9    | 4   | CONT      |       |     |        | 1         |
| 10   | 5   | JMP       |       |     |        | -\>1      |
| 12   | 6   | RETURN    |       |     |        | 1         |
