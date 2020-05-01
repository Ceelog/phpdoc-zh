范例
====

**目录**

-   [Basic SimpleXML
    usage](/simplexml/examples.html#Basic%20SimpleXML%20usage)
-   [Dealing with XML
    errors](/simplexml/examples.html#Dealing%20with%20XML%20errors)

Basic SimpleXML usage
---------------------

Many examples in this reference require an XML string. Instead of
repeating this string in every example, we put it into a file which we
include in each example. This included file is shown in the following
example section. Alternatively, you could create an XML document and
read it with <span class="function">simplexml\_load\_file</span>.

**示例 \#1 Include file example.php with XML string**

``` php
<?php
$xmlstr = <<<XML
<?xml version='1.0' standalone='yes'?>
<movies>
 <movie>
  <title>PHP: Behind the Parser</title>
  <characters>
   <character>
    <name>Ms. Coder</name>
    <actor>Onlivia Actora</actor>
   </character>
   <character>
    <name>Mr. Coder</name>
    <actor>El Act&#211;r</actor>
   </character>
  </characters>
  <plot>
   So, this language. It's like, a programming language. Or is it a
   scripting language? All is revealed in this thrilling horror spoof
   of a documentary.
  </plot>
  <great-lines>
   <line>PHP solves all my web problems</line>
  </great-lines>
  <rating type="thumbs">7</rating>
  <rating type="stars">5</rating>
 </movie>
</movies>
XML;
?>
```

The simplicity of SimpleXML appears most clearly when one extracts a
string or number from a basic XML document.

**示例 \#2 Getting *\<plot\>***

``` php
<?php
include 'example.php';

$movies = new SimpleXMLElement($xmlstr);

echo $movies->movie[0]->plot;
?>
```

以上例程会输出：


       So, this language. It's like, a programming language. Or is it a
       scripting language? All is revealed in this thrilling horror spoof
       of a documentary.

Accessing elements within an XML document that contain characters not
permitted under PHP's naming convention (e.g. the hyphen) can be
accomplished by encapsulating the element name within braces and the
apostrophe.

**示例 \#3 Getting *\<line\>***

``` php
<?php
include 'example.php';

$movies = new SimpleXMLElement($xmlstr);

echo $movies->movie->{'great-lines'}->line;
?>
```

以上例程会输出：

    PHP solves all my web problems

**示例 \#4 Accessing non-unique elements in SimpleXML**

When multiple instances of an element exist as children of a single
parent element, normal iteration techniques apply.

``` php
<?php
include 'example.php';

$movies = new SimpleXMLElement($xmlstr);

/* For each <character> node, we echo a separate <name>. */
foreach ($movies->movie->characters->character as $character) {
   echo $character->name, ' played by ', $character->actor, PHP_EOL;
}

?>
```

以上例程会输出：

    Ms. Coder played by Onlivia Actora
    Mr. Coder played by El ActÓr

> **Note**:
>
> Properties (*$movies-\>movie* in previous example) are not arrays.
> They are <a href="/class/iterator.html" class="link">iterable</a> and
> <a href="/class/arrayaccess.html" class="link">accessible</a> objects.

**示例 \#5 Using attributes**

So far, we have only covered the work of reading element names and their
values. SimpleXML can also access element attributes. Access attributes
of an element just as you would elements of an <span
class="type">array</span>.

``` php
<?php
include 'example.php';

$movies = new SimpleXMLElement($xmlstr);

/* Access the <rating> nodes of the first movie.
 * Output the rating scale, too. */
foreach ($movies->movie[0]->rating as $rating) {
    switch((string) $rating['type']) { // Get attributes as element indices
    case 'thumbs':
        echo $rating, ' thumbs up';
        break;
    case 'stars':
        echo $rating, ' stars';
        break;
    }
}
?>
```

以上例程会输出：

    7 thumbs up5 stars

**示例 \#6 Comparing Elements and Attributes with Text**

To compare an element or attribute with a string or pass it into a
function that requires a string, you must cast it to a string using
*(string)*. Otherwise, PHP treats the element as an object.

``` php
<?php
include 'example.php';

$movies = new SimpleXMLElement($xmlstr);

if ((string) $movies->movie->title == 'PHP: Behind the Parser') {
    print 'My favorite movie.';
}

echo htmlentities((string) $movies->movie->title);
?>
```

以上例程会输出：

    My favorite movie.PHP: Behind the Parser

**示例 \#7 Comparing Two Elements**

Two SimpleXMLElements are considered different even if they point to the
same element since PHP 5.2.0.

``` php
<?php
include 'example.php';

$movies1 = new SimpleXMLElement($xmlstr);
$movies2 = new SimpleXMLElement($xmlstr);
var_dump($movies1 == $movies2); // false since PHP 5.2.0
?>
```

以上例程会输出：

    bool(false)

**示例 \#8 Using XPath**

SimpleXML includes built-in XPath support. To find all *\<character\>*
elements:

``` php
<?php
include 'example.php';

$movies = new SimpleXMLElement($xmlstr);

foreach ($movies->xpath('//character') as $character) {
    echo $character->name, ' played by ', $character->actor, PHP_EOL;
}
?>
```

'*//*' serves as a wildcard. To specify absolute paths, omit one of the
slashes.

以上例程会输出：

    Ms. Coder played by Onlivia Actora
    Mr. Coder played by El ActÓr

**示例 \#9 Setting values**

Data in SimpleXML doesn't have to be constant. The object allows for
manipulation of all of its elements.

``` php
<?php
include 'example.php';
$movies = new SimpleXMLElement($xmlstr);

$movies->movie[0]->characters->character[0]->name = 'Miss Coder';

echo $movies->asXML();
?>
```

以上例程会输出：

    <?xml version="1.0" standalone="yes"?>
    <movies>
     <movie>
      <title>PHP: Behind the Parser</title>
      <characters>
       <character>
        <name>Miss Coder</name>
        <actor>Onlivia Actora</actor>
       </character>
       <character>
        <name>Mr. Coder</name>
        <actor>El Act&#xD3;r</actor>
       </character>
      </characters>
      <plot>
       So, this language. It's like, a programming language. Or is it a
       scripting language? All is revealed in this thrilling horror spoof
       of a documentary.
      </plot>
      <great-lines>
       <line>PHP solves all my web problems</line>
      </great-lines>
      <rating type="thumbs">7</rating>
      <rating type="stars">5</rating>
     </movie>
    </movies>

**示例 \#10 Adding elements and attributes**

Since PHP 5.1.3, SimpleXML has had the ability to easily add children
and attributes.

``` php
<?php
include 'example.php';
$movies = new SimpleXMLElement($xmlstr);

$character = $movies->movie[0]->characters->addChild('character');
$character->addChild('name', 'Mr. Parser');
$character->addChild('actor', 'John Doe');

$rating = $movies->movie[0]->addChild('rating', 'PG');
$rating->addAttribute('type', 'mpaa');

echo $movies->asXML();
?>
```

以上例程会输出：

    <?xml version="1.0" standalone="yes"?>
    <movies>
     <movie>
      <title>PHP: Behind the Parser</title>
      <characters>
       <character>
        <name>Ms. Coder</name>
        <actor>Onlivia Actora</actor>
       </character>
       <character>
        <name>Mr. Coder</name>
        <actor>El Act&#xD3;r</actor>
       </character>
      <character><name>Mr. Parser</name><actor>John Doe</actor></character></characters>
      <plot>
       So, this language. It's like, a programming language. Or is it a
       scripting language? All is revealed in this thrilling horror spoof
       of a documentary.
      </plot>
      <great-lines>
       <line>PHP solves all my web problems</line>
      </great-lines>
      <rating type="thumbs">7</rating>
      <rating type="stars">5</rating>
     <rating type="mpaa">PG</rating></movie>
    </movies>

**示例 \#11 DOM Interoperability**

PHP has a mechanism to convert XML nodes between SimpleXML and DOM
formats. This example shows how one might change a DOM element to
SimpleXML.

``` php
<?php
$dom = new DOMDocument;
$dom->loadXML('<books><book><title>blah</title></book></books>');
if (!$dom) {
    echo 'Error while parsing the document';
    exit;
}

$books = simplexml_import_dom($dom);

echo $books->book[0]->title;
?>
```

以上例程会输出：

    blah

Dealing with XML errors
-----------------------

Dealing with XML errors when loading documents is a very simple task.
Using the <a href="/book/libxml.html" class="link">libxml</a>
functionality it is possible to suppress all XML errors when loading the
document and then iterate over the errors.

The <span class="classname">libXMLError</span> object, returned by <span
class="function">libxml\_get\_errors</span>, contains several properties
including the
<a href="/class/libxmlerror.html#" class="link">message</a>,
<a href="/class/libxmlerror.html#" class="link">line</a> and
<a href="/class/libxmlerror.html#" class="link">column</a> (position) of
the error.

**示例 \#1 Loading broken XML string**

``` php
<?php
libxml_use_internal_errors(true);
$sxe = simplexml_load_string("<?xml version='1.0'><broken><xml></broken>");
if ($sxe === false) {
    echo "Failed loading XML\n";
    foreach(libxml_get_errors() as $error) {
        echo "\t", $error->message;
    }
}
?>
```

以上例程会输出：

    Failed loading XML
        Blank needed here
        parsing XML declaration: '?>' expected
        Opening and ending tag mismatch: xml line 1 and broken
        Premature end of data in tag broken line 1

参见
----

-   <span class="function">libxml\_use\_internal\_errors</span>
-   <span class="function">libxml\_get\_errors</span>
-   <a href="/class/libxmlerror.html" class="xref">libXMLError</a>
