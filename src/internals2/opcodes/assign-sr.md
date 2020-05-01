ASSIGN\_SR
----------

PHP code
--------

``` php
<?php
/*
 * Shift result by value1 bits to right and store in variable indicated by result
 * opcode number: 29
 */
$a >>= 3;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op         | fetch | ext | return | operands |
|------|-----|------------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN\_SR |       |     |        | !0,3     |
| 7    | 1   | RETURN     |       |     |        | 1        |
