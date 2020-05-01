支持的字符编码
==============

当前 *mbstring*
模块支持以下的字符编码。这些字符编码中的任意一个都能指定到 *mbstring*
函数中的 *encoding* 参数。

该 PHP 扩展支持的字符编码有以下几种：

-   <span class="simpara">UCS-4\*</span>
-   <span class="simpara">UCS-4BE</span>
-   <span class="simpara">UCS-4LE\*</span>
-   <span class="simpara">UCS-2</span>
-   <span class="simpara">UCS-2BE</span>
-   <span class="simpara">UCS-2LE</span>
-   <span class="simpara">UTF-32\*</span>
-   <span class="simpara">UTF-32BE\*</span>
-   <span class="simpara">UTF-32LE\*</span>
-   <span class="simpara">UTF-16\*</span>
-   <span class="simpara">UTF-16BE\*</span>
-   <span class="simpara">UTF-16LE\*</span>
-   <span class="simpara">UTF-7</span>
-   <span class="simpara">UTF7-IMAP</span>
-   <span class="simpara">UTF-8\*</span>
-   <span class="simpara">ASCII\*</span>
-   <span class="simpara">EUC-JP\*</span>
-   <span class="simpara">SJIS\*</span>
-   <span class="simpara">eucJP-win\*</span>
-   <span class="simpara">SJIS-win\*</span>
-   <span class="simpara">ISO-2022-JP</span>
-   <span class="simpara">ISO-2022-JP-MS</span>
-   <span class="simpara">CP932</span>
-   <span class="simpara">CP51932</span>
-   <span class="simpara">SJIS-mac\*\* (别名： MacJapanese)</span>
-   <span class="simpara">SJIS-Mobile\#DOCOMO\*\* (别名：
    SJIS-DOCOMO)</span>
-   <span class="simpara">SJIS-Mobile\#KDDI\*\* (别名：
    SJIS-KDDI)</span>
-   <span class="simpara">SJIS-Mobile\#SOFTBANK\*\* (别名：
    SJIS-SOFTBANK)</span>
-   <span class="simpara">UTF-8-Mobile\#DOCOMO\*\* (别名：
    UTF-8-DOCOMO)</span>
-   <span class="simpara">UTF-8-Mobile\#KDDI-A\*\*</span>
-   <span class="simpara">UTF-8-Mobile\#KDDI-B\*\* (别名：
    UTF-8-KDDI)</span>
-   <span class="simpara">UTF-8-Mobile\#SOFTBANK\*\* (别名：
    UTF-8-SOFTBANK)</span>
-   <span class="simpara">ISO-2022-JP-MOBILE\#KDDI\*\* (别名：
    ISO-2022-JP-KDDI)</span>
-   <span class="simpara">JIS</span>
-   <span class="simpara">JIS-ms</span>
-   <span class="simpara">CP50220</span>
-   <span class="simpara">CP50220raw</span>
-   <span class="simpara">CP50221</span>
-   <span class="simpara">CP50222</span>
-   <span class="simpara">ISO-8859-1\*</span>
-   <span class="simpara">ISO-8859-2\*</span>
-   <span class="simpara">ISO-8859-3\*</span>
-   <span class="simpara">ISO-8859-4\*</span>
-   <span class="simpara">ISO-8859-5\*</span>
-   <span class="simpara">ISO-8859-6\*</span>
-   <span class="simpara">ISO-8859-7\*</span>
-   <span class="simpara">ISO-8859-8\*</span>
-   <span class="simpara">ISO-8859-9\*</span>
-   <span class="simpara">ISO-8859-10\*</span>
-   <span class="simpara">ISO-8859-13\*</span>
-   <span class="simpara">ISO-8859-14\*</span>
-   <span class="simpara">ISO-8859-15\*</span>
-   <span class="simpara">ISO-8859-16\*</span>
-   <span class="simpara">byte2be</span>
-   <span class="simpara">byte2le</span>
-   <span class="simpara">byte4be</span>
-   <span class="simpara">byte4le</span>
-   <span class="simpara">BASE64</span>
-   <span class="simpara">HTML-ENTITIES</span>
-   <span class="simpara">7bit</span>
-   <span class="simpara">8bit</span>
-   <span class="simpara">EUC-CN\*</span>
-   <span class="simpara">CP936</span>
-   <span class="simpara">GB18030\*\*</span>
-   <span class="simpara">HZ</span>
-   <span class="simpara">EUC-TW\*</span>
-   <span class="simpara">CP950</span>
-   <span class="simpara">BIG-5\*</span>
-   <span class="simpara">EUC-KR\*</span>
-   <span class="simpara">UHC (CP949)</span>
-   <span class="simpara">ISO-2022-KR</span>
-   <span class="simpara">Windows-1251 (CP1251)</span>
-   <span class="simpara">Windows-1252 (CP1252)</span>
-   <span class="simpara">CP866 (IBM866)</span>
-   <span class="simpara">KOI8-R\*</span>
-   <span class="simpara">KOI8-U\*</span>
-   <span class="simpara">ArmSCII-8 (ArmSCII8)</span>

\* 表示该编码也可以在正则表达式中使用。

\*\* 表示该编码自 PHP 5.4.0 始可用。

任何接受编码名称的 `php.ini` 条目同样也可以使用 "*auto*" 和 "*pass*"
的值。 接受编码名的 *mbstring* 函数同样也可以使用值 "*auto*"。

如果设置了 "*pass*"，将不会对字符的编码进行转化。

如果设置了 "*auto*"，它将扩展成
<a href="/mbstring/setup.html#运行时配置" class="link">NLS</a>
中定义的每个字符编码列表。 比如，假设 NLS 设置为
*Japanese*，值将会认为是 "*ASCII,JIS,UTF-8,EUC-JP,SJIS*"。

参见 <span class="function">mb\_detect\_order</span>
