"counter" 扩展 - 一个连续的实例
===============================

**目录**

-   [安装／配置](/internals2/counter/setup.html)
    -   [简介](/internals2/counter/intro.html)
    -   [运行时配置](/internals2/counter/ini.html)
    -   [资源类型](/internals2/counter/resources.html)
-   [预定义常量](/internals2/counter/constants.html)
-   [范例](/internals2/counter/examples.html)
    -   [简单接口](/internals2/counter/examples/basic.html)
    -   [扩展接口](/internals2/counter/examples/extended.html)
    -   [对象化接口](/internals2/counter/examples/objective.html)
-   [Counter](/internals2/counter/counter-class.html) — Counter 类
    -   [Counter::\_\_construct](/internals2/counter/counter-class/construct.html)
        — 创建一个包含单一数值的计数器实例。
    -   [Counter::getValue](/internals2/counter/counter-class/getValue.html)
        — 获取计数器的当前值。
    -   [Counter::bumpValue](/internals2/counter/counter-class/bumpValue.html)
        — 修改计数器的当前值。
    -   [Counter::resetValue](/internals2/counter/counter-class/resetValue.html)
        — 重置计数器的当前值。
    -   [Counter::getMeta](/internals2/counter/counter-class/getMeta.html)
        — 返回计数器的部分元信息。
    -   [Counter::getNamed](/internals2/counter/counter-class/getNamed.html)
        — 取回一个名称已存在的计数器。
    -   [Counter::setCounterClass](/internals2/counter/counter-class/setCounterClass.html)
        — 设置由 Counter::getNamed 返回的计数器类。
-   [Basic](/internals2/counter/basic-interface.html) — 简单接口
    -   [counter\_get](/internals2/counter/function/counter-get.html) —
        获取简单计数器的当前值。
    -   [counter\_bump](/internals2/counter/function/counter-bump.html)
        — 修改简单计数器的当前值。
    -   [counter\_reset](/internals2/counter/function/counter-reset.html)
        — 重置简单计数器的当前值。
-   [Extended](/internals2/counter/extended-interface.html) — 扩展接口
    -   [counter\_create](/internals2/counter/function/counter-create.html)
        — 创建一个包含单个数值的计数器。
    -   [counter\_get\_value](/internals2/counter/function/counter-get-value.html)
        — 获取计数器资源的当前值。
    -   [counter\_bump\_value](/internals2/counter/function/counter-bump-value.html)
        — 更新计数器资源的当前值。
    -   [counter\_reset\_value](/internals2/counter/function/counter-reset-value.html)
        — 重置计数器资源的当前值。
    -   [counter\_get\_meta](/internals2/counter/function/counter-get-meta.html)
        — 返回计数器资源的部分元信息。
    -   [counter\_get\_named](/internals2/counter/function/counter-get-named.html)
        — 按名称查询一个已存在的计数器，并作为资源返回。

贯穿于整个 Zend 文档之中，参考文档中制作了一个实例模块用来阐述各种概念。
“counter”扩展就是这样一个范例，为了阐述各种概念，通过一个假定的但起作用的
Zend 模块，争取在合理情况下地尽可能多地使用 Zend
API。这个短章节描述了整个扩展的用户接口。

> **Note**: <span class="simpara">
> “counter”没有任何实际用途，所提供的功能就是来提供极为有效的通过适当的用户库实现的代码。
> </span>
