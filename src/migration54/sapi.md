SAPI 模块中的变化
-----------------

-   <span class="simpara"> 一个名为 *cli-server* 的新 SAPI
    模块可以使用。 </span>
-   <span class="simpara"> 新增 CLI 选项 *--rz* 用来显示 Zend
    扩展的信息。 </span>
-   <span class="simpara"> 新增快捷方式 *\#inisetting=value* 在 readline
    CLI 交互模式下来更改 `php.ini` 设置。 </span>
-   <span class="simpara"> 新增 apache 兼容函数： 用于 FastCGI SAPI
    的<span class="function">apache\_child\_terminate</span> 、 <span
    class="function">getallheaders</span> 、 <span
    class="function">apache\_request\_headers</span> 以及 <span
    class="function">apache\_response\_headers</span> 。 </span>
-   <span class="simpara"> PHP-FPM：新增 *process.max* 设置，用来控制
    FPM 能 fork 的进程数目。 </span>
