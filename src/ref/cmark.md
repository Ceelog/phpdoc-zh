CommonMark\\Parse
=================

Parsing

### 说明

<span class="type">CommonMark\\Node</span> <span
class="methodname">CommonMark\\Parse</span> ( <span
class="methodparam"><span class="type">string</span> `$content`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`</span> \] )

Shall parse `content`

### 参数

`content`  
markdown string

`options`  
A mask of:

**`CommonMark\Parser\Normal`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Parser\Normalize`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Parser\ValidateUTF8`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Parser\Smart`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

### 返回值

Shall return root CommonMark\\Node

CommonMark\\Render
==================

Rendering

### 说明

<span class="type">string</span> <span
class="methodname">CommonMark\\Render</span> ( <span
class="methodparam"><span class="type">CommonMark\\Node</span>
`$node`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`</span> \[, <span
class="methodparam"><span class="type">int</span> `$width`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`node`  

`options`  
A mask of:

**`CommonMark\Render\Normal`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\SourcePos`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\HardBreaks`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\Safe`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\NoBreaks`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

`width`  

### 返回值

CommonMark\\Render\\HTML
========================

Rendering

### 说明

<span class="type">string</span> <span
class="methodname">CommonMark\\Render\\HTML</span> ( <span
class="methodparam"><span class="type">CommonMark\\Node</span>
`$node`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`node`  

`options`  
A mask of:

**`CommonMark\Render\Normal`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\SourcePos`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\HardBreaks`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\Safe`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\NoBreaks`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

### 返回值

CommonMark\\Render\\Latex
=========================

Rendering

### 说明

<span class="type">string</span> <span
class="methodname">CommonMark\\Render\\Latex</span> ( <span
class="methodparam"><span class="type">CommonMark\\Node</span>
`$node`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`</span> \[, <span
class="methodparam"><span class="type">int</span> `$width`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`node`  

`options`  
A mask of:

**`CommonMark\Render\Normal`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\SourcePos`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\HardBreaks`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\Safe`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\NoBreaks`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

`width`  

### 返回值

CommonMark\\Render\\Man
=======================

Rendering

### 说明

<span class="type">string</span> <span
class="methodname">CommonMark\\Render\\Man</span> ( <span
class="methodparam"><span class="type">CommonMark\\Node</span>
`$node`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`</span> \[, <span
class="methodparam"><span class="type">int</span> `$width`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`node`  

`options`  
A mask of:

**`CommonMark\Render\Normal`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\SourcePos`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\HardBreaks`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\Safe`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\NoBreaks`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

`width`  

### 返回值

CommonMark\\Render\\XML
=======================

Rendering

### 说明

<span class="type">string</span> <span
class="methodname">CommonMark\\Render\\XML</span> ( <span
class="methodparam"><span class="type">CommonMark\\Node</span>
`$node`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`node`  

`options`  
A mask of:

**`CommonMark\Render\Normal`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\SourcePos`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\HardBreaks`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\Safe`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`CommonMark\Render\NoBreaks`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

### 返回值

**目录**

-   [CommonMark\\Parse](/ref/cmark.html#CommonMark\Parse) — Parsing
-   [CommonMark\\Render](/ref/cmark.html#CommonMark\Render) — Rendering
-   [CommonMark\\Render\\HTML](/ref/cmark.html#CommonMark\Render\HTML) —
    Rendering
-   [CommonMark\\Render\\Latex](/ref/cmark.html#CommonMark\Render\Latex)
    — Rendering
-   [CommonMark\\Render\\Man](/ref/cmark.html#CommonMark\Render\Man) —
    Rendering
-   [CommonMark\\Render\\XML](/ref/cmark.html#CommonMark\Render\XML) —
    Rendering
