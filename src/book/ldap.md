Lightweight Directory Access Protocol
=====================================

**目录**

-   [简介](/intro/ldap.html)
-   [安装／配置](/ldap/setup.html)
    -   [需求](/ldap/setup.html#需求)
    -   [安装](/ldap/setup.html#安装)
    -   [运行时配置](/ldap/setup.html#运行时配置)
    -   [资源类型](/ldap/setup.html#资源类型)
-   [预定义常量](/ldap/constants.html)
-   [Using the PHP LDAP calls](/ldap/using.html)
-   [LDAP controls](/ldap/controls.html)
-   [范例](/ldap/examples.html)
    -   [Basic usage](/ldap/examples.html#Basic%20usage)
    -   [LDAP Controls](/ldap/examples.html#LDAP%20Controls)
-   [LDAP 函数](/ref/ldap.html)
    -   [ldap\_8859\_to\_t61](/ref/ldap.html#ldap_8859_to_t61) —
        Translate 8859 characters to t61 characters
    -   [ldap\_add\_ext](/ref/ldap.html#ldap_add_ext) — Add entries to
        LDAP directory
    -   [ldap\_add](/ref/ldap.html#ldap_add) — Add entries to LDAP
        directory
    -   [ldap\_bind\_ext](/ref/ldap.html#ldap_bind_ext) — Bind to LDAP
        directory
    -   [ldap\_bind](/ref/ldap.html#ldap_bind) — 绑定 LDAP 目录
    -   [ldap\_close](/ref/ldap.html#ldap_close) — 别名 ldap\_unbind
    -   [ldap\_compare](/ref/ldap.html#ldap_compare) — Compare value of
        attribute found in entry specified with DN
    -   [ldap\_connect](/ref/ldap.html#ldap_connect) — Connect to an
        LDAP server
    -   [ldap\_control\_paged\_result\_response](/ref/ldap.html#ldap_control_paged_result_response)
        — Retrieve the LDAP pagination cookie
    -   [ldap\_control\_paged\_result](/ref/ldap.html#ldap_control_paged_result)
        — Send LDAP pagination control
    -   [ldap\_count\_entries](/ref/ldap.html#ldap_count_entries) —
        Count the number of entries in a search
    -   [ldap\_delete\_ext](/ref/ldap.html#ldap_delete_ext) — Delete an
        entry from a directory
    -   [ldap\_delete](/ref/ldap.html#ldap_delete) — Delete an entry
        from a directory
    -   [ldap\_dn2ufn](/ref/ldap.html#ldap_dn2ufn) — Convert DN to User
        Friendly Naming format
    -   [ldap\_err2str](/ref/ldap.html#ldap_err2str) — Convert LDAP
        error number into string error message
    -   [ldap\_errno](/ref/ldap.html#ldap_errno) — Return the LDAP error
        number of the last LDAP command
    -   [ldap\_error](/ref/ldap.html#ldap_error) — Return the LDAP error
        message of the last LDAP command
    -   [ldap\_escape](/ref/ldap.html#ldap_escape) — Escape a string for
        use in an LDAP filter or DN
    -   [ldap\_exop\_passwd](/ref/ldap.html#ldap_exop_passwd) — PASSWD
        extended operation helper
    -   [ldap\_exop\_refresh](/ref/ldap.html#ldap_exop_refresh) —
        Refresh extended operation helper
    -   [ldap\_exop\_whoami](/ref/ldap.html#ldap_exop_whoami) — WHOAMI
        extended operation helper
    -   [ldap\_exop](/ref/ldap.html#ldap_exop) — Performs an extended
        operation
    -   [ldap\_explode\_dn](/ref/ldap.html#ldap_explode_dn) — Splits DN
        into its component parts
    -   [ldap\_first\_attribute](/ref/ldap.html#ldap_first_attribute) —
        Return first attribute
    -   [ldap\_first\_entry](/ref/ldap.html#ldap_first_entry) — Return
        first result id
    -   [ldap\_first\_reference](/ref/ldap.html#ldap_first_reference) —
        Return first reference
    -   [ldap\_free\_result](/ref/ldap.html#ldap_free_result) — Free
        result memory
    -   [ldap\_get\_attributes](/ref/ldap.html#ldap_get_attributes) —
        Get attributes from a search result entry
    -   [ldap\_get\_dn](/ref/ldap.html#ldap_get_dn) — Get the DN of a
        result entry
    -   [ldap\_get\_entries](/ref/ldap.html#ldap_get_entries) — Get all
        result entries
    -   [ldap\_get\_option](/ref/ldap.html#ldap_get_option) — Get the
        current value for given option
    -   [ldap\_get\_values\_len](/ref/ldap.html#ldap_get_values_len) —
        Get all binary values from a result entry
    -   [ldap\_get\_values](/ref/ldap.html#ldap_get_values) — Get all
        values from a result entry
    -   [ldap\_list](/ref/ldap.html#ldap_list) — Single-level search
    -   [ldap\_mod\_add\_ext](/ref/ldap.html#ldap_mod_add_ext) — Add
        attribute values to current attributes
    -   [ldap\_mod\_add](/ref/ldap.html#ldap_mod_add) — Add attribute
        values to current attributes
    -   [ldap\_mod\_del\_ext](/ref/ldap.html#ldap_mod_del_ext) — Delete
        attribute values from current attributes
    -   [ldap\_mod\_del](/ref/ldap.html#ldap_mod_del) — Delete attribute
        values from current attributes
    -   [ldap\_mod\_replace\_ext](/ref/ldap.html#ldap_mod_replace_ext) —
        Replace attribute values with new ones
    -   [ldap\_mod\_replace](/ref/ldap.html#ldap_mod_replace) — Replace
        attribute values with new ones
    -   [ldap\_modify\_batch](/ref/ldap.html#ldap_modify_batch) — Batch
        and execute modifications on an LDAP entry
    -   [ldap\_modify](/ref/ldap.html#ldap_modify) — 别名
        ldap\_mod\_replace
    -   [ldap\_next\_attribute](/ref/ldap.html#ldap_next_attribute) —
        Get the next attribute in result
    -   [ldap\_next\_entry](/ref/ldap.html#ldap_next_entry) — Get next
        result entry
    -   [ldap\_next\_reference](/ref/ldap.html#ldap_next_reference) —
        Get next reference
    -   [ldap\_parse\_exop](/ref/ldap.html#ldap_parse_exop) — Parse
        result object from an LDAP extended operation
    -   [ldap\_parse\_reference](/ref/ldap.html#ldap_parse_reference) —
        Extract information from reference entry
    -   [ldap\_parse\_result](/ref/ldap.html#ldap_parse_result) —
        Extract information from result
    -   [ldap\_read](/ref/ldap.html#ldap_read) — Read an entry
    -   [ldap\_rename\_ext](/ref/ldap.html#ldap_rename_ext) — Modify the
        name of an entry
    -   [ldap\_rename](/ref/ldap.html#ldap_rename) — Modify the name of
        an entry
    -   [ldap\_sasl\_bind](/ref/ldap.html#ldap_sasl_bind) — Bind to LDAP
        directory using SASL
    -   [ldap\_search](/ref/ldap.html#ldap_search) — Search LDAP tree
    -   [ldap\_set\_option](/ref/ldap.html#ldap_set_option) — Set the
        value of the given option
    -   [ldap\_set\_rebind\_proc](/ref/ldap.html#ldap_set_rebind_proc) —
        Set a callback function to do re-binds on referral chasing
    -   [ldap\_sort](/ref/ldap.html#ldap_sort) — Sort LDAP result
        entries on the client side
    -   [ldap\_start\_tls](/ref/ldap.html#ldap_start_tls) — Start TLS
    -   [ldap\_t61\_to\_8859](/ref/ldap.html#ldap_t61_to_8859) —
        Translate t61 characters to 8859 characters
    -   [ldap\_unbind](/ref/ldap.html#ldap_unbind) — Unbind from LDAP
        directory
