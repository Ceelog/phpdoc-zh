PHP 内部的变化
--------------

-   <span class="simpara"> Extensions cannot override
    **zend\_execute()** any more and should override
    **zend\_execute\_ex()** instead. *EG(current\_execute\_data)* is
    already initialized in **zend\_execute\_ex()**, so for compatibility
    extensions may need to use
    *EG(current\_execute\_data)-\>prev\_execute\_data* instead. </span>
-   <span class="simpara"> 移除 *EG(arg\_types\_stack)* 、*EX(fbc)* 、
    *EX(called\_scope)* 以及*EX(current\_object)* 。 </span>
-   <span class="simpara"> Added *op\_array-\>nested\_calls*, which is
    calculated at compile time. </span>
-   <span class="simpara"> Added *EX(call\_slots)*, which is an array to
    store information about syntaticaly nested calls (e.g. *foo(bar())*)
    and is preallocated together with *execute\_data*. </span>
-   <span class="simpara"> Added *EX(call)*, which is a pointer to a
    current calling function, and is an element of *EX(call\_slots)*.
    </span>
-   <span class="simpara"> Opcodes
    <a href="/internals2/opcodes/init-method-call.html" class="link">INIT_METHOD_CALL</a>,
    <a href="/internals2/opcodes/init-static-method-call.html" class="link">ZEND_INIT_STATIC_METHOD_CALL</a>,
    <a href="/internals2/opcodes/init-fcall-by-name.html" class="link">ZEND_INIT_FCALL_BY_NAME</a>
    and
    <a href="/internals2/opcodes/init-ns-fcall-by-name.html" class="link">ZEND_INIT_NS_FCALL_BY_NAME</a>
    use *result.num* as an index in *EX(call\_slots)*. </span>
-   <span class="simpara"> Opcode
    <a href="/internals2/opcodes/new.html" class="link">ZEND_NEW</a>
    uses *extended\_value* as an index in *EX(call\_slots)*. </span>
-   <span class="simpara"> Opcodes
    <a href="/internals2/opcodes/do-fcall.html" class="link">ZEND_DO_FCALL</a>
    and
    <a href="/internals2/opcodes/do-fcall-by-name.html" class="link">ZEND_DO_FCALL_BY_NAME</a>
    use *op2.num* as an index in *EX(call\_slots)*. </span>
-   <span class="simpara"> Added *op\_array-\>used\_stack*, which is
    calculated at compile time; the corresponding stack space is
    preallocated together with *execute\_data*. As a result, the
    ZEND\_SEND\* and ZEND\_DO\_FCALL\* opcodes no longer need to check
    for stack overflow. </span>
-   <span class="simpara"> Removed *execute\_data-\>Ts* field. The VM
    temporary variables are always allocated immediately before the
    *execute\_data* structure, and are now accessed by their offset from
    the *execute\_data* base pointer instead of via
    *execute\_data-\>Ts*. The compiler stores new offsets in
    *op\_array-\>opcodes\[\*\].op?.num*. The **EX\_TMP\_VAR()** and
    **EX\_TMP\_VAR\_NUM()** macros can be used to access temporary
    variables by offset or number. You can convert the number to an
    offset using **EX\_TMP\_VAR\_NUM(0, num)** or offset to number using
    **(EX\_TMP\_VAR\_NUM(0,0)-EX\_TMP\_VAR(0,offset))**. </span>
-   <span class="simpara"> 移除 *execute\_data-\>CVs* 字段。The VM
    compiled variables are always allocated immediately after the
    *execute\_data* structure, and are now accessed by the offset from
    the *execute\_data* base pointer instead of via
    *execute\_data-\>CVs*. You can use the **EX\_CV\_NUM()** macro to
    access compiled variables by </span>
