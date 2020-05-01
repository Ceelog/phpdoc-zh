范例
====

**目录**

-   [Basic PECL/haru
    example](/haru/examples.html#Basic%20PECL/haru%20example)

Basic PECL/haru example
-----------------------

**示例 \#1 Fancy "Hello world"**

``` php
<?php

$doc = new HaruDoc;

$doc->setPageMode(HaruDoc::PAGE_MODE_USE_THUMBS); /* show thumbnails */

$page = $doc->addPage(); /* add page to the document */
$page->setSize(HaruPage::SIZE_A4, HaruPage::LANDSCAPE); /* set the page to use A4 landscape format */

$courier = $doc->getFont("Courier-Bold"); /* we'll use the bundled font a few lines below */

$page->setRGBStroke(0, 0, 0); /* set colors */
$page->setRGBFill(0.7, 0.8, 0.9);
$page->rectangle(150, 150, 550, 250); /* draw a rectangle */

$page->fillStroke(); /* fill and stroke it */

$page->setDash(array(3, 3), 0); /* set dash style for lines at this page */
$page->setFontAndSize($courier, 60); /* set font and size */

$page->setRGBStroke(0.5, 0.5, 0.1); /* set line color */
$page->setRGBFill(1, 1, 1); /* set filling color */

$page->setTextRenderingMode(HaruPage::FILL_THEN_STROKE); /* fill and stroke text */

/* print the text */
$page->beginText();
$page->textOut(210, 270, "Hello World!");
$page->endText();

$doc->save("/tmp/test.pdf"); /* save the document into a file */

?>
```

Open the result document in your favourite PDF viewer and you should see
a light-blue rectangle and white "Hello World!" on it.
