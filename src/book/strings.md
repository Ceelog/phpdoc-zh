字符串
======

**目录**

-   [简介](/intro/strings.html)
-   [安装／配置](/strings/setup.html)
    -   [需求](/strings/setup.html#需求)
    -   [安装](/strings/setup.html#安装)
    -   [运行时配置](/strings/setup.html#运行时配置)
    -   [资源类型](/strings/setup.html#资源类型)
-   [预定义常量](/string/constants.html)
-   [字符串 函数](/ref/strings.html)
    -   [addcslashes](/ref/strings.html#addcslashes) — 以 C
        语言风格使用反斜线转义字符串中的字符
    -   [addslashes](/ref/strings.html#addslashes) —
        使用反斜线引用字符串
    -   [bin2hex](/ref/strings.html#bin2hex) —
        函数把包含数据的二进制字符串转换为十六进制值
    -   [chop](/ref/strings.html#chop) — rtrim 的别名
    -   [chr](/ref/strings.html#chr) — 返回指定的字符
    -   [chunk\_split](/ref/strings.html#chunk_split) —
        将字符串分割成小块
    -   [convert\_cyr\_string](/ref/strings.html#convert_cyr_string) —
        将字符由一种 Cyrillic 字符转换成另一种
    -   [convert\_uudecode](/ref/strings.html#convert_uudecode) —
        解码一个 uuencode 编码的字符串
    -   [convert\_uuencode](/ref/strings.html#convert_uuencode) — 使用
        uuencode 编码一个字符串
    -   [count\_chars](/ref/strings.html#count_chars) —
        返回字符串所用字符的信息
    -   [crc32](/ref/strings.html#crc32) — 计算一个字符串的 crc32 多项式
    -   [crypt](/ref/strings.html#crypt) — 单向字符串散列
    -   [echo](/ref/strings.html#echo) — 输出一个或多个字符串
    -   [explode](/ref/strings.html#explode) —
        使用一个字符串分割另一个字符串
    -   [fprintf](/ref/strings.html#fprintf) —
        将格式化后的字符串写入到流
    -   [get\_html\_translation\_table](/ref/strings.html#get_html_translation_table)
        — 返回使用 htmlspecialchars 和 htmlentities 后的转换表
    -   [hebrev](/ref/strings.html#hebrev) —
        将逻辑顺序希伯来文（logical-Hebrew）转换为视觉顺序希伯来文（visual-Hebrew）
    -   [hebrevc](/ref/strings.html#hebrevc) —
        将逻辑顺序希伯来文（logical-Hebrew）转换为视觉顺序希伯来文（visual-Hebrew），并且转换换行符
    -   [hex2bin](/ref/strings.html#hex2bin) —
        转换十六进制字符串为二进制字符串
    -   [html\_entity\_decode](/ref/strings.html#html_entity_decode) —
        Convert HTML entities to their corresponding characters
    -   [htmlentities](/ref/strings.html#htmlentities) — 将字符转换为
        HTML 转义字符
    -   [htmlspecialchars\_decode](/ref/strings.html#htmlspecialchars_decode)
        — 将特殊的 HTML 实体转换回普通字符
    -   [htmlspecialchars](/ref/strings.html#htmlspecialchars) —
        将特殊字符转换为 HTML 实体
    -   [implode](/ref/strings.html#implode) —
        将一个一维数组的值转化为字符串
    -   [join](/ref/strings.html#join) — 别名 implode
    -   [lcfirst](/ref/strings.html#lcfirst) —
        使一个字符串的第一个字符小写
    -   [levenshtein](/ref/strings.html#levenshtein) —
        计算两个字符串之间的编辑距离
    -   [localeconv](/ref/strings.html#localeconv) — Get numeric
        formatting information
    -   [ltrim](/ref/strings.html#ltrim) —
        删除字符串开头的空白字符（或其他字符）
    -   [md5\_file](/ref/strings.html#md5_file) — 计算指定文件的 MD5
        散列值
    -   [md5](/ref/strings.html#md5) — 计算字符串的 MD5 散列值
    -   [metaphone](/ref/strings.html#metaphone) — Calculate the
        metaphone key of a string
    -   [money\_format](/ref/strings.html#money_format) —
        将数字格式化成货币字符串
    -   [nl\_langinfo](/ref/strings.html#nl_langinfo) — Query language
        and locale information
    -   [nl2br](/ref/strings.html#nl2br) — 在字符串所有新行之前插入 HTML
        换行标记
    -   [number\_format](/ref/strings.html#number_format) —
        以千位分隔符方式格式化一个数字
    -   [ord](/ref/strings.html#ord) — 转换字符串第一个字节为 0-255
        之间的值
    -   [parse\_str](/ref/strings.html#parse_str) —
        将字符串解析成多个变量
    -   [print](/ref/strings.html#print) — 输出字符串
    -   [printf](/ref/strings.html#printf) — 输出格式化字符串
    -   [quoted\_printable\_decode](/ref/strings.html#quoted_printable_decode)
        — 将 quoted-printable 字符串转换为 8-bit 字符串
    -   [quoted\_printable\_encode](/ref/strings.html#quoted_printable_encode)
        — 将 8-bit 字符串转换成 quoted-printable 字符串
    -   [quotemeta](/ref/strings.html#quotemeta) — 转义元字符集
    -   [rtrim](/ref/strings.html#rtrim) —
        删除字符串末端的空白字符（或者其他字符）
    -   [setlocale](/ref/strings.html#setlocale) — 设置地区信息
    -   [sha1\_file](/ref/strings.html#sha1_file) — 计算文件的 sha1
        散列值
    -   [sha1](/ref/strings.html#sha1) — 计算字符串的 sha1 散列值
    -   [similar\_text](/ref/strings.html#similar_text) —
        计算两个字符串的相似度
    -   [soundex](/ref/strings.html#soundex) — Calculate the soundex key
        of a string
    -   [sprintf](/ref/strings.html#sprintf) — Return a formatted string
    -   [sscanf](/ref/strings.html#sscanf) — 根据指定格式解析输入的字符
    -   [str\_contains](/ref/strings.html#str_contains) — Determine if a
        string contains a given substring
    -   [str\_ends\_with](/ref/strings.html#str_ends_with) — Checks if a
        string ends with a given substring
    -   [str\_getcsv](/ref/strings.html#str_getcsv) — 解析 CSV
        字符串为一个数组
    -   [str\_ireplace](/ref/strings.html#str_ireplace) — str\_replace
        的忽略大小写版本
    -   [str\_pad](/ref/strings.html#str_pad) —
        使用另一个字符串填充字符串为指定长度
    -   [str\_repeat](/ref/strings.html#str_repeat) — 重复一个字符串
    -   [str\_replace](/ref/strings.html#str_replace) — 子字符串替换
    -   [str\_rot13](/ref/strings.html#str_rot13) — 对字符串执行 ROT13
        转换
    -   [str\_shuffle](/ref/strings.html#str_shuffle) —
        随机打乱一个字符串
    -   [str\_split](/ref/strings.html#str_split) — 将字符串转换为数组
    -   [str\_starts\_with](/ref/strings.html#str_starts_with) — Checks
        if a string starts with a given substring
    -   [str\_word\_count](/ref/strings.html#str_word_count) —
        返回字符串中单词的使用情况
    -   [strcasecmp](/ref/strings.html#strcasecmp) —
        二进制安全比较字符串（不区分大小写）
    -   [strchr](/ref/strings.html#strchr) — 别名 strstr
    -   [strcmp](/ref/strings.html#strcmp) — 二进制安全字符串比较
    -   [strcoll](/ref/strings.html#strcoll) — 基于区域设置的字符串比较
    -   [strcspn](/ref/strings.html#strcspn) —
        获取不匹配遮罩的起始子字符串的长度
    -   [strip\_tags](/ref/strings.html#strip_tags) — 从字符串中去除
        HTML 和 PHP 标记
    -   [stripcslashes](/ref/strings.html#stripcslashes) —
        反引用一个使用 addcslashes 转义的字符串
    -   [stripos](/ref/strings.html#stripos) —
        查找字符串首次出现的位置（不区分大小写）
    -   [stripslashes](/ref/strings.html#stripslashes) —
        反引用一个引用字符串
    -   [stristr](/ref/strings.html#stristr) — strstr
        函数的忽略大小写版本
    -   [strlen](/ref/strings.html#strlen) — 获取字符串长度
    -   [strnatcasecmp](/ref/strings.html#strnatcasecmp) —
        使用“自然顺序”算法比较字符串（不区分大小写）
    -   [strnatcmp](/ref/strings.html#strnatcmp) —
        使用自然排序算法比较字符串
    -   [strncasecmp](/ref/strings.html#strncasecmp) —
        二进制安全比较字符串开头的若干个字符（不区分大小写）
    -   [strncmp](/ref/strings.html#strncmp) —
        二进制安全比较字符串开头的若干个字符
    -   [strpbrk](/ref/strings.html#strpbrk) —
        在字符串中查找一组字符的任何一个字符
    -   [strpos](/ref/strings.html#strpos) — 查找字符串首次出现的位置
    -   [strrchr](/ref/strings.html#strrchr) —
        查找指定字符在字符串中的最后一次出现
    -   [strrev](/ref/strings.html#strrev) — 反转字符串
    -   [strripos](/ref/strings.html#strripos) —
        计算指定字符串在目标字符串中最后一次出现的位置（不区分大小写）
    -   [strrpos](/ref/strings.html#strrpos) —
        计算指定字符串在目标字符串中最后一次出现的位置
    -   [strspn](/ref/strings.html#strspn) —
        计算字符串中全部字符都存在于指定字符集合中的第一段子串的长度。
    -   [strstr](/ref/strings.html#strstr) — 查找字符串的首次出现
    -   [strtok](/ref/strings.html#strtok) — 标记分割字符串
    -   [strtolower](/ref/strings.html#strtolower) — 将字符串转化为小写
    -   [strtoupper](/ref/strings.html#strtoupper) — 将字符串转化为大写
    -   [strtr](/ref/strings.html#strtr) — 转换指定字符
    -   [substr\_compare](/ref/strings.html#substr_compare) —
        二进制安全比较字符串（从偏移位置比较指定长度）
    -   [substr\_count](/ref/strings.html#substr_count) —
        计算字串出现的次数
    -   [substr\_replace](/ref/strings.html#substr_replace) —
        替换字符串的子串
    -   [substr](/ref/strings.html#substr) — 返回字符串的子串
    -   [trim](/ref/strings.html#trim) —
        去除字符串首尾处的空白字符（或者其他字符）
    -   [ucfirst](/ref/strings.html#ucfirst) —
        将字符串的首字母转换为大写
    -   [ucwords](/ref/strings.html#ucwords) —
        将字符串中每个单词的首字母转换为大写
    -   [vfprintf](/ref/strings.html#vfprintf) — 将格式化字符串写入流
    -   [vprintf](/ref/strings.html#vprintf) — 输出格式化字符串
    -   [vsprintf](/ref/strings.html#vsprintf) — 返回格式化字符串
    -   [wordwrap](/ref/strings.html#wordwrap) —
        打断字符串为指定数量的字串
-   [更新日志](/changelog/strings.html)
