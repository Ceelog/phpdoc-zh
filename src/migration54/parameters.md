变更的函数
----------

在 PHP 5.4 中 一些函数增加了新的参数和可选参数：

PHP 核心：

-   <span class="simpara"> <span
    class="function">debug\_backtrace</span> 和 <span
    class="function">debug\_print\_backtrace</span> 新增可选参数 `limit`
    来限制返回的堆栈帧数量。 </span>
-   <span class="simpara"> <span class="function">is\_link</span> 现在在
    Windows Vista
    或更新系统上对于符号链接能正确地运行。早期系统不支持符号链接。
    </span>
-   <span class="simpara"> <span class="function">parse\_url</span>
    在省略方案（scheme，如http）时，现在能识辨出主机，并存在一个主要的组件分隔符。自
    PHP 5.4.7 起。 </span>

OpenSSL:

-   <span class="simpara"> <span
    class="function">openssl\_encrypt</span> 和 <span
    class="function">openssl\_decrypt</span> 函数新增一个未填充的选项。
    </span>

Intl:

-   <span class="simpara"> <span class="function">idn\_to\_ascii</span>
    和 <span class="function">idn\_to\_utf8</span>
    现在可以使用两个额外的参数，一个代表变体，另一个通过应用传递，
    返回选择 UTS \#46 时的操作细节。 </span>
