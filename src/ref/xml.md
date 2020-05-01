utf8\_decode
============

将用 UTF-8 方式编码的 ISO-8859-1 字符串转换成单字节的 ISO-8859-1
字符串。

### 描述

<span class="type">string</span> <span
class="methodname">utf8\_decode</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> )

该函数将用 *UTF-8* 编码的数据解码为 *ISO-8859-1* 编码。

请参阅 <span class="function">utf8\_encode</span> 以查看关于 UTF-8
编码的解释。

utf8\_encode
============

将 ISO-8859-1 编码的字符串转换为 UTF-8 编码

### 描述

<span class="type">string</span> <span
class="methodname">utf8\_encode</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> )

该函数将 `data` 字符串转换为 *UTF-8* 编码，并返回编码后的字符串。*UTF-8*
是一种用于将<span class="glossterm">宽字符</span>值转换为字节流的
Unicode 的标准机制。*UTF-8* 对于纯 ASCII
字符来说是透明的，且是自同步的（也就是说这使得程序能够得知字符从字节流的何处开始），并可被普通字符串比较函数用以比较等操作。PHP
可将 *UTF-8* 编码为多达四个字节的字符，如：

| 字节（bytes） | 位（bits） | 表 示                               |
|---------------|------------|-------------------------------------|
| 1             | 7          | 0bbbbbbb                            |
| 2             | 11         | 110bbbbb 10bbbbbb                   |
| 3             | 16         | 1110bbbb 10bbbbbb 10bbbbbb          |
| 4             | 21         | 11110bbb 10bbbbbb 10bbbbbb 10bbbbbb |

每个 *UTF-8* 表示一个能被用以储存字符数据的位。

xml\_error\_string
==================

获取 XML 解析器的错误字符串

### 说明

<span class="type">string</span> <span
class="methodname">xml\_error\_string</span> ( <span
class="methodparam"><span class="type">int</span> `$code`</span> )

根据给定的 `code` 获得 XML 解析器错误字符串。

### 参数

`code`  
由 <span class="function">xml\_get\_error\_code</span> 返回的错误代码。

### 返回值

返回与 `code`
描述的错误代码参数对应的文本描述字符串，若没有与之对应的描述，则返回
**`FALSE`**。

### 参见

-   <span class="function">xml\_get\_error\_code</span>

xml\_get\_current\_byte\_index
==============================

获取 XML 解析器的当前字节索引

### 说明

<span class="type">int</span> <span
class="methodname">xml\_get\_current\_byte\_index</span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
)

获取指定的 XML 解析器的当前字节索引（current byte index）。

### 参数

`parser`  
指向要取得字节索引的 XML 解析器的引用。

### 返回值

如果 `parser` 没有指向一个合法的解析器，该函数将返回
**`FALSE`**，否则将返回解析器当前在其数据缓冲区中的字节索引（起始值为
0）。

### 注释

**Warning**

该函数将返回根据UTF-8编码的文本的字节索引，而不论输入是否是其他的编码。

### 参见

-   <span class="function">xml\_get\_current\_column\_index</span>
-   <span class="function">xml\_get\_current\_line\_index</span>

xml\_get\_current\_column\_number
=================================

获取 XML 解析器的当前列号

### 说明

<span class="type">int</span> <span
class="methodname">xml\_get\_current\_column\_number</span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
)

获得指定 XML 解析器当前的列号。

### 参数

`parser`  
一个指向要获取列号的 XML 解析器的指针。

### 返回值

如果 `parser` 参数没有指向一个合法的解析器，该函数将返回
**`FALSE`**，否则将返回指定解析器所在行（由函数 <span
class="function">xml\_get\_current\_line\_number</span>
给定）的当前列号。

### 参见

-   <span class="function">xml\_get\_current\_byte\_index</span>
-   <span class="function">xml\_get\_current\_line\_index</span>

xml\_get\_current\_line\_number
===============================

获取 XML 解析器的当前行号

### 说明

<span class="type">int</span> <span
class="methodname">xml\_get\_current\_line\_number</span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
)

获取指定 XML 解析器当前的行号。

### 参数

`parser`  
一个指向要获取当前行号的 XML 解析器的指针。

### 返回值

如果 `parser` 参数没有指向一个合法的解析器，该函数将返回
**`FALSE`**，否则将返回指定解析器在其缓存中的当前行号。

### 参见

-   <span class="function">xml\_get\_current\_column\_index</span>
-   <span class="function">xml\_get\_current\_byte\_index</span>

xml\_get\_error\_code
=====================

获取 XML 解析器错误代码

### 说明

<span class="type">int</span> <span
class="methodname">xml\_get\_error\_code</span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
)

获取 XML 解析器错误代码。

### 参数

`parser`  
一个指向要返回错误代码的 XML 解析器的指针

### 返回值

如果 `parser` 参数没有指向一个合法的解析器，该函数将返回
**`FALSE`**，否则将返回<a href="/xml/error-codes.html" class="link">错误代码</a>列表中的一个错误代码。

### 参见

