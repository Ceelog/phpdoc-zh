一般信息
========

本章包括了有关 PHP 的大多数一般问题： 它是什么和它做什么。

1.  [PHP是什么？](#faq.general.what)
2.  [PHP 这个缩写指的是什么？](#faq.general.acronym)
3.  [PHP 版本之间有什么联系？](#faq.general.relation-versions)
4.  [可以同时运行几个不同版本的 PHP
    吗？](#faq.general.running-concurent)
5.  [我觉得自己发现了一个 bug！应该告诉谁？](#faq.general.bug)

**PHP是什么？**  
根据本手册的 <a href="/preface.html" class="link">前言</a>：

PHP 是一种 HTML 嵌入式的脚本语言。 它的很多语法来自 C，Java 和 Perl，
并具有几个 PHP 独有的特点。 该语言的主要目标是让 Web
开发人员快速地书写动态生成的网页。

<!-- -->

**PHP 这个缩写指的是什么？**  
PHP 是*PHP: Hypertext Preprocessor*的首字母缩写。
很多人有些糊涂了，因为缩写中的第一个字母也来自缩写。
这种方法叫做递归缩写（recursive acronyms）， 对此好奇的人可以访问
<a href="http://foldoc.org/" class="link external">» 在线计算机词典（Free On-Line Dictionary of Computing）</a>
或者Wikipedia上
<a href="http://en.wikipedia.org/wiki/Recursive_acronym" class="link external">» 递归缩写</a>
的解释。

<!-- -->

**PHP 版本之间有什么联系？**  
PHP/FI 2.0 是最早的 PHP 版本，已经不再支持。 PHP 3 是 PHP/FI 2.0
的后继者，要好很多。 PHP 7 是目前一代的 PHP，内部使用了 Zend 引擎 3 代，
除了很多新功能之外还提供了许多附加的
<a href="/language/oop5.html" class="link">面向对象编程（OOP）</a>
特性。

<!-- -->

**可以同时运行几个不同版本的 PHP 吗？**  
可以，请参阅见 PHP 源程序发行包中的 `INSTALL`文件。

<!-- -->

**我觉得自己发现了一个 bug！应该告诉谁？**  
应该访问 PHP Bug 数据库并确认你发现的不是一个已知的 bug。
如果你在数据库中没有看到同样的， 用报告表单来报告此 bug。 使用 bug
数据库而不是给某个邮件列表发邮件非常重要， 因为该 bug
会被分配一个跟踪号码， 这样你就有可能在以后回来查看该 bug 的状态。 Bug
数据库在
<a href="https://bugs.php.net/" class="link external">» https://bugs.php.net/</a>。
