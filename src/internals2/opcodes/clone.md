CLONE
-----

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 110
 */
$obj = new A();
$copy = clone $obj;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$obj, !1=$copy

| line | \#  | op                  | fetch | ext | return | operands |
|------|-----|---------------------|-------|-----|--------|----------|
| 6    | 0   | ZEND\_FETCH\_CLASS  |       |     | :0     | 'A'      |
|      | 1   | NEW                 |       |     | $1     | :0       |
|      | 2   | DO\_FCALL\_BY\_NAME |       | 0   |        |          |
|      | 3   | ASSIGN              |       |     |        | !0,$1    |
| 7    | 4   | ZEND\_CLONE         |       |     | $4     | !0       |
|      | 5   | ASSIGN              |       |     |        | !1,$4    |
| 8    | 6   | RETURN              |       |     |        | 1        |
