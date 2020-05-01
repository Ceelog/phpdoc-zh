这些函数提供执行系统本身命令的能力， 以及安全执行系统命令。

> **Note**:
>
> 在 Windows 平台上，所有命令执行都是通过 *cmd.exe* 来完成的。
> 因此，调用这些函数的用户需要拥有运行此命令的相应权限。 但是当使用
> *bypass\_shell* 选项来调用 <span class="function">proc\_open</span>
> 函数时是个例外。
