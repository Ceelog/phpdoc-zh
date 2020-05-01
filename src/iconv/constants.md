预定义常量
==========

自 <span class="application">PHP</span> 4.3.0
起，它能够在运行时识别此扩展使用了哪种实现（implementation）。

| 名称                | 类型                             | 描述                         |
|---------------------|----------------------------------|------------------------------|
| **`ICONV_IMPL`**    | <span class="type">string</span> | 实现（implementation）的名称 |
| **`ICONV_VERSION`** | <span class="type">string</span> | 实现（implementation）的版本 |

> **Note**:
>
> 通过这些常量编写依赖于实现的脚本是极其不建议的。

自 <span class="application">PHP</span> 5.0.0 起，以下常量同样有效：

| 名称                                      | 类型                              | 描述                                                              |
|-------------------------------------------|-----------------------------------|-------------------------------------------------------------------|
| **`ICONV_MIME_DECODE_STRICT`**            | <span class="type">integer</span> | 使用于 <span class="function">iconv\_mime\_decode</span> 的位掩码 |
| **`ICONV_MIME_DECODE_CONTINUE_ON_ERROR`** | <span class="type">integer</span> | 使用于 <span class="function">iconv\_mime\_decode</span> 的位掩码 |
