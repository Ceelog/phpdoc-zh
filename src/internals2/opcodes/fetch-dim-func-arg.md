FETCH\_DIM\_FUNC\_ARG
---------------------

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 93
 */

function foo(&$x)
{
  print($x);
}

$x = array(0, 1, 2, 3, 4, 5);
$z = "foo";

$z($x[0]);

?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$x, !1=$z

| line | \#  | op                    | fetch | ext | return | operands |
|------|-----|-----------------------|-------|-----|--------|----------|
| 7    | 0   | NOP                   |       |     |        |          |
| 12   | 1   | INIT\_ARRAY           |       |     | \~0    | 0        |
|      | 2   | ADD\_ARRAY\_ELEMENT   |       |     | \~0    | 1        |
|      | 3   | ADD\_ARRAY\_ELEMENT   |       |     | \~0    | 2        |
|      | 4   | ADD\_ARRAY\_ELEMENT   |       |     | \~0    | 3        |
|      | 5   | ADD\_ARRAY\_ELEMENT   |       |     | \~0    | 4        |
|      | 6   | ADD\_ARRAY\_ELEMENT   |       |     | \~0    | 5        |
|      | 7   | ASSIGN                |       |     |        | !0,\~0   |
| 13   | 8   | ASSIGN                |       |     |        | !1,'foo' |
| 15   | 9   | INIT\_FCALL\_BY\_NAME |       |     |        | !1       |
|      | 10  | FETCH\_DIM\_FUNC\_ARG |       |     | $3     | !0,0     |
|      | 11  | SEND\_VAR             |       |     |        | $3       |
|      | 12  | DO\_FCALL\_BY\_NAME   |       | 1   |        |          |
| 17   | 13  | RETURN                |       |     |        | 1        |

Function name: foo

Compiled variables: !0=$x

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 7    | 0   | RECV   |       |     |        | 1        |
| 9    | 1   | PRINT  |       |     | \~0    | !0       |
|      | 2   | FREE   |       |     |        | \~0      |
| 10   | 3   | RETURN |       |     |        | null     |
