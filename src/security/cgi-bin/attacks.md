可能受到的攻击
--------------

如果不想把 PHP 嵌入到服务器端软件（如
Apache）作为一个模块安装的话，可以选择以 CGI 的模式安装。或者把 PHP
用于不同的 CGI 封装以便为代码创建安全的 chroot 和 setuid
环境。这种安装方式通常会把 PHP 的可执行文件安装到 web 服务器的 cgi-bin
目录。CERT 建议书
<a href="http://www.cert.org/advisories/CA-1996-11.html" class="link external">» CA-96.11</a>
建议不要把任何的解释器放到 cgi-bin 目录。尽管 PHP
可以作为一个独立的解释器，但是它的设计使它可以防止下面类型的攻击：

-   <span class="simpara">
    访问系统文件：`http://my.host/cgi-bin/php?/etc/passwd` </span> <span
    class="simpara"> 在 URL 请求的问号（?）后面的信息会传给 CGI
    接口作为命名行的参数。其它的解释器会在命令行中打开并执行第一个参数所指定的文件。
    </span> <span class="simpara"> 但是，以 CGI 模式安装的 PHP
    解释器被调用时，它会拒绝解释这些参数。 </span>
-   <span class="simpara">
    访问服务器上的任意目录：`http://my.host/cgi-bin/php/secret/doc.html`
    </span> <span class="simpara"> 好像上面这种情况，PHP
    解释器所在目录后面的 URL 信息 `/secret/doc.html` 将会例行地传给 CGI
    程序并进行解释。通常一些 web 服务器的会将它重定向到页面，如
    `http://my.host/secret/script.php`。如果是这样的话，某些服务器会先检查用户访问
    `/secret` 目录的权限，然后才会创建
    `http://my.host/cgi-bin/php/secret/script.php`
    上的页面重定向。不幸的是，很多服务器并没有检查用户访问
    /secret/script.php 的权限，只检查了 `/cgi-bin/php`
    的权限，这样任何能访问 `/cgi-bin/php` 的用户就可以访问 web
    目录下的任意文件了。 </span> <span class="simpara"> 在 PHP
    里，编译时配置选项
    <a href="/configure/about.html#configure.enable-force-cgi-redirect" class="link">--enable-force-cgi-redirect</a>
    以及运行时配置指令
    <a href="/ini/core.html#ini.doc-root" class="link">doc_root</a> 和
    <a href="/ini/core.html#ini.user-dir" class="link">user_dir</a>
    都可以为服务器上的文件和目录添加限制，用于防止这类攻击。下面将对各个选项的设置进行详细讲解。
    </span>
