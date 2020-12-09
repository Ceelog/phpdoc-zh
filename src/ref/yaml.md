yaml\_emit\_file
================

Send the YAML representation of a value to a file

### 说明

<span class="type">bool</span> <span
class="methodname">yaml\_emit\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$data`</span> \[, <span class="methodparam"><span
class="type">int</span> `$encoding`<span class="initializer"> =
YAML\_ANY\_ENCODING</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$linebreak`<span class="initializer"> =
YAML\_ANY\_BREAK</span></span> \[, <span class="methodparam"><span
class="type">array</span> `$callbacks`<span class="initializer"> =
**`null`**</span></span> \]\]\] )

Generate a YAML representation of the provided `data` in the `filename`.

### 参数

`filename`  
Path to the file.

`data`  
The `data` being encoded. Can be any type except a <span
class="type">resource</span>.

`encoding`  
Output character encoding chosen from **`YAML_ANY_ENCODING`**,
**`YAML_UTF8_ENCODING`**, **`YAML_UTF16LE_ENCODING`**,
**`YAML_UTF16BE_ENCODING`**.

`linebreak`  
Output linebreak style chosen from **`YAML_ANY_BREAK`**,
**`YAML_CR_BREAK`**, **`YAML_LN_BREAK`**, **`YAML_CRLN_BREAK`**.

`callbacks`  
Content handlers for emitting YAML nodes. Associative <span
class="type">array</span> of classname =\> <span
class="type">callable</span> mappings. See
<a href="/yaml/callbacks.html#Emit%20callbacks" class="link">emit callbacks</a>
for more details.

### 返回值

Returns **`true`** on success.

### 更新日志

| 版本            | 说明                                 |
|-----------------|--------------------------------------|
| PECL yaml 1.1.0 | The `callbacks` parameter was added. |

### 参见

-   <span class="function">yaml\_emit</span>
-   <span class="function">yaml\_parse</span>

yaml\_emit
==========

Returns the YAML representation of a value

### 说明

<span class="type">string</span> <span
class="methodname">yaml\_emit</span> ( <span class="methodparam"><span
class="type">mixed</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$encoding`<span
class="initializer"> = YAML\_ANY\_ENCODING</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$linebreak`<span
class="initializer"> = YAML\_ANY\_BREAK</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$callbacks`<span
class="initializer"> = **`null`**</span></span> \]\]\] )

Generate a YAML representation of the provided `data`.

### 参数

`data`  
The `data` being encoded. Can be any type except a <span
class="type">resource</span>.

`encoding`  
Output character encoding chosen from **`YAML_ANY_ENCODING`**,
**`YAML_UTF8_ENCODING`**, **`YAML_UTF16LE_ENCODING`**,
**`YAML_UTF16BE_ENCODING`**.

`linebreak`  
Output linebreak style chosen from **`YAML_ANY_BREAK`**,
**`YAML_CR_BREAK`**, **`YAML_LN_BREAK`**, **`YAML_CRLN_BREAK`**.

`callbacks`  
Content handlers for emitting YAML nodes. Associative <span
class="type">array</span> of classname =\> <span
class="type">callable</span> mappings. See
<a href="/yaml/callbacks.html#Emit%20callbacks" class="link">emit callbacks</a>
for more details.

### 返回值

Returns a YAML encoded <span class="type">string</span> on success.

### 更新日志

| 版本            | 说明                                 |
|-----------------|--------------------------------------|
| PECL yaml 1.1.0 | The `callbacks` parameter was added. |

### 范例

**示例 \#1 <span class="function">yaml\_emit</span> example**

``` php
<?php
$addr = array(
    "given" => "Chris",
    "family"=> "Dumars",
    "address"=> array(
        "lines"=> "458 Walkman Dr.
        Suite #292",
        "city"=> "Royal Oak",
        "state"=> "MI",
        "postal"=> 48046,
      ),
  );
$invoice = array (
    "invoice"=> 34843,
    "date"=> 980208000,
    "bill-to"=> $addr,
    "ship-to"=> $addr,
    "product"=> array(
        array(
            "sku"=> "BL394D",
            "quantity"=> 4,
            "description"=> "Basketball",
            "price"=> 450,
          ),
        array(
            "sku"=> "BL4438H",
            "quantity"=> 1,
            "description"=> "Super Hoop",
            "price"=> 2392,
          ),
      ),
    "tax"=> 251.42,
    "total"=> 4443.52,
    "comments"=> "Late afternoon is best. Backup contact is Nancy Billsmer @ 338-4338.",
  );
var_dump(yaml_emit($invoice));
?>
```

以上例程的输出类似于：

    string(628) "---
    invoice: 34843
    date: 980208000
    bill-to:
      given: Chris
      family: Dumars
      address:
        lines: |-
          458 Walkman Dr.
                  Suite #292
        city: Royal Oak
        state: MI
        postal: 48046
    ship-to:
      given: Chris
      family: Dumars
      address:
        lines: |-
          458 Walkman Dr.
                  Suite #292
        city: Royal Oak
        state: MI
        postal: 48046
    product:
    - sku: BL394D
      quantity: 4
      description: Basketball
      price: 450
    - sku: BL4438H
      quantity: 1
      description: Super Hoop
      price: 2392
    tax: 251.420000
    total: 4443.520000
    comments: Late afternoon is best. Backup contact is Nancy Billsmer @ 338-4338.
    ...
    "

### 参见

-   <span class="function">yaml\_emit\_file</span>
-   <span class="function">yaml\_parse</span>

yaml\_parse\_file
=================

Parse a YAML stream from a file

### 说明

<span class="type">mixed</span> <span
class="methodname">yaml\_parse\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span> `$pos`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `&$ndocs`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$callbacks`<span class="initializer"> = **`null`**</span></span> \]\]\]
)

