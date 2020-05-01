PRE\_INC\_OBJ
-------------

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 132
 */
$obj = new A();
++$obj->num;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$obj

| line | \#  | op                  | fetch | ext | return | operands |
|------|-----|---------------------|-------|-----|--------|----------|
| 6    | 0   | ZEND\_FETCH\_CLASS  |       |     | :0     | 'A'      |
|      | 1   | NEW                 |       |     | $1     | :0       |
|      | 2   | DO\_FCALL\_BY\_NAME |       | 0   |        |          |
|      | 3   | ASSIGN              |       |     |        | !0,$1    |
| 7    | 4   | ZEND\_PRE\_INC\_OBJ |       |     |        | !0,'num' |
| 8    | 5   | RETURN              |       |     |        | 1        |
