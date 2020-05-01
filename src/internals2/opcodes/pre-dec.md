PRE\_DEC
--------

PHP code
--------

``` php
<?php
/*
 * decrements variable indicated by value1 by 1 (before performing other operations) and stores in results
 * opcode number: 35
 */
--$a;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op       | fetch | ext | return | operands |
|------|-----|----------|-------|-----|--------|----------|
| 6    | 0   | PRE\_DEC |       |     |        | !0       |
| 7    | 1   | RETURN   |       |     |        | 1        |
