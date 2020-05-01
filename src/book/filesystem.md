文件系统
========

**目录**

-   [简介](/intro/filesystem.html)
-   [安装／配置](/filesystem/setup.html)
    -   [需求](/filesystem/setup.html#需求)
    -   [安装](/filesystem/setup.html#安装)
    -   [运行时配置](/filesystem/setup.html#运行时配置)
    -   [资源类型](/filesystem/setup.html#资源类型)
-   [预定义常量](/filesystem/constants.html)
-   [文件系统函数](/ref/filesystem.html)
    -   [basename](/ref/filesystem.html#basename) —
        返回路径中的文件名部分
    -   [chgrp](/ref/filesystem.html#chgrp) — 改变文件所属的组
    -   [chmod](/ref/filesystem.html#chmod) — 改变文件模式
    -   [chown](/ref/filesystem.html#chown) — 改变文件的所有者
    -   [clearstatcache](/ref/filesystem.html#clearstatcache) —
        清除文件状态缓存
    -   [copy](/ref/filesystem.html#copy) — 拷贝文件
    -   [delete](/ref/filesystem.html#delete) — 参见 unlink 或 unset
    -   [dirname](/ref/filesystem.html#dirname) — 返回路径中的目录部分
    -   [disk\_free\_space](/ref/filesystem.html#disk_free_space) —
        返回目录中的可用空间
    -   [disk\_total\_space](/ref/filesystem.html#disk_total_space) —
        返回一个目录的磁盘总大小
    -   [diskfreespace](/ref/filesystem.html#diskfreespace) —
        disk\_free\_space 的别名
    -   [fclose](/ref/filesystem.html#fclose) — 关闭一个已打开的文件指针
    -   [feof](/ref/filesystem.html#feof) —
        测试文件指针是否到了文件结束的位置
    -   [fflush](/ref/filesystem.html#fflush) — 将缓冲内容输出到文件
    -   [fgetc](/ref/filesystem.html#fgetc) — 从文件指针中读取字符
    -   [fgetcsv](/ref/filesystem.html#fgetcsv) —
        从文件指针中读入一行并解析 CSV 字段
    -   [fgets](/ref/filesystem.html#fgets) — 从文件指针中读取一行
    -   [fgetss](/ref/filesystem.html#fgetss) —
        从文件指针中读取一行并过滤掉 HTML 标记
    -   [file\_exists](/ref/filesystem.html#file_exists) —
        检查文件或目录是否存在
    -   [file\_get\_contents](/ref/filesystem.html#file_get_contents) —
        将整个文件读入一个字符串
    -   [file\_put\_contents](/ref/filesystem.html#file_put_contents) —
        将一个字符串写入文件
    -   [file](/ref/filesystem.html#file) — 把整个文件读入一个数组中
    -   [fileatime](/ref/filesystem.html#fileatime) —
        取得文件的上次访问时间
    -   [filectime](/ref/filesystem.html#filectime) — 取得文件的 inode
        修改时间
    -   [filegroup](/ref/filesystem.html#filegroup) — 取得文件的组
    -   [fileinode](/ref/filesystem.html#fileinode) — 取得文件的 inode
    -   [filemtime](/ref/filesystem.html#filemtime) — 取得文件修改时间
    -   [fileowner](/ref/filesystem.html#fileowner) — 取得文件的所有者
    -   [fileperms](/ref/filesystem.html#fileperms) — 取得文件的权限
    -   [filesize](/ref/filesystem.html#filesize) — 取得文件大小
    -   [filetype](/ref/filesystem.html#filetype) — 取得文件类型
    -   [flock](/ref/filesystem.html#flock) — 轻便的咨询文件锁定
    -   [fnmatch](/ref/filesystem.html#fnmatch) — 用模式匹配文件名
    -   [fopen](/ref/filesystem.html#fopen) — 打开文件或者 URL
    -   [fpassthru](/ref/filesystem.html#fpassthru) —
        输出文件指针处的所有剩余数据
    -   [fputcsv](/ref/filesystem.html#fputcsv) — 将行格式化为 CSV
        并写入文件指针
    -   [fputs](/ref/filesystem.html#fputs) — fwrite 的别名
    -   [fread](/ref/filesystem.html#fread) —
        读取文件（可安全用于二进制文件）
    -   [fscanf](/ref/filesystem.html#fscanf) — 从文件中格式化输入
    -   [fseek](/ref/filesystem.html#fseek) — 在文件指针中定位
    -   [fstat](/ref/filesystem.html#fstat) —
        通过已打开的文件指针取得文件信息
    -   [ftell](/ref/filesystem.html#ftell) — 返回文件指针读/写的位置
    -   [ftruncate](/ref/filesystem.html#ftruncate) —
        将文件截断到给定的长度
    -   [fwrite](/ref/filesystem.html#fwrite) —
        写入文件（可安全用于二进制文件）
    -   [glob](/ref/filesystem.html#glob) — 寻找与模式匹配的文件路径
    -   [is\_dir](/ref/filesystem.html#is_dir) —
        判断给定文件名是否是一个目录
    -   [is\_executable](/ref/filesystem.html#is_executable) —
        判断给定文件名是否可执行
    -   [is\_file](/ref/filesystem.html#is_file) —
        判断给定文件名是否为一个正常的文件
    -   [is\_link](/ref/filesystem.html#is_link) —
        判断给定文件名是否为一个符号连接
    -   [is\_readable](/ref/filesystem.html#is_readable) —
        判断给定文件名是否可读
    -   [is\_uploaded\_file](/ref/filesystem.html#is_uploaded_file) —
        判断文件是否是通过 HTTP POST 上传的
    -   [is\_writable](/ref/filesystem.html#is_writable) —
        判断给定的文件名是否可写
    -   [is\_writeable](/ref/filesystem.html#is_writeable) —
        is\_writable 的别名
    -   [lchgrp](/ref/filesystem.html#lchgrp) — 修改符号链接的所有组
    -   [lchown](/ref/filesystem.html#lchown) — 修改符号链接的所有者
    -   [link](/ref/filesystem.html#link) — 建立一个硬连接
    -   [linkinfo](/ref/filesystem.html#linkinfo) — 获取一个连接的信息
    -   [lstat](/ref/filesystem.html#lstat) —
        给出一个文件或符号连接的信息
    -   [mkdir](/ref/filesystem.html#mkdir) — 新建目录
    -   [move\_uploaded\_file](/ref/filesystem.html#move_uploaded_file)
        — 将上传的文件移动到新位置
    -   [parse\_ini\_file](/ref/filesystem.html#parse_ini_file) —
        解析一个配置文件
    -   [parse\_ini\_string](/ref/filesystem.html#parse_ini_string) —
        解析配置字符串
    -   [pathinfo](/ref/filesystem.html#pathinfo) — 返回文件路径的信息
    -   [pclose](/ref/filesystem.html#pclose) — 关闭进程文件指针
    -   [popen](/ref/filesystem.html#popen) — 打开进程文件指针
    -   [readfile](/ref/filesystem.html#readfile) — 输出文件
    -   [readlink](/ref/filesystem.html#readlink) —
        返回符号连接指向的目标
    -   [realpath\_cache\_get](/ref/filesystem.html#realpath_cache_get)
        — 获取真实目录缓存的详情
    -   [realpath\_cache\_size](/ref/filesystem.html#realpath_cache_size)
        — 获取真实路径缓冲区的大小
    -   [realpath](/ref/filesystem.html#realpath) —
        返回规范化的绝对路径名
    -   [rename](/ref/filesystem.html#rename) — 重命名一个文件或目录
    -   [rewind](/ref/filesystem.html#rewind) — 倒回文件指针的位置
    -   [rmdir](/ref/filesystem.html#rmdir) — 删除目录
    -   [set\_file\_buffer](/ref/filesystem.html#set_file_buffer) —
        stream\_set\_write\_buffer 的别名
    -   [stat](/ref/filesystem.html#stat) — 给出文件的信息
    -   [symlink](/ref/filesystem.html#symlink) — 建立符号连接
    -   [tempnam](/ref/filesystem.html#tempnam) —
        建立一个具有唯一文件名的文件
    -   [tmpfile](/ref/filesystem.html#tmpfile) — 建立一个临时文件
    -   [touch](/ref/filesystem.html#touch) — 设定文件的访问和修改时间
    -   [umask](/ref/filesystem.html#umask) — 改变当前的 umask
    -   [unlink](/ref/filesystem.html#unlink) — 删除文件
