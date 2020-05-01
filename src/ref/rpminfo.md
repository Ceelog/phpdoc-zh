rpmaddtag
=========

Add tag retrieved in query

### 说明

<span class="type">bool</span> <span class="methodname">rpmaddtag</span>
( <span class="methodparam"><span class="type">int</span> `$tag`</span>
)

Add an additional retrieved tag in subsequent queries.

### 参数

`tag`  
One of RPMTAG\_\* constant, see the
<a href="/rpminfo/constants.html" class="link">rpminfo constants</a>
page.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">rpminfo</span>
-   <span class="function">rpmdbinfo</span>
-   <span class="function">rpmdbsearch</span>

rpmdbinfo
=========

Get information from installed RPM

### 说明

<span class="type">array</span> <span
class="methodname">rpmdbinfo</span> ( <span class="methodparam"><span
class="type">string</span> `$nevr`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$full`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Retrieve information about an installed package, from the system RPM
database.

### 参数

`nevr`  
Name with optional epoch, version and release.

`full`  
If **`TRUE`** all information headers for the file are retrieved, else
only a minimal set.

### 返回值

An <span class="type">array</span> of <span class="type">array</span> of
information or NULL on error.

### 参见

-   <span class="function">rpmaddtag</span>

### 范例

**示例 \#1 A <span class="function">rpmdbinfo</span> example**

``` php
<?php
rpmaddtag(RPMTAG_INSTALLTIME);
$info = rpmdbinfo("php-pecl-rpminfo");
print_r($info);
?>
```

以上例程会输出：

    Array
    (
        [0] => Array
            (
                [Name] => php-pecl-rpminfo
                [Version] => 0.4.2
                [Release] => 1.fc31
                [Summary] => RPM information
                [Installtime] => 1586244687
                [Arch] => x86_64
            )
    )

rpmdbsearch
===========

Search RPM packages

### 说明

<span class="type">array</span> <span
class="methodname">rpmdbsearch</span> ( <span class="methodparam"><span
class="type">string</span> `$pattern`</span> \[, <span
class="methodparam"><span class="type">int</span> `$rpmtag`<span
class="initializer"> = RPMTAG\_NAME</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$rpmmire`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$full`<span
class="initializer"> = **`FALSE`**</span></span> \]\]\] )

Search packages in the system RPM database.

### 参数

`pattern`  
Value to search for.

`rpmtag`  
Search criterion, one of RPMTAG\_\* constant, see the
<a href="/rpminfo/constants.html" class="link">rpminfo constants</a>
page.

`rpmmire`  
Pattern type, one of RPMMIRE\_\* constant, see the
<a href="/rpminfo/constants.html" class="link">rpminfo constants</a>
page. When \< 0 the criterion must equals the value, and database index
is used if possible.

`full`  
If **`TRUE`** all information headers for the file are retrieved, else
only a minimal set.

### 返回值

An <span class="type">array</span> of <span class="type">array</span> of
information or NULL on error.

### 参见

-   <span class="function">rpmaddtag</span>

### 范例

**示例 \#1 Searching for the package owning a file**

``` php
<?php
$info = rpmdbsearch("/usr/bin/php", RPMTAG_INSTFILENAMES);
print_r($info);
?>
```

以上例程会输出：

    Array
    (
        [0] => Array
            (
                [Name] => php-cli
                [Version] => 7.4.4
                [Release] => 1.fc32
                [Summary] => Command-line interface for PHP
                [Arch] => x86_64
            )

    )

rpminfo
=======

Get information from a RPM file

### 说明

<span class="type">array</span> <span class="methodname">rpminfo</span>
( <span class="methodparam"><span class="type">string</span>
`$path`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$full`<span class="initializer"> =
**`FALSE`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `&$error`</span> \]\] )

Retrieve information about a local file, a RPM package.

### 参数

`path`  
Path of the RPM file.

`full`  
If **`TRUE`** all information headers for the file are retrieved, else
only a minimal set.

`error`  
If provided, will receive the possible error message, and will avoid a
runtime warning.

### 返回值

An <span class="type">array</span> of information or NULL on error.

### 参见

-   <span class="function">rpmaddtag</span>

### 范例

**示例 \#1 A <span class="function">rpminfo</span> example**

``` php
<?php
rpmaddtag(RPMTAG_BUILDTIME);
$info = rpminfo("./php-pecl-rpminfo-0.4.2-1.el8.remi.7.4.x86_64.rpm");
print_r($info);
?>
```

以上例程会输出：

    Array
    (
        [Name] => php-pecl-rpminfo
        [Version] => 0.4.2
        [Release] => 1.el8
        [Summary] => RPM information
        [Buildtime] => 1586244821
        [Arch] => x86_64
    )

rpmvercmp
=========

RPM version comparison

### 说明

<span class="type">int</span> <span class="methodname">rpmvercmp</span>
( <span class="methodparam"><span class="type">string</span>
`$evr1`</span> , <span class="methodparam"><span
class="type">string</span> `$evr2`</span> )

Compare 2 RPM versions.

### 参数

`evr1`  
First epoch:version-release string

`evr2`  
Second epoch:version-release string

### 返回值

Returns \< 0 if evr1 is less than evr2, \> 0 if evr1 is greater than
evr2, and 0 if they are equal.

**目录**

-   [rpmaddtag](/ref/rpminfo.html#rpmaddtag) — Add tag retrieved in
    query
-   [rpmdbinfo](/ref/rpminfo.html#rpmdbinfo) — Get information from
    installed RPM
-   [rpmdbsearch](/ref/rpminfo.html#rpmdbsearch) — Search RPM packages
-   [rpminfo](/ref/rpminfo.html#rpminfo) — Get information from a RPM
    file
-   [rpmvercmp](/ref/rpminfo.html#rpmvercmp) — RPM version comparison
