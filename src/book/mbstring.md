多字节字符串
============

**目录**

-   [简介](/intro/mbstring.html)
-   [安装／配置](/mbstring/setup.html)
    -   [需求](/mbstring/setup.html#需求)
    -   [安装](/mbstring/setup.html#安装)
    -   [运行时配置](/mbstring/setup.html#运行时配置)
    -   [资源类型](/mbstring/setup.html#资源类型)
-   [预定义常量](/mbstring/constants.html)
-   [支持编码的摘要](/mbstring/encodings.html)
-   [日文字符多字节编码基础](/mbstring/ja-basic.html)
-   [HTTP 输入和输出](/mbstring/http.html)
-   [支持的字符编码](/mbstring/supported-encodings.html)
-   [函数重载功能](/mbstring/overload.html)
-   [PHP字符编码的要求](/mbstring/php4/req.html)
-   [多字节字符串 函数](/ref/mbstring.html)
    -   [mb\_check\_encoding](/ref/mbstring.html#mb_check_encoding) —
        检查字符串在指定的编码里是否有效
    -   [mb\_chr](/ref/mbstring.html#mb_chr) — Get a specific character
    -   [mb\_convert\_case](/ref/mbstring.html#mb_convert_case) —
        对字符串进行大小写转换
    -   [mb\_convert\_encoding](/ref/mbstring.html#mb_convert_encoding)
        — 转换字符的编码
    -   [mb\_convert\_kana](/ref/mbstring.html#mb_convert_kana) —
        Convert "kana" one from another ("zen-kaku", "han-kaku" and
        more)
    -   [mb\_convert\_variables](/ref/mbstring.html#mb_convert_variables)
        — 转换一个或多个变量的字符编码
    -   [mb\_decode\_mimeheader](/ref/mbstring.html#mb_decode_mimeheader)
        — 解码 MIME 头字段中的字符串
    -   [mb\_decode\_numericentity](/ref/mbstring.html#mb_decode_numericentity)
        — 根据 HTML 数字字符串解码成字符
    -   [mb\_detect\_encoding](/ref/mbstring.html#mb_detect_encoding) —
        检测字符的编码
    -   [mb\_detect\_order](/ref/mbstring.html#mb_detect_order) —
        设置/获取 字符编码的检测顺序
    -   [mb\_encode\_mimeheader](/ref/mbstring.html#mb_encode_mimeheader)
        — 为 MIME 头编码字符串
    -   [mb\_encode\_numericentity](/ref/mbstring.html#mb_encode_numericentity)
        — Encode character to HTML numeric string reference
    -   [mb\_encoding\_aliases](/ref/mbstring.html#mb_encoding_aliases)
        — Get aliases of a known encoding type
    -   [mb\_ereg\_match](/ref/mbstring.html#mb_ereg_match) — Regular
        expression match for multibyte string
    -   [mb\_ereg\_replace\_callback](/ref/mbstring.html#mb_ereg_replace_callback)
        — Perform a regular expression search and replace with multibyte
        support using a callback
    -   [mb\_ereg\_replace](/ref/mbstring.html#mb_ereg_replace) —
        Replace regular expression with multibyte support
    -   [mb\_ereg\_search\_getpos](/ref/mbstring.html#mb_ereg_search_getpos)
        — Returns start point for next regular expression match
    -   [mb\_ereg\_search\_getregs](/ref/mbstring.html#mb_ereg_search_getregs)
        — Retrieve the result from the last multibyte regular expression
        match
    -   [mb\_ereg\_search\_init](/ref/mbstring.html#mb_ereg_search_init)
        — Setup string and regular expression for a multibyte regular
        expression match
    -   [mb\_ereg\_search\_pos](/ref/mbstring.html#mb_ereg_search_pos) —
        Returns position and length of a matched part of the multibyte
        regular expression for a predefined multibyte string
    -   [mb\_ereg\_search\_regs](/ref/mbstring.html#mb_ereg_search_regs)
        — Returns the matched part of a multibyte regular expression
    -   [mb\_ereg\_search\_setpos](/ref/mbstring.html#mb_ereg_search_setpos)
        — Set start point of next regular expression match
    -   [mb\_ereg\_search](/ref/mbstring.html#mb_ereg_search) —
        Multibyte regular expression match for predefined multibyte
        string
    -   [mb\_ereg](/ref/mbstring.html#mb_ereg) — Regular expression
        match with multibyte support
    -   [mb\_eregi\_replace](/ref/mbstring.html#mb_eregi_replace) —
        Replace regular expression with multibyte support ignoring case
    -   [mb\_eregi](/ref/mbstring.html#mb_eregi) — Regular expression
        match ignoring case with multibyte support
    -   [mb\_get\_info](/ref/mbstring.html#mb_get_info) — 获取 mbstring
        的内部设置
    -   [mb\_http\_input](/ref/mbstring.html#mb_http_input) — 检测 HTTP
        输入字符编码
    -   [mb\_http\_output](/ref/mbstring.html#mb_http_output) —
        设置/获取 HTTP 输出字符编码
    -   [mb\_internal\_encoding](/ref/mbstring.html#mb_internal_encoding)
        — 设置/获取内部字符编码
    -   [mb\_language](/ref/mbstring.html#mb_language) —
        设置/获取当前的语言
    -   [mb\_list\_encodings](/ref/mbstring.html#mb_list_encodings) —
        返回所有支持编码的数组
    -   [mb\_ord](/ref/mbstring.html#mb_ord) — Get code point of
        character
    -   [mb\_output\_handler](/ref/mbstring.html#mb_output_handler) —
        在输出缓冲中转换字符编码的回调函数
    -   [mb\_parse\_str](/ref/mbstring.html#mb_parse_str) — 解析
        GET/POST/COOKIE 数据并设置全局变量
    -   [mb\_preferred\_mime\_name](/ref/mbstring.html#mb_preferred_mime_name)
        — 获取 MIME 字符串
    -   [mb\_regex\_encoding](/ref/mbstring.html#mb_regex_encoding) —
        Set/Get character encoding for multibyte regex
    -   [mb\_regex\_set\_options](/ref/mbstring.html#mb_regex_set_options)
        — Set/Get the default options for mbregex functions
    -   [mb\_scrub](/ref/mbstring.html#mb_scrub) — Description
    -   [mb\_send\_mail](/ref/mbstring.html#mb_send_mail) —
        发送编码过的邮件
    -   [mb\_split](/ref/mbstring.html#mb_split) —
        使用正则表达式分割多字节字符串
    -   [mb\_str\_split](/ref/mbstring.html#mb_str_split) — Given a
        multibyte string, return an array of its characters
    -   [mb\_strcut](/ref/mbstring.html#mb_strcut) — 获取字符的一部分
    -   [mb\_strimwidth](/ref/mbstring.html#mb_strimwidth) —
        获取按指定宽度截断的字符串
    -   [mb\_stripos](/ref/mbstring.html#mb_stripos) —
        大小写不敏感地查找字符串在另一个字符串中首次出现的位置
    -   [mb\_stristr](/ref/mbstring.html#mb_stristr) —
        大小写不敏感地查找字符串在另一个字符串里的首次出现
    -   [mb\_strlen](/ref/mbstring.html#mb_strlen) — 获取字符串的长度
    -   [mb\_strpos](/ref/mbstring.html#mb_strpos) —
        查找字符串在另一个字符串中首次出现的位置
    -   [mb\_strrchr](/ref/mbstring.html#mb_strrchr) —
        查找指定字符在另一个字符串中最后一次的出现
    -   [mb\_strrichr](/ref/mbstring.html#mb_strrichr) —
        大小写不敏感地查找指定字符在另一个字符串中最后一次的出现
    -   [mb\_strripos](/ref/mbstring.html#mb_strripos) —
        大小写不敏感地在字符串中查找一个字符串最后出现的位置
    -   [mb\_strrpos](/ref/mbstring.html#mb_strrpos) —
        查找字符串在一个字符串中最后出现的位置
    -   [mb\_strstr](/ref/mbstring.html#mb_strstr) —
        查找字符串在另一个字符串里的首次出现
    -   [mb\_strtolower](/ref/mbstring.html#mb_strtolower) —
        使字符串小写
    -   [mb\_strtoupper](/ref/mbstring.html#mb_strtoupper) —
        使字符串大写
    -   [mb\_strwidth](/ref/mbstring.html#mb_strwidth) —
        返回字符串的宽度
    -   [mb\_substitute\_character](/ref/mbstring.html#mb_substitute_character)
        — 设置/获取替代字符
    -   [mb\_substr\_count](/ref/mbstring.html#mb_substr_count) —
        统计字符串出现的次数
    -   [mb\_substr](/ref/mbstring.html#mb_substr) — 获取部分字符串
