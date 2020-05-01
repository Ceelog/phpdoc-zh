编译此扩展无需任何额外的库，但想要 PHP 支持 Linux 的 LFS（large
files），需要最新的 glibc，并在编译 PHP 时带上以下标记：
*-D\_LARGEFILE\_SOURCE -D\_FILE\_OFFSET\_BITS=64*。
