ASSIGN\_SUB
-----------

PHP code
--------

``` php
<?php
/*
 * Subtract value1 from value2 and store in variable indicated by value1
 * opcode number: 24
 */
$a-=3;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op          | fetch | ext | return | operands |
|------|-----|-------------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN\_SUB |       |     |        | !0,3     |
| 7    | 1   | RETURN      |       |     |        | 1        |