-   <span class="function">xml\_error\_string</span>

xml\_parse\_into\_struct
========================

将 XML 数据解析到数组中

### 说明

<span class="type">int</span> <span
class="methodname">xml\_parse\_into\_struct</span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
, <span class="methodparam"><span class="type">string</span>
`$data`</span> , <span class="methodparam"><span
class="type">array</span> `&$values`</span> \[, <span
class="methodparam"><span class="type">array</span> `&$index`</span> \]
)

该函数将 XML 文件解析到两个对应的数组中，`index` 参数含有指向 `values`
数组中对应值的指针。最后两个数组参数可由指针传递给函数。

> **Note**:
>
> <span class="function">xml\_parse\_into\_struct</span> 失败返回
> 0，成功返回 1。这和 **`FALSE`** 与 **`TRUE`** 不同，使用例如 ===
> 的运算符时要注意。

以下范例显示了由该函数生成的数组的内部结构。我们简单地将一个 *note*
嵌入到一个 *para* 标记中，解析后我们可以打印出生成的数组的结构：

**示例 \#1 <span class="function">xml\_parse\_into\_struct</span> 示例**

``` php
<?php
$simple = "<para><note>simple note</note></para>";
$p = xml_parser_create();
xml_parse_into_struct($p, $simple, $vals, $index);
xml_parser_free($p);
echo "Index array\n";
print_r($index);
echo "\nVals array\n";
print_r($vals);
?>
```

运行以上代码，我们得到的输出将是：

    Index array
    Array
    (
        [PARA] => Array
            (
                [0] => 0
                [1] => 2
            )

        [NOTE] => Array
            (
                [0] => 1
            )

    )

    Vals array
    Array
    (
        [0] => Array
            (
                [tag] => PARA
                [type] => open
                [level] => 1
            )

        [1] => Array
            (
                [tag] => NOTE
                [type] => complete
                [level] => 2
                [value] => simple note
            )

        [2] => Array
            (
                [tag] => PARA
                [type] => close
                [level] => 1
            )

    )

如果您的 XML 文档很复杂，基于该文档的事件处理（Event-driven）解析（基于
expat 扩展库）也会对应的变得复杂。该函数生成的并非 DOM
风格的对象，而是横向的树状结构。因此，我们能够方便的建立表达 XML
文件数据的对象。我们假设以下 XML
文件表示一个关于氨基酸信息的小型数据库：

**示例 \#2 moldb.xml - 分子信息的小型数据库**

``` xml
<?xml version="1.0"?>
<moldb>

    <molecule>
        <name>Alanine</name>
        <symbol>ala</symbol>
        <code>A</code>
        <type>hydrophobic</type>
    </molecule>

    <molecule>
        <name>Lysine</name>
        <symbol>lys</symbol>
        <code>K</code>
        <type>charged</type>
    </molecule>

</moldb>
```

以下是解析该文档并生成相应对象的代码：

**示例 \#3 parsemoldb.php - 将 moldb.xml
解析到分子（molecular）对象的数组中**

``` php
<?php

class AminoAcid {
    var $name;  // aa 姓名
    var $symbol;    // 三字母符号
    var $code;  // 单字母代码
    var $type;  // hydrophobic, charged 或 neutral

    function AminoAcid ($aa)
    {
        foreach ($aa as $k=>$v)
            $this->$k = $aa[$k];
    }
}

function readDatabase($filename)
{
    // 读取 aminoacids 的 XML 数据
    $data = implode("",file($filename));
    $parser = xml_parser_create();
    xml_parser_set_option($parser, XML_OPTION_CASE_FOLDING, 0);
    xml_parser_set_option($parser, XML_OPTION_SKIP_WHITE, 1);
    xml_parse_into_struct($parser, $data, $values, $tags);
    xml_parser_free($parser);

    // 遍历 XML 结构
    foreach ($tags as $key=>$val) {
        if ($key == "molecule") {
            $molranges = $val;
            // each contiguous pair of array entries are the
            // lower and upper range for each molecule definition
            for ($i=0; $i < count($molranges); $i+=2) {
                $offset = $molranges[$i] + 1;
                $len = $molranges[$i + 1] - $offset;
                $tdb[] = parseMol(array_slice($values, $offset, $len));
            }
        } else {
            continue;
        }
    }
    return $tdb;
}

function parseMol($mvalues)
{
    for ($i=0; $i < count($mvalues); $i++) {
        $mol[$mvalues[$i]["tag"]] = $mvalues[$i]["value"];
    }
    return new AminoAcid($mol);
}

$db = readDatabase("moldb.xml");
echo "** Database of AminoAcid objects:\n";
print_r($db);

?>
```

在执行完 `parsemoldb.php` 后，变量 `$db` 将包含有一个由 <span
class="classname">AminoAcid</span> 对象组成的数组，该脚本的输出如下：

    ** Database of AminoAcid objects:
    Array
    (
        [0] => aminoacid Object
            (
                [name] => Alanine
                [symbol] => ala
                [code] => A
                [type] => hydrophobic
            )

        [1] => aminoacid Object
            (
                [name] => Lysine
                [symbol] => lys
                [code] => K
                [type] => charged
            )

    )

