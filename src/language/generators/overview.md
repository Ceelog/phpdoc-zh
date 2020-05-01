生成器总览
----------

生成器提供了一种更容易的方法来实现简单的<a href="/language/oop5/iterations.html" class="link">对象迭代</a>，相比较定义类实现
<span class="classname">Iterator</span>
接口的方式，性能开销和复杂性大大降低。

生成器允许你在
<a href="/control-structures/foreach.html" class="link">foreach</a>
代码块中写代码来迭代一组数据而不需要在内存中创建一个数组,
那会使你的内存达到上限，或者会占据可观的处理时间。相反，你可以写一个生成器函数，就像一个普通的自定义<a href="/functions/user-defined.html" class="link">函数</a>一样,
和普通函数只<a href="/functions/returning-values.html" class="link">返回</a>一次不同的是,
生成器可以根据需要
<a href="/language/generators/syntax.html#control-structures.yield" class="link">yield</a>
多次，以便生成需要迭代的值。

一个简单的例子就是使用生成器来重新实现 <span
class="function">range</span> 函数。 标准的 <span
class="function">range</span>
函数需要在内存中生成一个数组包含每一个在它范围内的值，然后返回该数组,
结果就是会产生多个很大的数组。 比如，调用 **range(0, 1000000)**
将导致内存占用超过 100 MB。

做为一种替代方法, 我们可以实现一个 *xrange()* 生成器,
只需要足够的内存来创建 <span class="classname">Iterator</span>
对象并在内部跟踪生成器的当前状态，这样只需要不到1K字节的内存。

**示例 \#1 将 <span class="function">range</span> 实现为生成器**

``` php
<?php
function xrange($start, $limit, $step = 1) {
    if ($start < $limit) {
        if ($step <= 0) {
            throw new LogicException('Step must be +ve');
        }

        for ($i = $start; $i <= $limit; $i += $step) {
            yield $i;
        }
    } else {
        if ($step >= 0) {
            throw new LogicException('Step must be -ve');
        }

        for ($i = $start; $i >= $limit; $i += $step) {
            yield $i;
        }
    }
}

/* 
 * 注意下面range()和xrange()输出的结果是一样的。
 */

echo 'Single digit odd numbers from range():  ';
foreach (range(1, 9, 2) as $number) {
    echo "$number ";
}
echo "\n";

echo 'Single digit odd numbers from xrange(): ';
foreach (xrange(1, 9, 2) as $number) {
    echo "$number ";
}
?>
```

以上例程会输出：

    Single digit odd numbers from range():  1 3 5 7 9 
    Single digit odd numbers from xrange(): 1 3 5 7 9 

### <span class="classname">Generator</span> objects

When a generator function is called for the first time, an object of the
internal <span class="classname">Generator</span> class is returned.
This object implements the <span class="classname">Iterator</span>
interface in much the same way as a forward-only iterator object would,
and provides methods that can be called to manipulate the state of the
generator, including sending values to and returning values from it.
