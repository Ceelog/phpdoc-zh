BOOL
----

PHP code
--------

``` php
<?php
/*
 * convert value1 to boolean and store in result??????????
 * opcode number: 52
 */
if (1 || 2 || 1) echo "foo";
//$a = true;
//if($a) echo "foo";
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op        | fetch | ext | return | operands |
|------|-----|-----------|-------|-----|--------|----------|
| 6    | 0   | JMPNZ\_EX |       |     | \~0    | 1,-\>2   |
|      | 1   | BOOL      |       |     | \~0    | 2        |
|      | 2   | JMPNZ\_EX |       |     | \~0    | \~0,-\>4 |
|      | 3   | BOOL      |       |     | \~0    | 1        |
|      | 4   | JMPZ      |       |     |        | \~0,-\>7 |
|      | 5   | ECHO      |       |     |        | 'foo'    |
|      | 6   | JMP       |       |     |        | -\>7     |
| 9    | 7   | RETURN    |       |     |        | 1        |
