IS\_IDENTICAL
-------------

PHP code
--------

``` php
<?php
/*
 * Compares value1 and value2 to see if they are equal AND have the same type
 * opcode number: 15
 */
echo (1===1);
echo (1==='a');
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op            | fetch | ext | return | operands |
|------|-----|---------------|-------|-----|--------|----------|
| 6    | 0   | IS\_IDENTICAL |       |     | \~0    | 1,1      |
|      | 1   | ECHO          |       |     |        | \~0      |
| 7    | 2   | IS\_IDENTICAL |       |     | \~1    | 1,'a'    |
|      | 3   | ECHO          |       |     |        | \~1      |
| 8    | 4   | RETURN        |       |     |        | 1        |
