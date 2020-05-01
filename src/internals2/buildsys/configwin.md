使用 Windows 构建系统：config.w32
---------------------------------

扩展的 `config.w32` 文件的用法与 `config.m4`
文件类似，但有两点决定性的不同：首先，它是用于 Windows
构建的，其次，它是使用 JavaScript 编写的。此章节不会包括 JavaScript
语法。目前，代替 Win32 试验台的这部分是不完整的，仅为例子提供的范例
`config.m4` 的仅试验性质的移植。

**示例 \#1 config.w32 文件举例**

``` javascript
// $Id$
// vim:ft=javascript
```

``` javascript
ARG_WITH("example", "for example support", "no");
ARG_ENABLE("example-debug", "for debugging support in example", "no")
ARG_WITH("example-extra", "for extra functionality in example", "no")
if (PHP_EXAMPLE != "no") {
    if (CHECK_LIB("libexample.lib", "example", PHP_EXAMPLE) &&
        CHECK_HEADER_ADD_INCLUDE("example.h", "CFLAGS_EXAMPLE", PHP_EXAMPLE + "\\include")) {
        
        if (PHP_EXAMPLE_DEBUG != "no") {
            AC_DEFINE('USE_EXAMPLE_DEBUG', 1, 'Debug support in example');
        }
        
        if (PHP_EXAMPLE_EXTRA != "no" &&
            CHECK_LIB("libexample-extra.lib", "example", PHP_EXAMPLE) &&
            CHECK_HEADER_ADD_INCLUDE("example-extra.h", "CFLAGS_EXAMPLE", PHP_EXAMPLE + ";" + PHP_PHP_BUILD + "\\include") {
            AC_DEFINE('HAVE_EXAMPLEEXTRA', 1, 'Extra functionality in example');
            HAVE_EXTRA = 1;
        } else {
            WARNING( "extra example functionality not enabled, lib not found" );
        }
        
        EXTENSION("example", "example.c");
        if (HAVE_EXTRA == 1) {
            ADD_SOURCES("example-extra.c");
        }
    } else {
        WARNING( "example not enabled; libraries not found" );
    }
}
```

### counter 扩展的 config.w32 文件

因为不使用很多构建系统的特性，以前所记载的 counter
扩展有一个比上面所描述的例子更简单的 `config.w32` 文件。

**示例 \#2 counter's config.w32 file**

``` autoconf
// $Id$
// vim:ft=javascript
```

``` autoconf
ARG_ENABLE("counter", "for counter support", "no");
if (PHP_COUNTER != "no") {
    EXTENSION("counter", "counter.c");
    ADD_SOURCE("counter-util.c");
}
```
