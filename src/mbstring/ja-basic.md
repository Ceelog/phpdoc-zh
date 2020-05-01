日文字符多字节编码基础
======================

日文字符只能使用多字节编码，而且，编码规范取决于平台和字符的使用
目的（text purpose)。跟糟糕的是，编码规范之间还稍有差异。为了开发
出适应日文环境的Web应用，开发人员必须对编码规范有个清晰的认识，确保
使用了合适的编码规范。

-   <span class="simpara">存储一个日文字符最大需要6个字节空间</span>
-   <span class="simpara">
    多数日文多字节字符是单字节字符出现频率的两倍。这些字符被称为
    "zen-kaku"，在日文中代表的意思是"full width"。
    其它窄一些的字符被称作"han-kaku"，意思是"half width"。
    字符实际显示的宽度，取决于显示时使用的字体。 </span>
-   <span class="simpara"> 有些字符编码采用ISO-2022定义的转码序列（shift
    sequences) 来转换特殊的编码 空间(*00h* to *7fh*)。 </span>
-   <span class="simpara"> 在SMTP/NNTP协议应用中 建议
    采用ISO-2022-JP编码，并且头部和实体部分，应该按照
    RFC要求重新编码。虽然这些并不是强制性要求，但最好还是按这个建议做，因为几款
    流行的客户端不支持其他的编码方式。 </span>
-   <span class="simpara">
    手机服务页面，例如<a href="http://www.nttdocomo.com/services/imode/" class="link external">» i-mode</a>或者<a href="http://www.au.kddi.com/english/service/ezweb/index.html" class="link external">» EZweb</a>
    应该 使用Shift\_JIS编码。 </span>
-   <span class="simpara"> 从PHP 5.4.0开始，象形字符（pictogram
    characters ）已经可以支持像
    <a href="http://www.nttdocomo.com/services/imode/" class="link external">» i-mode</a>
    或者
    <a href="http://www.au.kddi.com/english/service/ezweb/index.html" class="link external">» EZweb</a>
    这样的手机服务。 </span>
