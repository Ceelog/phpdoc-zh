ASSIGN
------

PHP code
--------

``` php
<?php
/*
 * assigns value1 to result
 * opcode number: 38
 */
$a=1;
$a='a';
$a=new A();
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op                  | fetch | ext | return | operands |
|------|-----|---------------------|-------|-----|--------|----------|
| 6    | 0   | ASSIGN              |       |     |        | !0,1     |
| 7    | 1   | ASSIGN              |       |     |        | !0,'a'   |
| 8    | 2   | ZEND\_FETCH\_CLASS  |       |     | :2     | 'A'      |
|      | 3   | NEW                 |       |     | $3     | :2       |
|      | 4   | DO\_FCALL\_BY\_NAME |       | 0   |        |          |
|      | 5   | ASSIGN              |       |     |        | !0,$3    |
| 9    | 6   | RETURN              |       |     |        | 1        |
