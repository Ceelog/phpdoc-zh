XMLWriter::endAttribute
=======================

xmlwriter\_end\_attribute
=========================

End attribute

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::endAttribute</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_end\_attribute</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
)

Ends the current attribute.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startAttribute</span>
-   <span class="methodname">XMLWriter::startAttributeNs</span>
-   <span class="methodname">XMLWriter::writeAttribute</span>
-   <span class="methodname">XMLWriter::writeAttributeNs</span>

XMLWriter::endCdata
===================

xmlwriter\_end\_cdata
=====================

End current CDATA

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::endCdata</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_end\_cdata</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
)

Ends the current CDATA section.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startCdata</span>
-   <span class="methodname">XMLWriter::writeCdata</span>

XMLWriter::endComment
=====================

xmlwriter\_end\_comment
=======================

Create end comment

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::endComment</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_end\_comment</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
)

Ends the current comment.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startComment</span>
-   <span class="methodname">XMLWriter::writeComment</span>

XMLWriter::endDocument
======================

xmlwriter\_end\_document
========================

End current document

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::endDocument</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_end\_document</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
)

Ends the current document.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startDocument</span>

XMLWriter::endDtdAttlist
========================

xmlwriter\_end\_dtd\_attlist
============================

End current DTD AttList

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::endDtdAttlist</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_end\_dtd\_attlist</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
)

Ends the current DTD attribute list.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startDtdAttlist</span>
-   <span class="methodname">XMLWriter::writeDtdAttlist</span>

XMLWriter::endDtdElement
========================

xmlwriter\_end\_dtd\_element
============================

End current DTD element

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::endDtdElement</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_end\_dtd\_element</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
)

Ends the current DTD element.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startDtdElement</span>
-   <span class="methodname">XMLWriter::writeDtdElement</span>

XMLWriter::endDtdEntity
=======================

xmlwriter\_end\_dtd\_entity
===========================

End current DTD Entity

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::endDtdEntity</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_end\_dtd\_entity</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
)

Ends the current DTD entity.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startDtdEntity</span>
-   <span class="methodname">XMLWriter::writeDtdEntity</span>

XMLWriter::endDtd
=================

xmlwriter\_end\_dtd
===================

End current DTD

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::endDtd</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_end\_dtd</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
)

Ends the DTD of the document.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">XMLWriter::startDtd</span>
-   <span class="methodname">XMLWriter::writeDtd</span>

XMLWriter::endElement
=====================

xmlwriter\_end\_element
=======================

End current element

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::endElement</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_end\_element</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
)

Ends the current element.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startElement</span>
-   <span class="methodname">XMLWriter::writeElement</span>

XMLWriter::endPi
================

xmlwriter\_end\_pi
==================

End current PI

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::endPi</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_end\_pi</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
)

Ends the current processing instruction.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startPi</span>
-   <span class="methodname">XMLWriter::writePi</span>

XMLWriter::flush
================

xmlwriter\_flush
================

Flush current buffer

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">int</span></span> <span
class="methodname">XMLWriter::flush</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$empty`<span
class="initializer"> = **`TRUE`**</span></span> \] )

过程化风格

<span class="type"><span class="type">string</span><span
class="type">int</span></span> <span
class="methodname">xmlwriter\_flush</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$empty`<span class="initializer"> = **`TRUE`**</span></span> \] )

Flushes the current buffer.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`empty`  
Whether to empty the buffer or not. Default is **`TRUE`**.

### 返回值

If you opened the writer in memory, this function returns the generated
XML buffer, Else, if using URI, this function will write the buffer and
return the number of written bytes.

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |
| 8.0.0 | This function can no longer return **`FALSE`**.                                                                                           |

XMLWriter::fullEndElement
=========================

xmlwriter\_full\_end\_element
=============================

End current element

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::fullEndElement</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_full\_end\_element</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
)

End the current xml element. Writes an end tag even if the element is
empty.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::endElement</span>

XMLWriter::openMemory
=====================

xmlwriter\_open\_memory
=======================

Create new xmlwriter using memory for string output

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::openMemory</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type"><span class="type">XMLWriter</span><span
class="type">false</span></span> <span
class="methodname">xmlwriter\_open\_memory</span> ( <span
class="methodparam">void</span> )

Creates a new <span class="classname">XMLWriter</span> using memory for
string output.

### 参数

### 返回值

面向对象风格: 成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

