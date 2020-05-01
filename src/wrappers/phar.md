phar://
=======

PHP 归档

### 说明

`phar://` 数据流包装器自 PHP 5.3.0 起开始有效。详细的描述可参见
<a href="/phar/using.html#Using%20Phar%20Archives:%20the%20phar%20stream%20wrapper" class="link">Phar 数据流包装器</a>。

### 用法

-   <span class="simpara">`phar://`</span>

### 可选项

| 属性                                                                      | 支持 |
|---------------------------------------------------------------------------|------|
| 支持 <a href="/filesystem/setup.html#" class="link">allow_url_fopen</a>   | No   |
| 支持 <a href="/filesystem/setup.html#" class="link">allow_url_include</a> | No   |
| 允许读取                                                                  | Yes  |
| 允许写入                                                                  | Yes  |
| 允许附加                                                                  | No   |
| 允许同时读写                                                              | Yes  |
| 支持 <span class="function">stat</span>                                   | Yes  |
| 支持 <span class="function">unlink</span>                                 | Yes  |
| 支持 <span class="function">rename</span>                                 | Yes  |
| 支持 <span class="function">mkdir</span>                                  | Yes  |
| 支持 <span class="function">rmdir</span>                                  | Yes  |

### 参见

-   <a href="/context/phar.html" class="xref">Phar 上下文（context）选项</a>
