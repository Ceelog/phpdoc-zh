parsekit\_compile\_file
=======================

Compile a PHP file and return the resulting op array

### 说明

<span class="type">array</span> <span
class="methodname">parsekit\_compile\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">array</span>
`&$errors`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`<span class="initializer"> =
PARSEKIT\_QUIET</span></span> \]\] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担 。

### 参数

`filename`  
A string containing the name of the file to compile. Similar to the
argument to <span class="function">include</span>.

`errors`  
A 2D hash of errors (including fatal errors) encountered during
compilation. Returned by reference.

`options`  
One of either **`PARSEKIT_QUIET`** or **`PARSEKIT_SIMPLE`**. To produce
varying degrees of verbosity in the returned output.

### 返回值

Returns a complex multi-layer array structure as detailed below.

### 范例

**示例 \#1 <span class="function">parsekit\_compile\_file</span>
example**

``` php
<?php
var_dump(parsekit_compile_file('hello_world.php', $errors, PARSEKIT_SIMPLE));
?>
```

以上例程会输出：

    array(5) {
      [0]=>
      string(37) "ZEND_ECHO UNUSED 'Hello World' UNUSED"
      [1]=>
      string(30) "ZEND_RETURN UNUSED NULL UNUSED"
      [2]=>
      string(42) "ZEND_HANDLE_EXCEPTION UNUSED UNUSED UNUSED"
      ["function_table"]=>
      NULL
      ["class_table"]=>
      NULL
    }

### 参见

-   <span class="function">parsekit\_compile\_string</span>

parsekit\_compile\_string
=========================

Compile a string of PHP code and return the resulting op array

### 说明

<span class="type">array</span> <span
class="methodname">parsekit\_compile\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$phpcode`</span>
\[, <span class="methodparam"><span class="type">array</span>
`&$errors`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`<span class="initializer"> =
PARSEKIT\_QUIET</span></span> \]\] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担 。

### 参数

`phpcode`  
A string containing phpcode. Similar to the argument to <span
class="function">eval</span>.

`errors`  
A 2D hash of errors (including fatal errors) encountered during
compilation. Returned by reference.

`options`  
One of either **`PARSEKIT_QUIET`** or **`PARSEKIT_SIMPLE`**. To produce
varying degrees of verbosity in the returned output.

### 返回值

Returns a complex multi-layer array structure as detailed below.

### 范例

**示例 \#1 <span class="function">parsekit\_compile\_string</span>
example**

``` php
<?php
  $ops = parsekit_compile_string('
echo "Foo\n";
', $errors, PARSEKIT_QUIET);

  var_dump($ops);
?>
```

以上例程会输出：

    array(20) {
      ["type"]=>
      int(4)
      ["type_name"]=>
      string(14) "ZEND_EVAL_CODE"
      ["fn_flags"]=>
      int(0)
      ["num_args"]=>
      int(0)
      ["required_num_args"]=>
      int(0)
      ["pass_rest_by_reference"]=>
      bool(false)
      ["uses_this"]=>
      bool(false)
      ["line_start"]=>
      int(0)
      ["line_end"]=>
      int(0)
      ["return_reference"]=>
      bool(false)
      ["refcount"]=>
      int(1)
      ["last"]=>
      int(3)
      ["size"]=>
      int(3)
      ["T"]=>
      int(0)
      ["last_brk_cont"]=>
      int(0)
      ["current_brk_cont"]=>
      int(-1)
      ["backpatch_count"]=>
      int(0)
      ["done_pass_two"]=>
      bool(true)
      ["filename"]=>
      string(17) "Parsekit Compiler"
      ["opcodes"]=>
      array(3) {
        [8594800]=>
        array(5) {
          ["opcode"]=>
          int(40)
          ["opcode_name"]=>
          string(9) "ZEND_ECHO"
          ["flags"]=>
          int(768)
          ["op1"]=>
          array(3) {
            ["type"]=>
            int(1)
            ["type_name"]=>
            string(8) "IS_CONST"
            ["constant"]=>
            &string(4) "Foo
    "
          }
          ["lineno"]=>
          int(2)
        }
        ["859484C"]=>
        array(6) {
          ["opcode"]=>
          int(62)
          ["opcode_name"]=>
          string(11) "ZEND_RETURN"
          ["flags"]=>
          int(16777984)
          ["op1"]=>
          array(3) {
            ["type"]=>
            int(1)
            ["type_name"]=>
            string(8) "IS_CONST"
            ["constant"]=>
            &NULL
          }
          ["extended_value"]=>
          int(0)
          ["lineno"]=>
          int(3)
        }
        [8594898]=>
        array(4) {
          ["opcode"]=>
          int(149)
          ["opcode_name"]=>
          string(21) "ZEND_HANDLE_EXCEPTION"
          ["flags"]=>
          int(0)
          ["lineno"]=>
          int(3)
        }
      }
    }

### 参见

-   <span class="function">parsekit\_compile\_file</span>

parsekit\_func\_arginfo
=======================

Return information regarding function argument(s)

### 说明

<span class="type">array</span> <span
class="methodname">parsekit\_func\_arginfo</span> ( <span
class="methodparam"><span class="type">mixed</span> `$function`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担 。

### 参数

`function`  
A string describing a function, or an array describing a class/method.

### 返回值

Returns an array containing argument information.

### 范例

**示例 \#1 <span class="function">parsekit\_func\_arginfo</span>
example**

``` php
<?php
function foo($bar, stdClass $baz, &$bomb, $bling = false) {
}

var_dump(parsekit_func_arginfo('foo'));
?>
```

以上例程会输出：

    array(4) {
      [0]=>
      array(3) {
        ["name"]=>
        string(3) "bar"
        ["allow_null"]=>
        bool(true)
        ["pass_by_reference"]=>
        bool(false)
      }
      [1]=>
      array(4) {
        ["name"]=>
        string(3) "baz"
        ["class_name"]=>
        string(8) "stdClass"
        ["allow_null"]=>
        bool(false)
        ["pass_by_reference"]=>
        bool(false)
      }
      [2]=>
      array(3) {
        ["name"]=>
        string(4) "bomb"
        ["allow_null"]=>
        bool(true)
        ["pass_by_reference"]=>
        bool(true)
      }
      [3]=>
      array(3) {
        ["name"]=>
        string(5) "bling"
        ["allow_null"]=>
        bool(true)
        ["pass_by_reference"]=>
        bool(false)
      }
    }

**目录**

-   [parsekit\_compile\_file](/ref/parsekit.html#parsekit_compile_file)
    — Compile a PHP file and return the resulting op array
-   [parsekit\_compile\_string](/ref/parsekit.html#parsekit_compile_string)
    — Compile a string of PHP code and return the resulting op array
-   [parsekit\_func\_arginfo](/ref/parsekit.html#parsekit_func_arginfo)
    — Return information regarding function argument(s)
