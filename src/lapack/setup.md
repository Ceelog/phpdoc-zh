安装／配置
==========

**目录**

-   [需求](/lapack/setup.html#需求)
-   [安装](/lapack/setup.html#安装)
-   [运行时配置](/lapack/setup.html#运行时配置)
-   [资源类型](/lapack/setup.html#资源类型)

需求
----

Lapack requires the LAPACK and LAPACKE libraries.

安装
----

Most distribution LAPACK packages do not include lapacke, so the easiest
method is to build from source:

      svn co https://icl.cs.utk.edu/svn/lapack-dev/lapack/trunk lapack
      cd lapack
      mkdir build
      cd build
      cmake -D BUILD_SHARED_LIBS=ON -D LAPACKE=ON ../
      make 
      sudo make install
      

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
