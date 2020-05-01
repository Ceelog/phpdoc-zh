方法修饰符
==========

**Warning**

仅适用于 pthreads v2。在 pthreads v3 中已经被移除。

pthreads 将会改写标明为 protected 和 private
的方法来提供更加适合多线程环境的对象。 对于所有的 Threaded
对象，pthreads 都会进行改写操作。

**示例 \#1 protected 方法示例： 标记为 protected
的方法在同一时间仅允许一个线程访问**

``` php
<?php
class ExampleThread extends Thread {
    public function run() {
        /* thread code */
        if ($this->synchronized()) {

        }
    }

    protected function exclusive() {
        /* synchronized method */
    }
}

$thread = new ExampleThread();
if ($thread->start()) {
    $thread->exclusive();
}
?>
```

**示例 \#2 private 方法示例：标记为 private
的方法只能由创建该对象的线程调用**

``` php
<?php
class ExampleThread extends Thread {
    public function run() {
        /* thread code */
        if ($this->insideonly()) {

        }
    }

    private function insideonly() {
        /* private method */
    }
}

$thread = new ExampleThread();
if ($thread->start()) {
    $thread->insideonly();
}
?>
```
