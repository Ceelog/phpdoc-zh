与 UNIX 构建系统交互: config.m4
-------------------------------

扩展的 `config.m4` 文件告诉 UNIX 构建系统哪些扩展 `configure`
选项是支持的，你需要哪些扩展库，以及哪些源文件要编译成它的一部分。对所有经常使用的
autoconf 宏，包括 PHP 特定的及 autoconf 内建的，请查看
<a href="/internals2/apiref.html" class="xref">Zend Engine 2 API 参考</a>
章节。

**小贴士**

当开发 PHP 扩展时，*强烈*建议安装 **autoconf** 2.13
版，尽管用更新的版本可使用。2.13 版被认为是在 **autoconf**
中可用性，适用性及用户基础等方面最好的版本。使用最新版本有时会与所期望的
**configure** 输出在样式上有所不同。

**示例 \#1 config.m4 文件举例**

``` autoconf
dnl $Id$
dnl config.m4 for extension example
```

``` autoconf
PHP_ARG_WITH(example, for example support,
[  --with-example[=FILE]       Include example support. File is the optional path to example-config])
PHP_ARG_ENABLE(example-debug, whether to enable debugging support in example,
[  --enable-example-debug        example: Enable debugging support in example], no, no)
PHP_ARG_WITH(example-extra, for extra libraries for example,
[  --with-example-extra=DIR      example: Location of extra libraries for example], no, no)

dnl 检测扩展是否已启用
if test "$PHP_EXAMPLE" != "no"; then
  
  dnl 检测 example-config。首先尝试所给出的路径，然后在 $PATH 中寻找
  AC_MSG_CHECKING([for example-config])
  EXAMPLE_CONFIG="example-config"
  if test "$PHP_EXAMPLE" != "yes"; then
    EXAMPLE_PATH=$PHP_EXAMPLE
  else
    EXAMPLE_PATH=`$php_shtool path $EXAMPLE_CONFIG`
  fi
  
  dnl 如果找到可用的 example-config，就使用它
  if test -f "$EXAMPLE_PATH" && test -x "$EXAMPLE_PATH" && $EXAMPLE_PATH --version > /dev/null 2>&1; then
    AC_MSG_RESULT([$EXAMPLE_PATH])
    EXAMPLE_LIB_NAME=`$EXAMPLE_PATH --libname`
    EXAMPLE_INCDIRS=`$EXAMPLE_PATH --incdirs`
    EXAMPLE_LIBS=`$EXAMPLE_PATH --libs`
    
    dnl 检测扩展库是否工作正常
    PHP_CHECK_LIBRARY($EXAMPLE_LIB_NAME, example_critical_function,
    [
      dnl 添加所需的 include 目录
      PHP_EVAL_INCLINE($EXAMPLE_INCDIRS)
      dnl 添加所需的扩展库及扩展库所在目录
      PHP_EVAL_LIBLINE($EXAMPLE_LIBS, EXAMPLE_SHARED_LIBADD)
    ],[
      dnl 跳出
      AC_MSG_ERROR([example library not found. Check config.log for more information.])
    ],[$EXAMPLE_LIBS]
    )
  else
    dnl 没有可用的 example-config，跳出
    AC_MSG_RESULT([not found])
    AC_MSG_ERROR([Please check your example installation.])
  fi
  
  dnl 检测是否启用调试
  if test "$PHP_EXAMPLE_DEBUG" != "no"; then
    dnl 是，则设置 C 语言宏指令
    AC_DEFINE(USE_EXAMPLE_DEBUG,1,[Include debugging support in example])
  fi
  
  dnl 检测额外的支持
  if test "$PHP_EXAMPLE_EXTRA" != "no"; then
    if test "$PHP_EXAMPLE_EXTRA" == "yes"; then
      AC_MSG_ERROR([You must specify a path when using --with-example-extra])
    fi
    
    PHP_CHECK_LIBRARY(example-extra, example_critical_extra_function,
    [
      dnl 添加所需路径
      PHP_ADD_INCLUDE($PHP_EXAMPLE_EXTRA/include)
      PHP_ADD_LIBRARY_WITH_PATH(example-extra, $PHP_EXAMPLE_EXTRA/lib, EXAMPLE_SHARED_LIBADD)
      AC_DEFINE(HAVE_EXAMPLEEXTRALIB,1,[Whether example-extra support is present and requested])
      EXAMPLE_SOURCES="$EXAMPLE_SOURCES example_extra.c"
    ],[
      AC_MSG_ERROR([example-extra lib not found. See config.log for more information.])
    ],[-L$PHP_EXAMPLE_EXTRA/lib]
    )
  fi
  
  dnl 最后，将扩展及其所需文件等信息传给构建系统
  PHP_NEW_EXTENSION(example, example.c $EXAMPLE_SOURCES, $ext_shared)
  PHP_SUBST(EXAMPLE_SHARED_LIBADD)
fi
```

