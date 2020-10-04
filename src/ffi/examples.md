范例
====

**目录**

-   [Basic FFI usage](/ffi/examples.html#Basic%20FFI%20usage)
-   [PHP Callbacks](/ffi/examples.html#PHP%20Callbacks)
-   [A Complete PHP/FFI/preloading
    Example](/ffi/examples.html#A%20Complete%20PHP/FFI/preloading%20Example)

Basic FFI usage
---------------

Before diving into the details of the FFI API, lets take a look at a few
examples demonstrating the simplicity of the FFI API usage for regular
tasks.

> **Note**:
>
> Some of these examples require `libc.so.6` and as such will not work
> on systems where it is not available.

**示例 \#1 Calling a function from shared library**

``` php
<?php
// create FFI object, loading libc and exporting function printf()
$ffi = FFI::cdef(
    "int printf(const char *format, ...);", // this is a regular C declaration
    "libc.so.6");
// call C's printf()
$ffi->printf("Hello %s!\n", "world");
?>
```

以上例程会输出：

    Hello world!

> **Note**:
>
> Note that some C functions need specific calling conventions, e.g.
> *\_\_fastcall*, *\_\_stdcall* or *,\_\_vectorcall*.

**示例 \#2 Calling a function, returning a structure through an
argument**

``` php
<?php
// create gettimeofday() binding
$ffi = FFI::cdef("
    typedef unsigned int time_t;
    typedef unsigned int suseconds_t;
 
    struct timeval {
        time_t      tv_sec;
        suseconds_t tv_usec;
    };
 
    struct timezone {
        int tz_minuteswest;
        int tz_dsttime;
    };
 
    int gettimeofday(struct timeval *tv, struct timezone *tz);    
", "libc.so.6");
// create C data structures
$tv = $ffi->new("struct timeval");
$tz = $ffi->new("struct timezone");
// call C's gettimeofday()
var_dump($ffi->gettimeofday(FFI::addr($tv), FFI::addr($tz)));
// access field of C data structure
var_dump($tv->tv_sec);
// print the whole C data structure
var_dump($tz);
?>
```

以上例程的输出类似于：

    int(0)
    int(1555946835)
    object(FFI\CData:struct timezone)#3 (2) {
      ["tz_minuteswest"]=>
      int(0)
      ["tz_dsttime"]=>
      int(0)
    }

**示例 \#3 Accessing existing C variables**

``` php
<?php
// create FFI object, loading libc and exporting errno variable
$ffi = FFI::cdef(
    "int errno;", // this is a regular C declaration
    "libc.so.6");
// print C's errno
var_dump($ffi->errno);
?>
```

以上例程会输出：

    int(0)

**示例 \#4 Creating and Modifying C variables**

``` php
<?php
// create a new C int variable
$x = FFI::new("int");
var_dump($x->cdata);

// simple assignment
$x->cdata = 5;
var_dump($x->cdata);

// compound assignment
$x->cdata += 2;
var_dump($x->cdata);
?>
```

以上例程会输出：

    int(0)
    int(5)
    int(7)

**示例 \#5 Working with C arrays**

``` php
<?php
// create C data structure
$a = FFI::new("long[1024]");
// work with it like with a regular PHP array
for ($i = 0; $i < count($a); $i++) {
    $a[$i] = $i;
}
var_dump($a[25]);
$sum = 0;
foreach ($a as $n) {
    $sum += $n;
}
var_dump($sum);
var_dump(count($a));
var_dump(FFI::sizeof($a));
?>
```

以上例程会输出：

    int(25)
    int(523776)
    int(1024)
    int(8192)

**示例 \#6 Working with C enums**

``` php
<?php
$a = FFI::cdef('typedef enum _zend_ffi_symbol_kind {
    ZEND_FFI_SYM_TYPE,
    ZEND_FFI_SYM_CONST = 2,
    ZEND_FFI_SYM_VAR,
    ZEND_FFI_SYM_FUNC
} zend_ffi_symbol_kind;
');
var_dump($a->ZEND_FFI_SYM_TYPE);
var_dump($a->ZEND_FFI_SYM_CONST);
var_dump($a->ZEND_FFI_SYM_VAR);
?>
```

以上例程会输出：

    int(0)
    int(2)
    int(3)

PHP Callbacks
-------------

It is possible to assign a PHP closure to a native variable of function
pointer type or to pass it as a function argument:

``` php
<?php
$zend = FFI::cdef("
    typedef int (*zend_write_func_t)(const char *str, size_t str_length);
    extern zend_write_func_t zend_write;
");
 
echo "Hello World 1!\n";
 
$orig_zend_write = clone $zend->zend_write;
$zend->zend_write = function($str, $len) {
    global $orig_zend_write;
    $orig_zend_write("{\n\t", 3);
    $ret = $orig_zend_write($str, $len);
    $orig_zend_write("}\n", 2);
    return $ret;
};
echo "Hello World 2!\n";
$zend->zend_write = $orig_zend_write;
echo "Hello World 3!\n";
?>
```

以上例程会输出：

    Hello World 1!
    {
            Hello World 2!
    }
    Hello World 3!

Although this works, this functionality is not supported on all libffi
platforms, is not efficient and leaks resources by the end of request.

**小贴士**

It is therefore recommended to minimize the usage of PHP callbacks.

A Complete PHP/FFI/preloading Example
-------------------------------------

`php.ini`

``` ini
ffi.enable=preload
opcache.preload=preload.php
```

`preload.php`

``` php
<?php
FFI::load(__DIR__ . "/dummy.h");
opcache_compile_file(__DIR__ . "/dummy.php");
?>
```

`dummy.h`

``` c
#define FFI_SCOPE "DUMMY"
#define FFI_LIB "libc.so.6"
 
int printf(const char *format, ...);
```

`dummy.php`

``` php
<?php
final class Dummy {
    private static $ffi = null;
    function __construct() {
        if (is_null(self::$ffi)) {
            self::$ffi = FFI::scope("DUMMY");
        }
    }
    function printf($format, ...$args) {
       return (int)self::$ffi->printf($format, ...$args);
    }
}
?>
```

`test.php`

``` php
<?php
$d = new Dummy();
$d->printf("Hello %s!\n", "world");
?>
```
