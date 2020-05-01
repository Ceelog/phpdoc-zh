预定义常量
==========

下列常量作为 PHP 核心的一部分总是可用的。

| 常量                   | 值  | 描述                                                                                                                                                                                     |
|------------------------|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`CREDITS_GROUP`**    | 1   | 核心开发者名单                                                                                                                                                                           |
| **`CREDITS_GENERAL`**  | 2   | 总的贡献：语言设计和理念，PHP 作者 和 SAPI 模块。                                                                                                                                        |
| **`CREDITS_SAPI`**     | 4   | PHP 的服务器 API 模块列表，以及它们的作者。                                                                                                                                              |
| **`CREDITS_MODULES`**  | 8   | PHP 扩展的列表，以及它们的作者。                                                                                                                                                         |
| **`CREDITS_DOCS`**     | 16  | 文档组的贡献。                                                                                                                                                                           |
| **`CREDITS_FULLPAGE`** | 32  | 通常与其他标志组合使用。通过其他标志指示了完整独立的 HTML 页面，用于打印包含信息。                                                                                                       |
| **`CREDITS_QA`**       | 64  | 质量保证团队的贡献。                                                                                                                                                                     |
| **`CREDITS_ALL`**      | -1  | 所有的贡献者，等于使用 *CREDITS\_DOCS + CREDITS\_GENERAL + CREDITS\_GROUP + CREDITS\_MODULES + CREDITS\_QA CREDITS\_FULLPAGE*。 它以合适的标签产生了完整的独立 HTML 页面。这是默认的值。 |

| 常量                     | 值  | 描述                                                                                                                                    |
|--------------------------|-----|-----------------------------------------------------------------------------------------------------------------------------------------|
| **`INFO_GENERAL`**       | 1   | 配置行，`php.ini` 的位置、构建日期，Web 服务器、操作系统及其他。                                                                        |
| **`INFO_CREDITS`**       | 2   | PHP 贡献者。参见 <span class="function">phpcredits</span>。                                                                             |
| **`INFO_CONFIGURATION`** | 4   | 当前 PHP 指令的本地（Local）和主（Master）值。参见 <span class="function">ini\_get</span>。                                             |
| **`INFO_MODULES`**       | 8   | 已加载的模块和各自的设置。                                                                                                              |
| **`INFO_ENVIRONMENT`**   | 16  | 环境变量信息在 `$_ENV` 中亦有效。                                                                                                       |
| **`INFO_VARIABLES`**     | 32  | 显示所有 *EGPCS* （环境变量、GET、POST、Cookie、Server）中的<a href="/language/variables/predefined.html" class="link">预定义变量</a>。 |
| **`INFO_LICENSE`**       | 64  | PHP 版权信息。参见 <a href="https://www.php.net/license/" class="link external">» license faq</a>。                                     |
| **`INFO_ALL`**           | -1  | 显示以上所有。这是默认值。                                                                                                              |

| 常量          | 值  | 描述   |
|---------------|-----|--------|
| *INI\_USER*   | 1   | Unused |
| *INI\_PERDIR* | 2   | Unused |
| *INI\_SYSTEM* | 4   | Unused |
| *INI\_ALL*    | 7   | Unused |

断言常量，这些值用于设置 <span class="function">assert\_options</span>
中的断言标记 。

| 常量                    | INI 设置           | 描述                                        |
|-------------------------|--------------------|---------------------------------------------|
| **`ASSERT_ACTIVE`**     | assert.active      | 启用 <span class="function">assert</span>。 |
| **`ASSERT_CALLBACK`**   | assert.callback    | 失败断言的回调函数。                        |
| **`ASSERT_BAIL`**       | assert.bail        | 断言失败时中止执行。                        |
| **`ASSERT_WARNING`**    | assert.warning     | 为每个失败的断言产生一条 PHP 警告。         |
| **`ASSERT_QUIET_EVAL`** | assert.quiet\_eval | 在执行断言表达式时禁用 *error\_reporting*。 |

以下常量仅在主机操作系统是
Windows的情况下有效，能得到不同版本信息，能够检测利用一些功能。 自 PHP
5.3.0 起有效。

