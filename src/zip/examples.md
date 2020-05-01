范例
====

**示例 \#1 创建一个 Zip 归档**

``` php
<?php

$zip = new ZipArchive();
$filename = "./test112.zip";

if ($zip->open($filename, ZIPARCHIVE::CREATE)!==TRUE) {
    exit("cannot open <$filename>\n");
}

$zip->addFromString("testfilephp.txt" . time(), "#1 This is a test string added as testfilephp.txt.\n");
$zip->addFromString("testfilephp2.txt" . time(), "#2 This is a test string added as testfilephp2.txt.\n");
$zip->addFile($thisdir . "/too.php","/testfromfile.php");
echo "numfiles: " . $zip->numFiles . "\n";
echo "status:" . $zip->status . "\n";
$zip->close();
?>
```

**示例 \#2 输出文档细节和列表**

``` php
<?php
$za = new ZipArchive();

$za->open('test_with_comment.zip');
print_r($za);
var_dump($za);
echo "numFiles: " . $za->numFiles . "\n";
echo "status: " . $za->status  . "\n";
echo "statusSys: " . $za->statusSys . "\n";
echo "filename: " . $za->filename . "\n";
echo "comment: " . $za->comment . "\n";

for ($i=0; $i<$za->numFiles;$i++) {
    echo "index: $i\n";
    print_r($za->statIndex($i));
}
echo "numFile:" . $za->numFiles . "\n";
?>
```

**示例 \#3 Zip 流封装，读取一个 OpenOffice 文件的元信息**

``` php
<?php
$reader = new XMLReader();

$reader->open('zip://' . dirname(__FILE__) . '/test.odt#meta.xml');
$odt_meta = array();
while ($reader->read()) {
    if ($reader->nodeType == XMLREADER::ELEMENT) {
        $elm = $reader->name;
    } else {
        if ($reader->nodeType == XMLREADER::END_ELEMENT && $reader->name == 'office:meta') {
            break;
        }
        if (!trim($reader->value)) {
            continue;
        }
        $odt_meta[$elm] = $reader->value;
    }
}
print_r($odt_meta);
?>
```

此例使用了旧的 API（PHP 4），它打开了一个 ZIP
文件归档，读取归档里的每个文件，并输出文件内容。此例用到的 `test2.zip`
文档是 ZZIPlib 源分布里测试文档中的一个。

**示例 \#4 Zip 使用范例**

``` php
<?php

$zip = zip_open("/tmp/test2.zip");

if ($zip) {
    while ($zip_entry = zip_read($zip)) {
        echo "Name:               " . zip_entry_name($zip_entry) . "\n";
        echo "Actual Filesize:    " . zip_entry_filesize($zip_entry) . "\n";
        echo "Compressed Size:    " . zip_entry_compressedsize($zip_entry) . "\n";
        echo "Compression Method: " . zip_entry_compressionmethod($zip_entry) . "\n";

        if (zip_entry_open($zip, $zip_entry, "r")) {
            echo "File Contents:\n";
            $buf = zip_entry_read($zip_entry, zip_entry_filesize($zip_entry));
            echo "$buf\n";

            zip_entry_close($zip_entry);
        }
        echo "\n";

    }

    zip_close($zip);

}
?>
```
