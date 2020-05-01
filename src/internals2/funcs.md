函数的编写
==========

输出到 PHP
用户层的函数是扩展的一个核心元素。甚至在打算编写面向对象扩展时，也建议阅读此章节，其中大部分信息对于编写方法也是有效的。

给一个扩展增加函数时，例如在使用
<a href="/internals2/buildsys/skeleton.html" class="link">ext_skel</a>
脚本创建初始结构后，可创建一个函数由 C
函数来实现，然后在扩展的函数表中提供一个入口。函数入口可含有一个对参数信息结构的指针。
不是必须要提供此信息，除非打算接受参数引用或返回一个引用，及提供由 PHP
的<a href="/book/reflection.html" class="link">反射 API</a>
访问的信息。在下面例子中，参数不是作为直接函数参数传递的，而是通过一个堆栈(stack)，由函数实现——不能直接作为信息源——进行核对。

**示例 \#1 最小的仅有一个函数的 PHP 扩展**

``` c
/* {{{ proto void hello_world()
       Do nothing */
PHP_FUNCTION(hello_world)
{
}
/* }}} */

/* {{{ arginfo_hello_world */
ZEND_BEGIN_ARG_INFO(arginfo_hello_world, 0)
ZEND_END_ARG_INFO()
/* }}} */

/* {{{ demo_functions */
function_entry demo_functions[] = {
    PHP_FE(hello_world, arginfo_hello_world)
    {NULL, NULL, NULL}
}
/* }}} */

/* {{{ demo_module_enry */
zend_module_entry demo_module_entry = {
#if ZEND_MODULE_API_NO >= 20010901
    STANDARD_MODULE_HEADER,
#endif
    "demo",
    demo_functions,
    NULL,
    NULL,
    NULL,
    NULL,
    NULL,
#if ZEND_MODULE_API_NO >= 20010901
    "1.0.0",
#en
    STANDARD_MODULE_PROPERTIES
}
/* }}} */
```

在此例程中，可以你看到上面讨论的元素和模块结构。模块结构可参见
<a href="/internals2/structure/modstruct.html" class="xref">The zend_module structure</a>。

此扩展的第一部分是实际的实现内容。
按照惯例，在每一个输出的函数之前用两行注释及函数后的一行短注释来描述函数的用户层模型。

为了源代码对不同版本 PHP 提供兼容性，函数声明被包装在 `PHP_FUNCTION`
宏里。编译器的预处理器会使用 PHP 5.3 将此转换为如下函数：

    void zif_hello_world(int ht, zval *return_value, zval **return_value_ptr,
                         zval *this_ptr, int return_value_used TSRMLS_DC)
    {
    }

为预防输出至用户层的函数与其他的同名函数间的命名冲突，输出函数的 C
符号用 `zif_` 作为前缀。你也可看到，此模型没有引用参数堆栈。如果存取 PHP
传递的参数，在下面进行描述。下方表格中列举了在
`INTERNAL_FUNCTION_PARAMETERS` 宏中定义了的 C
语言级别的参数。使用所提供的宏时，请注意这些参数可能在 PHP
版本间会发生变化。

| 名称和类型                | 描述                                                         | 访问宏                 |
|---------------------------|--------------------------------------------------------------|------------------------|
| `int ht`                  | 用户实际传递参数的数量                                       | `ZEND_NUM_ARGS()`      |
| `zval *return_value`      | PHP 变量的指针，可填充返回值传递给用户。默认值是 `IS_NULL`。 | `RETVAL_*`, `RETURN_*` |
| `zval **return_value_ptr` | 当返回引用时，PHP 将其设为变量的指针。不建议返回引用。       |                        |
| `zval *this_ptr`          | 假如这是一个方法调用，其指向存放 `$this` 对象的 PHP 变量。   | `getThis()`            |
| `int return_value_used`   | 指示返回值是否会被调用者使用的标志。 caller.                 |                        |

上面所述的函数什么事都不做，只是简单地返回 NULL 给用户。从 PHP
用户层可以带任意数量的参数调用此函数。更有用的函数通常由四部分组成：

