ASSIGN\_MOD
-----------

PHP code
--------

``` php
<?php
/*
 * Perform result mod value1 and store in variable indicated by result
 * opcode number: 27
 */
$a %= 3;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op          | fetch | ext | return | operands |
|------|-----|-------------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN\_MOD |       |     |        | !0,3     |
| 7    | 1   | RETURN      |       |     |        | 1        |
