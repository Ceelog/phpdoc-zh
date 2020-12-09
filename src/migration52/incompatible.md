Backward Incompatible Changes
-----------------------------

Although most existing PHP 5 code should work without changes, you
should pay attention to the following backward incompatible changes:

-   <span class="simpara"> <span class="function">getrusage</span>
    returns **`null`** when passed incompatible arguments as of PHP
    5.2.1. </span>
-   <span class="simpara"> <span
    class="function">ZipArchive::setCommentName</span> returns
    **`true`** on success as of PHP 5.2.1. </span>
-   <span class="simpara"> <span
    class="function">ZipArchive::setCommentIndex</span> returns
    **`true`** on success as of PHP 5.2.1. </span>
-   <span class="simpara"> <span
    class="function">SplFileObject::getFilename</span> returns the
    filename, not relative/path/to/file, as of PHP 5.2.1. </span>
-   <span class="simpara"> Changed priority of `PHPRC` environment
    variable on Win32 </span> <span class="simpara"> The `PHPRC`
    environment variable now takes priority over the path stored in the
    Windows registry. </span>
-   <span class="simpara"> CLI SAPI no longer checks cwd for `php.ini`
    or the `php-cli.ini` file </span> <span class="simpara"> In PHP
    5.1.x an undocumented feature was added that made the CLI binary
    check the current working directory for a PHP configuration file,
    potentially leading to unpredictable behavior if an unexpected
    configuration file were read. This functionality was removed in
    5.2.0, and PHP will no longer search CWD for the presence of
    `php.ini` or `php-cli.ini` files. See also the
    <a href="/features/commandline.html" class="link">command line</a>
    section of the manual. </span>
-   <span class="simpara"> Added a warning when performing modulus 0
    operations </span> <span class="simpara"> In earlier versions of
    PHP, performing integer % 0 did not emit any warning messages,
    instead returning an unexpected return value of **`false`**. As of
    PHP 5.2.0, this operation will emit an **`E_WARNING`**, as is the
    case in all other instances where division by zero is performed.
    </span>
    ``` php
    <?php
    print 10 % 0;
    /* Warning:  Division by zero in filename on line n */
    ?>
    ```
-   <span class="simpara"> Changed
    <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>
    to be called wherever applicable. </span> <span class="simpara"> The
    magic method
    <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>
    will now be called in a string context, that is, anywhere an object
    is used as a string. </span> <span class="simpara"> The fallback of
    returning a string that contains the object identifier was dropped
    in PHP 5.2.0. It became problematic because an object identifier
    cannot be considered unique. This change will mean that your
    application is flawed if you have relied on the object identifier as
    a return value. An attempt to use that value as a string will now
    result in a catchable fatal error. </span>
    ``` php
    <?php
    class foo {}
    $foo = new foo;
    print $foo;
    /* Catchable fatal error:  Object of class foo could
       not be converted to string in filename on line n */
    ?>
    ```

    <span class="simpara"> Even with
    <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>,
    objects cannot be used as array indices or keys. We may add built-in
    hash support for this at a later date, but as of PHP 5.2.x you will
    need to either provide your own hashing or use the new SPL function
    <span class="function">spl\_object\_hash</span>. </span> <span
    class="simpara"> Exceptions can not be thrown from
    <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>
    methods. </span>
    ``` php
    <?php
    class foo {
        public function __toString() {
            throw new Exception;
        }
    }

    try {
        print new foo;
        /* Fatal error:  Method foo::__toString() must
           not throw an exception in filename on line n */
    } catch(Exception $e) {}
    ?>
    ```
-   <span class="simpara"> Dropped abstract static class functions.
    </span> <span class="simpara"> Due to an oversight, PHP 5.0.x and
    5.1.x allowed abstract static functions in classes. As of PHP 5.2.x,
    only interfaces can have them. </span>
    ``` php
    <?php
    abstract class foo {
        abstract static function bar();
        /* Strict Standards:  Static function foo::bar()
           should not be abstract in filename on line n */
    }
    ?>
    ```
-   <span class="simpara">
    <a href="/book/oci8.html#OCI8%20函数" class="link">Oracle extension</a>
    requires at least Oracle 10 on Windows. </span>
-   <span class="simpara"> Added RFC2397 (*data:* stream) support.
    </span> <span class="simpara"> The introduction of the 'data' URL
    scheme has the potential to lead to a change of behavior under
    Windows. If you are working with a NTFS file system and making use
    of meta streams in your application, and if you just happen to be
    using a file with the name 'data:' that is accessed without any path
    information - it won't work any more. The fix is to use the 'file:'
    protocol when accessing it. </span> <span class="simpara"> See also
    <a href="http://www.faqs.org/rfcs/rfc2397" class="link external">» RFC 2397</a>
    </span>
    ``` php
    <?php
    /* when allow_url_include is OFF (default) */
    include "data:;base64,PD9waHAgcGhwaW5mbygpOz8+";
    /* Warning:  include(): URL file-access is disabled
       in the server configuration in filename on line n */
    ?>
    ```
-   <span class="simpara"> Regression in *glob()* patterns </span> <span
    class="simpara"> In version 5.2.4 a security fix caused a regression
    for patterns of the form "/foo/\*/bar/\*". Since version 5.2.5
    instead of raising a warning the *glob()* function will return
    **`false`** when *openbase\_dir* restrictions are violated. </span>