| 常量                                   | 描述                                                                                                                                                                        |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`PHP_WINDOWS_VERSION_MAJOR`**        | windows 主版本，可以是 *4* (NT4/Me/98/95)、 *5* (XP/2003 R2/2003/2000) 或 *6* (Vista/2008/7/8/8.1)。                                                                        |
| **`PHP_WINDOWS_VERSION_MINOR`**        | Windows 副版本号，可以是 *0* (Vista/2008/2000/NT4/95)、 *1* (XP)、*2* (2003 R2/2003/XP x64)、 *10* (98) 或 *90* (ME)。                                                      |
| **`PHP_WINDOWS_VERSION_BUILD`**        | Windows 内部版本号(例如 Windows Vista SP1 是 build 6001)                                                                                                                    |
| **`PHP_WINDOWS_VERSION_PLATFORM`**     | PHP 当前运行的平台， Windows Vista/XP/2000/NT4、Server 2008/2003 的值是 *2*， Windows ME/98/95 下值是 *1*。                                                                 |
| **`PHP_WINDOWS_VERSION_SP_MAJOR`**     | 安装的 service pack 主版本号，没有安装是 *0*。 例如， Windows XP service pack 3 上这个值是 *3*。                                                                            |
| **`PHP_WINDOWS_VERSION_SP_MINOR`**     | 安装的 service pack 副版本号，如果没有安装则是 *0* 。                                                                                                                       |
| **`PHP_WINDOWS_VERSION_SUITEMASK`**    | The suitemask is a bitmask that can tell if various features of Windows is installed, see the table below for possible bitfield values.                                     |
| **`PHP_WINDOWS_VERSION_PRODUCTTYPE`**  | This contains the value used to determine the *PHP\_WINDOWS\_NT\_\** constants. This value may be one of the *PHP\_WINDOWS\_NT\_\** constants indicating the platform type. |
| **`PHP_WINDOWS_NT_DOMAIN_CONTROLLER`** | 这是域控制器                                                                                                                                                                |
| **`PHP_WINDOWS_NT_SERVER`**            | 这是一个服务器系统 (eg. Server 2008/2003/2000)，注意如果这是一个域控制器，通过 **`PHP_WINDOWS_NT_DOMAIN_CONTROLLER`** 报告。                                                |
| **`PHP_WINDOWS_NT_WORKSTATION`**       | 这是一个工作站系统 (例如 Vista/XP/2000/NT4)                                                                                                                                 |

此功能列表可以通过 **`PHP_WINDOWS_VERSION_SUITEMASK`** 位掩码检测。

| Bits         | 描述                                                                                                                                                          |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *0x00000004* | 安装的是 Microsoft BackOffice components。                                                                                                                    |
| *0x00000400* | 安装的是 Windows Server 2003, Web Edition。                                                                                                                   |
| *0x00004000* | 安装的是 Windows Server 2003, Compute Cluster Edition。                                                                                                       |
| *0x00000080* | 安装的是 Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition or Windows 2000 Datacenter Server。                                          |
| *0x00000002* | 安装的是 Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, Windows 2000 Advanced Server 或 Windows NT Server 4.0 Enterprise Edition 。 |
| *0x00000040* | 安装的是 Windows XP Embedded。                                                                                                                                |
| *0x00000200* | 安装的是 Windows Vista Home Premium, Windows Vista Home Basic 或 Windows XP Home Edition。                                                                    |
| *0x00000100* | Remote Desktop is supported, but only one interactive session is supported. This value is set unless the system is running in application server mode.        |
| *0x00000001* | Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.                                   |
| *0x00000020* | Microsoft Small Business Server is installed with the restrictive client license in force.                                                                    |
| *0x00002000* | 安装的是 Windows Storage Server 2003 R2 或 Windows Storage Server 2003。                                                                                      |
| *0x00000010* | 中断服务安装了。这个值总是设置的。如果这个值设置了，但 *0x00000100* 没有设置，操作系统运行于 application server 模式。                                        |
| *0x00008000* | 安装的是 Windows Home Server。                                                                                                                                |
