ASSIGN\_CONCAT
--------------

PHP code
--------

``` php
<?php
/*
 * Concats string values result and value1 and store in variable indicated by result
 * opcode number: 30
 */
$a .= 'z';
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op             | fetch | ext | return | operands |
|------|-----|----------------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN\_CONCAT |       |     |        | !0,'z'   |
| 7    | 1   | RETURN         |       |     |        | 1        |
