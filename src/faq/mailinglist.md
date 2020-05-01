邮件列表
========

本章包括有关如何与 PHP 团体接触的问题。最好的方法是邮件列表。

1.  [有没有 PHP 的邮件列表？](#faq.mailinglist.isthere)
2.  [还有其它的团体吗？](#faq.mailinglist.others)
3.  [我可以建立我自己的PHP邮件列表吗？](#faq.mailinglist.myown)
4.  [救命！我看来不能订阅／取消任何一个邮件列表！](#faq.mailinglist.subscribing)
5.  [在哪里有个邮件列表的归档吗？](#faq.mailinglist.archive)
6.  [我可以在邮件列表中问什么？](#faq.mailinglist.question)
7.  [向邮件列表发帖子时我需要包括些什么信息？](#faq.mailinglist.guideline)

**有没有 PHP 的邮件列表？**  
当然有！有很多关于几个主题的邮件列表。所有邮件列表的完整列表在
<a href="https://www.php.net/mailing-lists.php" class="link external">» 技术支持</a>页面。

最通用的邮件列表是 *php-general*。要订阅，发送一封邮件到
<a href="mailto:php-general-subscribe@lists.php.net" class="link external">» php-general-subscribe@lists.php.net</a>。不需要在邮件主题或内容中包括任何特殊单词。要取消订阅，发送一封邮件到
<a href="mailto:php-general-unsubscribe@lists.php.net" class="link external">» php-general-unsubscribe@lists.php.net</a>。

也可以在我们的
<a href="https://www.php.net/mailing-lists.php" class="link external">» 技术支持</a>页面通过
web 界面来订阅和取消。

<!-- -->

**还有其它的团体吗？**  
世界上有无数 PHP 团体。我们的
<a href="https://www.php.net/support.php" class="link external">» 技术支持</a>页面上有例如一些
IRC 服务器和其它语种的邮件列表。

<!-- -->

**我可以建立我自己的PHP邮件列表吗？**  
百分百可以！实际上，我们不仅允许这么做，而且鼓励这么做！
通过分享您在PHP方面的知识和经验来帮助他人，
有助于促进PHP组织和PHP语言本身的增长和发展。

<!-- -->

**救命！我看来不能订阅／取消任何一个邮件列表！**  
如果你在订阅或取消 php-general
邮件列表上有问题，可能是因为邮件列表软件没法确定你正确的邮件地址。如果你的
email 地址是 *joeblow@example.com*，可以将订阅请求发送到
*php-general-subscribe-joeblow=example.com@lists.php.net*，或者将取消请求发送到
*php-general-unsubscribe-joeblow=example.com@lists.php.net*。对其它邮件列表用类似的地址。

The most common reason folks have a hard time unsubscribing from our
mailing lists is due to the use of mail forwarders. For example, if your
email address is danbrown@example.com, but you subscribed to the mailing
list with the forwarder php-lists@example.com and forward that to
danbrown@example.com, attempting to unsubscribe danbrown@example.com
will not work, as that address is not even known to our systems.
Instead, you will need to unsubscribe the address to which the mail is
being sent - in this example, php-lists@example.com.

<!-- -->

**在哪里有个邮件列表的归档吗？**  
是的，你可以在
<a href="https://www.php.net/mailing-lists.php" class="link external">» 技术支持</a>页面找到归档站点的列表。
You will also find dozens of sites that archive and/or syndicate our
mailing list content by using your favorite Internet search engine and
searching for "php mailing list archives".

邮件列表的文章也被作为新闻组消息归档。你可以用新闻组客户端来访问位于
<a href="news://news.php.net/" class="link external">» news://news.php.net/</a>的新闻组服务器。也有一个试验性质的新闻组服务器的
web 界面位于
<a href="http://news.php.net/" class="link external">» http://news.php.net/</a>。

<!-- -->

**我可以在邮件列表中问什么？**  
由于 PHP 一天比一天更流行，php-general 邮件列表的流量增加到现在的每天
150 到 200
个帖子。由于此原因，为了每个人的利益，使用此列表是你在寻找过所有其它地方后的最后手段。

在你向列表发帖之前请先看看本 FAQ
以及手册是不是能找到帮助。如果找不到的话试试邮件列表归档（见上面）。如果你有安装或者配置
PHP 的问题请从头到尾读一遍所有包含的文档和 README
文件。如果还是不能找到任何可以帮助你的信息，那么很欢迎你使用此邮件列表。

To ensure that you receive the best responses (and to reduce the
likelihood of frustrating your fellow developers), please be sure to
post your question to the appropriate list. For example, if you are
having difficulties installing PHP, you should send your question to the
*php-install* mailing list. A caveat: some lists have similar names and
completely different uses; a question regarding PHP scripts on Windows
should be directed to the Windows PHP users list, *not* to the Windows
Internals list.

在提问之前，阅读一下
<a href="http://www.catb.org/~esr/faqs/smart-questions.html" class="link external">» 怎样聪明地发问</a>这篇文章对每个人都是个好主意。

<!-- -->

**向邮件列表发帖子时我需要包括些什么信息？**  
像“我不能启动运行
PHP！帮帮我！哪里出错了？”之类的贴子对任何人都完全没有用。如果你在启动和运行
PHP 上有问题你必须包括你运行的操作系统，你试图配置的 PHP
版本，你怎样得到的（预编译的，CVS，RPM
等等），目前为止你都做了些什么，卡在了何处以及确切的错误信息。

这也同样适用于其它问题。你必须包括你做了什么，卡在了哪里，你试图做什么以及，如果有的话，确切的错误信息。如果你有源代码的问题那你需要包括不起作用部分的代码。可是不要包括超出所必需的代码！这将使贴子很难读并使很多人为此而跳过它。如果你不确定应该在邮件中包括多少信息，那包括多一些比一点点更好。

另一件重要的事是记住在主题一行中概述你的问题。类似“救命！”或者“这是怎么回事？”的主题会被一大半读者忽略。

最后，我们鼓励你阅读一下
<a href="http://www.catb.org/~esr/faqs/smart-questions.html" class="link external">» 怎样聪明地发问</a>这篇文章。这对每个人都有很大帮助，尤其是你自己。
