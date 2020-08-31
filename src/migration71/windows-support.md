Windows 支持
------------

### Support for long and UTF-8 path

If a web application is UTF-8 conform, no further action is required.
For applications depending on paths in non UTF-8 encodings for I/O, an
explicit INI directive has to be set. The encoding INI settings check
relies on the order in the core:

-   <span class="simpara"> internal\_encoding </span>
-   <span class="simpara"> default\_charset </span>
-   <span class="simpara"> zend.multibyte </span>

Several functions for codepage handling were introduced:

-   <span class="simpara"> sapi\_windows\_cp\_set() to set the default
    codepage </span>
-   <span class="simpara"> sapi\_windows\_cp\_get() to retrieve the
    current codepage </span>
-   <span class="simpara"> sapi\_windows\_cp\_is\_utf8() </span>
-   <span class="simpara"> sapi\_windows\_cp\_conv() to convert between
    codepages, using iconv() compatible signature </span>

These functions are thread safe.

The console output codepage is adjusted depending on the encoding used
in PHP. Depending on the concrete system OEM codepage, the visible
output might or might be not correct. For example, in the default
cmd.exe and on a system with the OEM codepage 437, outputs in codepages
1251, 1252, 1253 and some others can be shown correctly when using
UTF-8. On the same system, chars in codepage like 20932 probably won't
be shown correctly. This refers to the particular system rules for
codepage, font compatibility and the particular console program used.
PHP automatically sets the console codepage according to the encoding
rules from php.ini. Using alternative consoles instead of cmd.exe
directly might bring better experience in some cases.

Nevertheless be aware, runtime codepage switch after the request start
might bring unexpected side effects on CLI. The preferable way is
php.ini, When PHP CLI is used in a console emulator, that doesn't
support Unicode, it might possibly be required, to avoid changing the
console codepage. The best way to achieve it is by setting the default
or internal encoding to correspond the ANSI codepage. Another method is
to set the INI directives output\_encoding and input\_encoding to the
required codepage, in which case however the difference between internal
and I/O codepage is likely to cause mojibake. In rare cases, if PHP
happens to crash gracefully, the original console codepage might be not
restored. In this case, the chcp command can be used, to restore it
manually.

Special awareness for the DBCS systems - the codepage switch on runtime
using <span class="function">ini\_set</span> is likely to cause display
issues. The difference to the non DBCS systems is, that the extended
characters require two console cells to be displayed. In certain case,
only the mapping of the characters into the glyph set of the font could
happen, no actual font change. This is the nature of DBCS systems, the
most simple way to prevent display issues is to avoid usage of <span
class="function">ini\_set</span> for the codepage change.

As a result of UTF-8 support in the streams, PHP scripts are not limited
to ASCII or ANSI filenames anymore. This is supported out of the box on
CLI. For other SAPI, the documentation for the corresponding server is
useful.

Long paths support is transparent. Paths longer than 260 bytes get
automatically prefixed with *\\\\?\\*. The max path length is limited to
2048 bytes. Be aware, that the path segment limit (basename length)
still persists.

For the best portability, it is strongely recommended to handle
filenames, I/O and other related topics UTF-8. Additionally, for the
console applications, the usage of a TrueType font is preferable and the
usage of ini\_set() for the codepage change is discouraged.

### readline

<a href="/book/readline.html" class="link">readline 扩展</a> 现在通过
<a href="http://mingweditline.sourceforge.net/" class="link external">» WinEditLine 库</a>
来实现了支持。因此，一个交互式的 CLI 命令行也得到了支持。(*php.exe
-a*)。
