组成扩展的文件
--------------

不管是通过手工，通过**ext\_skel** ，还是通过另外的扩展生成器，例如
<a href="http://codegenerators.php-baustelle.de/" class="link external">» CodeGen</a>，所有的扩展都会有至少四个文件：

`config.m4`  
UNIX 构建系统配置 (见
<a href="/internals2/buildsys/configunix.html" class="xref">与 UNIX 构建系统交互: config.m4</a>)

`config.w32`  
Windows 构建系统配置 (见
<a href="/internals2/buildsys/configwin.html" class="xref">使用 Windows 构建系统：config.w32</a>)

`php_counter.h`  
当将扩展作为静态模块构建并放入 PHP 二进制包时，构建系统要求用 *php\_*
加扩展的名称命名的头文件包含一个对扩展模块结构的指针定义。就象其他头文件，此文件经常包含附加的宏、原型和全局量。

`counter.c`  
主要的扩展源文件。按惯例，此文件名就是扩展的名称，但不是必需的。此文件包含模块结构定义、INI
条目、管理函数、用户空间函数和其它扩展所需的内容。

构建系统的文件在别处讨论，本节关注于其余的部分。扩展应包含任意数量的头文件、源文件、单元测试和其他支持文件，此四个文件仅够组成最小的扩展。counter
扩展的文件列表如下所示：

**示例 \#1 counter 扩展中的文件，未特别排序**

    ext/
     counter/
      .cvsignore
      config.m4
      config.w32
      counter_util.h
      counter_util.c
      php_counter.h
      counter.c
      package.xml
      CREDITS
      tests/
       critical_function_001.phpt
       critical_function_002.phpt
       optional_function_001.phpt
       optional_function_002.phpt

### 非源文件

`.cvsignore` 文件用于已检入一个 PHP **CVS** 资源库（通常是
<a href="https://pecl.php.net/" class="link external">» PECL</a>）的扩展，由
**ext\_skel** 生成的这个文件内容如下：

``` cvsignore
.deps
*.lo
*.la
```

这几行告诉 **CVS** 要忽略由 PHP
构建系统生成的临时文件。这只是惯例，可以被完全省略掉且无不良影响。

`CREDITS` 文件用纯文本格式列出了扩展的贡献者和（或
）维护者。此文件的主要用途是为已捆绑的扩展生成被 <span
class="function">phpcredits</span>
所使用的荣誉信息。按惯例，文件的第一行应保存扩展的名称，第二行是用逗号分隔的贡献者名单。贡献者通常是按其贡献物的时间顺序排序。例如，在
<a href="https://pecl.php.net/" class="link external">» PECL</a>
包中，此信息已经维护在 `package.xml`
中了。这就是可以被省略且无不良影响的其他文件。

`package.xml` 文件是基于
<a href="https://pecl.php.net/" class="link external">» PECL</a>
的扩展特有的，是一个元信息文件，记录了扩展的信赖关系、作者、安装需求和其他有价值的信息。对于不是基于
<a href="https://pecl.php.net/" class="link external">» PECL</a>
的扩展来说，此文件就无关紧要了。
