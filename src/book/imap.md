IMAP, POP3 和 NNTP
==================

**目录**

-   [简介](/intro/imap.html)
-   [安装／配置](/imap/setup.html)
    -   [需求](/imap/setup.html#需求)
    -   [安装](/imap/setup.html#安装)
    -   [运行时配置](/imap/setup.html#运行时配置)
    -   [资源类型](/imap/setup.html#资源类型)
-   [预定义常量](/imap/constants.html)
-   [IMAP 函数](/ref/imap.html)
    -   [imap\_8bit](/ref/imap.html#imap_8bit) — Convert an 8bit string
        to a quoted-printable string
    -   [imap\_alerts](/ref/imap.html#imap_alerts) — Returns all IMAP
        alert messages that have occurred
    -   [imap\_append](/ref/imap.html#imap_append) — Append a string
        message to a specified mailbox
    -   [imap\_base64](/ref/imap.html#imap_base64) — Decode BASE64
        encoded text
    -   [imap\_binary](/ref/imap.html#imap_binary) — Convert an 8bit
        string to a base64 string
    -   [imap\_body](/ref/imap.html#imap_body) — Read the message body
    -   [imap\_bodystruct](/ref/imap.html#imap_bodystruct) — Read the
        structure of a specified body section of a specific message
    -   [imap\_check](/ref/imap.html#imap_check) — Check current mailbox
    -   [imap\_clearflag\_full](/ref/imap.html#imap_clearflag_full) —
        Clears flags on messages
    -   [imap\_close](/ref/imap.html#imap_close) — Close an IMAP stream
    -   [imap\_create](/ref/imap.html#imap_create) — 别名
        imap\_createmailbox
    -   [imap\_createmailbox](/ref/imap.html#imap_createmailbox) —
        Create a new mailbox
    -   [imap\_delete](/ref/imap.html#imap_delete) — Mark a message for
        deletion from current mailbox
    -   [imap\_deletemailbox](/ref/imap.html#imap_deletemailbox) —
        Delete a mailbox
    -   [imap\_errors](/ref/imap.html#imap_errors) — Returns all of the
        IMAP errors that have occurred
    -   [imap\_expunge](/ref/imap.html#imap_expunge) — Delete all
        messages marked for deletion
    -   [imap\_fetch\_overview](/ref/imap.html#imap_fetch_overview) —
        Read an overview of the information in the headers of the given
        message
    -   [imap\_fetchbody](/ref/imap.html#imap_fetchbody) — Fetch a
        particular section of the body of the message
    -   [imap\_fetchheader](/ref/imap.html#imap_fetchheader) — Returns
        header for a message
    -   [imap\_fetchmime](/ref/imap.html#imap_fetchmime) — Fetch MIME
        headers for a particular section of the message
    -   [imap\_fetchstructure](/ref/imap.html#imap_fetchstructure) —
        Read the structure of a particular message
    -   [imap\_fetchtext](/ref/imap.html#imap_fetchtext) — 别名
        imap\_body
    -   [imap\_gc](/ref/imap.html#imap_gc) — Clears IMAP cache
    -   [imap\_get\_quota](/ref/imap.html#imap_get_quota) — Retrieve the
        quota level settings, and usage statics per mailbox
    -   [imap\_get\_quotaroot](/ref/imap.html#imap_get_quotaroot) —
        Retrieve the quota settings per user
    -   [imap\_getacl](/ref/imap.html#imap_getacl) — Gets the ACL for a
        given mailbox
    -   [imap\_getmailboxes](/ref/imap.html#imap_getmailboxes) — Read
        the list of mailboxes, returning detailed information on each
        one
    -   [imap\_getsubscribed](/ref/imap.html#imap_getsubscribed) — List
        all the subscribed mailboxes
    -   [imap\_header](/ref/imap.html#imap_header) — 别名
        imap\_headerinfo
    -   [imap\_headerinfo](/ref/imap.html#imap_headerinfo) — Read the
        header of the message
    -   [imap\_headers](/ref/imap.html#imap_headers) — Returns headers
        for all messages in a mailbox
    -   [imap\_last\_error](/ref/imap.html#imap_last_error) — Gets the
        last IMAP error that occurred during this page request
    -   [imap\_list](/ref/imap.html#imap_list) — Read the list of
        mailboxes
    -   [imap\_listmailbox](/ref/imap.html#imap_listmailbox) — 别名
        imap\_list
    -   [imap\_listscan](/ref/imap.html#imap_listscan) — Returns the
        list of mailboxes that matches the given text
    -   [imap\_listsubscribed](/ref/imap.html#imap_listsubscribed) —
        别名 imap\_lsub
    -   [imap\_lsub](/ref/imap.html#imap_lsub) — List all the subscribed
        mailboxes
    -   [imap\_mail\_compose](/ref/imap.html#imap_mail_compose) — Create
        a MIME message based on given envelope and body sections
    -   [imap\_mail\_copy](/ref/imap.html#imap_mail_copy) — Copy
        specified messages to a mailbox
    -   [imap\_mail\_move](/ref/imap.html#imap_mail_move) — Move
        specified messages to a mailbox
    -   [imap\_mail](/ref/imap.html#imap_mail) — Send an email message
    -   [imap\_mailboxmsginfo](/ref/imap.html#imap_mailboxmsginfo) — Get
        information about the current mailbox
    -   [imap\_mime\_header\_decode](/ref/imap.html#imap_mime_header_decode)
        — Decode MIME header elements
    -   [imap\_msgno](/ref/imap.html#imap_msgno) — Gets the message
        sequence number for the given UID
    -   [imap\_mutf7\_to\_utf8](/ref/imap.html#imap_mutf7_to_utf8) —
        Decode a modified UTF-7 string to UTF-8
    -   [imap\_num\_msg](/ref/imap.html#imap_num_msg) — Gets the number
        of messages in the current mailbox
    -   [imap\_num\_recent](/ref/imap.html#imap_num_recent) — Gets the
        number of recent messages in current mailbox
    -   [imap\_open](/ref/imap.html#imap_open) — Open an IMAP stream to
        a mailbox
    -   [imap\_ping](/ref/imap.html#imap_ping) — Check if the IMAP
        stream is still active
    -   [imap\_qprint](/ref/imap.html#imap_qprint) — Convert a
        quoted-printable string to an 8 bit string
    -   [imap\_rename](/ref/imap.html#imap_rename) — 别名
        imap\_renamemailbox
    -   [imap\_renamemailbox](/ref/imap.html#imap_renamemailbox) —
        Rename an old mailbox to new mailbox
    -   [imap\_reopen](/ref/imap.html#imap_reopen) — Reopen IMAP stream
        to new mailbox
    -   [imap\_rfc822\_parse\_adrlist](/ref/imap.html#imap_rfc822_parse_adrlist)
        — Parses an address string
    -   [imap\_rfc822\_parse\_headers](/ref/imap.html#imap_rfc822_parse_headers)
        — Parse mail headers from a string
    -   [imap\_rfc822\_write\_address](/ref/imap.html#imap_rfc822_write_address)
        — Returns a properly formatted email address given the mailbox,
        host, and personal info
    -   [imap\_savebody](/ref/imap.html#imap_savebody) — Save a specific
        body section to a file
    -   [imap\_scan](/ref/imap.html#imap_scan) — 别名 imap\_listscan
    -   [imap\_scanmailbox](/ref/imap.html#imap_scanmailbox) — 别名
        imap\_listscan
    -   [imap\_search](/ref/imap.html#imap_search) — This function
        returns an array of messages matching the given search criteria
    -   [imap\_set\_quota](/ref/imap.html#imap_set_quota) — Sets a quota
        for a given mailbox
    -   [imap\_setacl](/ref/imap.html#imap_setacl) — Sets the ACL for a
        given mailbox
    -   [imap\_setflag\_full](/ref/imap.html#imap_setflag_full) — Sets
        flags on messages
    -   [imap\_sort](/ref/imap.html#imap_sort) — Gets and sort messages
    -   [imap\_status](/ref/imap.html#imap_status) — Returns status
        information on a mailbox
    -   [imap\_subscribe](/ref/imap.html#imap_subscribe) — Subscribe to
        a mailbox
    -   [imap\_thread](/ref/imap.html#imap_thread) — Returns a tree of
        threaded message
    -   [imap\_timeout](/ref/imap.html#imap_timeout) — Set or fetch imap
        timeout
    -   [imap\_uid](/ref/imap.html#imap_uid) — This function returns the
        UID for the given message sequence number
    -   [imap\_undelete](/ref/imap.html#imap_undelete) — Unmark the
        message which is marked deleted
    -   [imap\_unsubscribe](/ref/imap.html#imap_unsubscribe) —
        Unsubscribe from a mailbox
    -   [imap\_utf7\_decode](/ref/imap.html#imap_utf7_decode) — Decodes
        a modified UTF-7 encoded string
    -   [imap\_utf7\_encode](/ref/imap.html#imap_utf7_encode) — Converts
        ISO-8859-1 string to modified UTF-7 text
    -   [imap\_utf8\_to\_mutf7](/ref/imap.html#imap_utf8_to_mutf7) —
        Encode a UTF-8 string to modified UTF-7
    -   [imap\_utf8](/ref/imap.html#imap_utf8) — Converts MIME-encoded
        text to UTF-8
