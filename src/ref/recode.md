recode\_file
============

Recode from file to file according to recode request

### 说明

<span class="type">bool</span> <span
class="methodname">recode\_file</span> ( <span class="methodparam"><span
class="type">string</span> `$request`</span> , <span
class="methodparam"><span class="type">resource</span> `$input`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$output`</span> )

Recode the file referenced by file handle `input` into the file
referenced by file handle `output` according to the recode `request`.

### 参数

`request`  
The desired recode request type

`input`  
A local file handle <span class="type">resource</span> for the `input`

`output`  
A local file handle <span class="type">resource</span> for the `output`

### 返回值

Returns **`false`**, if unable to comply, **`true`** otherwise.

### 范例

**示例 \#1 Basic <span class="function">recode\_file</span> example**

``` php
<?php
$input = fopen('input.txt', 'r');
$output = fopen('output.txt', 'w');
recode_file("us..flat", $input, $output);
?>
```

### 注释

This function does not currently process file handles referencing remote
files (URLs). Both file handles must refer to local files.

### 参见

-   <span class="function">fopen</span>

recode\_string
==============

Recode a string according to a recode request

### 说明

<span class="type">string</span> <span
class="methodname">recode\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$request`</span> ,
<span class="methodparam"><span class="type">string</span>
`$string`</span> )

Recode the string `string` according to the recode request `request`.

### 参数

`request`  
The desired recode request type

`string`  
The <span class="type">string</span> to be recoded

### 返回值

Returns the recoded <span class="type">string</span> or **`false`**, if
unable to perform the recode request.

### 范例

**示例 \#1 Basic <span class="function">recode\_string</span> example**

``` php
<?php
echo recode_string("us..flat", "The following character has a diacritical mark: á");
?>
```

### 注释

A simple recode request may be "lat1..iso646-de".

### 参见

-   The GNU Recode documentation of your installation for detailed
    instructions about recode requests.

recode
======

别名 <span class="function">recode\_string</span>

### 说明

此函数是该函数的别名： <span class="function">recode\_string</span>.

**目录**

-   [recode\_file](/ref/recode.html#recode_file) — Recode from file to
    file according to recode request
-   [recode\_string](/ref/recode.html#recode_string) — Recode a string
    according to a recode request
-   [recode](/ref/recode.html#recode) — 别名 recode\_string
