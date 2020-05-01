扩展中的其他变化
----------------

扩展中行为和新特性的变化:

-   <span class="simpara">
    <a href="/set/mysqlinfo.html#Mysqli" class="link">mysqli</a> - <span
    class="classname">mysqli\_result</span> 现在实现
    <a href="/class/traversable.html" class="link">Traversable</a>
    </span>

<!-- -->

-   <span class="simpara">
    <a href="/book/pdo.html#MySQL%20(PDO)" class="link">pdo_mysql</a> -
    不再支持使用低于 4.1 版本的 MySQL 客户端库连接。 </span>

<!-- -->

-   <span class="simpara"> MySQL 扩展
    <a href="/set/mysqlinfo.html#Mysql（原始）" class="link">mysql</a>
    、<a href="/set/mysqlinfo.html#Mysqli" class="link">mysqli</a> 及
    <a href="/book/pdo.html#MySQL%20(PDO)" class="link">PDO_mysql</a>
    现在使用
    <a href="/set/mysqlinfo.html#Mysqlnd" class="link">mysqlnd</a>
    作为默认库。通过在配置选项中指定路径仍然可以使用 libmysqlclient 。
    </span>

<!-- -->

-   <span class="simpara">
    <a href="/set/mysqlinfo.html#Mysqlnd" class="link">mysqlnd</a> -
    增加支持命名管道 </span>
