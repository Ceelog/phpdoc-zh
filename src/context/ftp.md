FTP context options
===================

FTP context option listing

### 说明

Context options for *ftp://* and *ftps://* transports.

### 可选项

`overwrite` <span class="type">bool</span>  
Allow overwriting of already existing files on remote server. Applies to
write mode (uploading) only.

Defaults to **`FALSE`**.

`resume_pos` <span class="type">int</span>  
File offset at which to begin transfer. Applies to read mode
(downloading) only.

Defaults to *0* (Beginning of File).

`proxy` <span class="type">string</span>  
Proxy FTP request via http proxy server. Applies to file read operations
only. Ex: *tcp://squid.example.com:8000*.

### 注释

> **Note**: **Underlying socket stream context options**  
> <span class="simpara"> Additional context options may be supported by
> the
> <a href="/transports/inet.html" class="link">underlying transport</a>
> For *ftp://* streams, refer to context options for the *tcp://*
> transport. For *ftps://* streams, refer to context options for the
> *ssl://* transport. </span>

### 参见

-   <a href="/wrappers/ftp.html" class="xref">ftp://</a>
-   <a href="/context/socket.html" class="xref">套接字上下文选项</a>
-   <a href="/context/ssl.html" class="xref">SSL 上下文选项</a>