### autoconf 语法简介

`config.m4` 文件使用 GNU **autoconf**
语法编写。简而言之，就是用强大的宏语言增强的 shell 脚本。注释用字符串
*dnl* 分隔，字符串则放在左右方括号中间（例如，*\[* 和
*\]*）。字符串可按需要多次嵌套引用。完整的语法参考可参见位于
<a href="http://www.gnu.org/software/autoconf/manual/" class="link external">» http://www.gnu.org/software/autoconf/manual/</a>
的 **autoconf** 手册。

### PHP\_ARG\_\*: 赋予用户可选项

在以上的 `config.m4` 例子中，两条注释后，最先见到的 3 行代码，使用了
<span class="function">PHP\_ARG\_WITH</span> 和 <span
class="function">PHP\_ARG\_ENABLE</span>。这些给 **configure**
提供了可选项，和在运行 **./configure --help**
时显示的帮助文本。就象名称所暗示的，其两者的不同点在于是创建
**--with-\*** 选项还是 **--enable-\***
选项。每个扩展应提供至少一个以上的选项以及扩展名称，以便用户可选择是否将扩展构建至
PHP 中。按惯例，<span class="function">PHP\_ARG\_WITH</span>
用于取得参数的选项，例如扩展所需库或程序的位置；而 <span
class="function">PHP\_ARG\_ENABLE</span> 用于代表简单标志的选项。

**示例 \#2 configure 输出举例**

    $ ./configure --help
    ...
      --with-example[=FILE]       Include example support. FILE is the optional path to example-config
      --enable-example-debug        example: Enable debugging support in example
      --with-example-extra=DIR      example: Location of extra libraries for example
    ...

    $ ./configure --with-example=/some/library/path/example-config --disable-example-debug --with-example-extra=/another/library/path
    ...
    checking for example support... yes
    checking whether to enable debugging support in example... no
    checking for extra libraries for example... /another/library/path
    ...

> **Note**:
>
> 在调用 **configure** 时，不管选项在命令行中的顺序如何，都会按在
> `config.m4` 中指定的顺序进行检测。

### 处理用户选择

`config.m4`
可给用户提供一些做什么的选择，现在就是做出选择的时候了。在上例中，三个选项在未指定时显然默认为
"no"。习惯上，最好用此值作为用于启用扩展的选项的默认值，为了扩展与 PHP
分开构建则用 **phpize** 覆盖此值，而要构建在 PHP
中时则不应被默认值将扩展空间弄乱。处理这三个选项的代码要复杂得多。

#### 处理 --with-example\[=FILE\] 选项

首先检测是否设置了 **--with-example\[=FILE\]**
选项。如此选项未被指定，或使用否定的格式（**--without-example**），或赋值为
"no"
时，它会控制整个扩展的含有物其他任何事情都不会发生。在上面的例子中所指定的值为
*/some/library/path/example-config*，所以第一个 test 成功了。

接下来，代码调用 <span
class="function">AC\_MSG\_CHECKING</span>，这是一个 **autoconf**
宏，输出一行标准的如 "checking for ..." 的信息，并检测用户假定的
**example-config** 是否是一个明确的路径。在这个例子中，*PHP\_EXAMPLE*
所取到的值为 */some/library/path/example-config*，现已复制到
EXAMPLE\_PATH 变量中了。只有用户指定了 **--with-example**，才会执行代码
**$php\_shtool path $EXAMPLE\_CONFIG**，尝试使用用户当前的 *PATH*
环境变量推测 **example-config** 的位置。无论如何，下一步都是检测所选的
*EXAMPLE\_PATH*
是否是正常文件，是否可执行，及是否执行成功。如成功，则调用 <span
class="function">AC\_MSG\_RESULT</span>，结束由 <span
class="function">AC\_MSG\_CHECKING</span> 开始的输出行。否则，调用 <span
class="function">AC\_MSG\_ERROR</span>，打印所给的信息并立即中断执行
**configure**。

代码现在执行几次 **example-config**
以确定一些站点特定的配置信息。下一步调用的是 <span
class="function">PHP\_CHECK\_LIBRARY</span>，这是 PHP
构建系统提供的一个宏，包装了 **autoconf** 的 <span
class="function">AC\_CHECK\_LIB</span> 函数。<span
class="function">PHP\_CHECK\_LIBRARY</span>
尝试编译、链接和执行程序，在第一个参数指定的库中调用由第二个参数指定的符号，使用第五个参数给出的字符串作为额外的链接选项。如果尝试成功了，则运行第三个参数所给出的脚本。此脚本从
**example-config**
所提供的原始的选项字符串中取出头文件路径、库文件路径和库名称，告诉 PHP
构建系统。如果尝试失败，脚本则运行第四个参数中的脚本。此时调用 <span
class="function">AC\_MSG\_ERROR</span> 来中断程序执行。

