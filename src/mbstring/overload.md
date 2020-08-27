函数重载功能
============

**Warning**

本特性已自 PHP 7.2.0 起*废弃*。强烈建议不要使用本特性。

你也许常常会发现现存的 PHP 应用很难运行在多字节环境下。
发生这种情况的原因是大多数那种 PHP 应用使用了标准的字符串函数，类似
<span class="function">substr</span>，已知无法处理多字节编码的字符串。

mbstring
支持一个“函数重载”功能，将对应的多字节版本重载到标准字符处理函数上，例如你能够让这类应用在不修改代码的前提下添加多字节的处理能力。
比如，启用函数重载后，<span class="function">mb\_substr</span> 将会代替
<span class="function">substr</span> 被调用。
在很多情况下这个功能允许让仅支持单字节编码的应用简单地和多字节环境对接。

要使用函数重载功能，设置 `php.ini` 里的 *mbstring.func\_overload*
为正值，就是表示为重载函数分类的位掩码组合。 要重载 <span
class="function">mail</span> 函数需要设置它为 1。字符串函数设置为
2，正则表达式函数为 4。 例如，当它设置为 7， mail、strings 和
正则表达式函数将都会被重载。 以下列表显示了重载的函数。

| mbstring.func\_overload 的值 | 原始函数                                     | 重载后的函数                                     |
|------------------------------|----------------------------------------------|--------------------------------------------------|
| 1                            | <span class="function">mail</span>           | <span class="function">mb\_send\_mail</span>     |
| 2                            | <span class="function">strlen</span>         | <span class="function">mb\_strlen</span>         |
| 2                            | <span class="function">strpos</span>         | <span class="function">mb\_strpos</span>         |
| 2                            | <span class="function">strrpos</span>        | <span class="function">mb\_strrpos</span>        |
| 2                            | <span class="function">substr</span>         | <span class="function">mb\_substr</span>         |
| 2                            | <span class="function">strtolower</span>     | <span class="function">mb\_strtolower</span>     |
| 2                            | <span class="function">strtoupper</span>     | <span class="function">mb\_strtoupper</span>     |
| 2                            | <span class="function">stripos</span>        | <span class="function">mb\_stripos</span>        |
| 2                            | <span class="function">strripos</span>       | <span class="function">mb\_strripos</span>       |
| 2                            | <span class="function">strstr</span>         | <span class="function">mb\_strstr</span>         |
| 2                            | <span class="function">stristr</span>        | <span class="function">mb\_stristr</span>        |
| 2                            | <span class="function">strrchr</span>        | <span class="function">mb\_strrchr</span>        |
| 2                            | <span class="function">substr\_count</span>  | <span class="function">mb\_substr\_count</span>  |
| 4                            | <span class="function">ereg</span>           | <span class="function">mb\_ereg</span>           |
| 4                            | <span class="function">eregi</span>          | <span class="function">mb\_eregi</span>          |
| 4                            | <span class="function">ereg\_replace</span>  | <span class="function">mb\_ereg\_replace</span>  |
| 4                            | <span class="function">eregi\_replace</span> | <span class="function">mb\_eregi\_replace</span> |
| 4                            | <span class="function">split</span>          | <span class="function">mb\_split</span>          |

> **Note**:
>
> 不推荐每个目录的范围（context）内使用函数重载选项，因为还无法确定在生产环境中是否稳定，也许会导致不确定的行为。
