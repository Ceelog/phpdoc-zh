Secure Shell2
=============

**目录**

-   [简介](/intro/ssh2.html)
-   [安装／配置](/ssh2/setup.html)
    -   [需求](/ssh2/setup.html#需求)
    -   [安装](/ssh2/setup.html#安装)
    -   [运行时配置](/ssh2/setup.html#运行时配置)
    -   [资源类型](/ssh2/setup.html#资源类型)
-   [预定义常量](/ssh2/constants.html)
-   [SSH2 函数](/ref/ssh2.html)
    -   [ssh2\_auth\_agent](/ref/ssh2.html#ssh2_auth_agent) —
        Authenticate over SSH using the ssh agent
    -   [ssh2\_auth\_hostbased\_file](/ref/ssh2.html#ssh2_auth_hostbased_file)
        — Authenticate using a public hostkey
    -   [ssh2\_auth\_none](/ref/ssh2.html#ssh2_auth_none) — Authenticate
        as "none"
    -   [ssh2\_auth\_password](/ref/ssh2.html#ssh2_auth_password) —
        Authenticate over SSH using a plain password
    -   [ssh2\_auth\_pubkey\_file](/ref/ssh2.html#ssh2_auth_pubkey_file)
        — Authenticate using a public key
    -   [ssh2\_connect](/ref/ssh2.html#ssh2_connect) — Connect to an SSH
        server
    -   [ssh2\_disconnect](/ref/ssh2.html#ssh2_disconnect) — Close a
        connection to a remote SSH server
    -   [ssh2\_exec](/ref/ssh2.html#ssh2_exec) — Execute a command on a
        remote server
    -   [ssh2\_fetch\_stream](/ref/ssh2.html#ssh2_fetch_stream) — Fetch
        an extended data stream
    -   [ssh2\_fingerprint](/ref/ssh2.html#ssh2_fingerprint) — Retrieve
        fingerprint of remote server
    -   [ssh2\_methods\_negotiated](/ref/ssh2.html#ssh2_methods_negotiated)
        — Return list of negotiated methods
    -   [ssh2\_publickey\_add](/ref/ssh2.html#ssh2_publickey_add) — Add
        an authorized publickey
    -   [ssh2\_publickey\_init](/ref/ssh2.html#ssh2_publickey_init) —
        Initialize Publickey subsystem
    -   [ssh2\_publickey\_list](/ref/ssh2.html#ssh2_publickey_list) —
        List currently authorized publickeys
    -   [ssh2\_publickey\_remove](/ref/ssh2.html#ssh2_publickey_remove)
        — Remove an authorized publickey
    -   [ssh2\_scp\_recv](/ref/ssh2.html#ssh2_scp_recv) — Request a file
        via SCP
    -   [ssh2\_scp\_send](/ref/ssh2.html#ssh2_scp_send) — Send a file
        via SCP
    -   [ssh2\_sftp\_chmod](/ref/ssh2.html#ssh2_sftp_chmod) — Changes
        file mode
    -   [ssh2\_sftp\_lstat](/ref/ssh2.html#ssh2_sftp_lstat) — Stat a
        symbolic link
    -   [ssh2\_sftp\_mkdir](/ref/ssh2.html#ssh2_sftp_mkdir) — Create a
        directory
    -   [ssh2\_sftp\_readlink](/ref/ssh2.html#ssh2_sftp_readlink) —
        Return the target of a symbolic link
    -   [ssh2\_sftp\_realpath](/ref/ssh2.html#ssh2_sftp_realpath) —
        Resolve the realpath of a provided path string
    -   [ssh2\_sftp\_rename](/ref/ssh2.html#ssh2_sftp_rename) — Rename a
        remote file
    -   [ssh2\_sftp\_rmdir](/ref/ssh2.html#ssh2_sftp_rmdir) — Remove a
        directory
    -   [ssh2\_sftp\_stat](/ref/ssh2.html#ssh2_sftp_stat) — Stat a file
        on a remote filesystem
    -   [ssh2\_sftp\_symlink](/ref/ssh2.html#ssh2_sftp_symlink) — Create
        a symlink
    -   [ssh2\_sftp\_unlink](/ref/ssh2.html#ssh2_sftp_unlink) — Delete a
        file
    -   [ssh2\_sftp](/ref/ssh2.html#ssh2_sftp) — Initialize SFTP
        subsystem
    -   [ssh2\_shell](/ref/ssh2.html#ssh2_shell) — Request an
        interactive shell
    -   [ssh2\_tunnel](/ref/ssh2.html#ssh2_tunnel) — Open a tunnel
        through a remote server