#### 处理 --enable-example-debug 选项

处理 **--enable-example-debug**
很简单。只简单地检测其真实值。如果检测成功，则调用 <span
class="function">AC\_DEFINE</span> 使 C 语言宏指令 *USE\_EXAMPLE\_DEBUG*
可用于扩展的源代码。第三个参数是给 `config.h`
的注释字符串，通常可放心的留空。

#### 处理 --with-example-extra=DIR 选项

对于此例子来说，由 **--with-example-extra=DIR**
选项所请求的假定的“额外”功能操作不会与假定的 **example-config**
程序共享，也没有默认的搜索路径。因此，用户需要在所需的库之前提供设置程序。有点不象现实中的扩展，在这里的设置仅仅起说明性的作用。

代码开始用已熟知的方式来检测 *PHP\_EXAMPLE\_EXTRA*
的真实值。如果所提供的为否定形式，则不会进行其他处理，用户也不会请求额外的功能。如果所提供的为未提供参数的肯定形式，则调用
<span class="function">AC\_MSG\_ERROR</span> 中止处理。下一步则再次调用
<span
class="function">PHP\_CHECK\_LIBRARY</span>。这一次，因为没有提供预定义编译选项，<span
class="function">PHP\_ADD\_INCLUDE</span> 和 <span
class="function">PHP\_ADD\_LIBRARY\_WITH\_PATH</span>
用于构建额外功能所需的头文件路径、库文件路径和库标志。也调用 <span
class="function">AC\_DEFINE</span>
来指示所请求的额外功能代码是可用的，设置变量来告诉以后的代码，有额外的源代码要构建。如果检测失败，则调用所熟悉的
<span
class="function">AC\_MSG\_ERROR</span>。另一种不同的处理失败的方式是更换为调用
<span class="function">AC\_MSG\_WARNING</span>，例如：

``` autoconf
AC_MSG_WARNING([example-extra lib not found. example will be built without extra functionality.])
```

上例中，**configure**
会打印一段警告信息而不是错误，且继续处理。用哪种方式处理失败留给扩展开发人员在设计时决定。

### 告诉构建系统要做什么

有了所需的头文件和特定的库，有了全部选项处理代码及宏定义，还有一件事要做：必须告诉构建系统去构建扩展本身和被其用到的文件。为了做这些，则要调用
<span class="function">PHP\_NEW\_EXTENSION</span>
宏。第一个参数是扩展的名称，和包含它的目录同名。第二个参数是做为扩展的一部分的所有源文件的列表。参见
<span class="function">PHP\_ADD\_BUILD\_DIR</span>
以获取将在子目录中源文件添加到构建过程的相关信息。第三个参数总是
*$ext\_shared*， 当为了 **--with-example\[=FILE\]** 而调用 <span
class="function">PHP\_ARG\_WITH</span>时，由 **configure**
决定参数的值。第四个参数指定一个“SAPI 类”，仅用于专门需要 CGI 或 CLI
SAPI 的扩展。其他情况下应留空。第五个参数指定了构建时要加入 *CFLAGS*
的标志列表。第六个参数是一个布尔值，为 "yes" 时会强迫整个扩展使用 *$CXX*
代替 *$CC* 来构建。第三个以后的所有参数都是可选的。最后，调用 <span
class="function">PHP\_SUBST</span> 来启用扩展的共享构建。参见
<a href="/internals2/faq.html" class="xref">扩展相关 FAQ</a>
以获取更多有关禁用共享方式下构建扩展的信息。

### counter 扩展的 config.m4 文件

以前编写的 counter 扩展有一个比上面所述更简单的 `config.m4`
文件，它不使用很多构建系统的特性。对不使用外部的或绑定的库的扩展来说，这是一个比较好的操作方式。

**示例 \#3 counter 的 config.m4 文件**

``` autoconf
dnl
```

``` autoconf
$
```

``` autoconf
Id$
dnl config.m4 for extension counter

PHP_ARG_ENABLE(counter, for counter support,
[  --enable-counter            Include counter support])

dnl Check whether the extension is enabled at all
if test "$PHP_COUNTER" != "no"; then
  dnl Finally, tell the build system about the extension and what files are needed
  PHP_NEW_EXTENSION(counter, counter.c counter_util.c, $ext_shared)
  PHP_SUBST(COUNTER_SHARED_LIBADD)
fi
```
