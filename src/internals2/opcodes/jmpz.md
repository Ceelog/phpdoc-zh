JMPZ
----

PHP code
--------

``` php
<?php
/*
 * Jump to the address if the value is zero
 * opcode number: 43
 */
if($a != 0) echo "foo";
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op             | fetch | ext | return | operands |
|------|-----|----------------|-------|-----|--------|----------|
| 6    | 0   | IS\_NOT\_EQUAL |       |     | \~0    | !0,0     |
|      | 1   | JMPZ           |       |     |        | \~0,-\>4 |
|      | 2   | ECHO           |       |     |        | 'foo'    |
|      | 3   | JMP            |       |     |        | -\>4     |
| 7    | 4   | RETURN         |       |     |        | 1        |
