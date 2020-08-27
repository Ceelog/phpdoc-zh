使用 Register Globals
=====================

**Warning**

本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

可能 PHP 中最具争议的变化就是从 PHP
<a href="https://www.php.net/releases/4_2_0.php" class="link external">» 4.2.0</a>
版开始配置文件中 PHP 指令
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
的默认值从 on 改为 off
了。对此选项的依赖是如此普遍以至于很多人根本不知道它的存在而以为 PHP
本来就是这么工作的。本节会解释用这个指令如何写出不安全的代码，但要知道这个指令本身没有不安全的地方，误用才会。

当 register\_globals 打开以后，各种变量都被注入代码，例如来自 HTML
表单的请求变量。再加上 PHP
在使用变量之前是无需进行初始化的，这就使得更容易写出不安全的代码。这是个很艰难的抉择，但
PHP
社区还是决定默认关闭此选项。当打开时，人们使用变量时确实不知道变量是哪里来的，只能想当然。但是
register\_globals
的关闭改变了这种代码内部变量和客户端发送的变量混杂在一起的糟糕情况。下面举一个错误使用
register\_globals 的例子：

**示例 \#1 错误使用 register\_globals = on 的例子**

``` php
<?php
// 当用户合法的时候，赋值 $authorized = true
if (authenticated_user()) {
    $authorized = true;
}

// 由于并没有事先把 $authorized 初始化为 false，
// 当 register_globals 打开时，可能通过GET auth.php?authorized=1 来定义该变量值
// 所以任何人都可以绕过身份验证
if ($authorized) {
    include "/highly/sensitive/data.php";
}
?>
```

当 register\_globals = on 的时候，上面的代码就会有危险了。如果是
off，`$authorized` 就不能通过如 URL
请求等方式来改变，这样就好多了，尽管初始化变量是一个良好的编程习惯。比如说，如果在上面的代码执行之前加入
*$authorized = false* 的话，无论 register\_globals 是 on 还是 off
都可以，因为用户状态被初始化为未经认证。

另一个例子是关于<a href="/ref/session.html" class="link">会话</a>的。当
register\_globals = on 的时候，`$username`
也可以用在下面的代码中，但要意识到 `$username`
也可能会从其它途径进来，比如说通过 URL 的 GET。

**示例 \#2 使用会话时同时兼容 register\_globals on 和 off 的例子**

``` php
<?php
// 我们不知道 $username 的来源，但很清楚 $_SESSION 是
// 来源于会话数据
if (isset($_SESSION['username'])) {

    echo "Hello <b>{$_SESSION['username']}</b>";

} else {

    echo "Hello <b>Guest</b><br />";
    echo "Would you like to login?";

}
?>
```

采取相应的预防措施以便在伪造变量输入的时候给予警告是完全有可能的。如果事先确切知道变量是哪里来的，就可以检查所提交的数据是否是从不正当的表单提交而来。不过这不能保证变量未被伪造，这需要攻击者去猜测应该怎样去伪造。如果不在乎请求数据来源的话，可以使用
`$_REQUEST` 数组，它包括了 GET、POST 和 COOKIE
的所有数据。详情可参见本手册的<a href="/language/variables/external.html" class="link">来自 PHP 之外的变量</a>。

**示例 \#3 探测有害变量**

``` php
<?php
if (isset($_COOKIE['MAGIC_COOKIE'])) {

    // MAGIC_COOKIE 来自 cookie
    // 这样做是确保是来自 cookie 的数据

} elseif (isset($_GET['MAGIC_COOKIE']) || isset($_POST['MAGIC_COOKIE'])) {

   mail("admin@example.com", "Possible breakin attempt", $_SERVER['REMOTE_ADDR']);
   echo "Security violation, admin has been alerted.";
   exit;

} else {

   // 这一次请求中并没有设置 MAGIC_COOKIE 变量

}
?>
```

当然，单纯地关闭 register\_globals
并不代表所有的代码都安全了。对于每一段提交上来的数据，都要对其进行具体的检查。永远要验证用户数据和对变量进行初始化！把
<span class="function">error\_reporting</span> 设为 **`E_NOTICE`**
级别可以检查未初始化的变量。

更多关于模拟 register\_globals 为 on 或 off 的信息，请见此
<a href="/faq/misc.html#faq.misc.registerglobals" class="link">FAQ</a>。
