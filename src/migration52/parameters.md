New Parameters
--------------

Some functions were given new, optional, parameters in PHP 5.2.x:

PHP Core:

-   <span class="simpara"> <span class="function">htmlentities</span> -
    added `double_encode` in PHP 5.2.3. </span>
-   <span class="simpara"> <span
    class="function">htmlspecialchars</span> - added `double_encode` in
    PHP 5.2.3. </span>
-   <span class="simpara"> <span
    class="function">base64\_decode</span> - added `strict` </span>
-   <span class="simpara"> <span class="function">setcookie</span> -
    added `httponly` </span>
-   <span class="simpara"> <span class="function">setrawcookie</span> -
    added `httponly` </span>
-   <span class="simpara"> <span
    class="function">session\_set\_cookie\_params</span> - added
    `httponly` </span>
-   <span class="simpara"> <span
    class="function">memory\_get\_usage</span> - added `real_usage`
    </span>
-   <span class="simpara"> <span
    class="function">get\_loaded\_extensions</span> - added
    `zend_extensions` in PHP 5.2.4 </span>

<a href="/ref/curl.html" class="link">curl</a>:

-   <span class="simpara"> <span
    class="function">curl\_multi\_info\_read</span> - added
    `msgs_in_queue` </span>

<a href="/ref/datetime.html" class="link">datetime</a>

-   <span class="simpara"> <span class="function">date</span> - added
    "u" (milliseconds) format character in PHP 5.2.2 </span>

<a href="/ref/imap.html" class="link">imap</a>:

-   <span class="simpara"> <span class="function">imap\_open</span> -
    added `n_retries` </span>
-   <span class="simpara"> <span class="function">imap\_reopen</span> -
    added `n_retries` </span>

<a href="/ref/mbstring.html" class="link">mbstring</a>:

-   <span class="simpara"> <span class="function">mb\_strrpos</span> -
    added `offset` </span>
    **Warning**
    The `offset` parameter was put in the position the `encoding`
    parameter used to be. Backward compatibility has been provided by
    allowing `encoding` to be specified as the third parameter. Using
    this backward compatibility mode is not recommended because it will
    be removed in a future release of PHP.

<a href="/ref/ming.html" class="link">ming</a>:

-   <span class="simpara"> <span
    class="function">SWFMovie::streamMP3</span> - added `skip` in PHP
    5.2.1 </span>

<a href="/ref/openssl.html" class="link">openssl</a>:

-   <span class="simpara"> <span
    class="function">openssl\_verify</span> - added `signature_algo`
    </span>

<a href="/book/pgsql.html#PostgreSQL%20函数" class="link">pgsql</a>:

-   <span class="simpara"> <span
    class="function">pg\_escape\_bytea</span> - added `connection`
    </span>
-   <span class="simpara"> <span
    class="function">pg\_escape\_string</span> - added `connection`
    </span>

<a href="/ref/simplexml.html" class="link">simplexml</a>:

-   <span class="simpara"> <span
    class="function">SimpleXMLElement::\_\_construct</span> - added
    `is_prefix` </span>
-   <span class="simpara"> <span
    class="function">SimpleXMLElement::attributes</span> - added
    `is_prefix` </span>
-   <span class="simpara"> <span
    class="function">SimpleXMLElement::children</span> - added
    `is_prefix` </span>
-   <span class="simpara"> <span
    class="function">simplexml\_load\_file</span> - added `is_prefix`
    </span>
-   <span class="simpara"> <span
    class="function">simplexml\_load\_string</span> - added `is_prefix`
    </span>

<a href="/ref/spl.html" class="link">spl</a>:

-   <span class="simpara"> array iterator\_to\_array(Traversable it \[,
    bool use\_keys = true\]) - added `use_keys` in PHP 5.2.1 </span>

<a href="/book/xmlreader.html" class="link">xmlreader</a>:

-   <span class="simpara"> <span
    class="function">XMLReader::open</span> - added `encoding` and
    `options` </span>
-   <span class="simpara"> <span
    class="function">XMLReader::XML</span> - added `encoding` and
    `options` </span>

<a href="/ref/xmlwriter.html" class="link">XMLWriter</a>:

-   <span class="simpara"> <span
    class="function">xmlwriter\_write\_element</span> - the `content`
    became optional in PHP 5.2.3 </span>
-   <span class="simpara"> <span
    class="function">xmlwriter\_write\_element\_ns</span> - the
    `content` became optional in PHP 5.2.3 </span>
