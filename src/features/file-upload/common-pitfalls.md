常见缺陷
--------

对 *MAX\_FILE\_SIZE* 设置的值，不能大于 ini 设置中
<a href="/ini/core.html#ini.upload-max-filesize" class="link">upload_max_filesize</a>
选项设置的值。其默认值为 2M 字节。

如果内存限制设置被激活，可能需要将
<a href="/ini/core.html#ini.memory-limit" class="link">memory_limit</a>
设置的更大些，请确认
<a href="/ini/core.html#ini.memory-limit" class="link">memory_limit</a>
的设置足够的大。

如果 <a href="/info/setup.html#" class="link">max_execution_time</a>
设置的值太小，脚本运行的时间可能会超过该设置。因此，也请保证
*max\_execution\_time* 足够的大。

> **Note**: <span class="simpara">
> <a href="/info/setup.html#" class="link">max_execution_time</a>
> 仅仅只影响脚本本身运行的时间。任何其它花费在脚本运行之外的时间，诸如用函数
> <span class="function">system</span> 对系统的调用、<span
> class="function">sleep</span>
> 函数的使用、数据库查询、文件上传等，在计算脚本运行的最大时间时都不包括在内。
> </span>

**Warning**

<a href="/info/setup.html#" class="link">max_input_time</a>
以秒为单位设定了脚本接收输入的最大时间，包括文件上传。对于较大或多个文件，或者用户的网速较慢时，可能会超过默认的
*60 秒*。

如果
<a href="/ini/core.html#ini.post-max-size" class="link">post_max_size</a>
设置的值太小，则较大的文件会无法被上传。因此，请保证 *post\_max\_size*
的值足够的大。

不对正在操作的文件进行验证可能意味着用户能够访问其它目录下的敏感信息。

请注意 <span class="productname">CERN httpd</span>
似乎会丢弃它从客户端获得的 content-type mime
头信息中第一个空格后所有的内容，基于这一点，<span
class="productname">CERN httpd</span> 不支持文件上传特性。

鉴于文件路径的表示方法有很多种，我们无法确保用使用各种外语的文件名（尤其是包含空格的）能够被正确的处理。

开发人员不应将普通的输入字段和文件上传的字段混用同一个表单变量（例如都用
*foo\[\]*）。
