情形三：设置 doc\_root 或 user\_dir
-----------------------------------

在 web
服务器的主文档目录中包含动态内容如脚本和可执行程序有时被认为是一种不安全的实践。如果因为配置上的错误而未能执行脚本而作为普通
HTML
文档显示，那就可能导致知识产权或密码资料的泄露。所以很多系统管理员都会专门设置一个只能通过
PHP CGI 来访问的目录，这样该目录中的内容只会被解析而不会原样显示出来。

对于前面所说无法判断是否重定向的情况，很有必要在主文档目录之外建立一个专用于脚本的
doc\_root 目录。

可以通过<a href="/configuration/file.html" class="link">配置文件</a>内的
<a href="/ini/core.html#ini.doc-root" class="link">doc_root</a>
或设置环境变量 `PHP_DOCUMENT_ROOT` 来定义 PHP
脚本主目录。如果设置了该项，那么 PHP 就只会解释 `doc_root`
目录下的文件，并确保目录外的脚本不会被 PHP 解释器执行（下面所说的
`user_dir` 除外）。

另一个可用的选项就是
<a href="/ini/core.html#ini.user-dir" class="link">user_dir</a>。当
user\_dir 没有设置的时候，`doc_root`
就是唯一能控制在哪里打开文件的选项。访问如
`http://my.host/~user/doc.php` 这个 URL
时，并不会打开用户主目录下文件，而只会执行 doc\_root 目录下的
`~user/doc.php`（这个子目录以 \[*\~*\] 作开头）。

如果设置了 user\_dir，例如 `public_php`，那么像
`http://my.host/~user/doc.php` 这样的请求将会执行用户主目录下的
`public_php` 子目录下的 `doc.php` 文件。假设用户主目录的绝对路径是
`/home/user`，那么被执行文件将会是 `/home/user/public_php/doc.php`。

`user_dir` 的设置与 `doc_root` 无关，所以可以分别控制 PHP
脚本的主目录和用户目录。
