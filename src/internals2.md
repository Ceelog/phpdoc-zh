PHP 核心：骇客指南
==================

**目录**

-   [序言](/internals2/preface.html)
-   [内存管理](/internals2/memory.html)
    -   [内存管理基础](/internals2/memory/management.html)
    -   [数据持久化](/internals2/memory/persistence.html)
    -   [线程安全的资源管理器](/internals2/memory/TSRM.html)
-   [变量的使用](/internals2/variables.html)
    -   [介绍](/internals2/variables/intro.html)
    -   [创建变量并设置值](/internals2/variables/creating.html)
-   [函数的编写](/internals2/funcs.html)
-   [类和对象的使用](/internals2/objects.html)
-   [资源的使用](/internals2/resources.html)
-   [INI 设置的使用](/internals2/ini.html)
-   [流的使用](/internals2/streams.html)
-   ["counter" 扩展 - 一个连续的实例](/internals2/counter.html)
    -   [安装／配置](/internals2/counter/setup.html)
    -   [预定义常量](/internals2/counter/constants.html)
    -   [范例](/internals2/counter/examples.html)
    -   [Counter](/internals2/counter/counter-class.html) — Counter 类
    -   [Basic](/internals2/counter/basic-interface.html) — 简单接口
    -   [Extended](/internals2/counter/extended-interface.html) —
        扩展接口
-   [PHP 5 构建系统](/internals2/buildsys.html)
    -   [PHP 扩展开发构建](/internals2/buildsys/environment.html)
    -   [ext\_skel 脚本](/internals2/buildsys/skeleton.html)
    -   [与 UNIX 构建系统交互:
        config.m4](/internals2/buildsys/configunix.html)
    -   [使用 Windows
        构建系统：config.w32](/internals2/buildsys/configwin.html)
-   [扩展的结构](/internals2/structure.html)
    -   [组成扩展的文件](/internals2/structure/files.html)
    -   [Basic constructs](/internals2/structure/basics.html)
    -   [The zend\_module
        structure](/internals2/structure/modstruct.html)
    -   [Extension globals](/internals2/structure/globals.html)
    -   [Life cycle of an
        extension](/internals2/structure/lifecycle.html)
    -   [Testing an extension](/internals2/structure/tests.html)
-   [PDO 驱动](/internals2/pdo.html)
    -   [前提条件](/internals2/pdo/prerequisites.html)
    -   [配置与管理](/internals2/pdo/preparation.html)
    -   [Fleshing out your skeleton](/internals2/pdo/implementing.html)
    -   [Building](/internals2/pdo/building.html)
    -   [Testing](/internals2/pdo/testing.html)
    -   [Packaging and distribution](/internals2/pdo/packaging.html)
    -   [pdo\_dbh\_t definition](/internals2/pdo/pdo-dbh-t.html)
    -   [pdo\_stmt\_t definition](/internals2/pdo/pdo-stmt-t.html)
    -   [Constants](/internals2/pdo/constants.html)
    -   [Error handling](/internals2/pdo/error-handling.html)
-   [扩展相关 FAQ](/internals2/faq.html)
-   [Zend Engine 2 API 参考](/internals2/apiref.html)
-   [Zend Engine 2 操作码列表](/internals2/opcodes.html)
    -   [Opcode Descriptions and
        Examples](/internals2/opcodes/list.html)
-   [Zend Engine 1](/internals2/ze1.html)
    -   [旧的介绍](/internals2/ze1/intro.html)
    -   [Streams API for PHP Extension
        Authors](/internals2/ze1/streams.html)
    -   [Zend API：深入 PHP 内核](/internals2/ze1/zendapi.html)
    -   [TSRM API](/internals2/ze1/tsrm.html)
