New Methods
-----------

New methods were introduced in 5.2.0:

<a href="/book/dom.html" class="link">dom</a>:

-   <span class="simpara"> <span
    class="function">DOMDocument::registerNodeClass</span> - Register
    extended class used to create base node type </span>
-   <span class="simpara"> <span
    class="function">DOMElement::setIDAttribute</span> - Declares the
    attribute specified by name to be of type ID </span>
-   <span class="simpara"> <span
    class="function">DOMElement::setIDAttributeNode</span> - Declares
    the attribute specified by node to be of type ID </span>
-   <span class="simpara"> <span
    class="function">DOMElement::setIDAttributeNS</span> - Declares the
    attribute specified by local name and namespace URI to be of type ID
    </span>
-   <span class="simpara"> <span
    class="methodname">DOMNode::C14N</span>(\[bool exclusive \[, bool
    with\_comments \[, array xpath \[, array ns\_prefixes\]\]\]\]) -
    Canonicalize nodes to a string </span>
-   <span class="simpara"> <span
    class="methodname">DOMNode::C14NFile</span>(string uri \[, bool
    exclusive \[, bool with\_comments \[, array xpath \[, array
    ns\_prefixes\]\]\]\]) - Canonicalize nodes to a file </span>
-   <span class="simpara"> <span
    class="methodname">DOMNode::getNodePath</span>() - Gets an *xpath*
    for a node </span>

<a href="/ref/soap.html" class="link">soap</a>:

-   <span class="simpara"> <span
    class="methodname">SoapServer::setObject</span>(object obj) - Sets
    object which will handle SOAP requests </span>

<a href="/ref/spl.html" class="link">spl</a>:

-   <span class="simpara"> int <span
    class="methodname">ArrayObject::asort</span>(void) - Sort the
    entries by values </span>
-   <span class="simpara"> int <span
    class="methodname">ArrayObject::ksort</span>(void) - Sort the
    entries by key </span>
-   <span class="simpara"> int <span
    class="methodname">ArrayObject::natcasesort</span>(void) - Sort the
    entries by key using case insensitive "natural order" algorithm.
    </span>
-   <span class="simpara"> int <span
    class="methodname">ArrayObject::natsort</span>(void) - Sort the
    entries by values using "natural order" algorithm. </span>
-   <span class="simpara"> int <span
    class="methodname">ArrayObject::uasort</span>(callback
    cmp\_function) - Sort the entries by values using a user defined
    function </span>
-   <span class="simpara"> int <span
    class="methodname">ArrayObject::uksort</span>(callback
    cmp\_function) - Sort the entries by key using a user defined
    function. </span>
-   <span class="simpara"> ArrayIterator <span
    class="methodname">AppendIterator::getArrayIterator</span>() - Get
    access to inner *ArrayIterator* </span>
-   <span class="simpara"> int <span
    class="methodname">AppendIterator::getIteratorIndex</span>() - Get
    index of iterator </span>
-   <span class="simpara"> bool <span
    class="methodname">CachingIterator::getCache</span>() - Return the
    cache </span>
-   <span class="simpara"> int <span
    class="methodname">CachingIterator::getFlags</span>() - Return the
    internal flags </span>
-   <span class="simpara"> bool <span
    class="methodname">CachingIterator::offsetExists</span>(mixed
    index) - Returns **`TRUE`** if the requested index exists </span>
-   <span class="simpara"> string <span
    class="methodname">CachingIterator::offsetGet</span>(mixed index) -
    Return the internal cache if used </span>
-   <span class="simpara"> void <span
    class="methodname">CachingIterator::offsetSet</span>(mixed index,
    mixed newval) - Set given index in cache </span>
-   <span class="simpara"> void <span
    class="methodname">CachingIterator::offsetUnset</span>(mixed
    index) - Unset given index in cache </span>
-   <span class="simpara"> void <span
    class="methodname">CachingIterator::setFlags</span>() - Set the
    internal flags </span>
-   <span class="simpara"> array("delimiter" =\>, "enclosure" =\>) <span
    class="methodname">SplFileObject::getCsvControl</span>(void) - Get
    the delimiter and enclosure character used in <span
    class="function">fgetcsv</span> </span>
-   <span class="simpara"> void <span
    class="methodname">SplFileObject::setCsvControl</span>(\[string
    delimiter = ',' \[, string enclosure = '"'\]\]) - Set the delimiter
    and enclosure character used in <span
    class="function">fgetcsv</span> </span>

<a href="/ref/tidy.html" class="link">Tidy</a>

-   <span class="simpara"> tidyNode <span
    class="methodname">tidyNode::getParent</span>() - Returns the parent
    node of the current node (Added in PHP 5.2.2) </span>

<a href="/book/xmlreader.html" class="link">XMLReader</a>

-   <span class="simpara"> boolean <span
    class="function">XMLReader::setSchema</span> - Use W3C XSD schema to
    validate the document as it is processed. Activation is only
    possible before the first <span
    class="function">XMLReader::read</span> </span>

<a href="/ref/zip.html" class="link">zip</a>:

-   <span class="simpara"> <span
    class="methodname">ZipArchive::addEmptyDir</span>() - Creates an
    empty directory in the archive </span>
