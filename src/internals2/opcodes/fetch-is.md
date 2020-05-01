FETCH\_IS
---------

PHP code
--------

``` php
<?php
/*
 * Fetch the value from variable which is to be used to test if it is set or not, through isset()/isempty().
 * opcode number: 89
 */
echo isset($_SESSION['userid']);
echo isset($_SESSION['userid'][1]);
echo isset($_SESSION->prop->prop);
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op                              | fetch | ext | return | operands    |
|------|-----|---------------------------------|-------|-----|--------|-------------|
| 6    | 0   | FETCH\_IS                       |       |     | $0     | '\_SESSION' |
|      | 1   | ZEND\_ISSET\_ISEMPTY\_DIM\_OBJ  |       | 1   | \~1    | $0,'userid' |
|      | 2   | ECHO                            |       |     |        | \~1         |
| 7    | 3   | FETCH\_IS                       |       |     | $2     | '\_SESSION' |
|      | 4   | FETCH\_DIM\_IS                  |       |     | $3     | $2,'userid' |
|      | 5   | ZEND\_ISSET\_ISEMPTY\_DIM\_OBJ  |       | 1   | \~4    | $3,1        |
|      | 6   | ECHO                            |       |     |        | \~4         |
| 8    | 7   | FETCH\_IS                       |       |     | $5     | '\_SESSION' |
|      | 8   | FETCH\_OBJ\_IS                  |       |     | $6     | $5,'prop'   |
|      | 9   | ZEND\_ISSET\_ISEMPTY\_PROP\_OBJ |       |     | \~7    | $6,'prop'   |
|      | 10  | ECHO                            |       |     |        | \~7         |
| 9    | 11  | RETURN                          |       |     |        | 1           |
