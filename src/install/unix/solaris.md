针对 <span class="productname">Solaris</span> 的安装提示
--------------------------------------------------------

本节包含了在 <span class="productname">Solaris</span> 系统上安装 PHP
的说明和提示。

### 需要的软件

默认安装的 <span class="productname">Solaris</span> 系统经常缺少 C
语言编译器和其相关工具。部分工具必须使用该工具的 GNU 版本，原因请阅读
<a href="/faq/build.html#faq.installation.needgnu" class="link">FAQ</a>。

要解压缩 PHP 发行包，需要：

-   <span class="simpara"> tar </span>
-   <span class="simpara"> gzip 或 </span>
-   <span class="simpara"> bzip2 </span>

要编译 PHP，需要：

-   <span class="simpara"> gcc（推荐使用，其它 C 编译器也许也能用）
    </span>
-   <span class="simpara"> make </span>
-   <span class="simpara"> GNU sed </span>

要编译更多扩展库或自行开发 PHP 代码，可能还需要：

-   <span class="simpara"> flex（直到 PHP 5.2） </span>
-   <span class="simpara"> re2c </span>
-   <span class="simpara"> bison </span>
-   <span class="simpara"> m4 </span>
-   <span class="simpara"> autoconf </span>
-   <span class="simpara"> automake </span>

此外，还需要安装（甚至编译）针对自己的配置所需的软件，例如 Oracle 或
MySQL。

### 使用软件包

可以使用 pkgadd 来安装大部分需要的软件来简化 <span
class="productname">Solaris</span> 安装过程。<span
class="productname">Solaris 11 Express</span> 下的映像打包系统（Image
Packaging System，IPS）也包含了大多数安装所需的部件，通过 pkg 命令。
