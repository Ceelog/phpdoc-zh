Socket Errors
=============

Socket扩展编写的目的是提供一个面向功能强大的BSD
Socket的可用的接口。它能确保这些函数在Win32和Unix平台上都能很好的工作。
在特定条件下，大部分socket函数如果发生错误都会发出一个
**`E_WARNING`**信息描述错误内容。有时可能并不会如开发者所愿。例如，因为连接突然中断，
<span class="function">socket\_read</span>函数可能会突然发出一个
**`E_WARNING`**。 通常会使用*@*操作符来压制异常，然后在程序中用<span
class="function">socket\_last\_error</span>来捕获错误代码。
你可以调用<span
class="function">socket\_strerror</span>函数通过错误代码获取错误描述。查看函数描述获取更多信息。

> **Note**:
>
> Socket扩展发出的**`E_WARNING`**信息都是英文的，但获取到的错误描述会根据当前的locale展示。
> (**`LC_MESSAGES`**):
>
>     Warning - socket_bind() unable to bind address [98]: Die Adresse wird bereits verwendet
