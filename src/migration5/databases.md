数据库
------

关于数据库（MySQL 和 SQLite）在 PHP 5 中有些改变。

因为授权和维护问题，PHP 5 中不再*默认*绑定 MySQL 客户端连接库。
本质上讲， PHP 的
<a href="/configuration.html" class="link">configure</a> 不再包含
**--with-mysql** 选项， 所以需要在编译 PHP 的时候自己手动加上选项。
Windows 用户需要编辑 `php.ini` 开启 PHP 4 中不存在的 `php_mysql.dll` DLL
文件，因为之前内置于 PHP 二进制文件中。

有个新扩展库
<a href="/set/mysqlinfo.html#别名和过时的%20Mysqli%20函数" class="link">MySQLi（改良版 MySQL）</a>，设计用来工作于
MySQL 4.1 及更高版本之下。

自 PHP 5
起，<a href="/book/sqlite.html#SQLite%20函数" class="link">SQLite</a>
扩展库内置在 PHP 中。SQLite 是一个可嵌入 SQL
数据库引擎，不是客户端连接库用来连接大型数据库服务器（如 MySQL 或
PostgreSQL）的。SQLite 库直接读写磁盘上的数据库文件。
