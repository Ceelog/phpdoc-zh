FETCH\_OBJ\_R
-------------

PHP code
--------

``` php
<?php
/*
 * Fetch the "prop-name" property value of this object.  Read-only?
 * opcode number: 82
 */
$x = new A();
$a = 'x';
echo $$a->num;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$x, !1=$a

| line | \#  | op                  | fetch | ext | return | operands |
|------|-----|---------------------|-------|-----|--------|----------|
| 6    | 0   | ZEND\_FETCH\_CLASS  |       |     | :0     | 'A'      |
|      | 1   | NEW                 |       |     | $1     | :0       |
|      | 2   | DO\_FCALL\_BY\_NAME |       | 0   |        |          |
|      | 3   | ASSIGN              |       |     |        | !0,$1    |
| 7    | 4   | ASSIGN              |       |     |        | !1,'x'   |
| 8    | 5   | FETCH\_R            | local |     | $5     | !1       |
|      | 6   | FETCH\_OBJ\_R       |       |     | $6     | $5,'num' |
|      | 7   | ECHO                |       |     |        | $6       |
| 9    | 8   | RETURN              |       |     |        | 1        |
