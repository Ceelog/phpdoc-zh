**Warning**

此扩展是*实验性* 的。
此扩展的表象，包括其函数名称以及其他此扩展的相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本扩展风险自担。

This extension allows the loading of shared libraries (`.DLL` or `.so`),
calling of C functions and accessing of C data structures in pure PHP,
without having to have deep knowledge of the Zend extension API, and
without having to learn a third “intermediate” language. The public API
is implemented as a single class <span class="classname">FFI</span> with
several static methods (some of them may be called dynamically), and
overloaded object methods, which perform the actual interaction with C
data.

**Caution**

FFI is dangerous, since it allows to interface with the system on a very
low level. The FFI extension should only be used by developers having a
working knowledge of C and the used C APIs. To minimize the risk, the
FFI API usage may be restricted with the
<a href="/ffi/setup.html#" class="link">ffi.enable</a> `php.ini`
directive.

> **Note**:
>
> The FFI extension does not render the classic PHP extension API
> obsolete; it is merely provided for ad-hoc interfacing with C
> functions and data structures.

**小贴士**

Currently, accessing FFI data structures is significantly (about 2
times) slower than accessing native PHP arrays and objects. Therefore,
it makes no sense to use the FFI extension for speed; however, it may
make sense to use it to reduce memory consumption.
