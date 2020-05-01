在 Windows 上安装 PHP 扩展
--------------------------

在 Windows 上有两种加载 PHP 扩展的方式：把扩展编译进 PHP，或者加载
DLL。加载预编译的扩展是更简单更被推荐的方式。

要加载某扩展，需要在系统中有其相对应的“.dll”文件。所有扩展都会由 PHP
小组定期自动编译（如何下载见下节）。

要将一扩展编译入
PHP，请参考<a href="/install/windows/legacy/index.html#install.windows.building" class="link">从源程序编译</a>一章。

要编译一个独立的扩展（即 DLL
文件），请参考<a href="/install/windows/legacy/index.html#install.windows.building" class="link">从源程序编译</a>一章。如果在
PHP 发行包和 PCEL 中都没有某 DLL
文件，那可能需要自己编译之后才能使用该扩展。

### 去哪里找扩展库？

PHP
扩展库通常称为“php\_\*.dll”（其中星号代表具体某扩展的名字），位于“PHP\\ext”目录下（在
PHP 4 中位于“PHP\\extensions”目录下）。

PHP 发行包中包括了大多数开发者最常用到的扩展库。这些被称为“核心”扩展库。

不过呢，如果用户所需要的功能并没有被任何核心扩展提供，那还是有可能在
PECL 中找到。PHP Extension Community Library（PECL，PHP 扩展社区库）是个
PHP 扩展的储存室，提供了对于所有已知扩展的下载及开发途径的指南。

如果用户开发了一个自己使用的扩展，可以考虑将其发布到 PECL
中以便于其他有相同需求的用户使用。一个很好的副作用是可以得到其他用户的反馈，感谢，错误报告甚至修正／更新。不过在向
PECL 发布扩展之前，请先阅读 https://pecl.php.net/package-new.php。

### 下载哪个扩展？

*用户常常会发现每个 DLL 都有好几个版本：*

-   <span class="simpara"> 不同的版本号（至少前两个数字要一致） </span>
-   <span class="simpara"> 不同的线程安全性设定 </span>
-   <span class="simpara"> 不同的处理器体系（x86，x64，...) </span>
-   <span class="simpara"> 不同的排错设定 </span>
-   <span class="simpara"> *其它* </span>

请记住用户的扩展设定应该与所使用的 PHP
可执行文件的设定都保持一致。以下脚本可以显示*所有* PHP 设定：

**示例 \#1 <span class="function">phpinfo</span> call**

``` php
<?php
phpinfo();
?>
```

或者在命令行运行：

    drive:\\path\to\php\executable\php.exe -i

### 载入一个扩展

最常见的方式是在 `php.ini` 配置文件里包含一个 PHP
扩展。请注意很多扩展已经在 `php.ini` 里了，仅需要移除分号来激活它们。

    ;extension=php_extname.dll

    extension=php_extname.dll

不过呢，有些 web 服务器会搞混，因为其并不一定使用和 PHP
可执行文件处于同一目录下的 `php.ini` 文件。要搞清楚具体使用了哪一个
`php.ini` 文件，在 <span class="function">phpinfo</span> 的输出中查看：

    Configuration File (php.ini) Path  C:\WINDOWS

    Loaded Configuration File   C:\Program Files\PHP\5.2\php.ini

激活一个扩展后，保存 `php.ini` 文件并重启动 web 服务器，然后用 <span
class="function">phpinfo</span>
再次查看确定。新的扩展应该有其自己的一节。

### 解决问题

如果某扩展并未在 <span class="function">phpinfo</span>
中显示，应该查看日志以确定问题出在哪里。

如果是在命令行使用 PHP（CLI），扩展加载出错信息会直接在屏幕显示。

如果在 web 服务器中使用
PHP，则日志文件的位置与格式各不相同。请阅读所使用的 web
服务器之文档以确定日志文件的位置，这与 PHP 本身并无关系。

最常见的问题是 DLL 文件的位置，`php.ini`
中“<a href="/ini/core.html#ini.extension-dir" class="link">extension_dir</a>”设定的值，以及编译时的设置不匹配。

如果问题出在编译时设置不匹配，那可能所下载的 DLL
文件不对。可以尝试重新下载一个设置匹配的扩展。此外，<span
class="function">phpinfo</span> 可以起到很大帮助。
