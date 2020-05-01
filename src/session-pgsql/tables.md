Table definitions
=================

Session table definition

``` sql
CREATE TABLE php_session (
 sess_id            text,
 sess_name          text,
 sess_data          text,
 sess_created       integer,
 sess_modified      integer,
 sess_expire        integer,
 sess_addr_created  text,
 sess_addr_modified text,
 sess_counter       integer,
 sess_error         integer,
 sess_warning       integer,
 sess_notice        integer,
 sess_err_message   text,
 sess_custom        text
);

CREATE INDEX php_session_idx ON php_session USING BTREE (sess_id);
```

**Warning**

If you use *HASH* for *INDEX*, you'll have a deadlock problem when the
server load is *very* high. Even if it's unlikely to have a deadlock
under normal operation, it can occur. *Do not use *HASH* for *INDEX**.

You may change the session table as long as all fields are defined.

Application variables table definition

``` sql
CREATE TABLE php_app_vars (
 app_modified       integer,
 app_name           text,
 app_vars           text
);
```
