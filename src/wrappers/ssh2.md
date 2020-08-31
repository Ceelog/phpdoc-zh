ssh2://
=======

Secure Shell 2

### 说明

`ssh2.shell://` `ssh2.exec://` `ssh2.tunnel://` `ssh2.sftp://`
`ssh2.scp://` (PECL)

> **Note**: **该封装器默认没有激活**  
> <span class="simpara"> 为了使用 `ssh2.*://` 封装协议， 你必须安装来自
> <a href="https://pecl.php.net/" class="link external">» PECL</a> 的
> <a href="https://pecl.php.net/package/ssh2" class="link external">» SSH2</a>
> 扩展。 </span>

除了支持传统的 URI 登录信息，ssh2 封装协议也支持通过 URL
的主机（host）部分来复用打开连接。

### 用法

-   <span
    class="simpara">`ssh2.shell://user:pass@example.com:22/xterm`</span>
-   <span
    class="simpara">`ssh2.exec://user:pass@example.com:22/usr/local/bin/somecmd`</span>
-   <span
    class="simpara">`ssh2.tunnel://user:pass@example.com:22/192.168.0.1:14`</span>
-   <span
    class="simpara">`ssh2.sftp://user:pass@example.com:22/path/to/filename`</span>

### 可选项

| 属性                                                                       | ssh2.shell | ssh2.exec | ssh2.tunnel | ssh2.sftp                 | ssh2.scp |
|----------------------------------------------------------------------------|------------|-----------|-------------|---------------------------|----------|
| 受 <a href="/filesystem/setup.html#" class="link">allow_url_fopen</a> 影响 | Yes        | Yes       | Yes         | Yes                       | Yes      |
| 允许读取                                                                   | Yes        | Yes       | Yes         | Yes                       | Yes      |
| 允许写入                                                                   | Yes        | Yes       | Yes         | Yes                       | No       |
| 允许追加                                                                   | No         | No        | No          | Yes（当服务器支持的时候） | No       |
| 允许同时读和写                                                             | Yes        | Yes       | Yes         | Yes                       | No       |
| 支持 <span class="function">stat</span>                                    | No         | No        | No          | Yes                       | No       |
| 支持 <span class="function">unlink</span>                                  | No         | No        | No          | Yes                       | No       |
| 支持 <span class="function">rename</span>                                  | No         | No        | No          | Yes                       | No       |
| 支持 <span class="function">mkdir</span>                                   | No         | No        | No          | Yes                       | No       |
| 支持 <span class="function">rmdir</span>                                   | No         | No        | No          | Yes                       | No       |

| 名称            | 用法                                                                   | 默认                       |
|-----------------|------------------------------------------------------------------------|----------------------------|
| *session*       | 重复使用预连接的 ssh2 资源                                             |                            |
| *sftp*          | 重复使用预先分配的 sftp 资源                                           |                            |
| *methods*       | 密钥交换（key exchange）、主机密钥（hostkey）、cipher、压缩和 MAC 方法 |                            |
| *callbacks*     |                                                                        |                            |
| *username*      | 以该用户名连接                                                         |                            |
| *password*      | 使用的密码来进行密码验证                                               |                            |
| *pubkey\_file*  | 用于验证的公钥（public key）文件                                       |                            |
| *privkey\_file* | 用于验证的私钥（private key）文件                                      |                            |
| *env*           | 需要设置的环境变量的关联数组                                           |                            |
| *term*          | 在分配一个 pty 时请求的终端类型                                        |                            |
| *term\_width*   | 在分配一个 pty 时请求的终端宽度                                        |                            |
| *term\_height*  | 在分配一个 pty 时请求的终端宽度高度                                    |                            |
| *term\_units*   | term\_width 和 term\_height 的单位                                     | **`SSH2_TERM_UNIT_CHARS`** |

### 范例

**示例 \#1 从一个活动连接中打开字节流**

``` php
<?php
$session = ssh2_connect('example.com', 22);
ssh2_auth_pubkey_file($session, 'username', '/home/username/.ssh/id_rsa.pub',
                                            '/home/username/.ssh/id_rsa', 'secret');
$stream = fopen("ssh2.tunnel://$session/remote.example.com:1234", 'r');
?>
```

**示例 \#2 This `$session` variable must be kept available!**

In order to use the `ssh2.*://$session` wrappers you must keep the
`$session` resouce variable. The code below will not have the desired
effect:

``` php
<?php
$session = ssh2_connect('example.com', 22);
ssh2_auth_pubkey_file($session, 'username', '/home/username/.ssh/id_rsa.pub',
                                            '/home/username/.ssh/id_rsa', 'secret');
$connection_string = "ssh2.sftp://$session/";
unset($session);
$stream = fopen($connection_string . "path/to/file", 'r');
?>
```

unset() closes the session, because `$connection_string` does not hold a
reference to the `$session` variable, just a string cast derived from
it. This also happens when the <span class="function">unset</span> is
implicit because of leaving scope (like in a function).
