New Functions
-------------

PHP 5.2.x introduced some new functions:

PHP Core:

-   <span class="simpara"> <span
    class="function">array\_fill\_keys</span> - Create an array using
    the elements of the first parameter as keys, each initialized to
    *val* </span>
-   <span class="simpara"> <span
    class="function">error\_get\_last</span> - Get the last occurred
    error as associative array. Returns **`null`** if there hasn't been
    an error yet </span>
-   <span class="simpara"> <span
    class="function">image\_type\_to\_extension</span> - Get file
    extension for image-type returned by <span
    class="function">getimagesize</span>, <span
    class="function">exif\_read\_data</span>, <span
    class="function">exif\_thumbnail</span>, <span
    class="function">exif\_imagetype</span> </span>
-   <span class="simpara"> <span
    class="function">memory\_get\_peak\_usage</span> - Returns the peak
    allocated by PHP memory </span>
-   <span class="simpara"> <span
    class="function">sys\_get\_temp\_dir</span> - Returns directory path
    used for temporary files. (Added in 5.2.1) </span>
-   <span class="simpara"> <span
    class="function">timezone\_abbreviations\_list</span> - Returns
    associative array containing DST, offset and the timezone name
    </span>
-   <span class="simpara"> <span
    class="function">timezone\_identifiers\_list</span> - Returns
    numerically indexed array with all timezone identifiers </span>
-   <span class="simpara"> <span
    class="function">timezone\_name\_from\_abbr</span> - Returns the
    timezone name from abbreviation </span>
-   <span class="simpara"> <span
    class="function">stream\_socket\_shutdown</span> - Causes all or
    part of a full-duplex connection on the socket associated with
    stream to be shut down. As of PHP 5.2.1. </span>

<a href="/ref/image.html" class="link">Image</a>:

-   <span class="simpara"> <span
    class="function">imagegrabscreen</span> - Grabs a screenshot of the
    whole screen. As of PHP 5.2.2. </span>
-   <span class="simpara"> <span
    class="function">imagegrabwindow</span> - Captures a window. As of
    PHP 5.2.2. </span>

<a href="/book/libxml.html" class="link">libXML</a>:

-   <span class="simpara"> <span
    class="function">libxml\_disable\_entity\_loader</span> - Disable
    the ability to load external entities. As of PHP 5.2.11. </span>

<a href="/ref/mbstring.html" class="link">mbstring</a>:

-   <span class="simpara"> <span class="function">mb\_stripos</span> -
    Finds position of first occurrence of a string within another, case
    insensitive </span>
-   <span class="simpara"> <span class="function">mb\_stristr</span> -
    Finds first occurrence of a string within another, case insensitive
    </span>
-   <span class="simpara"> <span class="function">mb\_strrchr</span> -
    Finds the last occurrence of a character in a string within another
    </span>
-   <span class="simpara"> <span class="function">mb\_strrichr</span> -
    Finds the last occurrence of a character in a string within another,
    case insensitive </span>
-   <span class="simpara"> <span class="function">mb\_strripos</span> -
    Finds position of last occurrence of a string within another, case
    insensitive </span>
-   <span class="simpara"> <span class="function">mb\_strstr</span> -
    Finds first occurrence of a string within another </span>

ming (As of PHP 5.2.1):

-   <span class="simpara"> void ming\_setSWFCompression(int num) - Sets
    output compression </span>
-   <span class="simpara"> void swfmovie::namedanchor(string name) -
    Creates anchor </span>
-   <span class="simpara"> void swfmovie::protect(\[string password\]) -
    Protects </span>

<a href="/ref/openssl.html" class="link">openssl</a>:

-   <span class="simpara"> <span
    class="function">openssl\_csr\_get\_public\_key</span> - Extracts
    public key from a CERT and prepares it for use </span>
-   <span class="simpara"> <span
    class="function">openssl\_csr\_get\_subject</span> - Returns the
    subject of a CERT </span>
-   <span class="simpara"> <span
    class="function">openssl\_pkey\_get\_details</span> - Returns an
    array with the key details (bits, pkey, type) </span>

<a href="/ref/spl.html" class="link">spl</a>:

-   <span class="simpara"> <span
    class="function">spl\_object\_hash</span> - Return hash id for given
    object </span>
-   <span class="simpara"> int iterator\_apply(Traversable it, mixed
    function \[, mixed params\]) - Calls a function for every element in
    an iterator </span>

<a href="/ref/pcre.html" class="link">pcre</a>:

-   <span class="simpara"> <span
    class="function">preg\_last\_error</span> - Returns the error code
    of the last regex execution </span>

<a href="/book/pgsql.html#PostgreSQL%20函数" class="link">pgsql</a>:

-   <span class="simpara"> <span
    class="function">pg\_field\_table</span> - Returns the name of the
    table field belongs to, or table's oid if *oid\_only* is **`true`**
    </span>

<a href="/ref/posix.html" class="link">posix</a>:

-   <span class="simpara"> <span
    class="function">posix\_initgroups</span> - Calculate the group
    access list for the user specified in name </span>

<a href="/ref/gmp.html" class="link">gmp</a>:

-   <span class="simpara"> <span
    class="function">gmp\_nextprime</span> - Finds next prime number
    </span>

<a href="/ref/xmlwriter.html" class="link">xmlwriter</a>:

-   <span class="simpara"> <span
    class="function">xmlwriter\_full\_end\_element</span> - End current
    element - returns **`false`** on error </span>
-   <span class="simpara"> <span
    class="function">xmlwriter\_write\_raw</span> - Write text - returns
    **`false`** on error </span>
-   <span class="simpara"> <span
    class="function">xmlwriter\_start\_dtd\_entity</span> - Create start
    DTD Entity - returns **`false`** on error </span>
-   <span class="simpara"> <span
    class="function">xmlwriter\_end\_dtd\_entity</span> - End current
    DTD Entity - returns **`false`** on error </span>
-   <span class="simpara"> <span
    class="function">xmlwriter\_write\_dtd\_entity</span> - Write full
    DTD Entity tag - returns **`false`** on error </span>