过程化风格: Returns a new <span class="classname">XMLWriter</span> for
later use with the xmlwriter functions on success, 或者在失败时返回
**`FALSE`**.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                            |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | This function returns now an <span class="classname">XMLWriter</span> instance on success. Previouly, a <a href="/language/types/resource.html" class="link">资源(resource)</a> has been returned in this case. |

### 参见

-   <span class="methodname">XMLWriter::openUri</span>

XMLWriter::openUri
==================

xmlwriter\_open\_uri
====================

Create new xmlwriter using source uri for output

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::openUri</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> )

过程化风格

<span class="type"><span class="type">XMLWriter</span><span
class="type">false</span></span> <span
class="methodname">xmlwriter\_open\_uri</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> )

Creates a new <span class="classname">XMLWriter</span> using `uri` for
the output.

### 参数

`uri`  
The URI of the resource for the output.

### 返回值

面向对象风格: 成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

过程化风格: Returns a new <span class="classname">XMLWriter</span>
instance for later use with the xmlwriter functions on success,
或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                            |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | This function returns now an <span class="classname">XMLWriter</span> instance on success. Previouly, a <a href="/language/types/resource.html" class="link">资源(resource)</a> has been returned in this case. |

### 范例

**示例 \#1 Direct output of XML**

It is possible to directly output XML by using the
<a href="/wrappers/php.html#wrappers.php.output" class="link">php://output stream wrapper</a>.

``` php
<?php
$out =new XMLWriter();
$out->openURI('php://output');
?>
```

### 注释

> **Note**:
>
> On Windows, files opened with this function are locked until the
> writer is released.

### 参见

-   <span class="methodname">XMLWriter::openMemory</span>

XMLWriter::outputMemory
=======================

xmlwriter\_output\_memory
=========================

Returns current buffer

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">XMLWriter::outputMemory</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$flush`<span
class="initializer"> = **`TRUE`**</span></span> \] )

过程化风格

<span class="type">string</span> <span
class="methodname">xmlwriter\_output\_memory</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$flush`<span class="initializer"> = **`TRUE`**</span></span> \] )

Returns the current buffer.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`flush`  
Whether to flush the output buffer or not. Default is **`TRUE`**.

### 返回值

Returns the current buffer as a string.

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::flush</span>

XMLWriter::setIndentString
==========================

xmlwriter\_set\_indent\_string
==============================

Set string used for indenting

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::setIndentString</span> ( <span
class="methodparam"><span class="type">string</span>
`$indentation`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_set\_indent\_string</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$indentation`</span> )

Sets the string which will be used to indent each element/attribute of
the resulting xml.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`indentation`  
The indentation string.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 注释

> **Note**:
>
> The indent is reset when an xmlwriter is opened.

### 参见

-   <span class="methodname">XMLWriter::setIndent</span>

XMLWriter::setIndent
====================

xmlwriter\_set\_indent
======================

Toggle indentation on/off

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::setIndent</span> ( <span
class="methodparam"><span class="type">bool</span> `$enable`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_set\_indent</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">bool</span>
`$enable`</span> )

Toggles indentation on or off.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`enable`  
Whether indentation is enabled.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 范例

**示例 \#1 <span class="methodname">XMLWriter::setIndent</span> and
mixed Content**

Enabling indentation is not suitable for mixed content, because the
indent string is also inserted before inline elements.

``` php
<?php
$writer = new XMLWriter();
$writer->openMemory();
$writer->setIndent(2);
$writer->startDocument();
$writer->startElement('p');
$writer->text('before');
$writer->writeElement('a', 'element');
$writer->text('after');
$writer->endElement();
$writer->endDocument();
echo $writer->outputMemory();
?>
```

以上例程会输出：

    <?xml version="1.0"?>
    <p>before <a>element</a>
    after</p>

### 注释

> **Note**:
>
> The indent is reset when an xmlwriter is opened.

### 参见

-   <span class="methodname">XMLWriter::setIndentString</span>

XMLWriter::startAttributeNs
===========================

xmlwriter\_start\_attribute\_ns
===============================

Create start namespaced attribute

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::startAttributeNs</span> ( <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$prefix`</span> , <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$namespace`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_start\_attribute\_ns</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$prefix`</span> , <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$namespace`</span> )

Starts a namespaced attribute.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`prefix`  
The namespace prefix.

`name`  
The attribute name.

