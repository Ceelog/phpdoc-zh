SAPI 模块的改变
---------------

-   <span class="simpara"> 一个新增的名为 litespeed 的 SAPI 模块可用.
    </span>
-   <span class="simpara"> CGI SAPI 中的 FastCGI
    支持总是打开并且无法关闭. 更多信息请查看 *sapi/cgi/CHANGES*. </span>
-   <span class="simpara"> 一个新的 CGI SAPI 选项 *-T*
    可以被用来衡量一个脚本的重复执行时间. </span>
-   <span class="simpara"> CGI/FastCGI 现在支持 .htaccess 样式的
    用户自定义 `php.ini` 文件. </span>
-   <span class="simpara"> <span class="function">dl</span>
    函数默认被关闭, 并且现在只在 CLI, CGI, 和内嵌的 SAPI 环境下可用.
    </span>
