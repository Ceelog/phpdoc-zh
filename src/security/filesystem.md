文件系统安全
============

**目录**

-   [Null 字符问题](/security/filesystem/nullbytes.html)

PHP
遵从大多数服务器系统中关于文件和目录权限的安全机制。这就使管理员可以控制哪些文件在文件系统内是可读的。必须特别注意的是全局的可读文件，并确保每一个有权限的用户对这些文件的读取动作都是安全的。

PHP 被设计为以用户级别来访问文件系统，所以完全有可能通过编写一段 PHP
代码来读取系统文件如
/etc/passwd，更改网络连接以及发送大量打印任务等等。因此必须确保 PHP
代码读取和写入的是合适的文件。

请看下面的代码，用户想要删除自己主目录中的一个文件。假设此情形是通过 web
界面来管理文件系统，因此 Apache 用户有权删除用户目录下的文件。

**示例 \#1 不对变量进行安全检查会导致……**

``` php
<?php
// 从用户目录中删除指定的文件
$username = $_POST['user_submitted_name'];
$userfile = $_POST['user_submitted_filename'];
$homedir = "/home/$username";
unlink ("$homedir/$userfile");
echo "The file has been deleted!";
?>
```

既然 username 和 filename
变量可以通过用户表单来提交，那就可以提交别人的用户名和文件名，甚至可以删掉本来不应该让他们删除的文件。这种情况下，就要考虑其它方式的认证。想想看如果提交的变量是“../etc/”和“passwd”会发生什么。上面的代码就等同于：

**示例 \#2 ……文件系统攻击**

``` php
<?php
// 删除硬盘中任何 PHP 有访问权限的文件。如果 PHP 有 root 权限：
$username = $_POST['user_submitted_name']; // "../etc"
$userfile = $_POST['user_submitted_filename']; // "passwd"
$homedir  = "/home/$username"; // "/home/../etc"

unlink("$homedir/$userfile"); // "/home/../etc/passwd"

echo "The file has been deleted!";
?>
```

有两个重要措施来防止此类问题。

-   <span class="simpara"> 只给 PHP 的 web 用户很有限的权限。 </span>
-   <span class="simpara"> 检查所有提交上来的变量。 </span>

下面是改进的脚本：

**示例 \#3 更安全的文件名检查**

``` php
<?php
// 删除硬盘中 PHP 有权访问的文件
$username = $_SERVER['REMOTE_USER']; // 使用认证机制
$userfile = basename($_POST['user_submitted_filename']);
$homedir = "/home/$username";

$filepath = "$homedir/$userfile";


if (file_exists($filepath) && unlink($filepath)) {
    $logstring = "Deleted $filepath\n";
} else {
    $logstring = "Failed to delete $filepath\n";
}
$fp = fopen("/home/logging/filedelete.log", "a");
fwrite ($fp, $logstring);
fclose($fp);

echo htmlentities($logstring, ENT_QUOTES);
?>
```

然而，这样做仍然是有缺陷的。如果认证系统允许用户建立自己的登录用户名，而用户选择用“../etc/”作为用户名，系统又一次沦陷了。所以，需要加强检查：

**示例 \#4 更安全的文件名检查**

``` php
<?php
$username = $_SERVER['REMOTE_USER']; // 使用认证机制
$userfile     = $_POST['user_submitted_filename'];
$homedir = "/home/$username";

$filepath     = "$homedir/$userfile";
if (!ctype_alnum($username) || !preg_match('/^(?:[a-z0-9_-]|\.(?!\.))+$/iD', $userfile)) {
    die("Bad username/filename");
}
//后略……
?>
```

根据操作系统的不同，存在着各种各样需要注意的文件，包括联系到系统的设备（/dev/
或者 COM1）、配置文件（/ect/ 文件和 .ini文件）、常用的存储区域（/home/
或者 My
Documents）等等。由于此原因，建立一个策略禁止所有权限而只开放明确允许的通常更容易些。
