加密存储模型
------------

SSL/SSH 能保护客户端和服务器端交换的数据，但 SSL/SSH
并不能保护数据库中已有的数据。SSL 只是一个加密网络数据流的协议。

如果攻击者取得了直接访问数据库的许可（绕过 web
服务器），敏感数据就可能暴露或者被滥用，除非数据库自己保护了这些信息。对数据库内的数据加密是减少这类风险的有效途径，但是只有很少的数据库提供这些加密功能。

对于这个问题，有一个简单的解决办法，就是创建自己的加密机制，然后把它用在
PHP 程序内。PHP 有几个扩展库可以完成这个工作，比如说
<a href="/ref/mcrypt.html" class="link">Mcrypt</a> 和
<a href="/ref/mhash.html" class="link">Mhash</a>
等，它们包含多种加密运算法则。脚本在插入数据库之前先把数据加密，以后提取出来时再解密。有关加密如何工作的例子请参考相关手册。

对某些真正隐蔽的数据，如果不需要以明文的形式存在（即不用显示），可以考虑用散列算法。使用散列算法最常见的例子就是把密码经过
MD5 加密后的散列存进数据库来代替原来的明文密码。参见 <span
class="function">crypt</span> 和 <span class="function">md5</span>。

**示例 \#1 对密码字段进行散列加密**

``` php
<?php

// 存储密码散列
$query  = sprintf("INSERT INTO users(name,pwd) VALUES('%s','%s');",
            pg_escape_string($username), md5($password));
$result = pg_query($connection, $query);

// 发送请求来验证用户密码
$query = sprintf("SELECT 1 FROM users WHERE name='%s' AND pwd='%s';",
            pg_escape_string($username), md5($password));
$result = pg_query($connection, $query);

if (pg_num_rows($result) > 0) {
    echo 'Welcome, $username!';
} else {
    echo 'Authentication failed for $username.';
}

?>
```
