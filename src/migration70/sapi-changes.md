SAPI 模块的变化
---------------

### <a href="/book/fpm.html" class="link">FPM</a>

#### <a href="/install/fpm/configuration.html#listen" class="link">listen</a> 端口现在同时监听 IPv4 和 IPv6 地址。

在 PHP 5
中，<a href="/install/fpm/configuration.html#listen" class="link">listen</a>
指令如果仅带一个端口数字， 则会监听所有网络接口，但只是 IPv4。 现在 PHP
7 会同时接受来自 IPv4 和 IPv6 上的请求。

指定了 ip 地址后不受此影响；它们会继续仅仅监听在指定的地址和协议上。
