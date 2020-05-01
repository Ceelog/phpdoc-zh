More Details
============

**目录**

-   [Functions and Statements which will spread the tainted mark of a
    tainted
    string](/taint/detail.html#Functions%20and%20Statements%20which%20will%20spread%20the%20tainted%20mark%20of%20a%0A%20%20%20tainted%20string)
-   [Functions and statements which will check tainted
    string](/taint/detail.html#Functions%20and%20statements%20which%20will%20check%20tainted%20string)
-   [Functions which untaint the tainted
    string](/taint/detail.html#Functions%20which%20untaint%20the%20tainted%20string)

Functions and Statements which will spread the tainted mark of a tainted string
-------------------------------------------------------------------------------

| Function/Statement               | Since |
|----------------------------------|-------|
| = (assign)                       | 0.1.0 |
| . (concat)                       | 0.1.0 |
| "{$var}" (variable substitution) | 0.1.0 |
| .= (assign concat)               | 0.1.0 |
| strval                           | 0.3.0 |
| explode/split                    | 0.3.0 |
| implode/join                     | 0.3.0 |
| sprintf                          | 0.3.0 |
| vsprintf                         | 0.3.0 |
| trim                             | 0.4.0 |
| rtrim                            | 0.4.0 |
| ltrim                            | 0.4.0 |
| strstr                           | 0.5.0 |
| str\_pad                         | 0.5.0 |
| str\_replace                     | 0.5.0 |
| substr                           | 0.5.0 |
| strtolower                       | 0.5.0 |
| strtoupper                       | 0.5.0 |

Functions and statements which will check tainted string
--------------------------------------------------------

Function/Statement

Since

Basic statments

eval

0.1.0

include/include\_once

0.1.0

require/require\_once

0.1.0

Outputing Functions

echo

0.1.0

print

0.1.0

printf

0.1.0

file\_put\_contents

0.1.0

File System Functions

fopen

0.2.0

opendir

0.2.0

basename

0.2.0

dirname

0.2.0

file

0.2.0

pathinfo

0.2.0

Database relevant Functions

mysql\_query

0.2.0

mysqli\_query/MySQLi::query

0.2.0

sqlite\_query/SqliteDataBase::query

0.3.0

sqlite\_single\_query/SqliteDataBase::singleQuery

0.3.0

oci\_parse

0.3.0

PDO::query

0.3.0

PDO::prepare

0.3.0

SQLite3::query

2.0.1

SQLite3::prepare

2.0.1

Command Line relevant Functions

system

0.1.0

exec

0.1.0

proc\_open

0.1.0

passthru

0.1.0

shell\_exec

0.3.0

Functions which untaint the tainted string
------------------------------------------

| Function                                                  | Since |
|-----------------------------------------------------------|-------|
| addslashes                                                | 0.1.0 |
| addcslashes                                               | 0.1.0 |
| htmlspecialchars                                          | 0.1.0 |
| htmlentities                                              | 0.1.0 |
| escapeshellcmd                                            | 0.1.0 |
| mysql\_escape\_string                                     | 0.1.0 |
| mysql\_real\_escape\_string                               | 0.1.0 |
| mysqli\_escape\_string/MySQLi::escape\_string             | 0.1.0 |
| mysqli\_real\_escape\_string/MySQLi::real\_escape\_string | 0.1.0 |
| sqlite\_escape\_string/SqliteDataBase::escapeString       | 0.3.0 |
| PDO::quote                                                | 0.3.0 |
