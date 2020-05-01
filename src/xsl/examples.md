范例
====

**目录**

-   [Example collection.xml and collection.xsl
    files](/xsl/examples.html#Example%20collection.xml%20and%20collection.xsl%20files)
-   [Error handling with libxml error handling
    functions](/xsl/examples.html#Error%20handling%20with%20libxml%20error%20handling%20functions)

Example collection.xml and collection.xsl files
-----------------------------------------------

Many examples in this reference require both an XML and an XSL file. We
will use `collection.xml` and `collection.xsl` that contains the
following:

**示例 \#1 collection.xml**

``` xml
<collection>
 <cd>
  <title>Fight for your mind</title>
  <artist>Ben Harper</artist>
  <year>1995</year>
 </cd>
 <cd>
  <title>Electric Ladyland</title>
  <artist>Jimi Hendrix</artist>
  <year>1997</year>
 </cd>
</collection>
```

**示例 \#2 collection.xsl**

``` xml
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
 <xsl:param name="owner" select="'Nicolas Eliaszewicz'"/>
 <xsl:output method="html" encoding="iso-8859-1" indent="no"/>
 <xsl:template match="collection">
  Hey! Welcome to <xsl:value-of select="$owner"/>'s sweet CD collection! 
  <xsl:apply-templates/>
 </xsl:template>
 <xsl:template match="cd">
  <h1><xsl:value-of select="title"/></h1>
  <h2>by <xsl:value-of select="artist"/> - <xsl:value-of select="year"/></h2>
  <hr />
 </xsl:template>
</xsl:stylesheet>
```

Error handling with libxml error handling functions
---------------------------------------------------

libxml offers a number of functions for handling errors, which can be
employed to capture and deal with errors in XSLT processing.

**示例 \#1 fruits.xml**

A valid XML file.

``` xml
<fruits>
 <fruit>Apple</fruit>
 <fruit>Banana</fruit>
 <fruit>Cherry</fruit>
</fruits>
```

**示例 \#2 fruits.xsl**

Contains an invalid select expression.

``` xml
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
 <xsl:output method="html" encoding="utf-8" indent="no"/>
 <xsl:template match="fruits">
  <ul>
   <xsl:apply-templates/>
  </ul>
 </xsl:template>
 <xsl:template match="fruit">
  <li><xsl:value-of select="THIS IS A DELIBERATE ERROR!"/></li>
 </xsl:template>
</xsl:stylesheet>
```

**示例 \#3 Collating and printing errors**

The example below captures and displays libxml errors raised when
calling <span class="methodname">XSLTProcessor::importStyleSheet</span>
with a stylesheet containing an error.

``` php
<?php

$xmldoc = new DOMDocument();
$xsldoc = new DOMDocument();
$xsl = new XSLTProcessor();

$xmldoc->loadXML('fruits.xml');
$xsldoc->loadXML('fruits.xsl');

libxml_use_internal_errors(true);
$result = $xsl->importStyleSheet($xsldoc);
if (!$result) {
    foreach (libxml_get_errors() as $error) {
        echo "Libxml error: {$error->message}\n";
    }
}
libxml_use_internal_errors(false);

if ($result) {
    echo $xsl->transformToXML($xmldoc);
}

?>
```

以上例程的输出类似于：

    Libxml error: Invalid expression

    Libxml error: compilation error: file fruits.xsl line 9 element value-of
    Libxml error: xsl:value-of : could not compile select expression 'THIS IS A DELIBERATE ERROR!'
