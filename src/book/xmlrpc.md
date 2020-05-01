XML-RPC
=======

**目录**

-   [简介](/intro/xmlrpc.html)
-   [安装／配置](/xmlrpc/setup.html)
    -   [需求](/xmlrpc/setup.html#需求)
    -   [安装](/xmlrpc/setup.html#安装)
    -   [运行时配置](/xmlrpc/setup.html#运行时配置)
    -   [资源类型](/xmlrpc/setup.html#资源类型)
-   [预定义常量](/xmlrpc/constants.html)
-   [XML-RPC 函数](/ref/xmlrpc.html)
    -   [xmlrpc\_decode\_request](/ref/xmlrpc.html#xmlrpc_decode_request)
        — 将 XML 译码为 PHP 本身的类型
    -   [xmlrpc\_decode](/ref/xmlrpc.html#xmlrpc_decode) — 将 XML 译码为
        PHP 本身的类型
    -   [xmlrpc\_encode\_request](/ref/xmlrpc.html#xmlrpc_encode_request)
        — 为 PHP 的值生成 XML
    -   [xmlrpc\_encode](/ref/xmlrpc.html#xmlrpc_encode) — 为 PHP
        的值生成 XML
    -   [xmlrpc\_get\_type](/ref/xmlrpc.html#xmlrpc_get_type) — 为 PHP
        的值获取 xmlrpc 的类型
    -   [xmlrpc\_is\_fault](/ref/xmlrpc.html#xmlrpc_is_fault) —
        Determines if an array value represents an XMLRPC fault
    -   [xmlrpc\_parse\_method\_descriptions](/ref/xmlrpc.html#xmlrpc_parse_method_descriptions)
        — 将 XML 译码成方法描述的列表
    -   [xmlrpc\_server\_add\_introspection\_data](/ref/xmlrpc.html#xmlrpc_server_add_introspection_data)
        — 添加自我描述的文档
    -   [xmlrpc\_server\_call\_method](/ref/xmlrpc.html#xmlrpc_server_call_method)
        — 解析 XML 请求同时调用方法
    -   [xmlrpc\_server\_create](/ref/xmlrpc.html#xmlrpc_server_create)
        — 创建一个 xmlrpc 服务端
    -   [xmlrpc\_server\_destroy](/ref/xmlrpc.html#xmlrpc_server_destroy)
        — 销毁服务端资源
    -   [xmlrpc\_server\_register\_introspection\_callback](/ref/xmlrpc.html#xmlrpc_server_register_introspection_callback)
        — 注册一个 PHP 函数用于生成文档
    -   [xmlrpc\_server\_register\_method](/ref/xmlrpc.html#xmlrpc_server_register_method)
        — 注册一个 PHP 函数用于匹配 xmlrpc 方法名
    -   [xmlrpc\_set\_type](/ref/xmlrpc.html#xmlrpc_set_type) — 为一个
        PHP 字符串值设置 xmlrpc 的类型、base64 或日期时间
