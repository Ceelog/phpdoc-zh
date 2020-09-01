Windows 支持
------------

### PHP 核心

#### 更符合 POSIX 标准的文件删除方法

File descriptors are opened in shared read/write/delete mode by default.
This effectively maps the POSIX semantics and allows to delete files
with handles in use. It is not 100% same, some platform differences
still persist. After the deletion, the filename entry is blocked, until
all the opened handles to it are closed.
