用 PEAR 编译共享 PECL 扩展库
----------------------------

PECL 使建立共享 PHP 扩展库更容易。用
<a href="https://pear.php.net/manual/en/guide.users.commandline.cli.php" class="link external">» pecl 命令</a>这样做：

  
$ pecl install extname  

这将下载 *extname* 的源代码，编译之，并将 `extname.so` 安装到
<a href="/ini/core.html#ini.extension-dir" class="link">extension_dir</a>
中。然后 `extname.so` 就可以通过 `php.ini` 加载了。

默认情况下，*pecl* 命令不会安装标记为 *alpha* 或 *beta*
状态的包。如果没有 *stable* 包可用，也可以用以下命令安装一个 *beta* 包：

  
$ pecl install extname-beta  

也可以用此命令安装一个指定的版本：

  
$ pecl install extname-0.1  

> **Note**:
>
> 在 `php.ini` 中激活扩展之后，需要重新启动 web 服务以使更改生效。
