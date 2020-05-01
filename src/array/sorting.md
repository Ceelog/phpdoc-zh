对数组进行排序
==============

PHP 有一些用来排序数组的函数， 这个文档会把它们列出来。

主要区别有：

-   有些函数基于 <span class="type">array</span> 的键来排序，
    而其他的基于值来排序的：*$array\['key'\] = 'value';*。
-   排序之后键和值之间的关联关系是否能够保持， 是指排序之后数组的键可能
    会被重置为数字型的（0,1,2 ...）。
-   排序的顺序有：字母表顺序， 由低到高（升序），
    由高到低（降序），数字排序，自然排序，随机顺序或者用户自定义排序。
-   注意：下列的所有排序函数都是直接作用于数组本身，
    而不是返回一个新的有序的数组。
-   以下函数对于数组中相等的元素，它们在排序后的顺序是未定义的。
    （也即相等元素之间的顺序是不稳定的）。

| 函数名称                                       | 排序依据 | 数组索引键保持                   | 排序的顺序               | 相关函数                                  |
|------------------------------------------------|----------|----------------------------------|--------------------------|-------------------------------------------|
| <span class="function">array\_multisort</span> | 值       | 键值关联的保持，数字类型的不保持 | 第一个数组或者由选项指定 | <span class="function">array\_walk</span> |
| <span class="function">asort</span>            | 值       | 是                               | 由低到高                 | <span class="function">arsort</span>      |
| <span class="function">arsort</span>           | 值       | 是                               | 由高到低                 | <span class="function">asort</span>       |
| <span class="function">krsort</span>           | 键       | 是                               | 由高到低                 | <span class="function">ksort</span>       |
| <span class="function">ksort</span>            | 键       | 是                               | 由低到高                 | <span class="function">asort</span>       |
| <span class="function">natcasesort</span>      | 值       | 是                               | 自然排序，大小写不敏感   | <span class="function">natsort</span>     |
| <span class="function">natsort</span>          | 值       | 是                               | 自然排序                 | <span class="function">natcasesort</span> |
| <span class="function">rsort</span>            | 值       | 否                               | 由高到低                 | <span class="function">sort</span>        |
| <span class="function">shuffle</span>          | 值       | 否                               | 随机                     | <span class="function">array\_rand</span> |
| <span class="function">sort</span>             | 值       | 否                               | 由低到高                 | <span class="function">rsort</span>       |
| <span class="function">uasort</span>           | 值       | 是                               | 由用户定义               | <span class="function">uksort</span>      |
| <span class="function">uksort</span>           | 键       | 是                               | 由用户定义               | <span class="function">uasort</span>      |
| <span class="function">usort</span>            | 值       | 否                               | 由用户定义               | <span class="function">uasort</span>      |