`namespace`  
The namespace URI. If `namespace` is **`NULL`**, the namespace
declaration will be omitted.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |
| 8.0.0 | `prefix` is nullable now.                                                                                                                 |

### 参见

-   <span class="methodname">XMLWriter::startAttribute</span>
-   <span class="methodname">XMLWriter::endAttribute</span>
-   <span class="methodname">XMLWriter::writeAttribute</span>
-   <span class="methodname">XMLWriter::writeAttributeNs</span>

XMLWriter::startAttribute
=========================

xmlwriter\_start\_attribute
===========================

Create start attribute

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::startAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_start\_attribute</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> )

Starts an attribute.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`name`  
The attribute name.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 范例

**示例 \#1 Basic <span
class="methodname">XMLWriter::startAttribute</span> Usage**

``` php
<?php
$writer = new XMLWriter;
$writer->openURI('php://output');
$writer->startDocument('1.0', 'UTF-8');?>
$writer->startElement('element');
$writer->startAttribute('attribute');
$writer->text('value');
$writer->endAttribute();
$writer->endElement();
$writer->endDocument();
```

以上例程的输出类似于：

    <?xml version="1.0" encoding="UTF-8"?>
    <element attribute="value"/>

### 参见

-   <span class="methodname">XMLWriter::startAttributeNs</span>
-   <span class="methodname">XMLWriter::endAttribute</span>
-   <span class="methodname">XMLWriter::writeAttribute</span>
-   <span class="methodname">XMLWriter::writeAttributeNs</span>

XMLWriter::startCdata
=====================

xmlwriter\_start\_cdata
=======================

Create start CDATA tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::startCdata</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_start\_cdata</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
)

Starts a CDATA.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::endCdata</span>
-   <span class="methodname">XMLWriter::writeCdata</span>

XMLWriter::startComment
=======================

xmlwriter\_start\_comment
=========================

Create start comment

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::startComment</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_start\_comment</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
)

Starts a comment.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::endComment</span>
-   <span class="methodname">XMLWriter::writeComment</span>

XMLWriter::startDocument
========================

xmlwriter\_start\_document
==========================

Create document tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::startDocument</span> (\[ <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$version`<span class="initializer"> = "1.0"</span></span> \[, <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$encoding`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$standalone`<span class="initializer"> = **`NULL`**</span></span>
\]\]\] )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_start\_document</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
\[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$version`<span class="initializer"> = "1.0"</span></span> \[, <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$encoding`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$standalone`<span class="initializer"> = **`NULL`**</span></span>
\]\]\] )

Starts a document.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`version`  
The version number of the document as part of the XML declaration.

`encoding`  
The encoding of the document as part of the XML declaration.

`standalone`  
*yes* or *no*.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::endDocument</span>

XMLWriter::startDtdAttlist
==========================

xmlwriter\_start\_dtd\_attlist
==============================

Create start DTD AttList

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::startDtdAttlist</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_start\_dtd\_attlist</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> )

Starts a DTD attribute list.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`name`  
The attribute list name.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::endDtdAttlist</span>
-   <span class="methodname">XMLWriter::writeDtdAttlist</span>

XMLWriter::startDtdElement
==========================

xmlwriter\_start\_dtd\_element
==============================

Create start DTD element

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::startDtdElement</span> ( <span
class="methodparam"><span class="type">string</span>
`$qualifiedName`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_start\_dtd\_element</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$qualifiedName`</span> )

Starts a DTD element.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`qualifiedName`  
The qualified name of the document type to create.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::endDtdElement</span>
-   <span class="methodname">XMLWriter::writeDtdElement</span>

XMLWriter::startDtdEntity
=========================

xmlwriter\_start\_dtd\_entity
=============================

Create start DTD Entity

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::startDtdEntity</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">bool</span>
`$isParam`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_start\_dtd\_entity</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">bool</span> `$isParam`</span> )

Starts a DTD entity.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`name`  
The name of the entity.

`isParam`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::endDtdEntity</span>
-   <span class="methodname">XMLWriter::writeDtdEntity</span>

XMLWriter::startDtd
===================

xmlwriter\_start\_dtd
=====================

Create start DTD tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::startDtd</span> ( <span
class="methodparam"><span class="type">string</span>
`$qualifiedName`</span> \[, <span class="methodparam"><span
class="type"><span class="type">string</span><span
class="type">null</span></span> `$publicId`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type"><span class="type">string</span><span
class="type">null</span></span> `$systemId`<span class="initializer"> =
**`NULL`**</span></span> \]\] )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_start\_dtd</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$qualifiedName`</span> \[, <span class="methodparam"><span
class="type"><span class="type">string</span><span
class="type">null</span></span> `$publicId`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type"><span class="type">string</span><span
class="type">null</span></span> `$systemId`<span class="initializer"> =
**`NULL`**</span></span> \]\] )

