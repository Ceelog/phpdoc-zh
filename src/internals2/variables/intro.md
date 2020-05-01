介绍
----

为了在 PHP 核心中使用变量，就必须要学会 PHP
所使用的基本概念的差异。首先，PHP 是一门动态的弱类型语言。其次，PHP
的写机制里会使用内存处理的引用计数的复本。请查阅<a href="/features/gc/refcounting-basics.html" class="xref">引用计数基本知识</a>
章节以获得如何使用计数和引用的细节。

PHP
变量，通常来说，由两部分组成：标签（例如，可能是符号表中的一个条目）和实际变量容器。在此手册的绝大部分内容中都是针对变量容器。

变量容器，在代码中称为 `zval`，掌握了所需处理变量的所有数据。
包括实际值、当前类型、统计指向此容器的标签的数量，和指示这些标签是引用还是副本的标志。
在 PHP 5.3 中，有关结构可在 `Zend/zend.h` 中找到，类似于：

    typedef struct _zval_struct zval;

    typedef union _zvalue_value {
        long lval;                 /* long value */
        double dval;               /* double value */
        struct {                   /* string type */
            char *val;
            int len;
        } str;
        HashTable *ht;             /* hash table value */
        zend_object_value obj;
    } zvalue_value;
     
    struct _zval_struct {
        /* Variable information */
        zvalue_value value;        /* value */
        zend_uint refcount__gc;
        zend_uchar type;           /* active type */
        zend_uchar is_ref__gc;
    };

在 `zvalue_value`
中，通过名称和注释可清楚地找到字段所使用的不同类型的内部表现形式——尤其是当你知道
PHP 数组实际上是哈希表时。但是，其中也遗漏了几种 PHP 类型：`NULL`,
`boolean` 和 `resources`。`NULL` 不需要值，`NULL` 就是此类型的值。对
`boolean` 和 `resource` 的值来说，PHP 也使用值字段。比如 `boolean`
值，为 `false` 时存放 `0`，为 `true` 时存放 `1`。`resource`
类型的变量存放的是资源的 id。

现在，有个好消息是你不需要知道这些细节，因为在 PHP
中总是使用宏；坏消息是有很多宏： 有直接存取 `zval` 的宏，还有经常是指向
`zval` 的指针，甚至是指向 `zval`
的指针的指针，大多数宏都有引用这些指针的捷径。这些宏分布于
`Zend/zend.h`, `Zend/zend_operators.h` 和 `Zend/zend_API.h` 之中。
