QM\_ASSIGN
----------

PHP code
--------

``` php
<?php
/*
 * Question Mark Assign, used twice inside a question mark assign to temporarily assign result as value1  (this is followed up with an ASSIGN bytecode)
 * opcode number: 22
 */
function A(){
 echo 1?2:3;
}

function B(){
 $b = 0;
 $a = $b > 1 ? 10: 11;
}
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | NOP    |       |     |        |          |
| 10   | 1   | NOP    |       |     |        |          |
| 14   | 2   | RETURN |       |     |        | 1        |

Function name: A

Compiled variables: none

| line | \#  | op         | fetch | ext | return | operands |
|------|-----|------------|-------|-----|--------|----------|
| 7    | 0   | JMPZ       |       |     |        | 1,-\>3   |
|      | 1   | QM\_ASSIGN |       |     | \~0    | 2        |
|      | 2   | JMP        |       |     |        | -\>4     |
|      | 3   | QM\_ASSIGN |       |     | \~0    | 3        |
|      | 4   | ECHO       |       |     |        | \~0      |
| 8    | 5   | RETURN     |       |     |        | null     |

Function name: B

Compiled variables: !0=$b, !1=$a

| line | \#  | op          | fetch | ext | return | operands |
|------|-----|-------------|-------|-----|--------|----------|
| 11   | 0   | ASSIGN      |       |     |        | !0,0     |
| 12   | 1   | IS\_SMALLER |       |     | \~1    | 1,!0     |
|      | 2   | JMPZ        |       |     |        | \~1,-\>5 |
|      | 3   | QM\_ASSIGN  |       |     | \~2    | 10       |
|      | 4   | JMP         |       |     |        | -\>6     |
|      | 5   | QM\_ASSIGN  |       |     | \~2    | 11       |
|      | 6   | ASSIGN      |       |     |        | !1,\~2   |
| 13   | 7   | RETURN      |       |     |        | null     |