Starts a DTD.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`qualifiedName`  
The qualified name of the document type to create.

`publicId`  
The external subset public identifier.

`systemId`  
The external subset system identifier.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::endDtd</span>
-   <span class="methodname">XMLWriter::writeDtd</span>

XMLWriter::startElementNs
=========================

xmlwriter\_start\_element\_ns
=============================

Create start namespaced element tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::startElementNs</span> ( <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$prefix`</span> , <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$namespace`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_start\_element\_ns</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$prefix`</span> , <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$namespace`</span> )

Starts a namespaced element.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`prefix`  
The namespace prefix. If `prefix` is **`NULL`**, the namespace will be
omitted.

`name`  
The element name.

`namespace`  
The namespace URI. If `namespace` is **`NULL`**, the namespace
declaration will be omitted.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::endElement</span>
-   <span class="methodname">XMLWriter::writeElementNs</span>

XMLWriter::startElement
=======================

xmlwriter\_start\_element
=========================

Create start element tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::startElement</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_start\_element</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> )

Starts an element.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`name`  
The element name.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::endElement</span>
-   <span class="methodname">XMLWriter::writeElement</span>

XMLWriter::startPi
==================

xmlwriter\_start\_pi
====================

Create start PI tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::startPi</span> ( <span
class="methodparam"><span class="type">string</span> `$target`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_start\_pi</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$target`</span> )

Starts a processing instruction tag.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`target`  
The target of the processing instruction.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::endPi</span>
-   <span class="methodname">XMLWriter::writePi</span>

XMLWriter::text
===============

xmlwriter\_text
===============

Write text

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::text</span> ( <span
class="methodparam"><span class="type">string</span> `$content`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_text</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$content`</span> )

Writes a text.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`content`  
The contents of the text. The characters *\<*, *\>*, *&* and *"* are
written as entity references (i.e. *&lt;*, *&gt;*, *&amp;* and *&quot;*,
respectively). All other characters including *'* are written literally.
To write the special XML characters literally, or to write literal
entity references, <span class="function">xmlwriter\_write\_raw</span>
has to be used.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

XMLWriter::writeAttributeNs
===========================

xmlwriter\_write\_attribute\_ns
===============================

