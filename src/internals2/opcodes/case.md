CASE
----

PHP code
--------

``` php
<?php
/*
 * Set result to true if value1 equals value2.  The value2 must be a constant value?
 * opcode number: 48
 */
$i=0;
switch ($i) {
   case 0:
         echo "i=0";
         break;
   case 1:
         echo "i=1";
         break;
   case 2:
         echo "i=2";
         break;
}
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$i

| line | \#  | op     | fetch | ext | return | operands  |
|------|-----|--------|-------|-----|--------|-----------|
| 6    | 0   | ASSIGN |       |     |        | !0,0      |
| 8    | 1   | CASE   |       |     | \~1    | !0,0      |
|      | 2   | JMPZ   |       |     |        | \~1,-\>6  |
| 9    | 3   | ECHO   |       |     |        | 'i%3D0'   |
| 10   | 4   | BRK    |       |     |        | 1         |
| 11   | 5   | JMP    |       |     |        | -\>8      |
|      | 6   | CASE   |       |     | \~1    | !0,1      |
|      | 7   | JMPZ   |       |     |        | \~1,-\>11 |
| 12   | 8   | ECHO   |       |     |        | 'i%3D1'   |
| 13   | 9   | BRK    |       |     |        | 1         |
| 14   | 10  | JMP    |       |     |        | -\>13     |
|      | 11  | CASE   |       |     | \~1    | !0,2      |
|      | 12  | JMPZ   |       |     |        | \~1,-\>16 |
| 15   | 13  | ECHO   |       |     |        | 'i%3D2'   |
| 16   | 14  | BRK    |       |     |        | 1         |
| 17   | 15  | JMP    |       |     |        | -\>16     |
| 18   | 16  | RETURN |       |     |        | 1         |