1.  局部变量定义。在 C 语言中必须在函数的开头定义局部变量。

2.  解析的参数。PHP
    传递参数到一个特殊的堆栈上，从那里对参数进行读取、校验类型，有问题时根据需要可进行转换。

3.  实际逻辑。做所需做的。

4.  设定返回值，清理，返回。

在某些情况下，这些步骤的实际顺序可能发生变化。尤其是最后两步经常颠倒，但最好保持那个顺序。

**示例 \#2 一个简单的函数**

``` c
/* {{{ proto void hello_world(string name)
   Greets a user */
PHP_FUNCTION(hello_world)
{
    char *name;
    int name_len;

    if (zend_parse_parameters(ZEND_NUM_ARGS() TSRMLS_CC, "s", &name, &name_len) == FAILURE) {
        return;
    }

    php_printf("Hello %s!", name);

    RETURN_TRUE;
}
/* }}} */
```

上面的函数展示了那些部分。让我们开始分析最后几行：`php_printf`
可以很容易的被猜到是标准的 C 语言的 `printf` 针对 PHP 的版本。与
`printf` 不同，它不是打印到进程的 `STDOUT`
通道，而是到当前的输出流，可被用户进行缓冲。要注意的是，`php_printf`
不象大部分 PHP 的 API，它不是二进制安全的。想要二进制安全输出应使用
`PHPWRITE`。

> **Note**: <span class="simpara">
> 通常来说，要直接向输出流打印数据，建议改为返回字符串数据给用户，由用户决定做什么。
> 此规则的例外情况可能是处理二进制数据（如图像）的函数，API
> 要求就在函数里提供方法来存取数据。 </span>

最后一行的 `RETURN_TRUE` 宏做了三件事：将 `return_value`
指针变量的类型设为 `IS_BOOLEAN`，并将其值设为 `true` 值。然后从 C
函数中返回。所以当使用此宏时，你就是内存和要结束的其他资源的管家，此函数不会执行其后的代码。

`zend_parse_parameters()`
函数负责读取用户从参数堆栈传递来参数，并将其适当地转换后放入局部 C
语言变量。如果用户传递的参数个数有误或类型不可被转换，
函数会发出一个冗长的错误信息，并返回 `FAILURE`。
当从函数简单返回的情况下——不修改 `return_value`，将默认的返回值 `NULL`
返回给用户。

> **Note**: <span class="simpara"> 请注意，`FAILURE` 表示为
> `-1`，`SUCCESS` 表示为
> `0`。为了使代码清晰，应总是使用已命名的常量而不是其值。 </span>

传递给 `zend_parse_parameters()`
的第一个参数是用户实际传递到函数的参数数量。此数值做为 `ht`
参数传给函数，但就像上面讨论的那样，应使用做为实现细节的
`ZEND_NUM_ARGS()`。

为了与 PHP 的线程隔离、线程安全资源管理器兼容，还要用 `TSRMLS_CC`
传递线程上下文。与其他函数不同，它不能是最后的参数，因为在
`zend_parse_parameters`
内要求有不定数量的参数——依赖于要读取的用户参数的数量。

在线程上下文之后定义所要求的参数。每个参数都由字符串中的一个字符表示其类型。
如果希望一个字符串参数，则在此类型说明只不过是个 `"s"`。

最后一个是传递一个或多个指针给要填充变量值的 C
变量，或提供更多细节。比如字符串，事实上的字符串，总是以 NULL 结尾，以
`char*`，且其长度是除 NULL 字节外的 `int` 型值。

相关所有类型说明符和对应的附加的 C
语言类型的文档可在源代码发布包中的文件 `README.PARAMETER_PARSING_API`
中找到。大多数重要类型可见下表。

| 修饰符 | 附加参数的类型 | 描述              |
|--------|----------------|-------------------|
| `b`    | `zend_bool`    | Boolean 值        |
| `l`    | `long`         | integer (long) 值 |
| `d`    | `double`       | float (double) 值 |
| `s`    | `char*, int`   | 二进制的安全串    |
| `h`    | `HashTable*`   | 数组的哈希表      |
