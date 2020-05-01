下载 PECL 扩展库
----------------

下载 PECL 扩展库有几种方法，如：

-   <span class="simpara"> *pecl install extname*
    命令会自动下载扩展代码， 所以在这种情况下不需要再次下载。 </span>
-   <span class="simpara">
    <a href="https://pecl.php.net/" class="link external">» https://pecl.php.net/</a>
    </span> <span class="simpara"> PECL 网站包括有 PHP
    开发组提供的不同扩展库的信息。这里的信息包括：更新记录，版本说明，需求，以及其它信息。
    </span>
-   <span class="simpara"> *pecl download extname* </span> <span
    class="simpara"> PECL 网站中列出的 PECL 扩展库的发行版本可以用
    <a href="https://pear.php.net/manual/en/guide.users.commandline.cli.php" class="link external">» pear 命令</a>来下载和安装。也可以指明具体的修正版。
    </span>
-   <span class="simpara"> SVN </span> <span class="simpara"> 大多数
    PECL 扩展库也在 SVN 中。其 web 页面见 be seen at
    <a href="https://svn.php.net/viewvc/pecl/" class="link external">» https://svn.php.net/viewvc/pecl/</a>。要直接从
    SVN 中下载，用以下命令： </span>
      
    $ svn checkout http://svn.php.net/repository/pecl/extname/trunk
    extname  
-   <span class="simpara"> Windows 下载： </span> <span class="simpara">
    目前 PHP 项目没有为 Windows 下 PECL 扩展编译二进制文件。要在 Windows
    下编译
    PHP，请阅读<a href="/install/windows/legacy/index.html#install.windows.building" class="link">有关章节</a>。
    </span>
