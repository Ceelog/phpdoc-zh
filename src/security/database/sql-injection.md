SQL 注入
--------

很多 web 开发者没有注意到 SQL 查询是可以被篡改的，因而把 SQL
查询当作可信任的命令。殊不知道，SQL
查询可以绕开访问控制，从而绕过身份验证和权限检查。更有甚者，有可能通过
SQL 查询去运行主机操作系统级的命令。

直接 SQL 命令注入就是攻击者常用的一种创建或修改已有 SQL
语句的技术，从而达到取得隐藏数据，或覆盖关键的值，甚至执行数据库主机操作系统命令的目的。这是通过应用程序取得用户输入并与静态参数组合成
SQL 查询来实现的。下面将会给出一些真实的例子。

由于在缺乏对输入的数据进行验证，并且使用了超级用户或其它有权创建新用户的数据库帐号来连接，攻击者可以在数据库中新建一个超级用户。

**示例 \#1
一段实现数据分页显示的代码……也可以被用作创建一个超级用户（PostgreSQL系统）。**

``` php
<?php

$offset = $argv[0]; // 注意，没有输入验证！
$query  = "SELECT id, name FROM products ORDER BY name LIMIT 20 OFFSET $offset;";
$result = pg_query($conn, $query);

?>
```

一般的用户会点击 `$offset`
已被斌值的“上一页”、“下一页”的链接。原本代码只会认为 `$offset`
是一个数值。然而，如果有人尝试把以下语句先经过 <span
class="function">urlencode</span> 处理，然后加入URL中的话：

``` sql
0;
insert into pg_shadow(usename,usesysid,usesuper,usecatupd,passwd)
    select 'crack', usesysid, 't','t','crack'
    from pg_shadow where usename='postgres';
--
```

那么他就可以创建一个超级用户了。注意那个 *0;*
只不过是为了提供一个正确的偏移量以便补充完整原来的查询，使它不要出错而已。

> **Note**:
>
> *--* 是 SQL 的注释标记，一般可以使用来它告诉 SQL
> 解释器忽略后面的语句。

对显示搜索结果的页面下手是一个能得到密码的可行办法。攻击者所要做的只不过是找出哪些提交上去的变量是用于
SQL 语句并且处理不当的。而这类的变量通常都被用于 *SELECT*
查询中的条件语句，如 *WHERE, ORDER BY, LIMIT* 和
*OFFSET*。如果数据库支持 *UNION* 构造的话，攻击者还可能会把一个完整的
SQL
查询附加到原来的语句上以便从任意数据表中得到密码。因此，对密码字段加密是很重要的。

**示例 \#2 显示文章……以及一些密码（任何数据库系统）**

``` php
<?php

$query  = "SELECT id, name, inserted, size FROM products
                  WHERE size = '$size'
                  ORDER BY $order LIMIT $limit, $offset;";
$result = odbc_exec($conn, $query);

?>
```

可以在原来的查询的基础上添加另一个 *SELECT* 查询来获得密码：

``` sql
'
union select '1', concat(uname||'-'||passwd) as name, '1971-01-01', '0' from usertable;
--
```

假如上述语句（使用 *'* 和 *--*）被加入到 `$query`
中的任意一个变量的话，那么就麻烦了。

SQL 中的 UPDATE
也会受到攻击。这种查询也可能像上面的例子那样被插入或附加上另一个完整的请求。但是攻击者更愿意对
*SET*
子句下手，这样他们就可以更改数据表中的一些数据。这种情况下必须要知道数据库的结构才能修改查询成功进行。可以通过表单上的变量名对字段进行猜测，或者进行暴力破解。对于存放用户名和密码的字段，命名的方法并不多。

**示例 \#3 从重设密码……到获得更多权限（任何数据库系统）**

``` php
<?php
$query = "UPDATE usertable SET pwd='$pwd' WHERE uid='$uid';";
?>
```

但是恶意的用户会把 *' or uid like'%admin%'; --* 作为变量的值提交给
`$uid` 来改变 admin 的密码，或者把 `$pwd` 的值提交为 *"hehehe',
admin='yes', trusted=100
"*（后面有个空格）去获得更多的权限。这样做的话，查询语句实际上就变成了：

``` php
<?php

// $uid == ' or uid like'%admin%'; --
$query = "UPDATE usertable SET pwd='...' WHERE uid='' or uid like '%admin%'; --";

// $pwd == "hehehe', admin='yes', trusted=100 "
$query = "UPDATE usertable SET pwd='hehehe', admin='yes', trusted=100 WHERE
...;";

?>
```

