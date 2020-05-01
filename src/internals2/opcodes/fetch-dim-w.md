FETCH\_DIM\_W
-------------

PHP code
--------

``` php
<?php
/*
 * Fetch the value of the element at "index" in "array-value" to store it in "result".  Write-only?
 * opcode number: 84
 */
$a = 1;
while($a > 0){
    $a = 0;
}
/*$input =array(1,2,3);
while (list($var,) = @each($input)){
    unset($$var);
}*/
/*$a = array(1,2,3);
$x = 'a';
$$x[0] = 1;*/

/*while ($b = each($a)) {
  print $b;
}*/


?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op          | fetch | ext | return | operands |
|------|-----|-------------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN      |       |     |        | !0,1     |
| 7    | 1   | IS\_SMALLER |       |     | \~1    | 0,!0     |
|      | 2   | JMPZ        |       |     |        | \~1,-\>5 |
| 8    | 3   | ASSIGN      |       |     |        | !0,0     |
| 9    | 4   | JMP         |       |     |        | -\>1     |
| 23   | 5   | RETURN      |       |     |        | 1        |
