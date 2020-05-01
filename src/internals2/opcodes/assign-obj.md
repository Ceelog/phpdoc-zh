ASSIGN\_OBJ
-----------

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 136
 */
$obj->a = $otherobj;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$obj, !1=$otherobj

| line | \#  | op                | fetch | ext | return | operands |
|------|-----|-------------------|-------|-----|--------|----------|
| 6    | 0   | ZEND\_ASSIGN\_OBJ |       |     |        | !0,'a'   |
|      | 1   | ZEND\_OP\_DATA    |       |     |        | !1       |
| 7    | 2   | RETURN            |       |     |        | 1        |