xml\_parse
==========

开始解析一个 XML 文档

### 说明

<span class="type">int</span> <span class="methodname">xml\_parse</span>
( <span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$is_final`<span
class="initializer"> = false</span></span> \] )

<span class="function">xml\_parse</span> 解析 XML
文档。已配置事件的处理器根据需要被无限次调用。

### 参数

`parser`  
一个指向将要使用的 XML 解析器的指针

`data`  
需要解析的数据集。您可以多次对新的数据调用 <span
class="function">xml\_parse</span>
函数来分段解析一个文档；只要在解析最后一段数据时将 `is_final` 参数设置为
**`TRUE`**。

`is_final`  
如果被设置为 **`TRUE`**，则 `data` 为当前解析中最后一段数据。

### 返回值

成功时返回1，失败时返回0

若解析失败，可以使用如下函数获取错误信息： <span
class="function">xml\_get\_error\_code</span>, <span
class="function">xml\_error\_string</span>, <span
class="function">xml\_get\_current\_line\_number</span>, <span
class="function">xml\_get\_current\_column\_number</span> 和 <span
class="function">xml\_get\_current\_byte\_index</span>。

> **Note**:
>
> 将 `is_final` 参数设置为 **`TRUE`**，项目的错误将会报告在数据的末尾。

xml\_parser\_create\_ns
=======================

生成一个支持命名空间的 XML 解析器

### 描述

<span class="type">resource</span> <span
class="methodname">xml\_parser\_create\_ns</span> (\[ <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$sep`</span> \]\] )

函数 <span class="function">xml\_parser\_create\_ns</span>
建立一个新的支持 XML 命名空间的解析器并返回可被其它 XML
函数使用的资源句柄。

通过有命名空间支持的解析器，传递给各种各样句柄函数的标签参数将由命名空间和标签名组成。命名空间和标签名的分隔符由
`seperator` 参数制定的字符串决定，其默认值为“:”。

可选参数 `encoding` 在 PHP 4 中用来指定要被解析的 XML
输入的字符编码方式。PHP 5 开始，自动侦测输入的 XML 的编码，因此
`encoding` 参数仅用来指定解析后输出数据的编码。在 PHP 4
总，默认输出的编码与输入数据的编码是相同的。如果传递了空字符串，解析器会尝试搜索头
3 或 4 个字节以确定文档的编码。在 PHP 5.0.0 和 5.0.1
总，默认输出的字符编码是 ISO-8859-1，而 PHP 5.0.2 及以上版本是
UTF-8。解析器支持的编码有 *ISO-8859-1*, *UTF-8* 和 *US-ASCII*。

请参阅函数 <span class="function">xml\_parser\_create</span> 和 <span
class="function">xml\_parser\_free</span>。

xml\_parser\_create
===================

建立一个 XML 解析器

### 描述

<span class="type">resource</span> <span
class="methodname">xml\_parser\_create</span> (\[ <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
\] )

函数 <span class="function">xml\_parser\_create</span> 建立一个新的 XML
解析器并返回可被其它 XML 函数使用的资源句柄。

可选参数 `encoding` 在 PHP 4 中用来指定要被解析的 XML
输入的字符编码方式。PHP 5 开始，自动侦测输入的 XML 的编码，因此
`encoding` 参数仅用来指定解析后输出数据的编码。在 PHP 4
总，默认输出的编码与输入数据的编码是相同的。如果传递了空字符串，解析器会尝试搜索头
3 或 4 个字节以确定文档的编码。在 PHP 5.0.0 和 5.0.1
总，默认输出的字符编码是 ISO-8859-1，而 PHP 5.0.2 及以上版本是
UTF-8。解析器支持的编码有 *ISO-8859-1*, *UTF-8* 和 *US-ASCII*。

请参阅函数 <span class="function">xml\_parser\_create\_ns</span> 和
<span class="function">xml\_parser\_free</span>。

xml\_parser\_free
=================

释放指定的 XML 解析器

### 描述

<span class="type">bool</span> <span
class="methodname">xml\_parser\_free</span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
)

`parser`  
<span class="simpara"> 指向要释放的 XML 解析器的指针。 </span>

如果 `parser` 参数没有指向一个合法的解析器，该函数将返回
**`FALSE`**，否则将释放指定的解析器并返回 **`TRUE`**。

xml\_parser\_get\_option
========================

从 XML 解析器获取选项设置信息

### 描述

<span class="type">mixed</span> <span
class="methodname">xml\_parser\_get\_option</span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
, <span class="methodparam"><span class="type">int</span>
`$option`</span> )

`parser`  
<span class="simpara"> 指向要获取设置信息的 XML 解析器的指针。 </span>

`option`  
<span class="simpara"> 要获取的设置选项名称。可以使用
**`XML_OPTION_CASE_FOLDING`** 和 **`XML_OPTION_TARGET_ENCODING`**
常量。其说明见 <span class="function">xml\_parser\_set\_option</span>。
</span>

