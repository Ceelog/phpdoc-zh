Mailparse
=========

**目录**

-   [简介](/intro/mailparse.html)
-   [安装／配置](/mailparse/setup.html)
    -   [需求](/mailparse/setup.html#需求)
    -   [安装](/mailparse/setup.html#安装)
    -   [运行时配置](/mailparse/setup.html#运行时配置)
    -   [资源类型](/mailparse/setup.html#资源类型)
-   [预定义常量](/mailparse/constants.html)
-   [Mailparse 函数](/ref/mailparse.html)
    -   [mailparse\_determine\_best\_xfer\_encoding](/ref/mailparse.html#mailparse_determine_best_xfer_encoding)
        — Gets the best way of encoding
    -   [mailparse\_msg\_create](/ref/mailparse.html#mailparse_msg_create)
        — Create a mime mail resource
    -   [mailparse\_msg\_extract\_part\_file](/ref/mailparse.html#mailparse_msg_extract_part_file)
        — Extracts/decodes a message section
    -   [mailparse\_msg\_extract\_part](/ref/mailparse.html#mailparse_msg_extract_part)
        — Extracts/decodes a message section
    -   [mailparse\_msg\_extract\_whole\_part\_file](/ref/mailparse.html#mailparse_msg_extract_whole_part_file)
        — Extracts a message section including headers without decoding
        the transfer encoding
    -   [mailparse\_msg\_free](/ref/mailparse.html#mailparse_msg_free) —
        Frees a MIME resource
    -   [mailparse\_msg\_get\_part\_data](/ref/mailparse.html#mailparse_msg_get_part_data)
        — Returns an associative array of info about the message
    -   [mailparse\_msg\_get\_part](/ref/mailparse.html#mailparse_msg_get_part)
        — Returns a handle on a given section in a mimemessage
    -   [mailparse\_msg\_get\_structure](/ref/mailparse.html#mailparse_msg_get_structure)
        — Returns an array of mime section names in the supplied message
    -   [mailparse\_msg\_parse\_file](/ref/mailparse.html#mailparse_msg_parse_file)
        — Parses a file
    -   [mailparse\_msg\_parse](/ref/mailparse.html#mailparse_msg_parse)
        — Incrementally parse data into buffer
    -   [mailparse\_rfc822\_parse\_addresses](/ref/mailparse.html#mailparse_rfc822_parse_addresses)
        — Parse RFC 822 compliant addresses
    -   [mailparse\_stream\_encode](/ref/mailparse.html#mailparse_stream_encode)
        — Streams data from source file pointer, apply encoding and
        write to destfp
    -   [mailparse\_uudecode\_all](/ref/mailparse.html#mailparse_uudecode_all)
        — Scans the data from fp and extract each embedded uuencoded
        file
