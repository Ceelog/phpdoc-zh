ASSIGN\_BW\_OR
--------------

PHP code
--------

``` php
<?php
/*
 * Performs binary OR on result and value1 and stores in variable indicated by result.
 * opcode number: 31
 */
$a |= 64;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op             | fetch | ext | return | operands |
|------|-----|----------------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN\_BW\_OR |       |     |        | !0,64    |
| 7    | 1   | RETURN         |       |     |        | 1        |
