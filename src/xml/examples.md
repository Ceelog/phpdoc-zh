范例
====

**目录**

-   [XML 元素结构例程](/xml/examples.html#XML%20元素结构例程)
-   [XML 标签映射例程](/xml/examples.html#XML%20标签映射例程)
-   [XML 外部实体例程](/xml/examples.html#XML%20外部实体例程)

XML 元素结构例程
----------------

第一个例程缩进显示文档中的开始元素结构。

**示例 \#1 显示 XML 元素结构**

``` php
<?php
$file = "data.xml";
$depth = array();

function startElement($parser, $name, $attrs) 
{
    global $depth;
    for ($i = 0; $i < $depth[$parser]; $i++) {
        echo "  ";
    }
    echo "$name\n";
    $depth[$parser]++;
}

function endElement($parser, $name) 
{
    global $depth;
    $depth[$parser]--;
}

$xml_parser = xml_parser_create();
xml_set_element_handler($xml_parser, "startElement", "endElement");
if (!($fp = fopen($file, "r"))) {
    die("could not open XML input");
}

while ($data = fread($fp, 4096)) {
    if (!xml_parse($xml_parser, $data, feof($fp))) {
        die(sprintf("XML error: %s at line %d",
                    xml_error_string(xml_get_error_code($xml_parser)),
                    xml_get_current_line_number($xml_parser)));
    }
}
xml_parser_free($xml_parser);
?>
```

XML 标签映射例程
----------------

**示例 \#1 将 XML 映射为 HTML**

此例程直接地将 XML 标签映射为 HTML 标签。
在“map\_array”中未找到的元素将被忽略。 当然，此例程只针对特定的 XML
文档类型起作用。

``` php
<?php
$file = "data.xml";
$map_array = array(
    "BOLD"     => "B",
    "EMPHASIS" => "I",
    "LITERAL"  => "TT"
);

function startElement($parser, $name, $attrs) 
{
    global $map_array;
    if (isset($map_array[$name])) {
        echo "<$map_array[$name]>";
    }
}

function endElement($parser, $name) 
{
    global $map_array;
    if (isset($map_array[$name])) {
        echo "</$map_array[$name]>";
    }
}

function characterData($parser, $data) 
{
    echo $data;
}

$xml_parser = xml_parser_create();
// use case-folding so we are sure to find the tag in $map_array
xml_parser_set_option($xml_parser, XML_OPTION_CASE_FOLDING, true);
xml_set_element_handler($xml_parser, "startElement", "endElement");
xml_set_character_data_handler($xml_parser, "characterData");
if (!($fp = fopen($file, "r"))) {
    die("could not open XML input");
}

while ($data = fread($fp, 4096)) {
    if (!xml_parse($xml_parser, $data, feof($fp))) {
        die(sprintf("XML error: %s at line %d",
                    xml_error_string(xml_get_error_code($xml_parser)),
                    xml_get_current_line_number($xml_parser)));
    }
}
xml_parser_free($xml_parser);
?>
```

XML 外部实体例程
----------------

此例程用于加亮 XML
代码。举例说明如何使用外部实体引用来包含和解析其他文档，
及处理指令是如何被处理的，及判断处理指令所包含代码是否“可信任”的一种方法

用于此例程的 XML 文档位于此例程的下方(`xmltest.xml` 和 `xmltest2.xml`)。

**示例 \#1 外部实体例程**

``` php
<?php
$file = "xmltest.xml";

function trustedFile($file) 
{
    // 仅信任本地文件
    if (!preg_match("@^([a-z]+)\:\/\/@i", $file) 
        && fileowner($file) == getmyuid()) {
            return true;
    }
    return false;
}

function startElement($parser, $name, $attribs) 
{
    echo "&lt;<font color=\"#0000cc\">$name</font>";
    if (count($attribs)) {
        foreach ($attribs as $k => $v) {
            echo " <font color=\"#009900\">$k</font>=\"<font 
                   color=\"#990000\">$v</font>\"";
        }
    }
    echo "&gt;";
}

function endElement($parser, $name) 
{
    echo "&lt;/<font color=\"#0000cc\">$name</font>&gt;";
}

function characterData($parser, $data) 
{
    echo "<b>$data</b>";
}

function PIHandler($parser, $target, $data) 
{
    switch (strtolower($target)) {
        case "php":
            global $parser_file;
            // 如何要解析的文档是“可信任”的, 则说明可安全
            // 地执行其内部的 PHP 代码。否则，显示代码内容。
            if (trustedFile($parser_file[$parser])) {
                eval($data);
            } else {
                printf("Untrusted PHP code: <i>%s</i>", 
                        htmlspecialchars($data));
            }
            break;
    }
}

function defaultHandler($parser, $data) 
{
    if (substr($data, 0, 1) == "&" && substr($data, -1, 1) == ";") {
        printf('<font color="#aa00aa">%s</font>', 
                htmlspecialchars($data));
    } else {
        printf('<font size="-1">%s</font>', 
                htmlspecialchars($data));
    }
}

function externalEntityRefHandler($parser, $openEntityNames, $base, $systemId,
                                  $publicId) {
    if ($systemId) {
        if (!list($parser, $fp) = new_xml_parser($systemId)) {
            printf("Could not open entity %s at %s\n", $openEntityNames,
                   $systemId);
            return false;
        }
        while ($data = fread($fp, 4096)) {
            if (!xml_parse($parser, $data, feof($fp))) {
                printf("XML error: %s at line %d while parsing entity %s\n",
                       xml_error_string(xml_get_error_code($parser)),
                       xml_get_current_line_number($parser), $openEntityNames);
                xml_parser_free($parser);
                return false;
            }
        }
        xml_parser_free($parser);
        return true;
    }
    return false;
}

function new_xml_parser($file) 
{
    global $parser_file;

    $xml_parser = xml_parser_create();
    xml_parser_set_option($xml_parser, XML_OPTION_CASE_FOLDING, 1);
    xml_set_element_handler($xml_parser, "startElement", "endElement");
    xml_set_character_data_handler($xml_parser, "characterData");
    xml_set_processing_instruction_handler($xml_parser, "PIHandler");
    xml_set_default_handler($xml_parser, "defaultHandler");
    xml_set_external_entity_ref_handler($xml_parser, "externalEntityRefHandler");
    
    if (!($fp = @fopen($file, "r"))) {
        return false;
    }
    if (!is_array($parser_file)) {
        settype($parser_file, "array");
    }
    $parser_file[$xml_parser] = $file;
    return array($xml_parser, $fp);
}

if (!(list($xml_parser, $fp) = new_xml_parser($file))) {
    die("could not open XML input");
}

echo "<pre>";
while ($data = fread($fp, 4096)) {
    if (!xml_parse($xml_parser, $data, feof($fp))) {
        die(sprintf("XML error: %s at line %d\n",
                    xml_error_string(xml_get_error_code($xml_parser)),
                    xml_get_current_line_number($xml_parser)));
    }
}
echo "</pre>";
echo "parse complete\n";
xml_parser_free($xml_parser);

?>
```

**示例 \#2 xmltest.xml**

``` xml
<?xml version='1.0'?>
<!DOCTYPE chapter SYSTEM "/just/a/test.dtd" [
<!ENTITY plainEntity "FOO entity">
<!ENTITY systemEntity SYSTEM "xmltest2.xml">
]>
<chapter>
 <TITLE>Title &plainEntity;</TITLE>
 <para>
  <informaltable>
   <tgroup cols="3">
    <tbody>
     <row><entry>a1</entry><entry morerows="1">b1</entry><entry>c1</entry></row>
     <row><entry>a2</entry><entry>c2</entry></row>
     <row><entry>a3</entry><entry>b3</entry><entry>c3</entry></row>
    </tbody>
   </tgroup>
  </informaltable>
 </para>
 &systemEntity;
 <section id="about">
  <title>About this Document</title>
  <para>
   <!-- this is a comment -->
   <?php echo 'Hi!  This is PHP version ' . phpversion(); ?>
  </para>
 </section>
</chapter>
```

此文件包含在 `xmltest.xml` 中:

**示例 \#3 xmltest2.xml**

``` xml
<?xml version="1.0"?>
<!DOCTYPE foo [
<!ENTITY testEnt "test entity">
]>
<foo>
   <element attrib="value"/>
   &testEnt;
   <?php echo "This is some more PHP code being executed."; ?>
</foo>
```
