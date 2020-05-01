XLSWriter
=========

**目录**

-   [简介](/intro/xlswriter.html)
-   [安装／配置](/xlswriter/setup.html)
    -   [需求](/xlswriter/setup.html#需求)
    -   [安装](/xlswriter/setup.html#安装)
    -   [资源类型](/xlswriter/setup.html#资源类型)
-   [预定义常量](/xlswriter/constants.html)
-   [Vtiful\\Kernel\\Excel](/class/vtiful-kernel-excel.html) — The
    Vtiful\\Kernel\\Excel class
    -   [Vtiful\\Kernel\\Excel::addSheet](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::addSheet)
        — Vtiful\\Kernel\\Excel addSheet
    -   [Vtiful\\Kernel\\Excel::autoFilter](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::autoFilter)
        — Vtiful\\Kernel\\Excel autoFilter
    -   [Vtiful\\Kernel\\Excel::constMemory](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::constMemory)
        — Vtiful\\Kernel\\Excel constMemory
    -   [Vtiful\\Kernel\\Excel::\_\_construct](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::__construct)
        — Vtiful\\Kernel\\Excel constructor
    -   [Vtiful\\Kernel\\Excel::data](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::data)
        — Vtiful\\Kernel\\Excel data
    -   [Vtiful\\Kernel\\Excel::fileName](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::fileName)
        — Vtiful\\Kernel\\Excel fileName
    -   [Vtiful\\Kernel\\Excel::getHandle](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::getHandle)
        — Vtiful\\Kernel\\Excel getHandle
    -   [Vtiful\\Kernel\\Excel::header](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::header)
        — Vtiful\\Kernel\\Excel header
    -   [Vtiful\\Kernel\\Excel::insertFormula](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::insertFormula)
        — Vtiful\\Kernel\\Excel insertFormula
    -   [Vtiful\\Kernel\\Excel::insertImage](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::insertImage)
        — Vtiful\\Kernel\\Excel insertImage
    -   [Vtiful\\Kernel\\Excel::insertText](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::insertText)
        — Vtiful\\Kernel\\Excel insertText
    -   [Vtiful\\Kernel\\Excel::mergeCells](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::mergeCells)
        — Vtiful\\Kernel\\Excel mergeCells
    -   [Vtiful\\Kernel\\Excel::output](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::output)
        — Vtiful\\Kernel\\Excel output
    -   [Vtiful\\Kernel\\Excel::setColumn](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::setColumn)
        — Vtiful\\Kernel\\Excel setColumn
    -   [Vtiful\\Kernel\\Excel::setRow](/class/vtiful-kernel-excel.html#Vtiful\Kernel\Excel::setRow)
        — Vtiful\\Kernel\\Excel setRow
-   [Vtiful\\Kernel\\Format](/class/vtiful-kernel-format.html) — The
    Vtiful\\Kernel\\Format class
    -   [Vtiful\\Kernel\\Format::align](/class/vtiful-kernel-format.html#Vtiful\Kernel\Format::align)
        — Vtiful\\Kernel\\Format align
    -   [Vtiful\\Kernel\\Format::bold](/class/vtiful-kernel-format.html#Vtiful\Kernel\Format::bold)
        — Vtiful\\Kernel\\Format bold
    -   [Vtiful\\Kernel\\Format::italic](/class/vtiful-kernel-format.html#Vtiful\Kernel\Format::italic)
        — Vtiful\\Kernel\\Format italic
    -   [Vtiful\\Kernel\\Format::underline](/class/vtiful-kernel-format.html#Vtiful\Kernel\Format::underline)
        — Vtiful\\Kernel\\Format underline

简介
----

Create xlsx files and set cells and output xlsx files

类摘要
------

**Vtiful\\Kernel\\Excel**

<span class="ooclass"> class **Vtiful\\Kernel\\Excel** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">addSheet</span> ( <span class="methodparam"><span
class="type">string</span> `$sheetName`</span> )

<span class="modifier">public</span> <span
class="methodname">autoFilter</span> ( <span class="methodparam"><span
class="type">string</span> `$scope`</span> )

<span class="modifier">public</span> <span
class="methodname">constMemory</span> ( <span class="methodparam"><span
class="type">string</span> `$fileName`</span> \[, <span
class="methodparam"><span class="type">string</span> `$sheetName`</span>
\] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">array</span> `$config`</span> )

<span class="modifier">public</span> <span
class="methodname">data</span> ( <span class="methodparam"><span
class="type">array</span> `$data`</span> )

<span class="modifier">public</span> <span
class="methodname">fileName</span> ( <span class="methodparam"><span
class="type">string</span> `$fileName`</span> \[, <span
class="methodparam"><span class="type">string</span> `$sheetName`</span>
\] )

<span class="modifier">public</span> <span
class="methodname">getHandle</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">header</span> ( <span class="methodparam"><span
class="type">array</span> `$headerData`</span> )

<span class="modifier">public</span> <span
class="methodname">insertFormula</span> ( <span
class="methodparam"><span class="type">int</span> `$row`</span> , <span
class="methodparam"><span class="type">int</span> `$column`</span> ,
<span class="methodparam"><span class="type">string</span>
`$formula`</span> )

<span class="modifier">public</span> <span
class="methodname">insertImage</span> ( <span class="methodparam"><span
class="type">int</span> `$row`</span> , <span class="methodparam"><span
class="type">int</span> `$column`</span> , <span
class="methodparam"><span class="type">string</span>
`$localImagePath`</span> )

<span class="modifier">public</span> <span
class="methodname">insertText</span> ( <span class="methodparam"><span
class="type">int</span> `$row`</span> , <span class="methodparam"><span
class="type">int</span> `$column`</span> , <span
class="methodparam"><span class="type">string</span><span
class="type">int</span><span class="type">double</span> `$data`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$format`</span> \] )

<span class="modifier">public</span> <span
class="methodname">mergeCells</span> ( <span class="methodparam"><span
class="type">string</span> `$scope`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span
class="methodname">output</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span
class="methodname">setColumn</span> ( <span class="methodparam"><span
class="type">string</span> `$range`</span> , <span
class="methodparam"><span class="type">float</span> `$width`</span> \[,
<span class="methodparam"><span class="type">resource</span>
`$format`</span> \] )

<span class="modifier">public</span> <span
class="methodname">setRow</span> ( <span class="methodparam"><span
class="type">string</span> `$range`</span> , <span
class="methodparam"><span class="type">float</span> `$height`</span> \[,
<span class="methodparam"><span class="type">resource</span>
`$format`</span> \] )

}

Vtiful\\Kernel\\Excel::addSheet
===============================

Vtiful\\Kernel\\Excel addSheet

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::addSheet</span> ( <span
class="methodparam"><span class="type">string</span> `$sheetName`</span>
)

Create a new worksheet in the xlsx file.

### 参数

`sheetName`  
Worksheet name

### 返回值

<span class="classname">Vtiful\\Kernel\\Excel</span> instance

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$fileObject  = new \Vtiful\Kernel\Excel($config);

$file = $fileObject->fileName('tutorial.xlsx', 'sheet_one')
    ->header(['name', 'age'])
    ->data([
        ['viest', 23],
        ['wjx', 23]
    ]);

$file->addSheet('sheet_two')
    ->header(['name', 'age'])
    ->data([
        ['james', 33],
        ['king', 33]
    ]);

$file->output();
?>
```

Vtiful\\Kernel\\Excel::autoFilter
=================================

Vtiful\\Kernel\\Excel autoFilter

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::autoFilter</span> ( <span
class="methodparam"><span class="type">string</span> `$scope`</span> )

Add autofilter to a worksheet.

### 参数

`scope`  
Cell start and end coordinate string.

### 返回值

<span class="classname">Vtiful\\Kernel\\Excel</span> instance

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$fileObject  = new \Vtiful\Kernel\Excel($config);

$file = $excel->fileName('test.xlsx')
        ->header(['name', 'age'])
        ->data($data)
        ->autoFilter('A1:B11')  // auto filter
        ->output();
?>
```

Vtiful\\Kernel\\Excel::constMemory
==================================

Vtiful\\Kernel\\Excel constMemory

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::constMemory</span> ( <span
class="methodparam"><span class="type">string</span> `$fileName`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$sheetName`</span> \] )

Write a large file with constant memory usage.

### 参数

`fileName`  
XLSX file name

`sheetName`  
Worksheet name

### 返回值

<span class="classname">Vtiful\\Kernel\\Excel</span> instance

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
  'path' => '/home/viest'
];

$fileObject = new \Vtiful\Kernel\Excel($config);

$file = $instance->constMemory('tutorial.xlsx', 'sheet');
?>
```

Vtiful\\Kernel\\Excel::\_\_construct
====================================

Vtiful\\Kernel\\Excel constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::\_\_construct</span> ( <span
class="methodparam"><span class="type">array</span> `$config`</span> )

<span class="classname">Vtiful\\Kernel\\Excel</span> constructor, create
a class object.

### 参数

`config`  
XLSX file export configuration

### 返回值

<span class="classname">Vtiful\\Kernel\\Excel</span> instance

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
  'path' => '/home/viest'
];

$excelObject = new \Vtiful\Kernel\Excel($config);
?>
```

Vtiful\\Kernel\\Excel::data
===========================

Vtiful\\Kernel\\Excel data

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::data</span> ( <span
class="methodparam"><span class="type">array</span> `$data`</span> )

Write a data in the worksheet.

### 参数

`data`  
worksheet data

### 返回值

<span class="classname">Vtiful\\Kernel\\Excel</span> instance

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$fileObject  = new \Vtiful\Kernel\Excel($config);

$file = $fileObject->fileName('tutorial.xlsx', 'sheet_one')
    ->header(['name', 'age'])
    ->data([
      ['viest', 23],
      ['wjx', 23],
    ]);
?>
```

Vtiful\\Kernel\\Excel::fileName
===============================

Vtiful\\Kernel\\Excel fileName

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::fileName</span> ( <span
class="methodparam"><span class="type">string</span> `$fileName`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$sheetName`</span> \] )

Create a brand new xlsx file and create a worksheet.

### 参数

`fileName`  
XLSX file name

`sheetName`  
Worksheet name

### 返回值

<span class="classname">Vtiful\\Kernel\\Excel</span> instance

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
  'path' => '/home/viest'
];

$fileObject = new \Vtiful\Kernel\Excel($config);

$file = $instance->fileName('tutorial.xlsx', 'sheet');
?>
```

Vtiful\\Kernel\\Excel::getHandle
================================

Vtiful\\Kernel\\Excel getHandle

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::getHandle</span> ( <span
class="methodparam">void</span> )

Get the xlsx text resource handle.

### 参数

此函数没有参数。

### 返回值

Resource

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$fileObject  = new \Vtiful\Kernel\Excel($config);

$file = $fileObject->fileName('tutorial.xlsx', 'sheet_one')
    ->header(['name', 'age']);

$handle = $file->getHandle();
?>
```

Vtiful\\Kernel\\Excel::header
=============================

Vtiful\\Kernel\\Excel header

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::header</span> ( <span
class="methodparam"><span class="type">array</span> `$headerData`</span>
)

Write a header in the worksheet.

### 参数

`headerData`  
worksheet header data

### 返回值

<span class="classname">Vtiful\\Kernel\\Excel</span> instance

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$fileObject  = new \Vtiful\Kernel\Excel($config);

$file = $fileObject->fileName('tutorial.xlsx', 'sheet_one')
    ->header(['name', 'age']);
?>
```

Vtiful\\Kernel\\Excel::insertFormula
====================================

Vtiful\\Kernel\\Excel insertFormula

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::insertFormula</span> ( <span
class="methodparam"><span class="type">int</span> `$row`</span> , <span
class="methodparam"><span class="type">int</span> `$column`</span> ,
<span class="methodparam"><span class="type">string</span>
`$formula`</span> )

Insert calculation formula.

### 参数

`row`  
cell row

`column`  
cell column

`formula`  
formula string

### 返回值

<span class="classname">Vtiful\\Kernel\\Excel</span> instance

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$excel = new \Vtiful\Kernel\Excel($config);

$file = $excel->fileName("free.xlsx")
    ->header(['name', 'money']);

for($index = 1; $index < 10; $index++) {
    $file->insertText($index, 0, 'viest');
    $file->insertText($index, 1, 10);
}

$file->insertText(12, 0, "Total");
$file->insertFormula(12, 1, '=SUM(B2:B11)'); // insert formula

$file->output();
```

Vtiful\\Kernel\\Excel::insertImage
==================================

Vtiful\\Kernel\\Excel insertImage

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::insertImage</span> ( <span
class="methodparam"><span class="type">int</span> `$row`</span> , <span
class="methodparam"><span class="type">int</span> `$column`</span> ,
<span class="methodparam"><span class="type">string</span>
`$localImagePath`</span> )

Insert a local image into the cell.

### 参数

`row`  
cell row

`column`  
cell column

`localImagePath`  
local image path

### 返回值

<span class="classname">Vtiful\\Kernel\\Excel</span> instance

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$excel = new \Vtiful\Kernel\Excel($config);

$file = $excel->fileName("free.xlsx");

$file->insertImage(5, 0, '/vagrant/ASW-G-66.jpg');

$file->output();
```

Vtiful\\Kernel\\Excel::insertText
=================================

Vtiful\\Kernel\\Excel insertText

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::insertText</span> ( <span
class="methodparam"><span class="type">int</span> `$row`</span> , <span
class="methodparam"><span class="type">int</span> `$column`</span> ,
<span class="methodparam"><span class="type">string</span><span
class="type">int</span><span class="type">double</span> `$data`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$format`</span> \] )