如果 `parser` 参数没有指向一个合法的解析器或者 `option`
参数无效，该函数将返回 **`FALSE`**（同时产生 **`E_WARNING`**
警告）。否则将返回指定设置选项的值。

xml\_parser\_set\_option
========================

为指定 XML 解析进行选项设置

### 说明

<span class="type">bool</span> <span
class="methodname">xml\_parser\_set\_option</span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
, <span class="methodparam"><span class="type">int</span>
`$option`</span> , <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

`parser`  
<span class="simpara"> 指向要设置选项信息的 XML 解析器的指针。 </span>

`option`  
<span class="simpara"> 要设置的选项名称。请参考下文。 </span>

`value`  
<span class="simpara"> 要给选项设置的新值。 </span>

如果 `parser`
参数没有指向一个合法的解析器或者指定的选项无法设置，该函数将返回
**`FALSE`**，否则将会把选项设置为指定的值并返回 **`TRUE`**。

可被设置的选项如下：

| 选项常量                      | 数据类型 | 描述                                                                                                                                                                                                                                                                           |
|-------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| XML\_OPTION\_CASE\_FOLDING    | integer  | 控制在该 XML 解析器中 <a href="/xml/case-folding.html" class="link">大小写折叠（case-folding）</a> 是否有效。其默认值为有效。                                                                                                                                                  |
| XML\_OPTION\_SKIP\_TAGSTART   | integer  | 指明在一个标记名前应略过几个字符。                                                                                                                                                                                                                                             |
| XML\_OPTION\_SKIP\_WHITE      | integer  | 是否略过由白空字符组成的值。                                                                                                                                                                                                                                                   |
| XML\_OPTION\_TARGET\_ENCODING | string   | 设置该 XML 解析器所使用的<a href="/xml/encoding.html" class="link">目标编码（target encoding）</a>方式。其默认值和由 <span class="function">xml\_parser\_create</span> 函数设置的源编码（source encoding）方式相同。支持的目标编码方式有 *ISO-8859-1*、*US-ASCII* 和 *UTF-8*。 |

xml\_set\_character\_data\_handler
==================================

建立字符数据处理器

### 说明

<span class="type">bool</span> <span
class="methodname">xml\_set\_character\_data\_handler</span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
, <span class="methodparam"><span class="type">callable</span>
`$handler`</span> )

为 `parser` 变量指向的 XML 解析器指定字符数据处理函数。

### 参数

`parser`  
XML 解析器的引用，用于建立字符数据处理器。

`handler`  
`handler` 为表示一个函数名称的字符串，该函数必须在为 `parser`
指定的解析器调用 <span class="function">xml\_parse</span> 函数时已存在。

由 `handler` 参数命名的函数名必须接受两个参数：

<span class="methodname"><span class="replaceable">handler</span></span>
( <span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> )

`parser`  
<span class="simpara"> 第一个参数 <span
class="replaceable">parser</span> 为指向要调用处理器的 XML
解析器的指针。 </span>

`data`  
<span class="simpara"> 第二个参数 `data` 为包含有字符数据的字符串。
</span>

Character data handler is called for every piece of a text in the XML
document. It can be called multiple times inside each fragment (e.g. for
non-ASCII strings).

如果处理器函数名被设置为空字符串或者
**`FALSE`**，则该有问题的处理器将被屏蔽。

> **Note**: <span
> class="simpara">除了函数名，含有对象引用的数组和方法名也可以作为参数。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

xml\_set\_default\_handler
==========================

建立默认处理器

### 说明

<span class="type">bool</span> <span
class="methodname">xml\_set\_default\_handler</span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
, <span class="methodparam"><span class="type">callable</span>
`$handler`</span> )

为 `parser` 指定的 XML 处理器建立默认处理函数。

### 参数

`parser`  
XML 解析器的引用，用于建立默认处理器函数。

`handler`  
`handler` 为表示一个函数名称的字符串，该函数必须在为 `parser`
指定的解析器调用 <span class="function">xml\_parse</span> 函数时已存在。

由 `handler` 参数命名的函数名必须接受两个参数：

<span class="methodname"><span class="replaceable">handler</span></span>
( <span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> )

`parser`  
<span class="simpara"> 第一个参数 <span
class="replaceable">parser</span> 为指向要调用处理器的 XML
解析器的指针。 </span>

`data`  
<span class="simpara"> 第二个参数 `data`
为包含有字符数据的字符串。其内容可以是 XML
声明、文档类型声明、实体名或者其它没有已存在处理器的地数据。 </span>

如果处理器函数名被设置为空字符串或者
**`FALSE`**，则该有问题的处理器将被屏蔽。

> **Note**: <span
> class="simpara">除了函数名，含有对象引用的数组和方法名也可以作为参数。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

xml\_set\_element\_handler
==========================

建立起始和终止元素处理器

### 说明

<span class="type">bool</span> <span
class="methodname">xml\_set\_element\_handler</span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
, <span class="methodparam"><span class="type">callable</span>
`$start_element_handler`</span> , <span class="methodparam"><span
class="type">callable</span> `$end_element_handler`</span> )