Convert all or part of a YAML document stream read from a file to a PHP
variable.

### 参数

`filename`  
Path to the file.

`pos`  
Document to extract from stream (*-1* for all documents, *0* for first
document, ...).

`ndocs`  
If `ndocs` is provided, then it is filled with the number of documents
found in stream.

`callbacks`  
Content handlers for YAML nodes. Associative <span
class="type">array</span> of YAML tag =\> <span
class="type">callable</span> mappings. See
<a href="/yaml/callbacks.html#Parse%20callbacks" class="link">parse callbacks</a>
for more details.

### 返回值

Returns the value encoded in `input` in appropriate PHP type
或者在失败时返回 **`false`**. If `pos` is *-1* an <span
class="type">array</span> will be returned with one entry for each
document found in the stream.

### 注释

**Warning**

Processing untrusted user input with <span
class="function">yaml\_parse\_file</span> is dangerous if the use of
<span class="function">unserialize</span> is enabled for nodes using the
*!php/object* tag. This behavior can be disabled by using the
*yaml.decode\_php* ini setting.

### 参见

-   <span class="function">yaml\_parse</span>
-   <span class="function">yaml\_parse\_url</span>
-   <span class="function">yaml\_emit</span>

yaml\_parse\_url
================

Parse a Yaml stream from a URL

### 说明

<span class="type">mixed</span> <span
class="methodname">yaml\_parse\_url</span> ( <span
class="methodparam"><span class="type">string</span> `$url`</span> \[,
<span class="methodparam"><span class="type">int</span> `$pos`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `&$ndocs`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$callbacks`<span class="initializer"> = **`null`**</span></span> \]\]\]
)

Convert all or part of a YAML document stream read from a URL to a PHP
variable.

### 参数

`url`  
`url` should be of the form "scheme://...". PHP will search for a
protocol handler (also known as a wrapper) for that scheme. If no
wrappers for that protocol are registered, PHP will emit a notice to
help you track potential problems in your script and then continue as
though filename specifies a regular file.

`pos`  
Document to extract from stream (*-1* for all documents, *0* for first
document, ...).

`ndocs`  
If `ndocs` is provided, then it is filled with the number of documents
found in stream.

`callbacks`  
Content handlers for YAML nodes. Associative <span
class="type">array</span> of YAML tag =\> <span
class="type">callable</span> mappings. See
<a href="/yaml/callbacks.html#Parse%20callbacks" class="link">parse callbacks</a>
for more

### 返回值

Returns the value encoded in `input` in appropriate PHP type
或者在失败时返回 **`false`**. If `pos` is *-1* an <span
class="type">array</span> will be returned with one entry for each
document found in the stream.

### 注释

**Warning**

Processing untrusted user input with <span
class="function">yaml\_parse\_url</span> is dangerous if the use of
<span class="function">unserialize</span> is enabled for nodes using the
*!php/object* tag. This behavior can be disabled by using the
*yaml.decode\_php* ini setting.

### 参见

-   <span class="function">yaml\_parse</span>
-   <span class="function">yaml\_parse\_file</span>
-   <span class="function">yaml\_emit</span>

yaml\_parse
===========

Parse a YAML stream

### 说明

<span class="type">mixed</span> <span
class="methodname">yaml\_parse</span> ( <span class="methodparam"><span
class="type">string</span> `$input`</span> \[, <span
class="methodparam"><span class="type">int</span> `$pos`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `&$ndocs`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$callbacks`<span class="initializer"> = **`null`**</span></span> \]\]\]
)