Write full namespaced attribute

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::writeAttributeNs</span> ( <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$prefix`</span> , <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$namespace`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_write\_attribute\_ns</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$prefix`</span> , <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$namespace`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

Writes a full namespaced attribute.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`prefix`  
The namespace prefix. If `prefix` is **`NULL`**, the namespace will be
omitted.

`name`  
The attribute name.

`namespace`  
The namespace URI. If `namespace` is **`NULL`**, the namespace
declaration will be omitted.

`value`  
The attribute value.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::writeAttribute</span>
-   <span class="methodname">XMLWriter::startAttribute</span>
-   <span class="methodname">XMLWriter::startAttributeNs</span>
-   <span class="methodname">XMLWriter::endAttribute</span>

XMLWriter::writeAttribute
=========================

xmlwriter\_write\_attribute
===========================

Write full attribute

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::writeAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_write\_attribute</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

Writes a full attribute.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`name`  
The name of the attribute.

`value`  
The value of the attribute.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 范例

**示例 \#1 Intermixing Sub-elements and Attributes**

If writing sub-elements and attributes is intermixed, any attempt to
write attributes after the first sub-element will fail and return false.

``` php
<?php
$xml = new XMLWriter();
$xml->openMemory();

$xml->startElement('element');
$xml->writeAttribute('attr1', '0');
$xml->writeElement('subelem', '0');
var_dump($xml->writeAttribute('attr2', '0'));
$xml->endElement();

echo $xml->flush();
?>
```

以上例程会输出：

    bool(false)
    <element attr1="0"><subelem>0</subelem></element>

### 参见

-   <span class="methodname">XMLWriter::writeAttributeNs</span>
-   <span class="methodname">XMLWriter::startAttribute</span>
-   <span class="methodname">XMLWriter::startAttributeNs</span>
-   <span class="methodname">XMLWriter::endAttribute</span>

XMLWriter::writeCdata
=====================

xmlwriter\_write\_cdata
=======================

Write full CDATA tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::writeCdata</span> ( <span
class="methodparam"><span class="type">string</span> `$content`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_write\_cdata</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$content`</span> )

Writes a full CDATA.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`content`  
The contents of the CDATA.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 范例

**示例 \#1 Basic <span class="function">xmlwriter\_write\_cdata</span>
Usage**

``` php
<?php
// set up the document
$xml = new XmlWriter();
$xml->openMemory();
$xml->setIndent(true);
$xml->startDocument('1.0', 'UTF-8');
$xml->startElement('mydoc');
$xml->startElement('myele');

// CData output
$xml->startElement('mycdataelement');
$xml->writeCData("text for inclusion as CData");
$xml->endElement();

// end the document and output
$xml->endElement();
$xml->endElement();
echo $xml->outputMemory(true);
?>
```

以上例程会输出：

    <mydoc>
     <myele>
      <mycdataelement><![CDATA[text for inclusion as CData]​]></mycdataelement>
     </myele>
    </mydoc>

### 参见

-   <span class="methodname">XMLWriter::startCdata</span>
-   <span class="methodname">XMLWriter::endCdata</span>

XMLWriter::writeComment
=======================

xmlwriter\_write\_comment
=========================

Write full comment tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::writeComment</span> ( <span
class="methodparam"><span class="type">string</span> `$content`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_write\_comment</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$content`</span> )

Writes a full comment.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`content`  
The contents of the comment.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startComment</span>
-   <span class="methodname">XMLWriter::endComment</span>

XMLWriter::writeDtdAttlist
==========================

xmlwriter\_write\_dtd\_attlist
==============================

Write full DTD AttList tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::writeDtdAttlist</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$content`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_write\_dtd\_attlist</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$content`</span> )

Writes a DTD attribute list.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`name`  
The name of the DTD attribute list.

`content`  
The content of the DTD attribute list.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startDtdAttlist</span>
-   <span class="methodname">XMLWriter::endDtdAttlist</span>

XMLWriter::writeDtdElement
==========================

xmlwriter\_write\_dtd\_element
==============================

Write full DTD element tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::writeDtdElement</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$content`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_write\_dtd\_element</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$content`</span> )

Writes a full DTD element.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`name`  
The name of the DTD element.

`content`  
The content of the element.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startDtdElement</span>
-   <span class="methodname">XMLWriter::endDtdElement</span>

XMLWriter::writeDtdEntity
=========================

xmlwriter\_write\_dtd\_entity
=============================

Write full DTD Entity tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::writeDtdEntity</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$isParam`<span class="initializer"> =
**`FALSE`**</span></span> \[, <span class="methodparam"><span
class="type"><span class="type">string</span><span
class="type">null</span></span> `$publicId`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type"><span class="type">string</span><span
class="type">null</span></span> `$systemId`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type"><span class="type">string</span><span
class="type">null</span></span> `$notationData`<span
class="initializer"> = **`NULL`**</span></span> \]\]\]\] )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_write\_dtd\_entity</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$content`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$isParam`<span
class="initializer"> = **`FALSE`**</span></span> \[, <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$publicId`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$systemId`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$notationData`<span class="initializer"> = **`NULL`**</span></span>
\]\]\]\] )

Writes a full DTD entity.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`name`  
The name of the entity.

`content`  
The content of the entity.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |
| 8.0.0 | `publicId`, `systemId` and `notationData` are nullable now.                                                                               |

### 参见

-   <span class="methodname">XMLWriter::startDtdEntity</span>
-   <span class="methodname">XMLWriter::endDtdEntity</span>

XMLWriter::writeDtd
===================

xmlwriter\_write\_dtd
=====================

Write full DTD tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::writeDtd</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$publicId`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$systemId`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$content`<span class="initializer"> = **`NULL`**</span></span> \]\]\] )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_write\_dtd</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$publicId`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$systemId`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$content`<span class="initializer"> = **`NULL`**</span></span> \]\]\] )

Writes a full DTD.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`name`  
The DTD name.

`publicId`  
The external subset public identifier.

`systemId`  
The external subset system identifier.

