安全
====

**目录**

-   [简介](/security/intro.html)
-   [总则](/security/general.html)
-   [以 CGI 模式安装时](/security/cgi-bin.html)
    -   [可能受到的攻击](/security/cgi-bin/attacks.html)
    -   [情形一：只运行公开的文件](/security/cgi-bin/default.html)
    -   [情形二：使用 --enable-force-cgi-redirect
        选项](/security/cgi-bin/force-redirect.html)
    -   [情形三：设置 doc\_root 或
        user\_dir](/security/cgi-bin/doc-root.html)
    -   [情形四：PHP 解释器放在 web
        目录以外](/security/cgi-bin/shell.html)
-   [以 Apache 模块安装时](/security/apache.html)
-   [会话（Session）安全](/security/sessions.html)
-   [文件系统安全](/security/filesystem.html)
    -   [Null 字符问题](/security/filesystem/nullbytes.html)
-   [数据库安全](/security/database.html)
    -   [设计数据库](/security/database/design.html)
    -   [连接数据库](/security/database/connection.html)
    -   [加密存储模型](/security/database/storage.html)
    -   [SQL 注入](/security/database/sql-injection.html)
-   [错误报告](/security/errors.html)
-   [使用 Register Globals](/security/globals.html)
-   [用户提交的数据](/security/variables.html)
-   [魔术引号](/security/magicquotes.html)
    -   [什么是魔术引号](/security/magicquotes/what.html)
    -   [为什么要用魔术引号](/security/magicquotes/why.html)
    -   [为什么不用魔术引号](/security/magicquotes/whynot.html)
    -   [关闭魔术引号](/security/magicquotes/disabling.html)
-   [隐藏 PHP](/security/hiding.html)
-   [保持更新](/security/current.html)
