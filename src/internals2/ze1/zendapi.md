Zend API：深入 PHP 内核
-----------------------

### Introduction

知者不言。

言者不知。

有时，看起来简单的PHP并不够用。尽管不够用的情况对普通的程序员很少见，而专业的程序员很快就能将PHP带到它的边界(瓶颈)，从性能或功能方面看。新的功能不是生来就能被实现，是因为程序语言固有的限制和复杂，当不得不附添加巨大的默认代码库到每个简单脚本上时，就会出现这些限制和麻烦，于是需要寻找另一种方式来克服PHP这些终极缺陷。

基于上述说法，是时候接触PHP的心脏并看看它的核心了，即让PHP运行的C代码。

**Warning**

这些信息现在已经过时，且其中一部分仅适用于在PHP
4早期版本中用到的ZendEngine 1.0 API。

更多新的信息能在PHP源码的各种README文件和Zend网站中的<a href="http://devzone.zend.com/public/view/tag/Extension" class="link external">» Internals</a>章节找到。

### 概述

”扩展PHP“说起来容易做起来难。PHP已经进化成一个日趋成熟的源码包几十兆大小的工具。要骇客如此复杂的一个系统，不得不学习和思考。构建本章内容时，我们最终选择了“在实战中学习”的方式。这不是最科学也不是最专业的方式，但是此方式最有趣，也得出了最好的最终结果。下面的部分，你将先快速的学习到，如何获得最基本的扩展，且这些扩展立即就可运行。然后你将学习到
Zend 的高级 API 功能，这种方式将不得不试图说明（ZEND
API相关的）功能，设计，建议，技巧等等。以一言蔽之，在任何实战之前这样提供一个大框架的通览。尽管这是“较好”的方法，且没有垃圾hacks生成，但是这种学习方式很难并且费力又费时，这就是我们决定采用“在实战中学习”方式的原因。

注意到尽管本章内容试图尽可能多的说明PHP内部工作机制的知识，但是不可能真正给出任何情况任何时候都可用的PHP扩展的完全指导。因为PHP包是如此庞大复杂，以致你通过实战来使自己学习时,对它的内部工作机制仅仅可达到理解的程度。所以我们鼓励你跟着源码一起学习。

#### 什么是 Zend ? 什么是 PHP ?

