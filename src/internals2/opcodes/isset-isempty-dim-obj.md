ISSET\_ISEMPTY\_DIM\_OBJ
------------------------

PHP code
--------

``` php
<?php
/*
 * Tests if the entry of an array is set or not.
 * opcode number: 115
 */
if(isset($a[0])) return 0;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op                             | fetch | ext | return | operands |
|------|-----|--------------------------------|-------|-----|--------|----------|
| 6    | 0   | ZEND\_ISSET\_ISEMPTY\_DIM\_OBJ |       | 1   | \~0    | !0,0     |
|      | 1   | JMPZ                           |       |     |        | \~0,-\>4 |
|      | 2   | RETURN                         |       |     |        | 0        |
|      | 3   | JMP                            |       |     |        | -\>4     |
| 7    | 4   | RETURN                         |       |     |        | 1        |
