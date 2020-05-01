ogg://
======

音频流

### 说明

通过包装器 `ogg://` 读取的文件， 是作为 *OGG/Vorbis*
格式的压缩音频编码。 同样，通过包装器 `ogg://`
写入或追加的数据格式也是压缩音频。 当 <span
class="function">stream\_get\_meta\_data</span> 用于一个打开读取的
*OGG/Vorbis* 文件时，会返回关于数据流的详细信息，包含了 `vendor`
标签、任何内含的 `comments`、 `channels` 数字、采样率（`rate`），以及 用
`bitrate_lower`、`bitrate_upper`、 `bitrate_nominal` 和 `bitrate_window`
描述的可变比特率范围。

`ogg://` PHP 4.3.0 及以上（PECL）

> **Note**: **该封装器默认未激活**  
> <span class="simpara"> 要使用 `ogg://` 封装器，您必须安装
> <a href="https://pecl.php.net/package/oggvorbis" class="link external">» OGG/Vorbis</a>
> 扩展。 可以在
> <a href="https://pecl.php.net/" class="link external">» PECL</a>
> 上找到。 </span>

### 用法

-   <span class="simpara">`ogg://soundfile.ogg`</span>
-   <span class="simpara">`ogg:///path/to/soundfile.ogg`</span>
-   <span
    class="simpara">`ogg://http://www.example.com/path/to/soundstream.ogg`</span>

### 可选项

| 属性                                                                      | 支持 |
|---------------------------------------------------------------------------|------|
| 受限于 <a href="/filesystem/setup.html#" class="link">allow_url_fopen</a> | No   |
| 允许读取                                                                  | Yes  |
| 允许写入                                                                  | Yes  |
| 允许附加                                                                  | Yes  |
| 允许同时读写                                                              | No   |
| 支持 <span class="function">stat</span>                                   | No   |
| 支持 <span class="function">unlink</span>                                 | No   |
| 支持 <span class="function">rename</span>                                 | No   |
| 支持 <span class="function">mkdir</span>                                  | No   |
| 支持 <span class="function">rmdir</span>                                  | No   |

| Name        | Usage                                                                                                                                                                                                                                           | Default                 | Mode      |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|-----------|
| *pcm\_mode* | 读取时使用如下 PCM 编码之一: **`OGGVORBIS_PCM_U8`**、**`OGGVORBIS_PCM_S8`**、 **`OGGVORBIS_PCM_U16_BE`**、**`OGGVORBIS_PCM_S16_BE`**、 **`OGGVORBIS_PCM_U16_LE`** 和 **`OGGVORBIS_PCM_S16_LE`**。 (8 或 16 位，签名或未签名，大或小的 *endian*) | OGGVORBIS\_PCM\_S16\_LE | 读取      |
| *rate*      | 输入数据的采样率，单位为 Hz                                                                                                                                                                                                                     | 44100                   | 写入/附加 |
| *bitrate*   | 若给的值为整数，则是用固定的比特率进行编码。（16000 到 131072）若给的值为浮点数，则使用可变的比特率（质。(-1.0 到 1.0）                                                                                                                         | 128000                  | 写入/附加 |
| *channels*  | 要编码的声道的数量，典型为 1 (单声道), 或 2 (立体声)。最高支持 16 声道。                                                                                                                                                                        | 2                       | 写入/附加 |
| *comments*  | 编码到音轨头部的字符串数组。                                                                                                                                                                                                                    |                         | 写入/附加 |

### 范例
