数据库问题
==========

本节包括 PHP 和数据库之间关系的常见问题。 事实上， PHP
可以访问如今现有的任何数据库。

1.  [听说 PHP 有可能访问 Microsoft SQL
    Server，怎样访问？](#faq.databases.mssql)
2.  [能访问 Microsoft Access 数据库吗？](#faq.databases.access)
3.  [为什么我已经使用了十多年的 MySQL 扩展（ext/mysql）
    不建议继续使用了？
    它被废弃了吗？我应该选择什么替代方案？如何迁移到新的方案？](#faq.databases.mysql.deprecated)
4.  [为什么我得到类似如下的错误： “Warning: 0 is not a MySQL result
    index in \<file\> on line \<x\>” 或者 “Warning: Supplied argument is
    not a valid MySQL result resource in \<file\> on line
    \<x\>”？](#faq.databases.mysqlresource)

**听说 PHP 有可能访问 Microsoft SQL Server，怎样访问？**  
在 Unix 机器中，你可以使用
<a href="/book/pdo.html#ODBC%20and%20DB2%20(PDO)" class="link">PDO_ODBC</a>
或者 <a href="/book/uodbc.html" class="link">Unified ODBC API</a> 来访问
Microsoft SQL Server 数据库。

在 Windows 机器中，你可以使用
<a href="/book/pdo.html#MS%20SQL%20Server%20(PDO)" class="link">PDO_SQLSRV</a>
或 <a href="/book/sqlsrv.html" class="link">SQLSRV</a> 来访问 Microsoft
SQL Server 数据库。

同时，也可以参考下一个问题。

<!-- -->

**能访问 Microsoft Access 数据库吗？**  
可以。如果完全在 Windows 9x/Me/NT/2000
下运行，那已经有了所有所需的工具， 可以用 ODBC 和 Microsoft's ODBC
drivers for Microsoft Access database。

如果在 Unix 下运行 PHP 而想访问 Windows 中的 MS Access， 那需要 Unix
ODBC 驱动程序。
<a href="http://www.openlinksw.com/" class="link external">» OpenLink Software</a>
有一个基于 Unix 的 ODBC 驱动程序可以做这件事。

另外一个替代方案是用带 Windows ODBC 驱动的 SQL Server 并用它来储存数据，
可以通过 Microsoft Access（用 ODBC）和 PHP（用内置驱动）来访问，
或者用一个 Access 和 PHP 都识别的中间文件格式， 例如 flat 文件或者 dBase
数据库。 关于这一点 OpenLink Software 的 Tim Hayes 写道：

> 当可以通过 ODBC 直接从 PHP 访问数据库时——例如用 OpenLink 的驱动程序，
> 使用其它数据库做中间媒介不是一个好主意。
> 如果确实需要一个中间文件格式， OpenLink 已经发布了对应于 Windows
> NT，Linux 和其它 Unix 平台的 Virtuoso（一个虚拟数据库引擎）。
> 请访问我们的
> <a href="http://www.openlinksw.com/" class="link external">» 网站</a>来免费下载。

还有一个已被证实有效的选择是在 Windows 下用 MySQL 和它的 MyODBC
驱动来同步数据库。 Steve Lawrence 写道：

-   <span class="simpara"> 根据 MySQL 的说明在你的平台上安装
    MySQL。可以从
    <a href="http://www.mysql.com/" class="link external">» http://www.mysql.com/</a>得到最新版。
    除了设定数据库和配置用户帐号以外不需要特殊的配置， 应该在 host
    字段中放一个 % 或者要用来访问 MySQL 的 Windows 机器名。
    记下自己的服务器名， 用户名和密码。 </span>
-   <span class="simpara"> 从 MySQL 网站下载 MyODBC for Windows
    驱动程序。 在你的 Windows 机器中安装它。
    可以用此程序中包括的工具来测试其操作。 </span>
-   <span class="simpara"> 用控制面板中的 ODBC 管理器新建一个用户或系统
    dsn， 设定 dsn 名称， 输入你在第一步中配置的 MySQL
    数据库的主机名，用户名，密码，端口等。 </span>
-   <span class="simpara"> 完整安装 Access，
    这样可以确保得到适当的插件... 至少需要安装 ODBC 支持和连接表管理器。
    </span>
-   <span class="simpara"> 新建一个 Access 数据库。 在 Table
    窗口点击右键并选择 Link Tables， 或者在 File 菜单下选择 Get External
    Data -\> Link Tables。 当文件浏览窗口打开后，选择文件类型为：ODBC。
    接着选择 System dsn 以及在第三步建立的 dsn 的名字。
    再选择要连接的表，点击 OK。 现在你可以在你的 MySQL
    服务器中打开表并新建／删除／编辑数据了！
    也可以构造查询，导入／导出表到 MySQL，构造表单和报告等。 </span>

提示与技巧：

-   <span class="simpara"> 可以在 Access 中构造表并导出到 MySQL 中，
    再把它们连接回来。 这样可以使表的建立更快。 </span>
-   <span class="simpara"> 在 Access 中建立表时，
    必需定义一个基本键名来取得表的写权限。 确认在把表连接到 Access
    之前在 MySQL 中建立了基本键名。 </span>
-   <span class="simpara"> 如果在 MySQL 中修改了表， 必须重新连接到
    Access。 打开 Tools\>Add-ins\>Linked table manager， 找到你的 ODBC
    DSN，然后在这里选择要重新连接的表。 也可以在这里移动 dsn 源， 在点击
    OK 之前选中 “always prompt for new location”。 </span>

<!-- -->

**为什么我已经使用了十多年的 MySQL 扩展（ext/mysql） 不建议继续使用了？ 它被废弃了吗？我应该选择什么替代方案？如何迁移到新的方案？**  
在
<a href="/set/mysqlinfo.html#Choosing%20an%20API" class="link">选择一种 MySQL API</a>
一节中 描述了 3 中 MySQL 扩展。 不应该继续使用旧的 API
了，可能将来的某一天旧 API 就会被废弃甚至从 PHP 中移除。 当然，旧的 API
曾经是非常主流的，很多用户都用了它，所以这个被废弃及移除的过程不会太快。
但是仍然强烈建议使用
<a href="/set/mysqlinfo.html#Mysqli" class="link">mysqli</a> 或
<a href="/book/pdo.html#MySQL%20(PDO)" class="link">PDO_MySQL</a> 来访问
MySQL 数据库。

自动迁移脚本目前还没有。 mysqli API
包括了面向过程和面向对象的两种风格的调用方式，并且面向过程的版本中提供的
API 和 ext/mysql 是非常相似的。

不可以同时混合使用这几种 MySQL API。 例如，你不可以把一个 mysqli
的连接资源传入到 PDO\_MySQL 或者 ext/mysql 中去使用。

<!-- -->

**为什么我得到类似如下的错误： “Warning: 0 is not a MySQL result index in \<file\> on line \<x\>” 或者 “Warning: Supplied argument is not a valid MySQL result resource in \<file\> on line \<x\>”？**  
你试图用一个值为 0 的结果资源号。 0 表示你的查询由于某原因失败了，
需要在提交查询之后 和在使用返回结果资源号之前检查错误。
正确的方法是用类似如下的代码：

``` php
<?php

$result = mysql_query("SELECT * FROM tables_priv");
if (!$result) {
    echo mysql_error();
    exit;
}
?>
```

或者

``` php
<?php

$result = mysql_query("SELECT * FROM tables_priv")
    or die("Bad query: " . mysql_error());
?>
```
