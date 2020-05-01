Inotify 扩展提供了一系列 inotify 函数： <span
class="function">inotify\_init</span>、 <span
class="function">inotify\_add\_watch</span> 、 <span
class="function">inotify\_rm\_watch</span>。

类似 C 语言里的 <span class="function">inotify\_init</span>
函数会返回文件描述符，PHP 的 <span
class="function">inotify\_init</span>则返回 stream 资源。可以被标准的
Steam 函数使用，例如 <span class="function">stream\_select</span>、
<span class="function">stream\_set\_blocking</span> 以及 <span
class="function">fclose</span>。 <span
class="function">inotify\_read</span> 函数取代里 C 语言里读取 inotify
事件的那种方式。
