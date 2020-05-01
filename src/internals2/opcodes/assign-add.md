ASSIGN\_ADD
-----------

PHP code
--------

``` php
<?php
/*
 * Add value1 to value2 and store in variable indicated by value1
 * opcode number: 23
 */
$a+=3;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op          | fetch | ext | return | operands |
|------|-----|-------------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN\_ADD |       |     |        | !0,3     |
| 7    | 1   | RETURN      |       |     |        | 1        |
