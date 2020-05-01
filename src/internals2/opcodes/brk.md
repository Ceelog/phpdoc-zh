BRK
---

PHP code
--------

``` php
<?php
/*
 * ???  End of a case block exists the current switch block.  Followed by JMP?
 * opcode number: 50
 */
$x = 0;
while(1) {
    if($x == 0) break;
}
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$x

| line | \#  | op        | fetch | ext | return | operands |
|------|-----|-----------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN    |       |     |        | !0,0     |
| 7    | 1   | JMPZ      |       |     |        | 1,-\>7   |
| 8    | 2   | IS\_EQUAL |       |     | \~1    | !0,0     |
|      | 3   | JMPZ      |       |     |        | \~1,-\>6 |
|      | 4   | BRK       |       |     |        | 1        |
|      | 5   | JMP       |       |     |        | -\>6     |
| 9    | 6   | JMP       |       |     |        | -\>1     |
| 10   | 7   | RETURN    |       |     |        | 1        |