*Zend*是语言引擎，PHP内核。PHP是从外层展现的完整系统。咋一听似乎有点模糊不清，但是其实并不复杂(
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.fig.internal-struct" class="link">看下面</a>).为了实现一个
web 脚本解释器，你需要三个部分：

1.  第一：*解释器*部分分析输入代码，翻译代码，然后执行代码。

2.  第二：*功能*部分 完成语言的功能（函数，等等）。

3.  第三：*接口*部分与web通信，等等。

Zend完全参与第一部分，部分参与第二部分；PHP参与第二部分和三部分.他们一起构成完整的PHP包。实际上Zend自己仅仅构成语言核心，用预定义函数实现
PHP 非常基础部分。而 PHP 包含所有的实际形成语言突出能力的所有模块。

<img src="images/befd863081615f539082d9ff76bf7b39-zend.01-internal-structure.png" width="617" height="281" alt="PHP内部结构." />

以下部分将讨论PHP能在哪里扩展并如何扩展。

### Extension Possibilities

As shown
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.fig.internal-struct" class="link">above</a>,
PHP can be extended primarily at three points: external modules,
built-in modules, and the Zend engine. The following sections discuss
these options.

#### External Modules

External modules can be loaded at script runtime using the function
<span class="function">dl</span>. This function loads a shared object
from disk and makes its functionality available to the script to which
it's being bound. After the script is terminated, the external module is
discarded from memory. This method has both advantages and
disadvantages, as described in the following table:

|                                                                       |                                                                                                             |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Advantages                                                            | Disadvantages                                                                                               |
| External modules don't require recompiling of PHP.                    | The shared objects need to be loaded every time a script is being executed (every hit), which is very slow. |
| The size of PHP remains small by "outsourcing" certain functionality. | External additional files clutter up the disk.                                                              |
|                                                                       |                                                                                                             |

To sum up, external modules are great for third-party products, small
additions to PHP that are rarely used, or just for testing purposes. To
develop additional functionality quickly, external modules provide the
best results. For frequent usage, larger implementations, and complex
code, the disadvantages outweigh the advantages.

Third parties might consider using the *extension* tag in `php.ini` to
create additional external modules to PHP. These external modules are
completely detached from the main package, which is a very handy feature
in commercial environments. Commercial distributors can simply ship
disks or archives containing only their additional modules, without the
need to create fixed and solid PHP binaries that don't allow other
modules to be bound to them.

#### Built-in Modules

Built-in modules are compiled directly into PHP and carried around with
every PHP process; their functionality is instantly available to every
script that's being run. Like external modules, built-in modules have
advantages and disadvantages, as described in the following table:

|                                                                                    |                                                         |
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| Advantages                                                                         | Disadvantages                                           |
| No need to load the module specifically; the functionality is instantly available. | Changes to built-in modules require recompiling of PHP. |
| No external files clutter up the disk; everything resides in the PHP binary.       | The PHP binary grows and consumes more memory.          |

Built-in modules are best when you have a solid library of functions
that remains relatively unchanged, requires better than poor-to-average
performance, or is used frequently by many scripts on your site. The
need to recompile PHP is quickly compensated by the benefit in speed and
ease of use. However, built-in modules are not ideal when rapid
development of small additions is required.

#### The Zend Engine

Of course, extensions can also be implemented directly in the Zend
engine. This strategy is good if you need a change in the language
behavior or require special functions to be built directly into the
language core. In general, however, modifications to the Zend engine
should be avoided. Changes here result in incompatibilities with the
rest of the world, and hardly anyone will ever adapt to specially
patched Zend engines. Modifications can't be detached from the main PHP
sources and are overridden with the next update using the "official"
source repositories. Therefore, this method is generally considered bad
practice and, due to its rarity, is not covered in this book.

### Source Layout

> **Note**:
>
> Prior to working through the rest of this chapter, you should retrieve
> clean, unmodified source trees of your favorite Web server. We're
> working with Apache (available at
> <a href="http://httpd.apache.org/" class="link external">» http://httpd.apache.org/</a>)
> and, of course, with PHP (available at
> <a href="https://www.php.net/" class="link external">» https://www.php.net/</a>
> - does it need to be said?).
>
> Make sure that you can compile a working PHP environment by yourself!
> We won't go into this issue here, however, as you should already have
> this most basic ability when studying this chapter.

Before we start discussing code issues, you should familiarize yourself
with the source tree to be able to quickly navigate through PHP's files.
This is a must-have ability to implement and debug extensions.

The following table describes the contents of the major directories.

|                |                                                                                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Directory      | Contents                                                                                                                                                                                                                                                                           |
| `php-src`      | Main PHP source files and main header files; here you'll find all of PHP's API definitions, macros, etc. (important). Everything else is below this directory.                                                                                                                     |
| `php-src/ext`  | Repository for dynamic and built-in modules; by default, these are the "official" PHP modules that have been integrated into the main source tree. From PHP 4.0, it's possible to compile these standard extensions as dynamic loadable modules (at least, those that support it). |
| `php-src/main` | This directory contains the main php macros and definitions. (important)                                                                                                                                                                                                           |
| `php-src/pear` | Directory for the PHP Extension and Application Repository. This directory contains core PEAR files.                                                                                                                                                                               |
| `php-src/sapi` | Contains the code for the different server abstraction layers.                                                                                                                                                                                                                     |
| `TSRM`         | Location of the "Thread Safe Resource Manager" (TSRM) for Zend and PHP.                                                                                                                                                                                                            |
| `ZendEngine2`  | Location of the Zend Engine files; here you'll find all of Zend's API definitions, macros, etc. (important).                                                                                                                                                                       |

Discussing all the files included in the PHP package is beyond the scope
of this chapter. However, you should take a close look at the following
files:

-   `php-src/main/php.h`, located in the main PHP directory. This file
    contains most of PHP's macro and API definitions.

-   `php-src/Zend/zend.h`, located in the main Zend directory. This file
    contains most of Zend's macros and definitions.

-   `php-src/Zend/zend_API.h`, also located in the Zend directory, which
    defines Zend's API.

You should also follow some sub-inclusions from these files; for
example, the ones relating to the Zend executor, the PHP initialization
file support, and such. After reading these files, take the time to
navigate around the package a little to see the interdependencies of all
files and modules - how they relate to each other and especially how
they make use of each other. This also helps you to adapt to the coding
style in which PHP is authored. To extend PHP, you should quickly adapt
to this style.

#### Extension Conventions

Zend is built using certain conventions; to avoid breaking its
standards, you should follow the rules described in the following
sections.

#### Macros

For almost every important task, Zend ships predefined macros that are
extremely handy. The tables and figures in the following sections
describe most of the basic functions, structures, and macros. The macro
definitions can be found mainly in `zend.h` and `zend_API.h`. We suggest
that you take a close look at these files after having studied this
chapter. (Although you can go ahead and read them now, not everything
will make sense to you yet.)

#### Memory Management

Resource management is a crucial issue, especially in server software.
One of the most valuable resources is memory, and memory management
should be handled with extreme care. Memory management has been
partially abstracted in Zend, and you should stick to this abstraction
for obvious reasons: Due to the abstraction, Zend gets full control over
all memory allocations. Zend is able to determine whether a block is in
use, automatically freeing unused blocks and blocks with lost
references, and thus prevent memory leaks. The functions to be used are
described in the following table:

|                                        |                                                                                                                                                                                                                                    |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Function                               | Description                                                                                                                                                                                                                        |
| <span class="function">emalloc</span>  | Serves as replacement for <span class="function">malloc</span>.                                                                                                                                                                    |
| <span class="function">efree</span>    | Serves as replacement for <span class="function">free</span>.                                                                                                                                                                      |
| <span class="function">estrdup</span>  | Serves as replacement for <span class="function">strdup</span>.                                                                                                                                                                    |
| <span class="function">estrndup</span> | Serves as replacement for <span class="function">strndup</span>. Faster than <span class="function">estrdup</span> and binary-safe. This is the recommended function to use if you know the string length prior to duplicating it. |
| <span class="function">ecalloc</span>  | Serves as replacement for <span class="function">calloc</span>.                                                                                                                                                                    |
| <span class="function">erealloc</span> | Serves as replacement for <span class="function">realloc</span>.                                                                                                                                                                   |

<span class="function">emalloc</span>, <span
class="function">estrdup</span>, <span class="function">estrndup</span>,
<span class="function">ecalloc</span>, and <span
class="function">erealloc</span> allocate internal memory; <span
class="function">efree</span> frees these previously allocated blocks.
Memory handled by the <span class="function">e\*</span> functions is
considered local to the current process and is discarded as soon as the
script executed by this process is terminated.

**Warning**

To allocate resident memory that survives termination of the current
script, you can use <span class="function">malloc</span> and <span
class="function">free</span>. This should only be done with extreme
care, however, and only in conjunction with demands of the Zend API;
otherwise, you risk memory leaks.

Zend also features a thread-safe resource manager to provide better
native support for multithreaded Web servers. This requires you to
allocate local structures for all of your global variables to allow
concurrent threads to be run. Because the thread-safe mode of Zend was
not finished back when this was written, it is not yet extensively
covered here.

#### Directory and File Functions

The following directory and file functions should be used in Zend
modules. They behave exactly like their C counterparts, but provide
virtual working directory support on the thread level.

|                                              |                                                                                                      |
|----------------------------------------------|------------------------------------------------------------------------------------------------------|
| Zend Function                                | Regular C Function                                                                                   |
| <span class="function">V\_GETCWD</span>      | <span class="function">getcwd</span>                                                                 |
| <span class="function">V\_FOPEN</span>       | <span class="function">fopen</span>                                                                  |
| <span class="function">V\_OPEN</span>        | <span class="function">open</span>                                                                   |
| <span class="function">V\_CHDIR</span>       | <span class="function">chdir</span>                                                                  |
| <span class="function">V\_GETWD</span>       | <span class="function">getwd</span>                                                                  |
| <span class="function">V\_CHDIR\_FILE</span> | Takes a file path as an argument and changes the current working directory to that file's directory. |
| <span class="function">V\_STAT</span>        | <span class="function">stat</span>                                                                   |
| <span class="function">V\_LSTAT</span>       | <span class="function">lstat</span>                                                                  |

#### String Handling

Strings are handled a bit differently by the Zend engine than other
values such as integers, Booleans, etc., which don't require additional
memory allocation for storing their values. If you want to return a
string from a function, introduce a new string variable to the symbol
table, or do something similar, you have to make sure that the memory
the string will be occupying has previously been allocated, using the
aforementioned <span class="function">e\*</span> functions for
allocation. (This might not make much sense to you yet; just keep it
somewhere in your head for now - we'll get back to it shortly.)

#### Complex Types

Complex types such as arrays and objects require different treatment.
Zend features a single API for these types - they're stored using hash
tables.

> **Note**:
>
> To reduce complexity in the following source examples, we're only
> working with simple types such as integers at first. A discussion
> about creating more advanced types follows later in this chapter.

### PHP's Automatic Build System

PHP 4 features an automatic build system that's very flexible. All
modules reside in a subdirectory of the `ext` directory. In addition to
its own sources, each module consists of a config.m4 file, for extension
configuration. (for example, see
<a href="http://www.gnu.org/software/m4/" class="link external">» http://www.gnu.org/software/m4/</a>)

All these stub files are generated automatically, along with
`.cvsignore`, by a little shell script named `ext_skel` that resides in
the `ext` directory. As argument it takes the name of the module that
you want to create. The shell script then creates a directory of the
same name, along with the appropriate stub files.

Step by step, the process looks like this:

    :~/cvs/php4/ext:> ./ext_skel --extname=my_module
    Creating directory my_module
    Creating basic files: config.m4 .cvsignore my_module.c php_my_module.h CREDITS EXPERIMENTAL tests/001.phpt my_module.php [done].

    To use your new extension, you will have to execute the following steps:

    1.  $ cd ..
    2.  $ vi ext/my_module/config.m4
    3.  $ ./buildconf
    4.  $ ./configure --[with|enable]-my_module
    5.  $ make
    6.  $ ./php -f ext/my_module/my_module.php
    7.  $ vi ext/my_module/my_module.c
    8.  $ make

    Repeat steps 3-6 until you are satisfied with ext/my_module/config.m4 and
    step 6 confirms that your module is compiled into PHP. Then, start writing
    code and repeat the last two steps as often as necessary.

This instruction creates the aforementioned files. To include the new
module in the automatic configuration and build process, you have to run
`buildconf`, which regenerates the `configure` script by searching
through the `ext` directory and including all found `config.m4` files.

The default `config.m4` shown in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.config.m4" class="xref">The default config.m4.</a>
is a bit more complex:

**示例 \#1 The default `config.m4`.**

``` autoconf
dnl config.m4 for extension my_module

dnl Comments in this file start with the string 'dnl'.
dnl Remove where necessary. This file will not work
dnl without editing.

dnl If your extension references something external, use with:

dnl PHP_ARG_WITH(my_module, for my_module support,
dnl Make sure that the comment is aligned:
dnl [  --with-my_module             Include my_module support])

dnl Otherwise use enable:

dnl PHP_ARG_ENABLE(my_module, whether to enable my_module support,
dnl Make sure that the comment is aligned:
dnl [  --enable-my_module           Enable my_module support])

if test "$PHP_MY_MODULE" != "no"; then
  dnl Write more examples of tests here...

  dnl # --with-my_module -> check with-path
  dnl SEARCH_PATH="/usr/local /usr"     # you might want to change this
  dnl SEARCH_FOR="/include/my_module.h"  # you most likely want to change this
  dnl if test -r $PHP_MY_MODULE/; then # path given as parameter
  dnl   MY_MODULE_DIR=$PHP_MY_MODULE
  dnl else # search default path list
  dnl   AC_MSG_CHECKING([for my_module files in default path])
  dnl   for i in $SEARCH_PATH ; do
  dnl     if test -r $i/$SEARCH_FOR; then
  dnl       MY_MODULE_DIR=$i
  dnl       AC_MSG_RESULT(found in $i)
  dnl     fi
  dnl   done
  dnl fi
  dnl
  dnl if test -z "$MY_MODULE_DIR"; then
  dnl   AC_MSG_RESULT([not found])
  dnl   AC_MSG_ERROR([Please reinstall the my_module distribution])
  dnl fi

  dnl # --with-my_module -> add include path
  dnl PHP_ADD_INCLUDE($MY_MODULE_DIR/include)

  dnl # --with-my_module -> chech for lib and symbol presence
  dnl LIBNAME=my_module # you may want to change this
  dnl LIBSYMBOL=my_module # you most likely want to change this 

  dnl PHP_CHECK_LIBRARY($LIBNAME,$LIBSYMBOL,
  dnl [
  dnl   PHP_ADD_LIBRARY_WITH_PATH($LIBNAME, $MY_MODULE_DIR/lib, MY_MODULE_SHARED_LIBADD)
  dnl   AC_DEFINE(HAVE_MY_MODULELIB,1,[ ])
  dnl ],[
  dnl   AC_MSG_ERROR([wrong my_module lib version or lib not found])
  dnl ],[
  dnl   -L$MY_MODULE_DIR/lib -lm -ldl
  dnl ])
  dnl
  dnl PHP_SUBST(MY_MODULE_SHARED_LIBADD)

  PHP_NEW_EXTENSION(my_module, my_module.c, $ext_shared)
fi
```

If you're unfamiliar with M4 files (now is certainly a good time to get
familiar), this might be a bit confusing at first; but it's actually
quite easy.

*Note:* Everything prefixed with *dnl* is treated as a comment and is
not parsed.

The `config.m4` file is responsible for parsing the command-line options
passed to `configure` at configuration time. This means that it has to
check for required external files and do similar configuration and setup
tasks.

The default file creates two configuration directives in the `configure`
script: *--with-my\_module* and *--enable-my\_module*. Use the first
option when referring external files (such as the *--with-apache*
directive that refers to the Apache directory). Use the second option
when the user simply has to decide whether to enable your extension.
Regardless of which option you use, you should uncomment the other,
unnecessary one; that is, if you're using *--enable-my\_module*, you
should remove support for *--with-my\_module*, and vice versa.

By default, the `config.m4` file created by `ext_skel` accepts both
directives and automatically enables your extension. Enabling the
extension is done by using the *PHP\_EXTENSION* macro. To change the
default behavior to include your module into the PHP binary when desired
by the user (by explicitly specifying *--enable-my\_module* or
*--with-my\_module*), change the test for *$PHP\_MY\_MODULE* to *==
"yes"*:

    if test "$PHP_MY_MODULE" == "yes"; then dnl
        Action.. PHP_EXTENSION(my_module, $ext_shared)
        fi

This would require you to use *--enable-my\_module* each time when
reconfiguring and recompiling PHP.

*Note:* Be sure to run `buildconf` every time you change `config.m4`!

We'll go into more details on the M4 macros available to your
configuration scripts later in this chapter. For now, we'll simply use
the default files.

### Creating Extensions

We'll start with the creation of a very simple extension at first, which
basically does nothing more than implement a function that returns the
integer it receives as parameter.
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.simple" class="xref">A simple extension.</a>
shows the source.

**示例 \#2 A simple extension.**

``` c
/* include standard header */
#include "php.h"

/* declaration of functions to be exported */
ZEND_FUNCTION(first_module);

/* compiled function list so Zend knows what's in this module */
zend_function_entry firstmod_functions[] =
{
    ZEND_FE(first_module, NULL)
    ZEND_FE_END
};

/* compiled module information */
zend_module_entry firstmod_module_entry =
{
    STANDARD_MODULE_HEADER,
    "First Module",
    firstmod_functions,
    NULL, 
    NULL, 
    NULL, 
    NULL, 
    NULL,
    NO_VERSION_YET,
    STANDARD_MODULE_PROPERTIES
};

/* implement standard "stub" routine to introduce ourselves to Zend */
#if COMPILE_DL_FIRST_MODULE
ZEND_GET_MODULE(firstmod)
#endif

/* implement function that is meant to be made available to PHP */
ZEND_FUNCTION(first_module)
{
    long parameter;

    if (zend_parse_parameters(ZEND_NUM_ARGS() TSRMLS_CC, "l", &parameter) == FAILURE) {
        return;
    }

    RETURN_LONG(parameter);
}
```

This code contains a complete PHP module. We'll explain the source code
in detail shortly, but first we'd like to discuss the build process.
(This will allow the impatient to experiment before we dive into API
discussions.)

> **Note**:
>
> The example source makes use of some features introduced with the Zend
> version used in PHP 4.1.0 and above, it won't compile with older PHP
> 4.0.x versions.

#### Compiling Modules

There are basically two ways to compile modules:

-   Use the provided "make" mechanism in the `ext` directory, which also
    allows building of dynamic loadable modules.

-   Compile the sources manually.

The first method should definitely be favored, since, as of PHP 4.0,
this has been standardized into a sophisticated build process. The fact
that it is so sophisticated is also its drawback, unfortunately - it's
hard to understand at first. We'll provide a more detailed introduction
to this later in the chapter, but first let's work with the default
files.

The second method is good for those who (for some reason) don't have the
full PHP source tree available, don't have access to all files, or just
like to juggle with their keyboard. These cases should be extremely
rare, but for the sake of completeness we'll also describe this method.

##### Compiling Using Make

To compile the sample sources using the standard mechanism, copy all
their subdirectories to the `ext` directory of your PHP source tree.
Then run `buildconf`, which will create an updated `configure` script
containing appropriate options for the new extension. By default, all
the sample sources are disabled, so you don't have to fear breaking your
build process.

After you run `buildconf`, `configure      --help` shows the following
additional modules:

      --enable-array_experiments   BOOK: Enables array experiments
      --enable-call_userland       BOOK: Enables userland module
      --enable-cross_conversion    BOOK: Enables cross-conversion module
      --enable-first_module        BOOK: Enables first module
      --enable-infoprint           BOOK: Enables infoprint module
      --enable-reference_test      BOOK: Enables reference test module
      --enable-resource_test       BOOK: Enables resource test module
      --enable-variable_creation   BOOK: Enables variable-creation module

The module shown earlier in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.simple" class="xref">A simple extension.</a>
can be enabled with *--enable-first\_module* or
*--enable-first\_module=yes*.

##### Compiling Manually

To compile your modules manually, you need the following commands:

|           |                                                                                                                            |
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| Action    | Command                                                                                                                    |
| Compiling | cc -fpic -DCOMPILE\_DL\_FIRST\_MODULE=1 -I/usr/local/include -I. -I.. -I../Zend -c -o `<your_object_file>` `<your_c_file>` |
| Linking   | cc -shared -L/usr/local/lib -rdynamic -o `<your_module_file>` `<your_object_file(s)>`                                      |

The command to compile the module simply instructs the compiler to
generate position-independent code (*-fpic* shouldn't be omitted) and
additionally defines the constant *COMPILE\_DL\_FIRST\_MODULE* to tell
the module code that it's compiled as a dynamically loadable module (the
test module above checks for this; we'll discuss it shortly). After
these options, it specifies a number of standard include paths that
should be used as the minimal set to compile the source files.

*Note:* All include paths in the example are relative to the directory
`ext`. If you're compiling from another directory, change the pathnames
accordingly. Required items are the PHP directory, the `Zend` directory,
and (if necessary), the directory in which your module resides.

The link command is also a plain vanilla command instructing linkage as
a dynamic module.

You can include optimization options in the compilation command,
although these have been omitted in this example (but some are included
in the makefile template described in an earlier section).

*Note:* Compiling and linking manually as a static module into the PHP
binary involves very long instructions and thus is not discussed here.
(It's not very efficient to type all those commands.)

### Using Extensions

Depending on the build process you selected, you should either end up
with a new PHP binary to be linked into your Web server (or run as CGI),
or with an .so (shared object) file. If you compiled the example file
`first_module.c` as a shared object, your result file should be
`first_module.so`. To use it, you first have to copy it to a place from
which it's accessible to PHP. For a simple test procedure, you can copy
it to your `htdocs` directory and try it with the source in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.testfile" class="xref">A test file for first_module.so.</a>.
If you compiled it into the PHP binary, omit the call to <span
class="function">dl</span>, as the module's functionality is instantly
available to your scripts.

**Warning**

For security reasons, you *should not* put your dynamic modules into
publicly accessible directories. Even though it *can* be done and it
simplifies testing, you should put them into a separate directory in
production environments.

**示例 \#3 A test file for first\_module.so.**

``` php
<?php
    
// remove next comment if necessary
// dl("first_module.so"); 

$param = 2;
$return = first_module($param);

print("We sent '$param' and got '$return'");

?>
```

Calling this PHP file should output the following:

    We sent '2' and got '2'

If required, the dynamic loadable module is loaded by calling the <span
class="function">dl</span> function. This function looks for the
specified shared object, loads it, and makes its functions available to
PHP. The module exports the function <span
class="function">first\_module</span>, which accepts a single parameter,
converts it to an integer, and returns the result of the conversion.

If you've gotten this far, congratulations! You just built your first
extension to PHP.

### Troubleshooting

Actually, not much troubleshooting can be done when compiling static or
dynamic modules. The only problem that could arise is that the compiler
will complain about missing definitions or something similar. In this
case, make sure that all header files are available and that you
specified their path correctly in the compilation command. To be sure
that everything is located correctly, extract a clean PHP source tree
and use the automatic build in the `ext` directory with the fresh files;
this will guarantee a safe compilation environment. If this fails, try
manual compilation.

PHP might also complain about missing functions in your module. (This
shouldn't happen with the sample sources if you didn't modify them.) If
the names of external functions you're trying to access from your module
are misspelled, they'll remain as "unlinked symbols" in the symbol
table. During dynamic loading and linkage by PHP, they won't resolve
because of the typing errors - there are no corresponding symbols in the
main binary. Look for incorrect declarations in your module file or
incorrectly written external references. Note that this problem is
specific to dynamic loadable modules; it doesn't occur with static
modules. Errors in static modules show up at compile time.

### Source Discussion

Now that you've got a safe build environment and you're able to include
the modules into PHP files, it's time to discuss how everything works.

#### Module Structure

All PHP modules follow a common structure:

-   Header file inclusions (to include all required macros, API
    definitions, etc.)

-   C declaration of exported functions (required to declare the Zend
    function block)

-   Declaration of the Zend function block

-   Declaration of the Zend module block

-   Implementation of <span class="function">get\_module</span>

-   Implementation of all exported functions

#### Header File Inclusions

The only header file you really have to include for your modules is
`php.h`, located in the PHP directory. This file makes all macros and
API definitions required to build new modules available to your code.

*Tip:* It's good practice to create a separate header file for your
module that contains module-specific definitions. This header file
should contain all the forward definitions for exported functions and
include `php.h`. If you created your module using *ext\_skel* you
already have such a header file prepared.

#### Declaring Exported Functions

To declare functions that are to be exported (i.e., made available to
PHP as new native functions), Zend provides a set of macros. A sample
declaration looks like this:

``` c
ZEND_FUNCTION ( my_function );
```

*ZEND\_FUNCTION* declares a new C function that complies with Zend's
internal API. This means that the function is of type *void* and accepts
*INTERNAL\_FUNCTION\_PARAMETERS* (another macro) as parameters.
Additionally, it prefixes the function name with *zif*. The immediately
expanded version of the above definitions would look like this:

``` c
void zif_my_function ( INTERNAL_FUNCTION_PARAMETERS );
```

Expanding *INTERNAL\_FUNCTION\_PARAMETERS* results in the following:

``` c
void zif_my_function( int ht
                    , zval * return_value
                    , zval * this_ptr
                    , int return_value_used
                    , zend_executor_globals * executor_globals
                    );
```

Since the interpreter and executor core have been separated from the
main PHP package, a second API defining macros and function sets has
evolved: the Zend API. As the Zend API now handles quite a few of the
responsibilities that previously belonged to PHP, a lot of PHP functions
have been reduced to macros aliasing to calls into the Zend API. The
recommended practice is to use the Zend API wherever possible, as the
old API is only preserved for compatibility reasons. For example, the
types `zval` and `pval` are identical. `zval` is Zend's definition;
`pval` is PHP's definition (actually, `pval` is an alias for `zval`
now). As the macro *INTERNAL\_FUNCTION\_PARAMETERS* is a Zend macro, the
above declaration contains `zval`. When writing code, you should always
use `zval` to conform to the new Zend API.

The parameter list of this declaration is very important; you should
keep these parameters in mind (see
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.parameters" class="xref">Zend's Parameters to Functions Called from PHP</a>
for descriptions).

|                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Parameter           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| `ht`                | The number of arguments passed to the Zend function. You should not touch this directly, but instead use ZEND\_NUM\_ARGS() to obtain the value.                                                                                                                                                                                                                                                                                                       |
| `return_value`      | This variable is used to pass any return values of your function back to PHP. Access to this variable is best done using the predefined macros. For a description of these see below.                                                                                                                                                                                                                                                                 |
| `this_ptr`          | Using this variable, you can gain access to the object in which your function is contained, if it's used within an object. Use the function <span class="function">getThis</span> to obtain this pointer.                                                                                                                                                                                                                                             |
| `return_value_used` | This flag indicates whether an eventual return value from this function will actually be used by the calling script. *0* indicates that the return value is not used; *1* indicates that the caller expects a return value. Evaluation of this flag can be done to verify correct usage of the function as well as speed optimizations in case returning a value requires expensive operations (for an example, see how `array.c` makes use of this). |
| `executor_globals`  | This variable points to global settings of the Zend engine. You'll find this useful when creating new variables, for example (more about this later). The executor globals can also be introduced to your function by using the macro *TSRMLS\_FETCH()*.                                                                                                                                                                                              |

#### Declaration of the Zend Function Block

Now that you have declared the functions to be exported, you also have
to introduce them to Zend. Introducing the list of functions is done by
using an array of `zend_function_entry`. This array consecutively
contains all functions that are to be made available externally, with
the function's name as it should appear in PHP and its name as defined
in the C source. Internally, `zend_function_entry` is defined as shown
in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.zend-function-entry" class="xref">Internal declaration of zend_function_entry.</a>.

**示例 \#4 Internal declaration of `zend_function_entry`.**

``` c
typedef struct _zend_function_entry {
    char *fname;
    void (*handler)(INTERNAL_FUNCTION_PARAMETERS);
    unsigned char *func_arg_types;
} zend_function_entry;
```

|                  |                                                                                                                                                                    |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Entry            | Description                                                                                                                                                        |
| `fname`          | Denotes the function name as seen in PHP (for example, *fopen*, *mysql\_connect*, or, in our example, *first\_module*).                                            |
| `handler`        | Pointer to the C function responsible for handling calls to this function. For example, see the standard macro *INTERNAL\_FUNCTION\_PARAMETERS* discussed earlier. |
| `func_arg_types` | Allows you to mark certain parameters so that they're forced to be passed by reference. You usually should set this to NULL.                                       |

In the example above, the declaration looks like this:

``` c
zend_function_entry firstmod_functions[] =
{
    ZEND_FE(first_module, NULL)
    ZEND_FE_END
};
```

You can see that the last entry in the list always has to be
*ZEND\_FE\_END*. This marker has to be set for Zend to know when the end
of the list of exported functions is reached.

The macro *ZEND\_FE* (short for 'Zend Function Entry') simply expands to
a structure entry in `zend_function_entry`. Note that these macros
introduce a special naming scheme to your functions - your C functions
will be prefixed with *zif\_*, meaning that *ZEND\_FE(first\_module)*
will refer to a C function <span
class="function">zif\_first\_module</span>. If you want to mix macro
usage with hand-coded entries (not a good practice), keep this in mind.

Tip: Compilation errors that refer to functions named <span
class="function">zif\_\*</span> relate to functions defined with
*ZEND\_FE*.

<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.funcdef-macros" class="xref">Macros for Defining Functions</a>
shows a list of all the macros that you can use to define functions.

|                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Macro Name                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| *ZEND\_FE(name, arg\_types)*                      | Defines a function entry of the name `name` in `zend_function_entry`. Requires a corresponding C function. `arg_types` needs to be set to *NULL*. This function uses automatic C function name generation by prefixing the PHP function name with *zif\_*. For example, *ZEND\_FE("first\_module", NULL)* introduces a function <span class="function">first\_module</span> to PHP and links it to the C function <span class="function">zif\_first\_module</span>. Use in conjunction with *ZEND\_FUNCTION*. |
| *ZEND\_NAMED\_FE(php\_name, name, arg\_types)*    | Defines a function that will be available to PHP by the name `php_name` and links it to the corresponding C function `name`. `arg_types` needs to be set to *NULL*. Use this function if you don't want the automatic name prefixing introduced by *ZEND\_FE*. Use in conjunction with *ZEND\_NAMED\_FUNCTION*.                                                                                                                                                                                               |
| *ZEND\_FALIAS(name, alias, arg\_types)*           | Defines an alias named `alias` for `name`. `arg_types` needs to be set to *NULL*. Doesn't require a corresponding C function; refers to the alias target instead.                                                                                                                                                                                                                                                                                                                                             |
| *PHP\_FE(name, arg\_types)*                       | Old PHP API equivalent of *ZEND\_FE*.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| *PHP\_NAMED\_FE(runtime\_name, name, arg\_types)* | Old PHP API equivalent of *ZEND\_NAMED\_FE*.                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |

*Note:* You can't use *ZEND\_FE* in conjunction with *PHP\_FUNCTION*, or
*PHP\_FE* in conjunction with *ZEND\_FUNCTION*. However, it's perfectly
legal to mix *ZEND\_FE* and *ZEND\_FUNCTION* with *PHP\_FE* and
*PHP\_FUNCTION* when staying with the same macro set for each function
to be declared. But mixing is *not* recommended; instead, you're advised
to use the *ZEND\_\** macros only.

#### Declaration of the Zend Module Block

This block is stored in the structure `zend_module_entry` and contains
all necessary information to describe the contents of this module to
Zend. You can see the internal definition of this module in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.zend-module-entry" class="xref">Internal declaration of zend_module_entry.</a>.

**示例 \#5 Internal declaration of `zend_module_entry`.**

``` c
typedef struct _zend_module_entry zend_module_entry;
     
    struct _zend_module_entry {
    unsigned short size;
    unsigned int zend_api;
    unsigned char zend_debug;
    unsigned char zts;
    char *name;
    zend_function_entry *functions;
    int (*module_startup_func)(INIT_FUNC_ARGS);
    int (*module_shutdown_func)(SHUTDOWN_FUNC_ARGS);
    int (*request_startup_func)(INIT_FUNC_ARGS);
    int (*request_shutdown_func)(SHUTDOWN_FUNC_ARGS);
    void (*info_func)(ZEND_MODULE_INFO_FUNC_ARGS);
    char *version;

[ Rest of the structure is not interesting here ]

};
```

| Entry                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `size`, `zend_api`, `zend_debug` and `zts` | Usually filled with the *"STANDARD\_MODULE\_HEADER"*, which fills these four members with the size of the whole zend\_module\_entry, the *ZEND\_MODULE\_API\_NO*, whether it is a debug build or normal build (*ZEND\_DEBUG*) and if ZTS is enabled (*USING\_ZTS*).                                                                                                                                                                                                                                                                        |
| `name`                                     | Contains the module name (for example, *"File functions"*, *"Socket functions"*, *"Crypt"*, etc.). This name will show up in <span class="function">phpinfo</span>, in the section "Additional Modules."                                                                                                                                                                                                                                                                                                                                   |
| `functions`                                | Points to the Zend function block, discussed in the preceding section.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| `module_startup_func`                      | This function is called once upon module initialization and can be used to do one-time initialization steps (such as initial memory allocation, etc.). To indicate a failure during initialization, return *FAILURE*; otherwise, *SUCCESS*. To mark this field as unused, use *NULL*. To declare a function, use the macro *ZEND\_MINIT*.                                                                                                                                                                                                  |
| `module_shutdown_func`                     | This function is called once upon module shutdown and can be used to do one-time deinitialization steps (such as memory deallocation). This is the counterpart to <span class="function">module\_startup\_func</span>. To indicate a failure during deinitialization, return *FAILURE*; otherwise, *SUCCESS*. To mark this field as unused, use *NULL*. To declare a function, use the macro *ZEND\_MSHUTDOWN*.                                                                                                                            |
| `request_startup_func`                     | This function is called once upon every page request and can be used to do one-time initialization steps that are required to process a request. To indicate a failure here, return *FAILURE*; otherwise, *SUCCESS*. *Note:* As dynamic loadable modules are loaded only on page requests, the request startup function is called right after the module startup function (both initialization events happen at the same time). To mark this field as unused, use *NULL*. To declare a function, use the macro *ZEND\_RINIT*.              |
| `request_shutdown_func`                    | This function is called once after every page request and works as counterpart to <span class="function">request\_startup\_func</span>. To indicate a failure here, return *FAILURE*; otherwise, *SUCCESS*. *Note:* As dynamic loadable modules are loaded only on page requests, the request shutdown function is immediately followed by a call to the module shutdown handler (both deinitialization events happen at the same time). To mark this field as unused, use *NULL*. To declare a function, use the macro *ZEND\_RSHUTDOWN*. |
| `info_func`                                | When <span class="function">phpinfo</span> is called in a script, Zend cycles through all loaded modules and calls this function. Every module then has the chance to print its own "footprint" into the output page. Generally this is used to dump environmental or statistical information. To mark this field as unused, use *NULL*. To declare a function, use the macro *ZEND\_MINFO*.                                                                                                                                               |
| `version`                                  | The version of the module. You can use *NO\_VERSION\_YET* if you don't want to give the module a version number yet, but we really recommend that you add a version string here. Such a version string can look like this (in chronological order): *"2.5-dev"*, *"2.5RC1"*, *"2.5"* or *"2.5pl3"*.                                                                                                                                                                                                                                        |
| Remaining structure elements               | These are used internally and can be prefilled by using the macro *STANDARD\_MODULE\_PROPERTIES\_EX*. You should not assign any values to them. Use *STANDARD\_MODULE\_PROPERTIES\_EX* only if you use global startup and shutdown functions; otherwise, use *STANDARD\_MODULE\_PROPERTIES* directly.                                                                                                                                                                                                                                      |

In our example, this structure is implemented as follows:

``` c
zend_module_entry firstmod_module_entry =
{
    STANDARD_MODULE_HEADER,
    "First Module",
    firstmod_functions,
    NULL, NULL, NULL, NULL, NULL,
    NO_VERSION_YET,
    STANDARD_MODULE_PROPERTIES,
};
```

This is basically the easiest and most minimal set of values you could
ever use. The module name is set to *First Module*, then the function
list is referenced, after which all startup and shutdown functions are
marked as being unused.

For reference purposes, you can find a list of the macros involved in
declared startup and shutdown functions in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.init-shutdown" class="xref">Macros to Declare Startup and Shutdown Functions</a>.
These are not used in our basic example yet, but will be demonstrated
later on. You should make use of these macros to declare your startup
and shutdown functions, as these require special arguments to be passed
(*INIT\_FUNC\_ARGS* and *SHUTDOWN\_FUNC\_ARGS*), which are automatically
included into the function declaration when using the predefined macros.
If you declare your functions manually and the PHP developers decide
that a change in the argument list is necessary, you'll have to change
your module sources to remain compatible.

|                           |                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Macro                     | Description                                                                                                                                                                                                                                                      |
| *ZEND\_MINIT(module)*     | Declares a function for module startup. The generated name will be *zend\_minit\_\<module\>* (for example, *zend\_minit\_first\_module*). Use in conjunction with *ZEND\_MINIT\_FUNCTION*.                                                                       |
| *ZEND\_MSHUTDOWN(module)* | Declares a function for module shutdown. The generated name will be *zend\_mshutdown\_\<module\>* (for example, *zend\_mshutdown\_first\_module*). Use in conjunction with *ZEND\_MSHUTDOWN\_FUNCTION*.                                                          |
| *ZEND\_RINIT(module)*     | Declares a function for request startup. The generated name will be *zend\_rinit\_\<module\>* (for example, *zend\_rinit\_first\_module*). Use in conjunction with *ZEND\_RINIT\_FUNCTION*.                                                                      |
| *ZEND\_RSHUTDOWN(module)* | Declares a function for request shutdown. The generated name will be *zend\_rshutdown\_\<module\>* (for example, *zend\_rshutdown\_first\_module*). Use in conjunction with *ZEND\_RSHUTDOWN\_FUNCTION*.                                                         |
| *ZEND\_MINFO(module)*     | Declares a function for printing module information, used when <span class="function">phpinfo</span> is called. The generated name will be *zend\_info\_\<module\>* (for example, *zend\_info\_first\_module*). Use in conjunction with *ZEND\_MINFO\_FUNCTION*. |

#### Creation of <span class="function">get\_module</span>

This function is special to all dynamic loadable modules. Take a look at
the creation via the *ZEND\_GET\_MODULE* macro first:

``` c
#if COMPILE_DL_FIRSTMOD
     ZEND_GET_MODULE(firstmod) 
#endif
```

The function implementation is surrounded by a conditional compilation
statement. This is needed since the function <span
class="function">get\_module</span> is only required if your module is
built as a dynamic extension. By specifying a definition of
*COMPILE\_DL\_FIRSTMOD* in the compiler command (see above for a
discussion of the compilation instructions required to build a dynamic
extension), you can instruct your module whether you intend to build it
as a dynamic extension or as a built-in module. If you want a built-in
module, the implementation of <span class="function">get\_module</span>
is simply left out.

<span class="function">get\_module</span> is called by Zend at load time
of the module. You can think of it as being invoked by the <span
class="function">dl</span> call in your script. Its purpose is to pass
the module information block back to Zend in order to inform the engine
about the module contents.

If you don't implement a <span class="function">get\_module</span>
function in your dynamic loadable module, Zend will compliment you with
an error message when trying to access it.

#### Implementation of All Exported Functions

Implementing the exported functions is the final step. The example
function in *first\_module* looks like this:

``` c
ZEND_FUNCTION(first_module)
{
    long parameter;

    if (zend_parse_parameters(ZEND_NUM_ARGS() TSRMLS_CC, "l", &parameter) == FAILURE) {
        return;
    }

    RETURN_LONG(parameter);
}
```

The function declaration is done using *ZEND\_FUNCTION*, which
corresponds to *ZEND\_FE* in the function entry table (discussed
earlier).

After the declaration, code for checking and retrieving the function's
arguments, argument conversion, and return value generation follows
(more on this later).

#### Summary

That's it, basically - there's nothing more to implementing PHP modules.
Built-in modules are structured similarly to dynamic modules, so,
equipped with the information presented in the previous sections, you'll
be able to fight the odds when encountering PHP module source files.

Now, in the following sections, read on about how to make use of PHP's
internals to build powerful extensions.

### Accepting Arguments

One of the most important issues for language extensions is accepting
and dealing with data passed via arguments. Most extensions are built to
deal with specific input data (or require parameters to perform their
specific actions), and function arguments are the only real way to
exchange data between the PHP level and the C level. Of course, there's
also the possibility of exchanging data using predefined global values
(which is also discussed later), but this should be avoided by all
means, as it's extremely bad practice.

PHP doesn't make use of any formal function declarations; this is why
call syntax is always completely dynamic and never checked for errors.
Checking for correct call syntax is left to the user code. For example,
it's possible to call a function using only one argument at one time and
four arguments the next time - both invocations are syntactically
absolutely correct.

#### Determining the Number of Arguments

Since PHP doesn't have formal function definitions with support for call
syntax checking, and since PHP features variable arguments, sometimes
you need to find out with how many arguments your function has been
called. You can use the *ZEND\_NUM\_ARGS* macro in this case. In
previous versions of PHP, this macro retrieved the number of arguments
with which the function has been called based on the function's hash
table entry, `ht`, which is passed in the
*INTERNAL\_FUNCTION\_PARAMETERS* list. As `ht` itself now contains the
number of arguments that have been passed to the function,
*ZEND\_NUM\_ARGS* has been stripped down to a dummy macro (see its
definition in `zend_API.h`). But it's still good practice to use it, to
remain compatible with future changes in the call interface. *Note:* The
old PHP equivalent of this macro is *ARG\_COUNT*.

The following code checks for the correct number of arguments:

``` c
if(ZEND_NUM_ARGS() != 2) WRONG_PARAM_COUNT;
```

If the function is not called with two arguments, it exits with an error
message. The code snippet above makes use of the tool macro
*WRONG\_PARAM\_COUNT*, which can be used to generate a standard error
message like:

    "Warning: Wrong parameter count for firstmodule() in /home/www/htdocs/firstmod.php on line 5"

This macro prints a default error message and then returns to the
caller. Its definition can also be found in `zend_API.h` and looks like
this:

``` c
ZEND_API void wrong_param_count(void);

#define WRONG_PARAM_COUNT { wrong_param_count(); return; }
```

As you can see, it calls an internal function named <span
class="function">wrong\_param\_count</span> that's responsible for
printing the warning. For details on generating customized error
messages, see the later section "Printing Information."

#### Retrieving Arguments

> **Note**: **New parameter parsing API**  
>
> This chapter documents the new Zend parameter parsing API introduced
> by Andrei Zmievski. It was introduced in the development stage between
> PHP 4.0.6 and 4.1.0.

Parsing parameters is a very common operation and it may get a bit
tedious. It would also be nice to have standardized error checking and
error messages. Since PHP 4.1.0, there is a way to do just that by using
the new parameter parsing API. It greatly simplifies the process of
receiving parameters, but it has a drawback in that it can't be used for
functions that expect variable number of parameters. But since the vast
majority of functions do not fall into those categories, this parsing
API is recommended as the new standard way.

The prototype for parameter parsing function looks like this:

``` c
int zend_parse_parameters(int num_args TSRMLS_DC, char *type_spec, ...);
```

The first argument to this function is supposed to be the number of
actual parameters passed to your function, so *ZEND\_NUM\_ARGS()* can be
used for that. The second parameter should always be *TSRMLS\_CC* macro.
The third argument is a string that specifies the number and types of
arguments your function is expecting, similar to how printf format
string specifies the number and format of the output values it should
operate on. And finally the rest of the arguments are pointers to
variables which should receive the values from the parameters.

<span class="function">zend\_parse\_parameters</span> also performs type
conversions whenever possible, so that you always receive the data in
the format you asked for. Any type of scalar can be converted to another
one, but conversions between complex types (arrays, objects, and
resources) and scalar types are not allowed.

If the parameters could be obtained successfully and there were no
errors during type conversion, the function will return *SUCCESS*,
otherwise it will return *FAILURE*. The function will output informative
error messages, if the number of received parameters does not match the
requested number, or if type conversion could not be performed.

Here are some sample error messages:

  
Warning - ini\_get\_all() requires at most 1 parameter, 2 given  
Warning - wddx\_deserialize() expects parameter 1 to be string, array
given  

Of course each error message is accompanied by the filename and line
number on which it occurs.

Here is the full list of type specifiers:

-   *l* - long

-   *d* - double

-   *s* - string (with possible null bytes) and its length

-   *b* - boolean

-   *r* - resource, stored in *zval\**

-   *a* - array, stored in *zval\**

-   *o* - object (of any class), stored in *zval\**

-   *O* - object (of class specified by class entry), stored in *zval\**

-   *z* - the actual *zval\**

The following characters also have a meaning in the specifier string:

-   *\|* - indicates that the remaining parameters are optional. The
    storage variables corresponding to these parameters should be
    initialized to default values by the extension, since they will not
    be touched by the parsing function if the parameters are not passed.

-   */* - the parsing function will call <span
    class="function">SEPARATE\_ZVAL\_IF\_NOT\_REF</span> on the
    parameter it follows, to provide a copy of the parameter, unless
    it's a reference.

-   *!* - the parameter it follows can be of specified type or *NULL*
    (only applies to a, o, O, r, and z). If *NULL* value is passed by
    the user, the storage pointer will be set to *NULL*.

The best way to illustrate the usage of this function is through
examples:

``` c
/* Gets a long, a string and its length, and a zval. */
long l;
char *s;
int s_len;
zval *param;
if (zend_parse_parameters(ZEND_NUM_ARGS() TSRMLS_CC,
                          "lsz", &l, &s, &s_len, &param) == FAILURE) {
    return;
}

/* Gets an object of class specified by my_ce, and an optional double. */
zval *obj;
double d = 0.5;
if (zend_parse_parameters(ZEND_NUM_ARGS() TSRMLS_CC,
                          "O|d", &obj, my_ce, &d) == FAILURE) {
    return;
}

/* Gets an object or null, and an array.
   If null is passed for object, obj will be set to NULL. */
zval *obj;
zval *arr;
if (zend_parse_parameters(ZEND_NUM_ARGS() TSRMLS_CC, "O!a", &obj, &arr) == FAILURE) {
    return;
}

/* Gets a separated array. */
zval *arr;
if (zend_parse_parameters(ZEND_NUM_ARGS() TSRMLS_CC, "a/", &arr) == FAILURE) {
    return;
}

/* Get only the first three parameters (useful for varargs functions). */
zval *z;
zend_bool b;
zval *r;
if (zend_parse_parameters(3, "zbr!", &z, &b, &r) == FAILURE) {
    return;
}
```

Note that in the last example we pass 3 for the number of received
parameters, instead of <span class="function">ZEND\_NUM\_ARGS</span>.
What this lets us do is receive the least number of parameters if our
function expects a variable number of them. Of course, if you want to
operate on the rest of the parameters, you will have to use <span
class="function">zend\_get\_parameters\_array\_ex</span> to obtain them.

The parsing function has an extended version that allows for an
additional flags argument that controls its actions.

``` c
int zend_parse_parameters_ex(int flags, int num_args TSRMLS_DC, char *type_spec, ...);
```

The only flag you can pass currently is *ZEND\_PARSE\_PARAMS\_QUIET*,
which instructs the function to not output any error messages during its
operation. This is useful for functions that expect several sets of
completely different arguments, but you will have to output your own
error messages.

For example, here is how you would get either a set of three longs or a
string:

``` c
long l1, l2, l3;
char *s;
if (zend_parse_parameters_ex(ZEND_PARSE_PARAMS_QUIET,
                             ZEND_NUM_ARGS() TSRMLS_CC,
                             "lll", &l1, &l2, &l3) == SUCCESS) {
    /* manipulate longs */
} else if (zend_parse_parameters_ex(ZEND_PARSE_PARAMS_QUIET,
                                    ZEND_NUM_ARGS(), "s", &s, &s_len) == SUCCESS) {
    /* manipulate string */
} else {
    php_error(E_WARNING, "%s() takes either three long values or a string as argument",
              get_active_function_name(TSRMLS_C));
    return;
}
```

With all the abovementioned ways of receiving function parameters you
should have a good handle on this process. For even more example, look
through the source code for extensions that are shipped with PHP - they
illustrate every conceivable situation.

#### Old way of retrieving arguments (deprecated)

> **Note**: **Deprecated parameter parsing API**  
>
> This API is deprecated and superseded by the new ZEND parameter
> parsing API.

After having checked the number of arguments, you need to get access to
the arguments themselves. This is done with the help of <span
class="function">zend\_get\_parameters\_ex</span>:

``` c
zval **parameter;

if(zend_get_parameters_ex(1, &parameter) != SUCCESS)
  WRONG_PARAM_COUNT;
```

All arguments are stored in a `zval` container, which needs to be
pointed to *twice*. The snippet above tries to retrieve one argument and
make it available to us via the `parameter` pointer.

<span class="function">zend\_get\_parameters\_ex</span> accepts at least
two arguments. The first argument is the number of arguments to retrieve
(which should match the number of arguments with which the function has
been called; this is why it's important to check for correct call
syntax). The second argument (and all following arguments) are pointers
to pointers to pointers to `zval`s. (Confusing, isn't it?) All these
pointers are required because Zend works internally with `**zval`; to
adjust a local `**zval` in our function,<span
class="function">zend\_get\_parameters\_ex</span> requires a pointer to
it.

The return value of <span
class="function">zend\_get\_parameters\_ex</span> can either be
*SUCCESS* or *FAILURE*, indicating (unsurprisingly) success or failure
of the argument processing. A failure is most likely related to an
incorrect number of arguments being specified, in which case you should
exit with *WRONG\_PARAM\_COUNT*.

To retrieve more than one argument, you can use a similar snippet:

``` c
zval **param1, **param2, **param3, **param4;
     
if(zend_get_parameters_ex(4, &param1, &param2, &param3, &param4) != SUCCESS)
    WRONG_PARAM_COUNT;
```

<span class="function">zend\_get\_parameters\_ex</span> only checks
whether you're trying to retrieve too many parameters. If the function
is called with five arguments, but you're only retrieving three of them
with <span class="function">zend\_get\_parameters\_ex</span>, you won't
get an error but will get the first three parameters instead. Subsequent
calls of <span class="function">zend\_get\_parameters\_ex</span> won't
retrieve the remaining arguments, but will get the same arguments again.

#### Dealing with a Variable Number of Arguments/Optional Parameters

If your function is meant to accept a variable number of arguments, the
snippets just described are sometimes suboptimal solutions. You have to
create a line calling <span
class="function">zend\_get\_parameters\_ex</span> for every possible
number of arguments, which is often unsatisfying.

For this case, you can use the function <span
class="function">zend\_get\_parameters\_array\_ex</span>, which accepts
the number of parameters to retrieve and an array in which to store
them:

``` c
zval **parameter_array[4];

/* get the number of arguments */
argument_count = ZEND_NUM_ARGS();

/* see if it satisfies our minimal request (2 arguments) */
/* and our maximal acceptance (4 arguments) */
if(argument_count < 2 || argument_count > 4)
    WRONG_PARAM_COUNT;

/* argument count is correct, now retrieve arguments */
if(zend_get_parameters_array_ex(argument_count, parameter_array) != SUCCESS)
    WRONG_PARAM_COUNT;
```

First, the number of arguments is checked to make sure that it's in the
accepted range. After that, <span
class="function">zend\_get\_parameters\_array\_ex</span> is used to fill
`parameter_array` with valid pointers to the argument values.

A very clever implementation of this can be found in the code handling
PHP's <span class="function">fsockopen</span> located in
`ext/standard/fsock.c`, as shown in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.fsockopen" class="xref">PHP's implementation of variable arguments in fsockopen().</a>.
Don't worry if you don't know all the functions used in this source yet;
we'll get to them shortly.

**示例 \#6 PHP's implementation of variable arguments in fsockopen().**

``` c
pval **args[5];
int *sock=emalloc(sizeof(int));
int *sockp;
int arg_count=ARG_COUNT(ht);
int socketd = -1;
unsigned char udp = 0;
struct timeval timeout = { 60, 0 };
unsigned short portno;
unsigned long conv;
char *key = NULL;
FLS_FETCH();

if (arg_count > 5 || arg_count < 2 || zend_get_parameters_array_ex(arg_count,args)==FAILURE) {
    CLOSE_SOCK(1);
    WRONG_PARAM_COUNT;
}

switch(arg_count) {
    case 5:
        convert_to_double_ex(args[4]);
        conv = (unsigned long) (Z_DVAL_PP(args[4]) * 1000000.0);
        timeout.tv_sec = conv / 1000000;
        timeout.tv_usec = conv % 1000000;
        /* fall-through */
    case 4:
        if (!PZVAL_IS_REF(*args[3])) {
            php_error(E_WARNING,"error string argument to fsockopen not passed by reference");
        }
        pval_copy_constructor(*args[3]);
        ZVAL_EMPTY_STRING(*args[3]);
        /* fall-through */
    case 3:
        if (!PZVAL_IS_REF(*args[2])) {
            php_error(E_WARNING,"error argument to fsockopen not passed by reference");
            return;
        }
        ZVAL_LONG(*args[2], 0);
        break;
}

convert_to_string_ex(args[0]);
convert_to_long_ex(args[1]);
portno = (unsigned short) Z_LVAL_P(args[1]);

key = emalloc(Z_STRLEN_P(args[0]) + 10);
```

<span class="function">fsockopen</span> accepts two, three, four, or
five parameters. After the obligatory variable declarations, the
function checks for the correct range of arguments. Then it uses a
fall-through mechanism in a *switch()* statement to deal with all
arguments. The *switch()* statement starts with the maximum number of
arguments being passed (five). After that, it automatically processes
the case of four arguments being passed, then three, by omitting the
otherwise obligatory *break* keyword in all stages. After having
processed the last case, it exits the *switch()* statement and does the
minimal argument processing needed if the function is invoked with only
two arguments.

This multiple-stage type of processing, similar to a stairway, allows
convenient processing of a variable number of arguments.

#### Accessing Arguments

To access arguments, it's necessary for each argument to have a clearly
defined type. Again, PHP's extremely dynamic nature introduces some
quirks. Because PHP never does any kind of type checking, it's possible
for a caller to pass any kind of data to your functions, whether you
want it or not. If you expect an integer, for example, the caller might
pass an array, and vice versa - PHP simply won't notice.

To work around this, you have to use a set of API functions to force a
type conversion on every argument that's being passed (see
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.arg-conv" class="xref">Argument Conversion Functions</a>).

*Note:* All conversion functions expect a `**zval` as parameter.

|                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Function                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span class="function">convert\_to\_boolean\_ex</span> | Forces conversion to a Boolean type. Boolean values remain untouched. Longs, doubles, and strings containing *0* as well as NULL values will result in Boolean *0* (FALSE). Arrays and objects are converted based on the number of entries or properties, respectively, that they have. Empty arrays and objects are converted to FALSE; otherwise, to TRUE. All other values result in a Boolean *1* (TRUE). |
| <span class="function">convert\_to\_long\_ex</span>    | Forces conversion to a long, the default integer type. NULL values, Booleans, resources, and of course longs remain untouched. Doubles are truncated. Strings containing an integer are converted to their corresponding numeric representation, otherwise resulting in *0*. Arrays and objects are converted to *0* if empty, *1* otherwise.                                                                  |
| <span class="function">convert\_to\_double\_ex</span>  | Forces conversion to a double, the default floating-point type. NULL values, Booleans, resources, longs, and of course doubles remain untouched. Strings containing a number are converted to their corresponding numeric representation, otherwise resulting in *0.0*. Arrays and objects are converted to *0.0* if empty, *1.0* otherwise.                                                                   |
| <span class="function">convert\_to\_string\_ex</span>  | Forces conversion to a string. Strings remain untouched. NULL values are converted to an empty string. Booleans containing TRUE are converted to *"1"*, otherwise resulting in an empty string. Longs and doubles are converted to their corresponding string representation. Arrays are converted to the string *"Array"* and objects to the string *"Object"*.                                               |
| *convert\_to\_array\_ex(value)*                        | Forces conversion to an array. Arrays remain untouched. Objects are converted to an array by assigning all their properties to the array table. All property names are used as keys, property contents as values. NULL values are converted to an empty array. All other values are converted to an array that contains the specific source value in the element with the key *0*.                             |
| *convert\_to\_object\_ex(value)*                       | Forces conversion to an object. Objects remain untouched. NULL values are converted to an empty object. Arrays are converted to objects by introducing their keys as properties into the objects and their values as corresponding property contents in the object. All other types result in an object with the property *scalar* , having the corresponding source value as content.                         |
| *convert\_to\_null\_ex(value)*                         | Forces the type to become a NULL value, meaning empty.                                                                                                                                                                                                                                                                                                                                                         |

> **Note**:
>
> You can find a demonstration of the behavior in `cross_conversion.php`
> on the accompanying CD-ROM.

<img src="images/befd863081615f539082d9ff76bf7b39-zend.04-cross-converter.png" width="609" height="523" alt="Cross-conversion behavior of PHP." />

Using these functions on your arguments will ensure type safety for all
data that's passed to you. If the supplied type doesn't match the
required type, PHP forces dummy contents on the resulting value (empty
strings, arrays, or objects, *0* for numeric values, *FALSE* for
Booleans) to ensure a defined state.

Following is a quote from the sample module discussed previously, which
makes use of the conversion functions:

``` c
zval **parameter;

if((ZEND_NUM_ARGS() != 1) || (zend_get_parameters_ex(1, &parameter) != SUCCESS))
{
    WRONG_PARAM_COUNT;
}

convert_to_long_ex(parameter);

RETURN_LONG(Z_LVAL_P(parameter));
```

After retrieving the parameter pointer, the parameter value is converted
to a long (an integer), which also forms the return value of this
function. Understanding access to the contents of the value requires a
short discussion of the `zval` type, whose definition is shown in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.zval-typedef" class="xref">PHP/Zend zval type definition.</a>.

**示例 \#7 PHP/Zend `zval` type definition.**

``` c
typedef pval zval;
     
typedef struct _zval_struct zval;

typedef union _zvalue_value {
    long lval;                 /* long value */
    double dval;               /* double value */
    struct {
        char *val;
        int len;
    } str;
    HashTable *ht;             /* hash table value */
    struct {
        zend_class_entry *ce;
        HashTable *properties;
    } obj;
} zvalue_value;

struct _zval_struct {
    /* Variable information */
    zvalue_value value;        /* value */
    unsigned char type;        /* active type */
    unsigned char is_ref;
    short refcount;
};
```

Actually, `pval` (defined in `php.h`) is only an alias of `zval`
(defined in `zend.h`), which in turn refers to `_zval_struct`. This is a
most interesting structure. `_zval_struct` is the "master" structure,
containing the value structure, type, and reference information. The
substructure `zvalue_value` is a union that contains the variable's
contents. Depending on the variable's type, you'll have to access
different members of this union. For a description of both structures,
see
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.struct-zval" class="xref">Zend zval Structure</a>,
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.struct-zvalue-value" class="xref">Zend zvalue_value Structure</a>
and
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.ztype-constants" class="xref">Zend Variable Type Constants</a>.

|            |                                                                                                                                                                                                                                                                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Entry      | Description                                                                                                                                                                                                                                                                                                                                  |
| `value`    | Union containing this variable's contents. See <a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.struct-zvalue-value" class="xref">Zend zvalue_value Structure</a> for a description.                                                                                                                                         |
| `type`     | Contains this variable's type. For a list of available types, see <a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.ztype-constants" class="xref">Zend Variable Type Constants</a>.                                                                                                                                           |
| `is_ref`   | 0 means that this variable is not a reference; 1 means that this variable is a reference to another variable.                                                                                                                                                                                                                                |
| `refcount` | The number of references that exist for this variable. For every new reference to the value stored in this variable, this counter is increased by 1. For every lost reference, this counter is decreased by 1. When the reference counter reaches 0, no references exist to this value anymore, which causes automatic freeing of the value. |

|        |                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Entry  | Description                                                                                                                                                                                                                                  |
| `lval` | Use this property if the variable is of the type *IS\_LONG*, *IS\_BOOLEAN*, or *IS\_RESOURCE*.                                                                                                                                               |
| `dval` | Use this property if the variable is of the type *IS\_DOUBLE*.                                                                                                                                                                               |
| `str`  | This structure can be used to access variables of the type *IS\_STRING*. The member `len` contains the string length; the member `val` points to the string itself. Zend uses C strings; thus, the string length contains a trailing *0x00*. |
| `ht`   | This entry points to the variable's hash table entry if the variable is an array.                                                                                                                                                            |
| `obj`  | Use this property if the variable is of the type *IS\_OBJECT*.                                                                                                                                                                               |

|                |                                                                                |
|----------------|--------------------------------------------------------------------------------|
| Constant       | Description                                                                    |
| *IS\_NULL*     | Denotes a NULL (empty) value.                                                  |
| *IS\_LONG*     | A long (integer) value.                                                        |
| *IS\_DOUBLE*   | A double (floating point) value.                                               |
| *IS\_STRING*   | A string.                                                                      |
| *IS\_ARRAY*    | Denotes an array.                                                              |
| *IS\_OBJECT*   | An object.                                                                     |
| *IS\_BOOL*     | A Boolean value.                                                               |
| *IS\_RESOURCE* | A resource (for a discussion of resources, see the appropriate section below). |
| *IS\_CONSTANT* | A constant (defined) value.                                                    |

To access a long you access `zval.value.lval`, to access a double you
use `zval.value.dval`, and so on. Because all values are stored in a
union, trying to access data with incorrect union members results in
meaningless output.

Accessing arrays and objects is a bit more complicated and is discussed
later.

#### Dealing with Arguments Passed by Reference

If your function accepts arguments passed by reference that you intend
to modify, you need to take some precautions.

What we didn't say yet is that under the circumstances presented so far,
you don't have write access to any `zval` containers designating
function parameters that have been passed to you. Of course, you can
change any `zval` containers that you created within your function, but
you mustn't change any `zval`s that refer to Zend-internal data!

We've only discussed the so-called <span class="function">\*\_ex</span>
API so far. You may have noticed that the API functions we've used are
called <span class="function">zend\_get\_parameters\_ex</span> instead
of <span class="function">zend\_get\_parameters</span>, <span
class="function">convert\_to\_long\_ex</span> instead of <span
class="function">convert\_to\_long</span>, etc. The <span
class="function">\*\_ex</span> functions form the so-called new
"extended" Zend API. They give a minor speed increase over the old API,
but as a tradeoff are only meant for providing read-only access.

Because Zend works internally with references, different variables may
reference the same value. Write access to a `zval` container requires
this container to contain an isolated value, meaning a value that's not
referenced by any other containers. If a `zval` container were
referenced by other containers and you changed the referenced `zval`,
you would automatically change the contents of the other containers
referencing this `zval` (because they'd simply point to the changed
value and thus change their own value as well).

<span class="function">zend\_get\_parameters\_ex</span> doesn't care
about this situation, but simply returns a pointer to the desired `zval`
containers, whether they consist of references or not. Its corresponding
function in the traditional API, <span
class="function">zend\_get\_parameters</span>, immediately checks for
referenced values. If it finds a reference, it creates a new, isolated
`zval` container; copies the referenced data into this newly allocated
space; and then returns a pointer to the new, isolated value.

This action is called *zval separation* (or pval separation). Because
the <span class="function">\*\_ex</span> API doesn't perform zval
separation, it's considerably faster, while at the same time disabling
write access.

To change parameters, however, write access is required. Zend deals with
this situation in a special way: Whenever a parameter to a function is
passed by reference, it performs automatic zval separation. This means
that whenever you're calling a function like this in PHP, Zend will
automatically ensure that `$parameter` is being passed as an isolated
value, rendering it to a write-safe state:

``` c
my_function(&$parameter);
```

But this *is not* the case with regular parameters! All other parameters
that are not passed by reference are in a read-only state.

This requires you to make sure that you're really working with a
reference - otherwise you might produce unwanted results. To check for a
parameter being passed by reference, you can use the macro
*PZVAL\_IS\_REF*. This macro accepts a *zval\** to check if it is a
reference or not. Examples are given in in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.pass-by-ref" class="xref">Testing for referenced parameter passing.</a>.

**示例 \#8 Testing for referenced parameter passing.**

``` c
zval *parameter;

if (zend_parse_parameters(ZEND_NUM_ARGS() TSRMLS_CC, "z", &parameter) == FAILURE)
    return;

/* check for parameter being passed by reference */
if (!PZVAL_IS_REF(parameter)) {
{
    zend_error(E_WARNING, "Parameter wasn't passed by reference");
    RETURN_NULL();
}

/* make changes to the parameter */
ZVAL_LONG(parameter, 10);
```

<img src="images/befd863081615f539082d9ff76bf7b39-zend.05-reference-test.png" width="609" height="629" alt="Testing for referenced parameter passing" />

#### Assuring Write Safety for Other Parameters

You might run into a situation in which you need write access to a
parameter that's retrieved with <span
class="function">zend\_get\_parameters\_ex</span> but not passed by
reference. For this case, you can use the macro *SEPARATE\_ZVAL*, which
does a zval separation on the provided container. The newly generated
`zval` is detached from internal data and has only a local scope,
meaning that it can be changed or destroyed without implying global
changes in the script context:

``` c
zval **parameter;
     
/* retrieve parameter */
zend_get_parameters_ex(1, &parameter);

/* at this stage, <parameter> still is connected */
/* to Zend's internal data buffers */

/* make <parameter> write-safe */
SEPARATE_ZVAL(parameter);

/* now we can safely modify <parameter> */
/* without implying global changes */
```

*SEPARATE\_ZVAL* uses <span class="function">emalloc</span> to allocate
the new `zval` container, which means that even if you don't deallocate
this memory yourself, it will be destroyed automatically upon script
termination. However, doing a lot of calls to this macro without freeing
the resulting containers will clutter up your RAM.

*Note:* As you can easily work around the lack of write access in the
"traditional" API (with <span
class="function">zend\_get\_parameters</span> and so on), this API seems
to be obsolete, and is not discussed further in this chapter.

### Creating Variables

When exchanging data from your own extensions with PHP scripts, one of
the most important issues is the creation of variables. This section
shows you how to deal with the variable types that PHP supports.

#### Overview

To create new variables that can be seen "from the outside" by the
executing script, you need to allocate a new `zval` container, fill this
container with meaningful values, and then introduce it to Zend's
internal symbol table. This basic process is common to all variable
creations:

``` c
zval *new_variable; 

/* allocate and initialize new container */
MAKE_STD_ZVAL(new_variable); 

/* set type and variable contents here, see the following sections */ 

/* introduce this variable by the name "new_variable_name" into the symbol table */
ZEND_SET_SYMBOL(EG(active_symbol_table), "new_variable_name", new_variable); 

/* the variable is now accessible to the script by using $new_variable_name */
```

The macro *MAKE\_STD\_ZVAL* allocates a new `zval` container using
*ALLOC\_ZVAL* and initializes it using *INIT\_ZVAL*. As implemented in
Zend at the time of this writing, *initializing* means setting the
reference count to *1* and clearing the `is_ref` flag, but this process
could be extended later - this is why it's a good idea to keep using
*MAKE\_STD\_ZVAL* instead of only using *ALLOC\_ZVAL*. If you want to
optimize for speed (and you don't have to explicitly initialize the
`zval` container here), you can use *ALLOC\_ZVAL*, but this isn't
recommended because it doesn't ensure data integrity.

*ZEND\_SET\_SYMBOL* takes care of introducing the new variable to Zend's
symbol table. This macro checks whether the value already exists in the
symbol table and converts the new symbol to a reference if so (with
automatic deallocation of the old `zval` container). This is the
preferred method if speed is not a crucial issue and you'd like to keep
memory usage low.

Note that *ZEND\_SET\_SYMBOL* makes use of the Zend executor globals via
the macro *EG*. By specifying *EG(active\_symbol\_table)*, you get
access to the currently active symbol table, dealing with the active,
local scope. The local scope may differ depending on whether the
function was invoked from within a function.

If you need to optimize for speed and don't care about optimal memory
usage, you can omit the check for an existing variable with the same
value and instead force insertion into the symbol table by using <span
class="function">zend\_hash\_update</span>:

``` c
zval *new_variable;

/* allocate and initialize new container */
MAKE_STD_ZVAL(new_variable);

/* set type and variable contents here, see the following sections */

/* introduce this variable by the name "new_variable_name" into the symbol table */
zend_hash_update(
    EG(active_symbol_table),
    "new_variable_name",
    strlen("new_variable_name") + 1,
    &new_variable,
    sizeof(zval *),
    NULL
);
```

This is actually the standard method used in most modules.

The variables generated with the snippet above will always be of local
scope, so they reside in the context in which the function has been
called. To create new variables in the global scope, use the same method
but refer to another symbol table:

``` c
zval *new_variable;
     
// allocate and initialize new container
MAKE_STD_ZVAL(new_variable);

//
// set type and variable contents here
//

// introduce this variable by the name "new_variable_name" into the global symbol table
ZEND_SET_SYMBOL(&EG(symbol_table), "new_variable_name", new_variable);
```

The macro *ZEND\_SET\_SYMBOL* is now being called with a reference to
the main, global symbol table by referring *EG(symbol\_table)*.

*Note:* The `active_symbol_table` variable is a pointer, but
`symbol_table` is not. This is why you have to use
*EG(active\_symbol\_table)* and *&EG(symbol\_table)* as parameters to
*ZEND\_SET\_SYMBOL* - it requires a pointer.

Similarly, to get a more efficient version, you can hardcode the symbol
table update:

``` c
zval *new_variable;

// allocate and initialize new container
MAKE_STD_ZVAL(new_variable);

//
// set type and variable contents here
//

// introduce this variable by the name "new_variable_name" into the global symbol table
zend_hash_update(
    &EG(symbol_table),
    "new_variable_name",
    strlen("new_variable_name") + 1,
    &new_variable,
    sizeof(zval *),
    NULL
);
```

<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.variable-scopes" class="xref">Creating variables with different scopes.</a>
shows a sample source that creates two variables - `local_variable` with
a local scope and `global_variable` with a global scope (see Figure
9.7). The full example can be found on the CD-ROM.

Note: You can see that the global variable is actually not accessible
from within the function. This is because it's not imported into the
local scope using *global $global\_variable;* in the PHP source.

**示例 \#9 Creating variables with different scopes.**

``` c
ZEND_FUNCTION(variable_creation)
{
    zval *new_var1, *new_var2;

    MAKE_STD_ZVAL(new_var1);
    MAKE_STD_ZVAL(new_var2);

    ZVAL_LONG(new_var1, 10);
    ZVAL_LONG(new_var2, 5);

    ZEND_SET_SYMBOL(EG(active_symbol_table), "local_variable", new_var1);
    ZEND_SET_SYMBOL(&EG(symbol_table), "global_variable", new_var2);

    RETURN_NULL();

}
```

<img src="images/befd863081615f539082d9ff76bf7b39-zend.06-variable-creation.png" width="609" height="629" alt="Creating variables with different scopes" />

#### Longs (Integers)

Now let's get to the assignment of data to variables, starting with
longs. Longs are PHP's integers and are very simple to store. Looking at
the `zval.value` container structure discussed earlier in this chapter,
you can see that the long data type is directly contained in the union,
namely in the `lval` field. The corresponding `type` value for longs is
*IS\_LONG* (see
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.create-long" class="xref">Creation of a long.</a>).

**示例 \#10 Creation of a long.**

``` c
zval *new_long;

MAKE_STD_ZVAL(new_long);

new_long-&gt;type = IS_LONG;
new_long-&gt;value.lval = 10;
```

Alternatively, you can use the macro *ZVAL\_LONG*:

``` c
zval *new_long;

MAKE_STD_ZVAL(new_long);
ZVAL_LONG(new_long, 10);
```

#### Doubles (Floats)

Doubles are PHP's floats and are as easy to assign as longs, because
their value is also contained directly in the union. The member in the
`zval.value` container is `dval`; the corresponding type is
*IS\_DOUBLE*.

``` c
zval *new_double;

MAKE_STD_ZVAL(new_double);

new_double-&gt;type = IS_DOUBLE;
new_double-&gt;value.dval = 3.45;
```

Alternatively, you can use the macro *ZVAL\_DOUBLE*:

``` c
zval *new_double;

MAKE_STD_ZVAL(new_double);
ZVAL_DOUBLE(new_double, 3.45);
```

#### Strings

Strings need slightly more effort. As mentioned earlier, all strings
that will be associated with Zend's internal data structures need to be
allocated using Zend's own memory-management functions. Referencing of
static strings or strings allocated with standard routines is not
allowed. To assign strings, you have to access the structure `str` in
the `zval.value` container. The corresponding type is *IS\_STRING*:

``` c
zval *new_string;
char *string_contents = "This is a new string variable";

MAKE_STD_ZVAL(new_string);

new_string-&gt;type = IS_STRING;
new_string-&gt;value.str.len = strlen(string_contents);
new_string-&gt;value.str.val = estrdup(string_contents);
```

Note the usage of Zend's <span class="function">estrdup</span> here. Of
course, you can also use the predefined macro *ZVAL\_STRING*:

    zval *new_string;
    char *string_contents = "This is a new string variable";

    MAKE_STD_ZVAL(new_string);
    ZVAL_STRING(new_string, string_contents, 1);

*ZVAL\_STRING* accepts a third parameter that indicates whether the
supplied string contents should be duplicated (using <span
class="function">estrdup</span>). Setting this parameter to *1* causes
the string to be duplicated; *0* simply uses the supplied pointer for
the variable contents. This is most useful if you want to create a new
variable referring to a string that's already allocated in Zend internal
memory.

If you want to truncate the string at a certain position or you already
know its length, you can use *ZVAL\_STRINGL(zval, string, length,
duplicate)*, which accepts an explicit string length to be set for the
new string. This macro is faster than *ZVAL\_STRING* and also
binary-safe.

To create empty strings, set the string length to *0* and use
*empty\_string* as contents:

``` c
new_string-&gt;type = IS_STRING;
new_string-&gt;value.str.len = 0;
new_string-&gt;value.str.val = empty_string;
```

Of course, there's a macro for this as well (*ZVAL\_EMPTY\_STRING*):

``` c
MAKE_STD_ZVAL(new_string);
ZVAL_EMPTY_STRING(new_string);
```

#### Booleans

Booleans are created just like longs, but have the type *IS\_BOOL*.
Allowed values in `lval` are *0* and *1*:

``` c
zval *new_bool;

MAKE_STD_ZVAL(new_bool);

new_bool-&gt;type = IS_BOOL;
new_bool-&gt;value.lval = 1;
```

The corresponding macros for this type are *ZVAL\_BOOL* (allowing
specification of the value) as well as *ZVAL\_TRUE* and *ZVAL\_FALSE*
(which explicitly set the value to *TRUE* and *FALSE*, respectively).

#### Arrays

Arrays are stored using Zend's internal hash tables, which can be
accessed using the <span class="function">zend\_hash\_\*</span> API. For
every array that you want to create, you need a new hash table handle,
which will be stored in the `ht` member of the `zval.value` container.

There's a whole API solely for the creation of arrays, which is
extremely handy. To start a new array, you call <span
class="function">array\_init</span>.

``` c
zval *new_array;

MAKE_STD_ZVAL(new_array);

array_init(new_array);
```

<span class="function">array\_init</span> always returns *SUCCESS*.

To add new elements to the array, you can use numerous functions,
depending on what you want to do.
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.api-assoc-arrays" class="xref">Zend's API for Associative Arrays</a>,
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.api-indexed-arrays" class="xref">Zend's API for Indexed Arrays, Part 1</a>
and
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.api-indexed-array-2" class="xref">Zend's API for Indexed Arrays, Part 2</a>
describe these functions. All functions return *FAILURE* on failure and
*SUCCESS* on success.

|                                                                                                                        |                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Function                                                                                                               | Description                                                                                                                            |
| <span class="function">add\_assoc\_long(zval \*array, char \*key, long n);</span>                                      | Adds an element of type *long*.                                                                                                        |
| <span class="function">add\_assoc\_unset(zval \*array, char \*key);</span>                                             | Adds an unset element.                                                                                                                 |
| <span class="function">add\_assoc\_bool(zval \*array, char \*key, int b);</span>                                       | Adds a Boolean element.                                                                                                                |
| <span class="function">add\_assoc\_resource(zval \*array, char \*key, int r);</span>                                   | Adds a resource to the array.                                                                                                          |
| <span class="function">add\_assoc\_double(zval \*array, char \*key, double d);</span>                                  | Adds a floating-point value.                                                                                                           |
| <span class="function">add\_assoc\_string(zval \*array, char \*key, char \*str, int duplicate);</span>                 | Adds a string to the array. The flag `duplicate` specifies whether the string contents have to be copied to Zend internal memory.      |
| <span class="function"> add\_assoc\_stringl(zval \*array, char \*key, char \*str, uint length, int duplicate); </span> | Adds a string with the desired length `length` to the array. Otherwise, behaves like <span class="function">add\_assoc\_string</span>. |
| <span class="function">add\_assoc\_zval(zval \*array, char \*key, zval \*value);</span>                                | Adds a zval to the array. Useful for adding other arrays, objects, streams, etc...                                                     |

|                                                                                                                    |                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Function                                                                                                           | Description                                                                                                                                                                     |
| <span class="function">add\_index\_long(zval \*array, uint idx, long n);</span>                                    | Adds an element of type *long*.                                                                                                                                                 |
| <span class="function">add\_index\_unset(zval \*array, uint idx);</span>                                           | Adds an unset element.                                                                                                                                                          |
| <span class="function">add\_index\_bool(zval \*array, uint idx, int b);</span>                                     | Adds a Boolean element.                                                                                                                                                         |
| <span class="function">add\_index\_resource(zval \*array, uint idx, int r);</span>                                 | Adds a resource to the array.                                                                                                                                                   |
| <span class="function">add\_index\_double(zval \*array, uint idx, double d);</span>                                | Adds a floating-point value.                                                                                                                                                    |
| <span class="function">add\_index\_string(zval \*array, uint idx, char \*str, int duplicate);</span>               | Adds a string to the array. The flag `duplicate` specifies whether the string contents have to be copied to Zend internal memory.                                               |
| <span class="function">add\_index\_stringl(zval \*array, uint idx, char \*str, uint length, int duplicate);</span> | Adds a string with the desired length `length` to the array. This function is faster and binary-safe. Otherwise, behaves like <span class="function">add\_index\_string</span>. |
| <span class="function">add\_index\_zval(zval \*array, uint idx, zval \*value);</span>                              | Adds a zval to the array. Useful for adding other arrays, objects, streams, etc...                                                                                              |

|                                                                                                                |                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Function                                                                                                       | Description                                                                                                                                                                     |
| <span class="function">add\_next\_index\_long(zval \*array, long n);</span>                                    | Adds an element of type *long*.                                                                                                                                                 |
| <span class="function">add\_next\_index\_unset(zval \*array);</span>                                           | Adds an unset element.                                                                                                                                                          |
| <span class="function">add\_next\_index\_bool(zval \*array, int b);</span>                                     | Adds a Boolean element.                                                                                                                                                         |
| <span class="function">add\_next\_index\_resource(zval \*array, int r);</span>                                 | Adds a resource to the array.                                                                                                                                                   |
| <span class="function">add\_next\_index\_double(zval \*array, double d);</span>                                | Adds a floating-point value.                                                                                                                                                    |
| <span class="function">add\_next\_index\_string(zval \*array, char \*str, int duplicate);</span>               | Adds a string to the array. The flag `duplicate` specifies whether the string contents have to be copied to Zend internal memory.                                               |
| <span class="function">add\_next\_index\_stringl(zval \*array, char \*str, uint length, int duplicate);</span> | Adds a string with the desired length `length` to the array. This function is faster and binary-safe. Otherwise, behaves like <span class="function">add\_index\_string</span>. |
| <span class="function">add\_next\_index\_zval(zval \*array, zval \*value);</span>                              | Adds a zval to the array. Useful for adding other arrays, objects, streams, etc...                                                                                              |

All these functions provide a handy abstraction to Zend's internal hash
API. Of course, you can also use the hash functions directly - for
example, if you already have a `zval` container allocated that you want
to insert into an array. This is done using <span
class="function">zend\_hash\_update</span> for associative arrays (see
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.array-add-assoc" class="xref">Adding an element to an associative array.</a>)
and <span class="function">zend\_hash\_index\_update</span> for indexed
arrays (see
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.array-add-indexed" class="xref">Adding an element to an indexed array.</a>):

**示例 \#11 Adding an element to an associative array.**

``` c
zval *new_array, *new_element;
char *key = "element_key";
      
MAKE_STD_ZVAL(new_array);
MAKE_STD_ZVAL(new_element);

array_init(new_array);

ZVAL_LONG(new_element, 10);

if(zend_hash_update(new_array-&gt;value.ht, key, strlen(key) + 1, (void *)&new_element, sizeof(zval *), NULL) == FAILURE)
{
    // do error handling here
}
```

**示例 \#12 Adding an element to an indexed array.**

``` c
zval *new_array, *new_element;
int key = 2;

MAKE_STD_ZVAL(new_array);
MAKE_STD_ZVAL(new_element);

array_init(new_array);

ZVAL_LONG(new_element, 10);

if(zend_hash_index_update(new_array-&gt;value.ht, key, (void *)&new_element, sizeof(zval *), NULL) == FAILURE)
{
    // do error handling here
}
```

To emulate the functionality of <span
class="function">add\_next\_index\_\*</span>, you can use this:

``` c
zend_hash_next_index_insert(ht, zval **new_element, sizeof(zval *), NULL)
```

*Note:* To return arrays from a function, use <span
class="function">array\_init</span> and all following actions on the
predefined variable `return_value` (given as argument to your exported
function; see the earlier discussion of the call interface). You do not
have to use *MAKE\_STD\_ZVAL* on this.

*Tip:* To avoid having to write *new\_array-\>value.ht* every time, you
can use *HASH\_OF(new\_array)*, which is also recommended for
compatibility and style reasons.

#### Objects

Since objects can be converted to arrays (and vice versa), you might
have already guessed that they have a lot of similarities to arrays in
PHP. Objects are maintained with the same hash functions, but there's a
different API for creating them.

To initialize an object, you use the function <span
class="function">object\_init</span>:

``` c
zval *new_object;

MAKE_STD_ZVAL(new_object);

if(object_init(new_object) != SUCCESS)
{
    // do error handling here
}
```

You can use the functions described in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.object-creation" class="xref">Zend's API for Object Creation</a>
to add members to your object.

|                                                                                                                          |                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Function                                                                                                                 | Description                                                                                                                                                         |
| <span class="function">add\_property\_long(zval \*object, char \*key, long l);</span>                                    | Adds a long to the object.                                                                                                                                          |
| <span class="function">add\_property\_unset(zval \*object, char \*key);</span>                                           | Adds an unset property to the object.                                                                                                                               |
| <span class="function">add\_property\_bool(zval \*object, char \*key, int b);</span>                                     | Adds a Boolean to the object.                                                                                                                                       |
| <span class="function">add\_property\_resource(zval \*object, char \*key, long r);</span>                                | Adds a resource to the object.                                                                                                                                      |
| <span class="function">add\_property\_double(zval \*object, char \*key, double d);</span>                                | Adds a double to the object.                                                                                                                                        |
| <span class="function">add\_property\_string(zval \*object, char \*key, char \*str, int duplicate);</span>               | Adds a string to the object.                                                                                                                                        |
| <span class="function">add\_property\_stringl(zval \*object, char \*key, char \*str, uint length, int duplicate);</span> | Adds a string of the specified length to the object. This function is faster than <span class="function">add\_property\_string</span> and also binary-safe.         |
| <span class="function">add\_property\_zval(zval \*obect, char \*key, zval \*container):</span>                           | Adds a *zval* container to the object. This is useful if you have to add properties which aren't simple types like integers or strings but arrays or other objects. |

#### Resources

Resources are a special kind of data type in PHP. The term *resources*
doesn't really refer to any special kind of data, but to an abstraction
method for maintaining any kind of information. Resources are kept in a
special resource list within Zend. Each entry in the list has a
correspondending type definition that denotes the kind of resource to
which it refers. Zend then internally manages all references to this
resource. Access to a resource is never possible directly - only via a
provided API. As soon as all references to a specific resource are lost,
a corresponding shutdown function is called.

For example, resources are used to store database links and file
descriptors. The *de facto* standard implementation can be found in the
MySQL module, but other modules such as the Oracle module also make use
of resources.

> **Note**:
>
> In fact, a resource can be a pointer to anything you need to handle in
> your functions (e.g. pointer to a structure) and the user only has to
> pass a single resource variable to your function.

To create a new resource you need to register a resource destruction
handler for it. Since you can store any kind of data as a resource, Zend
needs to know how to free this resource if its not longer needed. This
works by registering your own resource destruction handler to Zend which
in turn gets called by Zend whenever your resource can be freed (whether
manually or automatically). Registering your resource handler within
Zend returns you the *resource type handle* for that resource. This
handle is needed whenever you want to access a resource of this type
later and is most of time stored in a global static variable within your
extension. There is no need to worry about thread safety here because
you only register your resource handler once during module
initialization.

The Zend function to register your resource handler is defined as:

``` c
ZEND_API int zend_register_list_destructors_ex(rsrc_dtor_func_t ld, rsrc_dtor_func_t pld, char *type_name, int module_number);
```

There are two different kinds of resource destruction handlers you can
pass to this function: a handler for normal resources and a handler for
persistent resources. Persistent resources are for example used for
database connection. When registering a resource, either of these
handlers must be given. For the other handler just pass *NULL*.

<span class="function">zend\_register\_list\_destructors\_ex</span>
accepts the following parameters:

|                  |                                                                                                                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ld*             | Normal resource destruction handler callback                                                                                                                                                                                        |
| *pld*            | Pesistent resource destruction handler callback                                                                                                                                                                                     |
| *type\_name*     | A string specifying the name of your resource. It's always a good thing to specify a unique name within PHP for the resource type so when the user for example calls *var\_dump($resource);* he also gets the name of the resource. |
| *module\_number* | The *module\_number* is automatically available in your *PHP\_MINIT\_FUNCTION* function and therefore you just pass it over.                                                                                                        |

The return value is a unique integer ID for your *resource type*.

The resource destruction handler (either normal or persistent resources)
has the following prototype:

    void resource_destruction_handler(zend_rsrc_list_entry *rsrc TSRMLS_DC);

The passed *rsrc* is a pointer to the following structure:

``` c
typedef struct _zend_rsrc_list_entry {
     
    void *ptr;
    int type;
    int refcount;

} zend_rsrc_list_entry;
```

The member *void \*ptr* is the actual pointer to your resource.

Now we know how to start things, we define our own resource we want
register within Zend. It is only a simple structure with two integer
members:

``` c
typedef struct {
     
    int resource_link;
    int resource_type;

} my_resource;
```

Our resource destruction handler is probably going to look something
like this:

``` c
void my_destruction_handler(zend_rsrc_list_entry *rsrc TSRMLS_DC) {

    // You most likely cast the void pointer to your structure type

    my_resource *my_rsrc = (my_resource *) rsrc->ptr;

    // Now do whatever needs to be done with you resource. Closing
    // Files, Sockets, freeing additional memory, etc.
    // Also, don't forget to actually free the memory for your resource too!

    do_whatever_needs_to_be_done_with_the_resource(my_rsrc);
}
```

> **Note**:
>
> One important thing to mention: If your resource is a rather complex
> structure which also contains pointers to memory you allocated during
> runtime you have to free them *before* freeing the resource itself!

Now that we have defined

1.  what our resource is and

2.  our resource destruction handler

we can go on and do the rest of the steps:

1.  create a global variable within the extension holding the resource
    ID so it can be accessed from every function which needs it

2.  define the resource name

3.  write the resource destruction handler

4.  and finally register the handler

``` c
// Somewhere in your extension, define the variable for your registered resources.
    // If you wondered what 'le' stands for: it simply means 'list entry'.
    static int le_myresource;

    // It's nice to define your resource name somewhere
    #define le_myresource_name  "My type of resource"

    [...]

    // Now actually define our resource destruction handler
    void my_destruction_handler(zend_rsrc_list_entry *rsrc TSRMLS_DC) {

        my_resource *my_rsrc = (my_resource *) rsrc->ptr;
        do_whatever_needs_to_be_done_with_the_resource(my_rsrc);
    }

    [...]

    PHP_MINIT_FUNCTION(my_extension) {

        // Note that 'module_number' is already provided through the
        // PHP_MINIT_FUNCTION() function definition.

        le_myresource = zend_register_list_destructors_ex(my_destruction_handler, NULL, le_myresource_name, module_number);

        // You can register additional resources, initialize
        // your global vars, constants, whatever.
    }
```

To actually register a new resource you use can either use the <span
class="function">zend\_register\_resource</span> function or the <span
class="function">ZEND\_REGISTER\_RESOURE</span> macro, both defined in
zend\_list.h. Although the arguments for both map 1:1 it's a good idea
to always use macros to be upwards compatible:

``` c
int ZEND_REGISTER_RESOURCE(zval *rsrc_result, void *rsrc_pointer, int rsrc_type);
```

|                 |                                                                                                                                                     |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| *rsrc\_result*  | This is an already initialized *zval \** container.                                                                                                 |
| *rsrc\_pointer* | Your resource pointer you want to store.                                                                                                            |
| *rsrc\_type*    | The type which you received when you registered the resource destruction handler. If you followed the naming scheme this would be *le\_myresource*. |

The return value is a unique integer identifier for that resource.

What is really going on when you register a new resource is it gets
inserted in an internal list in Zend and the result is just stored in
the given *zval \** container:

``` c
rsrc_id = zend_list_insert(rsrc_pointer, rsrc_type);
     
    if (rsrc_result) {
        rsrc_result->value.lval = rsrc_id;
        rsrc_result->type = IS_RESOURCE;
    }

    return rsrc_id;
```

The returned *rsrc\_id* uniquely identifies the newly registered
resource. You can use the macro *RETURN\_RESOURE* to return it to the
user:

        RETURN_RESOURCE(rsrc_id)

> **Note**:
>
> It is common practice that if you want to return the resource
> immediately to the user you specify the *return\_value* as the *zval
> \** container.

Zend now keeps track of all references to this resource. As soon as all
references to the resource are lost, the destructor that you previously
registered for this resource is called. The nice thing about this setup
is that you don't have to worry about memory leakages introduced by
allocations in your module - just register all memory allocations that
your calling script will refer to as resources. As soon as the script
decides it doesn't need them anymore, Zend will find out and tell you.

Now that the user got his resource, at some point he is passing it back
to one of your functions. The `value.lval` inside the *zval \**
container contains the key to your resource and thus can be used to
fetch the resource with the following macro: *ZEND\_FETCH\_RESOURCE*:

``` c
ZEND_FETCH_RESOURCE(rsrc, rsrc_type, rsrc_id, default_rsrc_id, resource_type_name, resource_type)
```

|                        |                                                                                                                                                          |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| *rsrc*                 | This is your pointer which will point to your previously registered resource.                                                                            |
| *rsrc\_type*           | This is the typecast argument for your pointer, e.g. *myresource \**.                                                                                    |
| *rsrc\_id*             | This is the address of the *zval \**container the user passed to your function, e.g. *&z\_resource* if *zval \*z\_resource* is given.                    |
| *default\_rsrc\_id*    | This integer specifies the default resource *ID* if no resource could be fetched or -1.                                                                  |
| *resource\_type\_name* | This is the name of the requested resource. It's a string and is used when the resource can't be found or is invalid to form a meaningful error message. |
| *resource\_type*       | The *resource\_type* you got back when registering the resource destruction handler. In our example this was `le_myresource`.                            |

This macro has no return value. It is for the developers convenience and
takes care of TSRMLS arguments passing and also does check if the
resource could be fetched. It throws a warning message and returns the
current PHP function with *NULL* if there was a problem retrieving the
resource.

To force removal of a resource from the list, use the function <span
class="function">zend\_list\_delete</span>. You can also force the
reference count to increase if you know that you're creating another
reference for a previously allocated value (for example, if you're
automatically reusing a default database link). For this case, use the
function <span class="function">zend\_list\_addref</span>. To search for
previously allocated resource entries, use <span
class="function">zend\_list\_find</span>. The complete API can be found
in `zend_list.h`.

#### Macros for Automatic Global Variable Creation

In addition to the macros discussed earlier, a few macros allow easy
creation of simple global variables. These are nice to know in case you
want to introduce global flags, for example. This is somewhat bad
practice, but Table
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.macros-global-vars" class="xref">Macros for Global Variable Creation</a>
describes macros that do exactly this task. They don't need any `zval`
allocation; you simply have to supply a variable name and value.

|                                          |                                                                                                                  |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| Macro                                    | Description                                                                                                      |
| *SET\_VAR\_STRING(name, value)*          | Creates a new string.                                                                                            |
| *SET\_VAR\_STRINGL(name, value, length)* | Creates a new string of the specified length. This macro is faster than *SET\_VAR\_STRING* and also binary-safe. |
| *SET\_VAR\_LONG(name, value)*            | Creates a new long.                                                                                              |
| *SET\_VAR\_DOUBLE(name, value)*          | Creates a new double.                                                                                            |

#### Creating Constants

Zend supports the creation of true constants (as opposed to regular
variables). Constants are accessed without the typical dollar sign (*$*)
prefix and are available in all scopes. Examples include *TRUE* and
*FALSE*, to name just two.

To create your own constants, you can use the macros in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.create-const" class="xref">Macros for Creating Constants</a>.
All the macros create a constant with the specified name and value.

You can also specify flags for each constant:

-   *CONST\_CS* - This constant's name is to be treated as case
    sensitive.

-   *CONST\_PERSISTENT* - This constant is persistent and won't be
    "forgotten" when the current process carrying this constant shuts
    down.

To use the flags, combine them using a inary OR:

     // register a new constant of type "long"
         REGISTER_LONG_CONSTANT("NEW_MEANINGFUL_CONSTANT", 324, CONST_CS |
         CONST_PERSISTENT); 

There are two types of macros - *REGISTER\_\*\_CONSTANT*
and*REGISTER\_MAIN\_\*\_CONSTANT*. The first type creates constants
bound to the current module. These constants are dumped from the symbol
table as soon as the module that registered the constant is unloaded
from memory. The second type creates constants that remain in the symbol
table independently of the module.

|                                                                                                                           |                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Macro                                                                                                                     | Description                                                                                                                                           |
| *REGISTER\_LONG\_CONSTANT(name, value, flags)* *REGISTER\_MAIN\_LONG\_CONSTANT(name, value, flags)*                       | Registers a new constant of type long.                                                                                                                |
| *REGISTER\_DOUBLE\_CONSTANT(name, value, flags)* *REGISTER\_MAIN\_DOUBLE\_CONSTANT(name, value, flags)*                   | Registers a new constant of type double.                                                                                                              |
| *REGISTER\_STRING\_CONSTANT(name, value, flags)* *REGISTER\_MAIN\_STRING\_CONSTANT(name, value, flags)*                   | Registers a new constant of type string. The specified string must reside in Zend's internal memory.                                                  |
| *REGISTER\_STRINGL\_CONSTANT(name, value, length, flags)* *REGISTER\_MAIN\_STRINGL\_CONSTANT(name, value, length, flags)* | Registers a new constant of type string. The string length is explicitly set to `length`. The specified string must reside in Zend's internal memory. |

### Duplicating Variable Contents: The Copy Constructor

Sooner or later, you may need to assign the contents of one `zval`
container to another. This is easier said than done, since the `zval`
container doesn't contain only type information, but also references to
places in Zend's internal data. For example, depending on their size,
arrays and objects may be nested with lots of hash table entries. By
assigning one `zval` to another, you avoid duplicating the hash table
entries, using only a reference to them (at most).

To copy this complex kind of data, use the *copy constructor*. Copy
constructors are typically defined in languages that support operator
overloading, with the express purpose of copying complex types. If you
define an object in such a language, you have the possibility of
overloading the "=" operator, which is usually responsible for assigning
the contents of the rvalue (result of the evaluation of the right side
of the operator) to the lvalue (same for the left side).

*Overloading* means assigning a different meaning to this operator, and
is usually used to assign a function call to an operator. Whenever this
operator would be used on such an object in a program, this function
would be called with the lvalue and rvalue as parameters. Equipped with
that information, it can perform the operation it intends the "="
operator to have (usually an extended form of copying).

This same form of "extended copying" is also necessary for PHP's `zval`
containers. Again, in the case of an array, this extended copying would
imply re-creation of all hash table entries relating to this array. For
strings, proper memory allocation would have to be assured, and so on.

Zend ships with such a function, called <span
class="function">zend\_copy\_ctor</span> (the previous PHP equivalent
was <span class="function">pval\_copy\_constructor</span>).

A most useful demonstration is a function that accepts a complex type as
argument, modifies it, and then returns the argument:

``` c
zval *parameter;
   
if (zend_parse_parameters(ZEND_NUM_ARGS() TSRMLS_CC, "z", &parameter) == FAILURE)
   return;
}
   
// do modifications to the parameter here

// now we want to return the modified container:
*return_value = *parameter;
zval_copy_ctor(return_value);
```

The first part of the function is plain-vanilla argument retrieval.
After the (left out) modifications, however, it gets interesting: The
container of `parameter` is assigned to the (predefined) `return_value`
container. Now, in order to effectively duplicate its contents, the copy
constructor is called. The copy constructor works directly with the
supplied argument, and the standard return values are *FAILURE* on
failure and *SUCCESS* on success.

If you omit the call to the copy constructor in this example, both
`parameter` and `return_value` would point to the same internal data,
meaning that `return_value` would be an illegal additional reference to
the same data structures. Whenever changes occurred in the data that
`parameter` points to, `return_value` might be affected. Thus, in order
to create separate copies, the copy constructor must be used.

The copy constructor's counterpart in the Zend API, the destructor <span
class="function">zval\_dtor</span>, does the opposite of the
constructor.

### Returning Values

Returning values from your functions to PHP was described briefly in an
earlier section; this section gives the details. Return values are
passed via the `return_value` variable, which is passed to your
functions as argument. The `return_value` argument consists of a `zval`
container (see the earlier discussion of the call interface) that you
can freely modify. The container itself is already allocated, so you
don't have to run *MAKE\_STD\_ZVAL* on it. Instead, you can access its
members directly.

To make returning values from functions easier and to prevent hassles
with accessing the internal structures of the `zval` container, a set of
predefined macros is available (as usual). These macros automatically
set the correspondent type and value, as described in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.return" class="xref">Predefined Macros for Returning Values from a Function</a>
and
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.retval" class="xref">Predefined Macros for Setting the Return Value of a Function</a>.

> **Note**:
>
> The macros in
> <a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.return" class="xref">Predefined Macros for Returning Values from a Function</a>
> automatically *return* from your function, those in
> <a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.retval" class="xref">Predefined Macros for Setting the Return Value of a Function</a>
> only *set* the return value; they don't return from your function.

|                                              |                                                                                                                                       |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Macro                                        | Description                                                                                                                           |
| *RETURN\_RESOURCE(resource)*                 | Returns a resource.                                                                                                                   |
| *RETURN\_BOOL(bool)*                         | Returns a Boolean.                                                                                                                    |
| *RETURN\_NULL()*                             | Returns nothing (a NULL value).                                                                                                       |
| *RETURN\_LONG(long)*                         | Returns a long.                                                                                                                       |
| *RETURN\_DOUBLE(double)*                     | Returns a double.                                                                                                                     |
| *RETURN\_STRING(string, duplicate)*          | Returns a string. The `duplicate` flag indicates whether the string should be duplicated using <span class="function">estrdup</span>. |
| *RETURN\_STRINGL(string, length, duplicate)* | Returns a string of the specified length; otherwise, behaves like *RETURN\_STRING*. This macro is faster and binary-safe, however.    |
| *RETURN\_EMPTY\_STRING()*                    | Returns an empty string.                                                                                                              |
| *RETURN\_FALSE*                              | Returns Boolean false.                                                                                                                |
| *RETURN\_TRUE*                               | Returns Boolean true.                                                                                                                 |

|                                              |                                                                                                                                                                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Macro                                        | Description                                                                                                                                                                                                       |
| *RETVAL\_RESOURCE(resource)*                 | Sets the return value to the specified resource.                                                                                                                                                                  |
| *RETVAL\_BOOL(bool)*                         | Sets the return value to the specified Boolean value.                                                                                                                                                             |
| *RETVAL\_NULL*                               | Sets the return value to NULL.                                                                                                                                                                                    |
| *RETVAL\_LONG(long)*                         | Sets the return value to the specified long.                                                                                                                                                                      |
| *RETVAL\_DOUBLE(double)*                     | Sets the return value to the specified double.                                                                                                                                                                    |
| *RETVAL\_STRING(string, duplicate)*          | Sets the return value to the specified string and duplicates it to Zend internal memory if desired (see also *RETURN\_STRING*).                                                                                   |
| *RETVAL\_STRINGL(string, length, duplicate)* | Sets the return value to the specified string and forces the length to become `length` (see also *RETVAL\_STRING*). This macro is faster and binary-safe, and should be used whenever the string length is known. |
| *RETVAL\_EMPTY\_STRING*                      | Sets the return value to an empty string.                                                                                                                                                                         |
| *RETVAL\_FALSE*                              | Sets the return value to Boolean false.                                                                                                                                                                           |
| *RETVAL\_TRUE*                               | Sets the return value to Boolean true.                                                                                                                                                                            |

Complex types such as arrays and objects can be returned by using <span
class="function">array\_init</span> and <span
class="function">object\_init</span>, as well as the corresponding hash
functions on `return_value`. Since these types cannot be constructed of
trivial information, there are no predefined macros for them.

### Printing Information

Often it's necessary to print messages to the output stream from your
module, just as <span class="function">print</span> would be used within
a script. PHP offers functions for most generic tasks, such as printing
warning messages, generating output for <span
class="function">phpinfo</span>, and so on. The following sections
provide more details. Examples of these functions can be found on the
CD-ROM.

#### <span class="function">zend\_printf</span>

<span class="function">zend\_printf</span> works like the standard <span
class="function">printf</span>, except that it prints to Zend's output
stream.

#### <span class="function">zend\_error</span>

<span class="function">zend\_error</span> can be used to generate error
messages. This function accepts two arguments; the first is the error
type (see `zend_errors.h`), and the second is the error message.

``` c
zend_error(E_WARNING, "This function has been called with empty arguments");
```

<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.error-messages" class="xref">Zend's Predefined Error Messages.</a>
shows a list of possible values (see
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.fig.warning-messages" class="link">below</a>).
These values are also referred to in `php.ini`. Depending on which error
type you choose, your messages will be logged.

|                         |                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Error                   | Description                                                                                                                        |
| **`E_ERROR`**           | Signals an error and terminates execution of the script immediately.                                                               |
| **`E_WARNING`**         | Signals a generic warning. Execution continues.                                                                                    |
| **`E_PARSE`**           | Signals a parser error. Execution continues.                                                                                       |
| **`E_NOTICE`**          | Signals a notice. Execution continues. Note that by default the display of this type of error messages is turned off in `php.ini`. |
| **`E_CORE_ERROR`**      | Internal error by the core; shouldn't be used by user-written modules.                                                             |
| **`E_COMPILE_ERROR`**   | Internal error by the compiler; shouldn't be used by user-written modules.                                                         |
| **`E_COMPILE_WARNING`** | Internal warning by the compiler; shouldn't be used by user-written modules.                                                       |

<img src="images/befd863081615f539082d9ff76bf7b39-zend.07-warning-messages.png" width="322" height="218" alt="Display of warning messages in the browser." />

#### Including Output in <span class="function">phpinfo</span>

After creating a real module, you'll want to show information about the
module in <span class="function">phpinfo</span> (in addition to the
module name, which appears in the module list by default). PHP allows
you to create your own section in the <span
class="function">phpinfo</span> output with the *ZEND\_MINFO()*
function. This function should be placed in the module descriptor block
(discussed earlier) and is always called whenever a script calls <span
class="function">phpinfo</span>.

PHP automatically prints a section in <span
class="function">phpinfo</span> for you if you specify the *ZEND\_MINFO*
function, including the module name in the heading. Everything else must
be formatted and printed by you.

Typically, you can print an HTML table header using <span
class="function">php\_info\_print\_table\_start</span> and then use the
standard functions <span
class="function">php\_info\_print\_table\_header</span> and <span
class="function">php\_info\_print\_table\_row</span>. As arguments, both
take the number of columns (as integers) and the column contents (as
strings).
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.phpinfo" class="xref">Source code and screenshot for output in phpinfo.</a>
shows a source example and its output. To print the table footer, use
<span class="function">php\_info\_print\_table\_end</span>.

**示例 \#13 Source code and screenshot for output in <span
class="function">phpinfo</span>.**

``` c
php_info_print_table_start();
php_info_print_table_header(2, "First column", "Second column");
php_info_print_table_row(2, "Entry in first row", "Another entry");
php_info_print_table_row(2, "Just to fill", "another row here");
php_info_print_table_end();
```

<img src="images/befd863081615f539082d9ff76bf7b39-zend.08-phpinfo-output.png" width="691" height="585" alt="Output of phpinfo()" />

#### Execution Information

You can also print execution information, such as the current file being
executed. The name of the function currently being executed can be
retrieved using the function <span
class="function">get\_active\_function\_name</span>. This function
returns a pointer to the function name and doesn't accept any arguments.
To retrieve the name of the file currently being executed, use <span
class="function">zend\_get\_executed\_filename</span>. This function
accesses the executor globals, which are passed to it using the
*TSRMLS\_C* macro. The executor globals are automatically available to
every function that's called directly by Zend (they're part of the
*INTERNAL\_FUNCTION\_PARAMETERS* described earlier in this chapter). If
you want to access the executor globals in another function that doesn't
have them available automatically, call the macro *TSRMLS\_FETCH()* once
in that function; this will introduce them to your local scope.

Finally, the line number currently being executed can be retrieved using
the function <span class="function">zend\_get\_executed\_lineno</span>.
This function also requires the executor globals as arguments. For
examples of these functions, see
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.exec-info" class="xref">Printing execution information.</a>.

**示例 \#14 Printing execution information.**

``` c
zend_printf("The name of the current function is %s&lt;br&gt;", get_active_function_name(TSRMLS_C));
zend_printf("The file currently executed is %s&lt;br&gt;", zend_get_executed_filename(TSRMLS_C));
zend_printf("The current line being executed is %i&lt;br&gt;", zend_get_executed_lineno(TSRMLS_C));
```

<img src="images/befd863081615f539082d9ff76bf7b39-zend.09-execution-info.png" width="477" height="268" alt="Printing execution information" />

### Startup and Shutdown Functions

Startup and shutdown functions can be used for one-time initialization
and deinitialization of your modules. As discussed earlier in this
chapter (see the description of the Zend module descriptor block), there
are module, and request startup and shutdown events.

The module startup and shutdown functions are called whenever a module
is loaded and needs initialization; the request startup and shutdown
functions are called every time a request is processed (meaning that a
file is being executed).

For dynamic extensions, module and request startup/shutdown events
happen at the same time.

Declaration and implementation of these functions can be done with
macros; see the earlier section "Declaration of the Zend Module Block"
for details.

### Calling User Functions

You can call user functions from your own modules, which is very handy
when implementing callbacks; for example, for array walking, searching,
or simply for event-based programs.

User functions can be called with the function <span
class="function">call\_user\_function\_ex</span>. It requires a hash
value for the function table you want to access, a pointer to an object
(if you want to call a method), the function name, return value, number
of arguments, argument array, and a flag indicating whether you want to
perform zval separation.

``` c
ZEND_API int call_user_function_ex(HashTable *function_table, zval *object,
zval *function_name, zval **retval_ptr_ptr,
int param_count, zval **params[],
int no_separation);
```

Note that you don't have to specify both `function_table` and `object`;
either will do. If you want to call a method, you have to supply the
object that contains this method, in which case <span
class="function">call\_user\_function</span>automatically sets the
function table to this object's function table. Otherwise, you only need
to specify `function_table` and can set `object` to *NULL*.

Usually, the default function table is the "root" function table
containing all function entries. This function table is part of the
compiler globals and can be accessed using the macro *CG*. To introduce
the compiler globals to your function, call the macro *TSRMLS\_FETCH*
once.

The function name is specified in a `zval` container. This might be a
bit surprising at first, but is quite a logical step, since most of the
time you'll accept function names as parameters from calling functions
within your script, which in turn are contained in `zval` containers
again. Thus, you only have to pass your arguments through to this
function. This `zval` must be of type *IS\_STRING*.

The next argument consists of a pointer to the return value. You don't
have to allocate memory for this container; the function will do so by
itself. However, you have to destroy this container (using <span
class="function">zval\_dtor</span>) afterward!

Next is the parameter count as integer and an array containing all
necessary parameters. The last argument specifies whether the function
should perform zval separation - this should always be set to *0*. If
set to *1*, the function consumes less memory but fails if any of the
parameters need separation.

<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.example.call-user-func" class="xref">Calling user functions.</a>
shows a small demonstration of calling a user function. The code calls a
function that's supplied to it as argument and directly passes this
function's return value through as its own return value. Note the use of
the constructor and destructor calls at the end - it might not be
necessary to do it this way here (since they should be separate values,
the assignment might be safe), but this is bulletproof.

**示例 \#15 Calling user functions.**

``` c
zval **function_name;
zval *retval;

if((ZEND_NUM_ARGS() != 1) || (zend_get_parameters_ex(1, &function_name) != SUCCESS))
{
    WRONG_PARAM_COUNT;
}

if((*function_name)->type != IS_STRING)
{
    zend_error(E_ERROR, "Function requires string argument");
}

TSRMSLS_FETCH();

if(call_user_function_ex(CG(function_table), NULL, *function_name, &retval, 0, NULL, 0) != SUCCESS)
{
    zend_error(E_ERROR, "Function call failed");
}

zend_printf("We have %i as type\n", retval->type);

*return_value = *retval;
zval_copy_ctor(return_value);
zval_ptr_dtor(&retval);
```

``` c
<?php

dl("call_userland.so");

function test_function()
{
    echo "We are in the test function!\n";
    return 'hello';
}

$return_value = call_userland("test_function");

echo "Return value: '$return_value'";
?>
```

以上例程会输出：

    We are in the test function!
    We have 3 as type
    Return value: 'hello'

### Initialization File Support

PHP 4 features a redesigned initialization file support. It's now
possible to specify default initialization entries directly in your
code, read and change these values at runtime, and create message
handlers for change notifications.

To create an .ini section in your own module, use the macros
*PHP\_INI\_BEGIN()* to mark the beginning of such a section and
*PHP\_INI\_END()* to mark its end. In between you can use
*PHP\_INI\_ENTRY()* to create entries.

``` c
PHP_INI_BEGIN()
PHP_INI_ENTRY("first_ini_entry",  "has_string_value", PHP_INI_ALL, NULL)
PHP_INI_ENTRY("second_ini_entry", "2",                PHP_INI_SYSTEM, OnChangeSecond)
PHP_INI_ENTRY("third_ini_entry",  "xyz",              PHP_INI_USER, NULL)
PHP_INI_END()
```

The *PHP\_INI\_ENTRY()* macro accepts four parameters: the entry name,
the entry value, its change permissions, and a pointer to a
change-notification handler. Both entry name and value must be specified
as strings, regardless of whether they really are strings or integers.

The permissions are grouped into three sections:*PHP\_INI\_SYSTEM*
allows a change only directly in the `php.ini` file; *PHP\_INI\_USER*
allows a change to be overridden by a user at runtime using additional
configuration files, such as `.htaccess`; and *PHP\_INI\_ALL* allows
changes to be made without restrictions. There's also a fourth level,
*PHP\_INI\_PERDIR*, for which we couldn't verify its behavior yet.

The fourth parameter consists of a pointer to a change-notification
handler. Whenever one of these initialization entries is changed, this
handler is called. Such a handler can be declared using the
*PHP\_INI\_MH* macro:

``` c
PHP_INI_MH(OnChangeSecond);             // handler for ini-entry "second_ini_entry"

// specify ini-entries here

PHP_INI_MH(OnChangeSecond)
{

    zend_printf("Message caught, our ini entry has been changed to %s&lt;br&gt;", new_value);

    return(SUCCESS);

}
```

The new value is given to the change handler as string in the variable
`new_value`. When looking at the definition of *PHP\_INI\_MH*, you
actually have a few parameters to use:

``` c
#define PHP_INI_MH(name) int name(php_ini_entry *entry, char *new_value,
                                  uint new_value_length, void *mh_arg1,
                                  void *mh_arg2, void *mh_arg3)
```

All these definitions can be found in `php_ini.h`. Your message handler
will have access to a structure that contains the full entry, the new
value, its length, and three optional arguments. These optional
arguments can be specified with the additional macros *PHP\_INI\_ENTRY1*
(allowing one additional argument), *PHP\_INI\_ENTRY2* (allowing two
additional arguments), and *PHP\_INI\_ENTRY3* (allowing three additional
arguments).

The change-notification handlers should be used to cache initialization
entries locally for faster access or to perform certain tasks that are
required if a value changes. For example, if a constant connection to a
certain host is required by a module and someone changes the hostname,
automatically terminate the old connection and attempt a new one.

Access to initialization entries can also be handled with the macros
shown in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.table.ini-macros" class="xref">Macros to Access Initialization Entries in PHP</a>.

|                         |                                                                                                                                                                                       |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Macro                   | Description                                                                                                                                                                           |
| *INI\_INT(name)*        | Returns the current value of entry *name* as integer (long).                                                                                                                          |
| *INI\_FLT(name)*        | Returns the current value of entry *name* as float (double).                                                                                                                          |
| *INI\_STR(name)*        | Returns the current value of entry *name* as string. *Note:* This string is not duplicated, but instead points to internal data. Further access requires duplication to local memory. |
| *INI\_BOOL(name)*       | Returns the current value of entry *name* as Boolean (defined as `zend_bool`, which currently means `unsigned char`).                                                                 |
| *INI\_ORIG\_INT(name)*  | Returns the original value of entry *name* as integer (long).                                                                                                                         |
| *INI\_ORIG\_FLT(name)*  | Returns the original value of entry *name* as float (double).                                                                                                                         |
| *INI\_ORIG\_STR(name)*  | Returns the original value of entry *name* as string. Note: This string is not duplicated, but instead points to internal data. Further access requires duplication to local memory.  |
| *INI\_ORIG\_BOOL(name)* | Returns the original value of entry *name* as Boolean (defined as `zend_bool`, which currently means `unsigned char`).                                                                |

Finally, you have to introduce your initialization entries to PHP. This
can be done in the module startup and shutdown functions, using the
macros *REGISTER\_INI\_ENTRIES()* and *UNREGISTER\_INI\_ENTRIES()*:

``` c
ZEND_MINIT_FUNCTION(mymodule)
{

    REGISTER_INI_ENTRIES();

}

ZEND_MSHUTDOWN_FUNCTION(mymodule)
{

    UNREGISTER_INI_ENTRIES();

}
```

### Where to Go from Here

You've learned a lot about PHP. You now know how to create dynamic
loadable modules and statically linked extensions. You've learned how
PHP and Zend deal with internal storage of variables and how you can
create and access these variables. You know quite a set of tool
functions that do a lot of routine tasks such as printing informational
texts, automatically introducing variables to the symbol table, and so
on.

Even though this chapter often had a mostly "referential" character, we
hope that it gave you insight on how to start writing your own
extensions. For the sake of space, we had to leave out a lot; we suggest
that you take the time to study the header files and some modules
(especially the ones in the `ext/standard` directory and the MySQL
module, as these implement commonly known functionality). This will give
you an idea of how other people have used the API functions -
particularly those that didn't make it into this chapter.

### Reference: Some Configuration Macros

#### `config.m4`

The file `config.m4` is processed by `buildconf` and must contain all
the instructions to be executed during configuration. For example, these
can include tests for required external files, such as header files,
libraries, and so on. PHP defines a set of macros that can be used in
this process, the most useful of which are described in
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.m4-macros" class="xref">M4 Macros for config.m4</a>.

|                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Macro                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                        |
| *AC\_MSG\_CHECKING(message)*                                              | Prints a "checking \<message\>" text during `configure`.                                                                                                                                                                                                                                                                                                                                           |
| *AC\_MSG\_RESULT(value)*                                                  | Gives the result to *AC\_MSG\_CHECKING*; should specify either *yes* or *no* as `value`.                                                                                                                                                                                                                                                                                                           |
| *AC\_MSG\_ERROR(message)*                                                 | Prints `message` as error message during `configure` and aborts the script.                                                                                                                                                                                                                                                                                                                        |
| *AC\_DEFINE(name,value,description)*                                      | Adds *\#define* to `php_config.h` with the value of `value` and a comment that says `description` (this is useful for conditional compilation of your module).                                                                                                                                                                                                                                     |
| *AC\_ADD\_INCLUDE(path)*                                                  | Adds a compiler include path; for example, used if the module needs to add search paths for header files.                                                                                                                                                                                                                                                                                          |
| *AC\_ADD\_LIBRARY\_WITH\_PATH(libraryname,librarypath)*                   | Specifies an additional library to link.                                                                                                                                                                                                                                                                                                                                                           |
| *AC\_ARG\_WITH(modulename,description,unconditionaltest,conditionaltest)* | Quite a powerful macro, adding the module with `description` to the `configure --help` output. PHP checks whether the option *--with-\<modulename\>* is given to the `configure` script. If so, it runs the script *unconditionaltest* (for example, *--with-myext=yes*), in which case the value of the option is contained in the variable `$withval`. Otherwise, it executes *conditionaltest*. |
| *PHP\_EXTENSION(modulename, \[shared\])*                                  | This macro is a *must* to call for PHP to configure your extension. You can supply a second argument in addition to your module name, indicating whether you intend compilation as a shared module. This will result in a definition at compile time for your source as *COMPILE\_DL\_\<modulename\>*.                                                                                             |

### API Macros

A set of macros was introduced into Zend's API that simplify access to
`zval` containers (see
<a href="/internals2/ze1/zendapi.html#internals2.ze1.zendapi.tab.api-macros" class="xref">API Macros for Accessing zval Containers</a>).

|                           |                          |
|---------------------------|--------------------------|
| Macro                     | Refers to                |
| *Z\_LVAL(zval)*           | `(zval).value.lval`      |
| *Z\_DVAL(zval)*           | `(zval).value.dval`      |
| *Z\_STRVAL(zval)*         | `(zval).value.str.val`   |
| *Z\_STRLEN(zval)*         | `(zval).value.str.len`   |
| *Z\_ARRVAL(zval)*         | `(zval).value.ht`        |
| *Z\_LVAL\_P(zval)*        | `(*zval).value.lval`     |
| *Z\_DVAL\_P(zval)*        | `(*zval).value.dval`     |
| *Z\_STRVAL\_P(zval\_p)*   | `(*zval).value.str.val`  |
| *Z\_STRLEN\_P(zval\_p)*   | `(*zval).value.str.len`  |
| *Z\_ARRVAL\_P(zval\_p)*   | `(*zval).value.ht`       |
| *Z\_LVAL\_PP(zval\_pp)*   | `(**zval).value.lval`    |
| *Z\_DVAL\_PP(zval\_pp)*   | `(**zval).value.dval`    |
| *Z\_STRVAL\_PP(zval\_pp)* | `(**zval).value.str.val` |
| *Z\_STRLEN\_PP(zval\_pp)* | `(**zval).value.str.len` |
| *Z\_ARRVAL\_PP(zval\_pp)* | `(**zval).value.ht`      |
