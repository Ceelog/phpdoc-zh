FETCH\_DIM\_TMP\_VAR
--------------------

PHP code
--------

``` php
<?php
/*
 * Fetch an entry of an array from a temporal variable?
 * opcode number: 98
 */
list($x) = array("X");
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$x

| line | \#  | op                   | fetch | ext | return | operands |
|------|-----|----------------------|-------|-----|--------|----------|
| 6    | 0   | INIT\_ARRAY          |       |     | \~0    | 'X'      |
|      | 1   | FETCH\_DIM\_TMP\_VAR |       |     | $1     | \~0,0    |
|      | 2   | ASSIGN               |       |     |        | !0,$1    |
|      | 3   | FREE                 |       |     |        | \~0      |
| 7    | 4   | RETURN               |       |     |        | 1        |
