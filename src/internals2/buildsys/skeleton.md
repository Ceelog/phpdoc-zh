ext\_skel 脚本
--------------

PHP
扩展由几个文件组成，这些文件对所有扩展来说都是通用的。不同扩展之间，这些文件的很多细节是相似的，只是要费力去复制每个文件的内容。幸运的是，有脚本可以做所有的初始化工作，名为
**ext\_skel**，自 PHP 4.0 起与其一起分发。

不带参数运行 **ext\_skel** 在 PHP 5.2.2 中会产生以下输出：

    php-5.2.2/ext$ ./ext_skel 
    ./ext_skel --extname=module [--proto=file] [--stubs=file] [--xml[=file]]
               [--skel=dir] [--full-xml] [--no-help]

      --extname=module   module is the name of your extension
      --proto=file       file contains prototypes of functions to create
      --stubs=file       generate only function stubs in file
      --xml              generate xml documentation to be added to phpdoc-cvs
      --skel=dir         path to the skeleton directory
      --full-xml         generate xml documentation for a self-contained extension
                         (not yet implemented)
      --no-help          don't try to be nice and create comments in the code
                         and helper functions to test if the module compiled

通常来说，开发一个新扩展时，仅需关注的参数是 *--extname* 和
*--no-help*。除非已经熟悉扩展的结构，*不*要想去使用 *--no-help*;
指定此参数会造成 **ext\_skel** 不会在生成的文件里省略很多有用的注释。

剩下的 *--extname* 会将扩展的名称传给 **ext\_skel**。"name"
是一个全为小写字母的标识符，仅包含字母和下划线，在 PHP 发行包的 `ext/`
文件夹下是唯一的。

*--proto* 选项允许开发人员指定一个头文件，由此创建一系列 PHP
函数，表面上看就是要开发基于一个函数库的扩展，但对大多数头现代的文件来说很少能起作用。如果用
`zlib.h` 头文件来做测试，就会导致在 **ext\_skel**
的输出文件中存在大量的空的和无意义的原型文件。*--xml* 和 *--full-xml*
选项当前完全不起作用。*--skel*
选项可用于指定用一套修改过的框架文件来工作，这是本节范围之外的话题了。
