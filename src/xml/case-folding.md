Case Folding(大写转换)
======================

元素处理函数可取得元素名称转换为 <span
class="glossterm">case-folded</span>(大写字母)形式。 Case-folding
被定义为“将非大写字母替换为相对应的大写字母的字符串操作”。换句话说，在
XML 中，case-folding 就是转换为大写。

默认情况下，所有的通过处理函数的元素名都被转换为大写字母。每个 XML
解析器可分别通过<span class="function">xml\_parser\_get\_option</span>与
<span
class="function">xml\_parser\_set\_option</span>函数来查询与控制此项功能。
