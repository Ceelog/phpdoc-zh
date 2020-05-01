使用内置的 PHP
--------------

从 OS X 10.0.0 版本开始，PHP 作为 Mac 机的标准配置被提供。在默认的 web
服务器中启用 PHP，只需将 Apache 配置文件 `httpd.conf`
中的几行配置指令最前面的注释符号去掉，而 CGI 或 CLI
默认都可使用（可以很容易的被终端程序使用）。

按照以下的使用说明，可以快速的建立一个本地 PHP 开发环境。*强烈建议*将
PHP 升级到最新的版本。在大多数活跃的软件中，
新的版本会修复错误和添加新的功能，PHP 也是如此。请参见相应的 Mac OS X
安装文档，以进一步了解详细的信息。以下的说明以初学者的角度来详细描述如何操作来得到一个缺省的运行环境。建议所有的用户都编译或者安装一个新的打包版本。

标准的安装类型为 mod\_php，在 Mac OS X 的 Apache web 服务器（默认 web
服务器，可以从系统设置中访问）中启用 PHP 包含以下的步骤：

1.  <span class="simpara">
    找到并打开Apache的配置文件。默认情况下，这个配置文件的位置是：
    `/private/etc/apache2/httpd.conf`。 </span> <span class="simpara">
    使用 *Finder* 或者 *Spotlight*
    来找到这个文件可能不是很容易的事情，因为在默认情况下它一般是 *root*
    用户拥有所有权的私有文件。 </span>

    > **Note**: <span class="simpara">
    > 要打开这个文件，可以在命令行下面使用基于 Unix 的文本编辑器，例如
    > *nano*，因为他的属主是 *root*，所以我们需要使用 *sudo* 来打开（以
    > *root* 用户权限）。例如我们在 *Terminal*
    > 程序中敲入下面的指令（操作后，会提示输入密码）：*sudo nano
    > /private/etc/apache2/httpd.conf* </span> <span class="simpara">
    > 注意 nano 中的命令：*^w*（搜索），*^o*（保存），以及
    > *^x*（退出）。*^* 表示 Ctrl 键。 </span>

    > **Note**: <span class="simpara"> 在Mac OS X
    > 10.5之前的版本中捆绑的是旧版本的 PHP 和 Apache。因此在旧的计算机中
    > Apache 配置文件的位置可能是 `/etc/httpd/httpd.conf`。 </span>

2.  使用文本的编辑器取消注释（删除前面的
    \#）看起来类似于下面的行（这两行常常不在一起，需要在文件中找到这两行）：

        # LoadModule php5_module libexec/httpd/libphp5.so

        # AddModule mod_php5.c

    注意位置／路径。如果在以后重新编译了
    PHP，以上文件应被更换或者注释掉。

3.  确保将所需要的文件扩展名解析为 PHP（例如：.php .html 以及
    .inc），否则不能正常运行。

    由于以下的配置已经写入 `httpd.conf`（自 Mac Panther 版起），一旦 PHP
    被启用则 `.php` 文件会被自动解析为 PHP 脚本。

        <IfModule mod_php5.c>
            # If php is turned on, we respect .php and .phps files.
            AddType application/x-httpd-php .php
            AddType application/x-httpd-php-source .phps

            # Since most users will want index.php to work we
            # also automatically enable index.php
            <IfModule mod_dir.c>
                DirectoryIndex index.html index.php
            </IfModule>
        </IfModule>

    > **Note**:
    >
    > 在 OS X 10.5（Leopard）以前版本中，捆绑的是 PHP 4 而不是 PHP
    > 5，因此上面的配置指令稍有不同，需要将 5 更改为 4。

4.  <span class="simpara"> 确保 DirectoryIndex
    加载了所需的默认索引文件。 </span> <span class="simpara"> 这个也是在
    `httpd.conf` 中设置的。 通常情况下使用 `index.php` 和 `index.html`
    。默认情况下 `index.php`
    会被启用，因为在我们上面的配置指令中写明了。根据实际情况可以做相应的调整。
    </span>

5.  <span class="simpara"> 设置 `php.ini` 的位置或者使用默认的位置。
    </span> <span class="simpara"> Mac OS X 上通常默认的位置是
    `/usr/local/php/php.ini` ，调用 <span
    class="function">phpinfo</span> 也可以得到此信息。如果没有使用
    `php.ini`，PHP
    将使用所有的默认值。参见常见问题中的<a href="/faq/installation.html#faq.installation.phpini" class="link">寻找 php.ini</a>。
    </span>

6.  <span class="simpara"> 定位或者设置 *DocumentRoot*。 </span> <span
    class="simpara"> 这是网站所有文件的根目录。此目录中的文件由 web
    服务器提供服务，从而使得 PHP 文件将在输出到浏览器之前解析为 PHP
    脚本。通常情况下默认的路径是
    `/Library/WebServer/Documents`，但是可以根据需要在
    `httpd.conf`中设置为任何其他目录。另外，用户自己的缺省
    `DocumentRoot` 是 `/Users/yourusername/Sites`。 </span>

7.  <span class="simpara"> 创建一个 <span
    class="function">phpinfo</span> 文件。 </span>

    <span class="function">phpinfo</span>
    将会显示PHP的相关系统信息。可以在 DocumentRoot 下创建一个 PHP
    文件，其代码如下：

    ``` php
    <?php phpinfo(); ?>
    ```

8.  <span class="simpara"> 重启 Apache，然后从浏览器访问上面创建的文件。
    </span>

    要重启Apache，可以在 shell 中执行 *sudo apachectl
    graceful*，也可以停止/启动 OS X 系统首选项中的“Personal Web
    Server”选项。默认情况下，从浏览器访问本地文件的 URL
    一般类似于：`http://localhost/info.php`，或者使用：`http://localhost/~yourusername/info.php`
    来访问用户自己 DocumentRoot 中的文件。

CLI（或者旧版本中的 CGI）一般文件名为 `php` ，其路径可能是
`/usr/bin/php`。打开一个终端，参考 PHP 手册中的
<a href="/features/commandline.html" class="link">PHP 的命令行模式</a>一章，然后执行
*php -v* 可以检查当前运行的 PHP 的版本。调用 <span
class="function">phpinfo</span> 也会显示相关的信息。
