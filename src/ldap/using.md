Using the PHP LDAP calls
========================

Before you can use the LDAP calls you will need to know...

-   The name or address of the directory server you will use

-   The "base dn" of the server (the part of the world directory that is
    held on this server, which could be "o=My Company,c=US")

-   Whether you need a password to access the server (many servers will
    provide read access for an "anonymous bind" but require a password
    for anything else)

The typical sequence of LDAP calls you will make in an application will
follow this pattern:

``` literallayout
  ldap_connect()    // establish connection to server
     |
  ldap_bind()       // anonymous or authenticated "login"
     |
  do something like search or update the directory
  and display the results
     |
  ldap_close()      // "logout"
```
