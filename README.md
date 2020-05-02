# phpdoc-zh

## What

Markdown 格式的 PHP 中文手册

## Why

markdown 已经成为主流的文档撰写标记语言，可以高效地撰写和阅读文档。

另外，markdown 有丰富的工具链，可以将文档转换为各种格式以及自定义渲染样式。

由于历史原因，php 手册一直使用 xml 格式编写，不利于推广应用。为了让更多的用户可以随心所欲的使用 php 手册，同时很容易地注意到文档最新的变更，本项目每天从 php 手册 svn 库拉取更新，并转换为 md 格式。

## How

[PHP 手册](http://svn.php.net/viewvc/phpdoc/)的原始内容是使用 docbook 语法的 xml 文件，通过 [PhD](http://doc.php.net/phd.php) 文档转换工具生成中间 html 格式的内容，再使用 [pandoc](https://github.com/jgm/pandoc) 转换为 md 格式。

最后，你可以使用 [mdbook](https://github.com/rust-lang/mdBook) 将 md 格式的内容渲染成想要的样式，方便阅读。

你也可以直接在 http://phpdoc-zh.roadmapedu.com/ 阅读生成的文档。

## Acknowledgement

- https://www.php.net/docs.php
- http://doc.php.net/phd.php
- https://github.com/jgm/pandoc
- https://github.com/rust-lang/mdBook
- http://phpdoc-zh.roadmapedu.com/
- http://phpdoc-en.roadmapedu.com/


