lzf\_compress
=============

LZF compression

### 说明

<span class="type">string</span> <span
class="methodname">lzf\_compress</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="function">lzf\_compress</span> compresses the given `data`
string using LZF encoding.

### 参数

`data`  
The string to compress.

### 返回值

Returns the compressed data or **`false`** if an error occurred.

### 参见

-   <span class="function">lzf\_decompress</span>

lzf\_decompress
===============

LZF decompression

### 说明

<span class="type">string</span> <span
class="methodname">lzf\_decompress</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="function">lzf\_compress</span> decompresses the given
`data` string containing lzf encoded data.

### 参数

`data`  
The compressed string.

### 返回值

Returns the decompressed data or **`false`** if an error occurred.

### 参见

-   <span class="function">lzf\_compress</span>

lzf\_optimized\_for
===================

Determines what LZF extension was optimized for

### 说明

<span class="type">int</span> <span
class="methodname">lzf\_optimized\_for</span> ( <span
class="methodparam">void</span> )

Determines what was LZF extension optimized for during compilation.

### 返回值

Returns 1 if LZF was optimized for speed, 0 for compression.

**目录**

-   [lzf\_compress](/ref/lzf.html#lzf_compress) — LZF compression
-   [lzf\_decompress](/ref/lzf.html#lzf_decompress) — LZF decompression
-   [lzf\_optimized\_for](/ref/lzf.html#lzf_optimized_for) — Determines
    what LZF extension was optimized for
