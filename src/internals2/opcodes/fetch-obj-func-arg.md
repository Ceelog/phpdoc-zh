FETCH\_OBJ\_FUNC\_ARG
---------------------

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 94
 */
include './classA.php';

function foo(&$x)
{
  print($x);
}

$z = "foo";

$obj = new A();
print $obj->num;
$z($obj->num);

?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$z, !1=$obj

| line | \#  | op                    | fetch | ext | return | operands                 |
|------|-----|-----------------------|-------|-----|--------|--------------------------|
| 6    | 0   | INCLUDE\_OR\_EVAL     |       |     |        | '.%2FclassA.php',INCLUDE |
| 8    | 1   | NOP                   |       |     |        |                          |
| 13   | 2   | ASSIGN                |       |     |        | !0,'foo'                 |
| 15   | 3   | ZEND\_FETCH\_CLASS    |       |     | :2     | 'A'                      |
|      | 4   | NEW                   |       |     | $3     | :2                       |
|      | 5   | DO\_FCALL\_BY\_NAME   |       | 0   |        |                          |
|      | 6   | ASSIGN                |       |     |        | !1,$3                    |
| 16   | 7   | FETCH\_OBJ\_R         |       |     | $6     | !1,'num'                 |
|      | 8   | PRINT                 |       |     | \~7    | $6                       |
|      | 9   | FREE                  |       |     |        | \~7                      |
| 17   | 10  | INIT\_FCALL\_BY\_NAME |       |     |        | !0                       |
|      | 11  | FETCH\_OBJ\_FUNC\_ARG |       |     | $8     | !1,'num'                 |
|      | 12  | SEND\_VAR             |       |     |        | $8                       |
|      | 13  | DO\_FCALL\_BY\_NAME   |       | 1   |        |                          |
| 19   | 14  | RETURN                |       |     |        | 1                        |

Function name: foo

Compiled variables: !0=$x

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 8    | 0   | RECV   |       |     |        | 1        |
| 10   | 1   | PRINT  |       |     | \~0    | !0       |
|      | 2   | FREE   |       |     |        | \~0      |
| 11   | 3   | RETURN |       |     |        | null     |

Function name: foo

Compiled variables: !0=$x

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 8    | 0   | RECV   |       |     |        | 1        |
| 10   | 1   | PRINT  |       |     | \~0    | !0       |
|      | 2   | FREE   |       |     |        | \~0      |
| 11   | 3   | RETURN |       |     |        | null     |
