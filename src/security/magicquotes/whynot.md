为什么不用魔术引号
------------------

**Warning**

本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

-   <span class="simpara"> 可移植性 </span> <span class="simpara">
    编程时认为其打开或并闭都会影响到移植性。可以用 <span
    class="function">get\_magic\_quotes\_gpc</span>
    来检查是否打开，并据此编程。 </span>
-   <span class="simpara"> 性能 </span> <span class="simpara">
    由于并不是每一段被转义的数据都要插入数据库的，如果所有进入 PHP
    的数据都被转义的话，那么会对程序的执行效率产生一定的影响。在运行时调用转义函数（如
    <span class="function">addslashes</span>）更有效率。 </span> <span
    class="simpara"> 尽管 `php.ini-dist` 默认打开了这个选项，但是
    `php.ini-recommended` 默认却关闭了它，主要是出于性能的考虑。 </span>
-   <span class="simpara"> 不便 </span> <span class="simpara">
    由于不是所有数据都需要转义，在不需要转义的地方看到转义的数据就很烦。比如说通过表单发送邮件，结果看到一大堆的
    \\'。针对这个问题，可以使用 <span
    class="function">stripslashes</span> 函数处理。 </span>
