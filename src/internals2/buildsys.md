PHP 5 构建系统
==============

**目录**

-   [PHP 扩展开发构建](/internals2/buildsys/environment.html)
-   [ext\_skel 脚本](/internals2/buildsys/skeleton.html)
-   [与 UNIX 构建系统交互:
    config.m4](/internals2/buildsys/configunix.html)
-   [使用 Windows
    构建系统：config.w32](/internals2/buildsys/configwin.html)

有了在 PHP 5
中的所有功能及灵活性，不用惊奇构建系统由几千个文件组成，有超过一百万行源代码。同样别惊奇构建系统管理如此之多数据的必要性。此章节描述了如何着手开发
PHP 扩展， 扩展在 PHP 源代码树中的布局，以及扩展如何与构建系统对接。
