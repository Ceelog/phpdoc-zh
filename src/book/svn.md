Subversion
==========

**目录**

-   [简介](/intro/svn.html)
-   [安装／配置](/svn/setup.html)
    -   [需求](/svn/setup.html#需求)
    -   [安装](/svn/setup.html#安装)
    -   [运行时配置](/svn/setup.html#运行时配置)
    -   [资源类型](/svn/setup.html#资源类型)
-   [预定义常量](/svn/constants.html)
-   [SVN 函数](/ref/svn.html)
    -   [svn\_add](/ref/svn.html#svn_add) — 计划在工作目录添加项
    -   [svn\_auth\_get\_parameter](/ref/svn.html#svn_auth_get_parameter)
        — Retrieves authentication parameter
    -   [svn\_auth\_set\_parameter](/ref/svn.html#svn_auth_set_parameter)
        — Sets an authentication parameter
    -   [svn\_blame](/ref/svn.html#svn_blame) — Get the SVN blame for a
        file
    -   [svn\_cat](/ref/svn.html#svn_cat) — Returns the contents of a
        file in a repository
    -   [svn\_checkout](/ref/svn.html#svn_checkout) — Checks out a
        working copy from the repository
    -   [svn\_cleanup](/ref/svn.html#svn_cleanup) — Recursively cleanup
        a working copy directory, finishing incomplete operations and
        removing locks
    -   [svn\_client\_version](/ref/svn.html#svn_client_version) —
        Returns the version of the SVN client libraries
    -   [svn\_commit](/ref/svn.html#svn_commit) —
        将修改的本地文件副本发送至版本库
    -   [svn\_delete](/ref/svn.html#svn_delete) — Delete items from a
        working copy or repository
    -   [svn\_diff](/ref/svn.html#svn_diff) — Recursively diffs two
        paths
    -   [svn\_export](/ref/svn.html#svn_export) — Export the contents of
        a SVN directory
    -   [svn\_fs\_abort\_txn](/ref/svn.html#svn_fs_abort_txn) — Abort a
        transaction, returns true if everything is okay, false otherwise
    -   [svn\_fs\_apply\_text](/ref/svn.html#svn_fs_apply_text) —
        Creates and returns a stream that will be used to replace
    -   [svn\_fs\_begin\_txn2](/ref/svn.html#svn_fs_begin_txn2) — Create
        a new transaction
    -   [svn\_fs\_change\_node\_prop](/ref/svn.html#svn_fs_change_node_prop)
        — Return true if everything is ok, false otherwise
    -   [svn\_fs\_check\_path](/ref/svn.html#svn_fs_check_path) —
        Determines what kind of item lives at path in a given repository
        fsroot
    -   [svn\_fs\_contents\_changed](/ref/svn.html#svn_fs_contents_changed)
        — Return true if content is different, false otherwise
    -   [svn\_fs\_copy](/ref/svn.html#svn_fs_copy) — Copies a file or a
        directory, returns true if all is ok, false otherwise
    -   [svn\_fs\_delete](/ref/svn.html#svn_fs_delete) — Deletes a file
        or a directory, return true if all is ok, false otherwise
    -   [svn\_fs\_dir\_entries](/ref/svn.html#svn_fs_dir_entries) —
        Enumerates the directory entries under path; returns a hash of
        dir names to file type
    -   [svn\_fs\_file\_contents](/ref/svn.html#svn_fs_file_contents) —
        Returns a stream to access the contents of a file from a given
        version of the fs
    -   [svn\_fs\_file\_length](/ref/svn.html#svn_fs_file_length) —
        Returns the length of a file from a given version of the fs
    -   [svn\_fs\_is\_dir](/ref/svn.html#svn_fs_is_dir) — Return true if
        the path points to a directory, false otherwise
    -   [svn\_fs\_is\_file](/ref/svn.html#svn_fs_is_file) — Return true
        if the path points to a file, false otherwise
    -   [svn\_fs\_make\_dir](/ref/svn.html#svn_fs_make_dir) — Creates a
        new empty directory, returns true if all is ok, false otherwise
    -   [svn\_fs\_make\_file](/ref/svn.html#svn_fs_make_file) — Creates
        a new empty file, returns true if all is ok, false otherwise
    -   [svn\_fs\_node\_created\_rev](/ref/svn.html#svn_fs_node_created_rev)
        — Returns the revision in which path under fsroot was created
    -   [svn\_fs\_node\_prop](/ref/svn.html#svn_fs_node_prop) — Returns
        the value of a property for a node
    -   [svn\_fs\_props\_changed](/ref/svn.html#svn_fs_props_changed) —
        Return true if props are different, false otherwise
    -   [svn\_fs\_revision\_prop](/ref/svn.html#svn_fs_revision_prop) —
        Fetches the value of a named property
    -   [svn\_fs\_revision\_root](/ref/svn.html#svn_fs_revision_root) —
        Get a handle on a specific version of the repository root
    -   [svn\_fs\_txn\_root](/ref/svn.html#svn_fs_txn_root) — Creates
        and returns a transaction root
    -   [svn\_fs\_youngest\_rev](/ref/svn.html#svn_fs_youngest_rev) —
        Returns the number of the youngest revision in the filesystem
    -   [svn\_import](/ref/svn.html#svn_import) — Imports an unversioned
        path into a repository
    -   [svn\_log](/ref/svn.html#svn_log) — Returns the commit log
        messages of a repository URL
    -   [svn\_ls](/ref/svn.html#svn_ls) — Returns list of directory
        contents in repository URL, optionally at revision number
    -   [svn\_mkdir](/ref/svn.html#svn_mkdir) — Creates a directory in a
        working copy or repository
    -   [svn\_repos\_create](/ref/svn.html#svn_repos_create) — Create a
        new subversion repository at path
    -   [svn\_repos\_fs\_begin\_txn\_for\_commit](/ref/svn.html#svn_repos_fs_begin_txn_for_commit)
        — Create a new transaction
    -   [svn\_repos\_fs\_commit\_txn](/ref/svn.html#svn_repos_fs_commit_txn)
        — Commits a transaction and returns the new revision
    -   [svn\_repos\_fs](/ref/svn.html#svn_repos_fs) — Gets a handle on
        the filesystem for a repository
    -   [svn\_repos\_hotcopy](/ref/svn.html#svn_repos_hotcopy) — Make a
        hot-copy of the repos at repospath; copy it to destpath
    -   [svn\_repos\_open](/ref/svn.html#svn_repos_open) — Open a shared
        lock on a repository
    -   [svn\_repos\_recover](/ref/svn.html#svn_repos_recover) — Run
        recovery procedures on the repository located at path
    -   [svn\_revert](/ref/svn.html#svn_revert) — Revert changes to the
        working copy
    -   [svn\_status](/ref/svn.html#svn_status) — Returns the status of
        working copy files and directories
    -   [svn\_update](/ref/svn.html#svn_update) — Update working copy
