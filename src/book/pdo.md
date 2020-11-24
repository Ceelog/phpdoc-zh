PHP 数据对象
============

**目录**

-   [简介](/book/pdo.html#简介)
-   [安装／配置](/book/pdo.html#安装／配置)
    -   [需求](/book/pdo.html#需求)
    -   [安装](/book/pdo.html#安装)
    -   [运行时配置](/book/pdo.html#运行时配置)
    -   [资源类型](/book/pdo.html#资源类型)
-   [预定义常量](/book/pdo.html#预定义常量)
-   [连接与连接管理](/book/pdo.html#连接与连接管理)
-   [事务与自动提交](/book/pdo.html#事务与自动提交)
-   [预处理语句与存储过程](/book/pdo.html#预处理语句与存储过程)
-   [错误与错误处理](/book/pdo.html#错误与错误处理)
-   [大对象 (LOBs)](/book/pdo.html#大对象%20(LOBs))
-   [PDO](/book/pdo.html#PDO) — PDO 类
    -   [PDO::beginTransaction](/book/pdo.html#PDO::beginTransaction) —
        启动一个事务
    -   [PDO::commit](/book/pdo.html#PDO::commit) — 提交一个事务
    -   [PDO::\_\_construct](/book/pdo.html#PDO::__construct) —
        创建一个表示数据库连接的 PDO 实例
    -   [PDO::errorCode](/book/pdo.html#PDO::errorCode) —
        获取跟数据库句柄上一次操作相关的 SQLSTATE
    -   [PDO::errorInfo](/book/pdo.html#PDO::errorInfo) — Fetch extended
        error information associated with the last operation on the
        database handle
    -   [PDO::exec](/book/pdo.html#PDO::exec) — 执行一条 SQL
        语句，并返回受影响的行数
    -   [PDO::getAttribute](/book/pdo.html#PDO::getAttribute) —
        取回一个数据库连接的属性
    -   [PDO::getAvailableDrivers](/book/pdo.html#PDO::getAvailableDrivers)
        — 返回一个可用驱动的数组
    -   [PDO::inTransaction](/book/pdo.html#PDO::inTransaction) —
        检查是否在一个事务内
    -   [PDO::lastInsertId](/book/pdo.html#PDO::lastInsertId) —
        返回最后插入行的ID或序列值
    -   [PDO::prepare](/book/pdo.html#PDO::prepare) —
        准备要执行的语句，并返回语句对象
    -   [PDO::query](/book/pdo.html#PDO::query) — 执行 SQL 语句，以
        PDOStatement 对象形式返回结果集
    -   [PDO::quote](/book/pdo.html#PDO::quote) — 为 SQL
        查询里的字符串添加引号
    -   [PDO::rollBack](/book/pdo.html#PDO::rollBack) — 回滚一个事务
    -   [PDO::setAttribute](/book/pdo.html#PDO::setAttribute) — 设置属性
-   [PDOStatement](/book/pdo.html#PDOStatement) — PDOStatement 类
    -   [PDOStatement::bindColumn](/book/pdo.html#PDOStatement::bindColumn)
        — 绑定一列到一个 PHP 变量
    -   [PDOStatement::bindParam](/book/pdo.html#PDOStatement::bindParam)
        — 绑定一个参数到指定的变量名
    -   [PDOStatement::bindValue](/book/pdo.html#PDOStatement::bindValue)
        — 把一个值绑定到一个参数
    -   [PDOStatement::closeCursor](/book/pdo.html#PDOStatement::closeCursor)
        — 关闭游标，使语句能再次被执行。
    -   [PDOStatement::columnCount](/book/pdo.html#PDOStatement::columnCount)
        — 返回结果集中的列数
    -   [PDOStatement::debugDumpParams](/book/pdo.html#PDOStatement::debugDumpParams)
        — 打印一条 SQL 预处理命令
    -   [PDOStatement::errorCode](/book/pdo.html#PDOStatement::errorCode)
        — 获取跟上一次语句句柄操作相关的 SQLSTATE
    -   [PDOStatement::errorInfo](/book/pdo.html#PDOStatement::errorInfo)
        — 获取跟上一次语句句柄操作相关的扩展错误信息
    -   [PDOStatement::execute](/book/pdo.html#PDOStatement::execute) —
        执行一条预处理语句
    -   [PDOStatement::fetch](/book/pdo.html#PDOStatement::fetch) —
        从结果集中获取下一行
    -   [PDOStatement::fetchAll](/book/pdo.html#PDOStatement::fetchAll)
        — 返回一个包含结果集中所有行的数组
    -   [PDOStatement::fetchColumn](/book/pdo.html#PDOStatement::fetchColumn)
        — 从结果集中的下一行返回单独的一列。
    -   [PDOStatement::fetchObject](/book/pdo.html#PDOStatement::fetchObject)
        — 获取下一行并作为一个对象返回。
    -   [PDOStatement::getAttribute](/book/pdo.html#PDOStatement::getAttribute)
        — 检索一个语句属性
    -   [PDOStatement::getColumnMeta](/book/pdo.html#PDOStatement::getColumnMeta)
        — 返回结果集中一列的元数据
    -   [PDOStatement::nextRowset](/book/pdo.html#PDOStatement::nextRowset)
        — 在一个多行集语句句柄中推进到下一个行集
    -   [PDOStatement::rowCount](/book/pdo.html#PDOStatement::rowCount)
        — 返回受上一个 SQL 语句影响的行数
    -   [PDOStatement::setAttribute](/book/pdo.html#PDOStatement::setAttribute)
        — 设置一个语句属性
    -   [PDOStatement::setFetchMode](/book/pdo.html#PDOStatement::setFetchMode)
        — 为语句设置默认的获取模式。
-   [PDOException](/book/pdo.html#PDOException) — PDOException 异常类
-   [PDO 驱动](/book/pdo.html#PDO%20驱动)
    -   [CUBRID (PDO)](/book/pdo.html#CUBRID%20(PDO)) — CUBRID Functions
        (PDO\_CUBRID)
    -   [MS SQL Server (PDO)](/book/pdo.html#MS%20SQL%20Server%20(PDO))
        — Microsoft SQL Server and Sybase Functions (PDO\_DBLIB)
    -   [Firebird (PDO)](/book/pdo.html#Firebird%20(PDO)) — Firebird
        Functions (PDO\_FIREBIRD)
    -   [IBM (PDO)](/book/pdo.html#IBM%20(PDO)) — IBM Functions
        (PDO\_IBM)
    -   [Informix (PDO)](/book/pdo.html#Informix%20(PDO)) — Informix
        Functions (PDO\_INFORMIX)
    -   [MySQL (PDO)](/book/pdo.html#MySQL%20(PDO)) — MySQL Functions
        (PDO\_MYSQL)
    -   [MS SQL Server (PDO)](/book/pdo.html#MS%20SQL%20Server%20(PDO))
        — Microsoft SQL Server Functions (PDO\_SQLSRV)
    -   [Oracle (PDO)](/book/pdo.html#Oracle%20(PDO)) — Oracle Functions
        (PDO\_OCI)
    -   [ODBC and DB2 (PDO)](/book/pdo.html#ODBC%20and%20DB2%20(PDO)) —
        ODBC and DB2 Functions (PDO\_ODBC)
    -   [PostgreSQL (PDO)](/book/pdo.html#PostgreSQL%20(PDO)) —
        PostgreSQL Functions (PDO\_PGSQL)
    -   [SQLite (PDO)](/book/pdo.html#SQLite%20(PDO)) — SQLite Functions
        (PDO\_SQLITE)

*PHP 数据对象* （PDO）
扩展为PHP访问数据库定义了一个轻量级的一致接口。实现 PDO
接口的每个数据库驱动可以公开具体数据库的特性作为标准扩展功能。 注意利用
PDO 扩展自身并不能实现任何数据库功能；必须使用一个
<a href="/book/pdo.html#PDO%20驱动" class="link">具体数据库的 PDO 驱动</a>
来访问数据库服务。

PDO 提供了一个 *数据访问*
抽象层，这意味着，不管使用哪种数据库，都可以用相同的函数（方法）来查询和获取数据。
PDO *不*提供 *数据库* 抽象层；它不会重写
SQL，也不会模拟缺失的特性。如果需要的话，应该使用一个成熟的抽象层。

从 PHP 5.1 开始附带了 PDO，在 PHP 5.0 中是作为一个 PECL 扩展使用。 PDO
需要PHP 5 核心的新 OO 特性，因此不能在较早版本的 PHP 上运行。

安装／配置
==========

**目录**

-   [需求](/book/pdo.html#需求)
-   [安装](/book/pdo.html#安装)
-   [运行时配置](/book/pdo.html#运行时配置)
-   [资源类型](/book/pdo.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

**在 Unix 系统上安装 PDO**

1.  自 PHP 5.1.0 起，PDO 和
    <a href="/book/pdo.html#SQLite%20(PDO)" class="link">PDO_SQLITE</a>
    驱动默认可用。对于自己选择的数据库，需要启用相应的 POD 驱动； 查阅
    <a href="/book/pdo.html#PDO%20驱动" class="link">特定数据库的 PDO 驱动</a>
    文档获取更多此内容。

    > **Note**:
    >
    > 当以共享扩展（*不推荐*）构建 PDO 时，所有 PDO 驱动 *必须* 在 PDO
    > 自身 *之后* 加载。

2.  当作为一个共享模块安装 PDO 时，需要更新 php.ini 文件以便当 PHP
    运行时 PDO
    扩展能被自动加载。还需要在那里启用具体的数据库驱动；确保它们被列在
    pdo.so 那一行之后，因为 PDO 必须在具体的
    数据库扩展被载入前初始化。如果静态地构建 PDO 和
    具体数据库扩展，可以跳过此步。

        extension=pdo.so

**Windows 用户**

1.  PDO 和所有主要的驱动作为共享扩展随 PHP
    一起发布，要激活它们只需简单地编辑 `php.ini` 文件：

        extension=php_pdo.dll

    > **Note**:
    >
    > 这一步在 PHP 5.3及更高版本中不是必须的，对于 PDO 不再需要做为一个
    > DLL 文件。

2.  下一步，选择其他具体数据库的 DLL 文件，然后要么在运行时用 <span
    class="function">dl</span> 载入，要么在 `php.ini` 中的 `php_pdo.dll`
    后面启用。例如：

        extension=php_pdo.dll
        extension=php_pdo_firebird.dll
        extension=php_pdo_informix.dll
        extension=php_pdo_mssql.dll
        extension=php_pdo_mysql.dll
        extension=php_pdo_oci.dll
        extension=php_pdo_oci8.dll
        extension=php_pdo_odbc.dll
        extension=php_pdo_pgsql.dll
        extension=php_pdo_sqlite.dll  

    那些 DLL
    文件应该在系统的<a href="/ini/core.html#ini.extension-dir" class="link">extension_dir</a>
    中存在。

> **Note**:
>
> 记住：更改 `php.ini` 文件后需要重启 PHP 服务才能使新的配置指令生效。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                 | 默认 | 可修改范围   | 更新日志 |
|------------------------------------------------------|------|--------------|----------|
| <a href="/book/pdo.html#" class="link">pdo.dsn.*</a> |      | 仅 `php.ini` |          |

这是配置指令的简短说明。

`pdo.dsn.*` <span class="type">string</span>  
定义 DSN 别名。 参见 <span class="function">PDO::\_\_construct</span>
详细说明。

资源类型
--------

此扩展没有定义资源类型。

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**Warning**

自 PHP 5.1 起，开始使用类常量。以前的版本使用类似 **`PDO_PARAM_BOOL`**
这样的全局常量。

**`PDO::PARAM_BOOL`** (<span class="type">integer</span>)  
<span class="simpara"> 表示布尔数据类型。 </span>

**`PDO::PARAM_NULL`** (<span class="type">integer</span>)  
<span class="simpara"> 表示 SQL 中的 NULL 数据类型。 </span>

**`PDO::PARAM_INT`** (<span class="type">integer</span>)  
<span class="simpara"> 表示 SQL 中的整型。 </span>

**`PDO::PARAM_STR`** (<span class="type">integer</span>)  
<span class="simpara"> 表示 SQL 中的 CHAR、VARCHAR 或其他字符串类型。
</span>

**`PDO::PARAM_STR_NATL`** (<span class="type">integer</span>)  
<span class="simpara"> 标记了字符使用的是国家字符集（national character
set）。 </span> <span class="simpara"> 自 PHP 7.2.0 起。 </span>

**`PDO::PARAM_STR_CHAR`** (<span class="type">integer</span>)  
<span class="simpara"> 标记了字符使用的是常规字符集（regular character
set）。 </span> <span class="simpara"> 自 PHP 7.2.0 起。 </span>

**`PDO::PARAM_LOB`** (<span class="type">integer</span>)  
<span class="simpara"> 表示 SQL 中大对象数据类型。 </span>

**`PDO::PARAM_STMT`** (<span class="type">integer</span>)  
<span class="simpara"> 表示一个记录集类型。当前尚未被任何驱动支持。
</span>

**`PDO::PARAM_INPUT_OUTPUT`** (<span class="type">integer</span>)  
<span class="simpara"> 指定参数为一个存储过程的 INOUT
参数。必须用一个明确的 PDO::PARAM\_\* 数据类型跟此值进行按位或。 </span>

**`PDO::FETCH_LAZY`** (<span class="type">integer</span>)  
<span class="simpara">
指定获取方式，将结果集中的每一行作为一个对象返回，此对象的变量名对应着列名。**`PDO::FETCH_LAZY`**
创建用来访问的对象变量名。在 <span
class="function">PDOStatement::fetchAll</span> 中无效。 </span>

**`PDO::FETCH_ASSOC`** (<span class="type">integer</span>)  
<span class="simpara">
指定获取方式，将对应结果集中的每一行作为一个由列名索引的数组返回。如果结果集中包含多个名称相同的列，则**`PDO::FETCH_ASSOC`**每个列名只返回一个值。
</span>

**`PDO::FETCH_NAMED`** (<span class="type">integer</span>)  
<span class="simpara">
指定获取方式，将对应结果集中的每一行作为一个由列名索引的数组返回。如果结果集中包含多个名称相同的列，则**`PDO::FETCH_ASSOC`**每个列名
返回一个包含值的数组。 </span>

**`PDO::FETCH_NUM`** (<span class="type">integer</span>)  
<span class="simpara">
指定获取方式，将对应结果集中的每一行作为一个由列号索引的数组返回，从第 0
列开始。 </span>

**`PDO::FETCH_BOTH`** (<span class="type">integer</span>)  
<span class="simpara">
指定获取方式，将对应结果集中的每一行作为一个由列号和列名索引的数组返回，从第
0 列开始。 </span>

**`PDO::FETCH_OBJ`** (<span class="type">integer</span>)  
<span class="simpara">
指定获取方式，将结果集中的每一行作为一个属性名对应列名的对象返回。
</span>

**`PDO::FETCH_BOUND`** (<span class="type">integer</span>)  
<span class="simpara"> 指定获取方式，返回 TRUE
且将结果集中的列值分配给通过 <span
class="function">PDOStatement::bindParam</span> 或 <span
class="function">PDOStatement::bindColumn</span> 方法绑定的 PHP 变量。
</span>

**`PDO::FETCH_COLUMN`** (<span class="type">integer</span>)  
<span class="simpara">
指定获取方式，从结果集中的下一行返回所需要的那一列。 </span>

**`PDO::FETCH_CLASS`** (<span class="type">integer</span>)  
<span class="simpara">
指定获取方式，返回一个所请求类的新实例，映射列到类中对应的属性名。
</span>

> **Note**: <span class="simpara"> 如果所请求的类中不存在该属性，则调用
> <a href="/language/oop5/overloading.html#language.oop5.overloading.members" class="link"><span class="methodname">__set</span></a>
> 魔术方法 </span>

**`PDO::FETCH_INTO`** (<span class="type">integer</span>)  
<span class="simpara">
指定获取方式，更新一个请求类的现有实例，映射列到类中对应的属性名。
</span>

**`PDO::FETCH_FUNC`** (<span class="type">integer</span>)  
<span class="simpara"> 允许在运行中完全用自定义的方式处理数据。（仅在
<span class="function">PDOStatement::fetchAll</span> 中有效）。 </span>

**`PDO::FETCH_GROUP`** (<span class="type">integer</span>)  
<span class="simpara"> 根据值分组返回。通常和 **`PDO::FETCH_COLUMN`** 或
**`PDO::FETCH_KEY_PAIR`** 一起使用。 </span>

**`PDO::FETCH_UNIQUE`** (<span class="type">integer</span>)  
<span class="simpara"> 只取唯一值。 </span>

**`PDO::FETCH_KEY_PAIR`** (<span class="type">integer</span>)  
<span class="simpara">
获取一个有两列的结果集到一个数组，其中第一列为键名，第二列为值。自 PHP
5.2.3 起可用。 </span>

**`PDO::FETCH_CLASSTYPE`** (<span class="type">integer</span>)  
<span class="simpara"> 根据第一列的值确定类名。 </span>

**`PDO::FETCH_SERIALIZE`** (<span class="type">integer</span>)  
<span class="simpara"> 类似 **`PDO::FETCH_INTO`**
，但是以一个序列化的字符串表示对象。自 PHP 5.1.0 起可用。从 PHP 5.3.0
开始，如果设置此标志，则类的构造函数从不会被调用。 </span>

**`PDO::FETCH_PROPS_LATE`** (<span class="type">integer</span>)  
<span class="simpara"> 设置属性前调用构造函数。自 PHP 5.2.0 起可用。
</span>

**`PDO::ATTR_AUTOCOMMIT`** (<span class="type">integer</span>)  
<span class="simpara"> 如果此值为 **`FALSE`** ，PDO
将试图禁用自动提交以便数据库连接开始一个事务。 </span>

**`PDO::ATTR_PREFETCH`** (<span class="type">integer</span>)  
<span class="simpara">
设置预取大小来为你的应用平衡速度和内存使用。并非所有的数据库/驱动组合都支持设置预取大小。较大的预取大小导致性能提高的同时也会占用更多的内存。
</span>

**`PDO::ATTR_TIMEOUT`** (<span class="type">integer</span>)  
<span class="simpara"> 设置连接数据库的超时秒数。 </span>

**`PDO::ATTR_ERRMODE`** (<span class="type">integer</span>)  
<span class="simpara"> 关于此属性的更多信息请参见
<a href="/book/pdo.html#错误与错误处理" class="link">错误及错误处理</a>
部分。 </span>

**`PDO::ATTR_SERVER_VERSION`** (<span class="type">integer</span>)  
<span class="simpara"> 此为只读属性；返回 PDO
所连接的数据库服务的版本信息。 </span>

**`PDO::ATTR_CLIENT_VERSION`** (<span class="type">integer</span>)  
<span class="simpara"> 此为只读属性；返回 PDO
驱动所用客户端库的版本信息。 </span>

**`PDO::ATTR_SERVER_INFO`** (<span class="type">integer</span>)  
<span class="simpara"> 此为只读属性。返回一些关于 PDO
所连接的数据库服务的元信息。 </span>

**`PDO::ATTR_CONNECTION_STATUS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`PDO::ATTR_CASE`** (<span class="type">integer</span>)  
<span class="simpara"> 用类似 *PDO::CASE\_\**
的常量强制列名为指定的大小写。 </span>

**`PDO::ATTR_CURSOR_NAME`** (<span class="type">integer</span>)  
<span class="simpara">
获取或设置使用游标的名称。当使用可滚动游标和定位更新时候非常有用。
</span>

**`PDO::ATTR_CURSOR`** (<span class="type">integer</span>)  
<span class="simpara"> 选择游标类型。 PDO 当前支持
**`PDO::CURSOR_FWDONLY`** 和 **`PDO::CURSOR_SCROLL`**。一般为
**`PDO::CURSOR_FWDONLY`**，除非确实需要一个可滚动游标。 </span>

**`PDO::ATTR_DRIVER_NAME`** (<span class="type">string</span>)  
<span class="simpara"> 返回驱动名称。 </span>

**示例 \#1 使用 **`PDO::ATTR_DRIVER_NAME`** 的例子**

``` php
<?php
if ($db->getAttribute(PDO::ATTR_DRIVER_NAME) == 'mysql') {
  echo "Running on mysql; doing something mysql specific here\n";
}
?>
```

**`PDO::ATTR_ORACLE_NULLS`** (<span class="type">integer</span>)  
<span class="simpara"> 在获取数据时将空字符串转换成 SQL 中的 NULL 。
</span>

**`PDO::ATTR_PERSISTENT`** (<span class="type">integer</span>)  
<span class="simpara">
请求一个持久连接，而非创建一个新连接。关于此属性的更多信息请参见
<a href="/book/pdo.html#连接与连接管理" class="link">连接与连接管理</a>
。 </span>

**`PDO::ATTR_STATEMENT_CLASS`** (<span class="type">integer</span>)  
<span class="simpara"> 设置返回的 statement 类名。 </span>

**`PDO::ATTR_FETCH_CATALOG_NAMES`** (<span class="type">integer</span>)  
<span class="simpara">
将包含的目录名添加到结果集中的每个列名前面。目录名和列名由一个小数点分开（.）。此属性在驱动层面支持，所以有些驱动可能不支持此属性。
</span>

**`PDO::ATTR_FETCH_TABLE_NAMES`** (<span class="type">integer</span>)  
<span class="simpara">
将包含的表名添加到结果集中的每个列名前面。表名和列名由一个小数点分开（.）。此属性在驱动层面支持，所以有些驱动可能不支持此属性。
</span>

**`PDO::ATTR_STRINGIFY_FETCHES`** (<span class="type">integer</span>)  
<span class="simpara"> 强制以字符串方式对待所有的值。 </span>

**`PDO::ATTR_MAX_COLUMN_LEN`** (<span class="type">integer</span>)  
<span class="simpara"> 设置字段名最长的尺寸。 </span>

**`PDO::ATTR_DEFAULT_FETCH_MODE`** (<span class="type">integer</span>)  
<span class="simpara"> 自 PHP 5.2.0 起可用。 </span>

**`PDO::ATTR_EMULATE_PREPARES`** (<span class="type">integer</span>)  
<span class="simpara"> 自 PHP 5.1.3 起可用。 </span>

**`PDO::ATTR_DEFAULT_STR_PARAM`** (<span class="type">integer</span>)  
<span class="simpara"> 设置默认 string 参数类型可以是
**`PDO::PARAM_STR_NATL`** 和 **`PDO::PARAM_STR_CHAR`**。 </span> <span
class="simpara"> 自 PHP 7.2.0 起可用 </span>

**`PDO::ERRMODE_SILENT`** (<span class="type">integer</span>)  
<span class="simpara">
如果发生错误，则不显示错误或异常。希望开发人员显式地检查错误。此为默认模式。关于此属性的更多信息请参见
<a href="/book/pdo.html#错误与错误处理" class="link">错误与错误处理</a>
。 </span>

**`PDO::ERRMODE_WARNING`** (<span class="type">integer</span>)  
<span class="simpara"> 如果发生错误，则显示一个 PHP **`E_WARNING`**
消息。关于此属性的更多信息请参见
<a href="/book/pdo.html#错误与错误处理" class="link">错误与错误处理</a>。
</span>

**`PDO::ERRMODE_EXCEPTION`** (<span class="type">integer</span>)  
<span class="simpara"> 如果发生错误，则抛出一个 <span
class="classname">PDOException</span> 异常。关于此属性的更多信息请参见
<a href="/book/pdo.html#错误与错误处理" class="link">错误与错误处理</a>。
</span>

**`PDO::CASE_NATURAL`** (<span class="type">integer</span>)  
<span class="simpara"> 保留数据库驱动返回的列名。 </span>

**`PDO::CASE_LOWER`** (<span class="type">integer</span>)  
<span class="simpara"> 强制列名小写。 </span>

**`PDO::CASE_UPPER`** (<span class="type">integer</span>)  
<span class="simpara"> 强制列名大写。 </span>

**`PDO::NULL_NATURAL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`PDO::NULL_EMPTY_STRING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`PDO::NULL_TO_STRING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`PDO::FETCH_ORI_NEXT`** (<span class="type">integer</span>)  
<span class="simpara"> 在结果集中获取下一行。仅对可滚动游标有效。
</span>

**`PDO::FETCH_ORI_PRIOR`** (<span class="type">integer</span>)  
<span class="simpara"> 在结果集中获取上一行。仅对可滚动游标有效。
</span>

**`PDO::FETCH_ORI_FIRST`** (<span class="type">integer</span>)  
<span class="simpara"> 在结果集中获取第一行。仅对可滚动游标有效。
</span>

**`PDO::FETCH_ORI_LAST`** (<span class="type">integer</span>)  
<span class="simpara"> 在结果集中获取最后一行。仅对可滚动游标有效。
</span>

**`PDO::FETCH_ORI_ABS`** (<span class="type">integer</span>)  
<span class="simpara">
根据行号从结果集中获取需要的行。仅对可滚动游标有效。 </span>

**`PDO::FETCH_ORI_REL`** (<span class="type">integer</span>)  
<span class="simpara">
根据当前游标位置的相对位置从结果集中获取需要的行。仅对可滚动游标有效。
</span>

**`PDO::CURSOR_FWDONLY`** (<span class="type">integer</span>)  
<span class="simpara"> 创建一个只进游标的 <span
class="classname">PDOStatement</span>
对象。此为默认的游标选项，因为此游标最快且是 PHP
中最常用的数据访问模式。 </span>

**`PDO::CURSOR_SCROLL`** (<span class="type">integer</span>)  
<span class="simpara"> 创建一个可滚动游标的 <span
class="classname">PDOStatement</span> 对象。通过 *PDO::FETCH\_ORI\_\**
常量来控制结果集中获取的行。 </span>

**`PDO::ERR_NONE`** (<span class="type">string</span>)  
<span class="simpara"> 对应 SQLSTATE '00000'，表示 SQL
语句没有错误或警告地成功发出。当用 <span
class="function">PDO::errorCode</span> 或 <span
class="function">PDOStatement::errorCode</span>
来确定是否有错误发生时，此常量非常方便。在检查上述方法返回的错误状态代码时，会经常用到。
</span>

**`PDO::PARAM_EVT_ALLOC`** (<span class="type">integer</span>)  
<span class="simpara"> 分配事件 </span>

**`PDO::PARAM_EVT_FREE`** (<span class="type">integer</span>)  
<span class="simpara"> 解除分配事件 </span>

**`PDO::PARAM_EVT_EXEC_PRE`** (<span class="type">integer</span>)  
<span class="simpara"> 执行一条预处理语句之前触发事件。 </span>

**`PDO::PARAM_EVT_EXEC_POST`** (<span class="type">integer</span>)  
<span class="simpara"> 执行一条预处理语句之后触发事件。 </span>

**`PDO::PARAM_EVT_FETCH_PRE`** (<span class="type">integer</span>)  
<span class="simpara"> 从一个结果集中取出一条结果之前触发事件。 </span>

**`PDO::PARAM_EVT_FETCH_POST`** (<span class="type">integer</span>)  
<span class="simpara"> 从一个结果集中取出一条结果之后触发事件。 </span>

**`PDO::PARAM_EVT_NORMALIZE`** (<span class="type">integer</span>)  
<span class="simpara">
在绑定参数注册允许驱动程序正常化变量名时触发事件。 </span>

**`PDO::SQLITE_DETERMINISTIC`** (<span class="type">integer</span>)  
<span class="simpara"> 设定 <span
class="function">PDO::sqliteCreateFunction</span>
返回的函数是结果确定的（deterministic）。 举例说明：在同一个 SQL
statement 内，函数的参数不变，则返回的结果也不变。 （PHP 7.1.4起有效）
</span>

连接与连接管理
==============

连接是通过创建 PDO 基类的实例而建立的。不管使用哪种驱动程序，都是用 PDO
类名。构造函数接收用于指定数据库源（所谓的
DSN）以及可能还包括用户名和密码（如果有的话）的参数。

**示例 \#1 连接到 MySQL**

``` php
<?php
$dbh = new PDO('mysql:host=localhost;dbname=test', $user, $pass);
?>
```

如果有任何连接错误，将抛出一个 *PDOException*
异常对象。如果想处理错误状态，可以捕获异常，或者选择留给通过 <span
class="function">set\_exception\_handler</span>
设置的应用程序全局异常处理程序。

**示例 \#2 处理连接错误**

``` php
<?php
try {
    $dbh = new PDO('mysql:host=localhost;dbname=test', $user, $pass);
    foreach($dbh->query('SELECT * from FOO') as $row) {
        print_r($row);
    }
    $dbh = null;
} catch (PDOException $e) {
    print "Error!: " . $e->getMessage() . "<br/>";
    die();
}
?>
```

**Warning**

如果应用程序不在 PDO 构造函数中捕获异常，zend
引擎采取的默认动作是结束脚本并显示一个回溯跟踪，此回溯跟踪可能泄漏完整的数据库连接细节，包括用户名和密码。因此有责任去显式（通过
*catch* 语句）或隐式（通过 <span
class="function">set\_exception\_handler</span> ）地捕获异常。

连接数据成功后，返回一个 PDO 类的实例给脚本，此连接在 PDO
对象的生存周期中保持活动。要想关闭连接，需要销毁对象以确保所有剩余到它的引用都被删除，可以赋一个
**`NULL`** 值给对象变量。如果不明确地这么做，PHP
在脚本结束时会自动关闭连接。

**示例 \#3 关闭一个连接**

``` php
<?php
$dbh = new PDO('mysql:host=localhost;dbname=test', $user, $pass);
// 在此使用连接


// 现在运行完成，在此关闭连接
$dbh = null;
?>
```

很多 web
应用程序通过使用到数据库服务的持久连接获得好处。持久连接在脚本结束后不会被关闭，且被缓存，当另一个使用相同凭证的脚本连接请求时被重用。持久连接缓存可以避免每次脚本需要与数据库回话时建立一个新连接的开销，从而让
web 应用程序更快。

**示例 \#4 持久化连接**

``` php
<?php
$dbh = new PDO('mysql:host=localhost;dbname=test', $user, $pass, array(
    PDO::ATTR_PERSISTENT => true
));
?>
```

> **Note**:
>
> 如果想使用持久连接，必须在传递给 PDO 构造函数的驱动选项数组中设置
> **`PDO::ATTR_PERSISTENT`** 。如果是在对象初始化之后用 <span
> class="function">PDO::setAttribute</span>
> 设置此属性，则驱动程序将不会使用持久连接。

> **Note**:
>
> 如果使用 PDO ODBC 驱动且 ODBC 库支持 ODBC 连接池（有unixODBC 和
> Windows 两种做法；可能会有更多），建议不要使用持久的 PDO
> 连接，而是把连接缓存留给 ODBC 连接池层处理。 ODBC
> 连接池在进程中与其他模块共享；如果要求 PDO
> 缓存连接，则此连接绝不会被返回到 ODBC
> 连接池，导致创建额外的连接来服务其他模块。

事务与自动提交
==============

现在通过 PDO 连接上了，在开始进行查询前，必须先理解 PDO
是如何管理事务的。事务支持四大特性（ACID）：原子性（Atomicity）、一致性（Consistency）、隔离性（Isolation）以及持久性（Durability）。通俗地讲，在一个事务中执行的任何操作，即使是分阶段执行的，也能保证安全地应用于数据库，并在提交时不会受到来自其他连接的干扰。事务操作也可以根据请求自动撤销（假设还没有提交），这使得在脚本中处理错误更加容易。

事务通常是通过把一批更改“积蓄”起来然后使之同时生效而实现的；这样做的好处是可以大大地提供这些更改的效率。换句话说，事务可以使脚本更快，而且可能更健壮（不过需要正确地使用事务才能获得这样的好处）。

不幸的是，并非每种数据库都支持事务，因此当第一次打开连接时，PDO
需要在所谓的“自动提交”模式下运行。自动提交模式意味着，如果数据库支持，运行的每个查询都有它自己的隐式事务，如果数据库不支持事务，则没有。如果需要一个事务，则必须用
<span class="function">PDO::beginTransaction</span>
方法来启动。如果底层驱动不支持事务，则抛出一个 PDOException
异常（不管错误处理设置是怎样的，这都是一个严重的错误状态）。一旦开始了事务，可用
<span class="function">PDO::commit</span> 或 <span
class="function">PDO::rollBack</span>来完成，这取决于事务中的代码是否运行成功。

**Warning**

PDO
仅在驱动层检查是否具有事务处理能力。如果某些运行时条件意味着事务不可用，且数据库服务接受请求去启动一个事务，
<span class="methodname">PDO::beginTransaction</span> 将仍然返回
**`TRUE`** 而且没有错误。

试着在 MySQL 数据库的 MyISAM 数据表中使用事务就是一个很好的例子。

当脚本结束或连接即将被关闭时，如果尚有一个未完成的事务，那么 PDO
将自动回滚该事务。这种安全措施有助于在脚本意外终止时避免出现不一致的情况——如果没有显式地提交事务，那么假设是某个地方出错了，所以执行回滚来保证数据安全。

**Warning**

只有通过 <span class="function">PDO::beginTransaction</span>
启动一个事务后，才可能发生自动回滚。如果手动发出一条查询启动事务， 则
PDO 无法知晓，从而在必要时不能进行回滚。

**示例 \#1 在事务中执行批处理**

在下面例子中，假设为新员工创建一组条目，分配一个为23的ID。除了登记此人的基本数据之外，还需要记录他的工资。两个更新分别完成起来很简单，但通过封闭在
<span class="function">PDO::beginTransaction</span> 和<span
class="function">PDO::commit</span>
调用中，可以保证在更改完成之前，其他人无法看到这些更改。如果发生了错误，catch
块回滚自事务启动以来发生的所有更改，并输出一条错误信息。

``` php
<?php
try {
  $dbh = new PDO('odbc:SAMPLE', 'db2inst1', 'ibmdb2', 
      array(PDO::ATTR_PERSISTENT => true));
  echo "Connected\n";
} catch (Exception $e) {
  die("Unable to connect: " . $e->getMessage());
}

try {  
  $dbh->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);

  $dbh->beginTransaction();
  $dbh->exec("insert into staff (id, first, last) values (23, 'Joe', 'Bloggs')");
  $dbh->exec("insert into salarychange (id, amount, changedate) 
      values (23, 50000, NOW())");
  $dbh->commit();
  
} catch (Exception $e) {
  $dbh->rollBack();
  echo "Failed: " . $e->getMessage();
}
?>
```

并不局限于在事务中更改，也可以发出复杂的查询来提取数据，还可以使用那些信息来构建更多的更改和查询；当事务激活时，可以保证其他人在操作进行当中无法作出更改。想更进一步阅读关于事务的信息，可参考数据库服务提供的文档。

预处理语句与存储过程
====================

很多更成熟的数据库都支持预处理语句的概念。什么是预处理语句？可以把它看作是想要运行的
SQL
的一种编译过的模板，它可以使用变量参数进行定制。预处理语句可以带来两大好处：

-   <span class="simpara">
    查询仅需解析（或预处理）一次，但可以用相同或不同的参数执行多次。当查询准备好后，数据库将分析、编译和优化执行该查询的计划。对于复杂的查询，此过程要花费较长的时间，如果需要以不同参数多次重复相同的查询，那么该过程将大大降低应用程序的速度。通过使用预处理语句，可以避免重复分析/编译/优化周期。简言之，预处理语句占用更少的资源，因而运行得更快。
    </span>
-   <span class="simpara">
    提供给预处理语句的参数不需要用引号括起来，驱动程序会自动处理。如果应用程序只使用预处理语句，可以确保不会发生SQL
    注入。（然而，如果查询的其他部分是由未转义的输入来构建的，则仍存在
    SQL 注入的风险）。 </span>

预处理语句如此有用，以至于它们唯一的特性是在驱动程序不支持的时PDO
将模拟处理。这样可以确保不管数据库是否具有这样的功能，都可以确保应用程序可以用相同的数据访问模式。

**示例 \#1 用预处理语句进行重复插入**

下面例子通过用 *name* 和 *value* 替代相应的命名占位符来执行一个插入查询

``` php
<?php
$stmt = $dbh->prepare("INSERT INTO REGISTRY (name, value) VALUES (:name, :value)");
$stmt->bindParam(':name', $name);
$stmt->bindParam(':value', $value);

// 插入一行
$name = 'one';
$value = 1;
$stmt->execute();

//  用不同的值插入另一行
$name = 'two';
$value = 2;
$stmt->execute();
?>
```

**示例 \#2 用预处理语句进行重复插入**

下面例子通过用 *name* 和 *value* 取代 *?*
占位符的位置来执行一条插入查询。

``` php
<?php
$stmt = $dbh->prepare("INSERT INTO REGISTRY (name, value) VALUES (?, ?)");
$stmt->bindParam(1, $name);
$stmt->bindParam(2, $value);

// 插入一行
$name = 'one';
$value = 1;
$stmt->execute();

// 用不同的值插入另一行
$name = 'two';
$value = 2;
$stmt->execute();
?>
```

**示例 \#3 使用预处理语句获取数据**

下面例子获取数据基于键值已提供的形式。用户的输入被自动用引号括起来，因此不会有
SQL 注入攻击的危险。

``` php
<?php
$stmt = $dbh->prepare("SELECT * FROM REGISTRY where name = ?");
if ($stmt->execute(array($_GET['name']))) {
  while ($row = $stmt->fetch()) {
    print_r($row);
  }
}
?>
```

如果数据库驱动支持，应用程序还可以绑定输出和输入参数.输出参数通常用于从存储过程获取值。输出参数使用起来比输入参数要稍微复杂一些，因为当绑定一个输出参数时，必须知道给定参数的长度。如果为参数绑定的值大于建议的长度，就会产生一个错误。

**示例 \#4 带输出参数调用存储过程**

``` php
<?php
$stmt = $dbh->prepare("CALL sp_returns_string(?)");
$stmt->bindParam(1, $return_value, PDO::PARAM_STR, 4000); 

// 调用存储过程
$stmt->execute();

print "procedure returned $return_value\n";
?>
```

还可以指定同时具有输入和输出值的参数，其语法类似于输出参数。在下一个例子中，字符串“hello”被传递给存储过程，当存储过程返回时，hello
被替换为该存储过程返回的值。

**示例 \#5 带输入/输出参数调用存储过程**

``` php
<?php
$stmt = $dbh->prepare("CALL sp_takes_string_returns_string(?)");
$value = 'hello';
$stmt->bindParam(1, $value, PDO::PARAM_STR|PDO::PARAM_INPUT_OUTPUT, 4000); 

// 调用存储过程
$stmt->execute();

print "procedure returned $value\n";
?>
```

**示例 \#6 占位符的无效使用**

``` php
<?php
$stmt = $dbh->prepare("SELECT * FROM REGISTRY where name LIKE '%?%'");
$stmt->execute(array($_GET['name']));

// 占位符必须被用在整个值的位置
$stmt = $dbh->prepare("SELECT * FROM REGISTRY where name LIKE ?");
$stmt->execute(array("%$_GET[name]%"));
?>
```

错误与错误处理
==============

PDO 提供了三种不同的错误处理模式，以满足不同风格的应用开发：

-   **`PDO::ERRMODE_SILENT`**

    此为默认模式。 PDO 将只简单地设置错误码，可使用 <span
    class="function">PDO::errorCode</span> 和 <span
    class="function">PDO::errorInfo</span>
    方法来检查语句和数据库对象。如果错误是由于对语句对象的调用而产生的，那么可以调用那个对象的
    <span class="function">PDOStatement::errorCode</span> 或 <span
    class="function">PDOStatement::errorInfo</span>
    方法。如果错误是由于调用数据库对象而产生的，那么可以在数据库对象上调用上述两个方法。

-   **`PDO::ERRMODE_WARNING`**

    除设置错误码之外，PDO 还将发出一条传统的 E\_WARNING
    信息。如果只是想看看发生了什么问题且不中断应用程序的流程，那么此设置在调试/测试期间非常有用。

-   **`PDO::ERRMODE_EXCEPTION`**

    除设置错误码之外，PDO 还将抛出一个 <span
    class="classname">PDOException</span>
    异常类并设置它的属性来反射错误码和错误信息。此设置在调试期间也非常有用，因为它会有效地放大脚本中产生错误的点，从而可以非常快速地指出代码中有问题的潜在区域（记住：如果异常导致脚本终止，则事务被自动回滚）。

    异常模式另一个非常有用的是，相比传统 PHP
    风格的警告，可以更清晰地构建自己的错误处理，而且比起静默模式和显式地检查每种数据库调用的返回值，异常模式需要的代码/嵌套更少。

    See <a href="/language/exceptions.html" class="link">Exceptions</a>
    for more information about Exceptions in PHP.

PDO 使用 SQL-92 SQLSTATE 来规范错误码字符串；不同 PDO
驱动程序负责将它们的本地代码映射为适当的 SQLSTATE 代码。<span
class="function">PDO::errorCode</span> 方法返回一个单独的 SQLSTATE
码。如果需要更多此错误的细节信息，PDO 还提供了一个 <span
class="function">PDO::errorInfo</span> 方法来返回一个包含 SQLSTATE
码、特定驱动错误码以及此驱动的错误字符串的数组。

**示例 \#1 创建 PDO 实例并设置错误模式**

``` php
<?php
$dsn = 'mysql:dbname=testdb;host=127.0.0.1';
$user = 'dbuser';
$password = 'dbpass';

try {
    $dbh = new PDO($dsn, $user, $password);
    $dbh->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
} catch (PDOException $e) {
    echo 'Connection failed: ' . $e->getMessage();
}

?>
```

> **Note**:
>
> 不管当前是否设置了 **`PDO::ATTR_ERRMODE`** ，如果连接失败，<span
> class="function">PDO::\_\_construct</span> 将总是抛出一个 <span
> class="classname">PDOException</span> 异常。未捕获异常是致命的。

**示例 \#2 创建 PDO 实例并在构造函数中设置错误模式**

``` php
<?php
$dsn = 'mysql:dbname=test;host=127.0.0.1';
$user = 'googleguy';
$password = 'googleguy';

/*
    使用 try/catch 围绕构造函数仍然有效，即使设置了 ERRMODE 为 WARNING，
    因为如果连接失败，PDO::__construct 将总是抛出一个  PDOException 异常。
*/
try {
    $dbh = new PDO($dsn, $user, $password, array(PDO::ATTR_ERRMODE => PDO::ERRMODE_WARNING));
} catch (PDOException $e) {
    echo 'Connection failed: ' . $e->getMessage();
    exit;
}

// 这里将导致 PDO 抛出一个 E_WARNING 级别的错误，而不是 一个异常 （当数据表不存在时）
$dbh->query("SELECT wrongcolumn FROM wrongtable");
?>
```

以上例程会输出：

    Warning: PDO::query(): SQLSTATE[42S02]: Base table or view not found: 1146 Table 'test.wrongtable' doesn't exist in
    /tmp/pdo_test.php on line 18

大对象 (LOBs)
=============

应用程序在某一时刻，可能需要在数据库中存储“大”数据。“大”通常意味着“大约
4kb 或以上”，尽管某些数据库在数据达到“大”之前可以轻松地处理多达 32kb
的数据。大对象本质上可能是文本或二进制。在 <span
class="function">PDOStatement::bindParam</span> 或 <span
class="function">PDOStatement::bindColumn</span>) 调用中使用
**`PDO::PARAM_LOB`** 类型码可以让 PDO
使用大数据类型。**`PDO::PARAM_LOB`** 告诉 PDO
作为流来映射数据，以便能使用
<a href="/ref/stream.html" class="link">PHP Streams API</a> 来操作。

**示例 \#1 从数据库中显示一张图片**

下面例子绑定一个 LOB 到 $lob 变量，然后用 <span
class="function">fpassthru</span> 将其发送到浏览器。因为 LOB
代表一个流，所以类似 <span class="function">fgets</span>、<span
class="function">fread</span> 以及 <span
class="function">stream\_get\_contents</span>
这样的函数都可以用在它上面。

``` php
<?php
$db = new PDO('odbc:SAMPLE', 'db2inst1', 'ibmdb2');
$stmt = $db->prepare("select contenttype, imagedata from images where id=?");
$stmt->execute(array($_GET['id']));
$stmt->bindColumn(1, $type, PDO::PARAM_STR, 256);
$stmt->bindColumn(2, $lob, PDO::PARAM_LOB);
$stmt->fetch(PDO::FETCH_BOUND);

header("Content-Type: $type");
fpassthru($lob);
?>
```

**示例 \#2 插入一张图片到数据库**

下面例子打开一个文件并将文件句柄传给 PDO 来做为一个 LOB
插入。PDO尽可能地让数据库以最有效的方式获取文件内容。

``` php
<?php
$db = new PDO('odbc:SAMPLE', 'db2inst1', 'ibmdb2');
$stmt = $db->prepare("insert into images (id, contenttype, imagedata) values (?, ?, ?)");
$id = get_new_id(); // 调用某个函数来分配一个新 ID

// 假设处理一个文件上传
// 可以在 PHP 文档中找到更多的信息

$fp = fopen($_FILES['file']['tmp_name'], 'rb');

$stmt->bindParam(1, $id);
$stmt->bindParam(2, $_FILES['file']['type']);
$stmt->bindParam(3, $fp, PDO::PARAM_LOB);

$db->beginTransaction();
$stmt->execute();
$db->commit();
?>
```

**示例 \#3 插入一张图片到数据库：Oracle**

对于从文件插入一个
lob，Oracle略有不同。必须在事务之后进行插入，否则当执行查询时导致新近插入
LOB 将以0长度被隐式提交：

``` php
<?php
$db = new PDO('oci:', 'scott', 'tiger');
$stmt = $db->prepare("insert into images (id, contenttype, imagedata) " .
"VALUES (?, ?, EMPTY_BLOB()) RETURNING imagedata INTO ?");
$id = get_new_id(); // 调用某个函数来分配一个新 ID

// 假设处理一个文件上传
// 可以在 PHP 文档中找到更多的信息

$fp = fopen($_FILES['file']['tmp_name'], 'rb');

$stmt->bindParam(1, $id);
$stmt->bindParam(2, $_FILES['file']['type']);
$stmt->bindParam(3, $fp, PDO::PARAM_LOB);

$stmt->beginTransaction();
$stmt->execute();
$stmt->commit();
?>
```

简介
----

代表 PHP 和数据库服务之间的一个连接

类摘要
------

**PDO**

<span class="ooclass"> class **PDO** </span> {

<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$dsn`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$username`</span> \[, <span class="methodparam"><span
class="type">string</span> `$password`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$driver_options`</span> \]\]\] )

<span class="type">bool</span> <span
class="methodname">beginTransaction</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span class="methodname">commit</span> (
<span class="methodparam">void</span> )

<span class="type">mixed</span> <span
class="methodname">errorCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">errorInfo</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span class="methodname">exec</span> (
<span class="methodparam"><span class="type">string</span>
`$statement`</span> )

<span class="type">mixed</span> <span
class="methodname">getAttribute</span> ( <span class="methodparam"><span
class="type">int</span> `$attribute`</span> )

<span class="modifier">static</span> <span class="type">array</span>
<span class="methodname">getAvailableDrivers</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">inTransaction</span> ( <span
class="methodparam">void</span> )

<span class="type">string</span> <span
class="methodname">lastInsertId</span> (\[ <span
class="methodparam"><span class="type">string</span> `$name`<span
class="initializer"> = **`NULL`**</span></span> \] )

<span class="modifier">public</span> <span
class="type">PDOStatement</span> <span class="methodname">prepare</span>
( <span class="methodparam"><span class="type">string</span>
`$statement`</span> \[, <span class="methodparam"><span
class="type">array</span> `$driver_options`<span class="initializer"> =
array()</span></span> \] )

<span class="modifier">public</span> <span
class="type">PDOStatement</span> <span class="methodname">query</span> (
<span class="methodparam"><span class="type">string</span>
`$statement`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">quote</span> ( <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">int</span> `$parameter_type`<span
class="initializer"> = PDO::PARAM\_STR</span></span> \] )

<span class="type">bool</span> <span class="methodname">rollBack</span>
( <span class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">setAttribute</span> ( <span class="methodparam"><span
class="type">int</span> `$attribute`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

}

PDO::beginTransaction
=====================

启动一个事务

### 说明

<span class="type">bool</span> <span
class="methodname">PDO::beginTransaction</span> ( <span
class="methodparam">void</span> )

关闭自动提交模式。自动提交模式被关闭的同时，通过 PDO
对象实例对数据库做出的更改直到调用 <span
class="function">PDO::commit</span> 结束事务才被提交。调用 <span
class="function">PDO::rollBack</span>
将回滚对数据库做出的更改并将数据库连接返回到自动提交模式。

包括 MySQL 在内的一些数据库，当发出一条类似 DROP TABLE 或 CREATE TABLE
这样的 DDL
语句时，会自动进行一个隐式地事务提交。隐式地提交将阻止你在此事务范围内回滚任何其他更改。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 回滚一个事务**

下面例子在回滚此更改前开始一个事务并发出两条修改数据库的语句。但在 MySQL
中，DROP TABLE 语句自动提交事务，使得在此事务中的任何更改都不会被回滚。

``` php
<?php
/* 开始一个事务，关闭自动提交 */
$dbh->beginTransaction();

/*  更改数据库架构及数据 */
$sth = $dbh->exec("DROP TABLE fruit");
$sth = $dbh->exec("UPDATE dessert
    SET name = 'hamburger'");

/*  识别出错误并回滚更改 */
$dbh->rollBack();

/* 数据库连接现在返回到自动提交模式 */
?>
```

### 参见

-   <span class="function">PDO::commit</span>
-   <span class="function">PDO::rollBack</span>
-   <a href="/book/pdo.html#事务与自动提交" class="link">事务与自动提交</a>

PDO::commit
===========

提交一个事务

### 说明

<span class="type">bool</span> <span
class="methodname">PDO::commit</span> ( <span
class="methodparam">void</span> )

提交一个事务，数据库连接返回到自动提交模式直到下次调用 <span
class="function">PDO::beginTransaction</span> 开始一个新的事务为止。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 提交一个基础事务**

``` php
<?php
/* 开始一个事务，关闭自动提交 */
$dbh->beginTransaction();

/* 在全有或全无的基础上插入多行记录（要么全部插入，要么全部不插入） */
$sql = 'INSERT INTO fruit
    (name, colour, calories)
    VALUES (?, ?, ?)';

$sth = $dbh->prepare($sql);

foreach ($fruits as $fruit) {
    $sth->execute(array(
        $fruit->name,
        $fruit->colour,
        $fruit->calories,
    ));
}

/* 提交更改 */
$dbh->commit();

/* 现在数据库连接返回到自动提交模式 */
?>
```

**示例 \#2 提交一个DDL事务**

``` php
<?php
/*  开始一个事务，关闭自动提交 */
$dbh->beginTransaction();

/* Change the database schema */
$sth = $dbh->exec("DROP TABLE fruit");

/* 更改数据库架构 */
$dbh->commit();

/* 现在数据库连接返回到自动提交模式 */
?>
```

> **Note**: <span class="simpara">
> 并不是所有数据库都允许使用DDL语句进行事务操作：有些会产生错误，而其他一些（包括MySQL）会在遇到第一个DDL语句后就自动提交事务。
> </span>

### 参见

-   <span class="function">PDO::beginTransaction</span>
-   <span class="function">PDO::rollBack</span>
-   <a href="/book/pdo.html#事务与自动提交" class="link">事务和自动提交</a>

PDO::\_\_construct
==================

创建一个表示数据库连接的 PDO 实例

### 说明

<span class="methodname">PDO::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$dsn`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$username`</span> \[, <span class="methodparam"><span
class="type">string</span> `$password`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$driver_options`</span> \]\]\] )

创建一个表示连接到请求数据库的数据库连接 PDO 实例。

### 参数

dsn  
数据源名称或叫做 DSN，包含了请求连接到数据库的信息。

通常，一个 DSN 由 PDO 驱动名、紧随其后的冒号、以及具体 PDO
驱动的连接语法组成。更深入的信息能从
<a href="/book/pdo.html#PDO%20驱动" class="link">PDO 具体驱动文档</a>找到。

The `dsn` 参数支持三种不同的方式 创建一个数据库连接：

Driver invocation  
`dsn` 包含完整的DSN。

URI invocation  
`dsn` consists of **`uri:`** followed by a URI that defines the location
of a file containing the DSN string. The URI can specify a local file or
a remote URL.

**`uri:file:///path/to/dsnfile`**

Aliasing  
`dsn` consists of a name `name` that maps to `pdo.dsn.name` in `php.ini`
defining the DSN string.

> **Note**:
>
> 别名必须得在 `php.ini` 中定义了，不能是在 `.htaccess` 或 `httpd.conf`
> 中 。

username  
DSN字符串中的用户名。对于某些PDO驱动，此参数为可选项。

password  
DSN字符串中的密码。对于某些PDO驱动，此参数为可选项。

driver\_options  
一个具体驱动的连接选项的键=\>值数组。

### 返回值

成功则返回一个PDO对象。

### 错误／异常

如果试图连接到请求的数据库失败，则<span
class="function">PDO::\_\_construct</span> 抛出一个 PDO异常（<span
class="classname">PDOException</span>） 。

### 范例

**示例 \#1 Create a PDO instance via driver invocation**

``` php
<?php
/* Connect to an ODBC database using driver invocation */
$dsn = 'mysql:dbname=testdb;host=127.0.0.1';
$user = 'dbuser';
$password = 'dbpass';

try {
    $dbh = new PDO($dsn, $user, $password);
} catch (PDOException $e) {
    echo 'Connection failed: ' . $e->getMessage();
}

?>
```

**示例 \#2 Create a PDO instance via URI invocation**

The following example assumes that the file `/usr/local/dbconnect`
exists with file permissions that enable PHP to read the file. The file
contains the PDO DSN to connect to a DB2 database through the PDO\_ODBC
driver:

    odbc:DSN=SAMPLE;UID=john;PWD=mypass

The PHP script can then create a database connection by simply passing
the *uri:* parameter and pointing to the file URI:

``` php
<?php
/* Connect to an ODBC database using driver invocation */
$dsn = 'uri:file:///usr/local/dbconnect';
$user = '';
$password = '';

try {
    $dbh = new PDO($dsn, $user, $password);
} catch (PDOException $e) {
    echo 'Connection failed: ' . $e->getMessage();
}

?>
```

**示例 \#3 使用别名创建一个PDO实例**

The following example assumes that `php.ini` contains the following
entry to enable a connection to a MySQL database using only the alias
*mydb*:

``` ini
[PDO]
pdo.dsn.mydb="mysql:dbname=testdb;host=localhost"
```

``` php
<?php
/*  使用别名连接到一个ODBC数据库  */
$dsn = 'mydb';
$user = '';
$password = '';

try {
    $dbh = new PDO($dsn, $user, $password);
} catch (PDOException $e) {
    echo 'Connection failed: ' . $e->getMessage();
}

?>
```

PDO::errorCode
==============

获取跟数据库句柄上一次操作相关的 SQLSTATE

### 说明

<span class="type">mixed</span> <span
class="methodname">PDO::errorCode</span> ( <span
class="methodparam">void</span> )

### 返回值

返回一个 SQLSTATE，一个由5个字母或数字组成的在 ANSI SQL
标准中定义的标识符。 简要地说，一个 SQLSTATE
由前面两个字符的类值和后面三个字符的子类值组成。 class value of 01
indicates a warning and is accompanied by a return code of
SQL\_SUCCESS\_WITH\_INFO. Class values other than '01', except for the
class 'IM', indicate an error. The class 'IM' is specific to warnings
and errors that derive from the implementation of PDO (or perhaps ODBC,
if you're using the ODBC driver) itself. The subclass value '000' in any
class indicates that there is no subclass for that SQLSTATE.

<span class="function">PDO::errorCode</span> only retrieves error codes
for operations performed directly on the database handle. If you create
a PDOStatement object through <span class="function">PDO::prepare</span>
or <span class="function">PDO::query</span> and invoke an error on the
statement handle, <span class="function">PDO::errorCode</span> will not
reflect that error. You must call <span
class="function">PDOStatement::errorCode</span> to return the error code
for an operation performed on a particular statement handle.

如果数据库句柄没有进行操作，则返回 **`NULL`** 。

### 范例

**示例 \#1 取得一个 SQLSTATE 码**

``` php
<?php
/* 引发一个错误 -- BONES 数据表不存在 */
$dbh->exec("INSERT INTO bones(skull) VALUES ('lucy')");

echo "\nPDO::errorCode(): ";
print $dbh->errorCode();
?>
```

以上例程会输出：

    PDO::errorCode(): 42S02

### 参见

-   <span class="function">PDO::errorInfo</span>
-   <span class="function">PDOStatement::errorCode</span>
-   <span class="function">PDOStatement::errorInfo</span>

PDO::errorInfo
==============

Fetch extended error information associated with the last operation on
the database handle

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">PDO::errorInfo</span> ( <span
class="methodparam">void</span> )

### 返回值

<span class="function">PDO::errorInfo</span> returns an array of error
information about the last operation performed by this database handle.
The array consists of at least the following fields:

| Element | Information                                                                                       |
|---------|---------------------------------------------------------------------------------------------------|
| 0       | SQLSTATE error code (a five characters alphanumeric identifier defined in the ANSI SQL standard). |
| 1       | Driver-specific error code.                                                                       |
| 2       | Driver-specific error message.                                                                    |

> **Note**:
>
> If the SQLSTATE error code is not set or there is no driver-specific
> error, the elements following element 0 will be set to **`NULL`**.

<span class="function">PDO::errorInfo</span> only retrieves error
information for operations performed directly on the database handle. If
you create a PDOStatement object through <span
class="function">PDO::prepare</span> or <span
class="function">PDO::query</span> and invoke an error on the statement
handle, <span class="function">PDO::errorInfo</span> will not reflect
the error from the statement handle. You must call <span
class="function">PDOStatement::errorInfo</span> to return the error
information for an operation performed on a particular statement handle.

### 范例

**示例 \#1 Displaying errorInfo() fields for a PDO\_ODBC connection to a
DB2 database**

``` php
<?php
/* Provoke an error -- bogus SQL syntax */
$stmt = $dbh->prepare('bogus sql');
if (!$stmt) {
    echo "\nPDO::errorInfo():\n";
    print_r($dbh->errorInfo());
}
?>
```

以上例程会输出：

    PDO::errorInfo():
    Array
    (
        [0] => HY000
        [1] => 1
        [2] => near "bogus": syntax error
    )

### 参见

-   <span class="function">PDO::errorCode</span>
-   <span class="function">PDOStatement::errorCode</span>
-   <span class="function">PDOStatement::errorInfo</span>

PDO::exec
=========

执行一条 SQL 语句，并返回受影响的行数

### 说明

<span class="type">int</span> <span class="methodname">PDO::exec</span>
( <span class="methodparam"><span class="type">string</span>
`$statement`</span> )

<span class="function">PDO::exec</span> 在一个单独的函数调用中执行一条
SQL 语句，返回受此语句影响的行数。

<span class="function">PDO::exec</span> 不会从一条 SELECT
语句中返回结果。对于在程序中只需要发出一次的 SELECT 语句，可以考虑使用
<span class="function">PDO::query</span>。对于需要发出多次的语句，可用
<span class="function">PDO::prepare</span> 来准备一个 PDOStatement
对象并用 <span class="function">PDOStatement::execute</span> 发出语句。

### 参数

`statement`  
要被预处理和执行的 SQL 语句。

查询中的数据应该被
<a href="/book/pdo.html#PDO::quote" class="link">妥善地转义</a> 。

### 返回值

<span class="function">PDO::exec</span> 返回受修改或删除 SQL
语句影响的行数。如果没有受影响的行，则 <span
class="function">PDO::exec</span> 返回 0。

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

下面例子依赖 <span class="function">PDO::exec</span>
的返回值是不正确的，其中受影响行数为 0 的语句会导致调用 <span
class="function">die</span> ：

``` php
<?php
$db->exec() or die(print_r($db->errorInfo(), true));
?>
```

### 范例

**示例 \#1 发出一条 DELETE 语句**

计算由一条不带 WHERE 字句的 DELETE 语句删除的行数。

``` php
<?php
$dbh = new PDO('odbc:sample', 'db2inst1', 'ibmdb2');

/*  删除 FRUIT 数据表中满足条件的所有行 */
$count = $dbh->exec("DELETE FROM fruit WHERE colour = 'red'");

/* 返回被删除的行数 */
print("Deleted $count rows.\n");
?>
```

以上例程会输出：

    Deleted 1 rows.

### 参见

-   <span class="function">PDO::prepare</span>
-   <span class="function">PDO::query</span>
-   <span class="function">PDOStatement::execute</span>

PDO::getAttribute
=================

取回一个数据库连接的属性

### 说明

<span class="type">mixed</span> <span
class="methodname">PDO::getAttribute</span> ( <span
class="methodparam"><span class="type">int</span> `$attribute`</span> )

此函数（方法）返回一个数据库连接的属性值。 取回 PDOStatement
属性，请参阅 <span class="function">PDOStatement::getAttribute</span>。

注意有些数据库/驱动可能不支持所有的数据库连接属性。

### 参数

`attribute`  
*PDO::ATTR\_\** 常量中的一个。下列为应用到数据库连接中的常量：

-   *PDO::ATTR\_AUTOCOMMIT*
-   *PDO::ATTR\_CASE*
-   *PDO::ATTR\_CLIENT\_VERSION*
-   *PDO::ATTR\_CONNECTION\_STATUS*
-   *PDO::ATTR\_DRIVER\_NAME*
-   *PDO::ATTR\_ERRMODE*
-   *PDO::ATTR\_ORACLE\_NULLS*
-   *PDO::ATTR\_PERSISTENT*
-   *PDO::ATTR\_PREFETCH*
-   *PDO::ATTR\_SERVER\_INFO*
-   *PDO::ATTR\_SERVER\_VERSION*
-   *PDO::ATTR\_TIMEOUT*

### 返回值

成功调用则返回请求的 PDO 属性值。不成功则返回 *null*。

### 范例

**示例 \#1 取回数据库连接属性**

``` php
<?php
$conn = new PDO('odbc:sample', 'db2inst1', 'ibmdb2');
$attributes = array(
    "AUTOCOMMIT", "ERRMODE", "CASE", "CLIENT_VERSION", "CONNECTION_STATUS",
    "ORACLE_NULLS", "PERSISTENT", "PREFETCH", "SERVER_INFO", "SERVER_VERSION",
    "TIMEOUT"
);

foreach ($attributes as $val) {
    echo "PDO::ATTR_$val: ";
    echo $conn->getAttribute(constant("PDO::ATTR_$val")) . "\n";
}
?>
```

### 参见

-   <span class="function">PDO::setAttribute</span>
-   <span class="function">PDOStatement::getAttribute</span>
-   <span class="function">PDOStatement::setAttribute</span>

PDO::getAvailableDrivers
========================

返回一个可用驱动的数组

### 说明

<span class="modifier">static</span> <span class="type">array</span>
<span class="methodname">PDO::getAvailableDrivers</span> ( <span
class="methodparam">void</span> )

<span class="type">array</span> <span
class="methodname">pdo\_drivers</span> ( <span
class="methodparam">void</span> )

此函数（方法）返回所有当前可用在 <span
class="function">PDO::\_\_construct</span> 的参数 `DSN` 中的 PDO 驱动。

### 返回值

<span class="function">PDO::getAvailableDrivers</span> 返回一个 包含可用
PDO 驱动名字的数组。如果没有可用的驱动，则返回一个空数组。

### 范例

**示例 \#1 一个 <span class="function">PDO::getAvailableDrivers</span>
的例子**

``` php
<?php
print_r(PDO::getAvailableDrivers());
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => mysql
        [1] => sqlite
    )

PDO::inTransaction
==================

检查是否在一个事务内

### 说明

<span class="type">bool</span> <span
class="methodname">PDO::inTransaction</span> ( <span
class="methodparam">void</span> )

检查驱动内的一个事务当前是否处于激活。此方法仅对支持事务的数据库驱动起作用。

### 参数

此函数没有参数。

### 返回值

如果当前事务处于激活，则返回 **`TRUE`** ，否则返回 **`FALSE`** 。

PDO::lastInsertId
=================

返回最后插入行的ID或序列值

### 说明

<span class="type">string</span> <span
class="methodname">PDO::lastInsertId</span> (\[ <span
class="methodparam"><span class="type">string</span> `$name`<span
class="initializer"> = **`NULL`**</span></span> \] )

返回最后插入行的ID，或者是一个序列对象最后的值，取决于底层的驱动。比如，<span
class="function">PDO\_PGSQL</span> 要求为 `name`
参数指定序列对象的名称。

> **Note**:
>
> 在不同的 PDO
> 驱动之间，此方法可能不会返回一个有意义或一致的结果，因为底层数据库可能不支持自增字段或序列的概念。

### 参数

`name`  
应该返回ID的那个序列对象的名称。

### 返回值

如果没有为参数 `name` 指定序列名称，<span
class="function">PDO::lastInsertId</span>
则返回一个表示最后插入数据库那一行的行ID的字符串。

如果为参数 `name` 指定了序列名称，<span
class="function">PDO::lastInsertId</span>
则返回一个表示从指定序列对象取回最后的值的字符串。

如果当前 PDO 驱动不支持此功能，则 <span
class="function">PDO::lastInsertId</span> 触发一个 *IM001* SQLSTATE 。

PDO::prepare
============

准备要执行的语句，并返回语句对象

### 说明

<span class="modifier">public</span> <span
class="type">PDOStatement</span> <span
class="methodname">PDO::prepare</span> ( <span class="methodparam"><span
class="type">string</span> `$statement`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$driver_options`<span class="initializer"> = array()</span></span> \] )

为 <span class="function">PDOStatement::execute</span> 方法准备待执行的
SQL 语句。 SQL
语句可以包含零个或多个参数占位标记，格式是命名（:name）或问号（?）的形式，当它执行时将用真实数据取代。
在同一个 SQL
语句里，命名形式和问号形式不能同时使用；只能选择其中一种参数形式。
请用参数形式绑定用户输入的数据，不要直接字符串拼接到查询里。

调用 <span class="function">PDOStatement::execute</span>
时，每一个值的参数占位标记，名称必须唯一。
除非启用模拟（emulation）模式，同一个语句里无法使用重名的参数。

> **Note**:
>
> 参数占位符仅能字面上展示完整的数据。不能是字面的一部分，不能是关键词，不能是标识符，不能是其他任意的范围。
> 举例说明：不能把多个值绑到单个参数里，然后在 SQL 语句里用 IN() 查询。

如果用不同参数，通过 <span class="function">PDO::prepare</span> 和 <span
class="function">PDOStatement::execute</span> 多次调用同一个 SQL
语句，将提升应用的性能 ——
驱动可以让客户端/服务器缓存查询和元信息，还能阻止 SQL
注入攻击，不需要手动给参数加引号。

如果内置驱动不支持参数，PDO
将模拟出参数的功能；如果驱动仅仅支持其中一种风格（命名参数和问号参数两种），也会自动重写到另外一种风格。

### 参数

`statement`  
必须是对目标数据库服务器有效的 SQL 语句模板。

`driver_options`  
数组包含一个或多个 key=\>value 键值对，为返回的 PDOStatement
对象设置属性。 常见用法是：设置 *PDO::ATTR\_CURSOR* 为
*PDO::CURSOR\_SCROLL*，将得到可滚动的光标。 某些驱动有驱动级的选项，在
prepare 时就设置。

### 返回值

如果数据库服务器完成准备了语句， <span
class="function">PDO::prepare</span> 返回 <span
class="classname">PDOStatement</span> 对象。
如果数据库服务器无法准备语句， <span
class="function">PDO::prepare</span> 返回 **`FALSE`** 或抛出 <span
class="classname">PDOException</span> (取决于
<a href="/book/pdo.html#错误与错误处理" class="link">错误处理器</a>)。

> **Note**:
>
> 模拟模式下的 prepare 语句不会和数据库服务器交互，所以 <span
> class="function">PDO::prepare</span> 不会检查语句。

### 范例

**示例 \#1 用命名参数形式准备 SQL 语句参数**

``` php
<?php
/* 传入数组的值，并执行准备好的语句 */
$sql = 'SELECT name, colour, calories
    FROM fruit
    WHERE calories < :calories AND colour = :colour';
$sth = $dbh->prepare($sql, array(PDO::ATTR_CURSOR => PDO::CURSOR_FWDONLY));
$sth->execute(array(':calories' => 150, ':colour' => 'red'));
$red = $sth->fetchAll();
$sth->execute(array(':calories' => 175, ':colour' => 'yellow'));
$yellow = $sth->fetchAll();
?>
```

**示例 \#2 用问号形式准备 SQL 语句参数**

``` php
<?php
/* 传入数组的值，并执行准备好的语句 */
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < ? AND colour = ?');
$sth->execute(array(150, 'red'));
$red = $sth->fetchAll();
$sth->execute(array(175, 'yellow'));
$yellow = $sth->fetchAll();
?>
```

### 参见

-   <span class="function">PDO::exec</span>
-   <span class="function">PDO::query</span>
-   <span class="function">PDOStatement::execute</span>

PDO::query
==========

执行 SQL 语句，以 PDOStatement 对象形式返回结果集

### 说明

<span class="modifier">public</span> <span
class="type">PDOStatement</span> <span
class="methodname">PDO::query</span> ( <span class="methodparam"><span
class="type">string</span> `$statement`</span> )

<span class="modifier">public</span> <span
class="type">PDOStatement</span> <span
class="methodname">PDO::query</span> ( <span class="methodparam"><span
class="type">string</span> `$statement`</span> , <span
class="methodparam"><span class="type">int</span>
`$PDO::FETCH_COLUMN`</span> , <span class="methodparam"><span
class="type">int</span> `$colno`</span> )

<span class="modifier">public</span> <span
class="type">PDOStatement</span> <span
class="methodname">PDO::query</span> ( <span class="methodparam"><span
class="type">string</span> `$statement`</span> , <span
class="methodparam"><span class="type">int</span>
`$PDO::FETCH_CLASS`</span> , <span class="methodparam"><span
class="type">string</span> `$classname`</span> , <span
class="methodparam"><span class="type">array</span> `$ctorargs`</span> )

<span class="modifier">public</span> <span
class="type">PDOStatement</span> <span
class="methodname">PDO::query</span> ( <span class="methodparam"><span
class="type">string</span> `$statement`</span> , <span
class="methodparam"><span class="type">int</span>
`$PDO::FETCH_INTO`</span> , <span class="methodparam"><span
class="type">object</span> `$object`</span> )

<span class="function">PDO::query</span> 在单次函数调用内执行 SQL
语句，以 PDOStatement 对象形式返回结果集（如果有数据的话）。

如果反复调用同一个查询，用 <span class="function">PDO::prepare</span>
准备 PDOStatement 对象，并用 <span
class="function">PDOStatement::execute</span>
执行语句，将具有更好的性能。

如果没有完整获取结果集内的数据，就调用下一个 <span
class="function">PDO::query</span>，将可能调用失败。 应当在执行下一个
<span class="function">PDO::query</span> 前，先用 <span
class="function">PDOStatement::closeCursor</span> 释放数据库PDOStatement
关联的资源。

> **Note**:
>
> 如果传入函数的参数数量超过一个，多余的参数将相当于调用结果对象 <span
> class="function">PDOStatement::setFetchMode</span> 方法。

### 参数

`statement`  
需要准备、执行的 SQL 语句。

查询里的数据应该用<a href="/book/pdo.html#PDO::quote" class="link">恰当的形式转义</a>。

### 返回值

<span class="function">PDO::query</span> 返回 PDOStatement
对象，或在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 展示 PDO::query 的使用**

<span class="function">PDO::query</span> 一个不错的功能是：执行 SELECT
语句，并能够循环遍历结果集。

``` php
<?php
function getFruit($conn) {
    $sql = 'SELECT name, color, calories FROM fruit ORDER BY name';
    foreach ($conn->query($sql) as $row) {
        print $row['name'] . "\t";
        print $row['color'] . "\t";
        print $row['calories'] . "\n";
    }
}
?>
```

以上例程会输出：

    apple   red     150
    banana  yellow  250
    kiwi    brown   75
    lemon   yellow  25
    orange  orange  300
    pear    green   150
    watermelon      pink    90

### 参见

-   <span class="function">PDO::exec</span>
-   <span class="function">PDO::prepare</span>
-   <span class="function">PDOStatement::execute</span>

PDO::quote
==========

为 SQL 查询里的字符串添加引号

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">PDO::quote</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$parameter_type`<span class="initializer"> =
PDO::PARAM\_STR</span></span> \] )

<span class="function">PDO::quote</span>
为输入的字符串添加引号（如果有需要），并对特殊字符进行转义，且引号的风格和底层驱动适配。

如果使用此函数构建 SQL 语句，*强烈*建议使用 <span
class="function">PDO::prepare</span> 配合参数构建，而不是用 <span
class="function">PDO::quote</span> 把用户输入的数据拼接进 SQL 语句。
使用 prepare 语句处理参数，不仅仅可移植性更好，而且更方便、免疫 SQL
注入；相对于拼接 SQL 更快，客户端和服务器都能缓存编译后的 SQL 查询。

不是所有的 PDO 驱动都实现了此功能（例如 PDO\_ODBC）。 考虑使用 prepare
代替。

**Caution**

字符集不仅仅要在数据库服务器上设置，也要为数据库连接设置（取决于驱动），它影响了
<span class="methodname">PDO::quote</span>。
更多信息可参考<a href="/book/pdo.html#PDO%20驱动" class="link">PDO 驱动文档</a>。

### 参数

`string`  
要添加引号的字符串。

`parameter_type`  
为驱动提示数据类型，以便选择引号风格。

### 返回值

返回加引号的字符串，理论上可以安全用于 SQL 语句。
如果驱动不支持这种方式，将返回 **`FALSE`** 。

### 范例

**示例 \#1 普通字符串加引号**

``` php
<?php
$conn = new PDO('sqlite:/home/lynn/music.sql3');

/* 简单字符串 */
$string = 'Nice';
print "Unquoted string: $string\n";
print "Quoted string: " . $conn->quote($string) . "\n";
?>
```

以上例程会输出：

    Unquoted string: Nice
    Quoted string: 'Nice'

**示例 \#2 危险字符串加引号**

``` php
<?php
$conn = new PDO('sqlite:/home/lynn/music.sql3');

/* 危险字符串 */
$string = 'Naughty \' string';
print "Unquoted string: $string\n";
print "Quoted string:" . $conn->quote($string) . "\n";
?>
```

以上例程会输出：

    Unquoted string: Naughty ' string
    Quoted string: 'Naughty '' string'

**示例 \#3 复杂字符串加引号**

``` php
<?php
$conn = new PDO('sqlite:/home/lynn/music.sql3');

/* 复杂字符串 */
$string = "Co'mpl''ex \"st'\"ring";
print "Unquoted string: $string\n";
print "Quoted string: " . $conn->quote($string) . "\n";
?>
```

以上例程会输出：

    Unquoted string: Co'mpl''ex "st'"ring
    Quoted string: 'Co''mpl''''ex "st''"ring'

### 参见

-   <span class="function">PDO::prepare</span>
-   <span class="function">PDOStatement::execute</span>

PDO::rollBack
=============

回滚一个事务

### 说明

<span class="type">bool</span> <span
class="methodname">PDO::rollBack</span> ( <span
class="methodparam">void</span> )

回滚由 <span class="function">PDO::beginTransaction</span>
发起的当前事务。如果没有事务激活，将抛出一个 <span
class="classname">PDOException</span> 异常。

如果数据库被设置成自动提交模式，此函数（方法）在回滚事务之后将恢复自动提交模式。

包括 MySQL 在内的一些数据库， 当在一个事务内有类似删除或创建数据表等 DLL
语句时，会自动导致一个隐式地提交。隐式地提交将无法回滚此事务范围内的任何更改。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 回滚一个事务**

下面例子在回滚更改之前开始一个事务并发出两条修改数据库的语句。但在 MySQL
中，DROP TABLE 语句自动提交事务，因此在此事务内的任何更改都不会被回滚。

``` php
<?php
/* 开始一个事务，关闭自动提交 */
$dbh->beginTransaction();

/* 更改数据库架构和数据  */
$sth = $dbh->exec("DROP TABLE fruit");
$sth = $dbh->exec("UPDATE dessert
    SET name = 'hamburger'");

/*  识别错误且回滚更改  */
$dbh->rollBack();

/*  此时数据库连接恢复到自动提交模式  */
?>
```

### 参见

-   <span class="function">PDO::beginTransaction</span>
-   <span class="function">PDO::commit</span>
-   <a href="/book/pdo.html#事务与自动提交" class="link">事务和自动提交</a>

PDO::setAttribute
=================

设置属性

### 说明

<span class="type">bool</span> <span
class="methodname">PDO::setAttribute</span> ( <span
class="methodparam"><span class="type">int</span> `$attribute`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

设置数据库句柄属性。下面列出了一些可用的通用属性；有些驱动可能使用另外的特定属性。

-   *PDO::ATTR\_CASE*：强制列名为指定的大小写。

    -   *PDO::CASE\_LOWER*：强制列名小写。

    -   *PDO::CASE\_NATURAL*：保留数据库驱动返回的列名。

    -   *PDO::CASE\_UPPER*：强制列名大写。

-   *PDO::ATTR\_ERRMODE*：错误报告。

    -   *PDO::ERRMODE\_SILENT*： 仅设置错误代码。

    -   *PDO::ERRMODE\_WARNING*: 引发
        <a href="" class="link">E_WARNING</a> 错误

    -   *PDO::ERRMODE\_EXCEPTION*: 抛出
        <a href="/book/pdo.html#PDOException" class="link">exceptions</a>
        异常。

-   *PDO::ATTR\_ORACLE\_NULLS* （在所有驱动中都可用，不仅限于Oracle）：
    转换 NULL 和空字符串。

    -   *PDO::NULL\_NATURAL*: 不转换。

    -   *PDO::NULL\_EMPTY\_STRING*： 将空字符串转换成 **`NULL`**。

    -   *PDO::NULL\_TO\_STRING*: 将 NULL 转换成空字符串。

-   *PDO::ATTR\_STRINGIFY\_FETCHES*: 提取的时候将数值转换为字符串。
    Requires <span class="type">bool</span>.

-   *PDO::ATTR\_STATEMENT\_CLASS*：
    设置从PDOStatement派生的用户提供的语句类。 不能用于持久的PDO实例。
    需要 *array(string 类名, array(mixed 构造函数的参数))*。

-   *PDO::ATTR\_TIMEOUT*：
    指定超时的秒数。并非所有驱动都支持此选项，这意味着驱动和驱动之间可能会有差异。比如，SQLite等待的时间达到此值后就放弃获取可写锁，但其他驱动可能会将此值解释为一个连接或读取超时的间隔。
    需要 <span class="type">int</span> 类型。

-   *PDO::ATTR\_AUTOCOMMIT* （在OCI，Firebird 以及 MySQL中可用）：
    是否自动提交每个单独的语句。

-   *PDO::ATTR\_EMULATE\_PREPARES* 启用或禁用预处理语句的模拟。
    有些驱动不支持或有限度地支持本地预处理。使用此设置强制PDO总是模拟预处理语句（如果为
    **`TRUE`** ），或试着使用本地预处理语句（如果为
    **`FALSE`**）。如果驱动不能成功预处理当前查询，它将总是回到模拟预处理语句上。
    需要 <span class="type">bool</span> 类型。

-   *PDO::MYSQL\_ATTR\_USE\_BUFFERED\_QUERY* （在MySQL中可用）：
    使用缓冲查询。

-   *PDO::ATTR\_DEFAULT\_FETCH\_MODE*：
    设置默认的提取模式。关于模式的说明可以在 <span
    class="function">PDOStatement::fetch</span> 文档找到。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

简介
----

代表一条预处理语句，并在该语句被执行后代表一个相关的结果集。

类摘要
------

**PDOStatement**

<span class="ooclass"> class **PDOStatement** </span> <span
class="oointerface">implements <span
class="interfacename">Traversable</span> </span> {

/\* 属性 \*/

<span class="modifier">readonly</span> <span
class="type">string</span>`$queryString`;

/\* 方法 \*/

<span class="type">bool</span> <span
class="methodname">bindColumn</span> ( <span class="methodparam"><span
class="type">mixed</span> `$column`</span> , <span
class="methodparam"><span class="type">mixed</span> `&$param`</span> \[,
<span class="methodparam"><span class="type">int</span> `$type`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$maxlen`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$driverdata`</span> \]\]\] )

<span class="type">bool</span> <span class="methodname">bindParam</span>
( <span class="methodparam"><span class="type">mixed</span>
`$parameter`</span> , <span class="methodparam"><span
class="type">mixed</span> `&$variable`</span> \[, <span
class="methodparam"><span class="type">int</span> `$data_type`<span
class="initializer"> = PDO::PARAM\_STR</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$length`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$driver_options`</span> \]\]\] )

<span class="type">bool</span> <span class="methodname">bindValue</span>
( <span class="methodparam"><span class="type">mixed</span>
`$parameter`</span> , <span class="methodparam"><span
class="type">mixed</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `$data_type`<span
class="initializer"> = PDO::PARAM\_STR</span></span> \] )

<span class="type">bool</span> <span
class="methodname">closeCursor</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">columnCount</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">debugDumpParams</span> ( <span
class="methodparam">void</span> )

<span class="type">string</span> <span
class="methodname">errorCode</span> ( <span
class="methodparam">void</span> )

<span class="type">array</span> <span
class="methodname">errorInfo</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span class="methodname">execute</span>
(\[ <span class="methodparam"><span class="type">array</span>
`$input_parameters`</span> \] )

<span class="type">mixed</span> <span class="methodname">fetch</span>
(\[ <span class="methodparam"><span class="type">int</span>
`$fetch_style`</span> \[, <span class="methodparam"><span
class="type">int</span> `$cursor_orientation`<span class="initializer">
= PDO::FETCH\_ORI\_NEXT</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$cursor_offset`<span
class="initializer"> = 0</span></span> \]\]\] )

<span class="type">array</span> <span class="methodname">fetchAll</span>
(\[ <span class="methodparam"><span class="type">int</span>
`$fetch_style`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$fetch_argument`</span> \[, <span
class="methodparam"><span class="type">array</span> `$ctor_args`<span
class="initializer"> = array()</span></span> \]\]\] )

<span class="type">string</span> <span
class="methodname">fetchColumn</span> (\[ <span
class="methodparam"><span class="type">int</span> `$column_number`<span
class="initializer"> = 0</span></span> \] )

<span class="type">mixed</span> <span
class="methodname">fetchObject</span> (\[ <span
class="methodparam"><span class="type">string</span> `$class_name`<span
class="initializer"> = "stdClass"</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$ctor_args`</span>
\]\] )

<span class="type">mixed</span> <span
class="methodname">getAttribute</span> ( <span class="methodparam"><span
class="type">int</span> `$attribute`</span> )

<span class="type">array</span> <span
class="methodname">getColumnMeta</span> ( <span
class="methodparam"><span class="type">int</span> `$column`</span> )

<span class="type">bool</span> <span
class="methodname">nextRowset</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span class="methodname">rowCount</span> (
<span class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">setAttribute</span> ( <span class="methodparam"><span
class="type">int</span> `$attribute`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="type">bool</span> <span
class="methodname">setFetchMode</span> ( <span class="methodparam"><span
class="type">int</span> `$mode`</span> )

}

属性
----

`queryString`  
所用的查询字符串

PDOStatement::bindColumn
========================

绑定一列到一个 PHP 变量

### 说明

<span class="type">bool</span> <span
class="methodname">PDOStatement::bindColumn</span> ( <span
class="methodparam"><span class="type">mixed</span> `$column`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`&$param`</span> \[, <span class="methodparam"><span
class="type">int</span> `$type`</span> \[, <span
class="methodparam"><span class="type">int</span> `$maxlen`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$driverdata`</span> \]\]\] )

安排一个特定的变量绑定到一个查询结果集中给定的列。每次调用 <span
class="function">PDOStatement::fetch</span> 或 <span
class="function">PDOStatement::fetchAll</span>
都将更新所有绑定到列的变量。

> **Note**:
>
> 在语句执行前 PDO 有关列的信息并非总是可用，可移植的应用应在 <span
> class="function">PDOStatement::execute</span> *之后*
> 调用此函数（方法）。
>
> 但是，当使用 *PgSQL 驱动* 时，要想能绑定一个 LOB
> 列作为流，应用程序必须在调用 <span
> class="function">PDOStatement::execute</span> *之前*
> 调用此方法，否则大对象 OID 作为一个整数返回。

### 参数

`column`  
结果集中的列号（从1开始索引）或列名。如果使用列名，注意名称应该与由驱动返回的列名大小写保持一致。

`param`  
将绑定到列的 PHP 变量名称

`type`  
通过 PDO::PARAM\_\* 常量指定的参数的数据类型。

`maxlen`  
预分配提示。

`driverdata`  
驱动的可选参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 把结果集输出绑定到 PHP 变量**

绑定结果集中的列到PHP变量是一种使每行包含的数据在应用程序中立即可用的有效方法。下面的例子演示了
PDO 怎样用多种选项和缺省值绑定和检索列。

``` php
<?php
function readData($dbh) {
  $sql = 'SELECT name, colour, calories FROM fruit';
  try {
    $stmt = $dbh->prepare($sql);
    $stmt->execute();

    /*  通过列号绑定  */
    $stmt->bindColumn(1, $name);
    $stmt->bindColumn(2, $colour);
    
    /*  通过列名绑定  */
    $stmt->bindColumn('calories', $cals);

    while ($row = $stmt->fetch(PDO::FETCH_BOUND)) {
      $data = $name . "\t" . $colour . "\t" . $cals . "\n";
      print $data;
    }
  }
  catch (PDOException $e) {
    print $e->getMessage();
  }
}
readData($dbh);
?>
```

以上例程会输出：

    apple   red     150
    banana  yellow  175
    kiwi    green   75
    orange  orange  150
    mango   red     200
    strawberry      red     25

### 参见

-   <span class="function">PDOStatement::execute</span>
-   <span class="function">PDOStatement::fetch</span>
-   <span class="function">PDOStatement::fetchAll</span>
-   <span class="function">PDOStatement::fetchColumn</span>

PDOStatement::bindParam
=======================

绑定一个参数到指定的变量名

### 说明

<span class="type">bool</span> <span
class="methodname">PDOStatement::bindParam</span> ( <span
class="methodparam"><span class="type">mixed</span> `$parameter`</span>
, <span class="methodparam"><span class="type">mixed</span>
`&$variable`</span> \[, <span class="methodparam"><span
class="type">int</span> `$data_type`<span class="initializer"> =
PDO::PARAM\_STR</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$length`</span> \[, <span
class="methodparam"><span class="type">mixed</span>
`$driver_options`</span> \]\]\] )

绑定一个PHP变量到用作预处理的SQL语句中的对应命名占位符或问号占位符。
不同于 <span class="function">PDOStatement::bindValue</span>
，此变量作为引用被绑定，并只在 <span
class="function">PDOStatement::execute</span> 被调用的时候才取其值。

大多数参数是输入参数，即，参数以只读的方式用来建立查询。一些驱动支持调用存储过程并作为输出参数返回数据，一些支持作为输入/输出参数，既发送数据又接收更新后的数据。

### 参数

`parameter`  
参数标识符。对于使用命名占位符的预处理语句，应是类似 `:name`
形式的参数名。对于使用问号占位符的预处理语句，应是以1开始索引的参数位置。

`variable`  
绑定到 SQL 语句参数的 PHP 变量名。

`data_type`  
使用 PDO::PARAM\_\* 常量明确地指定参数的类型。要从一个存储过程中返回一个
INOUT 参数，需要为 `data_type` 参数使用按位或操作符去设置
PDO::PARAM\_INPUT\_OUTPUT 位。

`length`  
数据类型的长度。为表明参数是一个存储过程的 OUT
参数，必须明确地设置此长度。

`driver_options`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 执行一条使用命名占位符的预处理语句**

``` php
<?php
/* 通过绑定的 PHP 变量执行一条预处理语句  */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < :calories AND colour = :colour');
$sth->bindParam(':calories', $calories, PDO::PARAM_INT);
$sth->bindParam(':colour', $colour, PDO::PARAM_STR, 12);
$sth->execute();
?>
```

**示例 \#2 执行一条使用问号占位符的预处理语句**

``` php
<?php
/*  通过绑定的 PHP 变量执行一条预处理语句 */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < ? AND colour = ?');
$sth->bindParam(1, $calories, PDO::PARAM_INT);
$sth->bindParam(2, $colour, PDO::PARAM_STR, 12);
$sth->execute();
?>
```

**示例 \#3 使用 INOUT 参数调用一个存储过程**

``` php
<?php
/* 使用 INOUT 参数调用一个存储过程 */
$colour = 'red';
$sth = $dbh->prepare('CALL puree_fruit(?)');
$sth->bindParam(1, $colour, PDO::PARAM_STR|PDO::PARAM_INPUT_OUTPUT, 12);
$sth->execute();
print("After pureeing fruit, the colour is: $colour");
?>
```

### 参见

-   <span class="function">PDO::prepare</span>
-   <span class="function">PDOStatement::execute</span>
-   <span class="function">PDOStatement::bindValue</span>

PDOStatement::bindValue
=======================

把一个值绑定到一个参数

### 说明

<span class="type">bool</span> <span
class="methodname">PDOStatement::bindValue</span> ( <span
class="methodparam"><span class="type">mixed</span> `$parameter`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$data_type`<span class="initializer"> =
PDO::PARAM\_STR</span></span> \] )

绑定一个值到用作预处理的 SQL 语句中的对应命名占位符或问号占位符。

### 参数

`parameter`  
参数标识符。对于使用命名占位符的预处理语句，应是类似 `:name`
形式的参数名。对于使用问号占位符的预处理语句，应是以1开始索引的参数位置。

`value`  
绑定到参数的值

`data_type`  
使用 PDO::PARAM\_\* 常量明确地指定参数的类型。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 执行一条使用命名占位符的预处理语句**

``` php
<?php
/* 通过绑定的 PHP 变量执行一条预处理语句 */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < :calories AND colour = :colour');
$sth->bindValue(':calories', $calories, PDO::PARAM_INT);
$sth->bindValue(':colour', $colour, PDO::PARAM_STR);
$sth->execute();
?>
```

**示例 \#2 执行一条使用问号占位符的预处理语句**

``` php
<?php
/* 通过绑定的 PHP 变量执行一条预处理语句 */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < ? AND colour = ?');
$sth->bindValue(1, $calories, PDO::PARAM_INT);
$sth->bindValue(2, $colour, PDO::PARAM_STR);
$sth->execute();
?>
```

### 参见

-   <span class="function">PDO::prepare</span>
-   <span class="function">PDOStatement::execute</span>
-   <span class="function">PDOStatement::bindParam</span>

PDOStatement::closeCursor
=========================

关闭游标，使语句能再次被执行。

### 说明

<span class="type">bool</span> <span
class="methodname">PDOStatement::closeCursor</span> ( <span
class="methodparam">void</span> )

<span class="function">PDOStatement::closeCursor</span>
释放到数据库服务的连接，以便发出其他 SQL
语句，但使语句处于一个可以被再次执行的状态。

当上一个执行的 PDOStatement
对象仍有未取行时，此方法对那些不支持再执行一个 PDOStatement
对象的数据库驱动非常有用。
如果数据库驱动受此限制，则可能出现失序错误的问题。

<span class="function">PDOStatement::closeCursor</span>
要么是一个可选驱动的特有方法（效率最高）来实现，要么是在没有驱动特定的功能时作为一般的PDO
备用来实现。一般的备用语义上与下面的 PHP 代码相同：

``` php
<?php
do {
    while ($stmt->fetch())
        ;
    if (!$stmt->nextRowset())
        break;
} while (true);
?>
```

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 一个 <span class="function">PDOStatement::closeCursor</span>
的例子**

在下面例子中，`$stmt` PDOStatement
对象返回多行，但应用程序只取第一行，让 PDOStatement
对象处于一个有未取行的状态。为确保应用程序对所有数据库驱动都能正常运行，在执行
`$otherStmt` PDOStatement 对象前，`$stmt` 调用一次
PDOStatement::closeCursor() 。

``` php
<?php
/* 创建一个 PDOStatement 对象 */
$stmt = $dbh->prepare('SELECT foo FROM bar');

/* 创建第二个 PDOStatement 对象 */
$otherStmt = $dbh->prepare('SELECT foobaz FROM foobar');

/* 执行第一条语句 */
$stmt->execute();

/*  从结果集中只取出第一行 */
$stmt->fetch();

/* The following call to closeCursor() may be required by some drivers */
$stmt->closeCursor();

/*  现在可以执行第二条语句了 */
$otherStmt->execute();
?>
```

### 参见

-   <span class="function">PDOStatement::execute</span>

PDOStatement::columnCount
=========================

返回结果集中的列数

### 说明

<span class="type">int</span> <span
class="methodname">PDOStatement::columnCount</span> ( <span
class="methodparam">void</span> )

使用 <span class="function">PDOStatement::columnCount</span> 返回由
PDOStatement 对象代表的结果集中的列数。

如果是由 <span class="function">PDO::query</span> 返回的 PDOStatement
对象，则列数计算立即可用。

如果是由 <span class="function">PDO::prepare</span> 返回的 PDOStatement
对象，则在调用 <span class="function">PDOStatement::execute</span>
之前都不能准确地计算出列数。

### 返回值

返回由 PDOStatement 对象代表的结果集中的列数。如果没有结果集，则 <span
class="function">PDOStatement::columnCount</span> 返回 *0*。

### 范例

**示例 \#1 计算列数**

下面例子演示如何使用 <span
class="function">PDOStatement::columnCount</span>
操作一个结果集和一个空集。

``` php
<?php
$dbh = new PDO('odbc:sample', 'db2inst1', 'ibmdb2');

$sth = $dbh->prepare("SELECT name, colour FROM fruit");

/*  计算一个（不存在）的结果集中的列数 */
$colcount = $sth->columnCount();
print("Before execute(), result set has $colcount columns (should be 0)\n");

$sth->execute();

/* 计算结果集中的列数 */
$colcount = $sth->columnCount();
print("After execute(), result set has $colcount columns (should be 2)\n");

?>
```

以上例程会输出：

    Before execute(), result set has 0 columns (should be 0)
    After execute(), result set has 2 columns (should be 2)

### 参见

-   <span class="function">PDO::prepare</span>
-   <span class="function">PDOStatement::execute</span>
-   <span class="function">PDOStatement::rowCount</span>

PDOStatement::debugDumpParams
=============================

打印一条 SQL 预处理命令

### 说明

<span class="type">bool</span> <span
class="methodname">PDOStatement::debugDumpParams</span> ( <span
class="methodparam">void</span> )

直接打印出一条预处理语句包含的信息。提供正在使用的 *SQL*
查询、所用参数（*Params*）的数目、参数的清单、参数名、用一个整数表示的参数类型（*paramtype*）、键名或位置、值、以及在查询中的位置（如果当前
POD 驱动不支持，则为-1）。

此为一个用于调试的功能，在正常输出的情况下直接输出数据。

**小贴士**

和直接将结果输出到浏览器一样，可使用<a href="/book/outcontrol.html" class="link">输出控制函数</a>来捕获当前函数的输出，然后(例如)保存到一个
<span class="type">string</span> 中。

只打印此时此刻语句中的参数。额外的参数不存储在语句中，也就不会被输出。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">PDOStatement::debugDumpParams</span>
使用命名参数的例子**

``` php
<?php
/* 通过绑定 PHP 变量执行一条预处理语句 */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < :calories AND colour = :colour');
$sth->bindParam(':calories', $calories, PDO::PARAM_INT);
$sth->bindValue(':colour', $colour, PDO::PARAM_STR, 12);
$sth->execute();

$sth->debugDumpParams();

?>
```

以上例程会输出：

    SQL: [96] SELECT name, colour, calories
        FROM fruit
        WHERE calories < :calories AND colour = :colour
    Params:  2
    Key: Name: [9] :calories
    paramno=-1
    name=[9] ":calories"
    is_param=1
    param_type=1
    Key: Name: [7] :colour
    paramno=-1
    name=[7] ":colour"
    is_param=1
    param_type=2

**示例 \#2 <span class="function">PDOStatement::debugDumpParams</span>
使用未命名参数的例子**

``` php
<?php

/* 通过绑定 PHP 变量执行一条预处理语句 */
$calories = 150;
$colour = 'red';
$name = 'apple';

$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < ? AND colour = ?');
$sth->bindParam(1, $calories, PDO::PARAM_INT);
$sth->bindValue(2, $colour, PDO::PARAM_STR);
$sth->execute();

$sth->debugDumpParams();

?>
```

以上例程会输出：

    SQL: [82] SELECT name, colour, calories
        FROM fruit
        WHERE calories < ? AND colour = ?
    Params:  2
    Key: Position #0:
    paramno=0
    name=[0] ""
    is_param=1
    param_type=1
    Key: Position #1:
    paramno=1
    name=[0] ""
    is_param=1
    param_type=2

### 参见

-   <span class="function">PDO::prepare</span>
-   <span class="function">PDOStatement::bindParam</span>
-   <span class="function">PDOStatement::bindValue</span>

PDOStatement::errorCode
=======================

获取跟上一次语句句柄操作相关的 SQLSTATE

### 说明

<span class="type">string</span> <span
class="methodname">PDOStatement::errorCode</span> ( <span
class="methodparam">void</span> )

### 返回值

与 <span class="function">PDO::errorCode</span> 相同，只是 <span
class="function">PDOStatement::errorCode</span> 只取回 PDOStatement
对象执行操作中的错误码。

### 范例

**示例 \#1 取回一个 SQLSTATE 码**

``` php
<?php
/* 引发一个错误 --  BONES 数据表不存在 */
$err = $dbh->prepare('SELECT skull FROM bones');
$err->execute();

echo "\nPDOStatement::errorCode(): ";
print $err->errorCode();
?>
```

以上例程会输出：

    PDOStatement::errorCode(): 42S02

### 参见

-   <span class="function">PDO::errorCode</span>
-   <span class="function">PDO::errorInfo</span>
-   <span class="function">PDOStatement::errorInfo</span>

PDOStatement::errorInfo
=======================

获取跟上一次语句句柄操作相关的扩展错误信息

### 说明

<span class="type">array</span> <span
class="methodname">PDOStatement::errorInfo</span> ( <span
class="methodparam">void</span> )

### 返回值

<span class="function">PDOStatement::errorInfo</span>
返回一个关于上一次语句句柄执行操作的错误信息的数组
。该数组包含下列字段：

| Element | Information                                                                  |
|---------|------------------------------------------------------------------------------|
| 0       | SQLSTATE 错误码（一个由5个字母或数字组成的在 ANSI SQL 标准中定义的标识符）。 |
| 1       | 具体驱动错误码。                                                             |
| 2       | 具体驱动错误信息。                                                           |

### 范例

**示例 \#1 显示连接到DB2数据库的 PDO\_ODBC 连接的 errorInfo() 的字段**

``` php
<?php
/* 激发一个错误 --  BONES 数据表不存在 */
$sth = $dbh->prepare('SELECT skull FROM bones');
$sth->execute();

echo "\nPDOStatement::errorInfo():\n";
$arr = $sth->errorInfo();
print_r($arr);
?>
```

以上例程会输出：

    PDOStatement::errorInfo():
    Array
    (
        [0] => 42S02
        [1] => -204
        [2] => [IBM][CLI Driver][DB2/LINUX] SQL0204N  "DANIELS.BONES" is an undefined name.  SQLSTATE=42704
    )

### 参见

-   <span class="function">PDO::errorCode</span>
-   <span class="function">PDO::errorInfo</span>
-   <span class="function">PDOStatement::errorCode</span>

PDOStatement::execute
=====================

执行一条预处理语句

### 说明

<span class="type">bool</span> <span
class="methodname">PDOStatement::execute</span> (\[ <span
class="methodparam"><span class="type">array</span>
`$input_parameters`</span> \] )

执行预处理过的语句。如果预处理过的语句含有参数标记，必须选择下面其中一种做法：

-   调用 <span class="function">PDOStatement::bindParam</span> 绑定 PHP
    变量到参数标记：如果有的话，通过关联参数标记绑定的变量来传递输入值和取得输出值

-   或传递一个只作为输入参数值的数组

### 参数

`input_parameters`  
一个元素个数和将被执行的 SQL 语句中绑定的参数一样多的数组。所有的值作为
**`PDO::PARAM_STR`** 对待。

不能绑定多个值到一个单独的参数；比如，不能绑定两个值到
IN（）子句中一个单独的命名参数。

绑定的值不能超过指定的个数。如果在 `input_parameters` 中存在比 <span
class="methodname">PDO::prepare</span> 预处理的SQL
指定的多的键名，则此语句将会失败并发出一个错误。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                           |
|-------|--------------------------------------------------------------------------------|
| 5.2.0 | `input_parameters` 中的键名必须和 SQL 中声明的相匹配。PHP 5.2.0 之前默认忽略。 |

### 范例

**示例 \#1 执行一条绑定变量的预处理语句**

``` php
<?php
/*  通过绑定 PHP 变量执行一条预处理语句 */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < :calories AND colour = :colour');
$sth->bindParam(':calories', $calories, PDO::PARAM_INT);
$sth->bindParam(':colour', $colour, PDO::PARAM_STR, 12);
$sth->execute();
?>
```

**示例 \#2 使用一个含有插入值的数组执行一条预处理语句（命名参数）**

``` php
<?php
/* 通过传递一个含有插入值的数组执行一条预处理语句 */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < :calories AND colour = :colour');
$sth->execute(array(':calories' => $calories, ':colour' => $colour));
?>
```

**示例 \#3 使用一个含有插入值的数组执行一条预处理语句（占位符）**

``` php
<?php
/*  通过传递一个插入值的数组执行一条预处理语句 */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < ? AND colour = ?');
$sth->execute(array($calories, $colour));
?>
```

**示例 \#4 执行一条问号占位符的预处理语句**

``` php
<?php
/* 通过绑定 PHP 变量执行一条预处理语句 */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < ? AND colour = ?');
$sth->bindParam(1, $calories, PDO::PARAM_INT);
$sth->bindParam(2, $colour, PDO::PARAM_STR, 12);
$sth->execute();
?>
```

**示例 \#5 使用数组执行一条含有 IN 子句的预处理语句**

``` php
<?php
/*  使用一个数组的值执行一条含有 IN 子句的预处理语句 */
$params = array(1, 21, 63, 171);
/*  创建一个填充了和params相同数量占位符的字符串 */
$place_holders = implode(',', array_fill(0, count($params), '?'));

/*
    对于 $params 数组中的每个值，要预处理的语句包含足够的未命名占位符 。
    语句被执行时， $params 数组中的值被绑定到预处理语句中的占位符。
    这和使用 PDOStatement::bindParam() 不一样，因为它需要一个引用变量。
    PDOStatement::execute() 仅作为通过值绑定的替代。
*/
$sth = $dbh->prepare("SELECT id, name FROM contacts WHERE id IN ($place_holders)");
$sth->execute($params);
?>
```

### 注释

> **Note**:
>
> 有些驱动在执行下一条语句前需要
> <a href="/book/pdo.html#PDOStatement::closeCursor" class="link">关闭游标</a>
> 。

### 参见

-   <span class="function">PDO::prepare</span>
-   <span class="function">PDOStatement::bindParam</span>
-   <span class="function">PDOStatement::fetch</span>
-   <span class="function">PDOStatement::fetchAll</span>
-   <span class="function">PDOStatement::fetchColumn</span>

PDOStatement::fetch
===================

从结果集中获取下一行

### 说明

<span class="type">mixed</span> <span
class="methodname">PDOStatement::fetch</span> (\[ <span
class="methodparam"><span class="type">int</span> `$fetch_style`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$cursor_orientation`<span class="initializer"> =
PDO::FETCH\_ORI\_NEXT</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$cursor_offset`<span class="initializer"> =
0</span></span> \]\]\] )

从一个 PDOStatement 对象相关的结果集中获取下一行。`fetch_style` 参数决定
POD 如何返回行。

### 参数

`fetch_style`  
控制下一行如何返回给调用者。此值必须是 *PDO::FETCH\_\**
系列常量中的一个，缺省为 *PDO::ATTR\_DEFAULT\_FETCH\_MODE* 的值 （默认为
*PDO::FETCH\_BOTH* ）。

-   *PDO::FETCH\_ASSOC*：返回一个索引为结果集列名的数组

-   *PDO::FETCH\_BOTH*（默认）：返回一个索引为结果集列名和以0开始的列号的数组

-   *PDO::FETCH\_BOUND*：返回 **`TRUE`** ，并分配结果集中的列值给 <span
    class="function">PDOStatement::bindColumn</span> 方法绑定的 PHP
    变量。

-   *PDO::FETCH\_CLASS*：返回一个请求类的新实例，映射结果集中的列名到类中对应的属性名。如果
    `fetch_style` 包含 PDO::FETCH\_CLASSTYPE（例如：*PDO::FETCH\_CLASS
    \| PDO::FETCH\_CLASSTYPE*），则类名由第一列的值决定

-   *PDO::FETCH\_INTO*：更新一个被请求类已存在的实例，映射结果集中的列到类中命名的属性

-   *PDO::FETCH\_LAZY*：结合使用 *PDO::FETCH\_BOTH* 和
    *PDO::FETCH\_OBJ*，创建供用来访问的对象变量名

-   *PDO::FETCH\_NUM*：返回一个索引为以0开始的结果集列号的数组

-   *PDO::FETCH\_OBJ*：返回一个属性名对应结果集列名的匿名对象

`cursor_orientation`  
对于 一个 PDOStatement
对象表示的可滚动游标，该值决定了哪一行将被返回给调用者。此值必须是
*PDO::FETCH\_ORI\_\** 系列常量中的一个，默认为
*PDO::FETCH\_ORI\_NEXT*。要想让 PDOStatement
对象使用可滚动游标，必须在用 <span class="function">PDO::prepare</span>
预处理SQL语句时，设置 *PDO::ATTR\_CURSOR* 属性为 *PDO::CURSOR\_SCROLL*。

`offset`  
对于一个 *cursor\_orientation* 参数设置为 *PDO::FETCH\_ORI\_ABS*
的PDOStatement
对象代表的可滚动游标，此值指定结果集中想要获取行的绝对行号。

对于一个 *cursor\_orientation* 参数设置为 *PDO::FETCH\_ORI\_REL*
的PDOStatement 对象代表的可滚动游标，此值指定想要获取行相对于调用 <span
class="function">PDOStatement::fetch</span> 前游标的位置

### 返回值

此函数（方法）成功时返回的值依赖于提取类型。在所有情况下，失败都返回
**`FALSE`** 。

### 范例

**示例 \#1 使用不同的提取方式获取行**

``` php
<?php
$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

/* 运用 PDOStatement::fetch 风格 */
print("PDO::FETCH_ASSOC: ");
print("Return next row as an array indexed by column name\n");
$result = $sth->fetch(PDO::FETCH_ASSOC);
print_r($result);
print("\n");

print("PDO::FETCH_BOTH: ");
print("Return next row as an array indexed by both column name and number\n");
$result = $sth->fetch(PDO::FETCH_BOTH);
print_r($result);
print("\n");

print("PDO::FETCH_LAZY: ");
print("Return next row as an anonymous object with column names as properties\n");
$result = $sth->fetch(PDO::FETCH_LAZY);
print_r($result);
print("\n");

print("PDO::FETCH_OBJ: ");
print("Return next row as an anonymous object with column names as properties\n");
$result = $sth->fetch(PDO::FETCH_OBJ);
print $result->NAME;
print("\n");
?>
```

以上例程会输出：

    PDO::FETCH_ASSOC: Return next row as an array indexed by column name
    Array
    (
        [NAME] => apple
        [COLOUR] => red
    )

    PDO::FETCH_BOTH: Return next row as an array indexed by both column name and number
    Array
    (
        [NAME] => banana
        [0] => banana
        [COLOUR] => yellow
        [1] => yellow
    )

    PDO::FETCH_LAZY: Return next row as an anonymous object with column names as properties
    PDORow Object
    (
        [NAME] => orange
        [COLOUR] => orange
    )

    PDO::FETCH_OBJ: Return next row as an anonymous object with column names as properties
    kiwi

**示例 \#2 使用一个可滚动游标获取行**

``` php
<?php
function readDataForwards($dbh) {
  $sql = 'SELECT hand, won, bet FROM mynumbers ORDER BY BET';
  try {
    $stmt = $dbh->prepare($sql, array(PDO::ATTR_CURSOR => PDO::CURSOR_SCROLL));
    $stmt->execute();
    while ($row = $stmt->fetch(PDO::FETCH_NUM, PDO::FETCH_ORI_NEXT)) {
      $data = $row[0] . "\t" . $row[1] . "\t" . $row[2] . "\n";
      print $data;
    }
    $stmt = null;
  }
  catch (PDOException $e) {
    print $e->getMessage();
  }
}
function readDataBackwards($dbh) {
  $sql = 'SELECT hand, won, bet FROM mynumbers ORDER BY bet';
  try {
    $stmt = $dbh->prepare($sql, array(PDO::ATTR_CURSOR => PDO::CURSOR_SCROLL));
    $stmt->execute();
    $row = $stmt->fetch(PDO::FETCH_NUM, PDO::FETCH_ORI_LAST);
    do {
      $data = $row[0] . "\t" . $row[1] . "\t" . $row[2] . "\n";
      print $data;
    } while ($row = $stmt->fetch(PDO::FETCH_NUM, PDO::FETCH_ORI_PRIOR));
    $stmt = null;
  }
  catch (PDOException $e) {
    print $e->getMessage();
  }
}

print "Reading forwards:\n";
readDataForwards($conn);

print "Reading backwards:\n";
readDataBackwards($conn);
?>
```

以上例程会输出：

    Reading forwards:
    21    10    5
    16    0     5
    19    20    10

    Reading backwards:
    19    20    10
    16    0     5
    21    10    5

### 参见

-   <span class="function">PDO::prepare</span>
-   <span class="function">PDOStatement::execute</span>
-   <span class="function">PDOStatement::fetchAll</span>
-   <span class="function">PDOStatement::fetchColumn</span>
-   <span class="function">PDOStatement::fetchObject</span>
-   <span class="function">PDOStatement::setFetchMode</span>

PDOStatement::fetchAll
======================

返回一个包含结果集中所有行的数组

### 说明

<span class="type">array</span> <span
class="methodname">PDOStatement::fetchAll</span> (\[ <span
class="methodparam"><span class="type">int</span> `$fetch_style`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$fetch_argument`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ctor_args`<span class="initializer"> =
array()</span></span> \]\]\] )

### 参数

`fetch_style`  
控制返回数组的内容如同 <span class="function">PDOStatement::fetch</span>
文档中记载的一样。默认为 **`PDO::ATTR_DEFAULT_FETCH_MODE`** 的值（
其缺省值为 **`PDO::FETCH_BOTH`** ）

想要返回一个包含结果集中单独一列所有值的数组，需要指定
**`PDO::FETCH_COLUMN`** 。通过指定 `column-index` 参数获取想要的列。

想要获取结果集中单独一列的唯一值，需要将 **`PDO::FETCH_COLUMN`** 和
**`PDO::FETCH_UNIQUE`** 按位或。

想要返回一个根据指定列把值分组后的关联数组，需要将
**`PDO::FETCH_COLUMN`** 和 **`PDO::FETCH_GROUP`** 按位或。

`fetch_argument`  
根据 `fetch_style` 参数的值，此参数有不同的意义：

-   **`PDO::FETCH_COLUMN`**：返回指定以0开始索引的列。

-   **`PDO::FETCH_CLASS`**：返回指定类的实例，映射每行的列到类中对应的属性名。

-   **`PDO::FETCH_FUNC`**：将每行的列作为参数传递给指定的函数，并返回调用函数后的结果。

`ctor_args`  
当 `fetch_style` 参数为 **`PDO::FETCH_CLASS`**
时，自定义类的构造函数的参数。

### 返回值

<span class="function">PDOStatement::fetchAll</span>
返回一个包含结果集中所有剩余行的数组。此数组的每一行要么是一个列值的数组，要么是属性对应每个列名的一个对象。

使用此方法获取大结果集将导致系统负担加重且可能占用大量网络资源。与其取回所有数据后用PHP来操作，倒不如考虑使用数据库服务来处理结果集。例如，在取回数据并通过PHP处理前，在
SQL 中使用 WHERE 和 ORDER BY 子句来限定结果。

### 范例

**示例 \#1 获取结果集中所有剩余的行**

``` php
<?php
$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

/* 获取结果集中所有剩余的行 */
print("Fetch all of the remaining rows in the result set:\n");
$result = $sth->fetchAll();
print_r($result);
?>
```

以上例程的输出类似于：

    Fetch all of the remaining rows in the result set:
    Array
    (
        [0] => Array
            (
                [NAME] => pear
                [0] => pear
                [COLOUR] => green
                [1] => green
            )

        [1] => Array
            (
                [NAME] => watermelon
                [0] => watermelon
                [COLOUR] => pink
                [1] => pink
            )

    )

**示例 \#2 获取结果集中单独一列的所有值**

下面例子演示了如何从一个结果集中返回单独一列所有的值，尽管 SQL
语句自身可能返回每行多列。

``` php
<?php
$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

/* 获取第一列所有值 */
$result = $sth->fetchAll(PDO::FETCH_COLUMN, 0);
var_dump($result);
?>
```

以上例程的输出类似于：

    Array(3)
    (
        [0] =>
        string(5) => apple
        [1] =>
        string(4) => pear
        [2] =>
        string(10) => watermelon
    )

**示例 \#3 根据单独的一列把所有值分组**

下面例子演示了如何返回一个根据结果集中指定列的值分组的关联数组。该数组包含三个键：返回的
*apple* 和 *pear* 数组包含了两种不同的颜色，而返回的 *watermelon*
数组仅包含一种颜色。

``` php
<?php
$insert = $dbh->prepare("INSERT INTO fruit(name, colour) VALUES (?, ?)");
$insert->execute(array('apple', 'green'));
$insert->execute(array('pear', 'yellow'));

$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

/* 根据第一列分组  */
var_dump($sth->fetchAll(PDO::FETCH_COLUMN|PDO::FETCH_GROUP));
?>
```

以上例程的输出类似于：

    array(3) {
      ["apple"]=>
      array(2) {
        [0]=>
        string(5) "green"
        [1]=>
        string(3) "red"
      }
      ["pear"]=>
      array(2) {
        [0]=>
        string(5) "green"
        [1]=>
        string(6) "yellow"
      }
      ["watermelon"]=>
      array(1) {
        [0]=>
        string(5) "green"
      }
    }

**示例 \#4 每行结果实例化一个类**

下面列子演示了 **`PDO::FETCH_CLASS`** 获取风格的行为。

``` php
<?php
class fruit {
    public $name;
    public $colour;
}

$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

$result = $sth->fetchAll(PDO::FETCH_CLASS, "fruit");
var_dump($result);
?>
```

以上例程的输出类似于：

    array(3) {
      [0]=>
      object(fruit)#1 (2) {
        ["name"]=>
        string(5) "apple"
        ["colour"]=>
        string(5) "green"
      }
      [1]=>
      object(fruit)#2 (2) {
        ["name"]=>
        string(4) "pear"
        ["colour"]=>
        string(6) "yellow"
      }
      [2]=>
      object(fruit)#3 (2) {
        ["name"]=>
        string(10) "watermelon"
        ["colour"]=>
        string(4) "pink"
      }
    }

**示例 \#5 每行调用一次函数**

下面列子演示了 **`PDO::FETCH_FUNC`** 获取风格的行为。

``` php
<?php
function fruit($name, $colour) {
    return "{$name}: {$colour}";
}

$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

$result = $sth->fetchAll(PDO::FETCH_FUNC, "fruit");
var_dump($result);
?>
```

以上例程的输出类似于：

    array(3) {
      [0]=>
      string(12) "apple: green"
      [1]=>
      string(12) "pear: yellow"
      [2]=>
      string(16) "watermelon: pink"
    }

### 参见

-   <span class="function">PDO::query</span>
-   <span class="function">PDOStatement::fetch</span>
-   <span class="function">PDOStatement::fetchColumn</span>
-   <span class="function">PDO::prepare</span>
-   <span class="function">PDOStatement::setFetchMode</span>

PDOStatement::fetchColumn
=========================

从结果集中的下一行返回单独的一列。

### 说明

<span class="type">string</span> <span
class="methodname">PDOStatement::fetchColumn</span> (\[ <span
class="methodparam"><span class="type">int</span> `$column_number`<span
class="initializer"> = 0</span></span> \] )

从结果集中的下一行返回单独的一列，如果没有了，则返回 **`FALSE`** 。

### 参数

`column_number`  
你想从行里取回的列的索引数字（以0开始的索引）。如果没有提供值，则 <span
class="function">PDOStatement::fetchColumn</span> 获取第一列。

### 返回值

<span class="function">PDOStatement::fetchColumn</span>
从结果集中的下一行返回单独的一列。

**Warning**

如果使用 <span class="function">PDOStatement::fetchColumn</span>
取回数据，则没有办法返回同一行的另外一列。

### 范例

**示例 \#1 返回下一行的第一列**

``` php
<?php
$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

/* 从结果集中的下一行获取第一列  */
print("从结果集中的下一行获取第一列：\n");
$result = $sth->fetchColumn();
print("name = $result\n");

print("从结果集中的下一行获取第二列：\n");
$result = $sth->fetchColumn(1);
print("colour = $result\n");
?>
```

以上例程会输出：

    从结果集中的下一行获取第一列：
    name = lemon
    从结果集中的下一行获取第二列：
    colour = red

### 参见

-   <span class="function">PDO::query</span>
-   <span class="function">PDOStatement::fetch</span>
-   <span class="function">PDOStatement::fetchAll</span>
-   <span class="function">PDO::prepare</span>
-   <span class="function">PDOStatement::setFetchMode</span>

PDOStatement::fetchObject
=========================

获取下一行并作为一个对象返回。

### 说明

<span class="type">mixed</span> <span
class="methodname">PDOStatement::fetchObject</span> (\[ <span
class="methodparam"><span class="type">string</span> `$class_name`<span
class="initializer"> = "stdClass"</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$ctor_args`</span>
\]\] )

获取下一行并作为一个对象返回。此函数（方法）是使用
**`PDO::FETCH_CLASS`** 或 **`PDO::FETCH_OBJ`** 风格的 <span
class="function">PDOStatement::fetch</span> 的一种替代。

### 参数

`class_name`  
创建类的名称。

`ctor_args`  
此数组的元素被传递给构造函数。

### 返回值

返回一个属性名对应于列名的所要求类的实例， 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">PDOStatement::fetch</span>

PDOStatement::getAttribute
==========================

检索一个语句属性

### 说明

<span class="type">mixed</span> <span
class="methodname">PDOStatement::getAttribute</span> ( <span
class="methodparam"><span class="type">int</span> `$attribute`</span> )

得到语句的一个属性。当前，不存在通用的属性，只有驱动特定的属性：

-   *PDO::ATTR\_CURSOR\_NAME* （Firebird 和 ODBC 特性）： 获取 *UPDATE
    ... WHERE CURRENT OF* 的游标名称。

### 返回值

返回属性值。

### 参见

-   <span class="function">PDO::getAttribute</span>
-   <span class="function">PDO::setAttribute</span>
-   <span class="function">PDOStatement::setAttribute</span>

PDOStatement::getColumnMeta
===========================

返回结果集中一列的元数据

### 说明

<span class="type">array</span> <span
class="methodname">PDOStatement::getColumnMeta</span> ( <span
class="methodparam"><span class="type">int</span> `$column`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

检索一个在结果集中以0开始索引的列的元数据作为一个关联数组。

**Warning**

并非所有 PDO 驱动都支持 <span
class="function">PDOStatement::getColumnMeta</span>。

### 参数

`column`  
结果集中以0开始索引的列。

### 返回值

返回一个关联数组，它包含了下列表示一个单独列的元数据的值：

| 名称                | 值                                                                                                                                                 |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| *native\_type*      | 用于表示列值的 PHP 原生类型。                                                                                                                      |
| *driver:decl\_type* | 在数据库中用于表示列值的 SQL 类型。如果结果集中的列是一个函数的结果，则该值不能被 <span class="function">PDOStatement::getColumnMeta</span> 返回。 |
| *flags*             | 任何设置于此列的标记。                                                                                                                             |
| *name*              | 通过数据库返回的列名。                                                                                                                             |
| *table*             | 通过数据库返回的该列的表名                                                                                                                         |
| *len*               | 该列的长度。除浮点小数外通常为 *-1*                                                                                                                |
| *precision*         | 该列的数值精度。除浮点小数外通常为 *0* 。                                                                                                          |
| *pdo\_type*         | 以 *PDO::PARAM\_\** 常量为代表的列类型。                                                                                                           |

如果结果集不存在，或者是请求的列在结果集中不存在，则返回 **`FALSE`** 。

### 更新日志

| 版本  | 说明         |
|-------|--------------|
| 5.2.3 | *table* 字段 |

### 范例

**示例 \#1 检索列的元数据**

下面例子展示了在一个PDO\_SQLITE中，检索一个通过函数（COUNT）生成单独列的元数据的结果。

``` php
<?php
$select = $DB->query('SELECT COUNT(*) FROM fruit');
$meta = $select->getColumnMeta(0);
var_dump($meta);
?>
```

以上例程会输出：

    array(6) {
      ["native_type"]=>
      string(7) "integer"
      ["flags"]=>
      array(0) {
      }
      ["name"]=>
      string(8) "COUNT(*)"
      ["len"]=>
      int(-1)
      ["precision"]=>
      int(0)
      ["pdo_type"]=>
      int(2)
    }

### 参见

-   <span class="function">PDOStatement::columnCount</span>
-   <span class="function">PDOStatement::rowCount</span>

PDOStatement::nextRowset
========================

在一个多行集语句句柄中推进到下一个行集

### 说明

<span class="type">bool</span> <span
class="methodname">PDOStatement::nextRowset</span> ( <span
class="methodparam">void</span> )

一些数据库服务支持返回一个以上行集（也被称为结果集）的存储过程。<span
class="function">PDOStatement::nextRowset</span> 使你能够结合一个
PDOStatement
对象访问第二个以及后续的行集。上述的每个行集可以有不同的列集合。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 获取由一个存储过程返回的多个行集**

下面例子展示了怎样调用一个存储过程，返回三个行集的 MULTIPLE\_ROWSETS
。用一个 do / while 循环来循环调用 <span
class="function">PDOStatement::nextRowset</span> 方法，
当不再有行集返回时返回 false 并结束循环。

``` php
<?php
$sql = 'CALL multiple_rowsets()';
$stmt = $conn->query($sql);
$i = 1;
do {
    $rowset = $stmt->fetchAll(PDO::FETCH_NUM);
    if ($rowset) {
        printResultSet($rowset, $i);
    }
    $i++;
} while ($stmt->nextRowset());

function printResultSet(&$rowset, $i) {
    print "Result set $i:\n";
    foreach ($rowset as $row) {
        foreach ($row as $col) {
            print $col . "\t";
        }
        print "\n";
    }
    print "\n";
}
?>
```

以上例程会输出：

    Result set 1:
    apple    red
    banana   yellow

    Result set 2:
    orange   orange    150
    banana   yellow    175

    Result set 3:
    lime     green
    apple    red
    banana   yellow

### 参见

-   <span class="function">PDOStatement::columnCount</span>
-   <span class="function">PDOStatement::execute</span>
-   <span class="function">PDOStatement::getColumnMeta</span>
-   <span class="function">PDO::query</span>

PDOStatement::rowCount
======================

返回受上一个 SQL 语句影响的行数

### 说明

<span class="type">int</span> <span
class="methodname">PDOStatement::rowCount</span> ( <span
class="methodparam">void</span> )

<span class="function">PDOStatement::rowCount</span> 返回上一个由对应的
*PDOStatement* 对象执行DELETE、 INSERT、或 UPDATE 语句受影响的行数。

如果上一条由相关 *PDOStatement* 执行的 SQL 语句是一条 SELECT
语句，有些数据可能返回由此语句返回的行数。但这种方式不能保证对所有数据有效，且对于可移植的应用不应依赖于此方式。

### 返回值

返回行数。

### 范例

**示例 \#1 返回删除的行数**

<span class="function">PDOStatement::rowCount</span> 返回受
DELETE、INSERT、 或 UPDATE 语句影响的行数。

``` php
<?php
/*  从 FRUIT 数据表中删除所有行 */
$del = $dbh->prepare('DELETE FROM fruit');
$del->execute();

/*  返回被删除的行数 */
print("Return number of rows that were deleted:\n");
$count = $del->rowCount();
print("Deleted $count rows.\n");
?>
```

以上例程会输出：

    Return number of rows that were deleted:
    Deleted 9 rows.

**示例 \#2 计算由一个 SELECT 语句返回的行数**

对于大多数数据库，<span class="function">PDOStatement::rowCount</span>
不能返回受一条 SELECT 语句影响的行数。替代的方法是，使用 <span
class="function">PDO::query</span>
来发出一条和原打算中的SELECT语句有相同条件表达式的 SELECT COUNT(\*)
语句，然后用 <span class="function">PDOStatement::fetchColumn</span>
来取得返回的行数。这样应用程序才能正确执行。

``` php
<?php
$sql = "SELECT COUNT(*) FROM fruit WHERE calories > 100";
if ($res = $conn->query($sql)) {

    /* 检查符合 SELECT 语句的行数 */
  if ($res->fetchColumn() > 0) {

        /* 发出一条真正的 SELECT 语句并操作返回的结果 */
         $sql = "SELECT name FROM fruit WHERE calories > 100";
       foreach ($conn->query($sql) as $row) {
           print "Name: " .  $row['NAME'] . "\n";
         }
    }
    /* 没有匹配的行 -- 执行其他 */
  else {
      print "No rows matched the query.";
    }
}

$res = null;
$conn = null;
?>
```

以上例程会输出：

    apple
    banana
    orange
    pear

### 参见

-   <span class="function">PDOStatement::columnCount</span>
-   <span class="function">PDOStatement::fetchColumn</span>
-   <span class="function">PDO::query</span>

PDOStatement::setAttribute
==========================

设置一个语句属性

### 说明

<span class="type">bool</span> <span
class="methodname">PDOStatement::setAttribute</span> ( <span
class="methodparam"><span class="type">int</span> `$attribute`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

给语句设置一个属性。当前，没有通用的属性可以设置，只有驱动特定的属性：

-   *PDO::ATTR\_CURSOR\_NAME* （Firebird 和 ODBC 特性）： 为 *UPDATE ...
    WHERE CURRENT OF* 设置游标名称。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">PDO::getAttribute</span>
-   <span class="function">PDO::setAttribute</span>
-   <span class="function">PDOStatement::getAttribute</span>

PDOStatement::setFetchMode
==========================

为语句设置默认的获取模式。

### 说明

<span class="type">bool</span> <span
class="methodname">PDOStatement::setFetchMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

<span class="type">bool</span> <span
class="methodname">PDOStatement::setFetchMode</span> ( <span
class="methodparam"><span class="type">int</span>
`$PDO::FETCH_COLUMN`</span> , <span class="methodparam"><span
class="type">int</span> `$colno`</span> )

<span class="type">bool</span> <span
class="methodname">PDOStatement::setFetchMode</span> ( <span
class="methodparam"><span class="type">int</span>
`$PDO::FETCH_CLASS`</span> , <span class="methodparam"><span
class="type">string</span> `$classname`</span> , <span
class="methodparam"><span class="type">array</span> `$ctorargs`</span> )

<span class="type">bool</span> <span
class="methodname">PDOStatement::setFetchMode</span> ( <span
class="methodparam"><span class="type">int</span>
`$PDO::FETCH_INTO`</span> , <span class="methodparam"><span
class="type">object</span> `$object`</span> )

### 参数

`mode`  
获取模式必须是 *PDO::FETCH\_\** 系列常量中的一个。

`colno`  
列号。

`classname`  
类名。

`ctorargs`  
构造函数参数。

`object`  
对象。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 设置获取模式**

The following example demonstrates how <span
class="function">PDOStatement::setFetchMode</span> changes the default
fetch mode for a PDOStatement object.下面的例子示范如何用 <span
class="function">PDOStatement::setFetchMode</span> 来为一个 PDOStatement
对象更改默认的获取模式。

``` php
<?php
$sql = 'SELECT name, colour, calories FROM fruit';
try {
  $stmt = $dbh->query($sql);
  $result = $stmt->setFetchMode(PDO::FETCH_NUM);
  while ($row = $stmt->fetch()) {
    print $row[0] . "\t" . $row[1] . "\t" . $row[2] . "\n";
  }
}
catch (PDOException $e) {
  print $e->getMessage();
}
?>
```

以上例程会输出：

    apple   red     150
    banana  yellow  250
    orange  orange  300
    kiwi    brown   75
    lemon   yellow  25
    pear    green   150
    watermelon      pink    90

简介
----

代表一个由 PDO 产生的错误。在自己的代码不应抛出一个 <span
class="classname">PDOException</span> 异常。关于 PHP
异常的更多信息请参见
<a href="/language/exceptions.html" class="link">异常</a> 。

类摘要
------

**PDOException**

<span class="ooclass"> class **PDOException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**RuntimeException** </span> {

/\* 属性 \*/

<span class="modifier">public</span> <span class="type">array</span>
`$errorInfo` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$code` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

属性
----

`errorInfo`  
相当于<span class="function">PDO::errorInfo</span> 或 <span
class="function">PDOStatement::errorInfo</span>

`message`  
文本错误信息。用 <span class="function">Exception::getMessage</span>
来访问。

`code`  
*SQLSTATE* 错误码。用<span class="function">Exception::getCode</span>
来访问。

PDO 驱动
========

**目录**

-   [CUBRID (PDO)](/book/pdo.html#CUBRID%20(PDO)) — CUBRID Functions
    (PDO\_CUBRID)
    -   [PDO\_CUBRID DSN](/book/pdo.html#PDO_CUBRID%20DSN) — Connecting
        to CUBRID databases
    -   [PDO::cubrid\_schema](/book/pdo.html#PDO::cubrid_schema) — Get
        the requested schema information
-   [MS SQL Server (PDO)](/book/pdo.html#MS%20SQL%20Server%20(PDO)) —
    Microsoft SQL Server and Sybase Functions (PDO\_DBLIB)
    -   [PDO\_DBLIB DSN](/book/pdo.html#PDO_DBLIB%20DSN) — Connecting to
        Microsoft SQL Server and Sybase databases
-   [Firebird (PDO)](/book/pdo.html#Firebird%20(PDO)) — Firebird
    Functions (PDO\_FIREBIRD)
    -   [PDO\_FIREBIRD DSN](/book/pdo.html#PDO_FIREBIRD%20DSN) —
        Connecting to Firebird databases
-   [IBM (PDO)](/book/pdo.html#IBM%20(PDO)) — IBM Functions (PDO\_IBM)
    -   [PDO\_IBM DSN](/book/pdo.html#PDO_IBM%20DSN) — Connecting to IBM
        databases
-   [Informix (PDO)](/book/pdo.html#Informix%20(PDO)) — Informix
    Functions (PDO\_INFORMIX)
    -   [PDO\_INFORMIX DSN](/book/pdo.html#PDO_INFORMIX%20DSN) —
        Connecting to Informix databases
-   [MySQL (PDO)](/book/pdo.html#MySQL%20(PDO)) — MySQL Functions
    (PDO\_MYSQL)
    -   [PDO\_MYSQL DSN](/book/pdo.html#PDO_MYSQL%20DSN) — Connecting to
        MySQL databases
-   [MS SQL Server (PDO)](/book/pdo.html#MS%20SQL%20Server%20(PDO)) —
    Microsoft SQL Server Functions (PDO\_SQLSRV)
    -   [PDO\_SQLSRV DSN](/book/pdo.html#PDO_SQLSRV%20DSN) — Connecting
        to MS SQL Server and SQL Azure databases
-   [Oracle (PDO)](/book/pdo.html#Oracle%20(PDO)) — Oracle Functions
    (PDO\_OCI)
    -   [PDO\_OCI DSN](/book/pdo.html#PDO_OCI%20DSN) — Connecting to
        Oracle databases
-   [ODBC and DB2 (PDO)](/book/pdo.html#ODBC%20and%20DB2%20(PDO)) — ODBC
    and DB2 Functions (PDO\_ODBC)
    -   [PDO\_ODBC DSN](/book/pdo.html#PDO_ODBC%20DSN) — Connecting to
        ODBC or DB2 databases
-   [PostgreSQL (PDO)](/book/pdo.html#PostgreSQL%20(PDO)) — PostgreSQL
    Functions (PDO\_PGSQL)
    -   [PDO\_PGSQL DSN](/book/pdo.html#PDO_PGSQL%20DSN) — Connecting to
        PostgreSQL databases
    -   [PDO::pgsqlCopyFromArray](/book/pdo.html#PDO::pgsqlCopyFromArray)
        — Copy data from PHP array into table
    -   [PDO::pgsqlCopyFromFile](/book/pdo.html#PDO::pgsqlCopyFromFile)
        — Copy data from file into table
    -   [PDO::pgsqlCopyToArray](/book/pdo.html#PDO::pgsqlCopyToArray) —
        Copy data from database table into PHP array
    -   [PDO::pgsqlCopyToFile](/book/pdo.html#PDO::pgsqlCopyToFile) —
        Copy data from table into file
    -   [PDO::pgsqlGetNotify](/book/pdo.html#PDO::pgsqlGetNotify) — Get
        asynchronous notification
    -   [PDO::pgsqlGetPid](/book/pdo.html#PDO::pgsqlGetPid) — Get the
        server PID
    -   [PDO::pgsqlLOBCreate](/book/pdo.html#PDO::pgsqlLOBCreate) —
        Creates a new large object
    -   [PDO::pgsqlLOBOpen](/book/pdo.html#PDO::pgsqlLOBOpen) — Opens an
        existing large object stream
    -   [PDO::pgsqlLOBUnlink](/book/pdo.html#PDO::pgsqlLOBUnlink) —
        Deletes the large object
-   [SQLite (PDO)](/book/pdo.html#SQLite%20(PDO)) — SQLite Functions
    (PDO\_SQLITE)
    -   [PDO\_SQLITE DSN](/book/pdo.html#PDO_SQLITE%20DSN) — Connecting
        to SQLite databases
    -   [PDO::sqliteCreateAggregate](/book/pdo.html#PDO::sqliteCreateAggregate)
        — Registers an aggregating User Defined Function for use in SQL
        statements
    -   [PDO::sqliteCreateCollation](/book/pdo.html#PDO::sqliteCreateCollation)
        — Registers a User Defined Function for use as a collating
        function in SQL statements
    -   [PDO::sqliteCreateFunction](/book/pdo.html#PDO::sqliteCreateFunction)
        — Registers a User Defined Function for use in SQL statements

下列驱动目前实现了 PDO 接口：

| 驱动名称                                                                       | 支持的数据库                               |
|--------------------------------------------------------------------------------|--------------------------------------------|
| <a href="/book/pdo.html#CUBRID%20(PDO)" class="link">PDO_CUBRID</a>            | Cubrid                                     |
| <a href="/book/pdo.html#MS%20SQL%20Server%20(PDO)" class="link">PDO_DBLIB</a>  | FreeTDS / Microsoft SQL Server / Sybase    |
| <a href="/book/pdo.html#Firebird%20(PDO)" class="link">PDO_FIREBIRD</a>        | Firebird                                   |
| <a href="/book/pdo.html#IBM%20(PDO)" class="link">PDO_IBM</a>                  | IBM DB2                                    |
| <a href="/book/pdo.html#Informix%20(PDO)" class="link">PDO_INFORMIX</a>        | IBM Informix Dynamic Server                |
| <a href="/book/pdo.html#MySQL%20(PDO)" class="link">PDO_MYSQL</a>              | MySQL 3.x/4.x/5.x                          |
| <a href="/book/pdo.html#Oracle%20(PDO)" class="link">PDO_OCI</a>               | Oracle Call Interface                      |
| <a href="/book/pdo.html#ODBC%20and%20DB2%20(PDO)" class="link">PDO_ODBC</a>    | ODBC v3 (IBM DB2, unixODBC and win32 ODBC) |
| <a href="/book/pdo.html#PostgreSQL%20(PDO)" class="link">PDO_PGSQL</a>         | PostgreSQL                                 |
| <a href="/book/pdo.html#SQLite%20(PDO)" class="link">PDO_SQLITE</a>            | SQLite 3 及 SQLite 2                       |
| <a href="/book/pdo.html#MS%20SQL%20Server%20(PDO)" class="link">PDO_SQLSRV</a> | Microsoft SQL Server / SQL Azure           |

简介
----

PDO\_CUBRID is a driver that implements the
<a href="/book/pdo.html#简介" class="link">PHP Data Objects (PDO) interface</a>
to enable access from PHP to CUBRID databases.

> **Note**:
>
> Current version of PDO\_CUBRID doesn't support persistent connection
> now.

安装
----

To build the PDO\_CUBRID extension, the CUBRID DBMS must be installed on
the same system as PHP. PDO\_CUBRID is a
<a href="https://pecl.php.net/" class="link external">» PECL</a>
extension, so follow the instructions in
<a href="/install/pecl.html" class="xref">PECL 扩展库安装</a> to install
the PDO\_CUBRID extension. Issue the **configure** command to point to
the location of your CUBRID base dir as follows:

       $ ./configure --with-pdo-cubrid=/path/to/CUBRID[,shared]

The **configure** command defaults to the value of the *CUBRID*
environment variable.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.legacy.building" class="link">在 Windows 上构建</a>章节。
Detailed information about installation on Linux and Windows manually,
please read build-guide.html in PECL package CUBRID for reference.

Features
--------

<table>
<caption><strong>PDO_CUBRID Features</strong></caption>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Feature</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Scrollable cursors</td>
<td>PDO_CUBRID supports scrollable cursors. The default cursor type is forward only, and you can use parameter driver_options in <span class="function">PDO::prepare</span> to change cursor type.</td>
</tr>
<tr class="even">
<td>Timeout</td>
<td>PDO_CUBRID supports sql statement execution timeout setting; You can use <span class="function">PDO::setAttribute</span> to set timeout value.</td>
</tr>
<tr class="odd">
<td>Autocommit_mode and Transaction</td>
<td>PDO_CUBRID supports both autocommit_mode and transaction, and autocommit_mode is enabled by default. You can use <span class="function">PDO::setAttribute</span> to change its state.
<p>If you use <span class="function">PDO::beginTransaction</span> to begin a transaction, it will disable autocommit_mode automatically and restore it after <span class="function">PDO::commit</span> or <span class="function">PDO::rollBack</span>. Note that before disabling the autocommit_mode, any pending work is automatically committed.</p></td>
</tr>
<tr class="even">
<td>Multiple SQL Statements</td>
<td>PDO_CUBRID supports Multiple SQL statements. Multiple SQL statements are separated by semicolons (;)</td>
</tr>
<tr class="odd">
<td>Schema Information</td>
<td>PDO_CUBRID implements a function <span class="function">PDO::cubrid_schema</span> to get schema information.</td>
</tr>
<tr class="even">
<td>LOBs</td>
<td>PDO_CUBRID supports BLOB/CLOB data type. The LOB in PDO is represented as a stream, so you can insert LOBs by binding a stream, and get LOBs by reading a stream returned by CUBRID PDO. For example:
<div id="example-1012" class="example">
<p><strong>示例 #1 Insert LOBs in CUBRID PDO</strong></p>
<div class="example-contents">
<div class="phpcode">
<div class="sourceCode" id="cb1"><pre class="sourceCode php"><code class="sourceCode php"><span id="cb1-1"><a href="#cb1-1"></a><span class="kw">&lt;?php</span></span>
<span id="cb1-2"><a href="#cb1-2"></a><span class="kw">$fp</span> = <span class="fu">fopen</span><span class="ot">(</span><span class="st">&#39;lob_test.png&#39;</span><span class="ot">,</span> <span class="st">&#39;rb&#39;</span><span class="ot">);</span></span>
<span id="cb1-3"><a href="#cb1-3"></a></span>
<span id="cb1-4"><a href="#cb1-4"></a><span class="kw">$sql_stmt</span> = <span class="st">&quot;INSERT INTO lob_test(name, content) VALUES(&#39;lob_test.png&#39;, ?)&quot;</span><span class="ot">;</span></span>
<span id="cb1-5"><a href="#cb1-5"></a></span>
<span id="cb1-6"><a href="#cb1-6"></a><span class="kw">$stmt</span> = <span class="kw">$dbh</span>-&gt;prepare<span class="ot">(</span><span class="kw">$sql_stmt</span><span class="ot">);</span></span>
<span id="cb1-7"><a href="#cb1-7"></a><span class="kw">$ret</span> = <span class="kw">$stmt</span>-&gt;bindParam<span class="ot">(</span><span class="dv">1</span><span class="ot">,</span> <span class="kw">$fp</span><span class="ot">,</span> <span class="kw">PDO</span>::<span class="kw">PARAM_LOB</span><span class="ot">);</span></span>
<span id="cb1-8"><a href="#cb1-8"></a><span class="kw">$ret</span> = <span class="kw">$stmt</span>-&gt;execute<span class="ot">();</span></span>
<span id="cb1-9"><a href="#cb1-9"></a><span class="kw">?&gt;</span></span></code></pre></div>
</div>
</div>
</div>
<div id="example-1013" class="example">
<p><strong>示例 #2 Fetch LOBs in CUBRID PDO</strong></p>
<div class="example-contents">
<div class="phpcode">
<div class="sourceCode" id="cb2"><pre class="sourceCode php"><code class="sourceCode php"><span id="cb2-1"><a href="#cb2-1"></a><span class="kw">&lt;?php</span></span>
<span id="cb2-2"><a href="#cb2-2"></a><span class="kw">$sql_stmt</span> = <span class="st">&quot;SELECT content FROM lob_test WHERE name=&#39;lob_test.png&#39;&quot;</span><span class="ot">;</span></span>
<span id="cb2-3"><a href="#cb2-3"></a></span>
<span id="cb2-4"><a href="#cb2-4"></a><span class="kw">$stmt</span> = <span class="kw">$dbh</span>-&gt;prepare<span class="ot">(</span><span class="kw">$sql_stmt</span><span class="ot">);</span></span>
<span id="cb2-5"><a href="#cb2-5"></a><span class="kw">$stmt</span>-&gt;execute<span class="ot">();</span></span>
<span id="cb2-6"><a href="#cb2-6"></a><span class="kw">$result</span> = <span class="kw">$stmt</span>-&gt;fetch<span class="ot">(</span><span class="kw">PDO</span>::<span class="kw">FETCH_NUM</span><span class="ot">);</span></span>
<span id="cb2-7"><a href="#cb2-7"></a></span>
<span id="cb2-8"><a href="#cb2-8"></a><span class="fu">header</span><span class="ot">(</span><span class="st">&quot;Content-Type: image/png&quot;</span><span class="ot">);</span></span>
<span id="cb2-9"><a href="#cb2-9"></a><span class="fu">fpassthru</span><span class="ot">(</span><span class="kw">$result</span><span class="ot">[</span><span class="dv">0</span><span class="ot">]);</span></span>
<span id="cb2-10"><a href="#cb2-10"></a><span class="kw">?&gt;</span></span></code></pre></div>
</div>
</div>
</div></td>
</tr>
<tr class="odd">
<td>Column meta</td>
<td>The <span class="function">PDOStatement::getColumnMeta</span> in CUBRID PDO will return an associative array containing the following values:
<ul>
<li>type</li>
<li>name</li>
<li>table</li>
<li>def</li>
<li>precision</li>
<li>scale</li>
<li>not_null</li>
<li>auto_increment</li>
<li>unique_key</li>
<li>multiple_key</li>
<li>primary_key</li>
<li>foreign_key</li>
<li>reverse_index</li>
<li>reverse_unique</li>
</ul></td>
</tr>
<tr class="even">
<td>Collection Data Type</td>
<td>PDO_CUBRID supports SET/MULTISET/SEQUENCE data type. If you don't specify data type, the default data type is char,for example:
<div id="example-1014" class="example">
<p><strong>示例 #3 Insert set in CUBRID PDO with default data type.</strong></p>
<div class="example-contents">
<div class="phpcode">
<div class="sourceCode" id="cb3"><pre class="sourceCode php"><code class="sourceCode php"><span id="cb3-1"><a href="#cb3-1"></a><span class="kw">&lt;?php</span></span>
<span id="cb3-2"><a href="#cb3-2"></a><span class="kw">$conn_str</span> =<span class="st">&quot;cubrid:dbname=demodb;host=localhost;port=33000&quot;</span><span class="ot">;</span></span>
<span id="cb3-3"><a href="#cb3-3"></a><span class="kw">$cubrid_pdo</span> = <span class="kw">new</span> <span class="kw">PDO</span><span class="ot">(</span><span class="kw">$conn_str</span><span class="ot">,</span> <span class="st">&#39;dba&#39;</span><span class="ot">,</span> <span class="st">&#39;&#39;</span><span class="ot">);</span></span>
<span id="cb3-4"><a href="#cb3-4"></a></span>
<span id="cb3-5"><a href="#cb3-5"></a><span class="kw">$cubrid_pdo</span>-&gt;<span class="fu">exec</span><span class="ot">(</span><span class="st">&quot;DROP TABLE if exists test_tbl&quot;</span><span class="ot">);</span> </span>
<span id="cb3-6"><a href="#cb3-6"></a><span class="kw">$cubrid_pdo</span>-&gt;<span class="fu">exec</span><span class="ot">(</span><span class="st">&quot;CREATE TABLE test_tbl (col_1 SET(VARCHAR))&quot;</span><span class="ot">);</span></span>
<span id="cb3-7"><a href="#cb3-7"></a> </span>
<span id="cb3-8"><a href="#cb3-8"></a><span class="kw">$sql_stmt_insert</span> = <span class="st">&quot;INSERT INTO test_tbl VALUES (?);&quot;</span><span class="ot">;</span></span>
<span id="cb3-9"><a href="#cb3-9"></a><span class="kw">$stmt</span> = <span class="kw">$cubrid_pdo</span>-&gt;prepare<span class="ot">(</span><span class="kw">$sql_stmt_insert</span><span class="ot">);</span></span>
<span id="cb3-10"><a href="#cb3-10"></a><span class="kw">$data</span> = <span class="kw">array</span><span class="ot">(</span><span class="st">&quot;abc&quot;</span><span class="ot">,</span><span class="st">&quot;def&quot;</span><span class="ot">,</span><span class="st">&quot;ghi&quot;</span><span class="ot">);</span></span>
<span id="cb3-11"><a href="#cb3-11"></a><span class="kw">$ret</span> = <span class="kw">$stmt</span>-&gt;bindParam<span class="ot">(</span><span class="dv">1</span><span class="ot">,</span> <span class="kw">$data</span><span class="ot">,</span> <span class="kw">PDO</span>::<span class="kw">PARAM_NULL</span><span class="ot">);</span></span>
<span id="cb3-12"><a href="#cb3-12"></a><span class="kw">$ret</span> = <span class="kw">$stmt</span>-&gt;execute<span class="ot">();</span></span>
<span id="cb3-13"><a href="#cb3-13"></a><span class="fu">var_Dump</span><span class="ot">(</span><span class="kw">$ret</span><span class="ot">);</span></span>
<span id="cb3-14"><a href="#cb3-14"></a><span class="kw">?&gt;</span></span></code></pre></div>
</div>
</div>
</div>
<div id="example-1015" class="example">
<p><strong>示例 #4 Specify data type when insert set in CUBRID PDO</strong></p>
<div class="example-contents">
<div class="phpcode">
<div class="sourceCode" id="cb4"><pre class="sourceCode php"><code class="sourceCode php"><span id="cb4-1"><a href="#cb4-1"></a><span class="kw">&lt;?php</span></span>
<span id="cb4-2"><a href="#cb4-2"></a><span class="kw">$conn_str</span> =<span class="st">&quot;cubrid:dbname=demodb;host=localhost;port=33000&quot;</span><span class="ot">;</span></span>
<span id="cb4-3"><a href="#cb4-3"></a><span class="kw">$cubrid_pdo</span> = <span class="kw">new</span> <span class="kw">PDO</span><span class="ot">(</span><span class="kw">$conn_str</span><span class="ot">,</span> <span class="st">&#39;dba&#39;</span><span class="ot">,</span> <span class="st">&#39;&#39;</span><span class="ot">);</span></span>
<span id="cb4-4"><a href="#cb4-4"></a></span>
<span id="cb4-5"><a href="#cb4-5"></a><span class="kw">$cubrid_pdo</span>-&gt;<span class="fu">exec</span><span class="ot">(</span><span class="st">&quot;DROP TABLE if exists test_tbl&quot;</span><span class="ot">);</span> </span>
<span id="cb4-6"><a href="#cb4-6"></a><span class="kw">$cubrid_pdo</span>-&gt;<span class="fu">exec</span><span class="ot">(</span><span class="st">&quot;CREATE TABLE test_tbl (col_1 SET(int))&quot;</span><span class="ot">);</span></span>
<span id="cb4-7"><a href="#cb4-7"></a> </span>
<span id="cb4-8"><a href="#cb4-8"></a><span class="kw">$sql_stmt_insert</span> = <span class="st">&quot;INSERT INTO test_tbl VALUES (?);&quot;</span><span class="ot">;</span></span>
<span id="cb4-9"><a href="#cb4-9"></a><span class="kw">$stmt</span> = <span class="kw">$cubrid_pdo</span>-&gt;prepare<span class="ot">(</span><span class="kw">$sql_stmt_insert</span><span class="ot">);</span></span>
<span id="cb4-10"><a href="#cb4-10"></a><span class="kw">$data</span> = <span class="kw">array</span><span class="ot">(</span><span class="dv">1</span><span class="ot">,</span><span class="dv">2</span><span class="ot">,</span><span class="dv">3</span><span class="ot">,</span><span class="dv">4</span><span class="ot">);</span></span>
<span id="cb4-11"><a href="#cb4-11"></a><span class="kw">$ret</span> = <span class="kw">$stmt</span>-&gt;bindParam<span class="ot">(</span><span class="dv">1</span><span class="ot">,</span> <span class="kw">$data</span><span class="ot">,</span> <span class="dv">0</span><span class="ot">,</span><span class="dv">0</span><span class="ot">,</span><span class="st">&quot;int&quot;</span><span class="ot">);</span></span>
<span id="cb4-12"><a href="#cb4-12"></a><span class="kw">$ret</span> = <span class="kw">$stmt</span>-&gt;execute<span class="ot">();</span></span>
<span id="cb4-13"><a href="#cb4-13"></a><span class="fu">var_Dump</span><span class="ot">(</span><span class="kw">$ret</span><span class="ot">);</span></span>
<span id="cb4-14"><a href="#cb4-14"></a><span class="kw">?&gt;</span></span></code></pre></div>
</div>
</div>
</div>
CUBRID Bind Data Types:(The fifth parameter of PDOStatement::bindParam):
<ul>
<li>CHAR</li>
<li>STRING</li>
<li>NCHAR</li>
<li>VARNCHAR</li>
<li>BIT</li>
<li>VARBIT</li>
<li>NUMERIC</li>
<li>NUMBER</li>
<li>INT</li>
<li>SHORT</li>
<li>BIGINT</li>
<li>MONETARY</li>
<li>FLOAT</li>
<li>DOUBLE</li>
<li>DATE</li>
<li>TIME</li>
<li>DATETIME</li>
<li>TIMESTAMP</li>
</ul></td>
</tr>
</tbody>
</table>

预定义常量
----------

下列常量由此驱动定义，且仅在扩展编译入 PHP
或在运行时动态载入时可用。另外，使用此驱动时，仅会使用这些驱动特定的常量。使用其他驱动的驱动特定的常量可能会导致不可预见的情况。如果代码可运行于多个驱动，<span
class="function">PDO::getAttribute</span> 可被用于获取
**`PDO_ATTR_DRIVER_NAME`** 属性以检查驱动。

The following constants can be used when setting the database attribute.
They can be passed to <span class="function">PDO::getAttribute</span> or
<span class="function">PDO::setAttribute</span>.

| Constant                               | Description                                                                                                                     |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| PDO::CUBRID\_ATTR\_ISOLATION\_LEVEL    | Transaction isolation level for the database connection.                                                                        |
| PDO::CUBRID\_ATTR\_LOCK\_TIMEOUT       | Transaction timeout in seconds.                                                                                                 |
| PDO::CUBRID\_ATTR\_MAX\_STRING\_LENGTH | Read only. The maximum string length for bit, varbit, char, varchar, nchar, nchar varying data types when using CUBRID PDO API. |

The following constants can be used when setting the transaction
isolation level. They can be passed to <span
class="function">PDO::getAttribute</span> or returned by <span
class="function">PDO::setAttribute</span>.

| Constant                                     | Description                                                                                                                                                |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PDO::TRAN\_COMMIT\_CLASS\_UNCOMMIT\_INSTANCE | The lowest isolation level (1). A dirty, non-repeatable or phantom read may occur for the tuple and a non-repeatable read may occur for the table as well. |
| PDO::TRAN\_COMMIT\_CLASS\_COMMIT\_INSTANCE   | A relatively low isolation level (2). A dirty read does not occur, but non-repeatable or phantom read may occur.                                           |
| PDO::TRAN\_REP\_CLASS\_UNCOMMIT\_INSTANCE    | The default isolation of CUBRID (3). A dirty, non-repeatable or phantom read may occur for the tuple, but repeatable read is ensured for the table.        |
| PDO::TRAN\_REP\_CLASS\_COMMIT\_INSTANCE      | A relatively low isolation level (4). A dirty read does not occur, but non-repeatable or phantom read may.                                                 |
| PDO::TRAN\_REP\_CLASS\_REP\_INSTANCE         | A relatively high isolation level (5). A dirty or non-repeatable read does not occur, but a phantom read may.                                              |
| PDO::TRAN\_SERIALIZABLE                      | The highest isolation level (6). Problems concerning concurrency (e.g. dirty read, non-repeatable read, phantom read, etc.) do not occur.                  |

The following constants can be used when getting schema information.
They can be passed to <span class="function">PDO::cubrid\_schema</span>.

| Constant                               | Description                                                                                                                                                                                               |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PDO::CUBRID\_SCH\_TABLE                | Get name and type of table in CUBRID.                                                                                                                                                                     |
| PDO::CUBRID\_SCH\_VIEW                 | Get name and type of view in CUBRID.                                                                                                                                                                      |
| PDO::CUBRID\_SCH\_QUERY\_SPEC          | Get the query definition of view.                                                                                                                                                                         |
| PDO::CUBRID\_SCH\_ATTRIBUTE            | Get the attributes of table column.                                                                                                                                                                       |
| PDO::CUBRID\_SCH\_TABLE\_ATTRIBUTE     | Get the attributes of table.                                                                                                                                                                              |
| PDO::CUBRID\_SCH\_METHOD               | Get the instance method. The instance method is a method called by a class instance. It is used more often than the class method because most operations are executed in the instance.                    |
| PDO::CUBRID\_SCH\_TABLE\_METHOD        | Get the class method. The class method is a method called by a class object. It is usually used to create a new class instance or to initialize it. It is also used to access or update class attributes. |
| PDO::CUBRID\_SCH\_METHOD\_FILE         | Get the information of the file where the method of the table is defined.                                                                                                                                 |
| PDO::CUBRID\_SCH\_SUPER\_TABLE         | Get the name and type of table which table inherites attributes from.                                                                                                                                     |
| PDO::CUBRID\_SCH\_SUB\_TABLE           | Get the name and type of table which inherites attributes from this table.                                                                                                                                |
| PDO::CUBRID\_SCH\_CONSTRAINT           | Get the table constraints.                                                                                                                                                                                |
| PDO::CUBRID\_SCH\_TRIGGER              | Get the table triggers.                                                                                                                                                                                   |
| PDO::CUBRID\_SCH\_TABLE\_PRIVILEGE     | Get the privilege information of table.                                                                                                                                                                   |
| PDO::CUBRID\_SCH\_COL\_PRIVILEGE       | Get the privilege information of column.                                                                                                                                                                  |
| PDO::CUBRID\_SCH\_DIRECT\_SUPER\_TABLE | Get the direct super table of table.                                                                                                                                                                      |
| PDO::CUBRID\_SCH\_PRIMARY\_KEY         | Get the table primary key.                                                                                                                                                                                |
| PDO::CUBRID\_SCH\_IMPORTED\_KEYS       | Get imported keys of table.                                                                                                                                                                               |
| PDO::CUBRID\_SCH\_EXPORTED\_KEYS       | Get exported keys of table.                                                                                                                                                                               |
| PDO::CUBRID\_SCH\_CROSS\_REFERENCE     | Get reference relationship of tow tables.                                                                                                                                                                 |

PDO\_CUBRID DSN
===============

Connecting to CUBRID databases

### 说明

The PDO\_CUBRID Data Source Name (DSN) is composed of the following
elements, delimited by semicolons:

DSN prefix  
The DSN prefix is **`cubrid:`**.

*host*  
The hostname on which the database server resides.

*port*  
The port on which the database server is running.

*dbname*  
The name of the database.

### 注释

> **Note**:
>
> When you estalish the connection to CUBRID, you should give username
> and password except DSN.

### 范例

**示例 \#1 PDO\_CUBRID DSN examples**

The following example shows a PDO\_CUBRID DSN for connecting to a CUBRID
database:

    cubrid:host=localhost;port=33000;dbname=demodb

PDO::cubrid\_schema
===================

Get the requested schema information

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">PDO::cubrid\_schema</span> ( <span
class="methodparam"><span class="type">int</span> `$schema_type`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$table_name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$col_name`</span> \]\] )

This function is used to get the requested schema information from
database. You have to designate `table_name`, if you want to get
information on certain table, `col_name`, if you want to get information
on certain column (can be used only with
PDO::CUBRID\_SCH\_COL\_PRIVILEGE).

The result of this function is returned as a two-dimensional array
(column (associative array) \* row (numeric array)). The following
tables shows types of schema and the column structure of the result
array to be returned based on the schema type.

| Schema                                                                                                   | Column Number | Column Name              | Value                                             |
|----------------------------------------------------------------------------------------------------------|---------------|--------------------------|---------------------------------------------------|
| PDO::CUBRID\_SCH\_TABLE                                                                                  | 1             | NAME                     |                                                   |
|                                                                                                          | 2             | TYPE                     | 0:system table 1:view 2:table                     |
| PDO::CUBRID\_SCH\_VIEW                                                                                   | 1             | NAME                     |                                                   |
|                                                                                                          | 2             | TYPE                     | 1:view                                            |
| PDO::CUBRID\_SCH\_QUERY\_SPEC                                                                            | 1             | QUERY\_SPEC              |                                                   |
| PDO::CUBRID\_SCH\_ATTRIBUTE / PDO::CUBRID\_SCH\_TABLE\_ATTRIBUTE                                         | 1             | ATTR\_NAME               |                                                   |
|                                                                                                          | 2             | DOMAIN                   |                                                   |
|                                                                                                          | 3             | SCALE                    |                                                   |
|                                                                                                          | 4             | PRECISION                |                                                   |
|                                                                                                          | 5             | INDEXED                  | 1:indexed                                         |
|                                                                                                          | 6             | NOT NULL                 | 1:not null                                        |
|                                                                                                          | 7             | SHARED                   | 1:shared                                          |
|                                                                                                          | 8             | UNIQUE                   | 1:unique                                          |
|                                                                                                          | 9             | DEFAULT                  |                                                   |
|                                                                                                          | 10            | ATTR\_ORDER              | base:1                                            |
|                                                                                                          | 11            | CLASS\_NAME              |                                                   |
|                                                                                                          | 12            | SOURCE\_CLASS            |                                                   |
|                                                                                                          | 13            | IS\_KEY                  | 1:key                                             |
| PDO::CUBRID\_SCH\_METHOD / PDO::CUBRID\_SCH\_TABLE\_METHOD                                               | 1             | NAME                     |                                                   |
|                                                                                                          | 2             | RET\_DOMAIN              |                                                   |
|                                                                                                          | 3             | ARG\_DOMAIN              |                                                   |
| PDO::CUBRID\_SCH\_METHOD\_FILE                                                                           | 1             | METHOD\_FILE             |                                                   |
| PDO::CUBRID\_SCH\_SUPER\_TABLE / PDO::CUBRID\_SCH\_DIRECT\_SUPER\_TABLE / PDO::CUBRID\_SCH\_SUB\_TABLE   | 1             | CLASS\_NAME              |                                                   |
|                                                                                                          | 2             | TYPE                     | 0:system table 1:view 2:table                     |
| PDO::CUBRID\_SCH\_CONSTRAINT                                                                             | 1             | TYPE                     | 0:unique 1:index 2:reverse unique 3:reverse index |
|                                                                                                          | 2             | NAME                     |                                                   |
|                                                                                                          | 3             | ATTR\_NAME               |                                                   |
|                                                                                                          | 4             | NUM\_PAGES               |                                                   |
|                                                                                                          | 5             | NUM\_KEYS                |                                                   |
|                                                                                                          | 6             | PRIMARY\_KEY             | 1:primary key                                     |
|                                                                                                          | 7             | KEY\_ORDER               | base:1                                            |
| PDO::CUBRID\_SCH\_TRIGGER                                                                                | 1             | NAME                     |                                                   |
|                                                                                                          | 2             | STATUS                   |                                                   |
|                                                                                                          | 3             | EVENT                    |                                                   |
|                                                                                                          | 4             | TARGET\_CLASS            |                                                   |
|                                                                                                          | 5             | TARGET\_ATTR             |                                                   |
|                                                                                                          | 6             | ACTION\_TIME             |                                                   |
|                                                                                                          | 7             | ACTION                   |                                                   |
|                                                                                                          | 8             | PRIORITY                 |                                                   |
|                                                                                                          | 9             | CONDITION\_TIME          |                                                   |
|                                                                                                          | 10            | CONDITION                |                                                   |
| PDO::CUBRID\_SCH\_TABLE\_PRIVILEGE / PDO::CUBRID\_SCH\_COL\_PRIVILEGE                                    | 1             | CLASS\_NAME / ATTR\_NAME |                                                   |
|                                                                                                          | 2             | PRIVILEGE                |                                                   |
|                                                                                                          | 3             | GRANTABLE                |                                                   |
| PDO::CUBRID\_SCH\_PRIMARY\_KEY                                                                           | 1             | CLASS\_NAME              |                                                   |
|                                                                                                          | 2             | ATTR\_NAME               |                                                   |
|                                                                                                          | 3             | KEY\_SEQ                 | base:1                                            |
|                                                                                                          | 4             | KEY\_NAME                |                                                   |
| PDO::CUBRID\_SCH\_IMPORTED\_KEYS / PDO::CUBRID\_SCH\_EXPORTED\_KEYS / PDO::CUBRID\_SCH\_CROSS\_REFERENCE | 1             | PKTABLE\_NAME            |                                                   |
|                                                                                                          | 2             | PKCOLUMN\_NAME           |                                                   |
|                                                                                                          | 3             | FKTABLE\_NAME            | base:1                                            |
|                                                                                                          | 4             | FKCOLUMN\_NAME           |                                                   |
|                                                                                                          | 5             | KEY\_SEQ                 | base:1                                            |
|                                                                                                          | 6             | UPDATE\_ACTION           | 0:cascade 1:restrict 2:no action 3:set null       |
|                                                                                                          | 7             | DELETE\_ACTION           | 0:cascade 1:restrict 2:no action 3:set null       |
|                                                                                                          | 8             | FK\_NAME                 |                                                   |
|                                                                                                          | 9             | PK\_NAME                 |                                                   |

### 参数

`schema_type`  
Schema type that you want to know.

`table_name`  
Table you want to know the schema of.

`col_name`  
Column you want to know the schema of.

### 返回值

Array containing the schema information, when process is successful;

FALSE, when process is unsuccessful

### 范例

**示例 \#1 A <span class="function">PDO::cubrid\_schema</span> example**

This example shows how to get primary key and foreign keys of table
game.

``` php
<?php
$pk_list = $dbh->cubrid_schema(PDO::CUBRID_SCH_PRIMARY_KEY, "game");
print_r($pk_list);

$fk_list = $dbh->cubrid_schema(PDO::CUBRID_SCH_IMPORTED_KEYS, "game");
print_r($fk_list);
?>
```

以上例程会输出：

    Result:
    Array
    (
        [0] => Array
            (
                [CLASS_NAME] => game
                [ATTR_NAME] => athlete_code
                [KEY_SEQ] => 3
                [KEY_NAME] => pk_game_host_year_event_code_athlete_code
            )

        [1] => Array
            (
                [CLASS_NAME] => game
                [ATTR_NAME] => event_code
                [KEY_SEQ] => 2
                [KEY_NAME] => pk_game_host_year_event_code_athlete_code
            )

        [2] => Array
            (
                [CLASS_NAME] => game
                [ATTR_NAME] => host_year
                [KEY_SEQ] => 1
                [KEY_NAME] => pk_game_host_year_event_code_athlete_code
            )

    )
    Array
    (
        [0] => Array
            (
                [PKTABLE_NAME] => athlete
                [PKCOLUMN_NAME] => code
                [FKTABLE_NAME] => game
                [FKCOLUMN_NAME] => athlete_code
                [KEY_SEQ] => 1
                [UPDATE_RULE] => 1
                [DELETE_RULE] => 1
                [FK_NAME] => fk_game_athlete_code
                [PK_NAME] => pk_athlete_code
            )

        [1] => Array
            (
                [PKTABLE_NAME] => event
                [PKCOLUMN_NAME] => code
                [FKTABLE_NAME] => game
                [FKCOLUMN_NAME] => event_code
                [KEY_SEQ] => 1
                [UPDATE_RULE] => 1
                [DELETE_RULE] => 1
                [FK_NAME] => fk_game_event_code
                [PK_NAME] => pk_event_code
            )

    )

**目录**

-   [PDO\_CUBRID DSN](/book/pdo.html#PDO_CUBRID%20DSN) — Connecting to
    CUBRID databases
-   [PDO::cubrid\_schema](/book/pdo.html#PDO::cubrid_schema) — Get the
    requested schema information

简介
----

PDO\_DBLIB is a driver that implements the
<a href="/book/pdo.html#简介" class="link">PHP Data Objects (PDO) interface</a>
to enable access from PHP to Microsoft SQL Server and Sybase databases
through the FreeTDS library.

This extension is not available anymore on Windows with PHP 5.3 or
later.

On Windows, you should use SqlSrv, an alternative driver for MS SQL is
available from Microsoft:
<a href="http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx" class="link external">» http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx</a>
.

If it is not possible to use SqlSrv, you can use the
<a href="/book/pdo.html#ODBC%20and%20DB2%20(PDO)" class="link">PDO_ODBC</a>
driver to connect to Microsoft SQL Server and Sybase databases, as the
native Windows DB-LIB is ancient, thread un-safe and no longer supported
by Microsoft.

PDO\_DBLIB DSN
==============

Connecting to Microsoft SQL Server and Sybase databases

### 说明

The PDO\_DBLIB Data Source Name (DSN) is composed of the following
elements:

DSN prefix  
The DSN prefix is **`sybase:`** if PDO\_DBLIB was linked against the
Sybase ct-lib libraries, **`mssql:`** if PDO\_DBLIB was linked against
the Microsoft SQL Server libraries, or **`dblib:`** if PDO\_DBLIB was
linked against the FreeTDS libraries.

*host*  
The hostname on which the database server resides. Defaults to
127.0.0.1.

*dbname*  
The name of the database.

*charset*  
The client character set.

*appname*  
The application name (used in sysprocesses). Defaults to "PHP Generic
DB-lib" or "PHP freetds".

*secure*  
Currently unused.

### 范例

**示例 \#1 PDO\_DBLIB DSN examples**

The following examples show a PDO\_DBLIB DSN for connecting to Microsoft
SQL Server and Sybase databases:

    mssql:host=localhost;dbname=testdb
    sybase:host=localhost;dbname=testdb
    dblib:host=localhost;dbname=testdb

**目录**

-   [PDO\_DBLIB DSN](/book/pdo.html#PDO_DBLIB%20DSN) — Connecting to
    Microsoft SQL Server and Sybase databases

简介
----

PDO\_FIREBIRD is a driver that implements the PHP Data Objects (PDO)
interface to enable access from PHP to Firebird database.

安装
----

Use **--with-pdo-firebird\[=DIR\]** to install the PDO Firebird
extension, where the optional *\[=DIR\]* is the Firebird base install
directory.

    $ ./configure --with-pdo-firebird

预定义常量
----------

下列常量由此驱动定义，且仅在扩展编译入 PHP
或在运行时动态载入时可用。另外，使用此驱动时，仅会使用这些驱动特定的常量。使用其他驱动的驱动特定的常量可能会导致不可预见的情况。如果代码可运行于多个驱动，<span
class="function">PDO::getAttribute</span> 可被用于获取
**`PDO_ATTR_DRIVER_NAME`** 属性以检查驱动。

**`PDO::FB_ATTR_DATE_FORMAT`** (<span class="type">int</span>)  
Available since PHP 5.3.0.

Sets the date format.

**`PDO::FB_ATTR_TIME_FORMAT`** (<span class="type">int</span>)  
Sets the time format.

Available since PHP 5.3.0.

**`PDO::FB_ATTR_TIMESTAMP_FORMAT`** (<span class="type">int</span>)  
Sets the timestamp format.

Available since PHP 5.3.0.

PDO\_FIREBIRD DSN
=================

Connecting to Firebird databases

### 说明

The PDO\_FIREBIRD Data Source Name (DSN) is composed of the following
elements:

DSN prefix  
The DSN prefix is **`firebird:`**.

*dbname*  
The name of the database.

*charset*  
The character set.

*role*  
The SQL role name.

*dialect*  
The dialect of the database; either *1* or *3*. If not specified, the
dialect defaults to *3*. Available as of PHP 7.4.0.

### 范例

**示例 \#1 PDO\_FIREBIRD DSN example with path**

The following example shows a PDO\_FIREBIRD DSN for connecting to
Firebird databases:

    firebird:dbname=/path/to/DATABASE.FDB

**示例 \#2 PDO\_FIREBIRD DSN example with port and path**

The following example shows a PDO\_FIREBIRD DSN for connecting to a
Firebird database using hostname port and path:

    firebird:dbname=hostname/port:/path/to/DATABASE.FDB

**示例 \#3 PDO\_FIREBIRD DSN example with localhost and path to
employee.fdb on Debian system**

The following example shows a PDO\_FIREBIRD DSN for connecting to a
Firebird database employee.fdb using localhost:

    firebird:dbname=localhost:/var/lib/firebird/2.5/data/employee.fdb

**示例 \#4 PDO\_FIREBIRD DSN to connect to a dialect 1 database**

The following example shows a PDO\_FIREBIRD DSN for connecting to a
Firebird database test.fdb which has been created using dialect 1. This
is only supported as of PHP 7.4.0.

    firebird:dbname=localhost:/var/lib/firebird/2.5/data/test.fdb;charset=utf-8;dialect=1

**目录**

-   [PDO\_FIREBIRD DSN](/book/pdo.html#PDO_FIREBIRD%20DSN) — Connecting
    to Firebird databases

简介
----

PDO\_IBM is a driver that implements the
<a href="/book/pdo.html#简介" class="link">PHP Data Objects (PDO)</a>
interface to enable access from PHP to IBM databases.

安装
----

To build the PDO\_IBM extension, the DB2 Client v9.1 or later must be
installed on the same system as PHP. The DB2 Client can be downloaded
from the IBM
<a href="http://www.ibm.com/software/data/db2/ad" class="link external">» Application Development Site</a>.

> **Note**: **Note**  
>
> The DB2 Client v9.1 or later supports direct access to DB2 for Linux,
> UNIX, and Windows v8 and v9.1 servers.
>
> The DB2 Client v9.1 also supports access to DB2 UDB for i5 and DB2 UDB
> for z/OS servers using the separately purchased
> <a href="http://www.ibm.com/software/data/db2/db2connect" class="link external">» DB2 Connect product</a>.

PDO\_IBM is a
<a href="https://pecl.php.net/" class="link external">» PECL</a>
extension, so follow the instructions in
<a href="/install/pecl.html" class="xref">PECL 扩展库安装</a> to install
the PDO\_IBM extension. Issue the **configure** command to point to the
location of your DB2 Client header files and libraries as follows:

    bash$ ./configure --with-pdo-ibm=/path/to/sqllib[,shared]

The **configure** command defaults to the value of the *DB2DIR*
environment variable.

PDO\_IBM DSN
============

Connecting to IBM databases

### 说明

The PDO\_IBM Data Source Name (DSN) is based on the IBM CLI DSN. The
major components of the PDO\_IBM DSN are:

DSN prefix  
The DSN prefix is **`ibm:`**.

DSN  
The DSN can be any of the following:

-   a\) Data source setup using `db2cli.ini` or `odbc.ini`

-   b\) Catalogued database name i.e. database alias in the DB2 client
    catalog

-   c\) Complete connection string in the following format:
    `DRIVER={IBM DB2 ODBC DRIVER};DATABASE=database`;HOSTNAME=`hostname`;PORT=`port`;PROTOCOL=TCPIP;UID=`username`;PWD=`password`;
    where the parameters represent the following values:

    `database`  
    The name of the database.

    `hostname`  
    The hostname or IP address of the database server.

    `port`  
    The TCP/IP port on which the database is listening for requests.

    `username`  
    The username with which you are connecting to the database.

    `password`  
    The password with which you are connecting to the database.

### 范例

**示例 \#1 PDO\_IBM DSN example using `db2cli.ini`**

The following example shows a PDO\_IBM DSN for connecting to an DB2
database cataloged as DB2\_9 in `db2cli.ini`:

    $db = new PDO("ibm:DSN=DB2_9", "", "");

    [DB2_9]
    Database=testdb
    Protocol=tcpip
    Hostname=11.22.33.444
    Servicename=56789

**示例 \#2 PDO\_IBM DSN example using a connection string**

The following example shows a PDO\_IBM DSN for connecting to an DB2
database named **`testdb`** using the DB2 CLI connection string syntax.

    $db = new PDO("ibm:DRIVER={IBM DB2 ODBC DRIVER};DATABASE=testdb;" .
      "HOSTNAME=11.22.33.444;PORT=56789;PROTOCOL=TCPIP;", "testuser", "tespass");

**目录**

-   [PDO\_IBM DSN](/book/pdo.html#PDO_IBM%20DSN) — Connecting to IBM
    databases

简介
----

PDO\_INFORMIX is a driver that implements the
<a href="/book/pdo.html#简介" class="link">PHP Data Objects (PDO)</a>
interface to enable access from PHP to Informix databases.

安装
----

To build the PDO\_INFORMIX extension, the Informix Client SDK 2.81 UC1
or higher must be installed on the same system as PHP. The Informix
Client SDK is available from the
<a href="http://www-306.ibm.com/software/data/informix/tools/csdk/" class="link external">» IBM Informix Support Site</a>.

PDO\_INFORMIX is a
<a href="https://pecl.php.net/" class="link external">» PECL</a>
extension, so follow the instructions in
<a href="/install/pecl.html" class="xref">PECL 扩展库安装</a> to install
the PDO\_INFORMIX extension. Issue the **configure** command to point to
the location of your Informix Client SDK header files and libraries as
follows:

       bash$ ./configure --with-pdo-informix=/path/to/SDK[,shared]

The **configure** command defaults to the value of the *INFORMIXDIR*
environment variable.

Scrollable cursors
------------------

PDO\_INFORMIX supports scrollable cursors; however, they are not enabled
by default. To enable scrollable cursor support, you must either set
**`ENABLESCROLLABLECURSORS=1`** in the corresponding ODBC connection
settings in `odbc.ini` or pass the **`EnableScrollableCursors=1`**
clause in the DSN connection string.

PDO\_INFORMIX DSN
=================

Connecting to Informix databases

### 说明

The PDO\_INFORMIX Data Source Name (DSN) is based on the Informix ODBC
DSN string. Details on configuring an Informix ODBC DSN are available
from the
<a href="http://publib.boulder.ibm.com/infocenter/idshelp/v10/index.jsp" class="link external">» Informix Dynamic Server Information Center</a>.
The major components of the PDO\_INFORMIX DSN are:

DSN prefix  
The DSN prefix is **`informix:`**.

DSN  
The DSN can be either a data source setup using `odbc.ini` or a complete
<a href="http://publib.boulder.ibm.com/infocenter/idshelp/v10/topic/com.ibm.odbc.doc/odbc66.htm#sii02998361" class="link external">» connection string</a>.

### 范例

**示例 \#1 PDO\_INFORMIX DSN example using `odbc.ini`**

The following example shows a PDO\_INFORMIX DSN for connecting to an
Informix database cataloged as Infdrv33 in `odbc.ini`:

    $db = new PDO("informix:DSN=Infdrv33", "", "");

    [ODBC Data Sources]
    Infdrv33=INFORMIX 3.3 32-BIT

    [Infdrv33]
    Driver=/opt/informix/csdk_2.81.UC1G2/lib/cli/iclis09b.so
    Description=INFORMIX 3.3 32-BIT
    Database=common_db
    LogonID=testuser
    pwd=testpass
    Servername=ids_server
    DB_LOCALE=en_US.819
    OPTIMIZEAUTOCOMMIT=1
    ENABLESCROLLABLECURSORS=1

**示例 \#2 PDO\_INFORMIX DSN example using a connection string**

The following example shows a PDO\_INFORMIX DSN for connecting to an
Informix database named **`common_db`** using the Informix connection
string syntax.

    $db = new PDO("informix:host=host.domain.com; service=9800;
        database=common_db; server=ids_server; protocol=onsoctcp;
        EnableScrollableCursors=1", "testuser", "tespass");

**目录**

-   [PDO\_INFORMIX DSN](/book/pdo.html#PDO_INFORMIX%20DSN) — Connecting
    to Informix databases

简介
----

PDO\_MYSQL is a driver that implements the
<a href="/book/pdo.html#简介" class="link">PHP Data Objects (PDO) interface</a>
to enable access from PHP to MySQL databases.

As of PHP 5.2.1, PDO\_MYSQL uses emulated prepares by default. Formerly,
PDO\_MYSQL defaulted to native prepared statement support present in
MySQL 4.1 and higher, and emulated them for older versions of the mysql
client libraries.

*MySQL 8*

When running a PHP version before 7.1.16, or PHP 7.2 before 7.2.4, set
MySQL 8 Server's default password plugin to *mysql\_native\_password* or
else you will see errors similar to *The server requested authentication
method unknown to the client \[caching\_sha2\_password\]* even when
*caching\_sha2\_password* is not used.

This is because MySQL 8 defaults to caching\_sha2\_password, a plugin
that is not recognized by the older PHP (mysqlnd) releases. Instead,
change it by setting
*default\_authentication\_plugin=mysql\_native\_password* in `my.cnf`.
The *caching\_sha2\_password* plugin will be supported in a future PHP
release. In the meantime, the
<a href="/set/mysqlinfo.html#Mysql_xdevapi" class="link">mysql_xdevapi</a>
extension does support it.

**Warning**

Beware: Some MySQL table types (storage engines) do not support
transactions. When writing transactional database code using a table
type that does not support transactions, MySQL will pretend that a
transaction was initiated successfully. In addition, any DDL queries
issued will implicitly commit any pending transactions.

安装
----

The common Unix distributions include binary versions of PHP that can be
installed. Although these binary versions are typically built with
support for the MySQL extensions, the extension libraries themselves may
need to be installed using an additional package. Check the package
manager than comes with your chosen distribution for availability.

For example, on Ubuntu the *php5-mysql* package installs the ext/mysql,
ext/mysqli, and PDO\_MYSQL PHP extensions. On CentOS, the *php-mysql*
package also installs these three PHP extensions.

Alternatively, you can compile this extension yourself. Building PHP
from source allows you to specify the MySQL extensions you want to use,
as well as your choice of client library for each extension.

When compiling, use **--with-pdo-mysql\[=DIR\]** to install the PDO
MySQL extension, where the optional *\[=DIR\]* is the MySQL base
library. As of PHP 5.4,
<a href="/set/mysqlinfo.html#Mysqlnd" class="link">mysqlnd</a> is the
default library. For details about choosing a library, see
<a href="/set/mysqlinfo.html#Choosing%20a%20library" class="link">Choosing a MySQL library</a>.

Optionally, the **--with-mysql-sock\[=DIR\]** sets to location to the
MySQL unix socket pointer for all MySQL extensions, including
PDO\_MYSQL. If unspecified, the default locations are searched.

Optionally, the **--with-zlib-dir\[=DIR\]** is used to set the path to
the libz install prefix.

    $ ./configure --with-pdo-mysql --with-mysql-sock=/var/mysql/mysql.sock

SSL support is enabled using the appropriate
<a href="/book/pdo.html#预定义常量" class="link">PDO_MySQL constants</a>,
which is equivalent to calling the
<a href="http://dev.mysql.com/doc/mysql/en/mysql-ssl-set.html" class="link external">» MySQL C API function mysql_ssl_set()</a>.
Also, SSL cannot be enabled with <span
class="classname">PDO::setAttribute</span> because the connection
already exists. See also the MySQL documentation about
<a href="http://dev.mysql.com/doc/mysql/en/configuring-for-ssl.html" class="link external">» connecting to MySQL with SSL</a>.

| 版本  | 说明                                                                                                                                                                                 |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.4.0 | <a href="/set/mysqlinfo.html#Mysqlnd" class="link">mysqlnd</a> became the default MySQL library when compiling PDO\_MYSQL. Previously, libmysqlclient was the default MySQL library. |
| 5.4.0 | MySQL client libraries 4.1 and below are no longer supported.                                                                                                                        |
| 5.3.9 | Added SSL support with mysqlnd and OpenSSL.                                                                                                                                          |
| 5.3.7 | Added SSL support with libmysqlclient and OpenSSL.                                                                                                                                   |

预定义常量
----------

下列常量由此驱动定义，且仅在扩展编译入 PHP
或在运行时动态载入时可用。另外，使用此驱动时，仅会使用这些驱动特定的常量。使用其他驱动的驱动特定的常量可能会导致不可预见的情况。如果代码可运行于多个驱动，<span
class="function">PDO::getAttribute</span> 可被用于获取
**`PDO_ATTR_DRIVER_NAME`** 属性以检查驱动。

**`PDO::MYSQL_ATTR_USE_BUFFERED_QUERY`** (<span class="type">int</span>)  
<span class="simpara"> If this attribute is set to **`TRUE`** on a <span
class="classname">PDOStatement</span>, the MySQL driver will use the
buffered versions of the MySQL API. If you're writing portable code, you
should use <span class="function">PDOStatement::fetchAll</span> instead.
</span>

**示例 \#1 Forcing queries to be buffered in mysql**

``` php
<?php
if ($db->getAttribute(PDO::ATTR_DRIVER_NAME) == 'mysql') {
    $stmt = $db->prepare('select * from foo',
        array(PDO::MYSQL_ATTR_USE_BUFFERED_QUERY => true));
} else {
    die("my application only works with mysql; I should use \$stmt->fetchAll() instead");
}
?>
```

**`PDO::MYSQL_ATTR_LOCAL_INFILE`** (<span class="type">int</span>)  
Enable *LOAD LOCAL INFILE*.

Note, this constant can only be used in the `driver_options` array when
constructing a new database handle.

**`PDO::MYSQL_ATTR_LOCAL_INFILE_DIRECTORY`** (<span class="type">string</span>)  
Allows restricting LOCAL DATA loading to files located in this
designated directory.

Note, this constant can only be used in the `driver_options` array when
constructing a new database handle.

**`PDO::MYSQL_ATTR_INIT_COMMAND`** (<span class="type">int</span>)  
Command to execute when connecting to the MySQL server. Will
automatically be re-executed when reconnecting.

Note, this constant can only be used in the `driver_options` array when
constructing a new database handle.

**`PDO::MYSQL_ATTR_READ_DEFAULT_FILE`** (<span class="type">int</span>)  
Read options from the named option file instead of from `my.cnf`. This
option is not available if mysqlnd is used, because mysqlnd does not
read the mysql configuration files.

**`PDO::MYSQL_ATTR_READ_DEFAULT_GROUP`** (<span class="type">int</span>)  
Read options from the named group from `my.cnf` or the file specified
with **`MYSQL_READ_DEFAULT_FILE`**. This option is not available if
mysqlnd is used, because mysqlnd does not read the mysql configuration
files.

**`PDO::MYSQL_ATTR_MAX_BUFFER_SIZE`** (<span class="type">int</span>)  
Maximum buffer size. Defaults to 1 MiB. This constant is not supported
when compiled against mysqlnd.

**`PDO::MYSQL_ATTR_DIRECT_QUERY`** (<span class="type">int</span>)  
Perform direct queries, don't use prepared statements.

**`PDO::MYSQL_ATTR_FOUND_ROWS`** (<span class="type">int</span>)  
Return the number of found (matched) rows, not the number of changed
rows.

**`PDO::MYSQL_ATTR_IGNORE_SPACE`** (<span class="type">int</span>)  
Permit spaces after function names. Makes all functions names reserved
words.

**`PDO::MYSQL_ATTR_COMPRESS`** (<span class="type">int</span>)  
Enable network communication compression. This is also supported when
compiled against mysqlnd as of PHP 5.3.11.

**`PDO::MYSQL_ATTR_SSL_CA`** (<span class="type">int</span>)  
The file path to the SSL certificate authority.

自以下版本起 PHP 5.3.7.

**`PDO::MYSQL_ATTR_SSL_CAPATH`** (<span class="type">int</span>)  
The file path to the directory that contains the trusted SSL CA
certificates, which are stored in PEM format.

自以下版本起 PHP 5.3.7.

**`PDO::MYSQL_ATTR_SSL_CERT`** (<span class="type">int</span>)  
The file path to the SSL certificate.

自以下版本起 PHP 5.3.7.

**`PDO::MYSQL_ATTR_SSL_CIPHER`** (<span class="type">int</span>)  
A list of one or more permissible ciphers to use for SSL encryption, in
a format understood by OpenSSL. For example:
*DHE-RSA-AES256-SHA:AES128-SHA*

自以下版本起 PHP 5.3.7.

**`PDO::MYSQL_ATTR_SSL_KEY`** (<span class="type">int</span>)  
The file path to the SSL key.

自以下版本起 PHP 5.3.7.

**`PDO::MYSQL_ATTR_SSL_VERIFY_SERVER_CERT`** (<span class="type">int</span>)  
Provides a way to disable verification of the server SSL certificate.

自以下版本起 PHP 7.0.18 and PHP 7.1.4.

**`PDO::MYSQL_ATTR_MULTI_STATEMENTS`** (<span class="type">int</span>)  
Disables multi query execution in both <span
class="function">PDO::prepare</span> and <span
class="function">PDO::query</span> when set to **`FALSE`**.

Note, this constant can only be used in the `driver_options` array when
constructing a new database handle.

自以下版本起 PHP 5.5.21 and PHP 5.6.5.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                | 默认              | 可修改范围       |
|---------------------------------------------------------------------|-------------------|------------------|
| <a href="/book/pdo.html#" class="link">pdo_mysql.default_socket</a> | "/tmp/mysql.sock" | PHP\_INI\_SYSTEM |
| <a href="/book/pdo.html#" class="link">pdo_mysql.debug</a>          | NULL              | PHP\_INI\_SYSTEM |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`pdo_mysql.default_socket` <span class="type">string</span>  
Sets a Unix domain socket. This value can either be set at compile time
if a domain socket is found at configure. This ini setting is Unix only.

`pdo_mysql.debug` <span class="type">bool</span>  
Enables debugging for PDO\_MYSQL. This setting is only available when
PDO\_MYSQL is compiled against mysqlnd and in PDO debug mode.

PDO\_MYSQL DSN
==============

Connecting to MySQL databases

### 说明

The PDO\_MYSQL Data Source Name (DSN) is composed of the following
elements:

DSN prefix  
The DSN prefix is **`mysql:`**.

*host*  
The hostname on which the database server resides.

*port*  
The port number where the database server is listening.

*dbname*  
The name of the database.

*unix\_socket*  
The MySQL Unix socket (shouldn't be used with *host* or *port*).

*charset*  
The character set. See the
<a href="/set/mysqlinfo.html#Character%20sets" class="link">character set</a>
concepts documentation for more information.

Prior to PHP 5.3.6, this element was silently ignored. The same
behaviour can be partly replicated with the
**`PDO::MYSQL_ATTR_INIT_COMMAND`** driver option, as the following
example shows.

**Warning**
The method in the below example can only be used with character sets
that share the same lower 7 bit representation as ASCII, such as
ISO-8859-1 and UTF-8. Users using character sets that have different
representations (such as UTF-16 or Big5) *must* use the *charset* option
provided in PHP 5.3.6 and later versions.

**示例 \#1 Setting the connection character set to UTF-8 prior to PHP
5.3.6**

``` php
<?php
$dsn = 'mysql:host=localhost;dbname=testdb';
$username = 'username';
$password = 'password';
$options = array(
    PDO::MYSQL_ATTR_INIT_COMMAND => 'SET NAMES utf8',
); 

$dbh = new PDO($dsn, $username, $password, $options);
?>
```

### 范例

**示例 \#2 PDO\_MYSQL DSN examples**

The following example shows a PDO\_MYSQL DSN for connecting to MySQL
databases:

    mysql:host=localhost;dbname=testdb

More complete examples:

    mysql:host=localhost;port=3307;dbname=testdb
    mysql:unix_socket=/tmp/mysql.sock;dbname=testdb

### 注释

> **Note**: **Unix only:**  
>
> When the host name is set to *"localhost"*, then the connection to the
> server is made thru a domain socket. If PDO\_MYSQL is compiled against
> libmysqlclient then the location of the socket file is at
> libmysqlclient's compiled in location. If PDO\_MYSQL is compiled
> against mysqlnd a default socket can be set thru the
> <a href="/book/pdo.html#" class="link">pdo_mysql.default_socket</a>
> setting.

**目录**

-   [PDO\_MYSQL DSN](/book/pdo.html#PDO_MYSQL%20DSN) — Connecting to
    MySQL databases

简介
----

PDO\_SQLSRV is a driver that implements the
<a href="/book/pdo.html#简介" class="link">PHP Data Objects (PDO) interface</a>
to enable access from PHP to MS SQL Server (starting with SQL Server
2005) and SQL Azure databases.

安装
----

The PDO\_SQLSRV extension is enabled by adding appropriate DLL file to
your PHP extension directory and the corresponding entry to the
`php.ini` file. The PDO\_SQLSRV download comes 8 driver files, four of
which are for PDO support. If you are running non-thread-safe PHP (PHP
5.3), use the php\_pdo\_sqlsrv\_53\_nts.dll file. (You should use a
non-thread-safe version if you are using IIS as your web server). If you
are running thread-safe PHP, use the php\_pdo\_sqlsrv\_53\_ts.dll file.
Similarly for PHP 5.4, use the php\_pdo\_sqlsrv\_54\_nts.dll or
php\_pdo\_sqlsrv\_54\_ts.dll depending on whether your PHP installation
is non-thread-safe or thread-safe.

The most recent version of the driver is available for download here:
<a href="http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx" class="link external">» SQLSRV download</a>.
If you need support for PHP 5.2 and/or PHP compiled with VC6, use the
2.0 release of the driver:
<a href="http://download.microsoft.com/download/C/D/B/CDB0A3BB-600E-42ED-8D5E-E4630C905371/SQLSRV20.EXE" class="link external">» SQLSRV 2.0 download</a>.
The driver sources are hosted in a
<a href="https://github.com/microsoft/msphpsql" class="link external">» public repository</a>.

For more information about system requirements, see
<a href="http://msdn.microsoft.com/en-us/library/cc296170.aspx" class="link external">» SQLSRV System Requirements</a>.

The PDO\_SQLSRV extension is only compatible with PHP running on
Windows. For Linux, see
<a href="/book/pdo.html#ODBC%20and%20DB2%20(PDO)" class="link">ODBC</a>
and
<a href="http://www.microsoft.com/download/en/details.aspx?id=28160" class="link external">» Microsoft's SQL Server ODBC Driver for Linux</a>.

预定义常量
----------

下列常量由此驱动定义，且仅在扩展编译入 PHP
或在运行时动态载入时可用。另外，使用此驱动时，仅会使用这些驱动特定的常量。使用其他驱动的驱动特定的常量可能会导致不可预见的情况。如果代码可运行于多个驱动，<span
class="function">PDO::getAttribute</span> 可被用于获取
**`PDO_ATTR_DRIVER_NAME`** 属性以检查驱动。

**`PDO::SQLSRV_TXN_READ_UNCOMMITTED`** (<span class="type">int</span>)  
<span class="simpara"> This constant is an acceptable value for the
SQLSRV DSN key TransactionIsolation. This constant sets the transaction
isolation level for the connection to Read Uncommitted. </span>

**`PDO::SQLSRV_TXN_READ_COMMITTED`** (<span class="type">int</span>)  
<span class="simpara"> This constant is an acceptable value for the
SQLSRV DSN key TransactionIsolation. This constant sets the transaction
isolation level for the connection to Read Committed. </span>

**`PDO::SQLSRV_TXN_REPEATABLE_READ`** (<span class="type">int</span>)  
<span class="simpara"> This constant is an acceptable value for the
SQLSRV DSN key TransactionIsolation. This constant sets the transaction
isolation level for the connection to Repeateable Read. </span>

**`PDO::SQLSRV_TXN_SNAPSHOT`** (<span class="type">int</span>)  
<span class="simpara"> This constant is an acceptable value for the
SQLSRV DSN key TransactionIsolation. This constant sets the transaction
isolation level for the connection to Snapshot. </span>

**`PDO::SQLSRV_TXN_SERIALIZABLE`** (<span class="type">int</span>)  
<span class="simpara"> This constant is an acceptable value for the
SQLSRV DSN key TransactionIsolation. This constant sets the transaction
isolation level for the connection to Serializable. </span>

**`PDO::SQLSRV_ENCODING_BINARY`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that data is sent/retrieved as a raw
byte stream to/from the server without performing encoding or
translation. This constant can be passed to PDOStatement::setAttribute,
PDO::prepare, PDOStatement::bindColumn, and PDOStatement::bindParam.
</span>

**`PDO::SQLSRV_ENCODING_SYSTEM`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that data is sent/retrieved to/from the
server as 8-bit characters as specified in the code page of the Windows
locale that is set on the system. Any multi-byte characters or
characters that do not map into this code page are substituted with a
single byte question mark (?) character. This constant can be passed to
PDOStatement::setAttribute, PDO::setAttribute, PDO::prepare,
PDOStatement::bindColumn, and PDOStatement::bindParam. </span>

**`PDO::SQLSRV_ENCODING_UTF8`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that data is sent/retrieved to/from the
server in UTF-8 encoding. This is the default encoding. This constant
can be passed to PDOStatement::setAttribute, PDO::setAttribute,
PDO::prepare, PDOStatement::bindColumn, and PDOStatement::bindParam.
</span>

**`PDO::SQLSRV_ENCODING_DEFAULT`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that data is sent/retrieved to/from the
server according to PDO::SQLSRV\_ENCODING\_SYSTEM if specified during
connection. The connection's encoding is used if specified in a prepare
statement. This constant can be passed to PDOStatement::setAttribute,
PDO::setAttribute, PDO::prepare, PDOStatement::bindColumn, and
PDOStatement::bindParam. </span>

**`PDO::SQLSRV_ATTR_QUERY_TIMEOUT`** (<span class="type">int</span>)  
<span class="simpara"> A non-negative integer representing the timeout
period, in seconds. Zero (0) is the default and means no timeout. This
constant can be passed to PDOStatement::setAttribute, PDO::setAttribute,
and PDO::prepare. </span>

**`PDO::SQLSRV_ATTR_DIRECT_QUERY`** (<span class="type">int</span>)  
<span class="simpara"> Indicates that a query should be executed
directly, without being prepared. This constant can be passed to
PDO::setAttribute, and PDO::prepare. For more information, see
<a href="http://msdn.microsoft.com/en-us/library/ff754356.aspx" class="link external">» Direct and Prepared Statement Execution</a>.
</span>

PDO\_SQLSRV DSN
===============

Connecting to MS SQL Server and SQL Azure databases

### 说明

The PDO\_SQLSRV Data Source Name (DSN) is composed of the following
elements:

DSN prefix  
The DSN prefix is **`sqlsrv:`**.

*APP*  
The application name used in tracing.

*ConnectionPooling*  
Specifies whether the connection is assigned from a connection pool (1
or **`TRUE`**) or not (0 or **`FALSE`**).

*Database*  
The name of the database.

*Encrypt*  
Specifies whether the communication with SQL Server is encrypted (1 or
**`TRUE`**) or unencrypted (0 or **`FALSE`**).

*Failover\_Partner*  
Specifies the server and instance of the database's mirror (if enabled
and configured) to use when the primary server is unavailable.

*LoginTimeout*  
Specifies the number of seconds to wait before failing the connection
attempt.

*MultipleActiveResultSets*  
Disables or explicitly enables support for multiple active Result sets
(MARS).

*QuotedId*  
Specifies whether to use SQL-92 rules for quoted identifiers (1 or
**`TRUE`**) or to use legacy Transact-SQL rules (0 or **`FALSE`**).

*Server*  
The name of the database server.

*TraceFile*  
Specifies the path for the file used for trace data.

*TraceOn*  
Specifies whether ODBC tracing is enabled (1 or **`TRUE`**) or disabled
(0 or **`FALSE`**) for the connection being established.

*TransactionIsolation*  
Specifies the transaction isolation level. The accepted values for this
option are PDO::SQLSRV\_TXN\_READ\_UNCOMMITTED,
PDO::SQLSRV\_TXN\_READ\_COMMITTED, PDO::SQLSRV\_TXN\_REPEATABLE\_READ,
PDO::SQLSRV\_TXN\_SNAPSHOT, and PDO::SQLSRV\_TXN\_SERIALIZABLE.

*TrustServerCertificate*  
Specifies whether the client should trust (1 or **`TRUE`**) or reject (0
or **`FALSE`**) a self-signed server certificate.

*WSID*  
Specifies the name of the computer for tracing.

### 范例

**示例 \#1 PDO\_SQLSRV DSN examples**

The following example shows how to connecto to a specified MS SQL Server
database:

    $c = new PDO("sqlsrv:Server=localhost;Database=testdb", "UserName", "Password");

The following example shows how to connect to a MS SQL Server database
on a specified port:

    $c = new PDO("sqlsrv:Server=localhost,1521;Database=testdb", "UserName", "Password");

The following example shows how to connecto to a SQL Azure database with
server ID 12345abcde. Note that when you connect to SQL Azure with PDO,
your username will be UserName@12345abcde (UserName@ServerId).

    $c = new PDO("sqlsrv:Server=12345abcde.database.windows.net;Database=testdb", "UserName@12345abcde", "Password");

**目录**

-   [PDO\_SQLSRV DSN](/book/pdo.html#PDO_SQLSRV%20DSN) — Connecting to
    MS SQL Server and SQL Azure databases

安装
----

If the Oracle Database is on the same machine as PHP, the database
software already contains the necessary libraries. When PHP is on a
different machine, use the free
<a href="https://www.oracle.com/database/technologies/instant-client.html" class="link external">» Oracle Instant Client</a>
libraries. For details refer to the
<a href="/book/oci8.html#需求" class="link">OCI8 Requirements</a>
section.

Use **--with-pdo-oci\[=DIR\]** to install the PDO Oracle OCI extension,
where the optional *\[=DIR\]* is the Oracle Home directory. *\[=DIR\]*
defaults to the `$ORACLE_HOME` environment variable.

Use **--with-pdo-oci=instantclient,prefix,version** for an Oracle
Instant Client SDK, where prefix and version are configured.

    // Using $ORACLE_HOME
    $ ./configure --with-pdo-oci

    // Using OIC for Linux with 10.2.0.3 RPMs with a /usr prefix
    $ ./configure --with-pdo-oci=instantclient,/usr,10.2.0.3

预定义常量
----------

下列常量由此驱动定义，且仅在扩展编译入 PHP
或在运行时动态载入时可用。另外，使用此驱动时，仅会使用这些驱动特定的常量。使用其他驱动的驱动特定的常量可能会导致不可预见的情况。如果代码可运行于多个驱动，<span
class="function">PDO::getAttribute</span> 可被用于获取
**`PDO_ATTR_DRIVER_NAME`** 属性以检查驱动。

**`PDO::OCI_ATTR_ACTION`** (<span class="type">int</span>)  
Provides a way to specify the action on the database session.

自以下版本起 PHP 7.2.16 and 7.3.3

**`PDO::OCI_ATTR_CLIENT_INFO`** (<span class="type">int</span>)  
Provides a way to specify the client info on the database session.

自以下版本起 PHP 7.2.16 and 7.3.3

**`PDO::OCI_ATTR_CLIENT_IDENTIFIER`** (<span class="type">int</span>)  
Provides a way to specify the client identifier on the database session.

自以下版本起 PHP 7.2.16 and 7.3.3

**`PDO::OCI_ATTR_MODULE`** (<span class="type">int</span>)  
Provides a way to specify the module on the database session.

自以下版本起 PHP 7.2.16 and 7.3.3

PDO\_OCI DSN
============

Connecting to Oracle databases

### 说明

The PDO\_OCI Data Source Name (DSN) is composed of the following
elements:

DSN prefix  
The DSN prefix is **`oci:`**.

*dbname* (Oracle Instant Client)  
The URI for the Oracle Instant Client connection takes the form of
`dbname=//hostname:port-number/database`. If you are connecting to a
database defined in `tnsnames.ora`, use only the name of the database:
`dbname=database`.

*charset*  
The client-side character set for the current environment handle.

### 范例

**示例 \#1 PDO\_OCI DSN examples**

The following examples show a PDO\_OCI DSN for connecting to Oracle
databases:

    // Connect to a database defined in tnsnames.ora
    oci:dbname=mydb

    // Connect using the Oracle Instant Client
    oci:dbname=//localhost:1521/mydb

**目录**

-   [PDO\_OCI DSN](/book/pdo.html#PDO_OCI%20DSN) — Connecting to Oracle
    databases

简介
----

PDO\_ODBC is a driver that implements the
<a href="/book/pdo.html#简介" class="link">PHP Data Objects (PDO) interface</a>
to enable access from PHP to databases through ODBC drivers or through
the IBM DB2 Call Level Interface (DB2 CLI) library. PDO\_ODBC currently
supports three different "flavours" of database drivers:

ibm-db2  
Supports access to IBM DB2 Universal Database, Cloudscape, and Apache
Derby servers through the free DB2 express-C client.

unixODBC  
Supports access to database servers through the unixODBC driver manager
and the database's own ODBC drivers.

generic  
Offers a compile option for ODBC driver managers that are not explicitly
supported by PDO\_ODBC.

On Windows, `php_pdo_odbc.dll` has to be enabled as extension in
`php.ini`. It is linked against the Windows ODBC Driver Manager so that
PHP can connect to any database cataloged as a System DSN, and is the
recommended driver for connecting to Microsoft SQL Server databases.

安装
----

**PDO\_ODBC on UNIX systems**

1.  As of PHP 5.1, PDO\_ODBC is included in the PHP source. You can
    compile the PDO\_ODBC extension as either a static or shared module
    using the following **configure** commands.

    ibm\_db2  
        ./configure --with-pdo-odbc=ibm-db2,/opt/IBM/db2/V8.1/

    To build PDO\_ODBC with the ibm-db2 flavour, you have to have
    previously installed the DB2 application development headers on the
    same machine on which you are compiling PDO\_ODBC. The DB2
    application development headers are an installable option in the DB2
    servers, and are also available as part of the DB2 Application
    Development Client freely available for download from the IBM
    developerWorks
    <a href="https://www.ibm.com/developerworks/downloads/im/db2express/index.html" class="link external">» website</a>.

    If you do not supply a location for the DB2 libraries and headers to
    the **configure** command, PDO\_ODBC defaults to
    `/home/db2inst1/sqllib`.

    unixODBC  
        ./configure --with-pdo-odbc=unixODBC,/usr/local

    If you do not supply a location for the unixODBC libraries and
    headers to the **configure** command, PDO\_ODBC defaults to
    `/usr/local`.

    generic  
        ./configure --with-pdo-odbc=generic,/usr/local,libname,ldflags,cflags

预定义常量
----------

下列常量由此驱动定义，且仅在扩展编译入 PHP
或在运行时动态载入时可用。另外，使用此驱动时，仅会使用这些驱动特定的常量。使用其他驱动的驱动特定的常量可能会导致不可预见的情况。如果代码可运行于多个驱动，<span
class="function">PDO::getAttribute</span> 可被用于获取
**`PDO_ATTR_DRIVER_NAME`** 属性以检查驱动。

**`PDO::ODBC_ATTR_USE_CURSOR_LIBRARY`** (<span class="type">int</span>)  
This option controls whether the ODBC cursor library is used. The ODBC
cursor library supports some advanced ODBC features (e.g. block
scrollable cursors), which may not be implemented by the driver. The
following values are supported:

-   **`PDO::ODBC_SQL_USE_IF_NEEDED`** (the default): use the ODBC cursor
    library when needed.

-   **`PDO::ODBC_SQL_USE_DRIVER`**: never use the ODBC cursor library.

-   **`PDO::ODBC_SQL_USE_ODBC`**: always use the ODBC cursor library.

**`PDO::ODBC_ATTR_ASSUME_UTF8`** (<span class="type">bool</span>)  
Windows only. If **`TRUE`**, UTF-16 encoded character data (*CHAR*,
*VARCHAR* and *LONGVARCHAR*) is converted to UTF-8 when reading from or
writing data to the database. If **`FALSE`** (the default), no character
encoding conversion is done.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                   | 默认     | 可修改范围       | 更新日志                                                        |
|------------------------------------------------------------------------|----------|------------------|-----------------------------------------------------------------|
| <a href="/book/pdo.html#" class="link">pdo_odbc.connection_pooling</a> | "strict" | PHP\_INI\_ALL    | Available since PHP 5.1.0.                                      |
| <a href="/book/pdo.html#" class="link">pdo_odbc.db2_instance_name</a>  | NULL     | PHP\_INI\_SYSTEM | Available since PHP 5.1.1. 本过时特性*将*肯定会在未来被*移除*。 |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`pdo_odbc.connection_pooling` <span class="type">string</span>  
Whether to pool ODBC connections. Can be one of *"strict"*, *"relaxed"*
or *"off"* (equals to *""*). The parameter describes how strict the
connection manager should be when matching connection parameters to
existing pooled connections. **`strict`** is the recommend default, and
will result in the use of cached connections only when all the
connection parameters match exactly. **`relaxed`** will result in the
use of cached connections when similar connection parameters are used.
This can result in increased use of the cache, at the risk of bleeding
connection information between (for example) virtual hosts.

This setting can only be changed from the `php.ini` file, and affects
the entire process; any other modules loaded into the process that use
the same ODBC libraries will be affected too, including the
<a href="/book/uodbc.html#ODBC%20函数" class="link">Unified ODBC extension</a>.

**Warning**
**`relaxed`** matching should not be used on a shared server, for
security reasons.

**小贴士**
Leave this setting at the default **`strict`** setting unless you have
good reason to change it.

`pdo_odbc.db2_instance_name` <span class="type">string</span>  
If you compile PDO\_ODBC using the *db2* flavour, this setting sets the
value of the DB2INSTANCE environment variable on Linux and UNIX
operating systems to the specified name of the DB2 instance. This
enables PDO\_ODBC to resolve the location of the DB2 libraries and make
cataloged connections to DB2 databases.

This setting can only be changed from the `php.ini` file, and affects
the entire process; any other modules loaded into the process that use
the same ODBC libraries will be affected too, including the
<a href="/book/uodbc.html#ODBC%20函数" class="link">Unified ODBC extension</a>.

This setting has no effect on Windows.

PDO\_ODBC DSN
=============

Connecting to ODBC or DB2 databases

### 说明

The PDO\_ODBC Data Source Name (DSN) is composed of the following
elements:

DSN prefix  
The DSN prefix is **`odbc:`**. If you are connecting to a database
cataloged in the ODBC driver manager or the DB2 catalog, you can append
the cataloged name of the database to the DSN.

DSN  
The name of the database as cataloged in the ODBC driver manager or the
DB2 catalog. Alternately, you can provide a complete ODBC connection
string to connect to a database as described at
<a href="http://www.connectionstrings.com/" class="link external">» http://www.connectionstrings.com/</a>.

*UID*  
The name of the user for the connection. If you specify the user name in
the DSN, PDO ignores the value of the user name argument in the PDO
constructor.

*PWD*  
The password of the user for the connection. If you specify the password
in the DSN, PDO ignores the value of the password argument in the PDO
constructor.

### 范例

**示例 \#1 PDO\_ODBC DSN example (ODBC driver manager)**

The following example shows a PDO\_ODBC DSN for connecting to an ODBC
database cataloged as testdb in the ODBC driver manager:

    odbc:testdb

**示例 \#2 PDO\_ODBC DSN example (IBM DB2 uncataloged connection)**

The following example shows a PDO\_ODBC DSN for connecting to an IBM DB2
database named **`SAMPLE`** using the full ODBC DSN syntax:

    odbc:DRIVER={IBM DB2 ODBC DRIVER};HOSTNAME=localhost;PORT=50000;DATABASE=SAMPLE;PROTOCOL=TCPIP;UID=db2inst1;PWD=ibmdb2;

**示例 \#3 PDO\_ODBC DSN example (Microsoft Access uncataloged
connection)**

The following example shows a PDO\_ODBC DSN for connecting to a
Microsoft Access database stored at **`C:\db.mdb`** using the full ODBC
DSN syntax:

    odbc:Driver={Microsoft Access Driver (*.mdb)};Dbq=C:\\db.mdb;Uid=Admin

**目录**

-   [PDO\_ODBC DSN](/book/pdo.html#PDO_ODBC%20DSN) — Connecting to ODBC
    or DB2 databases

简介
----

PDO\_PGSQL is a driver that implements the
<a href="/book/pdo.html#简介" class="link">PHP Data Objects (PDO) interface</a>
to enable access from PHP to PostgreSQL databases.

资源类型
--------

This extension defines a stream resource returned by <span
class="function">PDO::pgsqlLOBOpen</span>.

安装
----

Use **--with-pdo-pgsql\[=DIR\]** to install the PDO PostgreSQL
extension, where the optional *\[=DIR\]* is the PostgreSQL base install
directory, or the path to *pg\_config*.

    $ ./configure --with-pdo-pgsql

PDO\_PGSQL DSN
==============

Connecting to PostgreSQL databases

### 说明

The PDO\_PGSQL Data Source Name (DSN) is composed of the following
elements, delimited by spaces or semicolons:

DSN prefix  
The DSN prefix is **`pgsql:`**.

*host*  
The hostname on which the database server resides.

*port*  
The port on which the database server is running.

*dbname*  
The name of the database.

*user*  
The name of the user for the connection. If you specify the user name in
the DSN, PDO ignores the value of the user name argument in the PDO
constructor.

*password*  
The password of the user for the connection. If you specify the password
in the DSN, PDO ignores the value of the password argument in the PDO
constructor.

> **Note**:
>
> The *bytea* fields are returned as streams.

### 范例

**示例 \#1 PDO\_PGSQL DSN examples**

The following example shows a PDO\_PGSQL DSN for connecting to a
PostgreSQL database:

    pgsql:host=localhost;port=5432;dbname=testdb;user=bruce;password=mypass

PDO::pgsqlCopyFromArray
=======================

Copy data from PHP array into table

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PDO::pgsqlCopyFromArray</span> ( <span
class="methodparam"><span class="type">string</span>
`$table_name`</span> , <span class="methodparam"><span
class="type">array</span> `$rows`</span> \[, <span
class="methodparam"><span class="type">string</span> `$delimiter`<span
class="initializer"> = '\\t'</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$null_as`<span
class="initializer"> = "\\\\\\\\N"</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$fields`</span>
\]\]\] )

Copies data from `rows` array to table `table_name` using `delimiter` as
fields delimiter and `fields` list

### 参数

`table_name`  
String containing table name

`rows`  
Array of strings with fields separated by `delimiter`

`delimiter`  
Delimiter used in `rows` array

`null_as`  
How to interpret null values

`fields`  
List of fields to insert

### 返回值

Returns **`TRUE`** on success, 或者在失败时返回 **`FALSE`**.

PDO::pgsqlCopyFromFile
======================

Copy data from file into table

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PDO::pgsqlCopyFromFile</span> ( <span
class="methodparam"><span class="type">string</span>
`$table_name`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">string</span> `$delimiter`<span
class="initializer"> = '\\t'</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$null_as`<span
class="initializer"> = "\\\\\\\\N"</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$fields`</span>
\]\]\] )

Copies data from file specified by `filename` into table `table_name`
using `delimiter` as fields delimiter and `fields` list

### 参数

`table_name`  
String containing table name

`filename`  
Filename containing data to import

`delimiter`  
Delimiter used in file specified by `filename`

`null_as`  
How to interpret null values

`fields`  
List of fields to insert

### 返回值

Returns **`TRUE`** on success, 或者在失败时返回 **`FALSE`**.

PDO::pgsqlCopyToArray
=====================

Copy data from database table into PHP array

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">false</span></span> <span
class="methodname">PDO::pgsqlCopyToArray</span> ( <span
class="methodparam"><span class="type">string</span>
`$table_name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$delimiter`<span class="initializer"> =
'\\t'</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$null_as`<span class="initializer"> =
"\\\\\\\\N"</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$fields`</span> \]\]\] )

Copies data from `table` into array using `delimiter` as fields
delimiter and `fields` list

### 参数

`table_name`  
String containing table name

`delimiter`  
Delimiter used in rows

`null_as`  
How to interpret null values

`fields`  
List of fields to export

### 返回值

Returns an array of rows, 或者在失败时返回 **`FALSE`**.

PDO::pgsqlCopyToFile
====================

Copy data from table into file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PDO::pgsqlCopyToFile</span> ( <span
class="methodparam"><span class="type">string</span>
`$table_name`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">string</span> `$delimiter`<span
class="initializer"> = '\\t'</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$null_as`<span
class="initializer"> = "\\\\\\\\N"</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$fields`</span>
\]\]\] )

Copies data from table into file specified by `filename` using
`delimiter` as fields delimiter and `fields` list

### 参数

`table_name`  
String containing table name

`filename`  
Filename to export data

`delimiter`  
Delimiter used in file specified by `filename`

`null_as`  
How to interpret null values

`fields`  
List of fields to insert

### 返回值

Returns **`TRUE`** on success, 或者在失败时返回 **`FALSE`**.

PDO::pgsqlGetNotify
===================

Get asynchronous notification

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">PDO::pgsqlGetNotify</span> (\[ <span
class="methodparam"><span class="type">int</span> `$result_type`<span
class="initializer"> = **`PDO::FETCH_USE_DEFAULT`**</span></span> \[,
<span class="methodparam"><span class="type">int</span>
`$ms_timeout`<span class="initializer"> = 0</span></span> \]\] )

Returns a result set representing a pending asynchronous notification.

### 参数

`result_type`  
The format the result set should be returned as, represented as a
<a href="/book/pdo.html#PDOStatement::fetch" class="link"><strong><code>PDO::FETCH_*</code></strong></a>
constant.

`ms_timeout`  
The length of time to wait for a response, in milliseconds.

### 返回值

If one or more notifications is pending, returns a single row, with
fields *message* and *pid*, otherwise returns **`FALSE`**.

PDO::pgsqlGetPid
================

Get the server PID

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">PDO::pgsqlGetPid</span> ( <span
class="methodparam">void</span> )

Returns the server's PID.

### 返回值

The server's PID.

PDO::pgsqlLOBCreate
===================

Creates a new large object

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">PDO::pgsqlLOBCreate</span> ( <span
class="methodparam">void</span> )

<span class="function">PDO::pgsqlLOBCreate</span> creates a large object
and returns the OID of that object. You may then open a stream on the
object using <span class="function">PDO::pgsqlLOBOpen</span> to read or
write data to it. The OID can be stored in columns of type OID and be
used to reference the large object, without causing the row to grow
arbitrarily large. The large object will continue to live in the
database until it is removed by calling <span
class="function">PDO::pgsqlLOBUnlink</span>.

Large objects can be up to 2GB in size, but are cumbersome to use; you
need to ensure that <span class="function">PDO::pgsqlLOBUnlink</span> is
called prior to deleting the last row that references its OID from your
database. In addition, large objects have no access controls. As an
alternative, try the bytea column type; recent versions of PostgreSQL
allow bytea columns of up to 1GB in size and transparently manage the
storage for optimal row size.

> **Note**: <span class="simpara"> This function must be called within a
> transaction. </span>

### 参数

<span class="function">PDO::pgsqlLOBCreate</span> takes no parameters.

### 返回值

Returns the OID of the newly created large object on success, or
**`FALSE`** on failure.

### 范例

**示例 \#1 A <span class="function">PDO::pgsqlLOBCreate</span> example**

This example creates a new large object and copies the contents of a
file into it. The OID is then stored into a table.

``` php
<?php
$db = new PDO('pgsql:dbname=test host=localhost', $user, $pass);
$db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
$db->beginTransaction();
$oid = $db->pgsqlLOBCreate();
$stream = $db->pgsqlLOBOpen($oid, 'w');
$local = fopen($filename, 'rb');
stream_copy_to_stream($local, $stream);
$local = null;
$stream = null;
$stmt = $db->prepare("INSERT INTO BLOBS (ident, oid) VALUES (?, ?)");
$stmt->execute(array($some_id, $oid));
$db->commit();
?>
```

### 参见

-   <span class="function">PDO::pgsqlLOBOpen</span>
-   <span class="function">PDO::pgsqlLOBUnlink</span>
-   <span class="function">pg\_lo\_create</span>

PDO::pgsqlLOBOpen
=================

Opens an existing large object stream

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">resource</span><span class="type">false</span></span> <span
class="methodname">PDO::pgsqlLOBOpen</span> ( <span
class="methodparam"><span class="type">string</span> `$oid`</span> \[,
<span class="methodparam"><span class="type">string</span> `$mode`<span
class="initializer"> = "rb"</span></span> \] )

<span class="function">PDO::pgsqlLOBOpen</span> opens a stream to access
the data referenced by `oid`. If `mode` is *r*, the stream is opened for
reading, if `mode` is *w*, then the stream will be opened for writing.
You can use all the usual filesystem functions, such as <span
class="function">fread</span>, <span class="function">fwrite</span> and
<span class="function">fgets</span> to manipulate the contents of the
stream.

> **Note**: <span class="simpara"> This function, and all manipulations
> of the large object, must be called and carried out within a
> transaction. </span>

### 参数

`oid`  
A large object identifier.

`mode`  
If mode is *r*, open the stream for reading. If mode is *w*, open the
stream for writing.

### 返回值

Returns a stream resource on success 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 A <span class="function">PDO::pgsqlLOBOpen</span> example**

Following on from the <span class="function">PDO::pgsqlLOBCreate</span>
example, this code snippet retrieves the large object from the database
and outputs it to the browser.

``` php
<?php
$db = new PDO('pgsql:dbname=test host=localhost', $user, $pass);
$db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
$db->beginTransaction();
$stmt = $db->prepare("select oid from BLOBS where ident = ?");
$stmt->execute(array($some_id));
$stmt->bindColumn('oid', $oid, PDO::PARAM_STR);
$stmt->fetch(PDO::FETCH_BOUND);
$stream = $db->pgsqlLOBOpen($oid, 'r');
header("Content-type: application/octet-stream");
fpassthru($stream);
?>
```

### 参见

-   <span class="function">PDO::pgsqlLOBCreate</span>
-   <span class="function">PDO::pgsqlLOBUnlink</span>
-   <span class="function">pg\_lo\_open</span>

PDO::pgsqlLOBUnlink
===================

Deletes the large object

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PDO::pgsqlLOBUnlink</span> ( <span
class="methodparam"><span class="type">string</span> `$oid`</span> )

Deletes a large object from the database identified by OID.

> **Note**: <span class="simpara"> This function must be called within a
> transaction. </span>

### 参数

`oid`  
A large object identifier

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 A <span class="function">PDO::pgsqlLOBUnlink</span> example**

This example unlinks a large object from the database prior to deleting
the row that references it from the blobs table we've been using in our
<span class="function">PDO::pgsqlLOBCreate</span> and <span
class="function">PDO::pgsqlLOBOpen</span> examples.

``` php
<?php
$db = new PDO('pgsql:dbname=test host=localhost', $user, $pass);
$db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
$db->beginTransaction();
$db->pgsqlLOBUnlink($oid);
$stmt = $db->prepare("DELETE FROM BLOBS where ident = ?");
$stmt->execute(array($some_id));
$db->commit();
?>
```

### 参见

-   <span class="function">PDO::pgsqlLOBOpen</span>
-   <span class="function">PDO::pgsqlLOBCreate</span>

**目录**

-   [PDO\_PGSQL DSN](/book/pdo.html#PDO_PGSQL%20DSN) — Connecting to
    PostgreSQL databases
-   [PDO::pgsqlCopyFromArray](/book/pdo.html#PDO::pgsqlCopyFromArray) —
    Copy data from PHP array into table
-   [PDO::pgsqlCopyFromFile](/book/pdo.html#PDO::pgsqlCopyFromFile) —
    Copy data from file into table
-   [PDO::pgsqlCopyToArray](/book/pdo.html#PDO::pgsqlCopyToArray) — Copy
    data from database table into PHP array
-   [PDO::pgsqlCopyToFile](/book/pdo.html#PDO::pgsqlCopyToFile) — Copy
    data from table into file
-   [PDO::pgsqlGetNotify](/book/pdo.html#PDO::pgsqlGetNotify) — Get
    asynchronous notification
-   [PDO::pgsqlGetPid](/book/pdo.html#PDO::pgsqlGetPid) — Get the server
    PID
-   [PDO::pgsqlLOBCreate](/book/pdo.html#PDO::pgsqlLOBCreate) — Creates
    a new large object
-   [PDO::pgsqlLOBOpen](/book/pdo.html#PDO::pgsqlLOBOpen) — Opens an
    existing large object stream
-   [PDO::pgsqlLOBUnlink](/book/pdo.html#PDO::pgsqlLOBUnlink) — Deletes
    the large object

简介
----

PDO\_SQLITE is a driver that implements the
<a href="/book/pdo.html#简介" class="link">PHP Data Objects (PDO) interface</a>
to enable access to SQLite 3 databases.

> **Note**:
>
> PDO\_SQLITE allows using strings apart from streams together with
> **`PDO::PARAM_LOB`**.

安装
----

The PDO\_SQLITE PDO driver is enabled by default. To disable,
**--without-pdo-sqlite\[=DIR\]** may be used, where the optional
*\[=DIR\]* is the sqlite base install directory. As of PHP 7.4.0
<a href="http://sqlite.org/" class="link external">» libsqlite</a> ≥
3.5.0 is required. Formerly, the bundled libsqlite could have been used
instead, and was the default, if *\[=DIR\]* has been omitted.

> **Note**: **Additional setup on Windows as of PHP 7.4.0**  
>
> 为了使此扩展生效， DLL 文件必须能在 Windows 系统的 `PATH`
> 指示的路径下找到。如何操作的信息，请参见题为“<a href="/faq/installation.html#faq.installation.addtopath" class="link">如何在 Windows 中将 PHP 目录加到 PATH 中</a>”的FAQ。虽然将
> DLL 文件从 PHP 文件夹复制到 Windows 系统目录也行，但不建议这样做。
> *此扩展需要下列文件在 `PATH` 路径中：* `libsqlite3.dll`.

PDO\_SQLITE DSN
===============

Connecting to SQLite databases

### 说明

The PDO\_SQLITE Data Source Name (DSN) is composed of the following
elements:

DSN prefix (SQLite 3)  
The DSN prefix is **`sqlite:`**.

-   To access a database on disk, the absolute path has to be appended
    to the DSN prefix.

-   To create a database in memory, *:memory:* has to be appended to the
    DSN prefix.

-   If the DSN consists of the DSN prefix only, a temporary database is
    used, which is deleted when the connection is closed.

### 范例

**示例 \#1 PDO\_SQLITE DSN examples**

The following examples show PDO\_SQLITE DSN for connecting to SQLite
databases:

    sqlite:/opt/databases/mydb.sq3
    sqlite::memory:
    sqlite:

PDO::sqliteCreateAggregate
==========================

Registers an aggregating User Defined Function for use in SQL statements

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PDO::sqliteCreateAggregate</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$step_func`</span> , <span
class="methodparam"><span class="type">callable</span>
`$finalize_func`</span> \[, <span class="methodparam"><span
class="type">int</span> `$num_args`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

This method is similar to
<a href="/book/pdo.html#PDO::sqliteCreateFunction" class="xref"></a>
except that it registers functions that can be used to calculate a
result aggregated across all the rows of a query.

The key difference between this method and
<a href="/book/pdo.html#PDO::sqliteCreateFunction" class="xref"></a> is
that two functions are required to manage the aggregate.

### 参数

`function_name`  
The name of the function used in SQL statements.

`step_func`  
Callback function called for each row of the result set. Your PHP
function should accumulate the result and store it in the aggregation
context.

This function need to be defined as:

<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">step</span></span> ( <span class="methodparam"><span
class="type">mixed</span> `$context`</span> , <span
class="methodparam"><span class="type">int</span> `$rownumber`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> , <span class="methodparam"><span
class="type">mixed</span> `$values`</span> )

`context`  
**`NULL`** for the first row; on subsequent rows it will have the value
that was previously returned from the step function; you should use this
to maintain the aggregate state.

`rownumber`  
The current row number.

`value`  
The first argument passed to the aggregate.

`values`  
Further arguments passed to the aggregate.

The return value of this function will be used as the `context` argument
in the next call of the step or finalize functions.

`finalize_func`  
Callback function to aggregate the "stepped" data from each row. Once
all the rows have been processed, this function will be called and it
should then take the data from the aggregation context and return the
result. This callback function should return a type understood by SQLite
(i.e.
<a href="/language/types/intro.html" class="link">scalar type</a>).

This function need to be defined as:

<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">fini</span></span> ( <span class="methodparam"><span
class="type">mixed</span> `$context`</span> , <span
class="methodparam"><span class="type">int</span> `$rowcount`</span> )

`context`  
Holds the return value from the very last call to the step function.

`rowcount`  
Holds the number of rows over which the aggregate was performed.

The return value of this function will be used as the return value for
the aggregate.

`num_args`  
Hint to the SQLite parser if the callback function accepts a
predetermined number of arguments.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 max\_length aggregation function example**

``` php
<?php
$data = array(
   'one',
   'two',
   'three',
   'four',
   'five',
   'six',
   'seven',
   'eight',
   'nine',
   'ten',
   );
$db = new PDO('sqlite::memory:');
$db->exec("CREATE TABLE strings(a)");
$insert = $db->prepare('INSERT INTO strings VALUES (?)');
foreach ($data as $str) {
    $insert->execute(array($str));
}
$insert = null;

function max_len_step($context, $rownumber, $string) 
{
    if (strlen($string) > $context) {
        $context = strlen($string);
    }
    return $context;
}

function max_len_finalize($context, $rowcount) 
{
    return $context === null ? 0 : $context;
}

$db->sqliteCreateAggregate('max_len', 'max_len_step', 'max_len_finalize');

var_dump($db->query('SELECT max_len(a) from strings')->fetchAll());

?>
```

In this example, we are creating an aggregating function that will
calculate the length of the longest string in one of the columns of the
table. For each row, the *max\_len\_step* function is called and passed
a *$context* parameter. The context parameter is just like any other PHP
variable and be set to hold an array or even an object value. In this
example, we are simply using it to hold the maximum length we have seen
so far; if the *$string* has a length longer than the current maximum,
we update the context to hold this new maximum length.

After all of the rows have been processed, SQLite calls the
*max\_len\_finalize* function to determine the aggregate result. Here,
we could perform some kind of calculation based on the data found in the
*$context*. In our simple example though, we have been calculating the
result as the query progressed, so we simply need to return the context
value.

**小贴士**

It is NOT recommended for you to store a copy of the values in the
context and then process them at the end, as you would cause SQLite to
use a lot of memory to process the query - just think of how much memory
you would need if a million rows were stored in memory, each containing
a string 32 bytes in length.

**小贴士**

You can use
<a href="/book/pdo.html#PDO::sqliteCreateFunction" class="xref"></a> and
<a href="/book/pdo.html#PDO::sqliteCreateAggregate" class="xref"></a> to
override SQLite native SQL functions.

### 参见

-   <a href="/book/pdo.html#PDO::sqliteCreateFunction" class="xref"></a>
-   <span class="function">sqlite\_create\_function</span>
-   <span class="function">sqlite\_create\_aggregate</span>

PDO::sqliteCreateCollation
==========================

Registers a User Defined Function for use as a collating function in SQL
statements

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PDO::sqliteCreateCollation</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`name`  
Name of the SQL collating function to be created or redefined.

`callback`  
The name of a PHP function or user-defined function to apply as a
callback, defining the behavior of the collation. It should accept two
strings and return as strcmp() does, i.e. it should return -1, 1, or 0
if the first string sorts before, sorts after, or is equal to the
second.

This function need to be defined as:

<span class="type">int</span> <span class="methodname"><span
class="replaceable">collation</span></span> ( <span
class="methodparam"><span class="type">string</span> `$string1`</span> ,
<span class="methodparam"><span class="type">string</span>
`$string2`</span> )

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">PDO::sqliteCreateCollation</span>
example**

``` php
<?php
$db = new PDO('sqlite::memory:');
$db->exec("CREATE TABLE test (col1 string)");
$db->exec("INSERT INTO test VALUES ('a1')");
$db->exec("INSERT INTO test VALUES ('a10')");
$db->exec("INSERT INTO test VALUES ('a2')");

$db->sqliteCreateCollation('NATURAL_CMP', 'strnatcmp');
foreach ($db->query("SELECT col1 FROM test ORDER BY col1") as $row) {
  echo $row['col1'] . "\n";
}
echo "\n";
foreach ($db->query("SELECT col1 FROM test ORDER BY col1 COLLATE NATURAL_CMP") as $row) {
  echo $row['col1'] . "\n";
}
?>
```

以上例程会输出：

    a1
    a10
    a2

    a1
    a2
    a10

PDO::sqliteCreateFunction
=========================

Registers a User Defined Function for use in SQL statements

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PDO::sqliteCreateFunction</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">int</span> `$num_args`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \]\] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

This method allows you to register a PHP function with SQLite as an UDF
(User Defined Function), so that it can be called from within your SQL
statements.

The UDF can be used in any SQL statement that can call functions, such
as SELECT and UPDATE statements and also in triggers.

### 参数

`function_name`  
The name of the function used in SQL statements.

`callback`  
Callback function to handle the defined SQL function.

> **Note**: <span class="simpara"> Callback functions should return a
> type understood by SQLite (i.e.
> <a href="/language/types/intro.html" class="link">scalar type</a>).
> </span>

This function need to be defined as:

<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$values`</span> )

`value`  
The first argument passed to the SQL function.

`values`  
Further arguments passed to the SQL function.

`num_args`  
The number of arguments that the SQL function takes. If this parameter
is *-1*, then the SQL function may take any number of arguments.

`flags`  
A bitwise conjunction of flags. Currently, only
**`PDO::SQLITE_DETERMINISTIC`** is supported, which specifies that the
function always returns the same result given the same inputs within a
single SQL statement.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                  |
|-------|---------------------------------------|
| 7.1.4 | The `flags` parameter has been added. |

### 范例

**示例 \#1 <span class="function">PDO::sqliteCreateFunction</span>
example**

``` php
<?php
function md5_and_reverse($string) 
{
    return strrev(md5($string));
}

$db = new PDO('sqlite:sqlitedb');
$db->sqliteCreateFunction('md5rev', 'md5_and_reverse', 1);
$rows = $db->query('SELECT md5rev(filename) FROM files')->fetchAll();
?>
```

In this example, we have a function that calculates the md5 sum of a
string, and then reverses it. When the SQL statement executes, it
returns the value of the filename transformed by our function. The data
returned in *$rows* contains the processed result.

The beauty of this technique is that you do not need to process the
result using a
<a href="/control-structures/foreach.html" class="link">foreach</a> loop
after you have queried for the data.

**小贴士**

You can use
<a href="/book/pdo.html#PDO::sqliteCreateFunction" class="xref"></a> and
<a href="/book/pdo.html#PDO::sqliteCreateAggregate" class="xref"></a> to
override SQLite native SQL functions.

### 参见

-   <a href="/book/pdo.html#PDO::sqliteCreateAggregate" class="xref"></a>
-   <span class="function">sqlite\_create\_function</span>
-   <span class="function">sqlite\_create\_aggregate</span>

**目录**

-   [PDO\_SQLITE DSN](/book/pdo.html#PDO_SQLITE%20DSN) — Connecting to
    SQLite databases
-   [PDO::sqliteCreateAggregate](/book/pdo.html#PDO::sqliteCreateAggregate)
    — Registers an aggregating User Defined Function for use in SQL
    statements
-   [PDO::sqliteCreateCollation](/book/pdo.html#PDO::sqliteCreateCollation)
    — Registers a User Defined Function for use as a collating function
    in SQL statements
-   [PDO::sqliteCreateFunction](/book/pdo.html#PDO::sqliteCreateFunction)
    — Registers a User Defined Function for use in SQL statements
