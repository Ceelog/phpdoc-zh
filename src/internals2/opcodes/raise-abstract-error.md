RAISE\_ABSTRACT\_ERROR
----------------------

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 142
 */

abstract class fail {
    abstract function show();
}

class pass extends fail {
    function show() {
        echo "Call to function show()\n";
    }
}

$t2 = new pass();
$t2->show();

$t = new fail();
$t->show();

echo "Done\n"; // shouldn't be displayed
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$t2, !1=$t

| line | \#  | op                       | fetch | ext | return | operands  |
|------|-----|--------------------------|-------|-----|--------|-----------|
| 7    | 0   | NOP                      |       |     |        |           |
| 11   | 1   | NOP                      |       |     |        |           |
|      | 2   | NOP                      |       |     |        |           |
| 17   | 3   | ZEND\_FETCH\_CLASS       |       |     | :3     | 'pass'    |
|      | 4   | NEW                      |       |     | $4     | :3        |
|      | 5   | DO\_FCALL\_BY\_NAME      |       | 0   |        |           |
|      | 6   | ASSIGN                   |       |     |        | !0,$4     |
| 18   | 7   | ZEND\_INIT\_METHOD\_CALL |       |     |        | !0,'show' |
|      | 8   | DO\_FCALL\_BY\_NAME      |       | 0   |        |           |
| 20   | 9   | ZEND\_FETCH\_CLASS       |       |     | :9     | 'fail'    |
|      | 10  | NEW                      |       |     | $10    | :9        |
|      | 11  | DO\_FCALL\_BY\_NAME      |       | 0   |        |           |
|      | 12  | ASSIGN                   |       |     |        | !1,$10    |
| 21   | 13  | ZEND\_INIT\_METHOD\_CALL |       |     |        | !1,'show' |
|      | 14  | DO\_FCALL\_BY\_NAME      |       | 0   |        |           |
| 23   | 15  | ECHO                     |       |     |        | 'Done%0A' |
| 24   | 16  | RETURN                   |       |     |        | 1         |

Function name: show

Compiled variables: none

| line | \#  | op                           | fetch | ext | return | operands |
|------|-----|------------------------------|-------|-----|--------|----------|
| 8    | 0   | ZEND\_RAISE\_ABSTRACT\_ERROR |       |     |        |          |
|      | 1   | RETURN                       |       |     |        | null     |

Function name: show

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands                         |
|------|-----|--------|-------|-----|--------|----------------------------------|
| 13   | 0   | ECHO   |       |     |        | 'Call+to+function+show%28%29%0A' |
| 14   | 1   | RETURN |       |     |        | null                             |