为 `parser` 参数指定的 XML 解析器建立元素处理器函数。参数
`start_element_handler` 和 `end_element_handler`
为表示函数名称的字符串，这些函数必须在为 `parser` 指定的解析器调用 <span
class="function">xml\_parse</span> 函数时已存在。

### 参数

`parser`  
XML 解析器的引用，用于建立起始和终止元素处理器。

`start_element_handler`  
由 `start_element_handler` 参数命名的函数名必须接受三个参数：

<span class="methodname"><span
class="replaceable">start\_element\_handler</span></span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">array</span> `$attribs`</span> )

`parser`  
<span class="simpara"> 第一个参数 <span
class="replaceable">parser</span> 为指向要调用处理器的 XML
解析器的指针。 </span>

`name`  
<span class="simpara"> 第二个参数 `name`
为该处理器为之被调用的元素名。如果<a href="/xml/case-folding.html" class="link">大小写折叠（case-folding）</a>对该解析器有效，元素名将用大写字母表示。
</span>

`attribs`  
<span class="simpara"> 第三个参数 `attribs`
为一个包含有对应元素的属性的数组（如果该元素有属性）。数组元素的下标为属性名，元素的值即为属性的值。属性名将以和元素名同样的标准进行<a href="/xml/case-folding.html" class="link">大小写折叠（case-folded）</a>，其值*不*进行大小写折叠。
</span> <span class="simpara"> 属性的原始顺序将会被参数保留，用 <span
class="function">each</span> 函数遍历 `attribs`
时，该数组下表的顺序和属性的顺序相同。 </span>

> **Note**: <span
> class="simpara">除了函数名，含有对象引用的数组和方法名也可以作为参数。</span>

`end_element_handler`  
由 `end_element_handler` 参数命名的函数名必须接受两个参数：

<span class="methodname"><span
class="replaceable">end\_element\_handler</span></span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> )

`parser`  
<span class="simpara"> 第一个参数 <span
class="replaceable">parser</span> 为指向要调用处理器的 XML
解析器的指针。 </span>

`name`  
<span class="simpara"> 第二个参数 `name`
为该处理器为之被调用的元素名。如果<a href="/xml/case-folding.html" class="link">大小写折叠（case-folding）</a>对该解析器有效，元素名将用大写字母表示。
</span>

如果处理器函数名被设置为空字符串或者
**`FALSE`**，则该有问题的处理器将被屏蔽。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

xml\_set\_end\_namespace\_decl\_handler
=======================================

建立终止命名空间声明处理器

### 说明