Convert all or part of a YAML document stream to a PHP variable.

### 参数

`input`  
The <span class="type">string</span> to parse as a YAML document stream.

`pos`  
Document to extract from stream (*-1* for all documents, *0* for first
document, ...).

`ndocs`  
If `ndocs` is provided, then it is filled with the number of documents
found in stream.

`callbacks`  
Content handlers for YAML nodes. Associative <span
class="type">array</span> of YAML tag =\> <span
class="type">callable</span> mappings. See
<a href="/yaml/callbacks.html#Parse%20callbacks" class="link">parse callbacks</a>
for more details.

### 返回值

Returns the value encoded in `input` in appropriate PHP type
或者在失败时返回 **`false`**. If `pos` is *-1* an <span
class="type">array</span> will be returned with one entry for each
document found in the stream.

### 范例

**示例 \#1 <span class="function">yaml\_parse</span> example**

``` php
<?php
$yaml = <<<EOD
---
invoice: 34843
date: "2001-01-23"
bill-to: &id001
  given: Chris
  family: Dumars
  address:
    lines: |-
      458 Walkman Dr.
              Suite #292
    city: Royal Oak
    state: MI
    postal: 48046
ship-to: *id001
product:
- sku: BL394D
  quantity: 4
  description: Basketball
  price: 450
- sku: BL4438H
  quantity: 1
  description: Super Hoop
  price: 2392
tax: 251.420000
total: 4443.520000
comments: Late afternoon is best. Backup contact is Nancy Billsmer @ 338-4338.
...
EOD;

$parsed = yaml_parse($yaml);
var_dump($parsed);
?>
```

以上例程的输出类似于：

    array(8) {
      ["invoice"]=>
      int(34843)
      ["date"]=>
      string(10) "2001-01-23"
      ["bill-to"]=>
      &array(3) {
        ["given"]=>
        string(5) "Chris"
        ["family"]=>
        string(6) "Dumars"
        ["address"]=>
        array(4) {
          ["lines"]=>
          string(34) "458 Walkman Dr.
            Suite #292"
          ["city"]=>
          string(9) "Royal Oak"
          ["state"]=>
          string(2) "MI"
          ["postal"]=>
          int(48046)
        }
      }
      ["ship-to"]=>
      &array(3) {
        ["given"]=>
        string(5) "Chris"
        ["family"]=>
        string(6) "Dumars"
        ["address"]=>
        array(4) {
          ["lines"]=>
          string(34) "458 Walkman Dr.
            Suite #292"
          ["city"]=>
          string(9) "Royal Oak"
          ["state"]=>
          string(2) "MI"
          ["postal"]=>
          int(48046)
        }
      }
      ["product"]=>
      array(2) {
        [0]=>
        array(4) {
          ["sku"]=>
          string(6) "BL394D"
          ["quantity"]=>
          int(4)
          ["description"]=>
          string(10) "Basketball"
          ["price"]=>
          int(450)
        }
        [1]=>
        array(4) {
          ["sku"]=>
          string(7) "BL4438H"
          ["quantity"]=>
          int(1)
          ["description"]=>
          string(10) "Super Hoop"
          ["price"]=>
          int(2392)
        }
      }
      ["tax"]=>
      float(251.42)
      ["total"]=>
      float(4443.52)
      ["comments"]=>
      string(68) "Late afternoon is best. Backup contact is Nancy Billsmer @ 338-4338."
    }

### 注释

**Warning**

Processing untrusted user input with <span
class="function">yaml\_parse</span> is dangerous if the use of <span
class="function">unserialize</span> is enabled for nodes using the
*!php/object* tag. This behavior can be disabled by using the
*yaml.decode\_php* ini setting.

### 参见

-   <span class="function">yaml\_parse\_file</span>
-   <span class="function">yaml\_parse\_url</span>
-   <span class="function">yaml\_emit</span>

**目录**

-   [yaml\_emit\_file](/ref/yaml.html#yaml_emit_file) — Send the YAML
    representation of a value to a file
-   [yaml\_emit](/ref/yaml.html#yaml_emit) — Returns the YAML
    representation of a value
-   [yaml\_parse\_file](/ref/yaml.html#yaml_parse_file) — Parse a YAML
    stream from a file
-   [yaml\_parse\_url](/ref/yaml.html#yaml_parse_url) — Parse a Yaml
    stream from a URL
-   [yaml\_parse](/ref/yaml.html#yaml_parse) — Parse a YAML stream
