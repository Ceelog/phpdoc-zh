XML diff and merge
==================

**目录**

-   [简介](/intro/xmldiff.html)
-   [安装／配置](/xmldiff/setup.html)
    -   [需求](/xmldiff/setup.html#需求)
    -   [安装](/xmldiff/setup.html#安装)
-   [XMLDiff\\Base](/class/xmldiff-base.html) — The XMLDiff\\Base class
    -   [XMLDiff\\Base::\_\_construct](/class/xmldiff-base.html#XMLDiff\Base::__construct)
        — Constructor
    -   [XMLDiff\\Base::diff](/class/xmldiff-base.html#XMLDiff\Base::diff)
        — Produce diff of two XML documents
    -   [XMLDiff\\Base::merge](/class/xmldiff-base.html#XMLDiff\Base::merge)
        — Produce new XML document based on diff
-   [XMLDiff\\DOM](/class/xmldiff-dom.html) — The XMLDiff\\DOM class
    -   [XMLDiff\\DOM::diff](/class/xmldiff-dom.html#XMLDiff\DOM::diff)
        — Diff two DOMDocument objects
    -   [XMLDiff\\DOM::merge](/class/xmldiff-dom.html#XMLDiff\DOM::merge)
        — Produce merged DOMDocument
-   [XMLDiff\\Memory](/class/xmldiff-memory.html) — The XMLDiff\\Memory
    class
    -   [XMLDiff\\Memory::diff](/class/xmldiff-memory.html#XMLDiff\Memory::diff)
        — Diff two XML documents
    -   [XMLDiff\\Memory::merge](/class/xmldiff-memory.html#XMLDiff\Memory::merge)
        — Produce merged XML document
-   [XMLDiff\\File](/class/xmldiff-file.html) — The XMLDiff\\File class
    -   [XMLDiff\\File::diff](/class/xmldiff-file.html#XMLDiff\File::diff)
        — Diff two XML files
    -   [XMLDiff\\File::merge](/class/xmldiff-file.html#XMLDiff\File::merge)
        — Produce merged XML document

简介
----

Base abstract class for all the comparsion classes in the extension.

类摘要
------

**XMLDiff\\Base**

<span class="ooclass"> class **XMLDiff\\Base** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$nsname`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">diff</span> ( <span class="methodparam"><span
class="type">mixed</span> `$from`</span> , <span
class="methodparam"><span class="type">mixed</span> `$to`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">merge</span> ( <span class="methodparam"><span
class="type">mixed</span> `$src`</span> , <span
class="methodparam"><span class="type">mixed</span> `$diff`</span> )

}

XMLDiff\\Base::\_\_construct
============================

Constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">XMLDiff\\Base::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$nsname`</span> )

Base constructor for all the worker classes in the xmldiff extension.

### 参数

`nsname`  
Custom namespace name for the diff document. The default namespace is
http://www.locus.cz/diffmark and that's enough to avoid namespace
conflicts. Use this parameter if you want to change it for some reason.

### 返回值

XMLDiff\\Base::diff
===================

Produce diff of two XML documents

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">XMLDiff\\Base::diff</span> ( <span
class="methodparam"><span class="type">mixed</span> `$from`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$to`</span> )

Abstract diff method to be implemented by inheriting classes.

The basic purpose of this method is to produce diff of the two
documents. The param order matters and will produce different output.

### 参数

`from`  
Source XML document.

`to`  
Target XML document.

### 返回值

Implementation dependent.

XMLDiff\\Base::merge
====================

Produce new XML document based on diff

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">XMLDiff\\Base::merge</span> ( <span
class="methodparam"><span class="type">mixed</span> `$src`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$diff`</span>
)

Abstract merge method to be implemented by inheriting classes.

Basically the method purpose is to produce a new XML document based on
the diff information.

### 参数

`src`  
Source XML document.

`diff`  
Document produced by the diff method.

### 返回值

Implementation dependent.

简介
----

类摘要
------

**XMLDiff\\DOM**

<span class="ooclass"> class **XMLDiff\\DOM** </span> <span
class="ooclass"> <span class="modifier">extends</span> **XMLDiff\\Base**
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="type">DOMDocument</span> <span class="methodname">diff</span> (
<span class="methodparam"><span class="type">DOMDocument</span>
`$from`</span> , <span class="methodparam"><span
class="type">DOMDocument</span> `$to`</span> )

<span class="modifier">public</span> <span
class="type">DOMDocument</span> <span class="methodname">merge</span> (
<span class="methodparam"><span class="type">DOMDocument</span>
`$src`</span> , <span class="methodparam"><span
class="type">DOMDocument</span> `$diff`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">XMLDiff\\Base::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$nsname`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">XMLDiff\\Base::diff</span> ( <span
class="methodparam"><span class="type">mixed</span> `$from`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$to`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">XMLDiff\\Base::merge</span> ( <span
class="methodparam"><span class="type">mixed</span> `$src`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$diff`</span>
)

}

XMLDiff\\DOM::diff
==================

Diff two DOMDocument objects

### 说明

<span class="modifier">public</span> <span
class="type">DOMDocument</span> <span
class="methodname">XMLDiff\\DOM::diff</span> ( <span
class="methodparam"><span class="type">DOMDocument</span> `$from`</span>
, <span class="methodparam"><span class="type">DOMDocument</span>
`$to`</span> )

Diff two DOMDocument instances and produce the new one containing the
diff information.

### 参数

`from`  
Source DOMDocument object.

`to`  
Target DOMDocument object.

### 返回值

DOMDocument with the diff information or NULL.

XMLDiff\\DOM::merge
===================

Produce merged DOMDocument

### 说明

<span class="modifier">public</span> <span
class="type">DOMDocument</span> <span
class="methodname">XMLDiff\\DOM::merge</span> ( <span
class="methodparam"><span class="type">DOMDocument</span> `$src`</span>
, <span class="methodparam"><span class="type">DOMDocument</span>
`$diff`</span> )

Create new DOMDocument based on the diff.

### 参数

`src`  
Source DOMDocument object.

`diff`  
DOMDocument object containing the diff information.

### 返回值

Merged DOMDocument or NULL.

简介
----

类摘要
------

**XMLDiff\\Memory**

<span class="ooclass"> class **XMLDiff\\Memory** </span> <span
class="ooclass"> <span class="modifier">extends</span> **XMLDiff\\Base**
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">diff</span> ( <span class="methodparam"><span
class="type">string</span> `$from`</span> , <span
class="methodparam"><span class="type">string</span> `$to`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">merge</span> ( <span class="methodparam"><span
class="type">string</span> `$src`</span> , <span
class="methodparam"><span class="type">string</span> `$diff`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">XMLDiff\\Base::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$nsname`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">XMLDiff\\Base::diff</span> ( <span
class="methodparam"><span class="type">mixed</span> `$from`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$to`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">XMLDiff\\Base::merge</span> ( <span
class="methodparam"><span class="type">mixed</span> `$src`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$diff`</span>
)

}

XMLDiff\\Memory::diff
=====================

Diff two XML documents

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">XMLDiff\\Memory::diff</span> ( <span
class="methodparam"><span class="type">string</span> `$from`</span> ,
<span class="methodparam"><span class="type">string</span> `$to`</span>
)

Diff two strings containing XML documents and produce the diff
information.

### 参数

`from`  
Source XML document.

`to`  
Target XML document.

### 返回值

String with the XML document containing the diff information or NULL.

XMLDiff\\Memory::merge
======================

Produce merged XML document

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">XMLDiff\\Memory::merge</span> ( <span
class="methodparam"><span class="type">string</span> `$src`</span> ,
<span class="methodparam"><span class="type">string</span>
`$diff`</span> )

Create new XML document based on diffs and source document.

### 参数

`src`  
Source XML document.

`diff`  
XML document containing diff information.

### 返回值

String with the new XML document or NULL.

简介
----

类摘要
------

**XMLDiff\\File**

<span class="ooclass"> class **XMLDiff\\File** </span> <span
class="ooclass"> <span class="modifier">extends</span> **XMLDiff\\Base**
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">diff</span> ( <span class="methodparam"><span
class="type">string</span> `$from`</span> , <span
class="methodparam"><span class="type">string</span> `$to`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">merge</span> ( <span class="methodparam"><span
class="type">string</span> `$src`</span> , <span
class="methodparam"><span class="type">string</span> `$diff`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">XMLDiff\\Base::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$nsname`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">XMLDiff\\Base::diff</span> ( <span
class="methodparam"><span class="type">mixed</span> `$from`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$to`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">XMLDiff\\Base::merge</span> ( <span
class="methodparam"><span class="type">mixed</span> `$src`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$diff`</span>
)

}

XMLDiff\\File::diff
===================

Diff two XML files

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">XMLDiff\\File::diff</span> ( <span
class="methodparam"><span class="type">string</span> `$from`</span> ,
<span class="methodparam"><span class="type">string</span> `$to`</span>
)

Diff two local XML files and produce string with the diff information.

### 参数

`from`  
Path to the source document.

`to`  
Path to the target document.

### 返回值

String with the XML document containing the diff information or NULL.

XMLDiff\\File::merge
====================

Produce merged XML document

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">XMLDiff\\File::merge</span> ( <span
class="methodparam"><span class="type">string</span> `$src`</span> ,
<span class="methodparam"><span class="type">string</span>
`$diff`</span> )

Create new XML document based on diffs and source document.

### 参数

`src`  
Path to the source XML document.

`diff`  
Path to the XML document with the diff information.

### 返回值

String with the new XML document or NULL.
