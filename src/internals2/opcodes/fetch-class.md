FETCH\_CLASS
------------

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 109
 */
$obj = new A();
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
| 7    | 4   | RETURN              |       |     |        | 1        |
