新的扩展
--------

PHP 5.3.0 新增以下扩展(默认):

-   <span class="simpara">
    <a href="/book/enchant.html" class="link">Enchant</a> -
    各种拼写库的抽象层 </span>
-   <span class="simpara">
    <a href="/book/fileinfo.html" class="link">文件信息</a> -
    已经被移除的
    <a href="/book/mime-magic.html" class="link">Mimetype</a>
    扩展的一个改进的、更加可靠的替代, 以 BC 为特色. </span>
-   <span class="simpara">
    <a href="/book/intl.html" class="link">INTL</a> - 国际化扩展. INTL
    是
    <a href="http://www.icu-project.org/" class="link external">» ICU</a>
    库的一个包装器. </span>
-   <span class="simpara">
    <a href="/book/phar.html" class="link">Phar</a> - PHP
    档案文件的实现. </span>
-   <span class="simpara">
    <a href="/book/sqlite3.html" class="link">SQLite3</a> - 支持 SQLite
    version 3 数据库. </span>

mysqlnd 是随 PHP 发布的新核心库. 它是 PHP 独有的 libmysql 的替代.
如果系统上未发现 libmysql, mysqlnd 将被用来构建
<a href="/set/mysqlinfo.html#Mysql（原始）" class="link">mysql</a>,
<a href="/set/mysqlinfo.html#Mysqli" class="link">mysqli</a> 和
<a href="/book/pdo.html#MySQL%20(PDO)" class="link">PDO_MySQL</a> 扩展.
甚至 libmysql 存在的情况下, 它也可以被用来代替 libmysql.
由于性能上的原因, 推荐在全部的 PHP 安装中都使用 mysqlnd.
