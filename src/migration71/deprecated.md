PHP 7.1.x 中废弃的特性
----------------------

### ext/mcrypt

mcrypt 扩展已经过时了大约10年，并且用起来很复杂。因此它被废弃并且被
OpenSSL 所取代。 从PHP 7.2起它将被从核心代码中移除并且移到PECL中。

### <span class="function">mb\_ereg\_replace</span>和<span class="function">mb\_eregi\_replace</span>的Eval选项

对于<span class="function">mb\_ereg\_replace</span>和<span
class="function">mb\_eregi\_replace</span>的 *e*模式修饰符现在已被废弃。
