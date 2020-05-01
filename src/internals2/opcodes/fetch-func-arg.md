FETCH\_FUNC\_ARG
----------------

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 92
 */
function foo($x)
{
}

$x = 1;
$y = "x";
$z = "foo";

$z($$y);

?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$x, !1=$y, !2=$z

| line | \#  | op                    | fetch | ext | return | operands |
|------|-----|-----------------------|-------|-----|--------|----------|
| 6    | 0   | NOP                   |       |     |        |          |
| 10   | 1   | ASSIGN                |       |     |        | !0,1     |
| 11   | 2   | ASSIGN                |       |     |        | !1,'x'   |
| 12   | 3   | ASSIGN                |       |     |        | !2,'foo' |
| 14   | 4   | INIT\_FCALL\_BY\_NAME |       |     |        | !2       |
|      | 5   | FETCH\_FUNC\_ARG      | local |     | $3     | !1       |
|      | 6   | SEND\_VAR             |       |     |        | $3       |
|      | 7   | DO\_FCALL\_BY\_NAME   |       | 1   |        |          |
| 16   | 8   | RETURN                |       |     |        | 1        |

Function name: foo

Compiled variables: !0=$x

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | RECV   |       |     |        | 1        |
| 8    | 1   | RETURN |       |     |        | null     |
