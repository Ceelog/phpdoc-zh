预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

Mcrypt 支持以下四种分组密码模式：*CBC*， *OFB*，*CFB* 和 *ECB*。
如果使用 libmcrypt-2.4.x 或更高版本链接， 还可以支持 *nOFB* 分组模式 和
*STREAM* 模式。 下列是所支持的加密模式以及其对应的预定义常量。
完整的参考见：Applied Cryptography by Schneier (ISBN 0-471-11709-9)。

-   <span class="simpara"> **`MCRYPT_MODE_ECB`** (*electronic codebook*)
    是一种分组加密模式，但是它无法适用于大部分场景，
    所以不建议使用这种模式进行分组加密。 </span>
-   <span class="simpara"> **`MCRYPT_MODE_CBC`** (*cipher block
    chaining*) 也是一种分组加密方式， 相对 *ECB* 模式，它更加安全。
    </span>
-   <span class="simpara"> **`MCRYPT_MODE_CFB`** (*8 比特模式的 cipher
    feedback*) 是一种流式加密模式。 相对于 *CFB* 而言， 推荐使用 *NCFB*
    模式。 </span>
-   <span class="simpara"> **`MCRYPT_MODE_OFB`** (*output feedback, in
    8bit*) 和 *CFB* 类似，
    也是一种流式加密模式，它可以用在无法容忍加密错误传播的应用中。
    推荐使用 *NOFB* 模式，而不是 *OFB* 模式。 </span>
-   <span class="simpara"> **`MCRYPT_MODE_NOFB`** (*output feedback, in
    nbit*) 和 *OFB* 类似，但是更加安全，
    因为它可以按照算法指定的分组大小来对数据进行加密。 </span>
-   <span class="simpara"> **`MCRYPT_MODE_STREAM`** 是一种扩展模式，
    它包含了诸如 *"WAKE"* 或 *"RC4"* 的流加密算法。 </span>

Mcrypt 还支持一些尚未预定义常量的加密模式。
可以通过传入一个字符串来使用使用未预定义常量的加密模式。

-   <span class="simpara"> **`"ctr"`** (*counter mode*)
    是一种流式加密模式。 </span>
-   <span class="simpara"> **`"ncfb"`** (*cipher feedback, in n-bit
    mode*)，类似于 *CFB* 模式， 但是它会对于算法设定的整块数据进行操作。
    </span>

其他模式以及随机设备常量：

**`MCRYPT_ENCRYPT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MCRYPT_DECRYPT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MCRYPT_DEV_RANDOM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MCRYPT_DEV_URANDOM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MCRYPT_RAND`** (<span class="type">integer</span>)  
<span class="simpara"> </span>
