图像处理和 GD
=============

**目录**

-   [简介](/intro/image.html)
-   [安装／配置](/image/setup.html)
    -   [需求](/image/setup.html#需求)
    -   [安装](/image/setup.html#安装)
    -   [运行时配置](/image/setup.html#运行时配置)
    -   [资源类型](/image/setup.html#资源类型)
-   [预定义常量](/image/constants.html)
-   [范例](/image/examples.html)
    -   [使用 PHP 创建 PNG
        图像](/image/examples.html#使用%20PHP%20创建%20PNG%20图像)
    -   [使用 Alpha
        通道为图像加水印](/image/examples.html#使用%20Alpha%20通道为图像加水印)
    -   [使用 imagecopymerge
        函数创建半透明水印](/image/examples.html#使用%20imagecopymerge%20函数创建半透明水印)
-   [GD 和图像处理 函数](/ref/image.html)
    -   [gd\_info](/ref/image.html#gd_info) — 取得当前安装的 GD 库的信息
    -   [getimagesize](/ref/image.html#getimagesize) — 取得图像大小
    -   [getimagesizefromstring](/ref/image.html#getimagesizefromstring)
        — 从字符串中获取图像尺寸信息
    -   [image\_type\_to\_extension](/ref/image.html#image_type_to_extension)
        — 取得图像类型的文件后缀
    -   [image\_type\_to\_mime\_type](/ref/image.html#image_type_to_mime_type)
        — 取得
        getimagesize，exif\_read\_data，exif\_thumbnail，exif\_imagetype
        所返回的图像类型的 MIME 类型
    -   [image2wbmp](/ref/image.html#image2wbmp) — 以 WBMP
        格式将图像输出到浏览器或文件
    -   [imageaffine](/ref/image.html#imageaffine) —
        返回经过仿射变换后的图像，剪切区域可选
    -   [imageaffinematrixconcat](/ref/image.html#imageaffinematrixconcat)
        — Concatenate two affine transformation matrices
    -   [imageaffinematrixget](/ref/image.html#imageaffinematrixget) —
        Get an affine transformation matrix
    -   [imagealphablending](/ref/image.html#imagealphablending) —
        设定图像的混色模式
    -   [imageantialias](/ref/image.html#imageantialias) —
        是否使用抗锯齿（antialias）功能
    -   [imagearc](/ref/image.html#imagearc) — 画椭圆弧
    -   [imagebmp](/ref/image.html#imagebmp) — Output a BMP image to
        browser or file
    -   [imagechar](/ref/image.html#imagechar) — 水平地画一个字符
    -   [imagecharup](/ref/image.html#imagecharup) — 垂直地画一个字符
    -   [imagecolorallocate](/ref/image.html#imagecolorallocate) —
        为一幅图像分配颜色
    -   [imagecolorallocatealpha](/ref/image.html#imagecolorallocatealpha)
        — 为一幅图像分配颜色 + alpha
    -   [imagecolorat](/ref/image.html#imagecolorat) —
        取得某像素的颜色索引值
    -   [imagecolorclosest](/ref/image.html#imagecolorclosest) —
        取得与指定的颜色最接近的颜色的索引值
    -   [imagecolorclosestalpha](/ref/image.html#imagecolorclosestalpha)
        — 取得与指定的颜色加透明度最接近的颜色
    -   [imagecolorclosesthwb](/ref/image.html#imagecolorclosesthwb) —
        取得与给定颜色最接近的色度的黑白色的索引
    -   [imagecolordeallocate](/ref/image.html#imagecolordeallocate) —
        取消图像颜色的分配
    -   [imagecolorexact](/ref/image.html#imagecolorexact) —
        取得指定颜色的索引值
    -   [imagecolorexactalpha](/ref/image.html#imagecolorexactalpha) —
        取得指定的颜色加透明度的索引值
    -   [imagecolormatch](/ref/image.html#imagecolormatch) —
        使一个图像中调色板版本的颜色与真彩色版本更能匹配
    -   [imagecolorresolve](/ref/image.html#imagecolorresolve) —
        取得指定颜色的索引值或有可能得到的最接近的替代值
    -   [imagecolorresolvealpha](/ref/image.html#imagecolorresolvealpha)
        — 取得指定颜色 + alpha 的索引值或有可能得到的最接近的替代值
    -   [imagecolorset](/ref/image.html#imagecolorset) —
        给指定调色板索引设定颜色
    -   [imagecolorsforindex](/ref/image.html#imagecolorsforindex) —
        取得某索引的颜色
    -   [imagecolorstotal](/ref/image.html#imagecolorstotal) —
        取得一幅图像的调色板中颜色的数目
    -   [imagecolortransparent](/ref/image.html#imagecolortransparent) —
        将某个颜色定义为透明色
    -   [imageconvolution](/ref/image.html#imageconvolution) — 用系数
        div 和 offset 申请一个 3x3 的卷积矩阵
    -   [imagecopy](/ref/image.html#imagecopy) — 拷贝图像的一部分
    -   [imagecopymerge](/ref/image.html#imagecopymerge) —
        拷贝并合并图像的一部分
    -   [imagecopymergegray](/ref/image.html#imagecopymergegray) —
        用灰度拷贝并合并图像的一部分
    -   [imagecopyresampled](/ref/image.html#imagecopyresampled) —
        重采样拷贝部分图像并调整大小
    -   [imagecopyresized](/ref/image.html#imagecopyresized) —
        拷贝部分图像并调整大小
    -   [imagecreate](/ref/image.html#imagecreate) —
        新建一个基于调色板的图像
    -   [imagecreatefrombmp](/ref/image.html#imagecreatefrombmp) —
        由文件或 URL 创建一个新图象。
    -   [imagecreatefromgd2](/ref/image.html#imagecreatefromgd2) — 从
        GD2 文件或 URL 新建一图像
    -   [imagecreatefromgd2part](/ref/image.html#imagecreatefromgd2part)
        — 从给定的 GD2 文件或 URL 中的部分新建一图像
    -   [imagecreatefromgd](/ref/image.html#imagecreatefromgd) — 从 GD
        文件或 URL 新建一图像
    -   [imagecreatefromgif](/ref/image.html#imagecreatefromgif) —
        由文件或 URL 创建一个新图象。
    -   [imagecreatefromjpeg](/ref/image.html#imagecreatefromjpeg) —
        由文件或 URL 创建一个新图象。
    -   [imagecreatefrompng](/ref/image.html#imagecreatefrompng) —
        由文件或 URL 创建一个新图象。
    -   [imagecreatefromstring](/ref/image.html#imagecreatefromstring) —
        从字符串中的图像流新建一图像
    -   [imagecreatefromwbmp](/ref/image.html#imagecreatefromwbmp) —
        由文件或 URL 创建一个新图象。
    -   [imagecreatefromwebp](/ref/image.html#imagecreatefromwebp) —
        由文件或 URL 创建一个新图象。
    -   [imagecreatefromxbm](/ref/image.html#imagecreatefromxbm) —
        由文件或 URL 创建一个新图象。
    -   [imagecreatefromxpm](/ref/image.html#imagecreatefromxpm) —
        由文件或 URL 创建一个新图象。
    -   [imagecreatetruecolor](/ref/image.html#imagecreatetruecolor) —
        新建一个真彩色图像
    -   [imagecrop](/ref/image.html#imagecrop) — Crop an image to the
        given rectangle
    -   [imagecropauto](/ref/image.html#imagecropauto) — Crop an image
        automatically using one of the available modes
    -   [imagedashedline](/ref/image.html#imagedashedline) — 画一虚线
    -   [imagedestroy](/ref/image.html#imagedestroy) — 销毁一图像
    -   [imageellipse](/ref/image.html#imageellipse) — 画一个椭圆
    -   [imagefill](/ref/image.html#imagefill) — 区域填充
    -   [imagefilledarc](/ref/image.html#imagefilledarc) —
        画一椭圆弧且填充
    -   [imagefilledellipse](/ref/image.html#imagefilledellipse) —
        画一椭圆并填充
    -   [imagefilledpolygon](/ref/image.html#imagefilledpolygon) —
        画一多边形并填充
    -   [imagefilledrectangle](/ref/image.html#imagefilledrectangle) —
        画一矩形并填充
    -   [imagefilltoborder](/ref/image.html#imagefilltoborder) —
        区域填充到指定颜色的边界为止
    -   [imagefilter](/ref/image.html#imagefilter) — 对图像使用过滤器
    -   [imageflip](/ref/image.html#imageflip) — Flips an image using a
        given mode
    -   [imagefontheight](/ref/image.html#imagefontheight) —
        取得字体高度
    -   [imagefontwidth](/ref/image.html#imagefontwidth) — 取得字体宽度
    -   [imageftbbox](/ref/image.html#imageftbbox) — 给出一个使用
        FreeType 2 字体的文本框
    -   [imagefttext](/ref/image.html#imagefttext) — 使用 FreeType 2
        字体将文本写入图像
    -   [imagegammacorrect](/ref/image.html#imagegammacorrect) — 对 GD
        图像应用 gamma 修正
    -   [imagegd2](/ref/image.html#imagegd2) — 将 GD2
        图像输出到浏览器或文件
    -   [imagegd](/ref/image.html#imagegd) — 将 GD
        图像输出到浏览器或文件
    -   [imagegetclip](/ref/image.html#imagegetclip) — Get the clipping
        rectangle
    -   [imagegif](/ref/image.html#imagegif) — 输出图象到浏览器或文件。
    -   [imagegrabscreen](/ref/image.html#imagegrabscreen) — Captures
        the whole screen
    -   [imagegrabwindow](/ref/image.html#imagegrabwindow) — Captures a
        window
    -   [imageinterlace](/ref/image.html#imageinterlace) —
        激活或禁止隔行扫描
    -   [imageistruecolor](/ref/image.html#imageistruecolor) —
        检查图像是否为真彩色图像
    -   [imagejpeg](/ref/image.html#imagejpeg) —
        输出图象到浏览器或文件。
    -   [imagelayereffect](/ref/image.html#imagelayereffect) — 设定
        alpha 混色标志以使用绑定的 libgd 分层效果
    -   [imageline](/ref/image.html#imageline) — 画一条线段
    -   [imageloadfont](/ref/image.html#imageloadfont) — 载入一新字体
    -   [imageopenpolygon](/ref/image.html#imageopenpolygon) — Draws an
        open polygon
    -   [imagepalettecopy](/ref/image.html#imagepalettecopy) —
        将调色板从一幅图像拷贝到另一幅
    -   [imagepalettetotruecolor](/ref/image.html#imagepalettetotruecolor)
        — Converts a palette based image to true color
    -   [imagepng](/ref/image.html#imagepng) — 以 PNG
        格式将图像输出到浏览器或文件
    -   [imagepolygon](/ref/image.html#imagepolygon) — 画一个多边形
    -   [imagerectangle](/ref/image.html#imagerectangle) — 画一个矩形
    -   [imageresolution](/ref/image.html#imageresolution) — Get or set
        the resolution of the image
    -   [imagerotate](/ref/image.html#imagerotate) — 用给定角度旋转图像
    -   [imagesavealpha](/ref/image.html#imagesavealpha) —
        设置标记以在保存 PNG 图像时保存完整的 alpha
        通道信息（与单一透明色相反）
    -   [imagescale](/ref/image.html#imagescale) — Scale an image using
        the given new width and height
    -   [imagesetbrush](/ref/image.html#imagesetbrush) —
        设定画线用的画笔图像
    -   [imagesetclip](/ref/image.html#imagesetclip) — Set the clipping
        rectangle
    -   [imagesetinterpolation](/ref/image.html#imagesetinterpolation) —
        Set the interpolation method
    -   [imagesetpixel](/ref/image.html#imagesetpixel) — 画一个单一像素
    -   [imagesetstyle](/ref/image.html#imagesetstyle) — 设定画线的风格
    -   [imagesetthickness](/ref/image.html#imagesetthickness) —
        设定画线的宽度
    -   [imagesettile](/ref/image.html#imagesettile) —
        设定用于填充的贴图
    -   [imagestring](/ref/image.html#imagestring) — 水平地画一行字符串
    -   [imagestringup](/ref/image.html#imagestringup) —
        垂直地画一行字符串
    -   [imagesx](/ref/image.html#imagesx) — 取得图像宽度
    -   [imagesy](/ref/image.html#imagesy) — 取得图像高度
    -   [imagetruecolortopalette](/ref/image.html#imagetruecolortopalette)
        — 将真彩色图像转换为调色板图像
    -   [imagettfbbox](/ref/image.html#imagettfbbox) — 取得使用 TrueType
        字体的文本的范围
    -   [imagettftext](/ref/image.html#imagettftext) — 用 TrueType
        字体向图像写入文本
    -   [imagetypes](/ref/image.html#imagetypes) — 返回当前 PHP
        版本所支持的图像类型
    -   [imagewbmp](/ref/image.html#imagewbmp) — 以 WBMP
        格式将图像输出到浏览器或文件
    -   [imagewebp](/ref/image.html#imagewebp) — 将 WebP
        格式的图像输出到浏览器或文件
    -   [imagexbm](/ref/image.html#imagexbm) — 将 XBM
        图像输出到浏览器或文件
    -   [iptcembed](/ref/image.html#iptcembed) — 将二进制 IPTC
        数据嵌入到一幅 JPEG 图像中
    -   [iptcparse](/ref/image.html#iptcparse) — 将二进制 IPTC
        块解析为单个标记
    -   [jpeg2wbmp](/ref/image.html#jpeg2wbmp) — 将 JPEG 图像文件转换为
        WBMP 图像文件
    -   [png2wbmp](/ref/image.html#png2wbmp) — 将 PNG 图像文件转换为
        WBMP 图像文件
