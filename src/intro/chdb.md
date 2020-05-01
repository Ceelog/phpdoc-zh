CHDB (constant hash database) is a fast key-value database for constant
data, realized by using a memory-mapped file and thus providing the
following functionalities:

-   Extremely fast initial load, regardless of the size of the database.

-   Only the pages of the file which are actually used are loaded from
    the disk.

-   Once a page is loaded it is shared across multiple processes.

-   Loaded pages are cached across multiple requests and even process
    recycling.

A typical use of CHDB is as a faster alternative to defining many PHP
constants.

CHDB is internally implemented as a hash-table using a
<a href="http://en.wikipedia.org/wiki/Perfect_hash_function" class="link external">» perfect hashing</a>
function, thus guaranteeing worst case O(1) lookup time.
