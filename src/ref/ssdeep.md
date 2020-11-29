ssdeep\_fuzzy\_compare
======================

Calculates the match score between two fuzzy hash signatures

### 说明

<span class="type">int</span> <span
class="methodname">ssdeep\_fuzzy\_compare</span> ( <span
class="methodparam"><span class="type">string</span>
`$signature1`</span> , <span class="methodparam"><span
class="type">string</span> `$signature2`</span> )

Calculates the match score between `signature1` and `signature2` using
<a href="http://dfrws.org/2006/proceedings/12-Kornblum.pdf" class="link external">»  context-triggered piecewise hashing</a>,
and returns the match score.

### 参数

`signature1`  
The first fuzzy hash signature string.

`signature2`  
The second fuzzy hash signature string.

### 返回值

Returns an integer from 0 to 100 on success, **`FALSE`** otherwise.

ssdeep\_fuzzy\_hash\_filename
=============================

Create a fuzzy hash from a file

### 说明

<span class="type">string</span> <span
class="methodname">ssdeep\_fuzzy\_hash\_filename</span> ( <span
class="methodparam"><span class="type">string</span> `$file_name`</span>
)

<span class="function">ssdeep\_fuzzy\_hash\_filename</span> calculates
the hash of the file specified by `file_name` using
<a href="http://dfrws.org/2006/proceedings/12-Kornblum.pdf" class="link external">» context-triggered piecewise hashing</a>,
and returns that hash.

### 参数

`file_name`  
The filename of the file to hash.

### 返回值

Returns a string on success, **`FALSE`** otherwise.

ssdeep\_fuzzy\_hash
===================

Create a fuzzy hash from a string

### 说明

<span class="type">string</span> <span
class="methodname">ssdeep\_fuzzy\_hash</span> ( <span
class="methodparam"><span class="type">string</span> `$to_hash`</span> )

<span class="function">ssdeep\_fuzzy\_hash</span> calculates the hash of
`to_hash` using
<a href="http://dfrws.org/2006/proceedings/12-Kornblum.pdf" class="link external">»  context-triggered piecewise hashing</a>,
and returns that hash.

### 参数

`to_hash`  
The input string.

### 返回值

Returns a string on success, **`FALSE`** otherwise.

**目录**

-   [ssdeep\_fuzzy\_compare](/ref/ssdeep.html#ssdeep_fuzzy_compare) —
    Calculates the match score between two fuzzy hash signatures
-   [ssdeep\_fuzzy\_hash\_filename](/ref/ssdeep.html#ssdeep_fuzzy_hash_filename)
    — Create a fuzzy hash from a file
-   [ssdeep\_fuzzy\_hash](/ref/ssdeep.html#ssdeep_fuzzy_hash) — Create a
    fuzzy hash from a string
