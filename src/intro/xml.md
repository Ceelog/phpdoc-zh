XML(可扩展标记语言，eXtensible Markup Language)
是一种在互联网上用于结构化文档交互的数据格式。
它是互联网协会(W3C)定义的一个标准。与 XML 及其相关技术的信息可访问
<a href="http://www.w3.org/XML/" class="link external">» http://www.w3.org/XML/</a>。

此 PHP 扩展实现 支持 James Clark 使用 PHP 编写的 <span
class="productname">expat</span>。 此工具包可解析(但不能验证) XML
文档。它支持 PHP 所提供的 3
种<a href="/xml/encoding.html" class="link">字符编码</a>： *US-ASCII*,
*ISO-8859-1* 和 *UTF-8*。 不支持 *UTF-16*。

此扩展可
<a href="/ref/xml.html#xml_parser_create" class="link">创建 XML 解析器</a>
并为不同的 XML 事件定义 *处理程序(handler)*。 每个 XML
解析器还存在少数可以调节的
<a href="/ref/xml.html#xml_parser_set_option" class="link">参数</a>。
