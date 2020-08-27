安装／配置
==========

**目录**

-   [需求](/mbstring/setup.html#需求)
-   [安装](/mbstring/setup.html#安装)
-   [运行时配置](/mbstring/setup.html#运行时配置)
-   [资源类型](/mbstring/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

*mbstring* 不是一个默认扩展。这意味着它默认没有被激活。 你必须在
*configure* 选项中显式激活该模块。
详情参见<a href="/install.html" class="link">安装</a>这一节。

以下是涉及到 *mbstring* 的相关配置选项。

-   **--enable-mbstring**：激活 *mbstring* 函数。 要使用 *mbstring*
    函数必须启用这个选项。

    <span class="productname">libmbfl</span> 对 *mbstring* 是必要的。
    <span class="productname">libmbfl</span> 被捆绑到了 *mbstring*。
    如果系统已安装 <span
    class="productname">libmbfl</span>，**--with-libmbfl\[=DIR\]**
    可以指定使用已安装的库。

-   **--disable-mbregex**：禁用正则表达式函数中多字节字符的支持。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                                 | 默认                                | 可修改范围       | 更新日志                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <a href="/mbstring/setup.html#" class="link">mbstring.language</a>                   | "neutral"                           | PHP\_INI\_ALL    | 自 PHP 4.3.0 起有效。 PHP\_INI\_PERDIR 位于 PHP \<= 5.2.6                                                                                        |
| <a href="/mbstring/setup.html#" class="link">mbstring.detect_order</a>               | NULL                                | PHP\_INI\_ALL    | 自 PHP 4.0.6 起有效。                                                                                                                            |
| <a href="/mbstring/setup.html#" class="link">mbstring.http_input</a>                 | "pass"                              | PHP\_INI\_ALL    | 自 PHP 4.0.6 起有效。                                                                                                                            |
| <a href="/mbstring/setup.html#" class="link">mbstring.http_output</a>                | "pass"                              | PHP\_INI\_ALL    | 自 PHP 4.0.6 起有效。                                                                                                                            |
| <a href="/mbstring/setup.html#" class="link">mbstring.internal_encoding</a>          | NULL                                | PHP\_INI\_ALL    | 自 PHP 4.0.6 起有效。                                                                                                                            |
| mbstring.script\_encoding                                                            | NULL                                | PHP\_INI\_ALL    | 自 PHP 4.3.0 起有效。 在 PHP 5.4.0. 中移除， 使用 <a href="/ini/core.html#ini.zend.script-encoding" class="link">zend.script_encoding</a> 代替。 |
| <a href="/mbstring/setup.html#" class="link">mbstring.substitute_character</a>       | NULL                                | PHP\_INI\_ALL    | 自 PHP 4.0.6 起有效。                                                                                                                            |
| <a href="/mbstring/setup.html#" class="link">mbstring.func_overload</a>              | "0"                                 | PHP\_INI\_SYSTEM | PHP 4.3 到 5.2.6 是 PHP\_INI\_PERDIR，否则是 PHP\_INI\_SYSTEM。 自 PHP 4.2.0 起有效。 PHP 7.2.0 中废弃。                                         |
| <a href="/mbstring/setup.html#" class="link">mbstring.encoding_translation</a>       | "0"                                 | PHP\_INI\_PERDIR | 自 PHP 4.3.0 起有效。                                                                                                                            |
| <a href="/mbstring/setup.html#" class="link">mbstring.http_output_conv_mimetypes</a> | "^(text/\|application/xhtml\\+xml)" | PHP\_INI\_ALL    | Available since PHP 5.3.0.                                                                                                                       |
| <a href="/mbstring/setup.html#" class="link">mbstring.strict_detection</a>           | "0"                                 | PHP\_INI\_ALL    | 自 PHP 5.1.2 起有效。                                                                                                                            |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`mbstring.language` <span class="type">string</span>  
mbstring 使用了国家默认语言设置（NLS）。 注意，该选项自动地定义了
*mbstring.internal\_encoding* 和 *mbstring.internal\_encoding*，在
`php.ini` 里应当放置在 *mbstring.language* 之后。

`mbstring.encoding_translation` <span class="type">boolean</span>  
为传入的 HTTP
查询启用透明字符编码过滤器，将检测和转换输入的编码为内部字符编码（internal
character encoding）。

`mbstring.internal_encoding` <span class="type">string</span>  
**Warning**
本特性已自 PHP 5.6.0 起*废弃*。强烈建议不要使用本特性。

定义内部字符的默认编码。

PHP 5.6 及更新版的用户应该将此选项留空，并设置
<a href="/ini/core.html#ini.default-charset" class="link"><code class="parameter">default_charset</code></a>
作为代替。

`mbstring.http_input` <span class="type">string</span>  
**Warning**
本特性已自 PHP 5.6.0 起*废弃*。强烈建议不要使用本特性。

定义 HTTP 输入字符的默认编码。

PHP 5.6 及更新版的用户应该将此选项留空，并设置
<a href="/ini/core.html#ini.default-charset" class="link"><code class="parameter">default_charset</code></a>
作为代替。

`mbstring.http_output` <span class="type">string</span>  
**Warning**
本特性已自 PHP 5.6.0 起*废弃*。强烈建议不要使用本特性。

定义 HTTP 输出字符的默认编码。

PHP 5.6 及更新版的用户应该将此选项留空，并设置
<a href="/ini/core.html#ini.default-charset" class="link"><code class="parameter">default_charset</code></a>
作为代替。

`mbstring.detect_order` <span class="type">string</span>  
定义字符编码的默认检测顺序。参见 <span
class="function">mb\_detect\_order</span>。

`mbstring.substitute_character` <span class="type">string</span>  
为无效编码的字符定义替代字符。 参见 <span
class="function">mb\_substitute\_character</span> ，查看支持的值。

`mbstring.func_overload` <span class="type">string</span>  
**Warning**
本特性已自 PHP 7.2.0 起*废弃*。强烈建议不要使用本特性。

用 mbstring
对应的函数覆盖单字节版本的函数集。更多信息参见<a href="/mbstring/overload.html" class="link">函数的覆盖</a>。

该设置仅能通过 `php.ini` 文件来修改。

`mbstring.http_output_conv_mimetypes` <span class="type">string</span>  

`mbstring.strict_detection` <span class="type">boolean</span>  
使用严格的编码检测。

根据
<a href="http://www.w3.org/TR/REC-html40/interact/forms.html#adef-accept-charset" class="link external">» HTML4.01 规范</a>，允许
Web 浏览器以页面不同的字符编码来提交表单。 参见用 <span
class="function">mb\_http\_input</span> 来检测浏览器使用的字符编码。

尽管流行的浏览器能够根据给出的 HTML 文档合理猜测正确的编码，但如果能通过
<span class="function">header</span> 函数在 HTTP 的 *Content-Type*
头内或 ini 的
<a href="/ini/core.html#ini.sect.data-handling" class="link">default_charset</a>
里设置适当的 *charset* 参数则会更佳。

**示例 \#1 `php.ini` 设置例子**

    ; 设置默认语言
    mbstring.language        = Neutral; 设置默认语言 Neutral(UTF-8) (默认的值)
    mbstring.language        = English; 设置默认语言为 English 
    mbstring.language        = Japanese; 设置默认语言为 Japanese

    ;; 设置内部的默认编码
    ;; 注意：请确保这个编码能被 PHP 所处理
    mbstring.internal_encoding    = UTF-8  ; 设置内部的默认编码为 UTF-8

    ;; 启用 HTTP 输入编码的转换
    mbstring.encoding_translation = On

    ;; 设置 HTTP 输入的默认编码
    ;; 注意：脚本不能修改 http_input 的设置
    mbstring.http_input           = pass    ; 不转换
    mbstring.http_input           = auto    ; 设置 HTTP 输入为 auto
                                    ; "auto" 会根据 mbstring.language 自动扩展
    mbstring.http_input           = SJIS    ; 设置 HTTP 输入编码为 SJIS
    mbstring.http_input           = UTF-8,SJIS,EUC-JP ; 指定顺序

    ;; 设置 HTTP 输出的默认编码
    mbstring.http_output          = pass    ; 不转换
    mbstring.http_output          = UTF-8   ; 设置 HTTP 输出编码为 UTF-8

    ;; 设置字符编码的默认检测顺序
    mbstring.detect_order         = auto    ; Set detect order to auto
    mbstring.detect_order         = ASCII,JIS,UTF-8,SJIS,EUC-JP ; Specify order

    ;; 设置默认的替代字符
    mbstring.substitute_character = 12307   ; 指定 Unicode 值
    mbstring.substitute_character = none    ; 不打印字符
    mbstring.substitute_character = long    ; Long 的例子： U+3000,JIS+7E7E

**示例 \#2 `php.ini` 里 *EUC-JP* 用户的设置**

    ;; 禁用输出缓冲
    output_buffering      = Off

    ;; 设置 HTTP header 字符编码
    default_charset       = EUC-JP    

    ;; 设置默认语言为 Japanese
    mbstring.language = Japanese

    ;; 启用 HTTP 输入编码的转换
    mbstring.encoding_translation = On

    ;; 启用 HTTP 输入转换的编码为 auto
    mbstring.http_input   = auto 

    ;; 转换 HTTP 输出的编码为 EUC-JP
    mbstring.http_output  = EUC-JP    

    ;; 设置内部编码为 EUC-JP
    mbstring.internal_encoding = EUC-JP    

    ;; 不要打印无效的字符
    mbstring.substitute_character = none   

**示例 \#3 `php.ini` 里 *SJIS* 用户的设置**

    ;; 启用输出缓冲
    output_buffering     = On

    ;; 设置 mb_output_handler 来启用输出编码的转换
    output_handler       = mb_output_handler

    ;; 设置 HTTP header 的字符编码
    default_charset      = Shift_JIS

    ;; 设置默认语言为 Japanese
    mbstring.language = Japanese

    ;; 设置 http 输入转换的编码为 auto
    mbstring.http_input  = auto 

    ;; 转换成 SJIS
    mbstring.http_output = SJIS    

    ;; 设置内部变量为 EUC-JP
    mbstring.internal_encoding = EUC-JP    

    ;; 不要打印无效的字符
    mbstring.substitute_character = none   

资源类型
--------

此扩展没有定义资源类型。