Write text in a cell.

### 参数

`row`  
cell row

`column`  
cell column

`data`  
data to be written

`format`  
String format

### 返回值

<span class="classname">Vtiful\\Kernel\\Excel</span> instance

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$excel = new \Vtiful\Kernel\Excel($config);

$file = $excel->fileName("free.xlsx")
    ->header(['name', 'money']);

for ($index = 0; $index < 10; $index++) {
    $file->insertText($index+1, 0, 'viest');
    $file->insertText($index+1, 1, 10000, '#,##0');
}

$textFile->output();
```

Vtiful\\Kernel\\Excel::mergeCells
=================================

Vtiful\\Kernel\\Excel mergeCells

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::mergeCells</span> ( <span
class="methodparam"><span class="type">string</span> `$scope`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

Merge Cells.

### 参数

`scope`  
cell start and end coordinate strings

`data`  
string data

### 返回值

<span class="classname">Vtiful\\Kernel\\Excel</span> instance

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$excel = new \Vtiful\Kernel\Excel($config);

$excel->fileName("test.xlsx")
        ->mergeCells('A1:C1', 'Merge cells')
        ->output();
```

Vtiful\\Kernel\\Excel::output
=============================

Vtiful\\Kernel\\Excel output

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::output</span> ( <span
class="methodparam">void</span> )

