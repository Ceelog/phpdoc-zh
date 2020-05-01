PHP 是什么？
------------

PHP（“*PHP: Hypertext
Preprocessor*”，超文本预处理器的字母缩写）是一种被广泛应用的开放源代码的多用途脚本语言，它可嵌入到
HTML中，尤其适合 web 开发。

以上是一个简单的回答，不过这是什么意思呢？请看如下例子：

**示例 \#1 一个介绍性的范例**

``` php
<html>
    <head>
        <title>Example</title>
    </head>
    <body>

        <?php
        echo "Hi, I'm a PHP script!";
        ?>

    </body>
</html>
```

请注意这个范例和其它用 C 或 Perl
语言写的脚本之间的区别——与用大量的命令来编写程序以输出 HTML
不同的是，PHP 页面就是
HTML，只不过在其中嵌入了一些代码来做一些事情（在本例中输出了 "Hi, I'm a
PHP script!"）。PHP
代码被包含在特殊的<a href="/language/basic-syntax/phpmode.html" class="link">起始符和结束符 <code class="code">&lt;?php</code> 和 <code class="code">?&gt;</code></a>
中，使得可以进出“PHP 模式”。

和客户端的 JavaScript 不同的是，PHP
代码是运行在服务端的。如果在服务器上建立了如上例类似的代码，则在运行该脚本后，客户端就能接收到其结果，但他们无法得知其背后的代码是如何运作的。甚至可以将
web 服务器设置成让 PHP 来处理所有的 HTML
文件，这么一来，用户就无法得知服务端到底做了什么。

使用 PHP
的一大好处是它对于初学者来说极其简单，同时也给专业的程序员提供了各种高级的特性。当看到
PHP
长长的特性列表时，请不要害怕。可以很快的入门，只需几个小时就可以自己写一些简单的脚本。

尽管 PHP
的开发是以服务端脚本为目的，但事实上其功能远不局限与此。请继续读后面的章节，在“<a href="/intro-whatcando.html" class="link">PHP 能做什么</a>”一节中将获得更多的信息。如果对
web
编程感兴趣，也可以阅读<a href="/tutorial.html" class="link">简明教程</a>。
