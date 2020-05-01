This module contains an interface to those functions defined in the IEEE
1003.1 (POSIX.1) standards document which are not accessible through
other means.

**Warning**

Sensitive data can be retrieved with the POSIX functions, e.g. <span
class="function">posix\_getpwnam</span> and friends. None of the POSIX
function perform any kind of access checking when
<a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">safe mode</a>
is enabled. It's therefore *strongly* advised to disable the POSIX
extension at all (use *--disable-posix* in your configure line) if
you're operating in such an environment.

> **Note**: <span class="simpara">此扩展在 Windows 平台上不可用。</span>
