安装／配置
==========

**目录**

-   [需求](/sam/setup.html#需求)
-   [安装](/sam/setup.html#安装)
-   [运行时配置](/sam/setup.html#运行时配置)
-   [资源类型](/sam/setup.html#资源类型)

需求
----

The SAM extension interfaces to the IBM Messaging and Queuing middleware
products using a set of libraries and some client side code referred to
as XMS. This package is available as a free download in the guise of IBM
support pack IA94. There is a description of this package and download
links in the article
<a href="http://www-1.ibm.com/support/docview.wss?uid=swg24007092" class="link external">»  Introducing XMS - The IBM Message Service API</a>.

If you intend to use SAM to access the Messaging and Queuing
infrastructure within WebSphere MQ then you will also need to have
installed a local MQ queue manager or installed the WebSphere MQ clients
package. The clients package is freely available as a support pack
(<a href="http://www-1.ibm.com/support/docview.wss?rs=171&amp;uid=swg24009961&amp;loc=en_US&amp;cs=utf-8&amp;lang=en" class="link external">» MQC6</a>).

If you are only aiming to experiment with sending messages to and from
WebSphere Application Server queues using the *WebSphere Platform
Messaging protocol (WPM)* then you do not need to install the MQC6
package.

After installing these packages you will need to ensure the XMS binary
and, if you are using it, the MQ client bin directory are included in
the `PATH` environment variable so that Apache and PHP can find the
dependent .DLLs/libraries.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/sam" class="link external">» https://pecl.php.net/package/sam</a>.

The SAM framework and MQTT support can be built and used without any
other prerequisites. Support for protocols other than MQTT is provided
via a set of libraries and some client side code referred to as XMS.

If you only intend to use the built-in MQTT support then you can build
and configure SAM as an extension or simply refer to `php_sam.php` with
a <span class="function">require</span> or <span
class="function">require\_once</span> clause in your PHP script. In this
case you need only install the code without building the extension using
the pear installer:

    pecl install -B SAM

Linux installation steps
------------------------

The sam extension is supplied as a PECL module, which you should be able
to download and install in one step as follows:

    pecl install sam

(Depending on your php environment, you will probably need to be root to
do this.)

Make sure that the module is loaded by PHP, by adding following line to
`php.ini`:

    extension=sam.so

If you intend to use the XMS support to access the IBM Messaging and
Queuing family you must also enable the SAM XMS extension.

    extension=sam_xms.so

If you cannot use the PEAR installer, you can download the extension and
build it manually:

    pear download sam          #downloads sam-<version>.tgz
    tar -xzf sam-<version>.tgz
    cd sam-<version>
    phpize
    ./configure
    make
    make install               #you may need to be root for this step

To work with the very latest source, you'll need to extract it from SVN
and build manually as above.

Windows installation steps
--------------------------

You will probably need to build the sam extension for Windows as there
are only a limited range of pre-built binaries available from the SAM
website. The extension can be built using the standard Windows extension
build procedures.

You will need the PHP source tree for the version of PHP you wish to
build the SAM extension against which you can obtain from php.net. This
should be unpacked into a working directory of your choice.

You will also need the libraries and headers used by PHP extensions
available from http://www.php.net/extra/win32build.zip and this should
be unzipped so that is in your working directory.

You should have something like:

    c:\php-build\-
                  |
                  |---php-5.0.5--|---build
                  |              |---ext
                  |              |--- ...
                  |
                  |---win32build--|---bin
                                  |---include
                                  |---lib

You will need a compiler such as the free version of Visual Studio C++
Express from the Microsoft web site. Also you need the Microsoft *SDK
Microsoft Windows Platform* which again can be downloaded from the
Microsoft web site.

Obtain the SAM extension source using pear (pecl download sam) or by
using SVN and copy the files to a new "sam" directory under the "ext"
directory in your PHP source tree.

To build the extension open a build environment window by going to the
start

menu-\>all programs-\>microsoft platform SDK for windows-\>  
open build environment window-\>windows 200 build environment-\>  
set windows 2000 build environment (retail)

This should open a command prompt with all the environment variables set
up to access the platform SDK etc. You then need to set the environment
variables for Visual Studio by issuing the command **vcvars32.bat** in
the window.

Change directory to your working directory e.g. cd `c:\php-build`. Then
make sure the win32build tools are accessible by adding them to the
`PATH` environment variable:

    set PATH=..\win32build\bin;%PATH%

Run the **buildconf.bat** command. This should rebuild the
`configure.js` file.

Run the **cscript** command with the appropriate options. To build just
the SAM extension framework and MQTT support use:

    cscript /nologo configure.js --with-sam

To build the SAM framework and the XMS support use:

    cscript /nologo configure.js --with-sam --with-sam_xms="c:\program files\ibm\xms"

The additional parameter passed for sam\_xms is the installation path to
the XMS libraries and runtime that were installed as described under
prerequisites at the top of this page.

You can specify whatever other **cscript** parameters you require to
include or exclude items from the php build or select options.

Assuming all has gone well so far you can now finally run a make for the
SAM framework!

    nmake php_sam.dll

Also if you are using the XMS support you must make the sam\_xms
extensions:

    nmake php_sam_xms.dll

If you have used Visual Studio 2005 to build the DLLs please see below
for additional steps that must be carried out before proceeding further.

The DLLs created (`php_sam.dll` and optionally `php_sam_xms.dll`) can
now be copied to the subdirectory appropriate for your PHP set-up. Make
sure that the module(s) are loaded by PHP, by adding following line to
`php.ini`:

    extension=php_sam.dll

If you intend to use the XMS support to access the IBM Messaging and
Queuing family you must also enable the SAM XMS extension.

    extension=php_sam_xms.dll

Additional steps for Visual Studio 2005
---------------------------------------

If you build the SAM extension with the Microsoft Visual Studio 2005
compiler and tools you need to perform an additional step in the build
process to ensure the `php_sam.dll` is able to link with the C runtime
libraries at runtime. This step includes the dependancy manifest into
the DLL. Switch to the directory where the `php_sam.dll` has been
generated (usually Release\_TS or Debug\_TS below the php source
directory) and issue the following magic incantation:

    mt.exe -manifest php_sam.dll.manifest -outputresource:php_sam.dll;2

If you are using the XMS capabilities you will need to do the same with
the SAM XMS DLL:

    mt.exe -manifest php_sam_xms.dll.manifest -outputresource:php_sam_xms.dll;2

If you build the SAM extension using the compiler and libraries from
Microsoft Visual Studio 2005 you will also need to ensure that the
runtime components are installed on the system on which you intend to
use SAM. This can be accomplished by installing Visual Studio 2005 or by
using the freely distributable
<a href="http://www.microsoft.com/downloads/details.aspx?familyid=32BC1BEE-A3F9-4C13-9C99-220B62A191EE&amp;displaylang=en" class="link external">» runtime package</a>.

运行时配置
----------

Protocol support and mapping
----------------------------

The SAM framework can be extended to support other messaging protocols
and connection mechanisms. To add support for a new protocol or
connection library a support class has to be defined, either as a C
extension or as a PHP script, and a "factory" script must be created.
The support class must implement all the methods of the SAMConnection
class though it should not inherit from SAMConnection. The factory
script will be called by the SAM framework to create an instance of the
implemented class. The way SAM chooses which factory to call is based on
the protocol specified as the first parameter of the "connect" call.

By default the built-in MQTT support will be used if a connect call
specifies a protocol of SAM\_MQTT ("mqtt"), for any other protocol SAM
will attempt to use the XMS support extension. To add support for
additional protocols or to modify the default behavior entries may be
added to `php.ini` in the \[sam\] section. The default mapping is
equivalent to the following entries:

    [sam]
    sam.factory.mqtt=mqtt
    sam.factory.wmq=xms
    sam.factory.wmq:client=xms
    sam.factory.wmq:bindings=xms
    sam.factory.wpm=xms
    sam.factory.rtt=xms

As can be seen from these examples the entries take the form of
"sam.factory.pppp=xxx" where pppp is the protocol string specified on
the connect call and xxx is a factory suffix. Note: SAM defines
constants for these protocol strings such that *SAM\_WMQ=wmq*,
*SAM\_WPM=wpm*, *SAM\_RTT=rtt*, *SAM\_MQTT=mqtt*, etc.

When identifying the support code to use on a connect call SAM looks up
the protocol name in the `php.ini` entries and then invokes a factory
script named `sam_factory_xxx.php`. If no entry is found the support
will default to XMS.

资源类型
--------

此扩展没有定义资源类型。
