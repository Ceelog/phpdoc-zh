UNSET\_VAR
----------

PHP code
--------

``` php
<?php
/*
 * Unset the variable and store the original value into "result".
 * opcode number: 74
 */
$x = 1;
$a='x';
unset($$a);
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$x, !1=$a

| line | \#  | op         | fetch | ext | return | operands |
|------|-----|------------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN     |       |     |        | !0,1     |
| 7    | 1   | ASSIGN     |       |     |        | !1,'x'   |
| 8    | 2   | UNSET\_VAR |       |     | $2     | !1       |
| 9    | 3   | RETURN     |       |     |        | 1        |
