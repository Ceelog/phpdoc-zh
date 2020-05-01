范例
====

**目录**

-   [Basic Usage Examples](/pdf/examples.html#Basic%20Usage%20Examples)

Basic Usage Examples
--------------------

Most of the functions are fairly easy to use. The most difficult part is
probably creating your first PDF document. The following example should
help to get you started. It is developed for PHP 4 and creates the file
`hello.pdf` with one page. It defines some document info field contents,
loads the Helvetica-Bold font and outputs the text "Hello world! (says
PHP)".

**示例 \#1 Hello World example from PDFlib distribution for PHP 4**

``` php
<?php
$p = PDF_new();

/*  open new PDF file; insert a file name to create the PDF on disk */
if (PDF_begin_document($p, "", "") == 0) {
    die("Error: " . PDF_get_errmsg($p));
}

PDF_set_info($p, "Creator", "hello.php");
PDF_set_info($p, "Author", "Rainer Schaaf");
PDF_set_info($p, "Title", "Hello world (PHP)!");

PDF_begin_page_ext($p, 595, 842, "");

$font = PDF_load_font($p, "Helvetica-Bold", "winansi", "");

PDF_setfont($p, $font, 24.0);
PDF_set_text_pos($p, 50, 700);
PDF_show($p, "Hello world!");
PDF_continue_text($p, "(says PHP)");
PDF_end_page_ext($p, "");

PDF_end_document($p, "");

$buf = PDF_get_buffer($p);
$len = strlen($buf);

header("Content-type: application/pdf");
header("Content-Length: $len");
header("Content-Disposition: inline; filename=hello.pdf");
print $buf;

PDF_delete($p);
?>
```

The following example comes with the PDFlib distribution for PHP 5. It
uses the new exception handling and object encapsulation features
available in PHP 5. It creates the file `hello.pdf` with one page. It
defines some document info field contents, loads the Helvetica-Bold font
and outputs the text "Hello world! (says PHP)".

**示例 \#2 Hello World example from PDFlib distribution for PHP 5**

``` php
<?php

try {
    $p = new PDFlib();

    /*  open new PDF file; insert a file name to create the PDF on disk */
    if ($p->begin_document("", "") == 0) {
        die("Error: " . $p->get_errmsg());
    }

    $p->set_info("Creator", "hello.php");
    $p->set_info("Author", "Rainer Schaaf");
    $p->set_info("Title", "Hello world (PHP)!");

    $p->begin_page_ext(595, 842, "");

    $font = $p->load_font("Helvetica-Bold", "winansi", "");

    $p->setfont($font, 24.0);
    $p->set_text_pos(50, 700);
    $p->show("Hello world!");
    $p->continue_text("(says PHP)");
    $p->end_page_ext("");

    $p->end_document("");

    $buf = $p->get_buffer();
    $len = strlen($buf);

    header("Content-type: application/pdf");
    header("Content-Length: $len");
    header("Content-Disposition: inline; filename=hello.pdf");
    print $buf;
}
catch (PDFlibException $e) {
    die("PDFlib exception occurred in hello sample:\n" .
    "[" . $e->get_errnum() . "] " . $e->get_apiname() . ": " .
    $e->get_errmsg() . "\n");
}
catch (Exception $e) {
    die($e);
}
$p = 0;
?>
```
