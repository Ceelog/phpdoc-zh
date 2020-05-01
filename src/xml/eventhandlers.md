事件处理器
==========

XML 事件处理器的定义如下：

| PHP 处理器函数                                                           | 事件描述                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span class="function">xml\_set\_element\_handler</span>                 | 当 XML 解析器遇到开始或结束标签时，会触发元素事件。 开始标签和结束标签有不同的处理器。                                                                                                                         |
| <span class="function">xml\_set\_character\_data\_handler</span>         | 字符数据范指 XML 文档中所有非标记的内容，包括标签之间的空格。 注意，XML 解析器不会添加或删除任何空格，由应用程序(你)来判断空格是否有意义。                                                                     |
| <span class="function">xml\_set\_processing\_instruction\_handler</span> | PHP 程序员必须熟练掌握处理指令(PI)。\<?php ?\>是处理指令， 其中<span class="replaceable">php</span>被称为“处理指令对象”。 除所有以“XML”开头的处理指令对象是系统保留的外， 其他的处理函数均是由应用程序指定的。 |
| <span class="function">xml\_set\_default\_handler</span>                 | 不执行其他处理函数，则会执行缺省的处理函数。 在缺省的处理函数中可取得如 XML 和文档类型声明等信息。                                                                                                             |
| <span class="function">xml\_set\_unparsed\_entity\_decl\_handler</span>  | 未解析的实体声明(NDATA)会调用此处理函数。                                                                                                                                                                      |
| <span class="function">xml\_set\_notation\_decl\_handler</span>          | 符号声明会调用此处理函数                                                                                                                                                                                       |
| <span class="function">xml\_set\_external\_entity\_ref\_handler</span>   | 当 XML 解析器发现对外部已解析的普通实体的引用时， 会调用此处理函数。例如，引用一个文件或URL。实例可参见 <a href="/xml/examples.html#XML%20外部实体例程" class="link">XML 外部实体例程</a>。                    |
