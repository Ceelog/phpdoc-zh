安装／配置
==========

**目录**

-   [需求](/openssl/setup.html#需求)
-   [安装](/openssl/setup.html#安装)
-   [运行时配置](/openssl/setup.html#运行时配置)
-   [资源类型](/openssl/setup.html#资源类型)

需求
----

要使用 Open SSL
函数，你必须安装<a href="http://www.openssl.org/" class="link external">» OpenSSL</a>
库。 PHP 5 要求OpenSSL \>= 0.9.6。
然而PHP5后续版本会有些编译上的问题，所以最好是使用OpenSSL \>=
0.9.8(PHP7要求的最低版本) 。 其他版本(PHP \>= 7.1.0) 要求 OpenSSL \>=
1.0.1.

**Warning**

强烈建议你使用最新的OpenSSL版本，否则你的web服务器很容易受到攻击。

安装
----

要使用 PHP 的 OpenSSL
支持，你应该使用**--with-openssl\[=DIR\]**参数来编译PHP.

OpenSSL
库还在运行时对正常操作有额外的要求。最明显的是，OpenSSL需要访问随机或伪随机数生成器;
在大多数 Unix 和类 Unix 平台上(包括linux),意味着它必须要访问
*/dev/urandom* 或者 */dev/random* 设备。

> **Note**: **Win32 平台的用户请注意**  
>
> 为了使此扩展生效， DLL 文件必须能在 Windows 系统的 `PATH`
> 指示的路径下找到。如何操作的信息，请参见题为“<a href="/faq/installation.html#faq.installation.addtopath" class="link">如何在 Windows 中将 PHP 目录加到 PATH 中</a>”的FAQ。虽然将
> DLL 文件从 PHP 文件夹复制到 Windows 系统目录也行，但不建议这样做。
> *此扩展需要下列文件在 `PATH` 路径中：* `libeay32.dll`
>
> 此外，如果打算使用密钥生成和证书签名功能，你需要在你的系统上安装一个可用的
> `openssl.cnf` 文件。 在我们的 win32
> 二进制发行版本中，我们已经包含了一个示例配置文件，在 `extras/openssl`
> 文件夹中。
>
> PHP 将会使用如下逻辑搜索 `openssl.cnf` 文件:
>
> -   <span class="simpara">如果 *OPENSSL\_CONF*
>     环境变量设置了，该变量将会被当作配置文件的路径（含文件名）。
>     </span>
> -   <span class="simpara">如果 *SSLEAY\_CONF*
>     环境变量设置了，该变量将会被当作配置文件的路径（含文件名）。
>     </span>
> -   <span class="simpara">假设`openssl.cnf` 文件将会在 openssl DLL
>     被编译时配置的默认证书区域被找到。这通常意味着默认的文件名是
>     `c:\usr\local\ssl\openssl.cnf`. </span>
>
> <span class="simpara">
> 在你的安装过程中，你需要决定是否将配置文件安装在`c:\usr\local\ssl\openssl.cnf`
> 或者使用环境变量(可能是基于每个虚拟主机的基础)来定位配置文件安装到其他地方。注意，可以使用引入配置文件的函数中的
> `configargs` 参数来覆盖脚本中的默认路径。 </span>

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字           | 默认 | 可修改范围       | Changelog           |
|----------------|------|------------------|---------------------|
| openssl.cafile | ""   | PHP\_INI\_PERDIR | 自PHP 5.6.0起可用。 |
| openssl.capath | ""   | PHP\_INI\_PERDIR | 自PHP 5.6.0起可用。 |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`openssl.cafile` <span class="type">string</span>  
本地文件系统上证书颁发机构文件的位置，
被用来和对等校验上下文选项一起校验远程对等方的身份。

`openssl.capath` <span class="type">string</span>  
如果没有制定证书颁发机构文件或者证书找不到，将在由capath指向的目录下搜索一个合适的证书。capath
必须是一个正确的已被散列的证书目录。

参见 <a href="/context/ssl.html" class="link">SSL stream context</a>
选项。

资源类型
--------

在OpenSSL模块中有三种资源类型。第一种是一个
pkey(公钥或私钥)标识符，第二种是一个X509证书标识符，第三种是 CSR
(证书签名请求) 标识符。
