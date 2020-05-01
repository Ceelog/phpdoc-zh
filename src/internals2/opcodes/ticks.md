TICKS
-----

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 105
 */
// A function that records the time when it is called
function profile()
{
   echo "profile function is called\n";
}

// Set up a tick handler
register_tick_function("profile");

// Initialize the function before the declare block
profile();

// Run a block of code, throw a tick every 2nd statement
declare(ticks=2) {
   for ($x = 0; $x < 10; ++$x) {
         echo "hello world\n";
   }
}
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$x

| line | \#  | op          | fetch | ext | return | operands                   |
|------|-----|-------------|-------|-----|--------|----------------------------|
| 7    | 0   | NOP         |       |     |        |                            |
| 13   | 1   | SEND\_VAL   |       |     |        | 'profile'                  |
|      | 2   | DO\_FCALL   |       | 1   |        | 'register\_tick\_function' |
| 16   | 3   | DO\_FCALL   |       | 0   |        | 'profile'                  |
| 20   | 4   | ASSIGN      |       |     |        | !0,0                       |
|      | 5   | IS\_SMALLER |       |     | \~3    | !0,10                      |
|      | 6   | JMPZNZ      |       | 9   |        | \~3,-\>13                  |
|      | 7   | PRE\_INC    |       |     |        | !0                         |
|      | 8   | JMP         |       |     |        | -\>5                       |
| 21   | 9   | ECHO        |       |     |        | 'hello+world%0A'           |
|      | 10  | TICKS       |       |     |        | 2                          |
| 22   | 11  | TICKS       |       |     |        | 2                          |
|      | 12  | JMP         |       |     |        | -\>7                       |
|      | 13  | TICKS       |       |     |        | 2                          |
| 23   | 14  | TICKS       |       |     |        | 2                          |
| 24   | 15  | RETURN      |       |     |        | 1                          |

Function name: profile

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands                        |
|------|-----|--------|-------|-----|--------|---------------------------------|
| 9    | 0   | ECHO   |       |     |        | 'profile+function+is+called%0A' |
| 10   | 1   | RETURN |       |     |        | null                            |
