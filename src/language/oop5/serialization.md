对象序列化
----------

序列化对象 - 在会话中存放对象
-----------------------------

所有php里面的值都可以使用函数<span
class="function">serialize</span>来返回一个包含字节流的字符串来表示。<span
class="function">unserialize</span>函数能够重新把字符串变回php原来的值。
序列化一个对象将会保存对象的所有变量，但是不会保存对象的方法，只会保存类的名字。

为了能够<span
class="function">unserialize</span>一个对象，这个对象的类必须已经定义过。如果序列化类A的一个对象，将会返回一个跟类A相关，而且包含了对象所有变量值的字符串。
如果要想在另外一个文件中解序列化一个对象，这个对象的类必须在解序列化之前定义，可以通过包含一个定义该类的文件或使用函数<span
class="function">spl\_autoload\_register</span>来实现。

``` php
<?php
// classa.inc:
  
  class A {
      public $one = 1;
    
      public function show_one() {
          echo $this->one;
      }
  }
  
// page1.php:

  include("classa.inc");
  
  $a = new A;
  $s = serialize($a);
  // 把变量$s保存起来以便文件page2.php能够读到
  file_put_contents('store', $s);

// page2.php:
  
  // 要正确了解序列化，必须包含下面一个文件
  include("classa.inc");

  $s = file_get_contents('store');
  $a = unserialize($s);

  // 现在可以使用对象$a里面的函数 show_one()
  $a->show_one();
?>
```

当一个应用程序使用函数<span
class="function">session\_register</span>来保存对象到会话中时，在每个页面结束的时候这些对象都会自动序列化，而在每个页面开始的时候又自动解序列化。
所以一旦对象被保存在会话中，整个应用程序的页面都能使用这些对象。但是，<span
class="function">session\_register</span>在php5.4.0之后被移除了。

在应用程序中序列化对象以便在之后使用，强烈推荐在整个应用程序都包含对象的类的定义。
不然有可能出现在解序列化对象的时候，没有找到该对象的类的定义，从而把没有方法的类<span
class="classname">\_\_PHP\_Incomplete\_Class\_Name</span>作为该对象的类，导致返回一个没有用的对象。

所以在上面的例子中，当运行*session\_register("a")*，把变量`$a`放在会话里之后，需要在每个页面都包含文件*classa.inc*，而不是只有文件`page1.php`和`page2.php`。

除了以上建议，可以在对象上使用
<a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>
和
<a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>
方法对序列化/反序列化事件挂载钩子。 使用
<a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>
也能够让仅仅序列化对象的某些属性。
