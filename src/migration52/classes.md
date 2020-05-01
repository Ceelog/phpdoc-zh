New Classes
-----------

The following classes were introduced in PHP 5.2.0:

-   <span class="simpara">
    <a href="/ref/datetime.html" class="link">DateTime</a> </span>
-   <span class="simpara">
    <a href="/ref/datetime.html" class="link">DateTimeZone</a> </span>
-   <span class="simpara"> RegexIterator - extends <span
    class="classname">FilterIterator</span>; implements <span
    class="classname">Iterator</span>, <span
    class="classname">Traversable</span>, <span
    class="classname">OuterIterator</span> </span> <span
    class="simpara"> Constants: </span>
    -   <span class="simpara"> **`RegexIterator::ALL_MATCHES`** </span>
    -   <span class="simpara"> **`RegexIterator::GET_MATCH`** </span>
    -   <span class="simpara"> **`RegexIterator::MATCH`** </span>
    -   <span class="simpara"> **`RegexIterator::REPLACE`** </span>
    -   <span class="simpara"> **`RegexIterator::SPLIT`** </span>
    -   <span class="simpara"> **`RegexIterator::USE_KEY`** </span>

    <span class="simpara"> Properties: </span>
    -   <span class="simpara"> public <span
        class="property">replacement</span> </span>

    <span class="simpara"> Methods: </span>
    -   <span class="simpara"> RegexIterator::\_\_construct(Iterator it,
        string regex \[, int mode \[, int flags \[, int
        preg\_flags\]\]\]) - Create an *RegexIterator* from another
        iterator and a regular expression </span>
    -   <span class="simpara"> bool RegexIterator::accept() - Match
        (string)current() against regular expression </span>
    -   <span class="simpara"> bool RegexIterator::getFlags() - Returns
        current operation flags </span>
    -   <span class="simpara"> bool RegexIterator::getMode() - Returns
        current operation mode </span>
    -   <span class="simpara"> bool RegexIterator::getPregFlags() -
        Returns current PREG flags (if in use or **`NULL`**) </span>
    -   <span class="simpara"> bool RegexIterator::setFlags(int
        new\_flags) - Set operation flags </span>
    -   <span class="simpara"> bool RegexIterator::setMode(int
        new\_mode) - Set new operation mode </span>
    -   <span class="simpara"> bool RegexIterator::setPregFlags(int
        new\_flags) - Set PREG flags </span>
-   <span class="simpara"> RecursiveRegexIterator </span> <span
    class="simpara"> Constants: </span>
    -   <span class="simpara"> **`RecursiveRegexIterator::ALL_MATCHES`**
        </span>
    -   <span class="simpara"> **`RecursiveRegexIterator::GET_MATCH`**
        </span>
    -   <span class="simpara"> **`RecursiveRegexIterator::MATCH`**
        </span>
    -   <span class="simpara"> **`RecursiveRegexIterator::REPLACE`**
        </span>
    -   <span class="simpara"> **`RecursiveRegexIterator::SPLIT`**
        </span>
    -   <span class="simpara"> **`RecursiveRegexIterator::USE_KEY`**
        </span>

    <span class="simpara"> Methods: </span>
    -   <span class="simpara">
        RecursiveRegexIterator::\_\_construct(RecursiveIterator it,
        string regex \[, int mode \[, int flags \[, int
        preg\_flags\]\]\]) - Create an *RecursiveRegexIterator* from
        another recursive iterator and a regular expression </span>
    -   <span class="simpara"> RecursiveRegexIterator
        RecursiveRegexIterator::getChildren() - Return the inner
        iterator's children contained in a *RecursiveRegexIterator*
        </span>
    -   <span class="simpara"> bool
        RecursiveRegexIterator::hasChildren() - Check whether the inner
        iterator's current element has children </span>
