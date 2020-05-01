PHP标准库 (SPL)
===============

**目录**

-   [简介](/intro/spl.html)
-   [安装／配置](/spl/setup.html)
    -   [需求](/spl/setup.html#需求)
    -   [安装](/spl/setup.html#安装)
    -   [运行时配置](/spl/setup.html#运行时配置)
    -   [资源类型](/spl/setup.html#资源类型)
-   [预定义常量](/spl/constants.html)
-   [数据结构](/spl/datastructures.html)
    -   [SplDoublyLinkedList](/spl/datastructures.html#SplDoublyLinkedList)
        — The SplDoublyLinkedList class
    -   [SplStack](/spl/datastructures.html#SplStack) — The SplStack
        class
    -   [SplQueue](/spl/datastructures.html#SplQueue) — The SplQueue
        class
    -   [SplHeap](/spl/datastructures.html#SplHeap) — The SplHeap class
    -   [SplMaxHeap](/spl/datastructures.html#SplMaxHeap) — The
        SplMaxHeap class
    -   [SplMinHeap](/spl/datastructures.html#SplMinHeap) — The
        SplMinHeap class
    -   [SplPriorityQueue](/spl/datastructures.html#SplPriorityQueue) —
        The SplPriorityQueue class
    -   [SplFixedArray](/spl/datastructures.html#SplFixedArray) — The
        SplFixedArray class
    -   [SplObjectStorage](/spl/datastructures.html#SplObjectStorage) —
        The SplObjectStorage class
-   [迭代器](/spl/iterators.html)
    -   [AppendIterator](/spl/iterators.html#AppendIterator) — The
        AppendIterator class
    -   [ArrayIterator](/spl/iterators.html#ArrayIterator) —
        ArrayIterator 类
    -   [CachingIterator](/spl/iterators.html#CachingIterator) — The
        CachingIterator class
    -   [CallbackFilterIterator](/spl/iterators.html#CallbackFilterIterator)
        — The CallbackFilterIterator class
    -   [DirectoryIterator](/spl/iterators.html#DirectoryIterator) — The
        DirectoryIterator class
    -   [EmptyIterator](/spl/iterators.html#EmptyIterator) — The
        EmptyIterator class
    -   [FilesystemIterator](/spl/iterators.html#FilesystemIterator) —
        The FilesystemIterator class
    -   [FilterIterator](/spl/iterators.html#FilterIterator) — The
        FilterIterator class
    -   [GlobIterator](/spl/iterators.html#GlobIterator) — The
        GlobIterator class
    -   [InfiniteIterator](/spl/iterators.html#InfiniteIterator) — The
        InfiniteIterator class
    -   [IteratorIterator](/spl/iterators.html#IteratorIterator) — The
        IteratorIterator class
    -   [LimitIterator](/spl/iterators.html#LimitIterator) — The
        LimitIterator class
    -   [MultipleIterator](/spl/iterators.html#MultipleIterator) — The
        MultipleIterator class
    -   [NoRewindIterator](/spl/iterators.html#NoRewindIterator) — The
        NoRewindIterator class
    -   [ParentIterator](/spl/iterators.html#ParentIterator) — The
        ParentIterator class
    -   [RecursiveArrayIterator](/spl/iterators.html#RecursiveArrayIterator)
        — The RecursiveArrayIterator class
    -   [RecursiveCachingIterator](/spl/iterators.html#RecursiveCachingIterator)
        — The RecursiveCachingIterator class
    -   [RecursiveCallbackFilterIterator](/spl/iterators.html#RecursiveCallbackFilterIterator)
        — The RecursiveCallbackFilterIterator class
    -   [RecursiveDirectoryIterator](/spl/iterators.html#RecursiveDirectoryIterator)
        — The RecursiveDirectoryIterator class
    -   [RecursiveFilterIterator](/spl/iterators.html#RecursiveFilterIterator)
        — The RecursiveFilterIterator class
    -   [RecursiveIteratorIterator](/spl/iterators.html#RecursiveIteratorIterator)
        — The RecursiveIteratorIterator class
    -   [RecursiveRegexIterator](/spl/iterators.html#RecursiveRegexIterator)
        — The RecursiveRegexIterator class
    -   [RecursiveTreeIterator](/spl/iterators.html#RecursiveTreeIterator)
        — The RecursiveTreeIterator class
    -   [RegexIterator](/spl/iterators.html#RegexIterator) — The
        RegexIterator class
-   [接口](/spl/interfaces.html)
    -   [Countable](/spl/interfaces.html#Countable) — The Countable
        interface
    -   [OuterIterator](/spl/interfaces.html#OuterIterator) — The
        OuterIterator interface
    -   [RecursiveIterator](/spl/interfaces.html#RecursiveIterator) —
        The RecursiveIterator interface
    -   [SeekableIterator](/spl/interfaces.html#SeekableIterator) — The
        SeekableIterator interface
-   [异常](/spl/exceptions.html)
    -   [BadFunctionCallException](/spl/exceptions.html#BadFunctionCallException)
        — The BadFunctionCallException class
    -   [BadMethodCallException](/spl/exceptions.html#BadMethodCallException)
        — The BadMethodCallException class
    -   [DomainException](/spl/exceptions.html#DomainException) — The
        DomainException class
    -   [InvalidArgumentException](/spl/exceptions.html#InvalidArgumentException)
        — The InvalidArgumentException class
    -   [LengthException](/spl/exceptions.html#LengthException) — The
        LengthException class
    -   [LogicException](/spl/exceptions.html#LogicException) — The
        LogicException class
    -   [OutOfBoundsException](/spl/exceptions.html#OutOfBoundsException)
        — The OutOfBoundsException class
    -   [OutOfRangeException](/spl/exceptions.html#OutOfRangeException)
        — The OutOfRangeException class
    -   [OverflowException](/spl/exceptions.html#OverflowException) —
        The OverflowException class
    -   [RangeException](/spl/exceptions.html#RangeException) — The
        RangeException class
    -   [RuntimeException](/spl/exceptions.html#RuntimeException) — The
        RuntimeException class
    -   [UnderflowException](/spl/exceptions.html#UnderflowException) —
        The UnderflowException class
    -   [UnexpectedValueException](/spl/exceptions.html#UnexpectedValueException)
        — The UnexpectedValueException class
-   [SPL 函数](/ref/spl.html)
    -   [class\_implements](/ref/spl.html#class_implements) —
        返回指定的类实现的所有接口。
    -   [class\_parents](/ref/spl.html#class_parents) —
        返回指定类的父类。
    -   [class\_uses](/ref/spl.html#class_uses) — Return the traits used
        by the given class
    -   [iterator\_apply](/ref/spl.html#iterator_apply) —
        为迭代器中每个元素调用一个用户自定义函数
    -   [iterator\_count](/ref/spl.html#iterator_count) —
        计算迭代器中元素的个数
    -   [iterator\_to\_array](/ref/spl.html#iterator_to_array) —
        将迭代器中的元素拷贝到数组
    -   [spl\_autoload\_call](/ref/spl.html#spl_autoload_call) —
        尝试调用所有已注册的\_\_autoload()函数来装载请求类
    -   [spl\_autoload\_extensions](/ref/spl.html#spl_autoload_extensions)
        — 注册并返回spl\_autoload函数使用的默认文件扩展名。
    -   [spl\_autoload\_functions](/ref/spl.html#spl_autoload_functions)
        — 返回所有已注册的\_\_autoload()函数。
    -   [spl\_autoload\_register](/ref/spl.html#spl_autoload_register) —
        注册给定的函数作为 \_\_autoload 的实现
    -   [spl\_autoload\_unregister](/ref/spl.html#spl_autoload_unregister)
        — 注销已注册的\_\_autoload()函数
    -   [spl\_autoload](/ref/spl.html#spl_autoload) —
        \_\_autoload()函数的默认实现
    -   [spl\_classes](/ref/spl.html#spl_classes) — 返回所有可用的SPL类
    -   [spl\_object\_hash](/ref/spl.html#spl_object_hash) —
        返回指定对象的hash id
    -   [spl\_object\_id](/ref/spl.html#spl_object_id) — Return the
        integer object handle for given object
-   [文件处理](/spl/files.html)
    -   [SplFileInfo](/spl/files.html#SplFileInfo) — The SplFileInfo
        class
    -   [SplFileObject](/spl/files.html#SplFileObject) — The
        SplFileObject class
    -   [SplTempFileObject](/spl/files.html#SplTempFileObject) — The
        SplTempFileObject class
-   [各种类及接口](/spl/misc.html)
    -   [ArrayObject](/spl/misc.html#ArrayObject) — The ArrayObject
        class
    -   [SplObserver](/spl/misc.html#SplObserver) — The SplObserver
        interface
    -   [SplSubject](/spl/misc.html#SplSubject) — The SplSubject
        interface
