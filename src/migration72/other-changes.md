其他变更
--------

### 移动 <span class="function">utf8\_encode</span> 和 <span class="function">utf8\_decode</span>

<span class="function">utf8\_encode</span> 和 <span
class="function">utf8\_decode</span>
现在已经作为字符串处理函数移到标准扩展中， 在此之前需要启用
<a href="/book/xml.html" class="link">XML</a> 扩展才能使用。

### 支持 LMDB

<a href="/book/dba.html" class="link">DBA</a> 扩展现在已经支持 LMDB。

### PHP 构建系统的变更

-   <span class="simpara"> Unix: 构建 PHP 需要 Autoconf 2.64
    或更高的版本。 </span>
-   <span class="simpara"> Unix: *--with-pdo-oci* 配置选项不再需要指定
    Oracle Instant Client 的版本号数字。 </span>
-   <span class="simpara"> Unix: 移除了 *--enable-gd-native-ttf*
    配置参数。自 PHP 5.5.0 以来就已经不再使用。 </span>
-   <span class="simpara"> Windows: 添加了 *--with-config-profile*
    配置参数。 可用于保存细节配置，就像是神奇的 `config.nice.bat` 文件。
    </span>

### <a href="/book/image.html" class="link">GD</a>的变更

-   <span class="simpara"> 当编译时使用了系统的 libgd，<span
    class="function">imageantialias</span> 也能生效。 </span>
-   <span class="simpara"> <span class="function">imagegd</span>
    以真彩色储存真彩色图像。在此之前，会转化为调色板图像。 </span>

### 移动 <a href="/book/mcrypt.html" class="link">MCrypt</a> 到 PECL

<a href="/book/mcrypt.html" class="link">MCrypt</a> 扩展从内核移动到
PECL。 考虑到 mcrypt 库自 2007 年以来未见任何更新，不再建议使用。
代替品即可以用 <a href="/book/openssl.html" class="link">OpenSSL</a>
也可以用<a href="/book/sodium.html" class="link">Sodium</a>。
