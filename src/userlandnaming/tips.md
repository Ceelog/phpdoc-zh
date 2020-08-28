提示
----

要写出能经受住时间考验的代码，建议在全局的命名空间中，尽量不要用变量、函数或类名，以避免与其它用户空间代码出现命名空间冲突。

防止函数和类的命名冲突的一个常见方法是使用自己专属名字的
<a href="/language/namespaces.html" class="link">namespace</a>。

``` php
<?php

namespace MyProject;

function my_function() {
    return true;
}

\MyProject\my_function();
```

这仍然需要你跟踪已经使用过的命名空间，但一旦你用了在决定了要使用的命名空间后，你可以添加所有的函数和类到它，不用再考虑冲突。

最好的做法是，尽量控制一下添加到全局范围内的变量，以防止与第三方代码的命名产生命名空间冲突。

> **Note**: **Variable scoping**  
>
> Because of PHP's
> <a href="/language/variables/scope.html" class="link">scoping rules</a>
> variables defined inside functions and methods are not in the global
> scope and as such cannot conflict with other variables defined in the
> global scope.
