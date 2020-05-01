当PHP脚本有输出时，输出控制函数可以用这些来控制输出。这在多种不同情况中非常有用，尤其是用来在脚本开始输出
数据后，发送http头信息到浏览器。输出控制函数不影响由 <span
class="function">header</span> 或 <span
class="function">setcookie</span>发送的文件头信息，仅影响象 <span
class="function">echo</span>这样的函数和PHP代码块间的数据。

> **Note**:
>
> 由于早先的版本的缺陷，当从PHP4.1.x(4.2.x,4.3.x)升级时，必须保证`php.ini`中的*implicit\_flush*
> 是 *OFF*， 否则任何用<span
> class="function">ob\_start</span>的输出将在输出中隐藏掉。
