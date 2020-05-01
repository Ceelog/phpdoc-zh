PRE\_INC
--------

PHP code
--------

``` php
<?php
/*
 * increments variable indicated by value1 by 1 (before performing other operations) and stores in result
 * opcode number: 34
 */
++$a;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op       | fetch | ext | return | operands |
|------|-----|----------|-------|-----|--------|----------|
| 6    | 0   | PRE\_INC |       |     |        | !0       |
| 7    | 1   | RETURN   |       |     |        | 1        |
