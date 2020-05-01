预定义常量
==========

**目录**

-   [Constants for Attribute
    Flags](/kadm5/constants.html#Constants%20for%20Attribute%20Flags)
-   [Constants for
    Options](/kadm5/constants.html#Constants%20for%20Options)

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

Constants for Attribute Flags
-----------------------------

The functions <span class="function">kadm5\_create\_principal</span>,
<span class="function">kadm5\_modify\_principal</span>, and <span
class="function">kadm5\_modify\_principal</span> allow to specify
special attributes using a bitfield. The symbols are defined below:

| constant                         |
|----------------------------------|
| KRB5\_KDB\_DISALLOW\_POSTDATED   |
| KRB5\_KDB\_DISALLOW\_FORWARDABLE |
| KRB5\_KDB\_DISALLOW\_TGT\_BASED  |
| KRB5\_KDB\_DISALLOW\_RENEWABLE   |
| KRB5\_KDB\_DISALLOW\_PROXIABLE   |
| KRB5\_KDB\_DISALLOW\_DUP\_SKEY   |
| KRB5\_KDB\_DISALLOW\_ALL\_TIX    |
| KRB5\_KDB\_REQUIRES\_PRE\_AUTH   |
| KRB5\_KDB\_REQUIRES\_HW\_AUTH    |
| KRB5\_KDB\_REQUIRES\_PWCHANGE    |
| KRB5\_KDB\_DISALLOW\_SVR         |
| KRB5\_KDB\_PWCHANGE\_SERVER      |
| KRB5\_KDB\_SUPPORT\_DESMD5       |
| KRB5\_KDB\_NEW\_PRINC            |

Constants for Options
---------------------

The functions <span class="function">kadm5\_create\_principal</span>,
<span class="function">kadm5\_modify\_principal</span>, and <span
class="function">kadm5\_get\_principal</span> allow to specify or return
principal's options as an associative array. The keys for the
associative array are defined as string constants below:

| constant                   | funcdef | description                                                                                                           |
|----------------------------|---------|-----------------------------------------------------------------------------------------------------------------------|
| KADM5\_PRINCIPAL           | long    | The expire time of the princial as a Kerberos timestamp.                                                              |
| KADM5\_PRINC\_EXPIRE\_TIME | long    | The expire time of the princial as a Kerberos timestamp.                                                              |
| KADM5\_LAST\_PW\_CHANGE    | long    | The time this principal's password was last changed.                                                                  |
| KADM5\_PW\_EXPIRATION      | long    | The expire time of the principal's current password, as a Kerberos timestamp.                                         |
| KADM5\_MAX\_LIFE           | long    | The maximum lifetime of any Kerberos ticket issued to this principal.                                                 |
| KADM5\_MAX\_RLIFE          | long    | The maximum renewable lifetime of any Kerberos ticket issued to or for this principal.                                |
| KADM5\_MOD\_NAME           | string  | The name of the Kerberos principal that most recently modified this principal.                                        |
| KADM5\_MOD\_TIME           | long    | The time this principal was last modified, as a Kerberos timestamp.                                                   |
| KADM5\_KVNO                | long    | The version of the principal's current key.                                                                           |
| KADM5\_POLICY              | string  | The name of the policy controlling this principal.                                                                    |
| KADM5\_CLEARPOLICY         | long    | Standard procedure is to assign the 'default' policy to new principals. KADM5\_CLEARPOLICY suppresses this behaviour. |
| KADM5\_LAST\_SUCCESS       | long    | The KDC time of the last successfull AS\_REQ.                                                                         |
| KADM5\_LAST\_FAILED        | long    | The KDC time of the last failed AS\_REQ.                                                                              |
| KADM5\_FAIL\_AUTH\_COUNT   | long    | The number of consecutive failed AS\_REQs.                                                                            |
| KADM5\_RANDKEY             | long    | Generates a random password for the principal. The parameter `password` will be ignored.                              |
| KADM5\_ATTRIBUTES          | long    | A bitfield of attributes for use by the KDC.                                                                          |