Output xlsx file to disk.

### 参数

此函数没有参数。

### 返回值

XLSX file path;

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$fileObject  = new \Vtiful\Kernel\Excel($config);

$file = $fileObject->fileName('tutorial.xlsx', 'sheet_one')
    ->header(['name', 'age'])
    ->data([
      ['viest', 23],
      ['wjx', 23],
    ]);
    
$path = $file->output();
?>
```

Vtiful\\Kernel\\Excel::setColumn
================================

Vtiful\\Kernel\\Excel setColumn

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::setColumn</span> ( <span
class="methodparam"><span class="type">string</span> `$range`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$format`</span> \] )

Set the format of the column.

### 参数

`range`  
cell start and end coordinate strings

`width`  
column width

`format`  
cell format resource

### 返回值

<span class="classname">Vtiful\\Kernel\\Excel</span> instance

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$excel  = new \Vtiful\Kernel\Excel($config);

$fileObject = $excel->fileName('tutorial01.xlsx');
$fileHandle = $fileObject->getHandle();

$boldStyle = \Vtiful\Kernel\Format::bold($fileHandle);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $boldStyle)
    ->output();
```

Vtiful\\Kernel\\Excel::setRow
=============================

Vtiful\\Kernel\\Excel setRow

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Excel::setRow</span> ( <span
class="methodparam"><span class="type">string</span> `$range`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$format`</span> \] )

