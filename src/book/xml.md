XML 解析器
==========

**目录**

-   [简介](/intro/xml.html)
-   [安装／配置](/xml/setup.html)
    -   [需求](/xml/setup.html#需求)
    -   [安装](/xml/setup.html#安装)
    -   [运行时配置](/xml/setup.html#运行时配置)
    -   [资源类型](/xml/setup.html#资源类型)
-   [预定义常量](/xml/constants.html)
-   [事件处理器](/xml/eventhandlers.html)
-   [Case Folding(大写转换)](/xml/case-folding.html)
-   [错误代码](/xml/error-codes.html)
-   [字符编码](/xml/encoding.html)
-   [范例](/xml/examples.html)
    -   [XML 元素结构例程](/xml/examples.html#XML%20元素结构例程)
    -   [XML 标签映射例程](/xml/examples.html#XML%20标签映射例程)
    -   [XML 外部实体例程](/xml/examples.html#XML%20外部实体例程)
-   [XML 解析器函数](/ref/xml.html)
    -   [utf8\_decode](/ref/xml.html#utf8_decode) — 将用 UTF-8
        方式编码的 ISO-8859-1 字符串转换成单字节的 ISO-8859-1 字符串。
    -   [utf8\_encode](/ref/xml.html#utf8_encode) — 将 ISO-8859-1
        编码的字符串转换为 UTF-8 编码
    -   [xml\_error\_string](/ref/xml.html#xml_error_string) — 获取 XML
        解析器的错误字符串
    -   [xml\_get\_current\_byte\_index](/ref/xml.html#xml_get_current_byte_index)
        — 获取 XML 解析器的当前字节索引
    -   [xml\_get\_current\_column\_number](/ref/xml.html#xml_get_current_column_number)
        — 获取 XML 解析器的当前列号
    -   [xml\_get\_current\_line\_number](/ref/xml.html#xml_get_current_line_number)
        — 获取 XML 解析器的当前行号
    -   [xml\_get\_error\_code](/ref/xml.html#xml_get_error_code) — 获取
        XML 解析器错误代码
    -   [xml\_parse\_into\_struct](/ref/xml.html#xml_parse_into_struct)
        — 将 XML 数据解析到数组中
    -   [xml\_parse](/ref/xml.html#xml_parse) — 开始解析一个 XML 文档
    -   [xml\_parser\_create\_ns](/ref/xml.html#xml_parser_create_ns) —
        生成一个支持命名空间的 XML 解析器
    -   [xml\_parser\_create](/ref/xml.html#xml_parser_create) —
        建立一个 XML 解析器
    -   [xml\_parser\_free](/ref/xml.html#xml_parser_free) — 释放指定的
        XML 解析器
    -   [xml\_parser\_get\_option](/ref/xml.html#xml_parser_get_option)
        — 从 XML 解析器获取选项设置信息
    -   [xml\_parser\_set\_option](/ref/xml.html#xml_parser_set_option)
        — 为指定 XML 解析进行选项设置
    -   [xml\_set\_character\_data\_handler](/ref/xml.html#xml_set_character_data_handler)
        — 建立字符数据处理器
    -   [xml\_set\_default\_handler](/ref/xml.html#xml_set_default_handler)
        — 建立默认处理器
    -   [xml\_set\_element\_handler](/ref/xml.html#xml_set_element_handler)
        — 建立起始和终止元素处理器
    -   [xml\_set\_end\_namespace\_decl\_handler](/ref/xml.html#xml_set_end_namespace_decl_handler)
        — 建立终止命名空间声明处理器
    -   [xml\_set\_external\_entity\_ref\_handler](/ref/xml.html#xml_set_external_entity_ref_handler)
        — 建立外部实体指向处理器
    -   [xml\_set\_notation\_decl\_handler](/ref/xml.html#xml_set_notation_decl_handler)
        — 建立注释声明处理器
    -   [xml\_set\_object](/ref/xml.html#xml_set_object) — 在对象中使用
        XML 解析器
    -   [xml\_set\_processing\_instruction\_handler](/ref/xml.html#xml_set_processing_instruction_handler)
        — 建立处理指令（PI）处理器
    -   [xml\_set\_start\_namespace\_decl\_handler](/ref/xml.html#xml_set_start_namespace_decl_handler)
        — 建立起始命名空间声明处理器
    -   [xml\_set\_unparsed\_entity\_decl\_handler](/ref/xml.html#xml_set_unparsed_entity_decl_handler)
        — 建立未解析实体定义声明处理器