下面这个可怕的例子将会演示如何在某些数据库上执行系统命令。

**示例 \#4 攻击数据库所在主机的操作系统（MSSQL Server）**

``` php
<?php

$query  = "SELECT * FROM products WHERE id LIKE '%$prod%'";
$result = mssql_query($query);

?>
```

如果攻击提交 *a%' exec master..xp\_cmdshell 'net user test testpass
/ADD' --* 作为变量 `$prod`的值，那么 `$query` 将会变成

``` php
<?php

$query  = "SELECT * FROM products
                    WHERE id LIKE '%a%'
                    exec master..xp_cmdshell 'net user test testpass /ADD'--";
$result = mssql_query($query);

?>
```

MSSQL 服务器会执行这条 SQL
语句，包括它后面那个用于向系统添加用户的命令。如果这个程序是以 *sa*
运行而 MSSQLSERVER
服务又有足够的权限的话，攻击者就可以获得一个系统帐号来访问主机了。

> **Note**:
>
> 虽然以上的例子是针对某一特定的数据库系统的，但是这并不代表不能对其它数据库系统实施类似的攻击。使用不同的方法，各种数据库都有可能遭殃。

### 预防措施

也许有人会自我安慰，说攻击者要知道数据库结构的信息才能实施上面的攻击。没错，确实如此。但没人能保证攻击者一定得不到这些信息，一但他们得到了，数据库有泄露的危险。如果你在用开放源代码的软件包来访问数据库，比如论坛程序，攻击者就很容得到到相关的代码。如果这些代码设计不良的话，风险就更大了。

这些攻击总是建立在发掘安全意识不强的代码上的。所以，永远不要信任外界输入的数据，特别是来自于客户端的，包括选择框、表单隐藏域和
cookie。就如上面的第一个例子那样，就算是正常的查询也有可能造成灾难。

-   <span class="simpara">
    永远不要使用超级用户或所有者帐号去连接数据库。要用权限被严格限制的帐号。
    </span>

-   <span class="simpara"> 检查输入的数据是否具有所期望的数据格式。PHP
    有很多可以用于检查输入的函数，从简单的<a href="/ref/var.html" class="link">变量函数</a>和<a href="/ref/ctype.html" class="link">字符类型函数</a>（比如
    <span class="function">is\_numeric</span>，<span
    class="function">ctype\_digit</span>）到复杂的
    <a href="/ref/pcre.html" class="link">Perl 兼容正则表达式函数</a>都可以完成这个工作。
    </span>

-   如果程序等待输入一个数字，可以考虑使用 <span
    class="function">is\_numeric</span> 来检查，或者直接使用 <span
    class="function">settype</span> 来转换它的类型，也可以用 <span
    class="function">sprintf</span> 把它格式化为数字。

    **示例 \#5 一个实现分页更安全的方法**

    ``` php
    <?php

    settype($offset, 'integer');
    $query = "SELECT id, name FROM products ORDER BY name LIMIT 20 OFFSET $offset;";

    // 请注意格式字符串中的 %d，如果用 %s 就毫无意义了
    $query = sprintf("SELECT id, name FROM products ORDER BY name LIMIT 20 OFFSET %d;",
                     $offset);

    ?>
    ```

-   <span class="simpara"> 使用数据库特定的敏感字符转义函数（比如 <span
    class="function">mysql\_escape\_string</span> 和 <span
    class="function">sql\_escape\_string</span>）把用户提交上来的非数字数据进行转义。如果数据库没有专门的敏感字符转义功能的话
    <span class="function">addslashes</span> 和 <span
    class="function">str\_replace</span>
    可以代替完成这个工作。看看<a href="/security/database/storage.html" class="link">第一个例子</a>，此例显示仅在查询的静态部分加上引号是不够的，查询很容易被攻破。
    </span>

-   <span class="simpara">
    要不择手段避免显示出任何有关数据库的信心，尤其是数据库结构。参见<a href="/security/errors.html" class="link">错误报告</a>和<a href="/ref/errorfunc.html" class="link">错误处理函数</a>。
    </span>

-   <span class="simpara">
    也可以选择使用数据库的存储过程和预定义指针等特性来抽象数库访问，使用户不能直接访问数据表和视图。但这个办法又有别的影响。
    </span>

除此之外，在允许的情况下，使用代码或数据库系统保存查询日志也是一个好办法。显然，日志并不能防止任何攻击，但利用它可以跟踪到哪个程序曾经被尝试攻击过。日志本身没用，要查阅其中包含的信息才行。毕竟，更多的信息总比没有要好。
