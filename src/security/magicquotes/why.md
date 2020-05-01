为什么要用魔术引号
------------------

**Warning**

本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

-   <span class="simpara"> 没有理由再使用魔术引号，因为它不再是 PHP
    支持的一部分。
    不过它帮助了新手在不知不觉中写出了更好（更安全）的代码。
    但是在处理代码的时候，最好是更改你的代码而不是依赖于魔术引号的开启。
    </span> <span class="simpara">
    为什么这个功能存在？是为了阻止<a href="/security/database/sql-injection.html" class="link">SQL 注入</a>。
    在今天，开发者能够更好得意识到了安全问题，并最终使用数据库转移机制或者
    prepared 语句来取代魔术引号功能。 </span>