`content`  
The content of the DTD.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startDtd</span>
-   <span class="methodname">XMLWriter::endDtd</span>

XMLWriter::writeElementNs
=========================

xmlwriter\_write\_element\_ns
=============================

Write full namespaced element tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::writeElementNs</span> ( <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$prefix`</span> , <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$namespace`</span> \[, <span class="methodparam"><span
class="type"><span class="type">string</span><span
class="type">null</span></span> `$content`<span class="initializer"> =
**`NULL`**</span></span> \] )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_write\_element\_ns</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$prefix`</span> , <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$namespace`</span> \[, <span class="methodparam"><span
class="type"><span class="type">string</span><span
class="type">null</span></span> `$content`<span class="initializer"> =
**`NULL`**</span></span> \] )

Writes a full namespaced element tag.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`prefix`  
The namespace prefix. If `prefix` is **`NULL`**, the namespace will be
omitted.

`name`  
The element name.

`namespace`  
The namespace URI. If `namespace` is **`NULL`**, the namespace
declaration will be omitted.

`content`  
The element contents.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startElementNs</span>
-   <span class="methodname">XMLWriter::endElement</span>
-   <span class="methodname">XMLWriter::writeElement</span>

XMLWriter::writeElement
=======================

xmlwriter\_write\_element
=========================

Write full element tag

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::writeElement</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$content`<span class="initializer"> = **`NULL`**</span></span> \] )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_write\_element</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$content`<span class="initializer"> = **`NULL`**</span></span> \] )

Writes a full element tag.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`name`  
The element name.

`content`  
The element contents.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startElement</span>
-   <span class="methodname">XMLWriter::endElement</span>
-   <span class="methodname">XMLWriter::writeElementNs</span>

XMLWriter::writePi
==================

xmlwriter\_write\_pi
====================