<span class="type">bool</span> <span
class="methodname">xml\_set\_end\_namespace\_decl\_handler</span> (
<span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">callable</span> `$handler`</span> )

Set a handler to be called when leaving the scope of a namespace
declaration. This will be called, for each namespace declaration, after
the handler for the end tag of the element in which the namespace was
declared.

### 参数

`parser`  
A reference to the XML parser.

`handler`  
`handler` is a string containing the name of a function that must exist
when <span class="function">xml\_parse</span> is called for `parser`.

The function named by `handler` must accept two parameters, and should
return an integer value. If the value returned from the handler is
**`FALSE`** (which it will be if no value is returned), the XML parser
will stop parsing and <span
class="function">xml\_get\_error\_code</span> will return
**`XML_ERROR_EXTERNAL_ENTITY_HANDLING`**.

<span class="methodname"><span class="replaceable">handler</span></span>
( <span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">string</span> `$prefix`</span> )

`parser`  
<span class="simpara"> The first parameter, <span
class="replaceable">parser</span>, is a reference to the XML parser
calling the handler. </span>

`prefix`  
<span class="simpara"> The prefix is a string used to reference the
namespace within an XML object. </span>

If a handler function is set to an empty string, or **`FALSE`**, the
handler in question is disabled.

> **Note**: <span
> class="simpara">除了函数名，含有对象引用的数组和方法名也可以作为参数。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

> **Note**:
>
> This event is not supported under LibXML.

### 参见

-   <span
    class="function">xml\_set\_start\_namespace\_decl\_handler</span>

xml\_set\_external\_entity\_ref\_handler
========================================

建立外部实体指向处理器

### 说明

<span class="type">bool</span> <span
class="methodname">xml\_set\_external\_entity\_ref\_handler</span> (
<span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">callable</span> `$handler`</span> )

为 `parser` 参数指定的 XML 解析器建立外部实体指向处理器函数。

### 参数

`parser`  
XML 解析器的引用，用于建立外部实体指向处理器。

`handler`  
参数 `handler` 为表示函数名称的字符串，函数必须在为 `parser`
指定的解析器调用 <span class="function">xml\_parse</span> 函数时已存在。

由 `handler`
参数命名的函数名必须接受五个参数，并应该返回一个整型值。如果处理器的返回值为
**`FALSE`**（这也是函数没有确定返回值时的返回值），XML
解析器将停止解析， <span class="function">xml\_get\_error\_code</span>
函数将返回 **`XML_ERROR_EXTERNAL_ENTITY_HANDLING`**。

<span class="methodname"><span class="replaceable">handler</span></span>
( <span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">string</span> `$open_entity_names`</span> , <span
class="methodparam"><span class="type">string</span> `$base`</span> ,
<span class="methodparam"><span class="type">string</span>
`$system_id`</span> , <span class="methodparam"><span
class="type">string</span> `$public_id`</span> )

`parser`  
<span class="simpara"> 第一个参数 <span
class="replaceable">parser</span> 为指向要调用处理器的 XML
解析器的指针。 </span>

`open_entity_names`  
<span class="simpara"> 第二个参数 `open_entity_names`
是为该实体的解析开放的实体名列表（包括被指向的实体名），这些实体名由空格隔开。
</span>

`base`  
<span class="simpara">
这个参数是解析外部实体的系统标识符（`system_id`）的基础。当前该参数通常都被设置为空字符串。
</span>

`system_id`  
<span class="simpara"> 第四个参数 `system_id`
是在实体定义声明中指定的系统标识符。 </span>

`public_id`  
<span class="simpara"> 第五个参数 `public_id`
是在实体定义声明中指定的公共标识符，如果未指定任何标识符，则该字符串为空。公共标识符中的空格将按照
XML 的要求被正常化。 </span>

如果处理器函数名被设置为空字符串或者
**`FALSE`**，则该有问题的处理器将被屏蔽。

> **Note**: <span
> class="simpara">除了函数名，含有对象引用的数组和方法名也可以作为参数。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

xml\_set\_notation\_decl\_handler
=================================

建立注释声明处理器

### 说明

<span class="type">bool</span> <span
class="methodname">xml\_set\_notation\_decl\_handler</span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
, <span class="methodparam"><span class="type">callable</span>
`$handler`</span> )

为 `parser` 参数指定的 XML 解析器建立注释声明处理器函数。

注释声明是文档 DTD 的一部分，并有如下格式：

``` xml
<!NOTATION <parameter>name</parameter>
{<parameter>system_id</parameter> | <parameter>public_id</parameter>}?>
```

。请参考
<a href="http://www.w3.org/TR/1998/REC-xml-19980210#Notations" class="link external">» XML 1.0 参考的第 4.7 节</a>以了解注释声明的定义。

### 参数

`parser`  
XML 解析器的引用，用于设置声明处理器函数。

`handler`  
`handler` 为表示函数名称的字符串，函数必须在为 `parser` 指定的解析器调用
<span class="function">xml\_parse</span> 函数时已存在。

由 `handler` 参数命名的函数名必须接受五个参数：

<span class="methodname"><span class="replaceable">handler</span></span>
( <span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">string</span> `$notation_name`</span> , <span
class="methodparam"><span class="type">string</span> `$base`</span> ,
<span class="methodparam"><span class="type">string</span>
`$system_id`</span> , <span class="methodparam"><span
class="type">string</span> `$public_id`</span> )

`parser`  
<span class="simpara"> 第一个参数 <span
class="replaceable">parser</span> 为指向要调用处理器的 XML
解析器的指针。 </span>

`notation_name`  
<span class="simpara"> 该参数为以上注释格式定义中的 `name` 参数。
</span>

`base`  
<span class="simpara">
这个参数是解析注释声明的系统标识符（`system_id`）的基础。当前该参数通常都被设置为空字符串。
</span>

`system_id`  
<span class="simpara"> 外部注释声明的系统标识符。 </span>

`public_id`  
<span class="simpara"> 外部注释声明的公共标识符。 </span>

如果处理器函数名被设置为空字符串或者
**`FALSE`**，则该有问题的处理器将被屏蔽。

> **Note**: <span
> class="simpara">除了函数名，含有对象引用的数组和方法名也可以作为参数。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

xml\_set\_object
================

在对象中使用 XML 解析器

### 描述

<span class="type">pool</span> <span
class="methodname">xml\_set\_object</span> ( <span
class="methodparam"><span class="type">resource</span> `$parser`</span>
, <span class="methodparam"><span class="type">object</span>
`&$object`</span> )

该函数使得 `parser` 指定的解析器可以被用在 `object`
对象中。所有的回叫函数（callback function）都可以由 <span
class="function">xml\_set\_element\_handler</span>
等函数来设置，它们被假定为 `object` 对象的方法。

**示例 \#1 <span class="function">xml\_set\_object</span> 示例**

``` php
<?php
class xml  {
    var $parser;

    function xml() 
    {
        $this->parser = xml_parser_create();

        xml_set_object($this->parser, $this);
        xml_set_element_handler($this->parser, "tag_open", "tag_close");
        xml_set_character_data_handler($this->parser, "cdata");
    }

     function parse($data) 
    {
        xml_parse($this->parser, $data);
    }

    function tag_open($parser, $tag, $attributes) 
    {
        var_dump($parser, $tag, $attributes); 
    }

    function cdata($parser, $cdata) 
    {
        var_dump($parser, $cdata);
    }

    function tag_close($parser, $tag) 
    {
        var_dump($parser, $tag);
    }

} // end of class xml

$xml_parser = new xml();
$xml_parser->parse("<A ID='hallo'>PHP</A>");
?>
```

xml\_set\_processing\_instruction\_handler
==========================================

建立处理指令（PI）处理器

### 说明

<span class="type">bool</span> <span
class="methodname">xml\_set\_processing\_instruction\_handler</span> (
<span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">callable</span> `$handler`</span> )

为 `parser` 参数指定的 XML 解析器建立处理指令（PI）处理器函数。

处理指令有如下格式：

    <?

<span class="replaceable">target</span> <span
class="replaceable">data</span>

    ?>
          

您可以将 PHP 代码放置在类似的标识符中，但要注意一个限制：在 XML
处理指令（PI）中，PI
的终止符（*?\>*）不能被引号引用，因此该字符序列不应该在您用 PI 嵌入到
XML 文档中的 PHP 代码中出现。否则，剩下的 PHP 代码，包括“真正”的 PI
终止符将被当作字符数据处理。

### 参数

`parser`  
XML 解析器的引用，用于建立处理指令（PI）处理器。

`handler`  
参数 `handler` 为表示函数名称的字符串，函数必须在为 `parser`
指定的解析器调用 <span class="function">xml\_parse</span> 函数时已存在。

由 `handler` 参数命名的函数名必须接受三个参数：

<span class="methodname"><span class="replaceable">handler</span></span>
( <span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">string</span> `$target`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> )

`parser`  
<span class="simpara"> 第一个参数 <span
class="replaceable">parser</span> 为指向要调用处理器的 XML
解析器的指针。 </span>

`target`  
<span class="simpara"> 第二个参数 `target` 为 PI 对象（PI target）。
</span>

`data`  
<span class="simpara"> 第三个参数 `data` 包含了 PI 数据。 </span>

如果处理器函数名被设置为空字符串或者
**`FALSE`**，则该有问题的处理器将被屏蔽。

> **Note**: <span
> class="simpara">除了函数名，含有对象引用的数组和方法名也可以作为参数。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

xml\_set\_start\_namespace\_decl\_handler
=========================================

建立起始命名空间声明处理器

### 说明

<span class="type">bool</span> <span
class="methodname">xml\_set\_start\_namespace\_decl\_handler</span> (
<span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">callable</span> `$handler`</span> )

Set a handler to be called when a namespace is declared. Namespace
declarations occur inside start tags. But the namespace declaration
start handler is called before the start tag handler for each namespace
declared in that start tag.

### 参数

`parser`  
A reference to the XML parser.

`handler`  
`handler` is a string containing the name of a function that must exist
when <span class="function">xml\_parse</span> is called for `parser`.

The function named by `handler` must accept three parameters, and should
return an integer value. If the value returned from the handler is
**`FALSE`** (which it will be if no value is returned), the XML parser
will stop parsing and <span
class="function">xml\_get\_error\_code</span> will return
**`XML_ERROR_EXTERNAL_ENTITY_HANDLING`**.

<span class="methodname"><span class="replaceable">handler</span></span>
( <span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">string</span> `$prefix`</span> , <span
class="methodparam"><span class="type">string</span> `$uri`</span> )

`parser`  
<span class="simpara"> The first parameter, <span
class="replaceable">parser</span>, is a reference to the XML parser
calling the handler. </span>

`prefix`  
<span class="simpara"> The prefix is a string used to reference the
namespace within an XML object. </span>

`uri`  
<span class="simpara"> Uniform Resource Identifier (URI) of namespace.
</span>

If a handler function is set to an empty string, or **`FALSE`**, the
handler in question is disabled.

> **Note**: <span
> class="simpara">除了函数名，含有对象引用的数组和方法名也可以作为参数。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span
    class="function">xml\_set\_end\_namespace\_decl\_handler</span>

xml\_set\_unparsed\_entity\_decl\_handler
=========================================

建立未解析实体定义声明处理器

### 说明

<span class="type">bool</span> <span
class="methodname">xml\_set\_unparsed\_entity\_decl\_handler</span> (
<span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">callable</span> `$handler`</span> )

为 `parser` 参数指定的 XML 解析器建立未解析实体定义声明处理器函数。

当 XML 解析器遇到如下含有 NDATA 声明的外部实体定义声明时，该 `handler`
处理器将被调用：

``` xml
<!ENTITY <parameter>name</parameter> {<parameter>publicId</parameter> | <parameter>systemId</parameter>} 
        NDATA <parameter>notationName</parameter>
```

请参阅
<a href="http://www.w3.org/TR/1998/REC-xml-19980210#sec-external-ent" class="link external">» XML 1.0 参考的第 4.2.2 节</a>以获取有关已声明外部实体注释定义的信息。

### 参数

`parser`  
XML 解析器的引用，用于建立未解析实体定义声明处理器。

`handler`  
参数`handler` 为表示函数名称的字符串，这个函数必须在为 `parser`
指定的解析器调用 <span class="function">xml\_parse</span> 函数时已存在。

由 `handler` 参数命名的函数名必须接受六个参数：

<span class="methodname"><span class="replaceable">handler</span></span>
( <span class="methodparam"><span class="type">resource</span>
`$parser`</span> , <span class="methodparam"><span
class="type">string</span> `$entity_name`</span> , <span
class="methodparam"><span class="type">string</span> `$base`</span> ,
<span class="methodparam"><span class="type">string</span>
`$system_id`</span> , <span class="methodparam"><span
class="type">string</span> `$public_id`</span> , <span
class="methodparam"><span class="type">string</span>
`$notation_name`</span> )

`parser`  
<span class="simpara"> 第一个参数 <span
class="replaceable">parser</span> 为指向要调用处理器的 XML
解析器的指针。 </span>

`entity_name`  
<span class="simpara"> 将被定义的实体名。 </span>

`base`  
<span class="simpara">
这个参数是解析外部实体的系统标识符（`system_id`）的基础。当前该参数通常都被设置为空字符串。
</span>

`system_id`  
<span class="simpara"> 外部实体的系统标识符。 </span>

`public_id`  
<span class="simpara"> 外部实体的公共标识符。 </span>

`notation_name`  
<span class="simpara"> 该实体的注释名（请参阅 <span
class="function">xml\_set\_notation\_decl\_handler</span>）。 </span>

如果处理器函数名被设置为空字符串或者
**`FALSE`**，则该有问题的处理器将被屏蔽。

> **Note**: <span
> class="simpara">除了函数名，含有对象引用的数组和方法名也可以作为参数。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

**目录**

-   [utf8\_decode](/ref/xml.html#utf8_decode) — 将用 UTF-8 方式编码的
    ISO-8859-1 字符串转换成单字节的 ISO-8859-1 字符串。
-   [utf8\_encode](/ref/xml.html#utf8_encode) — 将 ISO-8859-1
    编码的字符串转换为 UTF-8 编码
-   [xml\_error\_string](/ref/xml.html#xml_error_string) — 获取 XML
    解析器的错误字符串
-   [xml\_get\_current\_byte\_index](/ref/xml.html#xml_get_current_byte_index)
    — 获取 XML 解析器的当前字节索引
-   [xml\_get\_current\_column\_number](/ref/xml.html#xml_get_current_column_number)
    — 获取 XML 解析器的当前列号
-   [xml\_get\_current\_line\_number](/ref/xml.html#xml_get_current_line_number)
    — 获取 XML 解析器的当前行号
-   [xml\_get\_error\_code](/ref/xml.html#xml_get_error_code) — 获取 XML
    解析器错误代码
-   [xml\_parse\_into\_struct](/ref/xml.html#xml_parse_into_struct) — 将
    XML 数据解析到数组中
-   [xml\_parse](/ref/xml.html#xml_parse) — 开始解析一个 XML 文档
-   [xml\_parser\_create\_ns](/ref/xml.html#xml_parser_create_ns) —
    生成一个支持命名空间的 XML 解析器
-   [xml\_parser\_create](/ref/xml.html#xml_parser_create) — 建立一个
    XML 解析器
-   [xml\_parser\_free](/ref/xml.html#xml_parser_free) — 释放指定的 XML
    解析器
-   [xml\_parser\_get\_option](/ref/xml.html#xml_parser_get_option) — 从
    XML 解析器获取选项设置信息
-   [xml\_parser\_set\_option](/ref/xml.html#xml_parser_set_option) —
    为指定 XML 解析进行选项设置
-   [xml\_set\_character\_data\_handler](/ref/xml.html#xml_set_character_data_handler)
    — 建立字符数据处理器
-   [xml\_set\_default\_handler](/ref/xml.html#xml_set_default_handler)
    — 建立默认处理器
-   [xml\_set\_element\_handler](/ref/xml.html#xml_set_element_handler)
    — 建立起始和终止元素处理器
-   [xml\_set\_end\_namespace\_decl\_handler](/ref/xml.html#xml_set_end_namespace_decl_handler)
    — 建立终止命名空间声明处理器
-   [xml\_set\_external\_entity\_ref\_handler](/ref/xml.html#xml_set_external_entity_ref_handler)
    — 建立外部实体指向处理器
-   [xml\_set\_notation\_decl\_handler](/ref/xml.html#xml_set_notation_decl_handler)
    — 建立注释声明处理器
-   [xml\_set\_object](/ref/xml.html#xml_set_object) — 在对象中使用 XML
    解析器
-   [xml\_set\_processing\_instruction\_handler](/ref/xml.html#xml_set_processing_instruction_handler)
    — 建立处理指令（PI）处理器
-   [xml\_set\_start\_namespace\_decl\_handler](/ref/xml.html#xml_set_start_namespace_decl_handler)
    — 建立起始命名空间声明处理器
-   [xml\_set\_unparsed\_entity\_decl\_handler](/ref/xml.html#xml_set_unparsed_entity_decl_handler)
    — 建立未解析实体定义声明处理器
