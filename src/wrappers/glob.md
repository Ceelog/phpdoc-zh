glob://
=======

查找匹配的文件路径模式

### 说明

`glob:` 数据流包装器自 PHP 5.3.0 起开始有效。

### 用法

-   <span class="simpara">`glob://`</span>

### 可选项

| 属性                                                                        | 支持 |
|-----------------------------------------------------------------------------|------|
| 受限于 <a href="/filesystem/setup.html#" class="link">allow_url_fopen</a>   | No   |
| 受限于 <a href="/filesystem/setup.html#" class="link">allow_url_include</a> | No   |
| 允许读取                                                                    | No   |
| 允许写入                                                                    | No   |
| 允许附加                                                                    | No   |
| 允许同时读写                                                                | No   |
| 支持 <span class="function">stat</span>                                     | No   |
| 支持 <span class="function">unlink</span>                                   | No   |
| 支持 <span class="function">rename</span>                                   | No   |
| 支持 <span class="function">mkdir</span>                                    | No   |
| 支持 <span class="function">rmdir</span>                                    | No   |

### 范例

**示例 \#1 基本用法**

``` php
<?php
// 循环 ext/spl/examples/ 目录里所有 *.php 文件
// 并打印文件名和文件尺寸
$it = new DirectoryIterator("glob://ext/spl/examples/*.php");
foreach($it as $f) {
    printf("%s: %.1FK\n", $f->getFilename(), $f->getSize()/1024);
}
?>
```

    tree.php: 1.0K
    findregex.php: 0.6K
    findfile.php: 0.7K
    dba_dump.php: 0.9K
    nocvsdir.php: 1.1K
    phar_from_dir.php: 1.0K
    ini_groups.php: 0.9K
    directorytree.php: 0.9K
    dba_array.php: 1.1K
    class_tree.php: 1.8K
