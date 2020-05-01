FETCH\_W
--------

PHP code
--------

``` php
<?php
/*
 * Fetch the value of the varible of "name" to assign it to a variable?  Write-only?
 * opcode number: 83
 */
$x = 1;
$a = 'x';
$$a = 2;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$x, !1=$a

| line | \#  | op       | fetch | ext | return | operands |
|------|-----|----------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN   |       |     |        | !0,1     |
| 7    | 1   | ASSIGN   |       |     |        | !1,'x'   |
| 8    | 2   | FETCH\_W | local |     | $2     | !1       |
|      | 3   | ASSIGN   |       |     |        | $2,2     |
| 9    | 4   | RETURN   |       |     |        | 1        |
