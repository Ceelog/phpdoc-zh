配置与管理
----------

### 源目录布局

一个典型的 PDO 驱动程序源目录布局如下所示，其中 *SKEL*
表示该驱动程序要连接到的数据库的名称的缩写形式。

    pdo_SKEL/          
      config.m4                  # unix 构建脚本
      config.w32                 # win32 构建脚本
      CREDITS
      package.xml                # 有关包的元信息
      pdo_SKEL.c                 # 标准 PHP 扩展
      php_pdo_SKEL.h
      php_pdo_SKEL_int.h         # 驱动程序私有头文件
      SKEL_dbh.c                 # 包含 PDO 的驱动程序接口的实现
      SKEL_stmt.c                # 包含 PDO 声明接口的实现
      tests/

稍后在本文档中阐述这些文件的内容。

### 创建一个基本框架

最简单的方法就是使用 PHP 目录树中的 `ext` 目录下的 **ext\_skel** Shell
脚本。这将生成包含很多上面列出的文件的基本框架目录。通过执行下面命令来完成:

    ./ext_skel --extname=pdo_SKEL

这将生成一个名为pdo\_SKEL包含基本框架文件的目录，目录名称可以自定义。该目录可以移动到PHP扩展目录之外。PDO
是 PECL
的一个扩展，不应该包括在标准扩展目录中。只要你有过PHP和PDO的安装，你就会想到从其它目录创建。

### 标准包含文件

#### 创建特定头文件

头文件 congfig.h
是由配置进程根据系统平台及其使用的驱动自动生成的。如果该头文件存在，HAVE\_CONFIG\_H
编译器变量将被设置。此变量应测试，如果设置，该文件的config.h应该被包含在编译单元内。

#### PHP 头文件

以下标准的公共的 PHP 头文件应包括在每个源模块中：

1.  php.h

2.  php\_ini.h

3.  ext/standard/info.h

#### PDO 接口头文件

以下标准的公共的 PDO 头文件也应该包括在每个源模块中：

pdo/php\_pdo.h  
该头文件包含了主驱动中初始值和关闭功能的定心及PDO全局变量的定义。

pdo/php\_pdo\_driver.h  
该头文件包含了用来编写PDO驱动程序的类型和API。它还包含了调用返回到PDO层的方法签名和注册/注销PDO驱动程序。最重要的是，此头文件包含
PDO 的数据库句柄和语句的类型定义。驱动程序处理的两种主要结构 pdo\_dbh\_t
和 pdo\_stmt\_t，更详细的描述请查阅附录 A 和 B。

#### 驱动程序特定的头文件

典型的PDO的驱动程序有两个特定于数据库实现头文件。这并不排除使用上更多的取决于实现。按照惯例，下面列举了这两个头文件:

php\_pdo\_SKEL.h  
这实际上是一个功能与内容和前面定义的专门为您的数据库定制的pdo/php\_pdo.h完全相同的头文件。如果你的驱动程序需要使用全局变量，那么他们应使用ZEND\_BEGIN\_MODULE\_GLOBALS
和 ZEND\_END\_MODULE\_GLOBALS宏来定义。
然后用宏来访问这些变量。这些宏通常被命名为PDO\_SKEL\_G(v)，其中v表示被访问的全局变量。更多信息，请查阅Zend
programmer文档。

php\_pdo\_SKEL\_int.h  
该头文件通常包括特定于驱动程序实现的类型定义和函数申明。此外，它还包含pdo\_SKEL\_handle
和
pdo\_SKEL\_stmt结构中DB的具体定义。这些都是被driver\_data所引用的句柄和语句结构成员的私有数据结构。

#### 可选头文件

根据实际情况，一个特定的驱动程序可能需要包括下面头文件:

``` c
#include <zend_exceptions.h>
```
