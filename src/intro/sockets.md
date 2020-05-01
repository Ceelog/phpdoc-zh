Socket扩展是基于流行的BSD
sockets，实现了和socket通讯功能的底层接口，它可以和客户端一样当做一个socket服务器。

想了解更通用的客户端socket接口，请看 <span
class="function">stream\_socket\_client</span>, <span
class="function">stream\_socket\_server</span>, <span
class="function">fsockopen</span>, 和 <span
class="function">pfsockopen</span>。

使用这些函数时请注意，虽然他们中有很多和C函数同名的，但声明却很可能不同。未避免混淆，请仔细阅读函数描述。

不熟悉socket编程的可以在Unix手册上找到很多有用的信息，网上也有很多C
socket编程方面的教程，简单修改一下就可以应用于PHP
socket编程。<a href="http://www.unixguide.net/network/socketfaq/" class="link external">» Unix Socket FAQ</a>是一个不错的入门。
