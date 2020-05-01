ASSIGN\_DIM
-----------

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 147
 */
$b = 1;
$a[1][2] = $b;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$b, !1=$a

| line | \#  | op                | fetch | ext | return | operands |
|------|-----|-------------------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN            |       |     |        | !0,1     |
| 7    | 1   | FETCH\_DIM\_W     |       |     | $1     | !1,1     |
|      | 2   | ZEND\_ASSIGN\_DIM |       |     |        | $1,2     |
|      | 3   | ZEND\_OP\_DATA    |       |     |        | !0,$3    |
| 8    | 4   | RETURN            |       |     |        | 1        |