Set the format of the column.

### 参数

`range`  
cell start and end coordinate strings

`height`  
row height

`format`  
cell format resource

### 返回值

<span class="classname">Vtiful\\Kernel\\Excel</span> instance

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$excel  = new \Vtiful\Kernel\Excel($config);

$fileObject = $excel->fileName('tutorial01.xlsx');
$fileHandle = $fileObject->getHandle();

$boldStyle = \Vtiful\Kernel\Format::bold($fileHandle);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setRow('A1', 20, $boldStyle,)
    ->output();
```

简介
----

Create a cell format object

类摘要
------

**Vtiful\\Kernel\\Format**

<span class="ooclass"> class **Vtiful\\Kernel\\Format** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::FORMAT_ALIGN_LEFT` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::FORMAT_ALIGN_CENTER` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::FORMAT_ALIGN_RIGHT` <span class="initializer"> =
3</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::FORMAT_ALIGN_FILL` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::FORMAT_ALIGN_JUSTIFY` <span class="initializer">
= 5</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::FORMAT_ALIGN_CENTER_ACROSS` <span
class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::FORMAT_ALIGN_DISTRIBUTED` <span
class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_TOP` <span
class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_BOTTOM` <span
class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_CENTER` <span
class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_JUSTIFY` <span
class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_DISTRIBUTED` <span
class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::UNDERLINE_SINGLE` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::UNDERLINE_DOUBLE` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::UNDERLINE_SINGLE_ACCOUNTING` <span
class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Vtiful\Kernel\Format::UNDERLINE_DOUBLE_ACCOUNTING` <span
class="initializer"> = 4</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">align</span> ( <span class="methodparam"><span
class="type">resource</span> `$handle`</span> , <span
class="methodparam"><span class="type">int</span> `$style`</span> )

<span class="modifier">public</span> <span
class="methodname">bold</span> ( <span class="methodparam"><span
class="type">resource</span> `$handle`</span> )

<span class="modifier">public</span> <span
class="methodname">italic</span> ( <span class="methodparam"><span
class="type">resource</span> `$handle`</span> )

<span class="modifier">public</span> <span
class="methodname">underline</span> ( <span class="methodparam"><span
class="type">resource</span> `$handle`</span> , <span
class="methodparam"><span class="type">int</span> `$style`</span> )

}

预定义常量
----------

**`Vtiful\Kernel\Format::FORMAT_ALIGN_LEFT`**  

**`Vtiful\Kernel\Format::FORMAT_ALIGN_CENTER`**  

**`Vtiful\Kernel\Format::FORMAT_ALIGN_RIGHT`**  

**`Vtiful\Kernel\Format::FORMAT_ALIGN_FILL`**  

**`Vtiful\Kernel\Format::FORMAT_ALIGN_JUSTIFY`**  

**`Vtiful\Kernel\Format::FORMAT_ALIGN_CENTER_ACROSS`**  

**`Vtiful\Kernel\Format::FORMAT_ALIGN_DISTRIBUTED`**  

**`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_TOP`**  

**`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_BOTTOM`**  

**`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_CENTER`**  

**`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_JUSTIFY`**  

**`Vtiful\Kernel\Format::FORMAT_ALIGN_VERTICAL_DISTRIBUTED`**  

**`Vtiful\Kernel\Format::UNDERLINE_SINGLE`**  

**`Vtiful\Kernel\Format::UNDERLINE_DOUBLE`**  

**`Vtiful\Kernel\Format::UNDERLINE_SINGLE_ACCOUNTING`**  

**`Vtiful\Kernel\Format::UNDERLINE_DOUBLE_ACCOUNTING`**  

Vtiful\\Kernel\\Format::align
=============================

Vtiful\\Kernel\\Format align

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Format::align</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
, <span class="methodparam"><span class="type">int</span>
`$style`</span> )

set cell align

### 参数

`handle`  
xlsx file handle

`style`  
<span class="classname">Vtiful\\Kernel\\Format</span> constant

### 返回值

Resource

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$excel  = new \Vtiful\Kernel\Excel($config);

$fileObject = $excel->fileName('tutorial01.xlsx');
$fileHandle = $fileObject->getHandle();

$alignStyle = \Vtiful\Kernel\Format::align($fileHandle, \Vtiful\Kernel\Format::FORMAT_ALIGN_LEFT);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $align)
    ->output();
?>
```

