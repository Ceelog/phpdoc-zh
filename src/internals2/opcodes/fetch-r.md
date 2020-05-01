FETCH\_R
--------

PHP code
--------

``` php
<?php
/*
 * Fetch the value of the varible of "name" to assign it to a variable?  Read-only?
 * opcode number: 80
 */
$x = 1;
$a = 'x';
echo $$a;
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
| 8    | 2   | FETCH\_R | local |     | $2     | !1       |
|      | 3   | ECHO     |       |     |        | $2       |
| 9    | 4   | RETURN   |       |     |        | 1        |
