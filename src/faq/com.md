PHP 和 COM
==========

PHP 可以在 Win32 平台中访问 COM 和 DCOM 对象。

1.  [我建立了一个 DLL 来做某种计算。有办法在 PHP 中运行这个 DLL
    吗？](#faq.com.q1)
2.  [“Unsupported variant type: xxxx (0xxxxx)”是什么意思？](#faq.com.q2)
3.  [在 PHP 中有可能操纵可视对象吗？](#faq.com.q3)
4.  [可以将一个 COM 对象保存在 session 中吗？](#faq.com.q4)
5.  [怎样可以捕获 COM 的错误？](#faq.com.q5)
6.  [我能像在 Perl 中一样从 PHP 脚本生成 DLL 文件吗？](#faq.com.q6)
7.  [“Unable to obtain IDispatch interface for CLSID
    {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}”是什么意思？](#faq.com.q7)
8.  [怎样从远端服务器运行 COM 对象？](#faq.com.q8)
9.  [我得到一个“DCOM is disabled in C:\\path...\\scriptname.php on line
    6”信息，应该怎么办？](#faq.com.q9)
10. [有可能在 PHP 页面中加载／操纵 ActiveX 对象吗？](#faq.com.q10)
11. [有可能得到一个组件在运行中的实例吗？](#faq.com.q11)
12. [有办法处理 COM 对象中发送的事件吗？](#faq.com.q12)
13. [我在尝试调用一个打开了多于一个接口的 COM
    对象中的方法时碰到问题，应该怎么办？](#faq.com.q13)
14. [这么说 PHP 可以和 COM 一起工作，那么 COM+ 呢？](#faq.com.q14)
15. [如果 PHP 可以操纵 COM 对象，那么可以设想结合 PHP 用 MTS
    来管理组件资源吗？](#faq.com.q15)

**我建立了一个 DLL 来做某种计算。有办法在 PHP 中运行这个 DLL 吗？**  
如果这是个简单的 DLL 那么还没有办法在 PHP 中运行它。如果这个 DLL
中包含有一个 COM 服务器并且它实现了 IDispatch 接口，那有可能访问它。

<!-- -->

**“Unsupported variant type: xxxx (0xxxxx)”是什么意思？**  
有几十种 VARIANT
类型以及它们的组合。大多数已经被支持了但还有几种尚未实现。数组没有完全被支持。只有一维的仅用作索引的数组可以在
PHP 和 COM 之间传递。如果你发现其它未支持的类型，请当作一个 bug
报告（如果尚未被报告的话）并提供尽可能多的信息。

<!-- -->

**在 PHP 中有可能操纵可视对象吗？**  
一般来说是可以的，但是 PHP 大都用来作为 web 脚本语言并运行在 web
服务器的上下文环境中，因此可视对象决不会在服务器的桌面上显示。如果你把
PHP 用作应用程序脚本例如结合 PHP-GTK 来使用，那么访问和通过 COM
来操纵可视对象方面没有限制。

<!-- -->

**可以将一个 COM 对象保存在 session 中吗？**  
不行。COM 的实例被看作是资源，因此只在一个脚本的上下文中有效。

<!-- -->

**怎样可以捕获 COM 的错误？**  
在 PHP 5 中，COM 扩展会发出 *com\_exception*异常信息，可以捕获并检查
*code*成员来决定下一步的行为。

在 PHP 4 中除了用 PHP
自己提供的办法之外（@，track\_errors，..）不可能捕获 COM 的错误。

<!-- -->

**我能像在 Perl 中一样从 PHP 脚本生成 DLL 文件吗？**  
不行，PHP 没有这样的工具。

<!-- -->

**“Unable to obtain IDispatch interface for CLSID {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}”是什么意思？**  
此错误可以有多种原因：

-   <span class="simpara">错误的 CLSID</span>
-   <span class="simpara">找不到所请求的 DLL</span>
-   <span class="simpara">所请求的组件没有实现 IDispatch 接口</span>

<!-- -->

**怎样从远端服务器运行 COM 对象？**  
完全和运行本地对象一样。只须将远端服务器的 IP 作为第二个变量传递给 COM
的构造函数即可。

确认在 `php.ini` 中设定了 <a href="/com/setup.html#" class="xref"></a>
*=*&true;。

<!-- -->

**我得到一个“DCOM is disabled in C:\\path...\\scriptname.php on line 6”信息，应该怎么办？**  
编辑 `php.ini` 并设定 <a href="/com/setup.html#" class="xref"></a>
*=*&true;。

<!-- -->

**有可能在 PHP 页面中加载／操纵 ActiveX 对象吗？**  
这不关 PHP 的事。如果在 HTML 文档中请求的话，ActiveX
对象被加载在客户端。这和 PHP
脚本没有关系，因此也不可能和服务器端发生直接的交互作用。

<!-- -->

**有可能得到一个组件在运行中的实例吗？**  
在绰号的帮助下这有可能。如果你想得到同一个 word
实例的多个引用你可以这样建立此实例：

``` php
<?php
$word = new COM("C:\docs\word.doc");
?>
```

如果没有运行中的实例这将建立一个新的实例，否则将会返回正在运行中的实例的句柄，如果可用的话。

<!-- -->

**有办法处理 COM 对象中发送的事件吗？**  
可以自定义事件收报方并且用 <span
class="function">com\_event\_sink</span>函数绑定之。可以用 <span
class="function">com\_print\_typeinfo</span>来让 PHP
产生事件收报方类的框架。

<!-- -->

**我在尝试调用一个打开了多于一个接口的 COM 对象中的方法时碰到问题，应该怎么办？**  
我也不知道怎么办，我想这没办法。如果什么人有对此问题的明确信息请
<a href="mailto:harald.radi@nme.at" class="link external">» 告诉我</a>。:)

<!-- -->

**这么说 PHP 可以和 COM 一起工作，那么 COM+ 呢？**  
COM+ 通过使用 MTS 和 MSMQ 来管理组件的框架扩展了
COM，但并没有什么特殊之处使 PHP 非要支持这样的组件。

<!-- -->

**如果 PHP 可以操纵 COM 对象，那么可以设想结合 PHP 用 MTS 来管理组件资源吗？**  
PHP
本身还并不处理事务。因而如果出错也不会发动撤回机制。如果你使用了支持事务处理的组件那你不得不自己实现事务管理。
