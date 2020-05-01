THROW
-----

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 108
 */
try {
    $error = 'Always throw this error';
    throw new Exception($error);

    // Code following an exception is not executed.
    echo 'Never executed';

} catch (Exception $e) {
    echo 'Caught exception: ',  $e->getMessage(), "\n";
}

// Continue execution
echo 'Hello World';
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$error, !1=$e

| line | \#  | op                       | fetch | ext | return | operands                     |
|------|-----|--------------------------|-------|-----|--------|------------------------------|
| 7    | 0   | ASSIGN                   |       |     |        | !0,'Always+throw+this+error' |
| 8    | 1   | ZEND\_FETCH\_CLASS       |       |     | :1     | 'Exception'                  |
|      | 2   | NEW                      |       |     | $2     | :1                           |
|      | 3   | SEND\_VAR                |       |     |        | !0                           |
|      | 4   | DO\_FCALL\_BY\_NAME      |       | 1   |        |                              |
|      | 5   | ZEND\_THROW              |       | 0   |        | $2                           |
| 11   | 6   | ECHO                     |       |     |        | 'Never+executed'             |
| 13   | 7   | JMP                      |       |     |        | -\>15                        |
|      | 8   | ZEND\_FETCH\_CLASS       |       |     | :4     | 'Exception'                  |
|      | 9   | ZEND\_CATCH              |       | 15  |        | $4,!1                        |
| 14   | 10  | ECHO                     |       |     |        | 'Caught+exception%3A+'       |
|      | 11  | ZEND\_INIT\_METHOD\_CALL |       |     |        | !1,'getMessage'              |
|      | 12  | DO\_FCALL\_BY\_NAME      |       | 0   |        |                              |
|      | 13  | ECHO                     |       |     |        | $6                           |
|      | 14  | ECHO                     |       |     |        | '%0A'                        |
| 18   | 15  | ECHO                     |       |     |        | 'Hello+World'                |
| 19   | 16  | RETURN                   |       |     |        | 1                            |
