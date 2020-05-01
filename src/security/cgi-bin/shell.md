情形四：PHP 解释器放在 web 目录以外
-----------------------------------

一个非常安全的做法就是把 PHP 解释器放在 web 目录外的地方，比如说
`/usr/local/bin`。这样做唯一不便的地方就是必须在每一个包含 PHP
代码的文件的第一行加入如下语句：

    #!/usr/local/bin/php

还要将这些文件的属性改成可执行。也就是说，要像处理用 Perl 或 sh
或其它任何脚本语言写的 CGI 脚本一样，使用以 *\#!* 开头的 shell-escape
机制来启动它们。

在这种情况下，要使 PHP 能正确处理 `PATH_INFO` 和 `PATH_TRANSLATED`
等变量的话，在编译 PHP 解释器时必须加入
<a href="/configure/about.html#configure.enable-discard-path" class="link">--enable-discard-path</a>
参数。
