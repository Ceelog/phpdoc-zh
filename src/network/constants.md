预定义常量
==========

下列常量作为 PHP 核心的一部分总是可用的。

| Constant         | Description                                                                                        |
|------------------|----------------------------------------------------------------------------------------------------|
| **`LOG_CONS`**   | if there is an error while sending data to the system logger, write directly to the system console |
| **`LOG_NDELAY`** | open the connection to the logger immediately                                                      |
| **`LOG_ODELAY`** | (default) delay opening the connection until the first message is logged                           |
| **`LOG_NOWAIT`** |                                                                                                    |
| **`LOG_PERROR`** | print log message also to standard error                                                           |
| **`LOG_PID`**    | include PID with each message                                                                      |

| Constant                        | Description                                                                                                |
|---------------------------------|------------------------------------------------------------------------------------------------------------|
| **`LOG_AUTH`**                  | security/authorization messages (use **`LOG_AUTHPRIV`** instead in systems where that constant is defined) |
| **`LOG_AUTHPRIV`**              | security/authorization messages (private)                                                                  |
| **`LOG_CRON`**                  | clock daemon (cron and at)                                                                                 |
| **`LOG_DAEMON`**                | other system daemons                                                                                       |
| **`LOG_KERN`**                  | kernel messages                                                                                            |
| **`LOG_LOCAL0 ... LOG_LOCAL7`** | reserved for local use, these are not available in Windows                                                 |
| **`LOG_LPR`**                   | line printer subsystem                                                                                     |
| **`LOG_MAIL`**                  | mail subsystem                                                                                             |
| **`LOG_NEWS`**                  | USENET news subsystem                                                                                      |
| **`LOG_SYSLOG`**                | messages generated internally by syslogd                                                                   |
| **`LOG_USER`**                  | generic user-level messages                                                                                |
| **`LOG_UUCP`**                  | UUCP subsystem                                                                                             |

| Constant          | Description                        |
|-------------------|------------------------------------|
| **`LOG_EMERG`**   | system is unusable                 |
| **`LOG_ALERT`**   | action must be taken immediately   |
| **`LOG_CRIT`**    | critical conditions                |
| **`LOG_ERR`**     | error conditions                   |
| **`LOG_WARNING`** | warning conditions                 |
| **`LOG_NOTICE`**  | normal, but significant, condition |
| **`LOG_INFO`**    | informational message              |
| **`LOG_DEBUG`**   | debug-level message                |

| Constant        | Description                                                                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`DNS_A`**     | IPv4 Address Resource                                                                                                                                                                        |
| **`DNS_CAA`**   | Certification Authority Authorization Resource (available as of PHP 7.0.16 and 7.1.2)                                                                                                        |
| **`DNS_MX`**    | Mail Exchanger Resource                                                                                                                                                                      |
| **`DNS_CNAME`** | Alias (Canonical Name) Resource                                                                                                                                                              |
| **`DNS_NS`**    | Authoritative Name Server Resource                                                                                                                                                           |
| **`DNS_PTR`**   | Pointer Resource                                                                                                                                                                             |
| **`DNS_HINFO`** | Host Info Resource (See IANA's <a href="http://www.iana.org/assignments/operating-system-names" class="link external">» <em>Operating System Names</em></a> for the meaning of these values) |
| **`DNS_SOA`**   | Start of Authority Resource                                                                                                                                                                  |
| **`DNS_TXT`**   | Text Resource                                                                                                                                                                                |
| **`DNS_ANY`**   | Any Resource Record. On most systems this returns all resource records, however it should not be counted upon for critical uses. Try **`DNS_ALL`** instead.                                  |
| **`DNS_AAAA`**  | IPv6 Address Resource                                                                                                                                                                        |
| **`DNS_ALL`**   | Iteratively query the name server for each available record type.                                                                                                                            |
