Building for Windows
====================

**目录**

-   [Prerequisites](/wincache/win32build.html#Prerequisites)
-   [Compiling and
    building](/wincache/win32build.html#Compiling%20and%20building)
-   [Verifying the
    build](/wincache/win32build.html#Verifying%20the%20build)

Prerequisites
-------------

Building WinCache extension will require:

1.  <span class="simpara">PHP source code</span>
2.  <span class="simpara">PHP build environment</span>
3.  <span class="simpara">WinCache source code</span>

For completing first two steps, follow the step-by-step guide for how to
<a href="https://wiki.php.net/internals/windows/stepbystepbuild" class="link external">» build PHP on Windows</a>.

For getting the WinCache source code follow the instructions described
in
<a href="/install/pecl/downloads.html" class="link">Downloading PECL extensions</a>.

Compiling and building
----------------------

The following steps describe how to compile and build WinCache on
Windows OS:

1.  Open a command prompt which is used to build PHP

2.  Go to the root folder where PHP sources are present

3.  Run the command:

    ``` cmd
    cscript.exe win32\build\buildconf.js
    ```

4.  Run the command:

    ``` cmd
    configure.bat --help
    ```

    The output will contain a new flag *--enable-wincache*.

5.  Run the command:

    ``` cmd
    configure.js [all options used to build PHP] --enable-wincache
    ```

    *--enable-wincache* is the only extra option which is required to
    ensure that WinCache extension gets built properly. This option will
    build WinCache and will statically link it with PHP dll. To build
    WinCache extension as a stand-alone DLL use the option
    *--enable-wincache=shared*.

6.  Run the command:

    ``` cmd
    nmake
    ```

Verifying the build
-------------------

The following steps describe how to verify that WinCache has been built
correctly:

1.  Go to the folder where the PHP binaries are built

2.  Run the command:

    ``` cmd
    php.exe -n -d extension=php_wincache.dll -re wincache
    ```

    If WinCache has been built properly, the output of this command will
    list the INI directives and functions supported by WinCache.
