FETCH\_OBJ\_W
-------------

PHP code
--------

``` php
<?php
/*
 * Fetch an object from the property of this object and write to the property of the fectched object.
 * opcode number: 85
 */
$foo = new stdclass;
$foo->bar = new stdclass;
$foo->bar->baz = 'quix';
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0 = $foo

| line | \#  | op                  | fetch | ext | return | operands   |
|------|-----|---------------------|-------|-----|--------|------------|
| 6    | 0   | ZEND\_FETCH\_CLASS  |       | 4   | :0     | 'stdclass' |
|      | 1   | NEW                 |       |     |        | :0         |
|      | 2   | DO\_FCALL\_BY\_NAME |       | 0   |        |            |
|      | 3   | ASSIGN              |       |     |        | !0         |
| 7    | 4   | ZEND\_FETCH\_CLASS  |       | 4   | :5     | 'stdclass' |
|      | 5   | NEW                 |       |     |        | :5         |
|      | 6   | DO\_FCALL\_BY\_NAME |       | 0   |        |            |
|      | 7   | ZEND\_ASSIGN\_OBJ   |       |     |        | !0, 'bar'  |
|      | 8   | ZEND\_OP\_DATA      |       |     |        |            |
| 8    | 9   | FETCH\_OBJ\_W       |       |     |        | !0, 'bar'  |
|      | 10  | ZEND\_ASSIGN\_OBJ   |       |     |        | 'baz'      |
|      | 11  | ZEND\_OP\_DATA      |       |     |        | 'quix'     |
| 9    | 12  | RETURN              |       |     |        | 1          |
