这些函数仅在 PHP 以 Apache 模块运行时有效。

> **Note**: <span class="simpara"> 截至 PHP 4.3.2，和Apache
> 1的情况下相比，`PATH_TRANSLATED` 在 Apache 2 的 SAPI
> 模式下不再隐式设定，相同的值设定在 `SCRIPT_FILENAME` server 变量。
> 该变化符合 CGI 协议， `PATH_TRANSLATED` 应该仅仅存在于 `PATH_INFO`
> 定义后的情况。 </span> <span class="simpara"> Apache 2 用户可以在
> `httpd.conf` 里使用 *AcceptPathInfo = On* 的设定来定义 `PATH_INFO`。
> </span>
