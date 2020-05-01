FE\_FETCH
---------

PHP code
--------

``` php
<?php
/*
 * Fetch an element from iterator.  If no element is available, jump to address.  Followed by OP_DATA?
 * opcode number: 78
 */
$a = array(1,2,3);
foreach($a as $num){
    print $num;
}
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a, !1=$num

| line | \#  | op                  | fetch | ext | return | operands |
|------|-----|---------------------|-------|-----|--------|----------|
| 6    | 0   | INIT\_ARRAY         |       |     | \~0    | 1        |
|      | 1   | ADD\_ARRAY\_ELEMENT |       |     | \~0    | 2        |
|      | 2   | ADD\_ARRAY\_ELEMENT |       |     | \~0    | 3        |
|      | 3   | ASSIGN              |       |     |        | !0,\~0   |
| 7    | 4   | FE\_RESET           |       |     | $2     | !0,-\>11 |
|      | 5   | FE\_FETCH           |       |     | $3     | $2,-\>11 |
|      | 6   | ZEND\_OP\_DATA      |       |     |        |          |
|      | 7   | ASSIGN              |       |     |        | !1,$3    |
| 8    | 8   | PRINT               |       |     | \~5    | !1       |
|      | 9   | FREE                |       |     |        | \~5      |
| 9    | 10  | JMP                 |       |     |        | -\>5     |
|      | 11  | SWITCH\_FREE        |       |     |        | $2       |
| 10   | 12  | RETURN              |       |     |        | 1        |
