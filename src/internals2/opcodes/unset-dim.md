UNSET\_DIM
----------

PHP code
--------

``` php
<?php
/*
 * Unset the entry of array-value, which is specified by index, and store the original element value into "result".
 * opcode number: 75
 */
$a = array(1,2,3);
unset($a[0]);
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op                  | fetch | ext | return | operands |
|------|-----|---------------------|-------|-----|--------|----------|
| 6    | 0   | INIT\_ARRAY         |       |     | \~0    | 1        |
|      | 1   | ADD\_ARRAY\_ELEMENT |       |     | \~0    | 2        |
|      | 2   | ADD\_ARRAY\_ELEMENT |       |     | \~0    | 3        |
|      | 3   | ASSIGN              |       |     |        | !0,\~0   |
| 7    | 4   | UNSET\_DIM          |       |     | $2     | !0,0     |
| 8    | 5   | RETURN              |       |     |        | 1        |
