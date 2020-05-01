ASSIGN\_MUL
-----------

PHP code
--------

``` php
<?php
/*
 * Multiply result by value1 and store in variable indicated by result
 * opcode number: 25
 */
$a*=3;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op          | fetch | ext | return | operands |
|------|-----|-------------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN\_MUL |       |     |        | !0,3     |
| 7    | 1   | RETURN      |       |     |        | 1        |
