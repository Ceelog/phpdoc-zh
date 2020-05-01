迭代器
======

**目录**

-   [AppendIterator](/spl/iterators.html#AppendIterator) — The
    AppendIterator class
    -   [AppendIterator::append](/spl/iterators.html#AppendIterator::append)
        — Appends an iterator
    -   [AppendIterator::\_\_construct](/spl/iterators.html#AppendIterator::__construct)
        — Constructs an AppendIterator
    -   [AppendIterator::current](/spl/iterators.html#AppendIterator::current)
        — Gets the current value
    -   [AppendIterator::getArrayIterator](/spl/iterators.html#AppendIterator::getArrayIterator)
        — Gets the ArrayIterator
    -   [AppendIterator::getInnerIterator](/spl/iterators.html#AppendIterator::getInnerIterator)
        — Gets the inner iterator
    -   [AppendIterator::getIteratorIndex](/spl/iterators.html#AppendIterator::getIteratorIndex)
        — Gets an index of iterators
    -   [AppendIterator::key](/spl/iterators.html#AppendIterator::key) —
        Gets the current key
    -   [AppendIterator::next](/spl/iterators.html#AppendIterator::next)
        — Moves to the next element
    -   [AppendIterator::rewind](/spl/iterators.html#AppendIterator::rewind)
        — Rewinds the Iterator
    -   [AppendIterator::valid](/spl/iterators.html#AppendIterator::valid)
        — Checks validity of the current element
-   [ArrayIterator](/spl/iterators.html#ArrayIterator) — ArrayIterator
    类
    -   [ArrayIterator::append](/spl/iterators.html#ArrayIterator::append)
        — Append an element
    -   [ArrayIterator::asort](/spl/iterators.html#ArrayIterator::asort)
        — Sort array by values
    -   [ArrayIterator::\_\_construct](/spl/iterators.html#ArrayIterator::__construct)
        — Construct an ArrayIterator
    -   [ArrayIterator::count](/spl/iterators.html#ArrayIterator::count)
        — Count elements
    -   [ArrayIterator::current](/spl/iterators.html#ArrayIterator::current)
        — Return current array entry
    -   [ArrayIterator::getArrayCopy](/spl/iterators.html#ArrayIterator::getArrayCopy)
        — Get array copy
    -   [ArrayIterator::getFlags](/spl/iterators.html#ArrayIterator::getFlags)
        — Get behavior flags
    -   [ArrayIterator::key](/spl/iterators.html#ArrayIterator::key) —
        Return current array key
    -   [ArrayIterator::ksort](/spl/iterators.html#ArrayIterator::ksort)
        — Sort array by keys
    -   [ArrayIterator::natcasesort](/spl/iterators.html#ArrayIterator::natcasesort)
        — Sort an array naturally, case insensitive
    -   [ArrayIterator::natsort](/spl/iterators.html#ArrayIterator::natsort)
        — Sort an array naturally
    -   [ArrayIterator::next](/spl/iterators.html#ArrayIterator::next) —
        Move to next entry
    -   [ArrayIterator::offsetExists](/spl/iterators.html#ArrayIterator::offsetExists)
        — Check if offset exists
    -   [ArrayIterator::offsetGet](/spl/iterators.html#ArrayIterator::offsetGet)
        — Get value for an offset
    -   [ArrayIterator::offsetSet](/spl/iterators.html#ArrayIterator::offsetSet)
        — Set value for an offset
    -   [ArrayIterator::offsetUnset](/spl/iterators.html#ArrayIterator::offsetUnset)
        — Unset value for an offset
    -   [ArrayIterator::rewind](/spl/iterators.html#ArrayIterator::rewind)
        — Rewind array back to the start
    -   [ArrayIterator::seek](/spl/iterators.html#ArrayIterator::seek) —
        Seek to position
    -   [ArrayIterator::serialize](/spl/iterators.html#ArrayIterator::serialize)
        — Serialize
    -   [ArrayIterator::setFlags](/spl/iterators.html#ArrayIterator::setFlags)
        — Set behaviour flags
    -   [ArrayIterator::uasort](/spl/iterators.html#ArrayIterator::uasort)
        — Sort with a user-defined comparison function and maintain
        index association
    -   [ArrayIterator::uksort](/spl/iterators.html#ArrayIterator::uksort)
        — Sort by keys using a user-defined comparison function
    -   [ArrayIterator::unserialize](/spl/iterators.html#ArrayIterator::unserialize)
        — Unserialize
    -   [ArrayIterator::valid](/spl/iterators.html#ArrayIterator::valid)
        — Check whether array contains more entries
-   [CachingIterator](/spl/iterators.html#CachingIterator) — The
    CachingIterator class
    -   [CachingIterator::\_\_construct](/spl/iterators.html#CachingIterator::__construct)
        — Construct a new CachingIterator object for the iterator
    -   [CachingIterator::count](/spl/iterators.html#CachingIterator::count)
        — The number of elements in the iterator
    -   [CachingIterator::current](/spl/iterators.html#CachingIterator::current)
        — Return the current element
    -   [CachingIterator::getCache](/spl/iterators.html#CachingIterator::getCache)
        — Retrieve the contents of the cache
    -   [CachingIterator::getFlags](/spl/iterators.html#CachingIterator::getFlags)
        — Get flags used
    -   [CachingIterator::getInnerIterator](/spl/iterators.html#CachingIterator::getInnerIterator)
        — Returns the inner iterator
    -   [CachingIterator::hasNext](/spl/iterators.html#CachingIterator::hasNext)
        — Check whether the inner iterator has a valid next element
    -   [CachingIterator::key](/spl/iterators.html#CachingIterator::key)
        — Return the key for the current element
    -   [CachingIterator::next](/spl/iterators.html#CachingIterator::next)
        — Move the iterator forward
    -   [CachingIterator::offsetExists](/spl/iterators.html#CachingIterator::offsetExists)
        — The offsetExists purpose
    -   [CachingIterator::offsetGet](/spl/iterators.html#CachingIterator::offsetGet)
        — The offsetGet purpose
    -   [CachingIterator::offsetSet](/spl/iterators.html#CachingIterator::offsetSet)
        — The offsetSet purpose
    -   [CachingIterator::offsetUnset](/spl/iterators.html#CachingIterator::offsetUnset)
        — The offsetUnset purpose
    -   [CachingIterator::rewind](/spl/iterators.html#CachingIterator::rewind)
        — Rewind the iterator
    -   [CachingIterator::setFlags](/spl/iterators.html#CachingIterator::setFlags)
        — The setFlags purpose
    -   [CachingIterator::\_\_toString](/spl/iterators.html#CachingIterator::__toString)
        — Return the string representation of the current element
    -   [CachingIterator::valid](/spl/iterators.html#CachingIterator::valid)
        — Check whether the current element is valid
-   [CallbackFilterIterator](/spl/iterators.html#CallbackFilterIterator)
    — The CallbackFilterIterator class
    -   [CallbackFilterIterator::accept](/spl/iterators.html#CallbackFilterIterator::accept)
        — Calls the callback with the current value, the current key and
        the inner iterator as arguments
    -   [CallbackFilterIterator::\_\_construct](/spl/iterators.html#CallbackFilterIterator::__construct)
        — Create a filtered iterator from another iterator
-   [DirectoryIterator](/spl/iterators.html#DirectoryIterator) — The
    DirectoryIterator class
    -   [DirectoryIterator::\_\_construct](/spl/iterators.html#DirectoryIterator::__construct)
        — Constructs a new directory iterator from a path
    -   [DirectoryIterator::current](/spl/iterators.html#DirectoryIterator::current)
        — Return the current DirectoryIterator item
    -   [DirectoryIterator::getATime](/spl/iterators.html#DirectoryIterator::getATime)
        — Get last access time of the current DirectoryIterator item
    -   [DirectoryIterator::getBasename](/spl/iterators.html#DirectoryIterator::getBasename)
        — Get base name of current DirectoryIterator item
    -   [DirectoryIterator::getCTime](/spl/iterators.html#DirectoryIterator::getCTime)
        — Get inode change time of the current DirectoryIterator item
    -   [DirectoryIterator::getExtension](/spl/iterators.html#DirectoryIterator::getExtension)
        — Gets the file extension
    -   [DirectoryIterator::getFilename](/spl/iterators.html#DirectoryIterator::getFilename)
        — Return file name of current DirectoryIterator item
    -   [DirectoryIterator::getGroup](/spl/iterators.html#DirectoryIterator::getGroup)
        — Get group for the current DirectoryIterator item
    -   [DirectoryIterator::getInode](/spl/iterators.html#DirectoryIterator::getInode)
        — Get inode for the current DirectoryIterator item
    -   [DirectoryIterator::getMTime](/spl/iterators.html#DirectoryIterator::getMTime)
        — Get last modification time of current DirectoryIterator item
    -   [DirectoryIterator::getOwner](/spl/iterators.html#DirectoryIterator::getOwner)
        — Get owner of current DirectoryIterator item
    -   [DirectoryIterator::getPath](/spl/iterators.html#DirectoryIterator::getPath)
        — Get path of current Iterator item without filename
    -   [DirectoryIterator::getPathname](/spl/iterators.html#DirectoryIterator::getPathname)
        — Return path and file name of current DirectoryIterator item
    -   [DirectoryIterator::getPerms](/spl/iterators.html#DirectoryIterator::getPerms)
        — Get the permissions of current DirectoryIterator item
    -   [DirectoryIterator::getSize](/spl/iterators.html#DirectoryIterator::getSize)
        — Get size of current DirectoryIterator item
    -   [DirectoryIterator::getType](/spl/iterators.html#DirectoryIterator::getType)
        — Determine the type of the current DirectoryIterator item
    -   [DirectoryIterator::isDir](/spl/iterators.html#DirectoryIterator::isDir)
        — Determine if current DirectoryIterator item is a directory
    -   [DirectoryIterator::isDot](/spl/iterators.html#DirectoryIterator::isDot)
        — Determine if current DirectoryIterator item is '.' or '..'
    -   [DirectoryIterator::isExecutable](/spl/iterators.html#DirectoryIterator::isExecutable)
        — Determine if current DirectoryIterator item is executable
    -   [DirectoryIterator::isFile](/spl/iterators.html#DirectoryIterator::isFile)
        — Determine if current DirectoryIterator item is a regular file
    -   [DirectoryIterator::isLink](/spl/iterators.html#DirectoryIterator::isLink)
        — Determine if current DirectoryIterator item is a symbolic link
    -   [DirectoryIterator::isReadable](/spl/iterators.html#DirectoryIterator::isReadable)
        — Determine if current DirectoryIterator item can be read
    -   [DirectoryIterator::isWritable](/spl/iterators.html#DirectoryIterator::isWritable)
        — Determine if current DirectoryIterator item can be written to
    -   [DirectoryIterator::key](/spl/iterators.html#DirectoryIterator::key)
        — Return the key for the current DirectoryIterator item
    -   [DirectoryIterator::next](/spl/iterators.html#DirectoryIterator::next)
        — Move forward to next DirectoryIterator item
    -   [DirectoryIterator::rewind](/spl/iterators.html#DirectoryIterator::rewind)
        — Rewind the DirectoryIterator back to the start
    -   [DirectoryIterator::seek](/spl/iterators.html#DirectoryIterator::seek)
        — Seek to a DirectoryIterator item
    -   [DirectoryIterator::\_\_toString](/spl/iterators.html#DirectoryIterator::__toString)
        — Get file name as a string
    -   [DirectoryIterator::valid](/spl/iterators.html#DirectoryIterator::valid)
        — Check whether current DirectoryIterator position is a valid
        file
-   [EmptyIterator](/spl/iterators.html#EmptyIterator) — The
    EmptyIterator class
    -   [EmptyIterator::current](/spl/iterators.html#EmptyIterator::current)
        — The current() method
    -   [EmptyIterator::key](/spl/iterators.html#EmptyIterator::key) —
        The key() method
    -   [EmptyIterator::next](/spl/iterators.html#EmptyIterator::next) —
        The next() method
    -   [EmptyIterator::rewind](/spl/iterators.html#EmptyIterator::rewind)
        — The rewind() method
    -   [EmptyIterator::valid](/spl/iterators.html#EmptyIterator::valid)
        — The valid() method
-   [FilesystemIterator](/spl/iterators.html#FilesystemIterator) — The
    FilesystemIterator class
    -   [FilesystemIterator::\_\_construct](/spl/iterators.html#FilesystemIterator::__construct)
        — Constructs a new filesystem iterator
    -   [FilesystemIterator::current](/spl/iterators.html#FilesystemIterator::current)
        — The current file
    -   [FilesystemIterator::getFlags](/spl/iterators.html#FilesystemIterator::getFlags)
        — Get the handling flags
    -   [FilesystemIterator::key](/spl/iterators.html#FilesystemIterator::key)
        — Retrieve the key for the current file
    -   [FilesystemIterator::next](/spl/iterators.html#FilesystemIterator::next)
        — Move to the next file
    -   [FilesystemIterator::rewind](/spl/iterators.html#FilesystemIterator::rewind)
        — Rewinds back to the beginning
    -   [FilesystemIterator::setFlags](/spl/iterators.html#FilesystemIterator::setFlags)
        — Sets handling flags
-   [FilterIterator](/spl/iterators.html#FilterIterator) — The
    FilterIterator class
    -   [FilterIterator::accept](/spl/iterators.html#FilterIterator::accept)
        — Check whether the current element of the iterator is
        acceptable
    -   [FilterIterator::\_\_construct](/spl/iterators.html#FilterIterator::__construct)
        — Construct a filterIterator
    -   [FilterIterator::current](/spl/iterators.html#FilterIterator::current)
        — Get the current element value
    -   [FilterIterator::getInnerIterator](/spl/iterators.html#FilterIterator::getInnerIterator)
        — Get the inner iterator
    -   [FilterIterator::key](/spl/iterators.html#FilterIterator::key) —
        Get the current key
    -   [FilterIterator::next](/spl/iterators.html#FilterIterator::next)
        — Move the iterator forward
    -   [FilterIterator::rewind](/spl/iterators.html#FilterIterator::rewind)
        — Rewind the iterator
    -   [FilterIterator::valid](/spl/iterators.html#FilterIterator::valid)
        — Check whether the current element is valid
-   [GlobIterator](/spl/iterators.html#GlobIterator) — The GlobIterator
    class
    -   [GlobIterator::\_\_construct](/spl/iterators.html#GlobIterator::__construct)
        — Construct a directory using glob
    -   [GlobIterator::count](/spl/iterators.html#GlobIterator::count) —
        Get the number of directories and files
-   [InfiniteIterator](/spl/iterators.html#InfiniteIterator) — The
    InfiniteIterator class
    -   [InfiniteIterator::\_\_construct](/spl/iterators.html#InfiniteIterator::__construct)
        — Constructs an InfiniteIterator
    -   [InfiniteIterator::next](/spl/iterators.html#InfiniteIterator::next)
        — Moves the inner Iterator forward or rewinds it
-   [IteratorIterator](/spl/iterators.html#IteratorIterator) — The
    IteratorIterator class
    -   [IteratorIterator::\_\_construct](/spl/iterators.html#IteratorIterator::__construct)
        — Create an iterator from anything that is traversable
    -   [IteratorIterator::current](/spl/iterators.html#IteratorIterator::current)
        — Get the current value
    -   [IteratorIterator::getInnerIterator](/spl/iterators.html#IteratorIterator::getInnerIterator)
        — Get the inner iterator
    -   [IteratorIterator::key](/spl/iterators.html#IteratorIterator::key)
        — Get the key of the current element
    -   [IteratorIterator::next](/spl/iterators.html#IteratorIterator::next)
        — Forward to the next element
    -   [IteratorIterator::rewind](/spl/iterators.html#IteratorIterator::rewind)
        — Rewind to the first element
    -   [IteratorIterator::valid](/spl/iterators.html#IteratorIterator::valid)
        — Checks if the iterator is valid
-   [LimitIterator](/spl/iterators.html#LimitIterator) — The
    LimitIterator class
    -   [LimitIterator::\_\_construct](/spl/iterators.html#LimitIterator::__construct)
        — Construct a LimitIterator
    -   [LimitIterator::current](/spl/iterators.html#LimitIterator::current)
        — Get current element
    -   [LimitIterator::getInnerIterator](/spl/iterators.html#LimitIterator::getInnerIterator)
        — Get inner iterator
    -   [LimitIterator::getPosition](/spl/iterators.html#LimitIterator::getPosition)
        — Return the current position
    -   [LimitIterator::key](/spl/iterators.html#LimitIterator::key) —
        Get current key
    -   [LimitIterator::next](/spl/iterators.html#LimitIterator::next) —
        Move the iterator forward
    -   [LimitIterator::rewind](/spl/iterators.html#LimitIterator::rewind)
        — Rewind the iterator to the specified starting offset
    -   [LimitIterator::seek](/spl/iterators.html#LimitIterator::seek) —
        Seek to the given position
    -   [LimitIterator::valid](/spl/iterators.html#LimitIterator::valid)
        — Check whether the current element is valid
-   [MultipleIterator](/spl/iterators.html#MultipleIterator) — The
    MultipleIterator class
    -   [MultipleIterator::attachIterator](/spl/iterators.html#MultipleIterator::attachIterator)
        — Attaches iterator information
    -   [MultipleIterator::\_\_construct](/spl/iterators.html#MultipleIterator::__construct)
        — Constructs a new MultipleIterator
    -   [MultipleIterator::containsIterator](/spl/iterators.html#MultipleIterator::containsIterator)
        — Checks if an iterator is attached
    -   [MultipleIterator::countIterators](/spl/iterators.html#MultipleIterator::countIterators)
        — Gets the number of attached iterator instances
    -   [MultipleIterator::current](/spl/iterators.html#MultipleIterator::current)
        — Gets the registered iterator instances
    -   [MultipleIterator::detachIterator](/spl/iterators.html#MultipleIterator::detachIterator)
        — Detaches an iterator
    -   [MultipleIterator::getFlags](/spl/iterators.html#MultipleIterator::getFlags)
        — Gets the flag information
    -   [MultipleIterator::key](/spl/iterators.html#MultipleIterator::key)
        — Gets the registered iterator instances
    -   [MultipleIterator::next](/spl/iterators.html#MultipleIterator::next)
        — Moves all attached iterator instances forward
    -   [MultipleIterator::rewind](/spl/iterators.html#MultipleIterator::rewind)
        — Rewinds all attached iterator instances
    -   [MultipleIterator::setFlags](/spl/iterators.html#MultipleIterator::setFlags)
        — Sets flags
    -   [MultipleIterator::valid](/spl/iterators.html#MultipleIterator::valid)
        — Checks the validity of sub iterators
-   [NoRewindIterator](/spl/iterators.html#NoRewindIterator) — The
    NoRewindIterator class
    -   [NoRewindIterator::\_\_construct](/spl/iterators.html#NoRewindIterator::__construct)
        — Construct a NoRewindIterator
    -   [NoRewindIterator::current](/spl/iterators.html#NoRewindIterator::current)
        — Get the current value
    -   [NoRewindIterator::getInnerIterator](/spl/iterators.html#NoRewindIterator::getInnerIterator)
        — Get the inner iterator
    -   [NoRewindIterator::key](/spl/iterators.html#NoRewindIterator::key)
        — Get the current key
    -   [NoRewindIterator::next](/spl/iterators.html#NoRewindIterator::next)
        — Forward to the next element
    -   [NoRewindIterator::rewind](/spl/iterators.html#NoRewindIterator::rewind)
        — Prevents the rewind operation on the inner iterator
    -   [NoRewindIterator::valid](/spl/iterators.html#NoRewindIterator::valid)
        — Validates the iterator
-   [ParentIterator](/spl/iterators.html#ParentIterator) — The
    ParentIterator class
    -   [ParentIterator::accept](/spl/iterators.html#ParentIterator::accept)
        — Determines acceptability
    -   [ParentIterator::\_\_construct](/spl/iterators.html#ParentIterator::__construct)
        — Constructs a ParentIterator
    -   [ParentIterator::getChildren](/spl/iterators.html#ParentIterator::getChildren)
        — Return the inner iterator's children contained in a
        ParentIterator
    -   [ParentIterator::hasChildren](/spl/iterators.html#ParentIterator::hasChildren)
        — Check whether the inner iterator's current element has
        children
    -   [ParentIterator::next](/spl/iterators.html#ParentIterator::next)
        — Move the iterator forward
    -   [ParentIterator::rewind](/spl/iterators.html#ParentIterator::rewind)
        — Rewind the iterator
-   [RecursiveArrayIterator](/spl/iterators.html#RecursiveArrayIterator)
    — The RecursiveArrayIterator class
    -   [RecursiveArrayIterator::getChildren](/spl/iterators.html#RecursiveArrayIterator::getChildren)
        — Returns an iterator for the current entry if it is an array or
        an object
    -   [RecursiveArrayIterator::hasChildren](/spl/iterators.html#RecursiveArrayIterator::hasChildren)
        — Returns whether current entry is an array or an object
-   [RecursiveCachingIterator](/spl/iterators.html#RecursiveCachingIterator)
    — The RecursiveCachingIterator class
    -   [RecursiveCachingIterator::\_\_construct](/spl/iterators.html#RecursiveCachingIterator::__construct)
        — Construct
    -   [RecursiveCachingIterator::getChildren](/spl/iterators.html#RecursiveCachingIterator::getChildren)
        — Return the inner iterator's children as a
        RecursiveCachingIterator
    -   [RecursiveCachingIterator::hasChildren](/spl/iterators.html#RecursiveCachingIterator::hasChildren)
        — Check whether the current element of the inner iterator has
        children
-   [RecursiveCallbackFilterIterator](/spl/iterators.html#RecursiveCallbackFilterIterator)
    — The RecursiveCallbackFilterIterator class
    -   [RecursiveCallbackFilterIterator::\_\_construct](/spl/iterators.html#RecursiveCallbackFilterIterator::__construct)
        — Create a RecursiveCallbackFilterIterator from a
        RecursiveIterator
    -   [RecursiveCallbackFilterIterator::getChildren](/spl/iterators.html#RecursiveCallbackFilterIterator::getChildren)
        — Return the inner iterator's children contained in a
        RecursiveCallbackFilterIterator
    -   [RecursiveCallbackFilterIterator::hasChildren](/spl/iterators.html#RecursiveCallbackFilterIterator::hasChildren)
        — Check whether the inner iterator's current element has
        children
-   [RecursiveDirectoryIterator](/spl/iterators.html#RecursiveDirectoryIterator)
    — The RecursiveDirectoryIterator class
    -   [RecursiveDirectoryIterator::\_\_construct](/spl/iterators.html#RecursiveDirectoryIterator::__construct)
        — Constructs a RecursiveDirectoryIterator
    -   [RecursiveDirectoryIterator::getChildren](/spl/iterators.html#RecursiveDirectoryIterator::getChildren)
        — Returns an iterator for the current entry if it is a directory
    -   [RecursiveDirectoryIterator::getSubPath](/spl/iterators.html#RecursiveDirectoryIterator::getSubPath)
        — Get sub path
    -   [RecursiveDirectoryIterator::getSubPathname](/spl/iterators.html#RecursiveDirectoryIterator::getSubPathname)
        — Get sub path and name
    -   [RecursiveDirectoryIterator::hasChildren](/spl/iterators.html#RecursiveDirectoryIterator::hasChildren)
        — Returns whether current entry is a directory and not '.' or
        '..'
    -   [RecursiveDirectoryIterator::key](/spl/iterators.html#RecursiveDirectoryIterator::key)
        — Return path and filename of current dir entry
    -   [RecursiveDirectoryIterator::next](/spl/iterators.html#RecursiveDirectoryIterator::next)
        — Move to next entry
    -   [RecursiveDirectoryIterator::rewind](/spl/iterators.html#RecursiveDirectoryIterator::rewind)
        — Rewind dir back to the start
-   [RecursiveFilterIterator](/spl/iterators.html#RecursiveFilterIterator)
    — The RecursiveFilterIterator class
    -   [RecursiveFilterIterator::\_\_construct](/spl/iterators.html#RecursiveFilterIterator::__construct)
        — Create a RecursiveFilterIterator from a RecursiveIterator
    -   [RecursiveFilterIterator::getChildren](/spl/iterators.html#RecursiveFilterIterator::getChildren)
        — Return the inner iterator's children contained in a
        RecursiveFilterIterator
    -   [RecursiveFilterIterator::hasChildren](/spl/iterators.html#RecursiveFilterIterator::hasChildren)
        — Check whether the inner iterator's current element has
        children
-   [RecursiveIteratorIterator](/spl/iterators.html#RecursiveIteratorIterator)
    — The RecursiveIteratorIterator class
    -   [RecursiveIteratorIterator::beginChildren](/spl/iterators.html#RecursiveIteratorIterator::beginChildren)
        — Begin children
    -   [RecursiveIteratorIterator::beginIteration](/spl/iterators.html#RecursiveIteratorIterator::beginIteration)
        — Begin Iteration
    -   [RecursiveIteratorIterator::callGetChildren](/spl/iterators.html#RecursiveIteratorIterator::callGetChildren)
        — Get children
    -   [RecursiveIteratorIterator::callHasChildren](/spl/iterators.html#RecursiveIteratorIterator::callHasChildren)
        — Has children
    -   [RecursiveIteratorIterator::\_\_construct](/spl/iterators.html#RecursiveIteratorIterator::__construct)
        — Construct a RecursiveIteratorIterator
    -   [RecursiveIteratorIterator::current](/spl/iterators.html#RecursiveIteratorIterator::current)
        — Access the current element value
    -   [RecursiveIteratorIterator::endChildren](/spl/iterators.html#RecursiveIteratorIterator::endChildren)
        — End children
    -   [RecursiveIteratorIterator::endIteration](/spl/iterators.html#RecursiveIteratorIterator::endIteration)
        — End Iteration
    -   [RecursiveIteratorIterator::getDepth](/spl/iterators.html#RecursiveIteratorIterator::getDepth)
        — Get the current depth of the recursive iteration
    -   [RecursiveIteratorIterator::getInnerIterator](/spl/iterators.html#RecursiveIteratorIterator::getInnerIterator)
        — Get inner iterator
    -   [RecursiveIteratorIterator::getMaxDepth](/spl/iterators.html#RecursiveIteratorIterator::getMaxDepth)
        — Get max depth
    -   [RecursiveIteratorIterator::getSubIterator](/spl/iterators.html#RecursiveIteratorIterator::getSubIterator)
        — The current active sub iterator
    -   [RecursiveIteratorIterator::key](/spl/iterators.html#RecursiveIteratorIterator::key)
        — Access the current key
    -   [RecursiveIteratorIterator::next](/spl/iterators.html#RecursiveIteratorIterator::next)
        — Move forward to the next element
    -   [RecursiveIteratorIterator::nextElement](/spl/iterators.html#RecursiveIteratorIterator::nextElement)
        — Next element
    -   [RecursiveIteratorIterator::rewind](/spl/iterators.html#RecursiveIteratorIterator::rewind)
        — Rewind the iterator to the first element of the top level
        inner iterator
    -   [RecursiveIteratorIterator::setMaxDepth](/spl/iterators.html#RecursiveIteratorIterator::setMaxDepth)
        — Set max depth
    -   [RecursiveIteratorIterator::valid](/spl/iterators.html#RecursiveIteratorIterator::valid)
        — Check whether the current position is valid
-   [RecursiveRegexIterator](/spl/iterators.html#RecursiveRegexIterator)
    — The RecursiveRegexIterator class
    -   [RecursiveRegexIterator::\_\_construct](/spl/iterators.html#RecursiveRegexIterator::__construct)
        — Creates a new RecursiveRegexIterator
    -   [RecursiveRegexIterator::getChildren](/spl/iterators.html#RecursiveRegexIterator::getChildren)
        — Returns an iterator for the current entry
    -   [RecursiveRegexIterator::hasChildren](/spl/iterators.html#RecursiveRegexIterator::hasChildren)
        — Returns whether an iterator can be obtained for the current
        entry
-   [RecursiveTreeIterator](/spl/iterators.html#RecursiveTreeIterator) —
    The RecursiveTreeIterator class
    -   [RecursiveTreeIterator::beginChildren](/spl/iterators.html#RecursiveTreeIterator::beginChildren)
        — Begin children
    -   [RecursiveTreeIterator::beginIteration](/spl/iterators.html#RecursiveTreeIterator::beginIteration)
        — Begin iteration
    -   [RecursiveTreeIterator::callGetChildren](/spl/iterators.html#RecursiveTreeIterator::callGetChildren)
        — Get children
    -   [RecursiveTreeIterator::callHasChildren](/spl/iterators.html#RecursiveTreeIterator::callHasChildren)
        — Has children
    -   [RecursiveTreeIterator::\_\_construct](/spl/iterators.html#RecursiveTreeIterator::__construct)
        — Construct a RecursiveTreeIterator
    -   [RecursiveTreeIterator::current](/spl/iterators.html#RecursiveTreeIterator::current)
        — Get current element
    -   [RecursiveTreeIterator::endChildren](/spl/iterators.html#RecursiveTreeIterator::endChildren)
        — End children
    -   [RecursiveTreeIterator::endIteration](/spl/iterators.html#RecursiveTreeIterator::endIteration)
        — End iteration
    -   [RecursiveTreeIterator::getEntry](/spl/iterators.html#RecursiveTreeIterator::getEntry)
        — Get current entry
    -   [RecursiveTreeIterator::getPostfix](/spl/iterators.html#RecursiveTreeIterator::getPostfix)
        — Get the postfix
    -   [RecursiveTreeIterator::getPrefix](/spl/iterators.html#RecursiveTreeIterator::getPrefix)
        — Get the prefix
    -   [RecursiveTreeIterator::key](/spl/iterators.html#RecursiveTreeIterator::key)
        — Get the key of the current element
    -   [RecursiveTreeIterator::next](/spl/iterators.html#RecursiveTreeIterator::next)
        — Move to next element
    -   [RecursiveTreeIterator::nextElement](/spl/iterators.html#RecursiveTreeIterator::nextElement)
        — Next element
    -   [RecursiveTreeIterator::rewind](/spl/iterators.html#RecursiveTreeIterator::rewind)
        — Rewind iterator
    -   [RecursiveTreeIterator::setPostfix](/spl/iterators.html#RecursiveTreeIterator::setPostfix)
        — Set postfix
    -   [RecursiveTreeIterator::setPrefixPart](/spl/iterators.html#RecursiveTreeIterator::setPrefixPart)
        — Set a part of the prefix
    -   [RecursiveTreeIterator::valid](/spl/iterators.html#RecursiveTreeIterator::valid)
        — Check validity
-   [RegexIterator](/spl/iterators.html#RegexIterator) — The
    RegexIterator class
    -   [RegexIterator::accept](/spl/iterators.html#RegexIterator::accept)
        — Get accept status
    -   [RegexIterator::\_\_construct](/spl/iterators.html#RegexIterator::__construct)
        — Create a new RegexIterator
    -   [RegexIterator::getFlags](/spl/iterators.html#RegexIterator::getFlags)
        — Get flags
    -   [RegexIterator::getMode](/spl/iterators.html#RegexIterator::getMode)
        — Returns operation mode
    -   [RegexIterator::getPregFlags](/spl/iterators.html#RegexIterator::getPregFlags)
        — Returns the regular expression flags
    -   [RegexIterator::getRegex](/spl/iterators.html#RegexIterator::getRegex)
        — Returns current regular expression
    -   [RegexIterator::setFlags](/spl/iterators.html#RegexIterator::setFlags)
        — Sets the flags
    -   [RegexIterator::setMode](/spl/iterators.html#RegexIterator::setMode)
        — Sets the operation mode
    -   [RegexIterator::setPregFlags](/spl/iterators.html#RegexIterator::setPregFlags)
        — Sets the regular expression flags

SPL 提供一系列迭代器以遍历不同的对象。

SPL Iterators Class Tree
------------------------

-   <span class="simpara"><span
    class="classname">ArrayIterator</span></span>
    -   <span class="simpara"><span
        class="classname">RecursiveArrayIterator</span></span>
-   <span class="simpara"><span
    class="classname">EmptyIterator</span></span>
-   <span class="simpara"><span
    class="classname">IteratorIterator</span></span>
    -   <span class="simpara"><span
        class="classname">AppendIterator</span></span>
    -   <span class="simpara"><span
        class="classname">CachingIterator</span></span>
        -   <span class="simpara"><span
            class="classname">RecursiveCachingIterator</span></span>
    -   <span class="simpara"><span
        class="classname">FilterIterator</span></span>
        -   <span class="simpara"><span
            class="classname">CallbackFilterIterator</span></span>
            -   <span class="simpara"><span
                class="classname">RecursiveCallbackFilterIterator</span></span>
        -   <span class="simpara"><span
            class="classname">RecursiveFilterIterator</span></span>
            -   <span class="simpara"><span
                class="classname">ParentIterator</span></span>
        -   <span class="simpara"><span
            class="classname">RegexIterator</span></span>
            -   <span class="simpara"><span
                class="classname">RecursiveRegexIterator</span></span>
    -   <span class="simpara"><span
        class="classname">InfiniteIterator</span></span>
    -   <span class="simpara"><span
        class="classname">LimitIterator</span></span>
    -   <span class="simpara"><span
        class="classname">NoRewindIterator</span></span>
-   <span class="simpara"><span
    class="classname">MultipleIterator</span></span>
-   <span class="simpara"><span
    class="classname">RecursiveIteratorIterator</span></span>
    -   <span class="simpara"><span
        class="classname">RecursiveTreeIterator</span></span>
-   <span class="simpara"><span
    class="classname">DirectoryIterator</span> (extends <span
    class="classname">SplFileInfo</span>)</span>
    -   <span class="simpara"><span
        class="classname">FilesystemIterator</span></span>
        -   <span class="simpara"><span
            class="classname">GlobIterator</span></span>
        -   <span class="simpara"><span
            class="classname">RecursiveDirectoryIterator</span></span>

简介
----

这个迭代器能陆续遍历几个迭代器

类摘要
------

**AppendIterator**

<span class="ooclass"> class **AppendIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**IteratorIterator** </span> <span class="oointerface">implements <span
class="interfacename">OuterIterator</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">append</span> ( <span class="methodparam"><span
class="type">Iterator</span> `$iterator`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ArrayIterator</span> <span
class="methodname">getArrayIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">getInnerIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getIteratorIndex</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">scalar</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">IteratorIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Traversable</span>
`$iterator`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">IteratorIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Traversable</span> <span
class="methodname">IteratorIterator::getInnerIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">IteratorIterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">IteratorIterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">IteratorIterator::rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IteratorIterator::valid</span> ( <span
class="methodparam">void</span> )

}

AppendIterator::append
======================

Appends an iterator

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">AppendIterator::append</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

Appends an iterator.

### 参数

`iterator`  
The iterator to append.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">AppendIterator::append</span>
example**

``` php
<?php
$array_a = new ArrayIterator(array('a', 'b', 'c'));
$array_b = new ArrayIterator(array('d', 'e', 'f'));

$iterator = new AppendIterator;
$iterator->append($array_a);
$iterator->append($array_b);

foreach ($iterator as $current) {
    echo $current;
}
?>
```

以上例程会输出：

    abcdef

### 参见

-   <span class="methodname">AppendIterator::\_\_construct</span>

AppendIterator::\_\_construct
=============================

Constructs an AppendIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">AppendIterator::\_\_construct</span> ( <span
class="methodparam">void</span> )

Constructs an AppendIterator.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 Iterating AppendIterator with foreach**

``` php
<?php
$pizzas   = new ArrayIterator(array('Margarita', 'Siciliana', 'Hawaii'));
$toppings = new ArrayIterator(array('Cheese', 'Anchovies', 'Olives', 'Pineapple', 'Ham'));

$appendIterator = new AppendIterator;
$appendIterator->append($pizzas);
$appendIterator->append($toppings);

foreach ($appendIterator as $key => $item) {
    echo $key . ' => ' . $item . PHP_EOL;
}
?>
```

以上例程会输出：

    0 => Margarita
    1 => Siciliana
    2 => Hawaii
    0 => Cheese
    1 => Anchovies
    2 => Olives
    3 => Pineapple
    4 => Ham

**示例 \#2 Iterating AppendIterator with the AppendIterator API**

``` php
<?php
$pizzas   = new ArrayIterator(array('Margarita', 'Siciliana', 'Hawaii'));
$toppings = new ArrayIterator(array('Cheese', 'Anchovies', 'Olives', 'Pineapple', 'Ham'));

$appendIterator = new AppendIterator;
$appendIterator->append($pizzas);
$appendIterator->append($toppings);

while ($appendIterator->valid()) {
    printf(
        '%s => %s => %s%s',
        $appendIterator->getIteratorIndex(),
        $appendIterator->key(),
        $appendIterator->current(),
        PHP_EOL
    );
    $appendIterator->next();
}
?>
```

以上例程会输出：

    0 => 0 => Margarita
    0 => 1 => Siciliana
    0 => 2 => Hawaii
    1 => 0 => Cheese
    1 => 1 => Anchovies
    1 => 2 => Olives
    1 => 3 => Pineapple
    1 => 4 => Ham

### 注释

**Caution**

When using <span class="function">iterator\_to\_array</span> to copy the
values of the AppendIterator into an array, you have to set the optional
`use_key` argument to **`FALSE`**. When `use_key` is not **`FALSE`** any
keys reoccuring in inner iterators will get overwritten in the returned
array. There is no way to preserve the original keys.

### 参见

-   <span class="methodname">AppendIterator::append</span>

AppendIterator::current
=======================

Gets the current value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">AppendIterator::current</span> ( <span
class="methodparam">void</span> )

Gets the current value.

### 参数

此函数没有参数。

### 返回值

The current value if it is valid or **`NULL`** otherwise.

### 参见

-   <span class="methodname">Iterator::current</span>
-   <span class="methodname">AppendIterator::key</span>
-   <span class="methodname">AppendIterator::valid</span>
-   <span class="methodname">AppendIterator::next</span>
-   <span class="methodname">AppendIterator::rewind</span>

AppendIterator::getArrayIterator
================================

Gets the ArrayIterator

### 说明

<span class="modifier">public</span> <span
class="type">ArrayIterator</span> <span
class="methodname">AppendIterator::getArrayIterator</span> ( <span
class="methodparam">void</span> )

This method gets the <span class="classname">ArrayIterator</span> that
is used to store the iterators added with <span
class="methodname">AppendIterator::append</span>.

### 参数

此函数没有参数。

### 返回值

Returns an <span class="classname">ArrayIterator</span> containing the
appended iterators.

### 参见

-   <span class="methodname">AppendIterator::getInnerIterator</span>

AppendIterator::getInnerIterator
================================

Gets the inner iterator

### 说明

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">AppendIterator::getInnerIterator</span> ( <span
class="methodparam">void</span> )

This method returns the current inner iterator.

### 参数

此函数没有参数。

### 返回值

The current inner iterator, or **`NULL`** if there is not one.

### 范例

**示例 \#1 <span
class="methodname">AppendIterator::getInnerIterator</span> example**

``` php
<?php
$array_a = new ArrayIterator(array('a' => 'aardwolf', 'b' => 'bear', 'c' => 'capybara'));
$array_b = new RegexIterator($array_a, '/^[ac]/');

$iterator = new AppendIterator;
$iterator->append($array_a);
$iterator->append($array_b);

foreach ($iterator as $current) {
    $inner = $iterator->getInnerIterator();
    if ($inner instanceOf RegexIterator) {
        echo 'Filtered: ';
    } else {
        echo 'Original: ';
    }
    echo $current . PHP_EOL;
}
?>
```

以上例程会输出：

    Original: aardwolf
    Original: bear
    Original: capybara
    Filtered: aardwolf
    Filtered: capybara

### 参见

-   <span class="methodname">AppendIterator::getIteratorIndex</span>

AppendIterator::getIteratorIndex
================================

Gets an index of iterators

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">AppendIterator::getIteratorIndex</span> ( <span
class="methodparam">void</span> )

Gets the index of the current inner iterator.

### 参数

此函数没有参数。

### 返回值

Returns an <span class="type">integer</span>, which is the zero-based
index of the current inner iterator.

### 范例

**示例 \#1 <span
class="methodname">AppendIterator.getIteratorIndex</span> basic
example**

``` php
<?php
$array_a = new ArrayIterator(array('a' => 'aardwolf', 'b' => 'bear', 'c' => 'capybara'));
$array_b = new ArrayIterator(array('apple', 'orange', 'lemon'));

$iterator = new AppendIterator;
$iterator->append($array_a);
$iterator->append($array_b);

foreach ($iterator as $key => $current) {
    echo $iterator->getIteratorIndex() . '  ' . $key . ' ' . $current . PHP_EOL;
}
?>
```

以上例程会输出：

    0  a aardwolf
    0  b bear
    0  c capybara
    1  0 apple
    1  1 orange
    1  2 lemon

### 参见

-   <span class="methodname">AppendIterator::getInnerIterator</span>
-   <span class="methodname">AppendIterator::getArrayIterator</span>

AppendIterator::key
===================

Gets the current key

### 说明

<span class="modifier">public</span> <span class="type">scalar</span>
<span class="methodname">AppendIterator::key</span> ( <span
class="methodparam">void</span> )

Get the current key.

### 参数

此函数没有参数。

### 返回值

The current key if it is valid or **`NULL`** otherwise.

### 范例

**示例 \#1 <span class="methodname">AppendIterator::key</span> basic
example**

``` php
<?php
$array_a = new ArrayIterator(array('a' => 'aardwolf', 'b' => 'bear', 'c' => 'capybara'));
$array_b = new ArrayIterator(array('apple', 'orange', 'lemon'));

$iterator = new AppendIterator;
$iterator->append($array_a);
$iterator->append($array_b);

// Manual iteration
$iterator->rewind();
while ($iterator->valid()) {
    echo $iterator->key() . ' ' . $iterator->current() . PHP_EOL;
    $iterator->next();
}

echo PHP_EOL;

// With foreach
foreach ($iterator as $key => $current) {
    echo $key . ' ' . $current . PHP_EOL;
}
?>
```

以上例程会输出：

    a aardwolf
    b bear
    c capybara
    0 apple
    1 orange
    2 lemon

    a aardwolf
    b bear
    c capybara
    0 apple
    1 orange
    2 lemon

### 参见

-   <span class="methodname">Iterator::key</span>
-   <span class="methodname">AppendIterator::current</span>
-   <span class="methodname">AppendIterator::valid</span>
-   <span class="methodname">AppendIterator::next</span>
-   <span class="methodname">AppendIterator::rewind</span>

AppendIterator::next
====================

Moves to the next element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">AppendIterator::next</span> ( <span
class="methodparam">void</span> )

Moves to the next element. If this means to another Iterator then it
rewinds that Iterator.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">Iterator::next</span>
-   <span class="methodname">AppendIterator::current</span>
-   <span class="methodname">AppendIterator::key</span>
-   <span class="methodname">AppendIterator::valid</span>
-   <span class="methodname">AppendIterator::rewind</span>

AppendIterator::rewind
======================

Rewinds the Iterator

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">AppendIterator::rewind</span> ( <span
class="methodparam">void</span> )

Rewind to the first element of the first inner Iterator.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">Iterator::rewind</span>
-   <span class="methodname">AppendIterator::current</span>
-   <span class="methodname">AppendIterator::key</span>
-   <span class="methodname">AppendIterator::next</span>
-   <span class="methodname">AppendIterator::valid</span>

AppendIterator::valid
=====================

Checks validity of the current element

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">AppendIterator::valid</span> ( <span
class="methodparam">void</span> )

Checks validity of the current element.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the current iteration is valid, **`FALSE`**
otherwise.

### 参见

-   <span class="methodname">AppendIterator::current</span>
-   <span class="methodname">AppendIterator::key</span>
-   <span class="methodname">AppendIterator::next</span>
-   <span class="methodname">AppendIterator::rewind</span>

简介
----

这个迭代器允许在遍历数组和对象时删除和更新值与键。

当你想多次遍历相同数组时你需要实例化 ArrayObject，然后让这个实例创建一个
ArrayIteratror 实例。 当你想遍历相同数组时多次你需要实例 ArrayObject
并且让这个实例创建一个 ArrayIteratror
实例，然后使用<a href="/control-structures/foreach.html" class="link">foreach</a>
或者 手动调用 getIterator() 方法。

类摘要
------

**ArrayIterator**

<span class="ooclass"> class **ArrayIterator** </span> <span
class="oointerface">implements <span
class="interfacename">ArrayAccess</span> </span> <span
class="oointerface">, <span
class="interfacename">SeekableIterator</span> </span> <span
class="oointerface">, <span class="interfacename">Countable</span>
</span> <span class="oointerface">, <span
class="interfacename">Serializable</span> </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`STD_PROP_LIST` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ARRAY_AS_PROPS` <span class="initializer"> = 2</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">append</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">asort</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$array`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getArrayCopy</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ksort</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">natcasesort</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">natsort</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">offsetExists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">offsetGet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetSet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$newval`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetUnset</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">seek</span> ( <span class="methodparam"><span
class="type">int</span> `$position`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setFlags</span> ( <span
class="methodparam"><span class="type">string</span> `$flags`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">uasort</span> ( <span class="methodparam"><span
class="type">callable</span> `$cmp_function`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">uksort</span> ( <span class="methodparam"><span
class="type">callable</span> `$cmp_function`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

ArrayIterator 标记
------------------

**`ArrayIterator::STD_PROP_LIST`**  
Properties of the object have their normal functionality when accessed
as list (var\_dump, foreach, etc.).

**`ArrayIterator::ARRAY_AS_PROPS`**  
可以通过属性访问条目（读写都支持）。

ArrayIterator::append
=====================

Append an element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::append</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

Appends value as the last element.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`value`  
The value to append.

### 返回值

没有返回值。

### 注释

> **Note**:
>
> This method cannot be called when the <span
> class="classname">ArrayIterator</span> refers to an <span
> class="type">object</span>.

### 参见

-   <span class="methodname">ArrayIterator::next</span>

ArrayIterator::asort
====================

Sort array by values

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::asort</span> ( <span
class="methodparam">void</span> )

Sorts an array by values.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">ArrayIterator::ksort</span>
-   <span class="methodname">ArrayIterator::natcasesort</span>
-   <span class="methodname">ArrayIterator::natsort</span>

ArrayIterator::\_\_construct
============================

Construct an ArrayIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">ArrayIterator::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$array`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \]\] )

Constructs an <span class="classname">ArrayIterator</span> <span
class="type">object</span>.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`array`  
The array or object to be iterated on.

`flags`  
Flags to control the behaviour of the <span
class="classname">ArrayIterator</span> object. See <span
class="methodname">ArrayIterator::setFlags</span>.

### 返回值

An <span class="classname">ArrayIterator</span> <span
class="type">object</span>.

### 错误／异常

<span class="function">ArrayIterator::\_\_construct</span> throws an
<span class="classname">InvalidArgumentException</span> if anything
besides an array or an object is given.

### 参见

-   <span class="methodname">ArrayIterator::getArrayCopy</span>

ArrayIterator::count
====================

Count elements

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ArrayIterator::count</span> ( <span
class="methodparam">void</span> )

Gets the number of elements in the <span class="type">array</span>, or
the number of public properties in the <span class="type">object</span>.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The number of elements or public properties in the associated <span
class="type">array</span> or <span class="type">object</span>,
respectively.

### 参见

-   <span class="methodname">ArrayIterator::getFlags</span>

ArrayIterator::current
======================

Return current array entry

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ArrayIterator::current</span> ( <span
class="methodparam">void</span> )

Get the current <span class="type">array</span> entry.

### 参数

此函数没有参数。

### 返回值

The current <span class="type">array</span> entry.

### 范例

**示例 \#1 <span class="function">ArrayIterator::current</span>
example**

``` php
<?php
$array = array('1' => 'one',
               '2' => 'two',
               '3' => 'three');

$arrayobject = new ArrayObject($array);

for($iterator = $arrayobject->getIterator();
    $iterator->valid();
    $iterator->next()) {

    echo $iterator->key() . ' => ' . $iterator->current() . "\n";
}
?>
```

以上例程会输出：

    1 => one
    2 => two
    3 => three

ArrayIterator::getArrayCopy
===========================

Get array copy

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ArrayIterator::getArrayCopy</span> ( <span
class="methodparam">void</span> )

Get a copy of an array.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

A copy of the <span class="type">array</span>, or array of public
properties if ArrayIterator refers to an <span
class="type">object</span>.

### 参见

-   <span class="methodname">ArrayIterator::valid</span>

ArrayIterator::getFlags
=======================

Get behavior flags

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ArrayIterator::getFlags</span> ( <span
class="methodparam">void</span> )

Gets the behavior flags of the <span
class="classname">ArrayIterator</span>. See the
<a href="/spl/iterators.html#ArrayIterator::setFlags" class="link">ArrayIterator::setFlags</a>
method for a list of the available flags.

### 参数

此函数没有参数。

### 返回值

Returns the behavior flags of the ArrayIterator.

### 参见

-   <span class="methodname">\>ArrayIterator::setFlags</span>
-   <span class="methodname">ArrayIterator::valid</span>

ArrayIterator::key
==================

Return current array key

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ArrayIterator::key</span> ( <span
class="methodparam">void</span> )

This function returns the current array key

### 参数

此函数没有参数。

### 返回值

The current <span class="type">array</span> key.

### 范例

**示例 \#1 <span class="function">ArrayIterator::key</span> example**

``` php
<?php
$array = array('key' => 'value');

$arrayobject = new ArrayObject($array);
$iterator = $arrayobject->getIterator();

echo $iterator->key(); //key
?>
```

ArrayIterator::ksort
====================

Sort array by keys

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::ksort</span> ( <span
class="methodparam">void</span> )

Sorts an array by the keys.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">ArrayIterator::asort</span>
-   <span class="methodname">ArrayIterator::natcasesort</span>
-   <span class="methodname">ArrayIterator::natsort</span>

ArrayIterator::natcasesort
==========================

Sort an array naturally, case insensitive

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::natcasesort</span> ( <span
class="methodparam">void</span> )

Sort the entries by values using a case insensitive "natural order"
algorithm.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">ArrayIterator::asort</span>
-   <span class="methodname">ArrayIterator::ksort</span>
-   <span class="methodname">ArrayIterator::natsort</span>
-   <span class="function">natcasesort</span>

ArrayIterator::natsort
======================

Sort an array naturally

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::natsort</span> ( <span
class="methodparam">void</span> )

Sort the entries by values using "natural order" algorithm.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">ArrayIterator::asort</span>
-   <span class="methodname">ArrayIterator::ksort</span>
-   <span class="methodname">ArrayIterator::natcasesort</span>
-   <span class="function">natsort</span>

ArrayIterator::next
===================

Move to next entry

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::next</span> ( <span
class="methodparam">void</span> )

The iterator to the next entry.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">ArrayIterator::next</span> example**

``` php
<?php
$arrayobject = new ArrayObject();

$arrayobject[] = 'zero';
$arrayobject[] = 'one';

$iterator = $arrayobject->getIterator();

while($iterator->valid()) {
    echo $iterator->key() . ' => ' . $iterator->current() . "\n";

    $iterator->next();
}
?>
```

以上例程会输出：

    0 => zero
    1 => one

ArrayIterator::offsetExists
===========================

Check if offset exists

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ArrayIterator::offsetExists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

Checks if the offset exists.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`index`  
The offset being checked.

### 返回值

**`TRUE`** if the offset exists, otherwise **`FALSE`**

### 参见

-   <span class="methodname">ArrayIterator::valid</span>

ArrayIterator::offsetGet
========================

Get value for an offset

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ArrayIterator::offsetGet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

Gets the value from the provided offset.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`index`  
The offset to get the value from.

### 返回值

The value at offset `index`.

### 参见

-   <span class="methodname">ArrayIterator::offsetSet</span>
-   <span class="methodname">ArrayIterator::offsetUnset</span>

ArrayIterator::offsetSet
========================

Set value for an offset

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::offsetSet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$newval`</span> )

Sets a value for a given offset.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`index`  
The index to set for.

`newval`  
The new value to store at the index.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">ArrayIterator::offsetGet</span>
-   <span class="methodname">ArrayIterator::offsetUnset</span>

ArrayIterator::offsetUnset
==========================

Unset value for an offset

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::offsetUnset</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

Unsets a value for an offset.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`index`  
The offset to unset.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">ArrayIterator::offsetGet</span>
-   <span class="methodname">ArrayIterator::offsetSet</span>

ArrayIterator::rewind
=====================

Rewind array back to the start

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::rewind</span> ( <span
class="methodparam">void</span> )

This rewinds the iterator to the beginning.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">ArrayIterator::rewind</span> example**

``` php
<?php
$arrayobject = new ArrayObject();

$arrayobject[] = 'zero';
$arrayobject[] = 'one';
$arrayobject[] = 'two';

$iterator = $arrayobject->getIterator();

$iterator->next();
echo $iterator->key(); //1

$iterator->rewind(); //rewinding to the begining
echo $iterator->key(); //0
?>
```

ArrayIterator::seek
===================

Seek to position

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::seek</span> ( <span
class="methodparam"><span class="type">int</span> `$position`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`position`  
The position to seek to.

### 返回值

没有返回值。

ArrayIterator::serialize
========================

Serialize

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ArrayIterator::serialize</span> ( <span
class="methodparam">void</span> )

Serialize.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The serialized <span class="classname">ArrayIterator</span>.

### 参见

-   <span class="methodname">ArrayIterator::unserialize</span>

ArrayIterator::setFlags
=======================

Set behaviour flags

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::setFlags</span> ( <span
class="methodparam"><span class="type">string</span> `$flags`</span> )

Set the flags that change the behavior of the ArrayIterator.

### 参数

`flags`  
The new ArrayIterator behavior. It takes on either a bitmask, or named
constants. Using named constants is strongly encouraged to ensure
compatibility for future versions.

The available behavior flags are listed below. The actual meanings of
these flags are described in the
<a href="/spl/iterators.html#预定义常量" class="link">predefined constants</a>.

| value | constant                                                                      |
|-------|-------------------------------------------------------------------------------|
| 1     | <a href="/spl/iterators.html#" class="link">ArrayIterator::STD_PROP_LIST</a>  |
| 2     | <a href="/spl/iterators.html#" class="link">ArrayIterator::ARRAY_AS_PROPS</a> |

### 返回值

没有返回值。

### 参见

-   <span class="methodname">ArrayIterator::getFlags</span>

ArrayIterator::uasort
=====================

Sort with a user-defined comparison function and maintain index
association

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::uasort</span> ( <span
class="methodparam"><span class="type">callable</span>
`$cmp_function`</span> )

This method sorts the elements such that indices maintain their
correlation with the values they are associated with, using a
user-defined comparison function.

> **Note**:
>
> If two members compare as equal, their relative order in the sorted
> array is undefined.

### 参数

`cmp_function`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

### 返回值

没有返回值。

### 参见

-   <span class="methodname">ArrayIterator::asort</span>
-   <span class="methodname">ArrayIterator::uksort</span>
-   <span class="function">usort</span>

ArrayIterator::uksort
=====================

Sort by keys using a user-defined comparison function

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::uksort</span> ( <span
class="methodparam"><span class="type">callable</span>
`$cmp_function`</span> )

This method sorts the elements by keys using a user-supplied comparison
function.

> **Note**:
>
> If two members compare as equal, their relative order in the sorted
> array is undefined.

### 参数

`cmp_function`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

### 返回值

没有返回值。

### 参见

-   <span class="methodname">ArrayIterator::ksort</span>
-   <span class="methodname">ArrayIterator::uasort</span>
-   <span class="function">uksort</span>

ArrayIterator::unserialize
==========================

Unserialize

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

Unserialize.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`serialized`  
The serialized ArrayIterator object to be unserialized.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">ArrayIterator::serialize</span>

ArrayIterator::valid
====================

Check whether array contains more entries

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ArrayIterator::valid</span> ( <span
class="methodparam">void</span> )

Checks if the <span class="type">array</span> contains any more entries.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the iterator is valid, otherwise **`FALSE`**

### 范例

**示例 \#1 <span class="function">ArrayIterator::valid</span> example**

``` php
<?php
$array = array('1' => 'one');

$arrayobject = new ArrayObject($array);
$iterator = $arrayobject->getIterator();

var_dump($iterator->valid()); //bool(true)

$iterator->next(); // advance to the next item

//bool(false) because there is only one array element
var_dump($iterator->valid());
?>
```

简介
----

This object supports cached iteration over another iterator.

类摘要
------

**CachingIterator**

<span class="ooclass"> class **CachingIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**IteratorIterator** </span> <span class="oointerface">implements <span
class="interfacename">OuterIterator</span> </span> <span
class="oointerface">, <span class="interfacename">ArrayAccess</span>
</span> <span class="oointerface">, <span
class="interfacename">Countable</span> </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CachingIterator::CALL_TOSTRING` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CachingIterator::CATCH_GET_CHILD` <span class="initializer"> =
16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CachingIterator::TOSTRING_USE_KEY` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CachingIterator::TOSTRING_USE_CURRENT` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CachingIterator::TOSTRING_USE_INNER` <span class="initializer"> =
8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CachingIterator::FULL_CACHE` <span class="initializer"> = 256</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
self::CALL\_TOSTRING</span></span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getCache</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">getInnerIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">hasNext</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">scalar</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetExists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetGet</span> ( <span
class="methodparam"><span class="type">string</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetSet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$newval`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetUnset</span> ( <span
class="methodparam"><span class="type">string</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setFlags</span> ( <span
class="methodparam"><span class="type">int</span> `$flags`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`CachingIterator::CALL_TOSTRING`**  
Convert every element to string.

**`CachingIterator::CATCH_GET_CHILD`**  
Don't throw exception in accessing children.

**`CachingIterator::TOSTRING_USE_KEY`**  
Use
<a href="/spl/iterators.html#CachingIterator::key" class="link">key</a>
for conversion to string.

**`CachingIterator::TOSTRING_USE_CURRENT`**  
Use
<a href="/spl/iterators.html#CachingIterator::current" class="link">current</a>
for conversion to string.

**`CachingIterator::TOSTRING_USE_INNER`**  
Use
<a href="/spl/iterators.html#CachingIterator::getInnerIterator" class="link">inner</a>
for conversion to string.

**`CachingIterator::FULL_CACHE`**  
Cache all read data.

CachingIterator::\_\_construct
==============================

Construct a new CachingIterator object for the iterator

### 说明

<span class="modifier">public</span> <span
class="methodname">CachingIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
self::CALL\_TOSTRING</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`iterator`  
Iterator to cache

`flags`  
Bitmask of flags.

CachingIterator::count
======================

The number of elements in the iterator

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CachingIterator::count</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

May return the number of elements in the iterator.

### 参数

此函数没有参数。

### 返回值

The count of the elements iterated over.

CachingIterator::current
========================

Return the current element

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">CachingIterator::current</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

May return the current element in the iteration.

### 参数

此函数没有参数。

### 返回值

Mixed

### 参见

-   <span class="methodname">Iterator::current</span>

CachingIterator::getCache
=========================

Retrieve the contents of the cache

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CachingIterator::getCache</span> ( <span
class="methodparam">void</span> )

Retrieve the contents of the cache.

> **Note**:
>
> The **`CachingIterator::FULL_CACHE`** flag must be being used.

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> containing the cache items.

### 错误／异常

Throws a <span class="classname">BadMethodCallException</span> when the
**`CachingIterator::FULL_CACHE`** flag is not being used.

### 范例

**示例 \#1 <span class="methodname">CachingIterator::getCache</span>
example**

``` php
<?php
$iterator = new ArrayIterator(array(1, 2, 3));
$cache    = new CachingIterator($iterator, CachingIterator::FULL_CACHE);

$cache->next();
$cache->next();
var_dump($cache->getCache());

$cache->next();
var_dump($cache->getCache());
?>
```

以上例程会输出：

    array(2) {
      [0]=>
      int(1)
      [1]=>
      int(2)
    }
    array(3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

CachingIterator::getFlags
=========================

Get flags used

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CachingIterator::getFlags</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Get the bitmask of the flags used for this CachingIterator instance.

### 参数

此函数没有参数。

### 返回值

Description...

CachingIterator::getInnerIterator
=================================

Returns the inner iterator

### 说明

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">CachingIterator::getInnerIterator</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Returns the iterator sent to the constructor.

### 参数

此函数没有参数。

### 返回值

Returns an object implementing the Iterator interface.

CachingIterator::hasNext
========================

Check whether the inner iterator has a valid next element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::hasNext</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

CachingIterator::key
====================

Return the key for the current element

### 说明

<span class="modifier">public</span> <span class="type">scalar</span>
<span class="methodname">CachingIterator::key</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

This method may return a key for the current element.

### 参数

此函数没有参数。

CachingIterator::next
=====================

Move the iterator forward

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::next</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Move the iterator forward.

### 参数

此函数没有参数。

### 返回值

没有返回值。

CachingIterator::offsetExists
=============================

The offsetExists purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::offsetExists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`index`  
The index being checked.

### 返回值

Returns **`TRUE`** if an entry referenced by the offset exists,
**`FALSE`** otherwise.

CachingIterator::offsetGet
==========================

The offsetGet purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::offsetGet</span> ( <span
class="methodparam"><span class="type">string</span> `$index`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`index`  
Description...

### 返回值

Description...

CachingIterator::offsetSet
==========================

The offsetSet purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::offsetSet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$newval`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`index`  
The index of the element to be set.

`newval`  
The new value for the `index`.

### 返回值

没有返回值。

CachingIterator::offsetUnset
============================

The offsetUnset purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::offsetUnset</span> ( <span
class="methodparam"><span class="type">string</span> `$index`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`index`  
The index of the element to be unset.

### 返回值

没有返回值。

CachingIterator::rewind
=======================

Rewind the iterator

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::rewind</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Rewind the iterator.

### 参数

此函数没有参数。

### 返回值

没有返回值。

CachingIterator::setFlags
=========================

The setFlags purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::setFlags</span> ( <span
class="methodparam"><span class="type">int</span> `$flags`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Set the flags for the CachingIterator object.

### 参数

`flags`  
Bitmask of the flags to set.

### 返回值

没有返回值。

CachingIterator::\_\_toString
=============================

Return the string representation of the current element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::\_\_toString</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Get the string representation of the current element.

### 参数

此函数没有参数。

### 返回值

The <span class="type">string</span> representation of the current
element.

CachingIterator::valid
======================

Check whether the current element is valid

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::valid</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Check whether the current element is valid.

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

简介
----

类摘要
------

**CallbackFilterIterator**

<span class="ooclass"> class **CallbackFilterIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**FilterIterator** </span> <span class="oointerface">implements <span
class="interfacename">OuterIterator</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">accept</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="modifier">abstract</span> <span class="type">bool</span> <span
class="methodname">FilterIterator::accept</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">FilterIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">FilterIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">FilterIterator::getInnerIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">FilterIterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilterIterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilterIterator::rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">FilterIterator::valid</span> ( <span
class="methodparam">void</span> )

}

范例
----

The callback should accept up to three arguments: the current item, the
current key and the iterator, respectively.

**示例 \#1 Available callback arguments**

``` php
<?php

/**
 * Callback for CallbackFilterIterator
 *
 * @param $current   Current item's value
 * @param $key       Current item's key
 * @param $iterator  Iterator being filtered
 * @return boolean   TRUE to accept the current item, FALSE otherwise
 */
function my_callback($current, $key, $iterator) {
    // Your filtering code here
}

?>
```

Any <span class="type">callable</span> may be used; such as a string
containing a function name, an array for a method, or an anonymous
function.

**示例 \#2 Callback basic examples**

``` php
<?php

$dir = new FilesystemIterator(__DIR__);

// Filter large files ( > 100MB)
function is_large_file($current) {
    return $current->isFile() && $current->getSize() > 104857600;
}
$large_files = new CallbackFilterIterator($dir, 'is_large_file');

// Filter directories
$files = new CallbackFilterIterator($dir, function ($current, $key, $iterator) {
    return $current->isDir() && ! $iterator->isDot();
});

?>
```

CallbackFilterIterator::accept
==============================

Calls the callback with the current value, the current key and the inner
iterator as arguments

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">CallbackFilterIterator::accept</span> ( <span
class="methodparam">void</span> )

This method calls the callback with the current value, current key and
the inner iterator.

The callback is expected to return **`TRUE`** if the current item is to
be accepted, or **`FALSE`** otherwise.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** to accept the current item, or **`FALSE`** otherwise.

### 参见

-   <a href="/spl/iterators.html#范例" class="link">CallbackFilterIterator Examples</a>
-   <span
    class="methodname">CallbackFilterIterator::\_\_construct</span>

CallbackFilterIterator::\_\_construct
=====================================

Create a filtered iterator from another iterator

### 说明

<span class="modifier">public</span> <span
class="methodname">CallbackFilterIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

Creates a filtered iterator using the `callback` to determine which
items are accepted or rejected.

### 参数

`iterator`  
The iterator to be filtered.

`callback`  
The callback, which should return **`TRUE`** to accept the current item
or **`FALSE`** otherwise. See
<a href="/spl/iterators.html#范例" class="link">Examples</a>.

May be any valid <span class="type">callable</span> value.

### 返回值

没有返回值。

### 参见

-   <a href="/spl/iterators.html#范例" class="link">CallbackFilterIterator Examples</a>
-   <span class="methodname">CallbackFilterIterator::accept</span>

简介
----

The DirectoryIterator class provides a simple interface for viewing the
contents of filesystem directories.

类摘要
------

**DirectoryIterator**

<span class="ooclass"> class **DirectoryIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span> **SplFileInfo**
</span> <span class="oointerface">implements <span
class="interfacename">SeekableIterator</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

<span class="modifier">public</span> <span
class="type">DirectoryIterator</span> <span
class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getATime</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getBasename</span> (\[ <span
class="methodparam"> <span class="type">string</span> `$suffix` </span>
\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getCTime</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getExtension</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getFilename</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getGroup</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getInode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getMTime</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getOwner</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getPath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getPathname</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getPerms</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isDir</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isDot</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isExecutable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isLink</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isReadable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isWritable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">seek</span> ( <span class="methodparam"><span
class="type">int</span> `$position`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

更新日志
--------

| 版本  | 说明                                                                                                 |
|-------|------------------------------------------------------------------------------------------------------|
| 5.1.2 | <span class="classname">DirectoryIterator</span> extends <span class="classname">SplFileInfo</span>. |

DirectoryIterator::\_\_construct
================================

Constructs a new directory iterator from a path

### 说明

<span class="modifier">public</span> <span
class="methodname">DirectoryIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

Constructs a new directory iterator from a path.

### 参数

`path`  
The path of the directory to traverse.

### 错误／异常

Throws an <span class="classname">UnexpectedValueException</span> if the
`path` cannot be opened.

Throws a <span class="classname">RuntimeException</span> if the `path`
is an empty string.

### 更新日志

| 版本  | 说明                                                                                                                         |
|-------|------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0 | Throws <span class="classname">UnexpectedValueException</span> if the `path` cannot be opened.                               |
| 5.1.3 | Throws <span class="classname">RuntimeException</span> if the `path` is an empty string.                                     |
| 5.1.0 | Throws <span class="classname">RuntimeException</span> on error. Previously, threw <span class="classname">Exception</span>. |

### 范例

**示例 \#1 A <span
class="methodname">DirectoryIterator::\_\_construct</span> example**

This example will list the contents of the directory containing the
script.

``` php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    if (!$fileinfo->isDot()) {
        var_dump($fileinfo->getFilename());
    }
}
?>
```

### 参见

-   <span class="classname">SplFileInfo</span>
-   <span class="classname">Iterator</span>

DirectoryIterator::current
==========================

Return the current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span
class="type">DirectoryIterator</span> <span
class="methodname">DirectoryIterator::current</span> ( <span
class="methodparam">void</span> )

Get the current <span class="classname">DirectoryIterator</span> item.

### 参数

此函数没有参数。

### 返回值

The current <span class="classname">DirectoryIterator</span> item.

### 范例

**示例 \#1 A <span class="methodname">DirectoryIterator::current</span>
example**

This example will list the contents of the directory containing the
script.

``` php
<?php
$iterator = new DirectoryIterator(__DIR__);
while($iterator->valid()) {
    $file = $iterator->current();
    echo $iterator->key() . " => " . $file->getFilename() . "\n";
    $iterator->next();
}
?>
```

以上例程的输出类似于：

    0 => .
    1 => ..
    2 => apple.jpg
    3 => banana.jpg
    4 => index.php
    5 => pear.jpg

### 参见

-   <span class="methodname">DirectoryIterator::key</span>
-   <span class="methodname">DirectoryIterator::next</span>
-   <span class="methodname">DirectoryIterator::rewind</span>
-   <span class="methodname">DirectoryIterator::valid</span>
-   <span class="methodname">Iterator::current</span>

DirectoryIterator::getATime
===========================

Get last access time of the current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getATime</span> ( <span
class="methodparam">void</span> )

Get the last access time of the current <span
class="classname">DirectoryIterator</span> item.

### 参数

此函数没有参数。

### 返回值

Returns the time the file was last accessed, as a Unix timestamp.

### 范例

**示例 \#1 A <span class="methodname">DirectoryIterator::getATime</span>
example**

Displays a list of the files in the directory of the script and their
last access times.

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isFile()) {
        echo $fileinfo->getFilename() . " " . $fileinfo->getATime() . "\n";
    }
}
?>
```

以上例程的输出类似于：

    apple.jpg 1240047118
    banana.jpg 1240065176
    index.php 1240047208
    pear.jpg 12240047979

### 参见

-   <span class="methodname">DirectoryIterator::getCTime</span>
-   <span class="methodname">DirectoryIterator::getMTime</span>
-   <span class="function">fileatime</span>

DirectoryIterator::getBasename
==============================

Get base name of current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::getBasename</span> (\[ <span
class="methodparam"> <span class="type">string</span> `$suffix` </span>
\] )

Get the base name of the current <span
class="classname">DirectoryIterator</span> item.

### 参数

`suffix`  
If the base name ends in `suffix`, this will be cut.

### 返回值

The base name of the current <span
class="classname">DirectoryIterator</span> item.

### 范例

**示例 \#1 A <span
class="methodname">DirectoryIterator::getBasename</span> example**

This example will list the full base name and the base name with suffix
*.jpg* removed for the files in the directory containing the script.

``` php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    if ($fileinfo->isFile()) {
        echo $fileinfo->getBasename() . "\n";
        echo $fileinfo->getBasename('.jpg') . "\n";
    }
}
?>
```

以上例程的输出类似于：

    apple.jpg
    apple
    banana.jpg
    banana
    index.php
    index.php
    pear.jpg
    pear

### 参见

-   <span class="methodname">DirectoryIterator::getFilename</span>
-   <span class="methodname">DirectoryIterator::getPath</span>
-   <span class="methodname">DirectoryIterator::getPathname</span>
-   <span class="function">basename</span>
-   <span class="function">pathinfo</span>

DirectoryIterator::getCTime
===========================

Get inode change time of the current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getCTime</span> ( <span
class="methodparam">void</span> )

Get the inode change time for the current <span
class="classname">DirectoryIterator</span> item.

### 参数

此函数没有参数。

### 返回值

Returns the last change time of the file, as a Unix timestamp.

### 范例

**示例 \#1 <span class="function">DirectoryIterator::getCTime</span>
example**

This example displays the file name and last change time of the files in
the directory containing the script.

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isFile()) {
        echo $fileinfo->getFilename() . " changed at " . $fileinfo->getCTime() . "\n";
    }
}
?>
```

以上例程的输出类似于：

    apple.jpg changed at 1240398312
    banana.jpg changed at 1238605440
    index.php changed at 1240398935
    pear.jpg changed at 1237423740

### 参见

-   <span class="methodname">DirectoryIterator::getATime</span>
-   <span class="methodname">DirectoryIterator::getMTime</span>
-   <span class="function">filectime</span>

DirectoryIterator::getExtension
===============================

Gets the file extension

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::getExtension</span> ( <span
class="methodparam">void</span> )

Retrieves the file extension.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="type">string</span> containing the file
extension, or an empty <span class="type">string</span> if the file has
no extension.

### 范例

**示例 \#1 <span class="function">DirectoryIterator::getExtension</span>
example**

``` php
<?php

$directory = new DirectoryIterator(__DIR__);
foreach ($directory as $fileinfo) {
    if ($fileinfo->isFile()) {
        echo $fileinfo->getExtension() . "\n";
    }
}

?>
```

以上例程的输出类似于：

    php
    txt
    jpg
    gz

### 注释

> **Note**:
>
> This method is only available as of PHP 5.3.6. Another way of getting
> the extension is to use the <span class="function">pathinfo</span>
> function.
>
> ``` php
> <?php
> $extension = pathinfo($fileinfo->getFilename(), PATHINFO_EXTENSION);
> ?>
> ```

### 参见

-   <span class="methodname">DirectoryIterator::getFilename</span>
-   <span class="methodname">DirectoryIterator::getBasename</span>
-   <span class="function">pathinfo</span>

DirectoryIterator::getFilename
==============================

Return file name of current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::getFilename</span> ( <span
class="methodparam">void</span> )

Get the file name of the current <span
class="classname">DirectoryIterator</span> item.

### 参数

此函数没有参数。

### 返回值

Returns the file name of the current <span
class="classname">DirectoryIterator</span> item.

### 范例

**示例 \#1 A <span
class="methodname">DirectoryIterator::getFilename</span> example**

This example will list the contents of the directory containing the
script.

``` php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    echo $fileinfo->getFilename() . "\n";
}
?>
```

以上例程的输出类似于：

    .
    ..
    apple.jpg
    banana.jpg
    index.php
    pear.jpg

### 参见

-   <span class="methodname">DirectoryIterator::getBasename</span>
-   <span class="methodname">DirectoryIterator::getPath</span>
-   <span class="methodname">DirectoryIterator::getPathname</span>
-   <span class="function">pathinfo</span>

DirectoryIterator::getGroup
===========================

Get group for the current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getGroup</span> ( <span
class="methodparam">void</span> )

Get the group id of the file.

### 参数

此函数没有参数。

### 返回值

Returns the group id of the current <span
class="classname">DirectoryIterator</span> item in numerical format.

### 范例

**示例 \#1 <span class="function">DirectoryIterator::getGroup</span>
example**

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
$groupid  = $iterator->getGroup();
echo 'Directory belongs to group id ' . $groupid . "\n";
print_r(posix_getgrgid($groupid));
?>
```

以上例程的输出类似于：

    Directory belongs to group id 42
    Array
    (
        [name]    => toons
        [passwd]  => x
        [members] => Array
            (
                [0] => tom
                [1] => jerry
            )
        [gid]     => 42
    )

### 参见

-   <span class="methodname">DirectoryIterator::getiNode</span>
-   <span class="methodname">DirectoryIterator::getOwner</span>
-   <span class="methodname">DirectoryIterator::getPerms</span>
-   <span class="function">filegroup</span>
-   <span class="function">posix\_getgrgid</span>

DirectoryIterator::getInode
===========================

Get inode for the current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getInode</span> ( <span
class="methodparam">void</span> )

Get the inode number for the current <span
class="classname">DirectoryIterator</span> item.

### 参数

此函数没有参数。

### 返回值

Returns the inode number for the file.

### 范例

**示例 \#1 <span class="function">DirectoryIterator::getInode</span>
example**

This example displays the inode number for the directory containing the
script.

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
echo $iterator->getInode();
?>
```

### 参见

-   <span class="methodname">DirectoryIterator::getGroup</span>
-   <span class="methodname">DirectoryIterator::getOwner</span>
-   <span class="methodname">DirectoryIterator::getPerms</span>
-   <span class="function">fileinode</span>

DirectoryIterator::getMTime
===========================

Get last modification time of current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getMTime</span> ( <span
class="methodparam">void</span> )

Get the last modification time of the current <span
class="classname">DirectoryIterator</span> item, as a Unix timestamp.

### 参数

此函数没有参数。

### 返回值

The last modification time of the file, as a Unix timestamp.

### 范例

**示例 \#1 A <span class="methodname">DirectoryIterator::getMTime</span>
example**

Displays a list of the files in the directory of the script and their
last modified times.

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isFile()) {
        echo $fileinfo->getFilename() . " " . $fileinfo->getMTime() . "\n";
    }
}
?>
```

以上例程的输出类似于：

    apple.jpg 1240047118
    banana.jpg 1240065176
    index.php 1240047208
    pear.jpg 12240047979

### 参见

-   <span class="methodname">DirectoryIterator::getATime</span>
-   <span class="methodname">DirectoryIterator::getCTime</span>
-   <span class="function">filemtime</span>

DirectoryIterator::getOwner
===========================

Get owner of current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getOwner</span> ( <span
class="methodparam">void</span> )

Get the owner of the current <span
class="classname">DirectoryIterator</span> item, in numerical format.

### 参数

此函数没有参数。

### 返回值

The file owner of the file, in numerical format.

### 范例

**示例 \#1 <span class="methodname">DirectoryIterator::getOwner</span>
example**

This example displays the owner of the directory which contains the
script.

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
print_r(posix_getpwuid($iterator->getOwner()));
?>
```

以上例程的输出类似于：

    Array
    (
        [name] => tom
        [passwd] => x
        [uid] => 501
        [gid] => 42
        [gecos] => Tom Cat
        [dir] => /home/tom
        [shell] => /bin/bash
    )

### 参见

-   <span class="methodname">DirectoryIterator::getGroup</span>
-   <span class="methodname">DirectoryIterator::getiNode</span>
-   <span class="methodname">DirectoryIterator::getPerms</span>
-   <span class="function">posix\_getpwuid</span>

DirectoryIterator::getPath
==========================

Get path of current Iterator item without filename

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::getPath</span> ( <span
class="methodparam">void</span> )

Get the path to the current <span
class="classname">DirectoryIterator</span> item.

### 参数

此函数没有参数。

### 返回值

Returns the path to the file, omitting the file name and any trailing
slash.

### 范例

**示例 \#1 <span class="function">DirectoryIterator::getPath</span>
example**

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
echo $iterator->getPath();
?>
```

以上例程的输出类似于：

    /home/examples/public_html

### 参见

-   <span class="methodname">DirectoryIterator::getBasename</span>
-   <span class="methodname">DirectoryIterator::getFilename</span>
-   <span class="methodname">DirectoryIterator::getPathname</span>
-   <span class="function">pathinfo</span>

DirectoryIterator::getPathname
==============================

Return path and file name of current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::getPathname</span> ( <span
class="methodparam">void</span> )

Get the path and file name of the current file.

### 参数

此函数没有参数。

### 返回值

Returns the path and file name of current file. Directories do not have
a trailing slash.

### 范例

**示例 \#1 <span class="function">DirectoryIterator::getPathname</span>
example**

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    echo $fileinfo->getPathname() . "\n";
}
?>
```

以上例程的输出类似于：

    /home/examples/.
    /home/examples/..
    /home/examples/apple.jpg
    /home/examples/banana.jpg
    /home/examples/getpathname.php
    /home/examples/pear.jpg

### 参见

-   <span class="methodname">DirectoryIterator::getBasename</span>
-   <span class="methodname">DirectoryIterator::getFilename</span>
-   <span class="methodname">DirectoryIterator::getPath</span>
-   <span class="function">pathinfo</span>

DirectoryIterator::getPerms
===========================

Get the permissions of current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getPerms</span> ( <span
class="methodparam">void</span> )

Get the permissions of the current <span
class="classname">DirectoryIterator</span> item.

### 参数

此函数没有参数。

### 返回值

Returns the permissions of the file, as a decimal <span
class="type">integer</span>.

### 范例

**示例 \#1 <span class="function">DirectoryIterator::getPerms</span>
example**

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if (!$fileinfo->isDot()) {
        $octal_perms = substr(sprintf('%o', $fileinfo->getPerms()), -4);
        echo $fileinfo->getFilename() . " " . $octal_perms . "\n";
    }
}
?>
```

以上例程的输出类似于：

    apple.jpg 0644
    banana.jpg 0644
    index.php 0744
    pear.jpg 0644

### 参见

-   <span class="methodname">DirectoryIterator::isExecutable</span>
-   <span class="methodname">DirectoryIterator::isReadable</span>
-   <span class="methodname">DirectoryIterator::isWritable</span>

DirectoryIterator::getSize
==========================

Get size of current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getSize</span> ( <span
class="methodparam">void</span> )

Get the file size for the current <span
class="classname">DirectoryIterator</span> item.

### 参数

此函数没有参数。

### 返回值

Returns the size of the file, in bytes.

### 范例

**示例 \#1 <span class="function">DirectoryIterator::getSize</span>
example**

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isFile()) {
        echo $fileinfo->getFilename() . " " . $fileinfo->getSize() . "\n";
    }
}
?>
```

以上例程的输出类似于：

    apple.jpg 15385
    banana.jpg 15190
    example.php 170
    pear.jpg 34406

### 参见

-   <span class="function">filesize</span>

DirectoryIterator::getType
==========================

Determine the type of the current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::getType</span> ( <span
class="methodparam">void</span> )

Determines which file type the current <span
class="classname">DirectoryIterator</span> item belongs to. One of
*file*, *link*, or *dir*.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="type">string</span> representing the type of the
file. May be one of *file*, *link*, or *dir*.

### 范例

**示例 \#1 <span class="function">DirectoryIterator::getType</span>
example**

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    echo $fileinfo->getFilename() . " " . $fileinfo->getType() . "\n";
}
?>
```

以上例程的输出类似于：

    . dir
    .. dir
    apple.jpg file
    banana.jpg file
    example.php file
    pear.jpg file

### 参见

-   <span class="methodname">DirectoryIterator::isDir</span>
-   <span class="methodname">DirectoryIterator::isDot</span>
-   <span class="methodname">DirectoryIterator::isFile</span>
-   <span class="methodname">DirectoryIterator::isLink</span>

DirectoryIterator::isDir
========================

Determine if current DirectoryIterator item is a directory

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isDir</span> ( <span
class="methodparam">void</span> )

Determines if the current <span
class="classname">DirectoryIterator</span> item is a directory.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if it is a directory, otherwise **`FALSE`**

### 范例

**示例 \#1 <span class="function">DirectoryIterator::isDir</span>
example**

This example lists the directories within the directory of the current
script.

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isDir()) {
        echo $fileinfo->getFilename() . "\n";
    }
}
?>
```

以上例程的输出类似于：

    .
    ..
    apples
    bananas
    pears

### 参见

-   <span class="methodname">DirectoryIterator::getType</span>
-   <span class="methodname">DirectoryIterator::isDot</span>
-   <span class="methodname">DirectoryIterator::isFile</span>
-   <span class="methodname">DirectoryIterator::isLink</span>

DirectoryIterator::isDot
========================

Determine if current DirectoryIterator item is '.' or '..'

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isDot</span> ( <span
class="methodparam">void</span> )

Determines if the current <span
class="classname">DirectoryIterator</span> item is a directory and
either *.* or *..*

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the entry is *.* or *..*, otherwise **`FALSE`**

### 范例

**示例 \#1 A <span class="methodname">DirectoryIterator::isDot</span>
example**

This example will list all files, omitting the *.* and *..* entries.

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if (!$fileinfo->isDot()) {
        echo $fileinfo->getFilename() . "\n";
    }
}
?>
```

以上例程的输出类似于：

    apple.jpg
    banana.jpg
    example.php
    pears.jpg

### 参见

-   <span class="methodname">DirectoryIterator::getType</span>
-   <span class="methodname">DirectoryIterator::isDir</span>
-   <span class="methodname">DirectoryIterator::isFile</span>
-   <span class="methodname">DirectoryIterator::isLink</span>

DirectoryIterator::isExecutable
===============================

Determine if current DirectoryIterator item is executable

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isExecutable</span> ( <span
class="methodparam">void</span> )

Determines if the current <span
class="classname">DirectoryIterator</span> item is executable.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the entry is executable, otherwise **`FALSE`**

### 范例

**示例 \#1 <span class="function">DirectoryIterator::isExecutable</span>
example**

This example lists files in the directory containing the script which
are executable.

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isExecutable()) {
        echo $fileinfo->getFilename() . "\n";
    }
}
?>
```

以上例程的输出类似于：

    example.php
    myscript.sh

### 参见

-   <span class="methodname">DirectoryIterator::isReadable</span>
-   <span class="methodname">DirectoryIterator::isWritable</span>
-   <span class="methodname">DirectoryIterator::getPerms</span>

DirectoryIterator::isFile
=========================

Determine if current DirectoryIterator item is a regular file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isFile</span> ( <span
class="methodparam">void</span> )

Determines if the current <span
class="classname">DirectoryIterator</span> item is a regular file.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the file exists and is a regular file (not a
*link* or *dir*), otherwise **`FALSE`**

### 范例

**示例 \#1 <span class="methodname">DirectoryIterator::isFile</span>
example**

This example will list all regular files in the directory containing the
script.

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isFile()) {
        echo $fileinfo->getFilename() . "\n";
    }
}
?>
```

以上例程的输出类似于：

    apple.jpg
    banana.jpg
    example.php
    pears.jpg

### 参见

-   <span class="methodname">DirectoryIterator::getType</span>
-   <span class="methodname">DirectoryIterator::isDir</span>
-   <span class="methodname">DirectoryIterator::isDot</span>
-   <span class="methodname">DirectoryIterator::isLink</span>

DirectoryIterator::isLink
=========================

Determine if current DirectoryIterator item is a symbolic link

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isLink</span> ( <span
class="methodparam">void</span> )

Determines if the current <span
class="classname">DirectoryIterator</span> item is a symbolic link.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the item is a symbolic link, otherwise **`FALSE`**

### 范例

**示例 \#1 A <span class="methodname">DirectoryIterator::isLink</span>
example**

This example contains a recursive function for removing a directory
tree.

``` php
<?php
/**
 * This function will recursively delete all files in the given path, without
 * following symlinks.
 * 
 * @param string $path Path to the directory to remove.
 */
function removeDir($path) {
    $dir = new DirectoryIterator($path);
    foreach ($dir as $fileinfo) {
        if ($fileinfo->isFile() || $fileinfo->isLink()) {
            unlink($fileinfo->getPathName());
        } elseif (!$fileinfo->isDot() && $fileinfo->isDir()) {
            removeDir($fileinfo->getPathName());
        }
    }
    rmdir($path);
}

removeDir('foo');
?>
```

### 参见

-   <span class="methodname">DirectoryIterator::getType</span>
-   <span class="methodname">DirectoryIterator::isDir</span>
-   <span class="methodname">DirectoryIterator::isDot</span>
-   <span class="methodname">DirectoryIterator::isFile</span>

DirectoryIterator::isReadable
=============================

Determine if current DirectoryIterator item can be read

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isReadable</span> ( <span
class="methodparam">void</span> )

Determines if the current <span
class="classname">DirectoryIterator</span> item is readable.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the file is readable, otherwise **`FALSE`**

### 范例

**示例 \#1 <span class="methodname">DirectoryIterator::isReadable</span>
example**

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isReadable()) {
        echo $fileinfo->getFilename() . "\n";
    }
}
?>
```

以上例程的输出类似于：

    apple.jpg
    banana.jpg
    example.php
    pears.jpg

### 参见

-   <span class="methodname">DirectoryIterator::isExecutable</span>
-   <span class="methodname">DirectoryIterator::isWritable</span>
-   <span class="methodname">DirectoryIterator::getPerms</span>

DirectoryIterator::isWritable
=============================

Determine if current DirectoryIterator item can be written to

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isWritable</span> ( <span
class="methodparam">void</span> )

Determines if the current <span
class="classname">DirectoryIterator</span> item is writable.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the file/directory is writable, otherwise
**`FALSE`**

### 范例

**示例 \#1 <span class="methodname">DirectoryIterator::isWritable</span>
example**

This example lists the files and directories which can be opened for
writing in the directory containing the script.

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isWritable()) {
        echo $fileinfo->getFilename() . "\n";
    }
}
?>
```

以上例程的输出类似于：

    apples.txt
    bananas.html
    pears

### 参见

-   <span class="methodname">DirectoryIterator::getPerms</span>
-   <span class="methodname">DirectoryIterator::isExecutable</span>
-   <span class="methodname">DirectoryIterator::isReadable</span>

DirectoryIterator::key
======================

Return the key for the current DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::key</span> ( <span
class="methodparam">void</span> )

Get the key for the current <span
class="classname">DirectoryIterator</span> item.

### 参数

此函数没有参数。

### 返回值

The key for the current <span class="classname">DirectoryIterator</span>
item.

### 范例

**示例 \#1 A <span class="methodname">DirectoryIterator::key</span>
example**

``` php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    if (!$fileinfo->isDot()) {
        echo $fileinfo->key() . " => " . $fileinfo->getFilename() . "\n";
    }
}
?>
```

以上例程的输出类似于：

    0 => apple.jpg
    1 => banana.jpg
    2 => index.php
    3 => pear.jpg

### 参见

-   <span class="methodname">DirectoryIterator::current</span>
-   <span class="methodname">DirectoryIterator::next</span>
-   <span class="methodname">DirectoryIterator::rewind</span>
-   <span class="methodname">DirectoryIterator::valid</span>
-   <span class="methodname">Iterator::key</span>

DirectoryIterator::next
=======================

Move forward to next DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DirectoryIterator::next</span> ( <span
class="methodparam">void</span> )

Move forward to the next <span
class="classname">DirectoryIterator</span> item.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">DirectoryIterator::next</span>
example**

List the contents of a directory using a while loop.

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
while($iterator->valid()) {
    echo $iterator->getFilename() . "\n";
    $iterator->next();
}
?>
```

以上例程的输出类似于：

    .
    ..
    apple.jpg
    banana.jpg
    index.php
    pear.jpg

### 参见

-   <span class="methodname">DirectoryIterator::current</span>
-   <span class="methodname">DirectoryIterator::key</span>
-   <span class="methodname">DirectoryIterator::rewind</span>
-   <span class="methodname">DirectoryIterator::valid</span>
-   <span class="methodname">Iterator::next</span>

DirectoryIterator::rewind
=========================

Rewind the DirectoryIterator back to the start

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DirectoryIterator::rewind</span> ( <span
class="methodparam">void</span> )

Rewind the <span class="classname">DirectoryIterator</span> back to the
start.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">DirectoryIterator::rewind</span>
example**

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));

$iterator->next();
echo $iterator->key(); //1

$iterator->rewind(); //rewinding to the beginning
echo $iterator->key(); //0
?>
```

### 参见

-   <span class="methodname">DirectoryIterator::current</span>
-   <span class="methodname">DirectoryIterator::key</span>
-   <span class="methodname">DirectoryIterator::next</span>
-   <span class="methodname">DirectoryIterator::valid</span>
-   <span class="methodname">Iterator::rewind</span>

DirectoryIterator::seek
=======================

Seek to a DirectoryIterator item

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DirectoryIterator::seek</span> ( <span
class="methodparam"><span class="type">int</span> `$position`</span> )

Seek to a given position in the <span
class="classname">DirectoryIterator</span>.

### 参数

`position`  
The zero-based numeric position to seek to.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">DirectoryIterator::seek</span>
example**

Seek to the fourth item in the directory containing the script. The
first two are usually *.* and *..*

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
$iterator->seek(3);
if ($iterator->valid()) {
    echo $iterator->getFilename();
} else {
    echo 'No file at position 3';
}
?>
```

### 参见

-   <span class="methodname">DirectoryIterator::rewind</span>
-   <span class="methodname">DirectoryIterator::next</span>
-   <span class="methodname">SeekableIterator::seek</span>

DirectoryIterator::\_\_toString
===============================

Get file name as a string

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::\_\_toString</span> ( <span
class="methodparam">void</span> )

Get the file name of the current <span
class="classname">DirectoryIterator</span> item.

### 参数

此函数没有参数。

### 返回值

Returns the file name of the current <span
class="classname">DirectoryIterator</span> item.

### 范例

**示例 \#1 A <span
class="methodname">DirectoryIterator::\_\_toString</span> example**

This example will list the contents of the directory containing the
script.

``` php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    echo $fileinfo;
}
?>
```

以上例程的输出类似于：

    .
    ..
    apple.jpg
    banana.jpg
    index.php
    pear.jpg

### 参见

-   <span class="methodname">DirectoryIterator::getFilename</span>
-   The
    <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>
    magic method

DirectoryIterator::valid
========================

Check whether current DirectoryIterator position is a valid file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::valid</span> ( <span
class="methodparam">void</span> )

Check whether current <span class="classname">DirectoryIterator</span>
position is a valid file.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the position is valid, otherwise **`FALSE`**

### 范例

**示例 \#1 A <span class="methodname">DirectoryIterator::valid</span>
example**

``` php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));

// Loop to end of iterator
while($iterator->valid()) {
    $iterator->next();
}

$iterator->valid(); // FALSE
$iterator->rewind(); 
$iterator->valid(); // TRUE

?>
```

### 参见

-   <span class="methodname">DirectoryIterator::current</span>
-   <span class="methodname">DirectoryIterator::key</span>
-   <span class="methodname">DirectoryIterator::next</span>
-   <span class="methodname">DirectoryIterator::rewind</span>
-   <span class="methodname">Iterator::valid</span>

简介
----

The EmptyIterator class for an empty iterator.

类摘要
------

**EmptyIterator**

<span class="ooclass"> class **EmptyIterator** </span> <span
class="oointerface">implements <span
class="interfacename">Iterator</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">scalar</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

EmptyIterator::current
======================

The current() method

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">EmptyIterator::current</span> ( <span
class="methodparam">void</span> )

This function must not be called. It throws an exception upon access.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 错误／异常

Throws an <span class="classname">Exception</span> if called.

### 返回值

没有返回值。

EmptyIterator::key
==================

The key() method

### 说明

<span class="modifier">public</span> <span class="type">scalar</span>
<span class="methodname">EmptyIterator::key</span> ( <span
class="methodparam">void</span> )

This function must not be called. It throws an exception upon access.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 错误／异常

Throws an <span class="classname">Exception</span> if called.

### 返回值

没有返回值。

EmptyIterator::next
===================

The next() method

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EmptyIterator::next</span> ( <span
class="methodparam">void</span> )

No operation, nothing to do.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

EmptyIterator::rewind
=====================

The rewind() method

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EmptyIterator::rewind</span> ( <span
class="methodparam">void</span> )

No operation, nothing to do.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

EmptyIterator::valid
====================

The valid() method

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EmptyIterator::valid</span> ( <span
class="methodparam">void</span> )

The EmptyIterator valid() method.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

**`FALSE`**

简介
----

The Filesystem iterator

类摘要
------

**FilesystemIterator**

<span class="ooclass"> class **FilesystemIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**DirectoryIterator** </span> <span class="oointerface">implements <span
class="interfacename">SeekableIterator</span> </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::CURRENT_AS_PATHNAME` <span class="initializer"> =
32</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::CURRENT_AS_FILEINFO` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::CURRENT_AS_SELF` <span class="initializer"> =
16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::CURRENT_MODE_MASK` <span class="initializer"> =
240</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::KEY_AS_PATHNAME` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::KEY_AS_FILENAME` <span class="initializer"> =
256</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::FOLLOW_SYMLINKS` <span class="initializer"> =
512</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::KEY_MODE_MASK` <span class="initializer"> =
3840</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::NEW_CURRENT_AND_KEY` <span class="initializer"> =
256</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::SKIP_DOTS` <span class="initializer"> = 4096</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::UNIX_PATHS` <span class="initializer"> =
8192</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = FilesystemIterator::KEY\_AS\_PATHNAME \|
FilesystemIterator::CURRENT\_AS\_FILEINFO \|
FilesystemIterator::SKIP\_DOTS</span></span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setFlags</span> (\[ <span
class="methodparam"><span class="type">int</span> `$flags`</span> \] )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="type">DirectoryIterator</span> <span
class="methodname">DirectoryIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getATime</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::getBasename</span> (\[ <span
class="methodparam"> <span class="type">string</span> `$suffix` </span>
\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getCTime</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::getExtension</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::getFilename</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getGroup</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getInode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getMTime</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getOwner</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::getPath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::getPathname</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getPerms</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DirectoryIterator::getSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isDir</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isDot</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isExecutable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isLink</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isReadable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::isWritable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DirectoryIterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DirectoryIterator::rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DirectoryIterator::seek</span> ( <span
class="methodparam"><span class="type">int</span> `$position`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DirectoryIterator::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DirectoryIterator::valid</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`FilesystemIterator::CURRENT_AS_PATHNAME`**  
Makes <span class="methodname">FilesystemIterator::current</span> return
the pathname.

**`FilesystemIterator::CURRENT_AS_FILEINFO`**  
Makes <span class="methodname">FilesystemIterator::current</span> return
an <span class="classname">SplFileInfo</span> instance.

**`FilesystemIterator::CURRENT_AS_SELF`**  
Makes <span class="methodname">FilesystemIterator::current</span> return
$this (the FilesystemIterator).

**`FilesystemIterator::CURRENT_MODE_MASK`**  
Masks <span class="methodname">FilesystemIterator::current</span>

**`FilesystemIterator::KEY_AS_PATHNAME`**  
Makes <span class="methodname">FilesystemIterator::key</span> return the
pathname.

**`FilesystemIterator::KEY_AS_FILENAME`**  
Makes <span class="methodname">FilesystemIterator::key</span> return the
filename.

**`FilesystemIterator::FOLLOW_SYMLINKS`**  
Makes <span
class="methodname">RecursiveDirectoryIterator::hasChildren</span> follow
symlinks.

**`FilesystemIterator::KEY_MODE_MASK`**  
Masks <span class="methodname">FilesystemIterator::key</span>

**`FilesystemIterator::NEW_CURRENT_AND_KEY`**  
Same as *FilesystemIterator::KEY\_AS\_FILENAME \|
FilesystemIterator::CURRENT\_AS\_FILEINFO*.

**`FilesystemIterator::SKIP_DOTS`**  
Skips dot files (*.* and *..*).

**`FilesystemIterator::UNIX_PATHS`**  
Makes paths use Unix-style forward slash irrespective of system default.
Note that the `path` that is passed to the constructor is not modified.

更新日志
--------

| 版本  | 说明                                            |
|-------|-------------------------------------------------|
| 5.3.1 | Added **`FilesystemIterator::FOLLOW_SYMLINKS`** |

FilesystemIterator::\_\_construct
=================================

Constructs a new filesystem iterator

### 说明

<span class="modifier">public</span> <span
class="methodname">FilesystemIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = FilesystemIterator::KEY\_AS\_PATHNAME \|
FilesystemIterator::CURRENT\_AS\_FILEINFO \|
FilesystemIterator::SKIP\_DOTS</span></span> \] )

Constructs a new filesystem iterator from the `path`.

### 参数

`path`  
The path of the filesystem item to be iterated over.

`flags`  
Flags may be provided which will affect the behavior of some methods. A
list of the flags can found under
<a href="/spl/iterators.html#预定义常量" class="link">FilesystemIterator predefined constants</a>.
They can also be set later with <span
class="methodname">FilesystemIterator::setFlags</span>

### 返回值

没有返回值。

### 错误／异常

Throws an <span class="classname">UnexpectedValueException</span> if the
`path` cannot be found.

### 范例

**示例 \#1 <span
class="function">FilesystemIterator::\_\_construct</span> example**

``` php
<?php
$it = new FilesystemIterator(dirname(__FILE__));
foreach ($it as $fileinfo) {
    echo $fileinfo->getFilename() . "\n";
}
?>
```

以上例程会输出：

    apples.jpg
    banana.jpg
    example.php

### 参见

-   <span class="methodname">FilesystemIterator::setFlags</span>
-   <span class="methodname">DirectoryIterator::\_\_construct</span>

FilesystemIterator::current
===========================

The current file

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">FilesystemIterator::current</span> ( <span
class="methodparam">void</span> )

Get file information of the current element.

### 参数

此函数没有参数。

### 返回值

The filename, file information, or $this depending on the set flags. See
the
<a href="/spl/iterators.html#预定义常量" class="link">FilesystemIterator constants</a>.

### 范例

**示例 \#1 <span class="methodname">FilesystemIterator::current</span>
example**

This example will list the contents of the directory containing the
script.

``` php
<?php
$iterator = new FilesystemIterator(__DIR__, FilesystemIterator::CURRENT_AS_PATHNAME);
foreach ($iterator as $fileinfo) {
    echo $iterator->current() . "\n";
}
?>
```

以上例程的输出类似于：

    /www/examples/apple.jpg
    /www/examples/banana.jpg
    /www/examples/example.php

### 参见

-   <a href="/spl/iterators.html#预定义常量" class="link">FilesystemIterator constants</a>
-   <span class="methodname">DirectoryIterator::current</span>
-   <span class="methodname">DirectoryIterator::getFileName</span>

FilesystemIterator::getFlags
============================

Get the handling flags

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">FilesystemIterator::getFlags</span> ( <span
class="methodparam">void</span> )

Gets the handling flags, as set in <span
class="methodname">FilesystemIterator::\_\_construct</span> or <span
class="methodname">FilesystemIterator::setFlags</span>.

### 参数

此函数没有参数。

### 返回值

The integer value of the set flags.

### 参见

-   <span class="methodname">FilesystemIterator::\_\_construct</span>
-   <span class="methodname">FilesystemIterator::setFlags</span>

FilesystemIterator::key
=======================

Retrieve the key for the current file

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">FilesystemIterator::key</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the pathname or filename depending on the set flags. See the
<a href="/spl/iterators.html#预定义常量" class="link">FilesystemIterator constants</a>.

### 范例

**示例 \#1 <span class="methodname">FilesystemIterator::key</span>
example**

This example will list the contents of the directory containing the
script.

``` php
<?php
$iterator = new FilesystemIterator(dirname(__FILE__), FilesystemIterator::KEY_AS_FILENAME);
foreach ($iterator as $fileinfo) {
    echo $iterator->key() . "\n";
}
?>
```

以上例程的输出类似于：

    apple.jpg
    banana.jpg
    example.php

### 参见

-   <a href="/spl/iterators.html#预定义常量" class="link">FilesystemIterator constants</a>
-   <span class="methodname">DirectoryIterator::key</span>
-   <span class="methodname">DirectoryIterator::getFilename</span>
-   <span class="methodname">DirectoryIterator::getPathname</span>

FilesystemIterator::next
========================

Move to the next file

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilesystemIterator::next</span> ( <span
class="methodparam">void</span> )

Move to the next file.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">FilesystemIterator::next</span>
example**

List the contents of a directory using a while loop.

``` php
<?php
$iterator = new FilesystemIterator(dirname(__FILE__));
while($iterator->valid()) {
    echo $iterator->getFilename() . "\n";
    $iterator->next();
}
?>
```

以上例程的输出类似于：

    apple.jpg
    banana.jpg
    example.php

### 参见

-   <span class="methodname">DirectoryIterator::next</span>

FilesystemIterator::rewind
==========================

Rewinds back to the beginning

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilesystemIterator::rewind</span> ( <span
class="methodparam">void</span> )

Rewinds the directory back to the start.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">FilesystemIterator::rewind</span>
example**

``` php
<?php
$iterator = new FilesystemIterator(dirname(__FILE__), FilesystemIterator::KEY_AS_FILENAME);

echo $iterator->key() . "\n";

$iterator->next();
echo $iterator->key() . "\n";

$iterator->rewind();
echo $iterator->key() . "\n";
?>
```

以上例程的输出类似于：

    apple.jpg
    banana.jpg
    apple.jpg

### 参见

-   <span class="methodname">DirectoryIterator::rewind</span>

FilesystemIterator::setFlags
============================

Sets handling flags

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilesystemIterator::setFlags</span> (\[ <span
class="methodparam"><span class="type">int</span> `$flags`</span> \] )

Sets handling flags.

### 参数

`flags`  
The handling flags to set. See the
<a href="/spl/iterators.html#预定义常量" class="link">FilesystemIterator constants</a>.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">FilesystemIterator::key</span>
example**

This example demonstrates the difference between the
<a href="/spl/iterators.html#" class="link">FilesystemIterator::KEY_AS_PATHNAME</a>
and
<a href="/spl/iterators.html#" class="link">FilesystemIterator::KEY_AS_FILENAME</a>
flags.

``` php
<?php
$iterator = new FilesystemIterator(dirname(__FILE__), FilesystemIterator::KEY_AS_PATHNAME);
echo "Key as Pathname:\n";
foreach ($iterator as $key => $fileinfo) {
    echo $key . "\n";
}

$iterator->setFlags(FilesystemIterator::KEY_AS_FILENAME);
echo "\nKey as Filename:\n";
foreach ($iterator as $key => $fileinfo) {
    echo $key . "\n";
}
?>
```

以上例程的输出类似于：

    Key as Pathname:
    /www/examples/apple.jpg
    /www/examples/banana.jpg
    /www/examples/example.php

    Key as Filename:
    apple.jpg
    banana.jpg
    example.php

### 参见

-   <span class="methodname">FilesystemIterator::\_\_construct</span>
-   <span class="methodname">FilesystemIterator::getFlags</span>

简介
----

这个抽象类的遍历并过滤出不想要的值.这个类应该被实现了迭代过滤器的类继承
<span
class="methodname">FilterIterator::accept</span>方法必须被子类实现.

类摘要
------

**FilterIterator**

<span class="ooclass"> <span class="modifier">abstract</span> class
**FilterIterator** </span> <span class="ooclass"> <span
class="modifier">extends</span> **IteratorIterator** </span> <span
class="oointerface">implements <span
class="interfacename">OuterIterator</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">abstract</span> <span class="type">bool</span> <span
class="methodname">accept</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">getInnerIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

FilterIterator::accept
======================

Check whether the current element of the iterator is acceptable

### 说明

<span class="modifier">public</span> <span
class="modifier">abstract</span> <span class="type">bool</span> <span
class="methodname">FilterIterator::accept</span> ( <span
class="methodparam">void</span> )

Returns whether the current element of the iterator is acceptable
through this filter.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the current element is acceptable, otherwise **`FALSE`**.

### 范例

**示例 \#1 <span class="function">FilterIterator::accept</span>
example**

``` php
<?php
// This iterator filters all values with less than 10 characters
class LengthFilterIterator extends FilterIterator {

    public function accept() {
        // Only accept strings with a length of 10 and greater
        return strlen(parent::current()) >= 10;
    }

}

$arrayIterator = new ArrayIterator(array('test1', 'more than 10 characters'));
$lengthFilter = new LengthFilterIterator($arrayIterator);

foreach ($lengthFilter as $value) {
    echo $value . "\n";
}
?>
```

以上例程会输出：

    more than 10 characters

FilterIterator::\_\_construct
=============================

Construct a filterIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">FilterIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

Constructs a new <span class="classname">FilterIterator</span>, which
consists of a passed in `iterator` with filters applied to it.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`iterator`  
The iterator that is being filtered.

### 返回值

The <span class="classname">FilterIterator</span>.

### 参见

-   <span class="methodname">LimitIterator::\_\_construct</span>

FilterIterator::current
=======================

Get the current element value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">FilterIterator::current</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Get the current element value.

### 参数

此函数没有参数。

### 返回值

The current element value.

### 参见

-   <span class="function">FilterIterator::key</span>
-   <span class="function">FilterIterator::next</span>

FilterIterator::getInnerIterator
================================

Get the inner iterator

### 说明

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">FilterIterator::getInnerIterator</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Get the inner iterator.

### 参数

此函数没有参数。

### 返回值

The inner iterator.

FilterIterator::key
===================

Get the current key

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">FilterIterator::key</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Get the current key.

### 参数

此函数没有参数。

### 返回值

The current key.

### 参见

-   <span class="function">FilterIterator::next</span>
-   <span class="function">FilterIterator::current</span>

FilterIterator::next
====================

Move the iterator forward

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilterIterator::next</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Move the iterator forward.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="function">FilterIterator::current</span>
-   <span class="function">FilterIterator::key</span>

FilterIterator::rewind
======================

Rewind the iterator

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilterIterator::rewind</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Rewind the iterator.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="function">FilterIterator::current</span>
-   <span class="function">FilterIterator::key</span>
-   <span class="function">FilterIterator::next</span>

FilterIterator::valid
=====================

Check whether the current element is valid

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">FilterIterator::valid</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Checks whether the current element is valid.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the current element is valid, otherwise **`FALSE`**

简介
----

遍历一个文件系统行为类似于 <span class="function">glob</span>.

类摘要
------

**GlobIterator**

<span class="ooclass"> class **GlobIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**FilesystemIterator** </span> <span class="oointerface">implements
<span class="interfacename">SeekableIterator</span> </span> <span
class="oointerface">, <span class="interfacename">Countable</span>
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> =
FilesystemIterator::KEY\_AS\_PATHNAME \|
FilesystemIterator::CURRENT\_AS\_FILEINFO</span></span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">FilesystemIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = FilesystemIterator::KEY\_AS\_PATHNAME \|
FilesystemIterator::CURRENT\_AS\_FILEINFO \|
FilesystemIterator::SKIP\_DOTS</span></span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">FilesystemIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">FilesystemIterator::getFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">FilesystemIterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilesystemIterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilesystemIterator::rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilesystemIterator::setFlags</span> (\[ <span
class="methodparam"><span class="type">int</span> `$flags`</span> \] )

}

GlobIterator::\_\_construct
===========================

Construct a directory using glob

### 说明

<span class="modifier">public</span> <span
class="methodname">GlobIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> =
FilesystemIterator::KEY\_AS\_PATHNAME \|
FilesystemIterator::CURRENT\_AS\_FILEINFO</span></span> \] )

Constructs a new directory iterator from a glob expression.

### 参数

`pattern`  
A <span class="function">glob</span> pattern.

`flags`  
Option flags, the flags may be a bitmask of the <span
class="classname">FilesystemIterator</span> constants.

### 范例

**示例 \#1 <span class="classname">GlobIterator</span> example**

``` php
<?php
$iterator = new GlobIterator('*.dll', FilesystemIterator::KEY_AS_FILENAME);

if (!$iterator->count()) {
    echo 'No matches';
} else {
    $n = 0;

    printf("Matched %d item(s)\r\n", $iterator->count());

    foreach ($iterator as $item) {
        printf("[%d] %s\r\n", ++$n, $iterator->key());
    }
}
?>
```

以上例程的输出类似于：

    Matched 2 item(s)
    [1] php5ts.dll
    [2] php_gd2.dll

### 参见

-   <span class="methodname">DirectoryIterator::\_\_construct</span>
-   <span class="methodname">GlobIterator::count</span>
-   <span class="function">glob</span>

GlobIterator::count
===================

Get the number of directories and files

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GlobIterator::count</span> ( <span
class="methodparam">void</span> )

Gets the number of directories and files found by the glob expression.

### 参数

此函数没有参数。

### 返回值

The number of returned directories and files, as an <span
class="type">integer</span>.

### 范例

**示例 \#1 <span class="methodname">GlobIterator::count</span> example**

``` php
<?php
$iterator = new GlobIterator('*.xml');

printf("Matched %d item(s)\r\n", $iterator->count());
?>
```

以上例程的输出类似于：

    Matched 8 item(s)

### 参见

-   <span class="methodname">GlobIterator::\_\_construct</span>
-   <span class="function">count</span>
-   <span class="function">glob</span>

简介
----

The <span class="classname">InfiniteIterator</span> allows one to
infinitely iterate over an iterator without having to manually rewind
the iterator upon reaching its end.

类摘要
------

**InfiniteIterator**

<span class="ooclass"> class **InfiniteIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**IteratorIterator** </span> <span class="oointerface">implements <span
class="interfacename">OuterIterator</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">IteratorIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Traversable</span>
`$iterator`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">IteratorIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Traversable</span> <span
class="methodname">IteratorIterator::getInnerIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">IteratorIterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">IteratorIterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">IteratorIterator::rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IteratorIterator::valid</span> ( <span
class="methodparam">void</span> )

}

InfiniteIterator::\_\_construct
===============================

Constructs an InfiniteIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">InfiniteIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

Constructs an <span class="classname">InfiniteIterator</span> from an
<span class="classname">Iterator</span>.

### 参数

`iterator`  
The iterator to infinitely iterate over.

### 返回值

没有返回值。

### 错误／异常

Throws an **`E_RECOVERABLE_ERROR`** if the `iterator` parameter is not
an <span class="classname">Iterator</span>.

### 范例

**示例 \#1 <span class="function">InfiniteIterator::\_\_construct</span>
example**

``` php
<?php
$arrayit  = new ArrayIterator(array('cat','dog'));
$infinite = new InfiniteIterator($arrayit);
$limit    = new LimitIterator($infinite, 0, 7);
foreach($limit as $value)
{
    echo "$value\n";
}
?>
```

以上例程会输出：

    cat
    dog
    cat
    dog
    cat
    dog
    cat

### 参见

-   <span class="methodname">InfiniteIterator::next</span>

InfiniteIterator::next
======================

Moves the inner Iterator forward or rewinds it

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">InfiniteIterator::next</span> ( <span
class="methodparam">void</span> )

Moves the inner <span class="classname">Iterator</span> forward to its
next element if there is one, otherwise rewinds the inner <span
class="classname">Iterator</span> back to the beginning.

> **Note**:
>
> Even an <span class="classname">InfiniteIterator</span> stops if its
> inner <span class="classname">Iterator</span> is empty.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">InfiniteIterator::\_\_construct</span>

简介
----

This iterator wrapper allows the conversion of anything that is
<a href="/class/traversable.html" class="link">Traversable</a> into an
Iterator. It is important to understand that most classes that do not
implement Iterators have reasons as most likely they do not allow the
full Iterator feature set. If so, techniques should be provided to
prevent misuse, otherwise expect exceptions or fatal errors.

类摘要
------

**IteratorIterator**

<span class="ooclass"> class **IteratorIterator** </span> <span
class="oointerface">implements <span
class="interfacename">OuterIterator</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">Traversable</span>
`$iterator`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Traversable</span> <span
class="methodname">getInnerIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

注释
----

> **Note**:
>
> This class permits access to methods of the inner iterator via the
> \_\_call magic method.

IteratorIterator::\_\_construct
===============================

Create an iterator from anything that is traversable

### 说明

<span class="modifier">public</span> <span
class="methodname">IteratorIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Traversable</span>
`$iterator`</span> )

Creates an iterator from anything that is traversable.

### 参数

`iterator`  
The traversable iterator.

### 返回值

没有返回值。

### 参见

-   <span class="classname">Traversable</span>

IteratorIterator::current
=========================

Get the current value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">IteratorIterator::current</span> ( <span
class="methodparam">void</span> )

Get the value of the current element.

### 参数

此函数没有参数。

### 返回值

The value of the current element.

### 参见

-   <span class="methodname">IteratorIterator::key</span>

IteratorIterator::getInnerIterator
==================================

Get the inner iterator

### 说明

<span class="modifier">public</span> <span
class="type">Traversable</span> <span
class="methodname">IteratorIterator::getInnerIterator</span> ( <span
class="methodparam">void</span> )

Get the inner iterator.

### 参数

此函数没有参数。

### 返回值

The inner iterator as passed to <span
class="methodname">IteratorIterator::\_\_construct</span>.

### 参见

-   <span class="classname">Iterator</span>
-   <span class="classname">OuterIterator</span>

IteratorIterator::key
=====================

Get the key of the current element

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">IteratorIterator::key</span> ( <span
class="methodparam">void</span> )

Get the key of the current element.

### 参数

此函数没有参数。

### 返回值

The key of the current element.

### 参见

-   <span class="methodname">IteratorIterator::current</span>

IteratorIterator::next
======================

Forward to the next element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">IteratorIterator::next</span> ( <span
class="methodparam">void</span> )

Forward to the next element.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">IteratorIterator::rewind</span>
-   <span class="methodname">IteratorIterator::valid</span>

IteratorIterator::rewind
========================

Rewind to the first element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">IteratorIterator::rewind</span> ( <span
class="methodparam">void</span> )

Rewinds to the first element.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">IteratorIterator::next</span>
-   <span class="methodname">IteratorIterator::valid</span>

IteratorIterator::valid
=======================

Checks if the iterator is valid

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IteratorIterator::valid</span> ( <span
class="methodparam">void</span> )

Checks if the iterator is valid.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the iterator is valid, otherwise **`FALSE`**

### 参见

-   <span class="function">iterator\_count</span>
-   <span class="methodname">IteratorIterator::current</span>

简介
----

<span class="classname">LimitIterator</span>类允许遍历一个 <span
class="classname">Iterator</span> 的限定子集的元素.

类摘要
------

**LimitIterator**

<span class="ooclass"> class **LimitIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**IteratorIterator** </span> <span class="oointerface">implements <span
class="interfacename">OuterIterator</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$count`<span class="initializer"> =
-1</span></span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">getInnerIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getPosition</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">seek</span> ( <span class="methodparam"><span
class="type">int</span> `$position`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

范例
----

**示例 \#1 <span class="classname">LimitIterator</span> usage example**

``` php
<?php

// Create an iterator to be limited
$fruits = new ArrayIterator(array(
    'apple',
    'banana',
    'cherry',
    'damson',
    'elderberry'
));

// Loop over first three fruits only
foreach (new LimitIterator($fruits, 0, 3) as $fruit) {
    var_dump($fruit);
}

echo "\n";

// Loop from third fruit until the end
// Note: offset starts from zero for apple
foreach (new LimitIterator($fruits, 2) as $fruit) {
    var_dump($fruit);
}

?>
```

以上例程会输出：

    string(5) "apple"
    string(6) "banana"
    string(6) "cherry"

    string(6) "cherry"
    string(6) "damson"
    string(10) "elderberry"

LimitIterator::\_\_construct
============================

Construct a LimitIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">LimitIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$count`<span class="initializer"> =
-1</span></span> \]\] )

Constructs a new <span class="classname">LimitIterator</span> from an
`iterator` with a given starting `offset` and maximum `count`.

### 参数

`iterator`  
The <span class="classname">Iterator</span> to limit.

`offset`  
Optional offset of the limit.

`count`  
Optional count of the limit.

### 返回值

The new <span class="classname">LimitIterator</span>.

### 错误／异常

Throws an <span class="classname">OutOfRangeException</span> if the
`offset` is less than *0* or the `count` is less than *-1*.

### 范例

**示例 \#1 <span class="function">LimitIterator::\_\_construct</span>
example**

``` php
<?php
$ait = new ArrayIterator(array('a', 'b', 'c', 'd', 'e'));
$lit = new LimitIterator($ait, 1, 3);
foreach ($lit as $value) {
    echo $value . "\n";
}
?>
```

以上例程会输出：

    b
    c
    d

### 参见

-   <a href="/spl/iterators.html#范例" class="link">LimitIterator examples</a>

LimitIterator::current
======================

Get current element

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">LimitIterator::current</span> ( <span
class="methodparam">void</span> )

Gets the current element of the inner <span
class="classname">Iterator</span>.

### 参数

此函数没有参数。

### 返回值

Returns the current element or **`NULL`** if there is none.

### 参见

-   <span class="methodname">LimitIterator::key</span>
-   <span class="methodname">LimitIterator::next</span>
-   <span class="methodname">LimitIterator::rewind</span>
-   <span class="methodname">LimitIterator::seek</span>
-   <span class="methodname">LimitIterator::valid</span>

LimitIterator::getInnerIterator
===============================

Get inner iterator

### 说明

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">LimitIterator::getInnerIterator</span> ( <span
class="methodparam">void</span> )

Gets the inner <span class="classname">Iterator</span>.

### 参数

此函数没有参数。

### 返回值

The inner iterator passed to <span
class="methodname">LimitIterator::\_\_construct</span>.

### 参见

-   <span class="methodname">LimitIterator::\_\_construct</span>
-   <span class="methodname">IteratorIterator::getInnerIterator</span>

LimitIterator::getPosition
==========================

Return the current position

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">LimitIterator::getPosition</span> ( <span
class="methodparam">void</span> )

Gets the current zero-based position of the inner <span
class="classname">Iterator</span>.

### 参数

此函数没有参数。

### 返回值

The current position.

### 范例

**示例 \#1 <span class="function">LimitIterator::getPosition</span>
example**

``` php
<?php
$fruits = array(
    'a' => 'apple',
    'b' => 'banana',
    'c' => 'cherry',
    'd' => 'damson',
    'e' => 'elderberry'
);
$array_it = new ArrayIterator($fruits);
$limit_it = new LimitIterator($array_it, 2, 3);
foreach ($limit_it as $item) {
    echo $limit_it->getPosition() . ' ' . $item . "\n";
}
?>
```

以上例程会输出：

    2 cherry
    3 damson
    4 elderberry

### 参见

-   <span class="methodname">FilterIterator::key</span>

LimitIterator::key
==================

Get current key

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">LimitIterator::key</span> ( <span
class="methodparam">void</span> )

Gets the key for the current item in the inner <span
class="classname">Iterator</span>.

### 参数

此函数没有参数。

### 返回值

Returns the key for the current item.

### 参见

-   <span class="methodname">LimitIterator::getPosition</span>
-   <span class="methodname">LimitIterator::current</span>
-   <span class="methodname">LimitIterator::next</span>
-   <span class="methodname">LimitIterator::rewind</span>
-   <span class="methodname">LimitIterator::seek</span>
-   <span class="methodname">LimitIterator::valid</span>

LimitIterator::next
===================

Move the iterator forward

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">LimitIterator::next</span> ( <span
class="methodparam">void</span> )

Moves the iterator forward.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">LimitIterator::current</span>
-   <span class="methodname">LimitIterator::key</span>
-   <span class="methodname">LimitIterator::rewind</span>
-   <span class="methodname">LimitIterator::seek</span>
-   <span class="methodname">LimitIterator::valid</span>

LimitIterator::rewind
=====================

Rewind the iterator to the specified starting offset

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">LimitIterator::rewind</span> ( <span
class="methodparam">void</span> )

Rewinds the iterator to the starting offset specified in <span
class="methodname">LimitIterator::\_\_construct</span>.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">LimitIterator::current</span>
-   <span class="methodname">LimitIterator::key</span>
-   <span class="methodname">LimitIterator::next</span>
-   <span class="methodname">LimitIterator::seek</span>
-   <span class="methodname">LimitIterator::valid</span>

LimitIterator::seek
===================

Seek to the given position

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">LimitIterator::seek</span> ( <span
class="methodparam"><span class="type">int</span> `$position`</span> )

Moves the iterator to the offset specified by `position`.

### 参数

`position`  
The position to seek to.

### 返回值

Returns the offset position after seeking.

### 错误／异常

Throws an <span class="classname">OutOfBoundsException</span> if the
position is outside of the limits specified in <span
class="methodname">LimitIterator::\_\_construct</span>.

### 参见

-   <span class="methodname">LimitIterator::current</span>
-   <span class="methodname">LimitIterator::key</span>
-   <span class="methodname">LimitIterator::rewind</span>
-   <span class="methodname">LimitIterator::next</span>
-   <span class="methodname">LimitIterator::valid</span>

LimitIterator::valid
====================

Check whether the current element is valid

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">LimitIterator::valid</span> ( <span
class="methodparam">void</span> )

Checks whether the current element is valid.

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">LimitIterator::current</span>
-   <span class="methodname">LimitIterator::key</span>
-   <span class="methodname">LimitIterator::rewind</span>
-   <span class="methodname">LimitIterator::next</span>
-   <span class="methodname">LimitIterator::seek</span>

简介
----

An Iterator that sequentially iterates over all attached iterators

类摘要
------

**MultipleIterator**

<span class="ooclass"> class **MultipleIterator** </span> <span
class="oointerface">implements <span
class="interfacename">Iterator</span> </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`MultipleIterator::MIT_NEED_ANY` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MultipleIterator::MIT_NEED_ALL` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MultipleIterator::MIT_KEYS_NUMERIC` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MultipleIterator::MIT_KEYS_ASSOC` <span class="initializer"> = 2</span>
;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span class="methodparam">
<span class="type">int</span> `$flags` <span class="initializer"> =
MultipleIterator::MIT\_NEED\_ALL\|MultipleIterator::MIT\_KEYS\_NUMERIC</span>
</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">attachIterator</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> \[, <span class="methodparam"><span
class="type">string</span> `$infos`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">containsIterator</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">countIterators</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">detachIterator</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setFlags</span> ( <span
class="methodparam"><span class="type">int</span> `$flags`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`MultipleIterator::MIT_NEED_ANY`**  
Do not require all sub iterators to be valid in iteration.

**`MultipleIterator::MIT_NEED_ALL`**  
Require all sub iterators to be valid in iteration.

**`MultipleIterator::MIT_KEYS_NUMERIC`**  
Keys are created from the sub iterators position.

**`MultipleIterator::MIT_KEYS_ASSOC`**  
Keys are created from sub iterators associated information.

MultipleIterator::attachIterator
================================

Attaches iterator information

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">MultipleIterator::attachIterator</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> \[, <span class="methodparam"><span
class="type">string</span> `$infos`</span> \] )

Attaches iterator information.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`iterator`  
The new iterator to attach.

`infos`  
The associative information for the Iterator, which must be an <span
class="type">integer</span>, a <span class="type">string</span>, or
**`NULL`**.

### 返回值

Description...

### 错误／异常

An <span class="classname">IllegalValueException</span> if the
`iterator` parameter is invalid, or if `infos` is already associated
information.

### 参见

-   <span class="methodname">MultipleIterator::\_\_construct</span>

MultipleIterator::\_\_construct
===============================

Constructs a new MultipleIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">MultipleIterator::\_\_construct</span> (\[ <span
class="methodparam"> <span class="type">int</span> `$flags` <span
class="initializer"> =
MultipleIterator::MIT\_NEED\_ALL\|MultipleIterator::MIT\_KEYS\_NUMERIC</span>
</span> \] )

Construct a new MultipleIterator.

### 参数

`flags`  
The flags to set, according to the
<a href="/spl/iterators.html#预定义常量" class="link">Flag Constants</a>.

-   **`MultipleIterator::MIT_NEED_ALL`** or
    **`MultipleIterator::MIT_NEED_ANY`**
-   **`MultipleIterator::MIT_KEYS_NUMERIC`** or
    **`MultipleIterator::MIT_KEYS_ASSOC`**

Defaults to
**`MultipleIterator::MIT_NEED_ALL`**\|**`MultipleIterator::MIT_KEYS_NUMERIC`**.

### 返回值

没有返回值。

### 范例

**示例 \#1 Iterating a MultipleIterator**

``` php
<?php
$people = new ArrayIterator(array('John', 'Jane', 'Jack', 'Judy'));
$roles  = new ArrayIterator(array('Developer', 'Scrum Master', 'Project Owner'));

$team = new MultipleIterator($flags);
$team->attachIterator($people, 'person');
$team->attachIterator($roles, 'role');

foreach ($team as $member) {
    print_r($member);
}
?>
```

Output with *$flags = MIT\_NEED\_ALL\|MIT\_KEYS\_NUMERIC*

    Array
    (
        [0] => John
        [1] => Developer
    )
    Array
    (
        [0] => Jane
        [1] => Scrum Master
    )
    Array
    (
        [0] => Jack
        [1] => Project Owner
    )

Output with *$flags = MIT\_NEED\_ANY\|MIT\_KEYS\_NUMERIC*

    Array
    (
        [0] => John
        [1] => Developer
    )
    Array
    (
        [0] => Jane
        [1] => Scrum Master
    )
    Array
    (
        [0] => Jack
        [1] => Project Owner
    )
    Array
    (
        [0] => Judy
        [1] =>
    )

Output with *$flags = MIT\_NEED\_ALL\|MIT\_KEYS\_ASSOC*

    Array
    (
        [person] => John
        [role] => Developer
    )
    Array
    (
        [person] => Jane
        [role] => Scrum Master
    )
    Array
    (
        [person] => Jack
        [role] => Project Owner
    )

Output with *$flags = MIT\_NEED\_ANY\|MIT\_KEYS\_ASSOC*

    Array
    (
        [person] => John
        [role] => Developer
    )
    Array
    (
        [person] => Jane
        [role] => Scrum Master
    )
    Array
    (
        [person] => Jack
        [role] => Project Owner
    )
    Array
    (
        [person] => Judy
        [role] =>
    )

### 参见

-   <a href="/spl/iterators.html#预定义常量" class="link">Flag Constants</a>
-   <span class="methodname">MultipleIterator::valid</span>

MultipleIterator::containsIterator
==================================

Checks if an iterator is attached

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MultipleIterator::containsIterator</span> (
<span class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

Checks if an iterator is attached or not.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`iterator`  
The iterator to check.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">MultipleIterator::valid</span>

MultipleIterator::countIterators
================================

Gets the number of attached iterator instances

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MultipleIterator::countIterators</span> ( <span
class="methodparam">void</span> )

Gets the number of attached iterator instances.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The number of attached iterator instances (as an <span
class="type">integer</span>).

### 参见

-   <span class="methodname">MultipleIterator::containsIterator</span>

MultipleIterator::current
=========================

Gets the registered iterator instances

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MultipleIterator::current</span> ( <span
class="methodparam">void</span> )

Get the registered iterator instances current() result.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> containing the current values of each
attached iterator, or **`FALSE`** if no iterators are attached.

### 错误／异常

A <span class="classname">RuntimeException</span> if mode
**`MIT_NEED_ALL`** is set and at least one attached iterator is not
valid. Or an <span class="classname">IllegalValueException</span> if a
key is **`NULL`** and **`MIT_KEYS_ASSOC`** is set.

### 参见

-   <span class="methodname">MultipleIterator::valid</span>

MultipleIterator::detachIterator
================================

Detaches an iterator

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">MultipleIterator::detachIterator</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

Detaches an iterator.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`iterator`  
The iterator to detach.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">MultipleIterator::attachIterator</span>

MultipleIterator::getFlags
==========================

Gets the flag information

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MultipleIterator::getFlags</span> ( <span
class="methodparam">void</span> )

Gets information about the flags.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Information about the flags, as an <span class="type">integer</span>.

### 参见

-   <a href="/spl/iterators.html#预定义常量" class="link">Flag Constants</a>
-   <span class="methodname">MultipleIterator::\_\_construct</span>
-   <span class="methodname">MultipleIterator::setFlags</span>

MultipleIterator::key
=====================

Gets the registered iterator instances

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MultipleIterator::key</span> ( <span
class="methodparam">void</span> )

Get the registered iterator instances key() result.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> of all registered iterator instances,
or **`FALSE`** if no sub iterator is attached.

### 错误／异常

A <span class="classname">LogicException</span> if mode
**`MIT_NEED_ALL`** is set, and at least one attached iterator is not
valid.

Calling this method from
<a href="/control-structures/foreach.html" class="xref">foreach</a>
triggers warning "Illegal type returned".

### 参见

-   <span class="methodname">MultipleIterator::current</span>

MultipleIterator::next
======================

Moves all attached iterator instances forward

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">MultipleIterator::next</span> ( <span
class="methodparam">void</span> )

Moves all attached iterator instances forward.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">MultipleIterator::rewind</span>

MultipleIterator::rewind
========================

Rewinds all attached iterator instances

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">MultipleIterator::rewind</span> ( <span
class="methodparam">void</span> )

Rewinds all attached iterator instances.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">MultipleIterator::next</span>

MultipleIterator::setFlags
==========================

Sets flags

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">MultipleIterator::setFlags</span> ( <span
class="methodparam"><span class="type">int</span> `$flags`</span> )

Sets flags.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`flags`  
The flags to set, according to the
<a href="/spl/iterators.html#预定义常量" class="link">Flag Constants</a>

### 返回值

没有返回值。

### 参见

-   <a href="/spl/iterators.html#预定义常量" class="link">Flag Constants</a>
-   <span class="methodname">MultipleIterator::\_\_construct</span>
-   <span class="methodname">MultipleIterator::getFlags</span>

MultipleIterator::valid
=======================

Checks the validity of sub iterators

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MultipleIterator::valid</span> ( <span
class="methodparam">void</span> )

Checks the validity of sub iterators.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if one or all sub iterators are valid depending on
flags, otherwise **`FALSE`**

### 参见

-   <span class="methodname">MultipleIterator::\_\_construct</span>

简介
----

This iterator ignores rewind operations. This allows processing an
iterator in multiple partial foreach loops.

类摘要
------

**NoRewindIterator**

<span class="ooclass"> class **NoRewindIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**IteratorIterator** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">iterator</span>
<span class="methodname">getInnerIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">IteratorIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Traversable</span>
`$iterator`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">IteratorIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Traversable</span> <span
class="methodname">IteratorIterator::getInnerIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">IteratorIterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">IteratorIterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">IteratorIterator::rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">IteratorIterator::valid</span> ( <span
class="methodparam">void</span> )

}

NoRewindIterator::\_\_construct
===============================

Construct a NoRewindIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">NoRewindIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

Constructs a NoRewindIterator.

### 参数

`iterator`  
The iterator being used.

### 返回值

A <span class="methodname">NoRewindIterator</span> based on the passed
in `iterator`.

### 范例

**示例 \#1 <span
class="methodname">NoRewindIterator::\_\_construct</span> example**

The second loop does not output because the iterator is only used once,
as it does not rewind.

``` php
<?php
$fruit = array('apple', 'banana', 'cranberry');

$arr = new ArrayObject($fruit);
$it  = new NoRewindIterator($arr->getIterator());

echo "Fruit A:\n";
foreach( $it as $item ) {
    echo $item . "\n";
}

echo "Fruit B:\n";
foreach( $it as $item ) {
    echo $item . "\n";
}
?>
```

以上例程的输出类似于：

    Fruit A:
    apple
    banana
    cranberry
    Fruit B:

### 参见

-   <span class="methodname">NoRewindIterator::valid</span>

NoRewindIterator::current
=========================

Get the current value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">NoRewindIterator::current</span> ( <span
class="methodparam">void</span> )

Gets the current value.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The current value.

### 参见

-   <span class="methodname">NoRewindIterator::key</span>

NoRewindIterator::getInnerIterator
==================================

Get the inner iterator

### 说明

<span class="modifier">public</span> <span class="type">iterator</span>
<span class="methodname">NoRewindIterator::getInnerIterator</span> (
<span class="methodparam">void</span> )

Gets the inner iterator, that was passed in to <span
class="classname">NoRewindIterator</span>.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The inner iterator, as passed to <span
class="methodname">NoRewindIterator::\_\_construct</span>.

### 参见

-   <span class="methodname">NoRewindIterator::valid</span>

NoRewindIterator::key
=====================

Get the current key

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">NoRewindIterator::key</span> ( <span
class="methodparam">void</span> )

Gets the current key.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The current key.

### 参见

-   <span class="methodname">NoRewindIterator::next</span>

NoRewindIterator::next
======================

Forward to the next element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">NoRewindIterator::next</span> ( <span
class="methodparam">void</span> )

Forwards to the next element.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">NoRewindIterator::rewind</span>

NoRewindIterator::rewind
========================

Prevents the rewind operation on the inner iterator

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">NoRewindIterator::rewind</span> ( <span
class="methodparam">void</span> )

Prevents the rewind operation on the inner iterator.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">NoRewindIterator::rewind</span>
example**

This example demonstrates that calling rewind on a NoRewindIterator
object has no effect.

``` php
<?php
$fruits = array("lemon", "orange", "apple", "pear");

$noRewindIterator = new NoRewindIterator(new ArrayIterator($fruits));

echo $noRewindIterator->current() . "\n";
$noRewindIterator->next();
// now rewind the iterator (nothing should happen)
$noRewindIterator->rewind();
echo $noRewindIterator->current() . "\n";
?>
```

以上例程会输出：

    lemon
    orange

NoRewindIterator::valid
=======================

Validates the iterator

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">NoRewindIterator::valid</span> ( <span
class="methodparam">void</span> )

Checks whether the iterator is valid.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">NoRewindIterator::getInnerIterator</span>

简介
----

This extended <span class="classname">FilterIterator</span> allows a
recursive iteration using <span
class="classname">RecursiveIteratorIterator</span> that only shows those
elements which have children.

类摘要
------

**ParentIterator**

<span class="ooclass"> class **ParentIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**RecursiveFilterIterator** </span> <span class="oointerface">implements
<span class="interfacename">RecursiveIterator</span> </span> <span
class="oointerface">, <span class="interfacename">OuterIterator</span>
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">accept</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">RecursiveIterator</span>
`$iterator`</span> )

<span class="modifier">public</span> <span
class="type">ParentIterator</span> <span
class="methodname">getChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">OuterIterator::getInnerIterator</span> ( <span
class="methodparam">void</span> )

}

ParentIterator::accept
======================

Determines acceptability

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ParentIterator::accept</span> ( <span
class="methodparam">void</span> )

Determines if the current element has children.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the current element is acceptable, otherwise **`FALSE`**.

### 参见

-   <span class="methodname">ParentIterator::hasChildren</span>
-   <span class="methodname">FilterIterator::accept</span>

ParentIterator::\_\_construct
=============================

Constructs a ParentIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">ParentIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">RecursiveIterator</span>
`$iterator`</span> )

Constructs a <span class="classname">ParentIterator</span> on an
iterator.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`iterator`  
The iterator being constructed upon.

### 返回值

The <span class="classname">ParentIterator</span>.

ParentIterator::getChildren
===========================

Return the inner iterator's children contained in a ParentIterator

### 说明

<span class="modifier">public</span> <span
class="type">ParentIterator</span> <span
class="methodname">ParentIterator::getChildren</span> ( <span
class="methodparam">void</span> )

Get the inner iterator's children contained in a ParentIterator.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

An <span class="type">object</span>.

ParentIterator::hasChildren
===========================

Check whether the inner iterator's current element has children

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ParentIterator::hasChildren</span> ( <span
class="methodparam">void</span> )

Check whether the inner iterator's current element has children.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

ParentIterator::next
====================

Move the iterator forward

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ParentIterator::next</span> ( <span
class="methodparam">void</span> )

Moves the iterator forward.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

ParentIterator::rewind
======================

Rewind the iterator

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ParentIterator::rewind</span> ( <span
class="methodparam">void</span> )

Rewinds the iterator.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

简介
----

This iterator allows to unset and modify values and keys while iterating
over Arrays and Objects in the same way as the <span
class="type">ArrayIterator</span>. Additionally it is possible to
iterate over the current iterator entry.

类摘要
------

**RecursiveArrayIterator**

<span class="ooclass"> class **RecursiveArrayIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span> **ArrayIterator**
</span> <span class="oointerface">implements <span
class="interfacename">RecursiveIterator</span> </span> {

/\* 继承的常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`STD_PROP_LIST` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ARRAY_AS_PROPS` <span class="initializer"> = 2</span> ;

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CHILD_ARRAYS_ONLY` <span class="initializer"> = 4</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="type">RecursiveArrayIterator</span> <span
class="methodname">getChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasChildren</span> ( <span
class="methodparam">void</span> )

/\* Inherits \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::append</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::asort</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">ArrayIterator::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$array`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ArrayIterator::count</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ArrayIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ArrayIterator::getArrayCopy</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ArrayIterator::getFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ArrayIterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::ksort</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::natcasesort</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::natsort</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ArrayIterator::offsetExists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ArrayIterator::offsetGet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::offsetSet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$newval`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::offsetUnset</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::seek</span> ( <span
class="methodparam"><span class="type">int</span> `$position`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ArrayIterator::serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::setFlags</span> ( <span
class="methodparam"><span class="type">string</span> `$flags`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::uasort</span> ( <span
class="methodparam"><span class="type">callable</span>
`$cmp_function`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::uksort</span> ( <span
class="methodparam"><span class="type">callable</span>
`$cmp_function`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayIterator::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ArrayIterator::valid</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

RecursiveArrayIterator Flags
----------------------------

**`RecursiveArrayIterator::CHILD_ARRAYS_ONLY`**  
Treat only arrays (not objects) as having children for recursive
iteration.

更新日志
--------

| 版本  | 说明                                    |
|-------|-----------------------------------------|
| 5.3.0 | **`CHILD_ARRAYS_ONLY`** flag was added. |

RecursiveArrayIterator::getChildren
===================================

Returns an iterator for the current entry if it is an <span
class="type">array</span> or an <span class="type">object</span>

### 说明

<span class="modifier">public</span> <span
class="type">RecursiveArrayIterator</span> <span
class="methodname">RecursiveArrayIterator::getChildren</span> ( <span
class="methodparam">void</span> )

Returns an iterator for the current iterator entry.

### 参数

此函数没有参数。

### 返回值

An iterator for the current entry, if it is an <span
class="type">array</span> or <span class="type">object</span>.

### 错误／异常

An <span class="classname">InvalidArgumentException</span> will be
thrown if the current entry does not contain an <span
class="type">array</span> or an <span class="type">object</span>.

### 范例

**示例 \#1 <span
class="function">RecursiveArrayIterator::getChildren</span> example**

``` php
<?php
$fruits = array("a" => "lemon", "b" => "orange", array("a" => "apple", "p" => "pear"));

$iterator = new RecursiveArrayIterator($fruits);

while ($iterator->valid()) {

    if ($iterator->hasChildren()) {
        // print all children
        foreach ($iterator->getChildren() as $key => $value) {
            echo $key . ' : ' . $value . "\n";
        }
    } else {
        echo "No children.\n";
    }

    $iterator->next();
}
?>
```

以上例程会输出：

    No children.
    No children.
    a : apple
    p : pear

### 参见

-   <span class="function">RecursiveArrayIterator::hasChildren</span>

RecursiveArrayIterator::hasChildren
===================================

Returns whether current entry is an array or an object

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RecursiveArrayIterator::hasChildren</span> (
<span class="methodparam">void</span> )

Returns whether current entry is an <span class="type">array</span> or
an <span class="type">object</span> for which an iterator can be
obtained via <span
class="methodname">RecursiveArrayIterator::getChildren</span>.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the current entry is an <span
class="type">array</span> or an <span class="type">object</span>,
otherwise **`FALSE`** is returned.

### 范例

**示例 \#1 <span
class="function">RecursiveArrayIterator::hasChildren</span> example**

``` php
<?php
$fruits = array("a" => "lemon", "b" => "orange", array("a" => "apple", "p" => "pear"));

$iterator = new RecursiveArrayIterator($fruits);

while ($iterator->valid()) {

    // Check if there are children
    if ($iterator->hasChildren()) {
        // print all children
        foreach ($iterator->getChildren() as $key => $value) {
            echo $key . ' : ' . $value . "\n";
        }
    } else {
        echo "No children.\n";
    }

    $iterator->next();
}
?>
```

以上例程会输出：

    No children.
    No children.
    a : apple
    p : pear

### 参见

-   <span class="function">RecursiveArrayIterator::getChildren</span>

简介
----

...

类摘要
------

**RecursiveCachingIterator**

<span class="ooclass"> class **RecursiveCachingIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**CachingIterator** </span> <span class="oointerface">implements <span
class="interfacename">Countable</span> </span> <span
class="oointerface">, <span class="interfacename">ArrayAccess</span>
</span> <span class="oointerface">, <span
class="interfacename">OuterIterator</span> </span> <span
class="oointerface">, <span
class="interfacename">RecursiveIterator</span> </span> {

/\* 继承的常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CachingIterator::CALL_TOSTRING` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CachingIterator::CATCH_GET_CHILD` <span class="initializer"> =
16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CachingIterator::TOSTRING_USE_KEY` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CachingIterator::TOSTRING_USE_CURRENT` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CachingIterator::TOSTRING_USE_INNER` <span class="initializer"> =
8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CachingIterator::FULL_CACHE` <span class="initializer"> = 256</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
self::CALL\_TOSTRING</span></span> \] )

<span class="modifier">public</span> <span
class="type">RecursiveCachingIterator</span> <span
class="methodname">getChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasChildren</span> ( <span
class="methodparam">void</span> )

/\* Inherits \*/

<span class="modifier">public</span> <span
class="methodname">CachingIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
self::CALL\_TOSTRING</span></span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CachingIterator::count</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">CachingIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CachingIterator::getCache</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CachingIterator::getFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">CachingIterator::getInnerIterator</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::hasNext</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">scalar</span>
<span class="methodname">CachingIterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::offsetExists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::offsetGet</span> ( <span
class="methodparam"><span class="type">string</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::offsetSet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$newval`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::offsetUnset</span> ( <span
class="methodparam"><span class="type">string</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::setFlags</span> ( <span
class="methodparam"><span class="type">int</span> `$flags`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CachingIterator::valid</span> ( <span
class="methodparam">void</span> )

}

RecursiveCachingIterator::\_\_construct
=======================================

Construct

### 说明

<span class="modifier">public</span> <span
class="methodname">RecursiveCachingIterator::\_\_construct</span> (
<span class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
self::CALL\_TOSTRING</span></span> \] )

Constructs a new <span
class="classname">RecursiveCachingIterator</span>, which consists of a
passed in `iterator`.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`iterator`  
The iterator being used.

`flags`  
The flags. Use **`CALL_TOSTRING`** to call <span
class="methodname">RecursiveCachingIterator::\_\_toString</span> for
every element (the default), and/or **`CATCH_GET_CHILD`** to catch
exceptions when trying to get children.

### 返回值

The <span class="classname">RecursiveCachingIterator</span>.

### 参见

-   <span class="methodname">CachingIterator::\_\_construct</span>

RecursiveCachingIterator::getChildren
=====================================

Return the inner iterator's children as a RecursiveCachingIterator

### 说明

<span class="modifier">public</span> <span
class="type">RecursiveCachingIterator</span> <span
class="methodname">RecursiveCachingIterator::getChildren</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The inner iterator's children, as a RecursiveCachingIterator.

RecursiveCachingIterator::hasChildren
=====================================

Check whether the current element of the inner iterator has children

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RecursiveCachingIterator::hasChildren</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the inner iterator has children, otherwise **`FALSE`**

简介
----

类摘要
------

**RecursiveCallbackFilterIterator**

<span class="ooclass"> class **RecursiveCallbackFilterIterator** </span>
<span class="ooclass"> <span class="modifier">extends</span>
**CallbackFilterIterator** </span> <span class="oointerface">implements
<span class="interfacename">OuterIterator</span> </span> <span
class="oointerface">, <span
class="interfacename">RecursiveIterator</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">RecursiveIterator</span>
`$iterator`</span> , <span class="methodparam"><span
class="type">string</span> `$callback`</span> )

<span class="modifier">public</span> <span
class="type">RecursiveCallbackFilterIterator</span> <span
class="methodname">getChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasChildren</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">CallbackFilterIterator::accept</span> ( <span
class="methodparam">void</span> )

}

范例
----

The callback should accept up to three arguments: the current item, the
current key and the iterator, respectively.

**示例 \#1 Available callback arguments**

``` php
<?php

/**
 * Callback for RecursiveCallbackFilterIterator
 *
 * @param $current   Current item's value
 * @param $key       Current item's key
 * @param $iterator  Iterator being filtered
 * @return boolean   TRUE to accept the current item, FALSE otherwise
 */
function my_callback($current, $key, $iterator) {
    // Your filtering code here
}

?>
```

Filtering a recursive iterator generally involves two conditions. The
first is that, to allow recursion, the callback function should return
**`TRUE`** if the current iterator item has children. The second is the
normal filter condition, such as a file size or extension check as in
the example below.

**示例 \#2 Recursive callback basic example**

``` php
<?php

$dir = new RecursiveDirectoryIterator(__DIR__);

// Filter large files ( > 100MB)
$files = new RecursiveCallbackFilterIterator($dir, function ($current, $key, $iterator) {
    // Allow recursion
    if ($iterator->hasChildren()) {
        return TRUE;
    }
    // Check for large file
    if ($current->isFile() && $current->getSize() > 104857600) {
        return TRUE;
    }
    return FALSE;
});
 
foreach (new RecursiveIteratorIterator($files) as $file) {
    echo $file->getPathname() . PHP_EOL;
}

?>
```

RecursiveCallbackFilterIterator::\_\_construct
==============================================

Create a RecursiveCallbackFilterIterator from a RecursiveIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">RecursiveCallbackFilterIterator::\_\_construct</span>
( <span class="methodparam"><span class="type">RecursiveIterator</span>
`$iterator`</span> , <span class="methodparam"><span
class="type">string</span> `$callback`</span> )

Creates a filtered iterator from a <span
class="interfacename">RecursiveIterator</span> using the `callback` to
determine which items are accepted or rejected.

### 参数

`iterator`  
The recursive iterator to be filtered.

`callback`  
The callback, which should return **`TRUE`** to accept the current item
or **`FALSE`** otherwise. See
<a href="/spl/iterators.html#范例" class="link">Examples</a>.

May be any valid <span class="type">callable</span> value.

### 返回值

没有返回值。

### 参见

-   <a href="/spl/iterators.html#范例" class="link">RecursiveCallbackFilterIterator Examples</a>
-   <span
    class="methodname">RecursiveCallbackFilterIterator::getChildren</span>
-   <span
    class="methodname">RecursiveCallbackFilteriterator::hasChildren</span>

RecursiveCallbackFilterIterator::getChildren
============================================

Return the inner iterator's children contained in a
RecursiveCallbackFilterIterator

### 说明

<span class="modifier">public</span> <span
class="type">RecursiveCallbackFilterIterator</span> <span
class="methodname">RecursiveCallbackFilterIterator::getChildren</span> (
<span class="methodparam">void</span> )

Fetches the filtered children of the inner iterator.

<span
class="methodname">RecursiveCallbackFilterIterator::hasChildren</span>
should be used to determine if there are children to be fetched.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="classname">RecursiveCallbackFilterIterator</span>
containing the children.

### 参见

-   <a href="/spl/iterators.html#范例" class="link">RecursiveCallbackFilterIterator Examples</a>
-   <span
    class="methodname">RecursiveCallbackFilterIterator::\_\_construct</span>
-   <span
    class="methodname">RecursiveCallbackFilteriterator::hasChildren</span>

RecursiveCallbackFilterIterator::hasChildren
============================================

Check whether the inner iterator's current element has children

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">RecursiveCallbackFilterIterator::hasChildren</span> (
<span class="methodparam">void</span> )

Returns **`TRUE`** if the current element has children, **`FALSE`**
otherwise.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the current element has children, **`FALSE`**
otherwise.

### 范例

**示例 \#1 <span
class="methodname">RecursiveCallbackFilterIterator::hasChildren</span>
basic usage**

``` php
<?php

$dir = new RecursiveDirectoryIterator(__DIR__);

// Recursively iterate over XML files
$files = new RecursiveCallbackFilterIterator($dir, function ($current, $key, $iterator) {
    // Allow recursion into directories
    if ($iterator->hasChildren()) {
        return TRUE;
    }
    // Check for XML file
    if (!strcasecmp($current->getExtension(), 'xml')) {
        return TRUE;
    }
    return FALSE;
});

?>
```

### 参见

-   <a href="/spl/iterators.html#范例" class="link">RecursiveCallbackFilterIterator Examples</a>
-   <span
    class="methodname">RecursiveCallbackFilterIterator::\_\_construct</span>
-   <span
    class="methodname">RecursiveCallbackFilteriterator::getChildren</span>

简介
----

The <span class="classname">RecursiveDirectoryIterator</span> provides
an interface for iterating recursively over filesystem directories.

类摘要
------

**RecursiveDirectoryIterator**

<span class="ooclass"> class **RecursiveDirectoryIterator** </span>
<span class="ooclass"> <span class="modifier">extends</span>
**FilesystemIterator** </span> <span class="oointerface">implements
<span class="interfacename">SeekableIterator</span> </span> <span
class="oointerface">, <span
class="interfacename">RecursiveIterator</span> </span> {

/\* 继承的常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::CURRENT_AS_PATHNAME` <span class="initializer"> =
32</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::CURRENT_AS_FILEINFO` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::CURRENT_AS_SELF` <span class="initializer"> =
16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::CURRENT_MODE_MASK` <span class="initializer"> =
240</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::KEY_AS_PATHNAME` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::KEY_AS_FILENAME` <span class="initializer"> =
256</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::FOLLOW_SYMLINKS` <span class="initializer"> =
512</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::KEY_MODE_MASK` <span class="initializer"> =
3840</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::NEW_CURRENT_AND_KEY` <span class="initializer"> =
256</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::SKIP_DOTS` <span class="initializer"> = 4096</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`FilesystemIterator::UNIX_PATHS` <span class="initializer"> =
8192</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = FilesystemIterator::KEY\_AS\_PATHNAME \|
FilesystemIterator::CURRENT\_AS\_FILEINFO</span></span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getSubPath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getSubPathname</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasChildren</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$allow_links`<span
class="initializer"> = **`FALSE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

/\* Inherits \*/

<span class="modifier">public</span> <span
class="methodname">FilesystemIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = FilesystemIterator::KEY\_AS\_PATHNAME \|
FilesystemIterator::CURRENT\_AS\_FILEINFO \|
FilesystemIterator::SKIP\_DOTS</span></span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">FilesystemIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">FilesystemIterator::getFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">FilesystemIterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilesystemIterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilesystemIterator::rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilesystemIterator::setFlags</span> (\[ <span
class="methodparam"><span class="type">int</span> `$flags`</span> \] )

}

更新日志
--------

| 版本          | 说明                                                                                                                                                                       |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0         | The <span class="classname">FilesystemIterator</span> was introduced as the parent class. Previously, the parent was the <span class="classname">DirectoryIterator</span>. |
| 5.3.0         | Implements <span class="interfacename">SeekableIterator</span>.                                                                                                            |
| 5.2.11, 5.3.1 | Added **`RecursiveDirectoryIterator::FOLLOW_SYMLINKS`**                                                                                                                    |

RecursiveDirectoryIterator::\_\_construct
=========================================

Constructs a RecursiveDirectoryIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">RecursiveDirectoryIterator::\_\_construct</span> (
<span class="methodparam"><span class="type">string</span>
`$path`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
FilesystemIterator::KEY\_AS\_PATHNAME \|
FilesystemIterator::CURRENT\_AS\_FILEINFO</span></span> \] )

Constructs a <span class="methodname">RecursiveDirectoryIterator</span>
for the provided `path`.

### 参数

`path`  
The path of the directory to be iterated over.

`flags`  
Flags may be provided which will affect the behavior of some methods. A
list of the flags can found under
<a href="/spl/iterators.html#预定义常量" class="link">FilesystemIterator predefined constants</a>.
They can also be set later with <span
class="methodname">FilesystemIterator::setFlags</span>.

### 返回值

Returns the newly created <span
class="classname">RecursiveDirectoryIterator</span>.

### 错误／异常

Throws an <span class="classname">UnexpectedValueException</span> if the
`path` cannot be found or is not a directory.

### 范例

**示例 \#1 <span class="classname">RecursiveDirectoryIterator</span>
example**

``` php
<?php

$directory = '/tmp';

$it = new RecursiveIteratorIterator(new RecursiveDirectoryIterator($directory));

$it->rewind();
while($it->valid()) {

    if (!$it->isDot()) {
        echo 'SubPathName: ' . $it->getSubPathName() . "\n";
        echo 'SubPath:     ' . $it->getSubPath() . "\n";
        echo 'Key:         ' . $it->key() . "\n\n";
    }

    $it->next();
}

?>
```

以上例程的输出类似于：

    SubPathName: fruit/apple.xml
    SubPath:     fruit
    Key:         /tmp/fruit/apple.xml

    SubPathName: stuff.xml
    SubPath:     
    Key:         /tmp/stuff.xml

    SubPathName: veggies/carrot.xml
    SubPath:     veggies
    Key:         /tmp/veggies/carrot.xml

### 参见

-   <span class="methodname">FilesystemIterator::\_\_construct</span>
-   <span
    class="methodname">RecursiveIteratorIterator::\_\_construct</span>
-   <a href="/spl/iterators.html#预定义常量" class="link">FilesystemIterator predefined constants</a>

RecursiveDirectoryIterator::getChildren
=======================================

Returns an iterator for the current entry if it is a directory

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">RecursiveDirectoryIterator::getChildren</span>
( <span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The filename, file information, or $this depending on the set flags. See
the
<a href="/spl/iterators.html#预定义常量" class="link">FilesystemIterator constants</a>.

RecursiveDirectoryIterator::getSubPath
======================================

Get sub path

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RecursiveDirectoryIterator::getSubPath</span> (
<span class="methodparam">void</span> )

Returns the sub path relative to the directory given in the constructor.

### 参数

此函数没有参数。

### 返回值

The sub path.

### 范例

**示例 \#1 <span class="function">getSubPath</span> example**

``` php
$directory = '/tmp';
      
      $it = new RecursiveIteratorIterator(new RecursiveDirectoryIterator($directory));
      
      foreach ($it as $file) {
          echo 'SubPathName: ' . $it->getSubPathName() . "\n";
          echo 'SubPath:     ' . $it->getSubPath() . "\n\n";
      }
```

以上例程的输出类似于：

         SubPathName: fruit/apple.xml
         SubPath:     fruit
         
         SubPathName: stuff.xml
         SubPath:     
         
         SubPathName: veggies/carrot.xml
         SubPath:     veggies
        

### 参见

-   <span
    class="methodname">RecursiveDirectoryIterator::getSubPathName</span>
-   <span class="methodname">RecursiveDirectoryIterator::key</span>

RecursiveDirectoryIterator::getSubPathname
==========================================

Get sub path and name

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">RecursiveDirectoryIterator::getSubPathname</span> (
<span class="methodparam">void</span> )

Gets the sub path and filename.

### 参数

此函数没有参数。

### 返回值

The sub path (sub directory) and filename.

### 范例

**示例 \#1 <span class="function">getSubPathname</span> example**

``` php
$directory = '/tmp';
      
      $it = new RecursiveIteratorIterator(new RecursiveDirectoryIterator($directory));
      
      foreach ($it as $file) {
          echo 'SubPathName: ' . $it->getSubPathName() . "\n";
          echo 'SubPath:     ' . $it->getSubPath() . "\n\n";
      }
```

以上例程的输出类似于：

         SubPathName: fruit/apple.xml
         SubPath:     fruit
         
         SubPathName: stuff.xml
         SubPath:     
         
         SubPathName: veggies/carrot.xml
         SubPath:     veggies
        

### 参见

-   <span
    class="methodname">RecursiveDirectoryIterator::getSubPath</span>
-   <span class="methodname">RecursiveDirectoryIterator::key</span>

RecursiveDirectoryIterator::hasChildren
=======================================

Returns whether current entry is a directory and not '.' or '..'

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RecursiveDirectoryIterator::hasChildren</span>
(\[ <span class="methodparam"><span class="type">bool</span>
`$allow_links`<span class="initializer"> = **`FALSE`**</span></span> \]
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`allow_links`  

### 返回值

Returns whether the current entry is a directory, but not '.' or '..'

RecursiveDirectoryIterator::key
===============================

Return path and filename of current dir entry

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RecursiveDirectoryIterator::key</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The path and filename of the current dir entry.

RecursiveDirectoryIterator::next
================================

Move to next entry

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveDirectoryIterator::next</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveDirectoryIterator::rewind
==================================

Rewind dir back to the start

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveDirectoryIterator::rewind</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

简介
----

This abstract iterator filters out unwanted values for a <span
class="classname">RecursiveIterator</span>. This class should be
extended to implement custom filters. The <span
class="methodname">RecursiveFilterIterator::accept</span> must be
implemented in the subclass.

类摘要
------

**RecursiveFilterIterator**

<span class="ooclass"> <span class="modifier">abstract</span> class
**RecursiveFilterIterator** </span> <span class="ooclass"> <span
class="modifier">extends</span> **FilterIterator** </span> <span
class="oointerface">implements <span
class="interfacename">OuterIterator</span> </span> <span
class="oointerface">, <span
class="interfacename">RecursiveIterator</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">RecursiveIterator</span>
`$iterator`</span> )

<span class="modifier">public</span> <span
class="type">RecursiveFilterIterator</span> <span
class="methodname">getChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasChildren</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="modifier">abstract</span> <span class="type">bool</span> <span
class="methodname">FilterIterator::accept</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">FilterIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">FilterIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">FilterIterator::getInnerIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">FilterIterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilterIterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilterIterator::rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">FilterIterator::valid</span> ( <span
class="methodparam">void</span> )

}

RecursiveFilterIterator::\_\_construct
======================================

Create a RecursiveFilterIterator from a RecursiveIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">RecursiveFilterIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">RecursiveIterator</span>
`$iterator`</span> )

Create a <span class="classname">RecursiveFilterIterator</span> from a
<span class="classname">RecursiveIterator</span>.

### 参数

`iterator`  
The <span class="classname">RecursiveIterator</span> to be filtered.

### 返回值

没有返回值。

### 范例

**示例 \#1 Basic <span class="methodname">RecursiveFilterIterator</span>
example**

``` php
<?php
class TestsOnlyFilter extends RecursiveFilterIterator {
    public function accept() {
        // Accept the current item if we can recurse into it
        // or it is a value starting with "test"
        return $this->hasChildren() || (strpos($this->current(), "test") !== FALSE);
    }
}

$array    = array("test1", array("taste2", "test3", "test4"), "test5");
$iterator = new RecursiveArrayIterator($array);
$filter   = new TestsOnlyFilter($iterator);

foreach(new RecursiveIteratorIterator($filter) as $key => $value)
{
    echo $value . "\n";
}
?>
```

以上例程的输出类似于：

    test1
    test3
    test4
    test5

**示例 \#2 <span class="methodname">RecursiveFilterIterator</span>
example**

``` php
<?php
class StartsWithFilter extends RecursiveFilterIterator {

    protected $word;

    public function __construct(RecursiveIterator $rit, $word) {
        $this->word = $word;
        parent::__construct($rit);
    }

    public function accept() {
        return $this->hasChildren() OR strpos($this->current(), $this->word) === 0;
    }
    
    public function getChildren() {
        return new self($this->getInnerIterator()->getChildren(), $this->word);
    }
}

$array    = array("test1", array("taste2", "test3", "test4"), "test5");
$iterator = new RecursiveArrayIterator($array);
$filter   = new StartsWithFilter($iterator, "test");

foreach(new RecursiveIteratorIterator($filter) as $key => $value)
{
    echo $value . "\n";
}
?>
```

以上例程的输出类似于：

    test1
    test3
    test4
    test5

### 参见

-   <span class="methodname">RecursiveFilterIterator::getChildren</span>
-   <span class="methodname">RecursiveFilterIterator::hasChildren</span>
-   <span class="methodname">FilterIterator::accept</span>

RecursiveFilterIterator::getChildren
====================================

Return the inner iterator's children contained in a
RecursiveFilterIterator

### 说明

<span class="modifier">public</span> <span
class="type">RecursiveFilterIterator</span> <span
class="methodname">RecursiveFilterIterator::getChildren</span> ( <span
class="methodparam">void</span> )

Return the inner iterator's children contained in a <span
class="classname">RecursiveFilterIterator</span>.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="classname">RecursiveFilterIterator</span>
containing the inner iterator's children.

### 参见

-   <span class="methodname">RecursiveFilterIterator::hasChildren</span>
-   <span class="methodname">RecursiveIterator::getChildren</span>

RecursiveFilterIterator::hasChildren
====================================

Check whether the inner iterator's current element has children

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RecursiveFilterIterator::hasChildren</span> (
<span class="methodparam">void</span> )

Check whether the inner iterator's current element has children.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the inner iterator has children, otherwise **`FALSE`**

### 参见

-   <span class="methodname">RecursiveFilterIterator::getChildren</span>
-   <span class="methodname">RecursiveIterator::hasChildren</span>

简介
----

Can be used to iterate through recursive iterators.

类摘要
------

**RecursiveIteratorIterator**

<span class="ooclass"> class **RecursiveIteratorIterator** </span> <span
class="oointerface">implements <span
class="interfacename">OuterIterator</span> </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveIteratorIterator::LEAVES_ONLY` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveIteratorIterator::SELF_FIRST` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveIteratorIterator::CHILD_FIRST` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveIteratorIterator::CATCH_GET_CHILD` <span class="initializer">
= 16</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">beginChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">beginIteration</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">RecursiveIterator</span> <span
class="methodname">callGetChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">callHasChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">Traversable</span>
`$iterator`</span> \[, <span class="methodparam"><span
class="type">int</span> `$mode`<span class="initializer"> =
RecursiveIteratorIterator::LEAVES\_ONLY</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">endChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">endIteration</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getDepth</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">iterator</span>
<span class="methodname">getInnerIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getMaxDepth</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">RecursiveIterator</span> <span
class="methodname">getSubIterator</span> (\[ <span
class="methodparam"><span class="type">int</span> `$level`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">nextElement</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMaxDepth</span> (\[ <span
class="methodparam"><span class="type">int</span> `$max_depth`<span
class="initializer"> = -1</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">OuterIterator::getInnerIterator</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`RecursiveIteratorIterator::LEAVES_ONLY`**  

**`RecursiveIteratorIterator::SELF_FIRST`**  

**`RecursiveIteratorIterator::CHILD_FIRST`**  

**`RecursiveIteratorIterator::CATCH_GET_CHILD`**  

RecursiveIteratorIterator::beginChildren
========================================

Begin children

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::beginChildren</span>
( <span class="methodparam">void</span> )

Is called after calling <span
class="methodname">RecursiveIteratorIterator::getChildren</span>, and
its associated <span
class="methodname">RecursiveIteratorIterator::rewind</span>.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveIteratorIterator::beginIteration
=========================================

Begin Iteration

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span
class="methodname">RecursiveIteratorIterator::beginIteration</span> (
<span class="methodparam">void</span> )

Called when iteration begins (after the first <span
class="methodname">RecursiveIteratorIterator::rewind</span> call.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveIteratorIterator::callGetChildren
==========================================

Get children

### 说明

<span class="modifier">public</span> <span
class="type">RecursiveIterator</span> <span
class="methodname">RecursiveIteratorIterator::callGetChildren</span> (
<span class="methodparam">void</span> )

Get children of the current element.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

A <span class="methodname">RecursiveIterator</span>.

RecursiveIteratorIterator::callHasChildren
==========================================

Has children

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">RecursiveIteratorIterator::callHasChildren</span> (
<span class="methodparam">void</span> )

Called for each element to test whether it has children.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the element has children, otherwise **`FALSE`**

RecursiveIteratorIterator::\_\_construct
========================================

Construct a RecursiveIteratorIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">RecursiveIteratorIterator::\_\_construct</span> (
<span class="methodparam"><span class="type">Traversable</span>
`$iterator`</span> \[, <span class="methodparam"><span
class="type">int</span> `$mode`<span class="initializer"> =
RecursiveIteratorIterator::LEAVES\_ONLY</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \]\] )

Creates a <span class="classname">RecursiveIteratorIterator</span> from
a <span class="classname">RecursiveIterator</span>.

### 参数

`iterator`  
The iterator being constructed from. Either a <span
class="classname">RecursiveIterator</span> or <span
class="classname">IteratorAggregate</span>.

`mode`  
Optional mode. Possible values are

-   **`RecursiveIteratorIterator::LEAVES_ONLY`** - The default. Lists
    only leaves in iteration.
-   **`RecursiveIteratorIterator::SELF_FIRST`** - Lists leaves and
    parents in iteration with parents coming first.
-   **`RecursiveIteratorIterator::CHILD_FIRST`** - Lists leaves and
    parents in iteration with leaves coming first.

`flags`  
Optional flag. Possible values are
**`RecursiveIteratorIterator::CATCH_GET_CHILD`** which will then ignore
exceptions thrown in calls to <span
class="methodname">RecursiveIteratorIterator::getChildren</span>.

### 返回值

没有返回值。

### 范例

**示例 \#1 Iterating a RecursiveIteratorIterator**

``` php
<?php
$array = array(
    array(
        array(
            array(
                'leaf-0-0-0-0',
                'leaf-0-0-0-1'
            ),
            'leaf-0-0-0'
        ),
        array(
            array(
                'leaf-0-1-0-0',
                'leaf-0-1-0-1'
            ),
            'leaf-0-1-0'
        ),
        'leaf-0-0'
    )
);

$iterator = new RecursiveIteratorIterator(
    new RecursiveArrayIterator($array),
    $mode
);
foreach ($iterator as $key => $leaf) {
    echo "$key => $leaf", PHP_EOL;
}
?>
```

Output with *$mode = RecursiveIteratorIterator::LEAVES\_ONLY*

    0 => leaf-0-0-0-0
    1 => leaf-0-0-0-1
    0 => leaf-0-0-0
    0 => leaf-0-1-0-0
    1 => leaf-0-1-0-1
    0 => leaf-0-1-0
    0 => leaf-0-0

Output with *$mode = RecursiveIteratorIterator::SELF\_FIRST*

    0 => Array
    0 => Array
    0 => Array
    0 => leaf-0-0-0-0
    1 => leaf-0-0-0-1
    1 => leaf-0-0-0
    1 => Array
    0 => Array
    0 => leaf-0-1-0-0
    1 => leaf-0-1-0-1
    1 => leaf-0-1-0
    2 => leaf-0-0

Output with *$mode = RecursiveIteratorIterator::CHILD\_FIRST*

    0 => leaf-0-0-0-0
    1 => leaf-0-0-0-1
    0 => Array
    1 => leaf-0-0-0
    0 => Array
    0 => leaf-0-1-0-0
    1 => leaf-0-1-0-1
    0 => Array
    1 => leaf-0-1-0
    1 => Array
    2 => leaf-0-0
    0 => Array

RecursiveIteratorIterator::current
==================================

Access the current element value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">RecursiveIteratorIterator::current</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The current elements value.

RecursiveIteratorIterator::endChildren
======================================

End children

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::endChildren</span> (
<span class="methodparam">void</span> )

Called when end recursing one level.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveIteratorIterator::endIteration
=======================================

End Iteration

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::endIteration</span>
( <span class="methodparam">void</span> )

Called when the iteration ends (when <span
class="methodname">RecursiveIteratorIterator::valid</span> first returns
**`FALSE`**.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveIteratorIterator::getDepth
===================================

Get the current depth of the recursive iteration

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RecursiveIteratorIterator::getDepth</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The current depth of the recursive iteration.

RecursiveIteratorIterator::getInnerIterator
===========================================

Get inner iterator

### 说明

<span class="modifier">public</span> <span class="type">iterator</span>
<span
class="methodname">RecursiveIteratorIterator::getInnerIterator</span> (
<span class="methodparam">void</span> )

Gets the current active sub iterator.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The current active sub iterator.

RecursiveIteratorIterator::getMaxDepth
======================================

Get max depth

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">RecursiveIteratorIterator::getMaxDepth</span> (
<span class="methodparam">void</span> )

Gets the maximum allowable depth.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The maximum accepted depth, or **`FALSE`** if any depth is allowed.

### 参见

-   <span
    class="methodname">RecursiveIteratorIterator::setMaxDepth</span>

RecursiveIteratorIterator::getSubIterator
=========================================

The current active sub iterator

### 说明

<span class="modifier">public</span> <span
class="type">RecursiveIterator</span> <span
class="methodname">RecursiveIteratorIterator::getSubIterator</span> (\[
<span class="methodparam"><span class="type">int</span> `$level`</span>
\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`level`  

### 返回值

The current active sub iterator.

RecursiveIteratorIterator::key
==============================

Access the current key

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">RecursiveIteratorIterator::key</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The current key.

RecursiveIteratorIterator::next
===============================

Move forward to the next element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::next</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveIteratorIterator::nextElement
======================================

Next element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::nextElement</span> (
<span class="methodparam">void</span> )

Called when the next element is available.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveIteratorIterator::rewind
=================================

Rewind the iterator to the first element of the top level inner iterator

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::rewind</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveIteratorIterator::setMaxDepth
======================================

Set max depth

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::setMaxDepth</span>
(\[ <span class="methodparam"><span class="type">int</span>
`$max_depth`<span class="initializer"> = -1</span></span> \] )

Set the maximum allowed depth.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`max_depth`  
The maximum allowed depth. *-1* is used for any depth.

### 返回值

没有返回值。

### 错误／异常

Emits an <span class="classname">Exception</span> if `max_depth` is less
than *-1*.

RecursiveIteratorIterator::valid
================================

Check whether the current position is valid

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RecursiveIteratorIterator::valid</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the current position is valid, otherwise **`FALSE`**

简介
----

This recursive iterator can filter another recursive iterator via a
regular expression.

类摘要
------

**RecursiveRegexIterator**

<span class="ooclass"> class **RecursiveRegexIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span> **RegexIterator**
</span> <span class="oointerface">implements <span
class="interfacename">RecursiveIterator</span> </span> {

/\* 继承的常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`MATCH` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`GET_MATCH` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ALL_MATCHES` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`SPLIT` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`REPLACE` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`USE_KEY` <span class="initializer"> = 1</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">RecursiveIterator</span>
`$iterator`</span> , <span class="methodparam"><span
class="type">string</span> `$regex`</span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = self::MATCH</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$preg_flags`<span
class="initializer"> = 0</span></span> \]\]\] )

<span class="modifier">public</span> <span
class="type">RecursiveRegexIterator</span> <span
class="methodname">getChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasChildren</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="type">RecursiveIterator</span> <span
class="methodname">RecursiveIterator::getChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RecursiveIterator::hasChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RegexIterator::accept</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RegexIterator::getFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RegexIterator::getMode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RegexIterator::getPregFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RegexIterator::getRegex</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RegexIterator::setFlags</span> ( <span
class="methodparam"><span class="type">int</span> `$flags`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RegexIterator::setMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RegexIterator::setPregFlags</span> ( <span
class="methodparam"><span class="type">int</span> `$preg_flags`</span> )

}

RecursiveRegexIterator::\_\_construct
=====================================

Creates a new RecursiveRegexIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">RecursiveRegexIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">RecursiveIterator</span>
`$iterator`</span> , <span class="methodparam"><span
class="type">string</span> `$regex`</span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = self::MATCH</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$preg_flags`<span
class="initializer"> = 0</span></span> \]\]\] )

Creates a new regular expression iterator.

### 参数

`iterator`  
The recursive iterator to apply this regex filter to.

`regex`  
The regular expression to match.

`mode`  
Operation mode, see <span
class="methodname">RegexIterator::setMode</span> for a list of modes.

`flags`  
Special flags, see <span
class="methodname">RegexIterator::setFlags</span> for a list of
available flags.

`preg_flags`  
The regular expression flags. These flags depend on the operation mode
parameter:

| operation mode                        | available flags                                     |
|---------------------------------------|-----------------------------------------------------|
| `RecursiveRegexIterator::ALL_MATCHES` | See <span class="function">preg\_match\_all</span>. |
| `RecursiveRegexIterator::GET_MATCH`   | See <span class="function">preg\_match</span>.      |
| `RecursiveRegexIterator::MATCH`       | See <span class="function">preg\_match</span>.      |
| `RecursiveRegexIterator::REPLACE`     | none.                                               |
| `RecursiveRegexIterator::SPLIT`       | See <span class="function">preg\_split</span>.      |

### 范例

**示例 \#1 <span
class="function">RecursiveRegexIterator::\_\_construct</span> example**

Creates a new RegexIterator that filters all strings that start with
'test'.

``` php
<?php
$rArrayIterator = new RecursiveArrayIterator(array('test1', array('tet3', 'test4', 'test5')));
$rRegexIterator = new RecursiveRegexIterator($rArrayIterator, '/^test/',
    RecursiveRegexIterator::ALL_MATCHES);

foreach ($rRegexIterator as $key1 => $value1) {

    if ($rRegexIterator->hasChildren()) {

        // print all children
        echo "Children: ";
        foreach ($rRegexIterator->getChildren() as $key => $value) {
            echo $value . " ";
        }
        echo "\n";
    } else {
        echo "No children\n";
    }

}
?>
```

以上例程的输出类似于：

    No children
    Children: test4 test5

### 参见

-   <span class="function">preg\_match</span>
-   <span class="function">preg\_match\_all</span>
-   <span class="function">preg\_replace</span>
-   <span class="function">preg\_split</span>

RecursiveRegexIterator::getChildren
===================================

Returns an iterator for the current entry

### 说明

<span class="modifier">public</span> <span
class="type">RecursiveRegexIterator</span> <span
class="methodname">RecursiveRegexIterator::getChildren</span> ( <span
class="methodparam">void</span> )

Returns an iterator for the current iterator entry.

### 参数

此函数没有参数。

### 返回值

An iterator for the current entry, if it can be iterated over by the
inner iterator.

### 错误／异常

An <span class="classname">InvalidArgumentException</span> will be
thrown if the current entry does not contain a value that can be
iterated over by the inner iterator.

### 范例

**示例 \#1 <span
class="function">RecursiveRegexIterator::getChildren</span> example**

``` php
<?php
$rArrayIterator = new RecursiveArrayIterator(array('test1', array('tet3', 'test4', 'test5')));
$rRegexIterator = new RecursiveRegexIterator($rArrayIterator, '/^test/',
    RecursiveRegexIterator::ALL_MATCHES);

foreach ($rRegexIterator as $key1 => $value1) {

    if ($rRegexIterator->hasChildren()) {

        // print all children
        echo "Children: ";
        foreach ($rRegexIterator->getChildren() as $key => $value) {
            echo $value . " ";
        }
        echo "\n";
    } else {
        echo "No children\n";
    }

}
?>
```

以上例程会输出：

    No children
    Children: test4 test5

### 参见

-   <span class="function">RecursiveRegexIterator::hasChildren</span>

RecursiveRegexIterator::hasChildren
===================================

Returns whether an iterator can be obtained for the current entry

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RecursiveRegexIterator::hasChildren</span> (
<span class="methodparam">void</span> )

Returns whether an iterator can be obtained for the current entry. This
iterator can be obtained via <span
class="methodname">RecursiveRegexIterator::getChildren</span>.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if an iterator can be obtained for the current entry,
otherwise returns **`FALSE`**.

### 范例

**示例 \#1 <span
class="function">RecursiveRegexIterator::hasChildren</span> example**

``` php
<?php
$rArrayIterator = new RecursiveArrayIterator(array('test1', array('tet3', 'test4', 'test5')));
$rRegexIterator = new RecursiveRegexIterator($rArrayIterator, '/^test/',
    RecursiveRegexIterator::ALL_MATCHES);

foreach ($rRegexIterator as $value) {
    var_dump($rRegexIterator->hasChildren());
}
?>
```

以上例程会输出：

    bool(false)
    bool(true)

### 参见

-   <span class="function">RecursiveRegexIterator::getChildren</span>

简介
----

Allows iterating over a <span class="classname">RecursiveIterator</span>
to generate an ASCII graphic tree.

类摘要
------

**RecursiveTreeIterator**

<span class="ooclass"> class **RecursiveTreeIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**RecursiveIteratorIterator** </span> <span
class="oointerface">implements <span
class="interfacename">OuterIterator</span> </span> {

/\* 继承的常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveIteratorIterator::LEAVES_ONLY` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveIteratorIterator::SELF_FIRST` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveIteratorIterator::CHILD_FIRST` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveIteratorIterator::CATCH_GET_CHILD` <span class="initializer">
= 16</span> ;

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveTreeIterator::BYPASS_CURRENT` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveTreeIterator::BYPASS_KEY` <span class="initializer"> =
8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveTreeIterator::PREFIX_LEFT` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveTreeIterator::PREFIX_MID_HAS_NEXT` <span class="initializer">
= 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveTreeIterator::PREFIX_MID_LAST` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveTreeIterator::PREFIX_END_HAS_NEXT` <span class="initializer">
= 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveTreeIterator::PREFIX_END_LAST` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RecursiveTreeIterator::PREFIX_RIGHT` <span class="initializer"> =
5</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">beginChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">RecursiveIterator</span> <span
class="methodname">beginIteration</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">RecursiveIterator</span> <span
class="methodname">callGetChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">callHasChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span
class="type">RecursiveIterator\|IteratorAggregate</span> `$it`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> =
RecursiveTreeIterator::BYPASS\_KEY</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$cit_flags`<span
class="initializer"> = CachingIterator::CATCH\_GET\_CHILD</span></span>
\[, <span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> =
RecursiveIteratorIterator::SELF\_FIRST</span></span> \]\]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">endChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">endIteration</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getEntry</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getPostfix</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getPrefix</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">nextElement</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setPostfix</span> ( <span
class="methodparam"><span class="type">string</span> `$postfix`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setPrefixPart</span> ( <span
class="methodparam"><span class="type">int</span> `$part`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::beginChildren</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span
class="methodname">RecursiveIteratorIterator::beginIteration</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">RecursiveIterator</span> <span
class="methodname">RecursiveIteratorIterator::callGetChildren</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">RecursiveIteratorIterator::callHasChildren</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">RecursiveIteratorIterator::\_\_construct</span> (
<span class="methodparam"><span class="type">Traversable</span>
`$iterator`</span> \[, <span class="methodparam"><span
class="type">int</span> `$mode`<span class="initializer"> =
RecursiveIteratorIterator::LEAVES\_ONLY</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">RecursiveIteratorIterator::current</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::endChildren</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::endIteration</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RecursiveIteratorIterator::getDepth</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">iterator</span>
<span
class="methodname">RecursiveIteratorIterator::getInnerIterator</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">RecursiveIteratorIterator::getMaxDepth</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">RecursiveIterator</span> <span
class="methodname">RecursiveIteratorIterator::getSubIterator</span> (\[
<span class="methodparam"><span class="type">int</span> `$level`</span>
\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">RecursiveIteratorIterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::nextElement</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::rewind</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveIteratorIterator::setMaxDepth</span>
(\[ <span class="methodparam"><span class="type">int</span>
`$max_depth`<span class="initializer"> = -1</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RecursiveIteratorIterator::valid</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`RecursiveTreeIterator::BYPASS_CURRENT`**  

**`RecursiveTreeIterator::BYPASS_KEY`**  

**`RecursiveTreeIterator::PREFIX_LEFT`**  

**`RecursiveTreeIterator::PREFIX_MID_HAS_NEXT`**  

**`RecursiveTreeIterator::PREFIX_MID_LAST`**  

**`RecursiveTreeIterator::PREFIX_END_HAS_NEXT`**  

**`RecursiveTreeIterator::PREFIX_END_LAST`**  

**`RecursiveTreeIterator::PREFIX_RIGHT`**  

RecursiveTreeIterator::beginChildren
====================================

Begin children

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveTreeIterator::beginChildren</span> (
<span class="methodparam">void</span> )

Called when recursing one level down.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveTreeIterator::beginIteration
=====================================

Begin iteration

### 说明

<span class="modifier">public</span> <span
class="type">RecursiveIterator</span> <span
class="methodname">RecursiveTreeIterator::beginIteration</span> ( <span
class="methodparam">void</span> )

Called when iteration begins (after the first <span
class="methodname">RecursiveTreeIterator::rewind</span> call).

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

A <span class="classname">RecursiveIterator</span>.

RecursiveTreeIterator::callGetChildren
======================================

Get children

### 说明

<span class="modifier">public</span> <span
class="type">RecursiveIterator</span> <span
class="methodname">RecursiveTreeIterator::callGetChildren</span> ( <span
class="methodparam">void</span> )

Gets children of the current element.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

A <span class="classname">RecursiveIterator</span>.

RecursiveTreeIterator::callHasChildren
======================================

Has children

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RecursiveTreeIterator::callHasChildren</span> (
<span class="methodparam">void</span> )

Called for each element to test whether it has children.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if there are children, otherwise **`FALSE`**

RecursiveTreeIterator::\_\_construct
====================================

Construct a RecursiveTreeIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">RecursiveTreeIterator::\_\_construct</span> ( <span
class="methodparam"><span
class="type">RecursiveIterator\|IteratorAggregate</span> `$it`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> =
RecursiveTreeIterator::BYPASS\_KEY</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$cit_flags`<span
class="initializer"> = CachingIterator::CATCH\_GET\_CHILD</span></span>
\[, <span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> =
RecursiveIteratorIterator::SELF\_FIRST</span></span> \]\]\] )

Constructs a new <span class="classname">RecursiveTreeIterator</span>
from the supplied recursive iterator.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`it`  
The <span class="classname">RecursiveIterator</span> or <span
class="classname">IteratorAggregate</span> to iterate over.

`flags`  
Flags may be provided which will affect the behavior of some methods. A
list of the flags can found under
<a href="/spl/iterators.html#预定义常量" class="link">RecursiveTreeIterator predefined constants</a>.

`caching_it_flags`  
Flags to affect the behavior of the <span
class="classname">RecursiveCachingIterator</span> used internally.

`mode`  
Flags to affect the behavior of the <span
class="classname">RecursiveIteratorIterator</span> used internally.

### 返回值

没有返回值。

RecursiveTreeIterator::current
==============================

Get current element

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RecursiveTreeIterator::current</span> ( <span
class="methodparam">void</span> )

Gets the current element prefixed and postfixed.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns the current element prefixed and postfixed.

RecursiveTreeIterator::endChildren
==================================

End children

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveTreeIterator::endChildren</span> (
<span class="methodparam">void</span> )

Called when end recursing one level.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveTreeIterator::endIteration
===================================

End iteration

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveTreeIterator::endIteration</span> (
<span class="methodparam">void</span> )

Called when the iteration ends (when <span
class="methodname">RecursiveTreeIterator::valid</span> first returns
**`FALSE`**)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveTreeIterator::getEntry
===============================

Get current entry

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RecursiveTreeIterator::getEntry</span> ( <span
class="methodparam">void</span> )

Gets the part of the tree built for the current element.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns the part of the tree built for the current element.

RecursiveTreeIterator::getPostfix
=================================

Get the postfix

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RecursiveTreeIterator::getPostfix</span> (
<span class="methodparam">void</span> )

Gets the string to place after the current element.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns the string to place after the current element.

RecursiveTreeIterator::getPrefix
================================

Get the prefix

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RecursiveTreeIterator::getPrefix</span> ( <span
class="methodparam">void</span> )

Gets the string to place in front of current element

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns the string to place in front of current element

RecursiveTreeIterator::key
==========================

Get the key of the current element

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RecursiveTreeIterator::key</span> ( <span
class="methodparam">void</span> )

Gets the current key prefixed and postfixed.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns the current key prefixed and postfixed.

RecursiveTreeIterator::next
===========================

Move to next element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveTreeIterator::next</span> ( <span
class="methodparam">void</span> )

Moves forward to the next element.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveTreeIterator::nextElement
==================================

Next element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveTreeIterator::nextElement</span> (
<span class="methodparam">void</span> )

Called when the next element is available.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveTreeIterator::rewind
=============================

Rewind iterator

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveTreeIterator::rewind</span> ( <span
class="methodparam">void</span> )

Rewinds the iterator to the first element of the top level inner
iterator.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

RecursiveTreeIterator::setPostfix
=================================

Set postfix

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveTreeIterator::setPostfix</span> (
<span class="methodparam"><span class="type">string</span>
`$postfix`</span> )

Sets postfix as used in <span
class="methodname">RecursiveTreeIterator::getPostfix</span>.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`postfix`  

### 返回值

没有返回值。

RecursiveTreeIterator::setPrefixPart
====================================

Set a part of the prefix

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RecursiveTreeIterator::setPrefixPart</span> (
<span class="methodparam"><span class="type">int</span> `$part`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

Sets a part of the prefix used in the graphic tree.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`part`  
One of the
<a href="/spl/iterators.html#预定义常量" class="link">RecursiveTreeIterator::PREFIX_*</a>
constants.

`value`  
The value to assign to the part of the prefix specified in `part`.

### 返回值

没有返回值。

RecursiveTreeIterator::valid
============================

Check validity

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RecursiveTreeIterator::valid</span> ( <span
class="methodparam">void</span> )

Check whether the current position is valid.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the current position is valid, otherwise **`FALSE`**

简介
----

This iterator can be used to filter another iterator based on a regular
expression.

类摘要
------

**RegexIterator**

<span class="ooclass"> class **RegexIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**FilterIterator** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`MATCH` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`GET_MATCH` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ALL_MATCHES` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`SPLIT` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`REPLACE` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`USE_KEY` <span class="initializer"> = 1</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> , <span class="methodparam"><span
class="type">string</span> `$regex`</span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = self::MATCH</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$preg_flags`<span
class="initializer"> = 0</span></span> \]\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">accept</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getMode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getPregFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getRegex</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setFlags</span> ( <span
class="methodparam"><span class="type">int</span> `$flags`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setPregFlags</span> ( <span
class="methodparam"><span class="type">int</span> `$preg_flags`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="modifier">abstract</span> <span class="type">bool</span> <span
class="methodname">FilterIterator::accept</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">FilterIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">FilterIterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Iterator</span>
<span class="methodname">FilterIterator::getInnerIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">FilterIterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilterIterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">FilterIterator::rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">FilterIterator::valid</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

RegexIterator operation modes
-----------------------------

**`RegexIterator::ALL_MATCHES`**  
Return all matches for the current entry (see <span
class="function">preg\_match\_all</span>).

**`RegexIterator::GET_MATCH`**  
Return the first match for the current entry (see <span
class="function">preg\_match</span>).

**`RegexIterator::MATCH`**  
Only execute match (filter) for the current entry (see <span
class="function">preg\_match</span>).

**`RegexIterator::REPLACE`**  
Replace the current entry (see <span
class="function">preg\_replace</span>; Not fully implemented yet)

**`RegexIterator::SPLIT`**  
Returns the split values for the current entry (see <span
class="function">preg\_split</span>).

RegexIterator Flags
-------------------

**`RegexIterator::USE_KEY`**  
Special flag: Match the entry key instead of the entry value.

RegexIterator::accept
=====================

Get accept status

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RegexIterator::accept</span> ( <span
class="methodparam">void</span> )

Matches *(string)* <span
class="methodname">RegexIterator::current</span> (or <span
class="methodname">RegexIterator::key</span> if the
<a href="/spl/iterators.html#" class="link">RegexIterator::USE_KEY</a>
flag is set) against the regular expression.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if a match, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="methodname">RegexIterator::accept</span>
example**

This example shows that only items matching the regular expression are
accepted.

``` php
<?php
$names = new ArrayIterator(array('Ann', 'Bob', 'Charlie', 'David'));
$filter = new RegexIterator($names, '/^[B-D]/');
foreach ($filter as $name) {
    echo $name . PHP_EOL;
}
?>
```

以上例程会输出：

    Bob
    Charlie
    David

### 参见

-   <a href="/spl/iterators.html#预定义常量" class="link">RegexIterator constants</a>
-   <span class="methodname">RegexIterator::setFlags</span>

RegexIterator::\_\_construct
============================

Create a new RegexIterator

### 说明

<span class="modifier">public</span> <span
class="methodname">RegexIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Iterator</span>
`$iterator`</span> , <span class="methodparam"><span
class="type">string</span> `$regex`</span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = self::MATCH</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$preg_flags`<span
class="initializer"> = 0</span></span> \]\]\] )

Create a new <span class="classname">RegexIterator</span> which filters
an <span class="interfacename">Iterator</span> using a regular
expression.

### 参数

`iterator`  
The iterator to apply this regex filter to.

`regex`  
The regular expression to match.

`mode`  
Operation mode, see <span
class="methodname">RegexIterator::setMode</span> for a list of modes.

`flags`  
Special flags, see <span
class="methodname">RegexIterator::setFlags</span> for a list of
available flags.

`preg_flags`  
The regular expression flags. These flags depend on the operation mode
parameter:

| operation mode               | available flags                                     |
|------------------------------|-----------------------------------------------------|
| `RegexIterator::ALL_MATCHES` | See <span class="function">preg\_match\_all</span>. |
| `RegexIterator::GET_MATCH`   | See <span class="function">preg\_match</span>.      |
| `RegexIterator::MATCH`       | See <span class="function">preg\_match</span>.      |
| `RegexIterator::REPLACE`     | none.                                               |
| `RegexIterator::SPLIT`       | See <span class="function">preg\_split</span>.      |

### 错误／异常

Throws an <span class="classname">InvalidArgumentException</span> if the
`regex` argument is invalid.

### 范例

**示例 \#1 <span class="function">RegexIterator::\_\_construct</span>
example**

Creates a new RegexIterator that filters all strings that start with
'test'.

``` php
<?php
$arrayIterator = new ArrayIterator(array('test 1', 'another test', 'test 123'));
$regexIterator = new RegexIterator($arrayIterator, '/^test/');

foreach ($regexIterator as $value) {
    echo $value . "\n";
}
?>
```

以上例程的输出类似于：

    test 1
    test 123

### 参见

-   <span class="function">preg\_match</span>
-   <span class="function">preg\_match\_all</span>
-   <span class="function">preg\_replace</span>
-   <span class="function">preg\_split</span>

RegexIterator::getFlags
=======================

Get flags

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RegexIterator::getFlags</span> ( <span
class="methodparam">void</span> )

Returns the flags, see <span
class="methodname">RegexIterator::setFlags</span> for a list of
available flags.

### 返回值

Returns the set flags.

### 范例

**示例 \#1 <span class="methodname">RegexIterator::getFlags</span>
example**

``` php
<?php

$test = array ('str1' => 'test 1', 'teststr2' => 'another test', 'str3' => 'test 123');

$arrayIterator = new ArrayIterator($test);
$regexIterator = new RegexIterator($arrayIterator, '/^test/');
$regexIterator->setFlags(RegexIterator::USE_KEY);

if ($regexIterator->getFlags() & RegexIterator::USE_KEY) {
    echo 'Filtering based on the array keys.';
} else {
    echo 'Filtering based on the array values.';
}
?>
```

以上例程会输出：

    Filtering based on the array keys.

### 参见

-   <span class="methodname">RegexIterator::setFlags</span>

RegexIterator::getMode
======================

Returns operation mode

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RegexIterator::getMode</span> ( <span
class="methodparam">void</span> )

Returns the operation mode, see <span
class="methodname">RegexIterator::setMode</span> for the list of
operation modes.

### 返回值

Returns the operation mode.

### 范例

**示例 \#1 <span class="methodname">RegexIterator::getMode</span>
example**

``` php
<?php

$test = array ('str1' => 'test 1', 'teststr2' => 'another test', 'str3' => 'test 123');

$arrayIterator = new ArrayIterator($test);
$regexIterator = new RegexIterator($arrayIterator, '/^[a-z]+/', RegexIterator::GET_MATCH);

$mode = $regexIterator->getMode();
if ($mode & RegexIterator::GET_MATCH) {
    echo 'Getting the match for each item.';
} elseif ($mode & RegexIterator::ALL_MATCHES) {
    echo 'Getting all matches for each item.';
} elseif ($mode & RegexIterator::MATCH) {
    echo 'Getting each item if it matches.';
} elseif ($mode & RegexIterator::SPLIT) {
    echo 'Getting split pieces of each.';
}
?>
```

以上例程会输出：

    Getting the match for each item.

### 参见

-   <span class="methodname">RegexIterator::setMode</span>

RegexIterator::getPregFlags
===========================

Returns the regular expression flags

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RegexIterator::getPregFlags</span> ( <span
class="methodparam">void</span> )

Returns the regular expression flags, see <span
class="methodname">RegexIterator::\_\_construct</span> for the list of
flags.

### 返回值

Returns a bitmask of the regular expression flags.

### 范例

**示例 \#1 <span class="methodname">RegexIterator::getPregFlags</span>
example**

``` php
<?php

$test = array ('str1' => 'test 1', 'teststr2' => 'another test', 'str3' => 'test 123');

$arrayIterator = new ArrayIterator($test);
$regexIterator = new RegexIterator($arrayIterator, '/\s/', RegexIterator::SPLIT);
$regexIterator->setPregFlags(PREG_SPLIT_NO_EMPTY | PREG_SPLIT_OFFSET_CAPTURE);

if ($regexIterator->getPregFlags() & PREG_SPLIT_NO_EMPTY) {
    echo 'Ignoring empty pieces';
} else {
    echo 'Not ignoring empty pieces';
}

?>
```

以上例程会输出：

    Ignoring empty pieces

### 参见

-   <span class="methodname">RegexIterator::setPregFlags</span>

RegexIterator::getRegex
=======================

Returns current regular expression

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RegexIterator::getRegex</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

RegexIterator::setFlags
=======================

Sets the flags

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RegexIterator::setFlags</span> ( <span
class="methodparam"><span class="type">int</span> `$flags`</span> )

Sets the flags.

### 参数

`flags`  
The flags to set, a bitmask of class constants.

The available flags are listed below. The actual meanings of these flags
are described in the
<a href="/spl/iterators.html#预定义常量" class="link">predefined constants</a>.

| value | constant                                                               |
|-------|------------------------------------------------------------------------|
| 1     | <a href="/spl/iterators.html#" class="link">RegexIterator::USE_KEY</a> |

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">RegexIterator::setFlags</span>
example**

Creates a new RegexIterator that filters all entries whose key starts
with '*test*'.

``` php
<?php
$test = array ('str1' => 'test 1', 'teststr2' => 'another test', 'str3' => 'test 123');

$arrayIterator = new ArrayIterator($test);
$regexIterator = new RegexIterator($arrayIterator, '/^test/');
$regexIterator->setFlags(RegexIterator::USE_KEY);

foreach ($regexIterator as $key => $value) {
    echo $key . ' => ' . $value . "\n";
}
?>
```

以上例程会输出：

    teststr2 => another test

### 参见

-   <span class="methodname">RegexIterator::getFlags</span>

RegexIterator::setMode
======================

Sets the operation mode

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RegexIterator::setMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

Sets the operation mode.

### 参数

`mode`  
The operation mode.

The available modes are listed below. The actual meanings of these modes
are described in the
<a href="/spl/iterators.html#预定义常量" class="link">predefined constants</a>.

| value | constant                                                                   |
|-------|----------------------------------------------------------------------------|
| 0     | <a href="/spl/iterators.html#" class="link">RegexIterator::MATCH</a>       |
| 1     | <a href="/spl/iterators.html#" class="link">RegexIterator::GET_MATCH</a>   |
| 2     | <a href="/spl/iterators.html#" class="link">RegexIterator::ALL_MATCHES</a> |
| 3     | <a href="/spl/iterators.html#" class="link">RegexIterator::SPLIT</a>       |
| 4     | <a href="/spl/iterators.html#" class="link">RegexIterator::REPLACE</a>     |

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">RegexIterator::setMode</span>
example**

``` php
<?php
$test = array ('str1' => 'test 1', 'test str2' => 'another test', 'str3' => 'test 123');

$arrayIterator = new ArrayIterator($test);
// Filter everything that starts with 'test ' followed by one or more numbers.
$regexIterator = new RegexIterator($arrayIterator, '/^test (\d+)/');
// Operation mode: Replace actual value with the matches
$regexIterator->setMode(RegexIterator::GET_MATCH);

foreach ($regexIterator as $key => $value) {
    // print out the matched number(s)
    echo $key . ' => ' . $value[1] . PHP_EOL;
}
?>
```

以上例程的输出类似于：

    str1 => 1
    str3 => 123

### 参见

-   <span class="methodname">RegexIterator::getMode</span>

RegexIterator::setPregFlags
===========================

Sets the regular expression flags

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RegexIterator::setPregFlags</span> ( <span
class="methodparam"><span class="type">int</span> `$preg_flags`</span> )

Sets the regular expression flags.

### 参数

`preg_flags`  
The regular expression flags. See <span
class="methodname">RegexIterator::\_\_construct</span> for an overview
of available flags.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">RegexIterator::setPregFlags</span>
example**

Creates a new RegexIterator that filters all entries with where the
array key starts with 'test'.

``` php
<?php
$test = array ('test 1', 'another test', 'test 123');

$arrayIterator = new ArrayIterator($test);
$regexIterator = new RegexIterator($arrayIterator, '/^test/', RegexIterator::GET_MATCH);

$regexIterator->setPregFlags(PREG_OFFSET_CAPTURE);

foreach ($regexIterator as $key => $value) {
    var_dump($value);
}
?>
```

以上例程的输出类似于：

    array(1) {
      [0]=>
      array(2) {
        [0]=>
        string(4) "test"
        [1]=>
        int(0)
      }
    }
    array(1) {
      [0]=>
      array(2) {
        [0]=>
        string(4) "test"
        [1]=>
        int(0)
      }
    }

### 参见

-   <span class="methodname">RegexIterator::getPregFlags</span>
