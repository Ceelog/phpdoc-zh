ISSET\_ISEMPTY\_VAR
-------------------

PHP code
--------

``` php
<?php
/*
 * Tests if the value of a variable is set or not.
 * opcode number: 114
 */
if(isset($a)){ return 0;}
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op                        | fetch | ext | return | operands |
|------|-----|---------------------------|-------|-----|--------|----------|
| 6    | 0   | ZEND\_ISSET\_ISEMPTY\_VAR |       | 5   | \~0    | !0       |
|      | 1   | JMPZ                      |       |     |        | \~0,-\>4 |
|      | 2   | RETURN                    |       |     |        | 0        |
|      | 3   | JMP                       |       |     |        | -\>4     |
| 7    | 4   | RETURN                    |       |     |        | 1        |
