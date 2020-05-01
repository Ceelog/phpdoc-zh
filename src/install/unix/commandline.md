CGI 和命令行设置
----------------

默认为将 PHP 编译为 CLI 和 CGI 程序。这将建立一个命令行解释器，可用于
CGI 处理或非 web 相关的 PHP 脚本。如果用户运行着一个 PHP 模块支持的 web
服务器，那通常为性能考虑应该使用模块方式。不过 CGI 版可以使 Apache
用户用不同的用户 ID 运行不同的 PHP 页面。

**Warning**

服务器使用 CGI 方式进行部署可能存在几个公开的缺陷。请阅读
<a href="/security/cgi-bin.html" class="link">CGI 安全</a>一章 以学习
如何抵御这些攻击。

### 测试

如果将 PHP 编译为 CGI 程序，可以通过键入 **make test**
来测试你的编译。测试一下编译永远是个好主意。这样就可以在你的平台上及早捕捉到
PHP 的问题而不是以后再费力的解决。

### 使用变量

某些<a href="/reserved/variables/server.html" class="link">服务器提供的环境变量</a>没有定义在当前的
<a href="http://www.faqs.org/rfcs/rfc3875" class="link external">» CGI/1.1 标准</a>中。只有下列变量定义在其中：
`AUTH_TYPE`， `CONTENT_LENGTH`, `CONTENT_TYPE`, `GATEWAY_INTERFACE`,
`PATH_INFO`, `PATH_TRANSLATED`, `QUERY_STRING`, `REMOTE_ADDR`,
`REMOTE_HOST`, `REMOTE_IDENT`, `REMOTE_USER`, `REQUEST_METHOD`,
`SCRIPT_NAME`, `SERVER_NAME`, `SERVER_PORT`, `SERVER_PROTOCOL` 和
`SERVER_SOFTWARE`。其它的变量均作为“供应商扩展（vendor
extensions）”来对待。