Writes a PI

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::writePi</span> ( <span
class="methodparam"><span class="type">string</span> `$target`</span> ,
<span class="methodparam"><span class="type">string</span>
`$content`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_write\_pi</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$target`</span> , <span class="methodparam"><span
class="type">string</span> `$content`</span> )

Writes a processing instruction.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`target`  
The target of the processing instruction.

`content`  
The content of the processing instruction.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::startPi</span>
-   <span class="methodname">XMLWriter::endPi</span>

XMLWriter::writeRaw
===================

xmlwriter\_write\_raw
=====================

Write a raw XML text

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLWriter::writeRaw</span> ( <span
class="methodparam"><span class="type">string</span> `$content`</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">xmlwriter\_write\_raw</span> ( <span
class="methodparam"><span class="type">XMLWriter</span> `$writer`</span>
, <span class="methodparam"><span class="type">string</span>
`$content`</span> )

Writes a raw xml text.

### 参数

` xmlwriter`  
仅用于过程调用。被修改的 XMLWriter <span
class="type">resource</span>。此资源来自于对 <span
class="function">xmlwriter\_open\_uri</span> 或 <span
class="function">xmlwriter\_open\_memory</span> 的调用。

`content`  
The text string to write.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `writer` expects an <span class="classname">XMLWriter</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="methodname">XMLWriter::text</span>

**目录**

-   [XMLWriter::endAttribute](/ref/xmlwriter.html#XMLWriter::endAttribute)
    — End attribute
-   [XMLWriter::endCdata](/ref/xmlwriter.html#XMLWriter::endCdata) — End
    current CDATA
-   [XMLWriter::endComment](/ref/xmlwriter.html#XMLWriter::endComment) —
    Create end comment
-   [XMLWriter::endDocument](/ref/xmlwriter.html#XMLWriter::endDocument)
    — End current document
-   [XMLWriter::endDtdAttlist](/ref/xmlwriter.html#XMLWriter::endDtdAttlist)
    — End current DTD AttList
-   [XMLWriter::endDtdElement](/ref/xmlwriter.html#XMLWriter::endDtdElement)
    — End current DTD element
-   [XMLWriter::endDtdEntity](/ref/xmlwriter.html#XMLWriter::endDtdEntity)
    — End current DTD Entity
-   [XMLWriter::endDtd](/ref/xmlwriter.html#XMLWriter::endDtd) — End
    current DTD
-   [XMLWriter::endElement](/ref/xmlwriter.html#XMLWriter::endElement) —
    End current element
-   [XMLWriter::endPi](/ref/xmlwriter.html#XMLWriter::endPi) — End
    current PI
-   [XMLWriter::flush](/ref/xmlwriter.html#XMLWriter::flush) — Flush
    current buffer
-   [XMLWriter::fullEndElement](/ref/xmlwriter.html#XMLWriter::fullEndElement)
    — End current element
-   [XMLWriter::openMemory](/ref/xmlwriter.html#XMLWriter::openMemory) —
    Create new xmlwriter using memory for string output
-   [XMLWriter::openUri](/ref/xmlwriter.html#XMLWriter::openUri) —
    Create new xmlwriter using source uri for output
-   [XMLWriter::outputMemory](/ref/xmlwriter.html#XMLWriter::outputMemory)
    — Returns current buffer
-   [XMLWriter::setIndentString](/ref/xmlwriter.html#XMLWriter::setIndentString)
    — Set string used for indenting
-   [XMLWriter::setIndent](/ref/xmlwriter.html#XMLWriter::setIndent) —
    Toggle indentation on/off
-   [XMLWriter::startAttributeNs](/ref/xmlwriter.html#XMLWriter::startAttributeNs)
    — Create start namespaced attribute
-   [XMLWriter::startAttribute](/ref/xmlwriter.html#XMLWriter::startAttribute)
    — Create start attribute
-   [XMLWriter::startCdata](/ref/xmlwriter.html#XMLWriter::startCdata) —
    Create start CDATA tag
-   [XMLWriter::startComment](/ref/xmlwriter.html#XMLWriter::startComment)
    — Create start comment
-   [XMLWriter::startDocument](/ref/xmlwriter.html#XMLWriter::startDocument)
    — Create document tag
-   [XMLWriter::startDtdAttlist](/ref/xmlwriter.html#XMLWriter::startDtdAttlist)
    — Create start DTD AttList
-   [XMLWriter::startDtdElement](/ref/xmlwriter.html#XMLWriter::startDtdElement)
    — Create start DTD element
-   [XMLWriter::startDtdEntity](/ref/xmlwriter.html#XMLWriter::startDtdEntity)
    — Create start DTD Entity
-   [XMLWriter::startDtd](/ref/xmlwriter.html#XMLWriter::startDtd) —
    Create start DTD tag
-   [XMLWriter::startElementNs](/ref/xmlwriter.html#XMLWriter::startElementNs)
    — Create start namespaced element tag
-   [XMLWriter::startElement](/ref/xmlwriter.html#XMLWriter::startElement)
    — Create start element tag
-   [XMLWriter::startPi](/ref/xmlwriter.html#XMLWriter::startPi) —
    Create start PI tag
-   [XMLWriter::text](/ref/xmlwriter.html#XMLWriter::text) — Write text
-   [XMLWriter::writeAttributeNs](/ref/xmlwriter.html#XMLWriter::writeAttributeNs)
    — Write full namespaced attribute
-   [XMLWriter::writeAttribute](/ref/xmlwriter.html#XMLWriter::writeAttribute)
    — Write full attribute
-   [XMLWriter::writeCdata](/ref/xmlwriter.html#XMLWriter::writeCdata) —
    Write full CDATA tag
-   [XMLWriter::writeComment](/ref/xmlwriter.html#XMLWriter::writeComment)
    — Write full comment tag
-   [XMLWriter::writeDtdAttlist](/ref/xmlwriter.html#XMLWriter::writeDtdAttlist)
    — Write full DTD AttList tag
-   [XMLWriter::writeDtdElement](/ref/xmlwriter.html#XMLWriter::writeDtdElement)
    — Write full DTD element tag
-   [XMLWriter::writeDtdEntity](/ref/xmlwriter.html#XMLWriter::writeDtdEntity)
    — Write full DTD Entity tag
-   [XMLWriter::writeDtd](/ref/xmlwriter.html#XMLWriter::writeDtd) —
    Write full DTD tag
-   [XMLWriter::writeElementNs](/ref/xmlwriter.html#XMLWriter::writeElementNs)
    — Write full namespaced element tag
-   [XMLWriter::writeElement](/ref/xmlwriter.html#XMLWriter::writeElement)
    — Write full element tag
-   [XMLWriter::writePi](/ref/xmlwriter.html#XMLWriter::writePi) —
    Writes a PI
-   [XMLWriter::writeRaw](/ref/xmlwriter.html#XMLWriter::writeRaw) —
    Write a raw XML text