Vtiful\\Kernel\\Format::bold
============================

Vtiful\\Kernel\\Format bold

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Format::bold</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
)

<span class="classname">Vtiful\\Kernel\\Format</span> bold format

### 参数

`handle`  
xlsx file handle

### 返回值

Resource

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$excel  = new \Vtiful\Kernel\Excel($config);

$fileObject = $excel->fileName('tutorial01.xlsx');
$fileHandle = $fileObject->getHandle();

$boldStyle = \Vtiful\Kernel\Format::bold($fileHandle);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $boldStyle)
    ->output();
?>
```

Vtiful\\Kernel\\Format::italic
==============================

Vtiful\\Kernel\\Format italic

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Format::italic</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
)

<span class="classname">Vtiful\\Kernel\\Format</span> italic format

### 参数

`handle`  
xlsx file handle

### 返回值

Resource

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$excel  = new \Vtiful\Kernel\Excel($config);

$fileObject = $excel->fileName('tutorial01.xlsx');
$fileHandle = $fileObject->getHandle();

$italicStyle = \Vtiful\Kernel\Format::italic($fileHandle);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $italicStyle)
    ->output();
?>
```

Vtiful\\Kernel\\Format::underline
=================================

Vtiful\\Kernel\\Format underline

### 说明

<span class="modifier">public</span> <span
class="methodname">Vtiful\\Kernel\\Format::underline</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
, <span class="methodparam"><span class="type">int</span>
`$style`</span> )

<span class="classname">Vtiful\\Kernel\\Format</span> underline format

### 参数

`handle`  
xlsx file handle

`style`  
<span class="classname">Vtiful\\Kernel\\Format</span> constant

### 返回值

Resource

### 范例

**示例 \#1 example**

``` php
<?php
$config = [
    'path' => './tests'
];

$excel  = new \Vtiful\Kernel\Excel($config);

$fileObject = $excel->fileName('tutorial01.xlsx');
$fileHandle = $fileObject->getHandle();

$underlineStyle = \Vtiful\Kernel\Format::underline($fileHandle, \Vtiful\Kernel\Format::UNDERLINE_SINGLE);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $underlineStyle)
    ->output();
?>
```
