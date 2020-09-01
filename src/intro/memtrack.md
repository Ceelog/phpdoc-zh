The purpose of this extension is to detect the most memory hungry
scripts and functions.

memtrack tracks memory consumption in PHP scripts and produces reports
(warnings) when the consumption reaches certain levels set by the user.
This is achieved by replacing default executor function by a special
function which compares memory usage before and after running the
original executor - this way we can tell how much the memory usage has
changed during the execution of the current part of the code.

Zend Engine runs its executor for each opcode array (op\_array), which
usually means function, plain script and such, so memtrack doesn't have
any noticeable effect on performance.

memtrack doesn't provide any functions, there are only INI directives
which allow you to configure the way it should work.

**Warning**

此扩展是*实验性* 的。
此扩展的表象，包括其函数名称以及其他此扩展的相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本扩展风险自担。
