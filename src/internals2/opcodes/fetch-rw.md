FETCH\_RW
---------

PHP code
--------

``` php
<?php
/*
 * Fetch the value of the varible of "name" to assign it to a variable?
 * opcode number: 86
 */
$x = 1;
$a = 'x';
$$a++;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$x, !1=$a

| line | \#  | op        | fetch | ext | return | operands |
|------|-----|-----------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN    |       |     |        | !0,1     |
| 7    | 1   | ASSIGN    |       |     |        | !1,'x'   |
| 8    | 2   | FETCH\_RW | local |     | $2     | !1       |
|      | 3   | POST\_INC |       |     | \~3    | $2       |
|      | 4   | FREE      |       |     |        | \~3      |
| 9    | 5   | RETURN    |       |     |        | 1        |
