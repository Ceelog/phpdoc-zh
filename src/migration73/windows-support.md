Windows Support
---------------

### PHP Core

#### More POSIX Conforming File Deletion

File descriptors are opened in shared read/write/delete mode by default.
This effectively maps the POSIX semantics and allows to delete files
with handles in use. It is not 100% same, some platform differences
still persist. After the deletion, the filename entry is blocked, until
all the opened handles to it are closed.
