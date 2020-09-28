反射
====

**目录**

-   [简介](/intro/reflection.html)
-   [安装／配置](/reflection/setup.html)
    -   [需求](/reflection/setup.html#需求)
    -   [安装](/reflection/setup.html#安装)
    -   [运行时配置](/reflection/setup.html#运行时配置)
    -   [资源类型](/reflection/setup.html#资源类型)
-   [预定义常量](/reflection/constants.html)
-   [范例](/reflection/examples.html)
-   [扩展](/reflection/extending.html)
-   [Reflection](/class/reflection.html) — Reflection 类
    -   [Reflection::export](/class/reflection.html#Reflection::export)
        — Exports
    -   [Reflection::getModifierNames](/class/reflection.html#Reflection::getModifierNames)
        — 获取修饰符的名称
-   [ReflectionClass](/class/reflectionclass.html) — ReflectionClass 类
    -   [ReflectionClass::\_\_construct](/class/reflectionclass.html#ReflectionClass::__construct)
        — 初始化 ReflectionClass 类
    -   [ReflectionClass::export](/class/reflectionclass.html#ReflectionClass::export)
        — 导出一个类
    -   [ReflectionClass::getConstant](/class/reflectionclass.html#ReflectionClass::getConstant)
        — 获取定义过的一个常量
    -   [ReflectionClass::getConstants](/class/reflectionclass.html#ReflectionClass::getConstants)
        — 获取一组常量
    -   [ReflectionClass::getConstructor](/class/reflectionclass.html#ReflectionClass::getConstructor)
        — 获取类的构造函数
    -   [ReflectionClass::getDefaultProperties](/class/reflectionclass.html#ReflectionClass::getDefaultProperties)
        — 获取默认属性
    -   [ReflectionClass::getDocComment](/class/reflectionclass.html#ReflectionClass::getDocComment)
        — 获取文档注释
    -   [ReflectionClass::getEndLine](/class/reflectionclass.html#ReflectionClass::getEndLine)
        — 获取最后一行的行数
    -   [ReflectionClass::getExtension](/class/reflectionclass.html#ReflectionClass::getExtension)
        — 根据已定义的类获取所在扩展的 ReflectionExtension 对象
    -   [ReflectionClass::getExtensionName](/class/reflectionclass.html#ReflectionClass::getExtensionName)
        — 获取定义的类所在的扩展的名称
    -   [ReflectionClass::getFileName](/class/reflectionclass.html#ReflectionClass::getFileName)
        — 获取定义类的文件名
    -   [ReflectionClass::getInterfaceNames](/class/reflectionclass.html#ReflectionClass::getInterfaceNames)
        — 获取接口（interface）名称
    -   [ReflectionClass::getInterfaces](/class/reflectionclass.html#ReflectionClass::getInterfaces)
        — 获取接口
    -   [ReflectionClass::getMethod](/class/reflectionclass.html#ReflectionClass::getMethod)
        — 获取一个类方法的 ReflectionMethod。
    -   [ReflectionClass::getMethods](/class/reflectionclass.html#ReflectionClass::getMethods)
        — 获取方法的数组
    -   [ReflectionClass::getModifiers](/class/reflectionclass.html#ReflectionClass::getModifiers)
        — 获取类的修饰符
    -   [ReflectionClass::getName](/class/reflectionclass.html#ReflectionClass::getName)
        — 获取类名
    -   [ReflectionClass::getNamespaceName](/class/reflectionclass.html#ReflectionClass::getNamespaceName)
        — 获取命名空间的名称
    -   [ReflectionClass::getParentClass](/class/reflectionclass.html#ReflectionClass::getParentClass)
        — 获取父类
    -   [ReflectionClass::getProperties](/class/reflectionclass.html#ReflectionClass::getProperties)
        — 获取一组属性
    -   [ReflectionClass::getProperty](/class/reflectionclass.html#ReflectionClass::getProperty)
        — 获取类的一个属性的 ReflectionProperty
    -   [ReflectionClass::getReflectionConstant](/class/reflectionclass.html#ReflectionClass::getReflectionConstant)
        — Gets a ReflectionClassConstant for a class's constant
    -   [ReflectionClass::getReflectionConstants](/class/reflectionclass.html#ReflectionClass::getReflectionConstants)
        — Gets class constants
    -   [ReflectionClass::getShortName](/class/reflectionclass.html#ReflectionClass::getShortName)
        — 获取短名
    -   [ReflectionClass::getStartLine](/class/reflectionclass.html#ReflectionClass::getStartLine)
        — 获取起始行号
    -   [ReflectionClass::getStaticProperties](/class/reflectionclass.html#ReflectionClass::getStaticProperties)
        — 获取静态（static）属性
    -   [ReflectionClass::getStaticPropertyValue](/class/reflectionclass.html#ReflectionClass::getStaticPropertyValue)
        — 获取静态（static）属性的值
    -   [ReflectionClass::getTraitAliases](/class/reflectionclass.html#ReflectionClass::getTraitAliases)
        — 返回 trait 别名的一个数组
    -   [ReflectionClass::getTraitNames](/class/reflectionclass.html#ReflectionClass::getTraitNames)
        — 返回这个类所使用 traits 的名称的数组
    -   [ReflectionClass::getTraits](/class/reflectionclass.html#ReflectionClass::getTraits)
        — 返回这个类所使用的 traits 数组
    -   [ReflectionClass::hasConstant](/class/reflectionclass.html#ReflectionClass::hasConstant)
        — 检查常量是否已经定义
    -   [ReflectionClass::hasMethod](/class/reflectionclass.html#ReflectionClass::hasMethod)
        — 检查方法是否已定义
    -   [ReflectionClass::hasProperty](/class/reflectionclass.html#ReflectionClass::hasProperty)
        — 检查属性是否已定义
    -   [ReflectionClass::implementsInterface](/class/reflectionclass.html#ReflectionClass::implementsInterface)
        — 接口的实现
    -   [ReflectionClass::inNamespace](/class/reflectionclass.html#ReflectionClass::inNamespace)
        — 检查是否位于命名空间中
    -   [ReflectionClass::isAbstract](/class/reflectionclass.html#ReflectionClass::isAbstract)
        — 检查类是否是抽象类（abstract）
    -   [ReflectionClass::isAnonymous](/class/reflectionclass.html#ReflectionClass::isAnonymous)
        — 检查类是否是匿名类
    -   [ReflectionClass::isCloneable](/class/reflectionclass.html#ReflectionClass::isCloneable)
        — 返回了一个类是否可复制
    -   [ReflectionClass::isFinal](/class/reflectionclass.html#ReflectionClass::isFinal)
        — 检查类是否声明为 final
    -   [ReflectionClass::isInstance](/class/reflectionclass.html#ReflectionClass::isInstance)
        — 检查类的实例
    -   [ReflectionClass::isInstantiable](/class/reflectionclass.html#ReflectionClass::isInstantiable)
        — 检查类是否可实例化
    -   [ReflectionClass::isInterface](/class/reflectionclass.html#ReflectionClass::isInterface)
        — 检查类是否是一个接口（interface）
    -   [ReflectionClass::isInternal](/class/reflectionclass.html#ReflectionClass::isInternal)
        — 检查类是否由扩展或核心在内部定义
    -   [ReflectionClass::isIterable](/class/reflectionclass.html#ReflectionClass::isIterable)
        — Check whether this class is iterable
    -   [ReflectionClass::isIterateable](/class/reflectionclass.html#ReflectionClass::isIterateable)
        — 检查是否可迭代（iterateable）
    -   [ReflectionClass::isSubclassOf](/class/reflectionclass.html#ReflectionClass::isSubclassOf)
        — 检查是否为一个子类
    -   [ReflectionClass::isTrait](/class/reflectionclass.html#ReflectionClass::isTrait)
        — 返回了是否为一个 trait
    -   [ReflectionClass::isUserDefined](/class/reflectionclass.html#ReflectionClass::isUserDefined)
        — 检查是否由用户定义的
    -   [ReflectionClass::newInstance](/class/reflectionclass.html#ReflectionClass::newInstance)
        — 从指定的参数创建一个新的类实例
    -   [ReflectionClass::newInstanceArgs](/class/reflectionclass.html#ReflectionClass::newInstanceArgs)
        — 从给出的参数创建一个新的类实例。
    -   [ReflectionClass::newInstanceWithoutConstructor](/class/reflectionclass.html#ReflectionClass::newInstanceWithoutConstructor)
        — 创建一个新的类实例而不调用它的构造函数
    -   [ReflectionClass::setStaticPropertyValue](/class/reflectionclass.html#ReflectionClass::setStaticPropertyValue)
        — 设置静态属性的值
    -   [ReflectionClass::\_\_toString](/class/reflectionclass.html#ReflectionClass::__toString)
        — 返回 ReflectionClass 对象字符串的表示形式。
-   [ReflectionClassConstant](/class/reflectionclassconstant.html) — The
    ReflectionClassConstant class
    -   [ReflectionClassConstant::\_\_construct](/class/reflectionclassconstant.html#ReflectionClassConstant::__construct)
        — Constructs a ReflectionClassConstant
    -   [ReflectionClassConstant::export](/class/reflectionclassconstant.html#ReflectionClassConstant::export)
        — Export
    -   [ReflectionClassConstant::getDeclaringClass](/class/reflectionclassconstant.html#ReflectionClassConstant::getDeclaringClass)
        — Gets declaring class
    -   [ReflectionClassConstant::getDocComment](/class/reflectionclassconstant.html#ReflectionClassConstant::getDocComment)
        — Gets doc comments
    -   [ReflectionClassConstant::getModifiers](/class/reflectionclassconstant.html#ReflectionClassConstant::getModifiers)
        — Gets the class constant modifiers
    -   [ReflectionClassConstant::getName](/class/reflectionclassconstant.html#ReflectionClassConstant::getName)
        — Get name of the constant
    -   [ReflectionClassConstant::getValue](/class/reflectionclassconstant.html#ReflectionClassConstant::getValue)
        — Gets value
    -   [ReflectionClassConstant::isPrivate](/class/reflectionclassconstant.html#ReflectionClassConstant::isPrivate)
        — Checks if class constant is private
    -   [ReflectionClassConstant::isProtected](/class/reflectionclassconstant.html#ReflectionClassConstant::isProtected)
        — Checks if class constant is protected
    -   [ReflectionClassConstant::isPublic](/class/reflectionclassconstant.html#ReflectionClassConstant::isPublic)
        — Checks if class constant is public
    -   [ReflectionClassConstant::\_\_toString](/class/reflectionclassconstant.html#ReflectionClassConstant::__toString)
        — Returns the string representation of the
        ReflectionClassConstant object
-   [ReflectionZendExtension](/class/reflectionzendextension.html) —
    ReflectionZendExtension 类
    -   [ReflectionZendExtension::\_\_clone](/class/reflectionzendextension.html#ReflectionZendExtension::__clone)
        — Clone handler
    -   [ReflectionZendExtension::\_\_construct](/class/reflectionzendextension.html#ReflectionZendExtension::__construct)
        — Constructor
    -   [ReflectionZendExtension::export](/class/reflectionzendextension.html#ReflectionZendExtension::export)
        — Export
    -   [ReflectionZendExtension::getAuthor](/class/reflectionzendextension.html#ReflectionZendExtension::getAuthor)
        — Gets author
    -   [ReflectionZendExtension::getCopyright](/class/reflectionzendextension.html#ReflectionZendExtension::getCopyright)
        — Gets copyright
    -   [ReflectionZendExtension::getName](/class/reflectionzendextension.html#ReflectionZendExtension::getName)
        — Gets name
    -   [ReflectionZendExtension::getURL](/class/reflectionzendextension.html#ReflectionZendExtension::getURL)
        — Gets URL
    -   [ReflectionZendExtension::getVersion](/class/reflectionzendextension.html#ReflectionZendExtension::getVersion)
        — Gets version
    -   [ReflectionZendExtension::\_\_toString](/class/reflectionzendextension.html#ReflectionZendExtension::__toString)
        — To string handler
-   [ReflectionExtension](/class/reflectionextension.html) —
    ReflectionExtension 类
    -   [ReflectionExtension::\_\_clone](/class/reflectionextension.html#ReflectionExtension::__clone)
        — Clones
    -   [ReflectionExtension::\_\_construct](/class/reflectionextension.html#ReflectionExtension::__construct)
        — Constructs a ReflectionExtension
    -   [ReflectionExtension::export](/class/reflectionextension.html#ReflectionExtension::export)
        — Export
    -   [ReflectionExtension::getClasses](/class/reflectionextension.html#ReflectionExtension::getClasses)
        — Gets classes
    -   [ReflectionExtension::getClassNames](/class/reflectionextension.html#ReflectionExtension::getClassNames)
        — 获取类名称
    -   [ReflectionExtension::getConstants](/class/reflectionextension.html#ReflectionExtension::getConstants)
        — 获取常量
    -   [ReflectionExtension::getDependencies](/class/reflectionextension.html#ReflectionExtension::getDependencies)
        — 获取依赖
    -   [ReflectionExtension::getFunctions](/class/reflectionextension.html#ReflectionExtension::getFunctions)
        — 获取扩展中的函数
    -   [ReflectionExtension::getINIEntries](/class/reflectionextension.html#ReflectionExtension::getINIEntries)
        — 获取ini配置
    -   [ReflectionExtension::getName](/class/reflectionextension.html#ReflectionExtension::getName)
        — 获取扩展名称
    -   [ReflectionExtension::getVersion](/class/reflectionextension.html#ReflectionExtension::getVersion)
        — 获取扩展版本号
    -   [ReflectionExtension::info](/class/reflectionextension.html#ReflectionExtension::info)
        — 输出扩展信息
    -   [ReflectionExtension::isPersistent](/class/reflectionextension.html#ReflectionExtension::isPersistent)
        — 返回扩展是否持久化载入
    -   [ReflectionExtension::isTemporary](/class/reflectionextension.html#ReflectionExtension::isTemporary)
        — 返回扩展是否是临时载入
    -   [ReflectionExtension::\_\_toString](/class/reflectionextension.html#ReflectionExtension::__toString)
        — To string
-   [ReflectionFunction](/class/reflectionfunction.html) —
    ReflectionFunction 类
    -   [ReflectionFunction::\_\_construct](/class/reflectionfunction.html#ReflectionFunction::__construct)
        — Constructs a ReflectionFunction object
    -   [ReflectionFunction::export](/class/reflectionfunction.html#ReflectionFunction::export)
        — Exports function
    -   [ReflectionFunction::getClosure](/class/reflectionfunction.html#ReflectionFunction::getClosure)
        — Returns a dynamically created closure for the function
    -   [ReflectionFunction::invoke](/class/reflectionfunction.html#ReflectionFunction::invoke)
        — Invokes function
    -   [ReflectionFunction::invokeArgs](/class/reflectionfunction.html#ReflectionFunction::invokeArgs)
        — Invokes function args
    -   [ReflectionFunction::isDisabled](/class/reflectionfunction.html#ReflectionFunction::isDisabled)
        — Checks if function is disabled
    -   [ReflectionFunction::\_\_toString](/class/reflectionfunction.html#ReflectionFunction::__toString)
        — To string
-   [ReflectionFunctionAbstract](/class/reflectionfunctionabstract.html)
    — ReflectionFunctionAbstract 类
    -   [ReflectionFunctionAbstract::\_\_clone](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::__clone)
        — 复制函数
    -   [ReflectionFunctionAbstract::getClosureScopeClass](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getClosureScopeClass)
        — Returns the scope associated to the closure
    -   [ReflectionFunctionAbstract::getClosureThis](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getClosureThis)
        — 返回本身的匿名函数
    -   [ReflectionFunctionAbstract::getDocComment](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getDocComment)
        — 获取注释内容
    -   [ReflectionFunctionAbstract::getEndLine](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getEndLine)
        — 获取结束行号
    -   [ReflectionFunctionAbstract::getExtension](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getExtension)
        — 获取扩展信息
    -   [ReflectionFunctionAbstract::getExtensionName](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getExtensionName)
        — 获取扩展名称
    -   [ReflectionFunctionAbstract::getFileName](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getFileName)
        — 获取文件名称
    -   [ReflectionFunctionAbstract::getName](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getName)
        — 获取函数名称
    -   [ReflectionFunctionAbstract::getNamespaceName](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getNamespaceName)
        — 获取命名空间
    -   [ReflectionFunctionAbstract::getNumberOfParameters](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getNumberOfParameters)
        — 获取参数数目
    -   [ReflectionFunctionAbstract::getNumberOfRequiredParameters](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getNumberOfRequiredParameters)
        — 获取必须输入参数个数
    -   [ReflectionFunctionAbstract::getParameters](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getParameters)
        — 获取参数
    -   [ReflectionFunctionAbstract::getReturnType](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getReturnType)
        — Gets the specified return type of a function
    -   [ReflectionFunctionAbstract::getShortName](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getShortName)
        — 获取函数短名称
    -   [ReflectionFunctionAbstract::getStartLine](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getStartLine)
        — 获取开始行号
    -   [ReflectionFunctionAbstract::getStaticVariables](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::getStaticVariables)
        — 获取静态变量
    -   [ReflectionFunctionAbstract::hasReturnType](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::hasReturnType)
        — Checks if the function has a specified return type
    -   [ReflectionFunctionAbstract::inNamespace](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::inNamespace)
        — 检查是否处于命名空间
    -   [ReflectionFunctionAbstract::isClosure](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::isClosure)
        — 检查是否是匿名函数
    -   [ReflectionFunctionAbstract::isDeprecated](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::isDeprecated)
        — 检查是否已经弃用
    -   [ReflectionFunctionAbstract::isGenerator](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::isGenerator)
        — 判断函数是否是一个生成器函数
    -   [ReflectionFunctionAbstract::isInternal](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::isInternal)
        — 判断函数是否是内置函数
    -   [ReflectionFunctionAbstract::isUserDefined](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::isUserDefined)
        — 检查是否是用户定义
    -   [ReflectionFunctionAbstract::isVariadic](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::isVariadic)
        — Checks if the function is variadic
    -   [ReflectionFunctionAbstract::returnsReference](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::returnsReference)
        — 检查是否返回参考信息
    -   [ReflectionFunctionAbstract::\_\_toString](/class/reflectionfunctionabstract.html#ReflectionFunctionAbstract::__toString)
        — 字符串化
-   [ReflectionMethod](/class/reflectionmethod.html) — ReflectionMethod
    类
    -   [ReflectionMethod::\_\_construct](/class/reflectionmethod.html#ReflectionMethod::__construct)
        — ReflectionMethod 的构造函数
    -   [ReflectionMethod::export](/class/reflectionmethod.html#ReflectionMethod::export)
        — 输出一个回调方法
    -   [ReflectionMethod::getClosure](/class/reflectionmethod.html#ReflectionMethod::getClosure)
        —
        返回一个动态建立的方法调用接口，译者注：可以使用这个返回值直接调用非公开方法。
    -   [ReflectionMethod::getDeclaringClass](/class/reflectionmethod.html#ReflectionMethod::getDeclaringClass)
        — 获取反射函数调用参数的类表达
    -   [ReflectionMethod::getModifiers](/class/reflectionmethod.html#ReflectionMethod::getModifiers)
        — 获取方法的修饰符
    -   [ReflectionMethod::getPrototype](/class/reflectionmethod.html#ReflectionMethod::getPrototype)
        — 返回方法原型 (如果存在)
    -   [ReflectionMethod::invoke](/class/reflectionmethod.html#ReflectionMethod::invoke)
        — Invoke
    -   [ReflectionMethod::invokeArgs](/class/reflectionmethod.html#ReflectionMethod::invokeArgs)
        — 带参数执行
    -   [ReflectionMethod::isAbstract](/class/reflectionmethod.html#ReflectionMethod::isAbstract)
        — 判断方法是否是抽象方法
    -   [ReflectionMethod::isConstructor](/class/reflectionmethod.html#ReflectionMethod::isConstructor)
        — 判断方法是否是构造方法
    -   [ReflectionMethod::isDestructor](/class/reflectionmethod.html#ReflectionMethod::isDestructor)
        — 判断方法是否是析构方法
    -   [ReflectionMethod::isFinal](/class/reflectionmethod.html#ReflectionMethod::isFinal)
        — 判断方法是否定义 final
    -   [ReflectionMethod::isPrivate](/class/reflectionmethod.html#ReflectionMethod::isPrivate)
        — 判断方法是否是私有方法
    -   [ReflectionMethod::isProtected](/class/reflectionmethod.html#ReflectionMethod::isProtected)
        — 判断方法是否是保护方法 (protected)
    -   [ReflectionMethod::isPublic](/class/reflectionmethod.html#ReflectionMethod::isPublic)
        — 判断方法是否是公开方法
    -   [ReflectionMethod::isStatic](/class/reflectionmethod.html#ReflectionMethod::isStatic)
        — 判断方法是否是静态方法
    -   [ReflectionMethod::setAccessible](/class/reflectionmethod.html#ReflectionMethod::setAccessible)
        — 设置方法是否访问
    -   [ReflectionMethod::\_\_toString](/class/reflectionmethod.html#ReflectionMethod::__toString)
        — 返回反射方法对象的字符串表达
-   [ReflectionObject](/class/reflectionobject.html) — ReflectionObject
    类
    -   [ReflectionObject::\_\_construct](/class/reflectionobject.html#ReflectionObject::__construct)
        — Constructs a ReflectionObject
    -   [ReflectionObject::export](/class/reflectionobject.html#ReflectionObject::export)
        — Export
-   [ReflectionParameter](/class/reflectionparameter.html) —
    ReflectionParameter 类
    -   [ReflectionParameter::allowsNull](/class/reflectionparameter.html#ReflectionParameter::allowsNull)
        — Checks if null is allowed
    -   [ReflectionParameter::canBePassedByValue](/class/reflectionparameter.html#ReflectionParameter::canBePassedByValue)
        — Returns whether this parameter can be passed by value
    -   [ReflectionParameter::\_\_clone](/class/reflectionparameter.html#ReflectionParameter::__clone)
        — Clone
    -   [ReflectionParameter::\_\_construct](/class/reflectionparameter.html#ReflectionParameter::__construct)
        — Construct
    -   [ReflectionParameter::export](/class/reflectionparameter.html#ReflectionParameter::export)
        — Exports
    -   [ReflectionParameter::getClass](/class/reflectionparameter.html#ReflectionParameter::getClass)
        — 获得类型提示类。
    -   [ReflectionParameter::getDeclaringClass](/class/reflectionparameter.html#ReflectionParameter::getDeclaringClass)
        — Gets declaring class
    -   [ReflectionParameter::getDeclaringFunction](/class/reflectionparameter.html#ReflectionParameter::getDeclaringFunction)
        — Gets declaring function
    -   [ReflectionParameter::getDefaultValue](/class/reflectionparameter.html#ReflectionParameter::getDefaultValue)
        — Gets default parameter value
    -   [ReflectionParameter::getDefaultValueConstantName](/class/reflectionparameter.html#ReflectionParameter::getDefaultValueConstantName)
        — Returns the default value's constant name if default value is
        constant or null
    -   [ReflectionParameter::getName](/class/reflectionparameter.html#ReflectionParameter::getName)
        — Gets parameter name
    -   [ReflectionParameter::getPosition](/class/reflectionparameter.html#ReflectionParameter::getPosition)
        — Gets parameter position
    -   [ReflectionParameter::getType](/class/reflectionparameter.html#ReflectionParameter::getType)
        — Gets a parameter's type
    -   [ReflectionParameter::hasType](/class/reflectionparameter.html#ReflectionParameter::hasType)
        — Checks if parameter has a type
    -   [ReflectionParameter::isArray](/class/reflectionparameter.html#ReflectionParameter::isArray)
        — Checks if parameter expects an array
    -   [ReflectionParameter::isCallable](/class/reflectionparameter.html#ReflectionParameter::isCallable)
        — Returns whether parameter MUST be callable
    -   [ReflectionParameter::isDefaultValueAvailable](/class/reflectionparameter.html#ReflectionParameter::isDefaultValueAvailable)
        — 检查是否有默认值。
    -   [ReflectionParameter::isDefaultValueConstant](/class/reflectionparameter.html#ReflectionParameter::isDefaultValueConstant)
        — Returns whether the default value of this parameter is a
        constant
    -   [ReflectionParameter::isOptional](/class/reflectionparameter.html#ReflectionParameter::isOptional)
        — Checks if optional
    -   [ReflectionParameter::isPassedByReference](/class/reflectionparameter.html#ReflectionParameter::isPassedByReference)
        — Checks if passed by reference
    -   [ReflectionParameter::isVariadic](/class/reflectionparameter.html#ReflectionParameter::isVariadic)
        — Checks if the parameter is variadic
    -   [ReflectionParameter::\_\_toString](/class/reflectionparameter.html#ReflectionParameter::__toString)
        — To string
-   [ReflectionProperty](/class/reflectionproperty.html) —
    ReflectionProperty 类
    -   [ReflectionProperty::\_\_clone](/class/reflectionproperty.html#ReflectionProperty::__clone)
        — Clone
    -   [ReflectionProperty::\_\_construct](/class/reflectionproperty.html#ReflectionProperty::__construct)
        — Construct a ReflectionProperty object
    -   [ReflectionProperty::export](/class/reflectionproperty.html#ReflectionProperty::export)
        — Export
    -   [ReflectionProperty::getDeclaringClass](/class/reflectionproperty.html#ReflectionProperty::getDeclaringClass)
        — Gets declaring class
    -   [ReflectionProperty::getDocComment](/class/reflectionproperty.html#ReflectionProperty::getDocComment)
        — Gets the property doc comment
    -   [ReflectionProperty::getModifiers](/class/reflectionproperty.html#ReflectionProperty::getModifiers)
        — Gets the property modifiers
    -   [ReflectionProperty::getName](/class/reflectionproperty.html#ReflectionProperty::getName)
        — Gets property name
    -   [ReflectionProperty::getType](/class/reflectionproperty.html#ReflectionProperty::getType)
        — Gets a property's type
    -   [ReflectionProperty::getValue](/class/reflectionproperty.html#ReflectionProperty::getValue)
        — Gets value
    -   [ReflectionProperty::hasType](/class/reflectionproperty.html#ReflectionProperty::hasType)
        — Checks if property has a type
    -   [ReflectionProperty::isDefault](/class/reflectionproperty.html#ReflectionProperty::isDefault)
        — Checks if property is a default property
    -   [ReflectionProperty::isInitialized](/class/reflectionproperty.html#ReflectionProperty::isInitialized)
        — Checks whether a property is initialized
    -   [ReflectionProperty::isPrivate](/class/reflectionproperty.html#ReflectionProperty::isPrivate)
        — Checks if property is private
    -   [ReflectionProperty::isProtected](/class/reflectionproperty.html#ReflectionProperty::isProtected)
        — Checks if property is protected
    -   [ReflectionProperty::isPublic](/class/reflectionproperty.html#ReflectionProperty::isPublic)
        — Checks if property is public
    -   [ReflectionProperty::isStatic](/class/reflectionproperty.html#ReflectionProperty::isStatic)
        — Checks if property is static
    -   [ReflectionProperty::setAccessible](/class/reflectionproperty.html#ReflectionProperty::setAccessible)
        — Set property accessibility
    -   [ReflectionProperty::setValue](/class/reflectionproperty.html#ReflectionProperty::setValue)
        — Set property value
    -   [ReflectionProperty::\_\_toString](/class/reflectionproperty.html#ReflectionProperty::__toString)
        — To string
-   [ReflectionType](/class/reflectiontype.html) — The ReflectionType
    class
    -   [ReflectionType::allowsNull](/class/reflectiontype.html#ReflectionType::allowsNull)
        — Checks if null is allowed
    -   [ReflectionType::isBuiltin](/class/reflectiontype.html#ReflectionType::isBuiltin)
        — Checks if it is a built-in type
    -   [ReflectionType::\_\_toString](/class/reflectiontype.html#ReflectionType::__toString)
        — To string
-   [ReflectionGenerator](/class/reflectiongenerator.html) —
    生成器反射类
    -   [ReflectionGenerator::\_\_construct](/class/reflectiongenerator.html#ReflectionGenerator::__construct)
        — Constructs a ReflectionGenerator object
    -   [ReflectionGenerator::getExecutingFile](/class/reflectiongenerator.html#ReflectionGenerator::getExecutingFile)
        — Gets the file name of the currently executing generator
    -   [ReflectionGenerator::getExecutingGenerator](/class/reflectiongenerator.html#ReflectionGenerator::getExecutingGenerator)
        — Gets the executing Generator object
    -   [ReflectionGenerator::getExecutingLine](/class/reflectiongenerator.html#ReflectionGenerator::getExecutingLine)
        — Gets the currently executing line of the generator
    -   [ReflectionGenerator::getFunction](/class/reflectiongenerator.html#ReflectionGenerator::getFunction)
        — Gets the function name of the generator
    -   [ReflectionGenerator::getThis](/class/reflectiongenerator.html#ReflectionGenerator::getThis)
        — Gets the $this value of the generator
    -   [ReflectionGenerator::getTrace](/class/reflectiongenerator.html#ReflectionGenerator::getTrace)
        — Gets the trace of the executing generator
-   [Reflector](/class/reflector.html) — Reflector 接口
    -   [Reflector::export](/class/reflector.html#Reflector::export) —
        Exports
    -   [Reflector::\_\_toString](/class/reflector.html#Reflector::__toString)
        — 转化成字符串
-   [ReflectionException](/class/reflectionexception.html) —
    ReflectionException 类

简介
----

反射（reflection）类。

类摘要
------

**Reflection**

<span class="ooclass"> class **Reflection** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">export</span> ( <span class="methodparam"><span
class="type">Reflector</span> `$reflector`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$return`<span
class="initializer"> = false</span></span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getModifierNames</span> ( <span
class="methodparam"><span class="type">int</span> `$modifiers`</span> )

}

Reflection::export
==================

Exports

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Reflection::export</span> ( <span
class="methodparam"><span class="type">Reflector</span>
`$reflector`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$return`<span class="initializer"> =
false</span></span> \] )

导出一个反射（reflection）。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`reflector`  
导出的反射。

`return`  
设为 **`TRUE`** 时返回导出结果，设为 **`FALSE`**（默认值）则忽略返回。

### 返回值

如果参数 `return` 设为 **`TRUE`**，导出结果将作为 <span
class="type">string</span> 返回，否则返回 **`NULL`**。

### 参见

-   <span class="methodname">Reflection::getModifierNames</span>

Reflection::getModifierNames
============================

获取修饰符的名称

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Reflection::getModifierNames</span> ( <span
class="methodparam"><span class="type">int</span> `$modifiers`</span> )

获取修饰符的名称。

### 参数

`modifiers`  
根据标志位域获取修饰符。

### 返回值

修饰符名称的一个数组。

### 范例

**示例 \#1 <span class="methodname">Reflection::getModifierNames</span>
例子**

``` php
<?php
class Testing
{
    final public static function foo()
    {
        return;
    }

    public function bar()
    {
        return;
    }
}

$foo = new ReflectionMethod('Testing', 'foo');

echo "Modifiers for method foo():\n";
echo $foo->getModifiers() . "\n";
echo implode(' ', Reflection::getModifierNames($foo->getModifiers())) . "\n";

$bar = new ReflectionMethod('Testing', 'bar');

echo "Modifiers for method bar():\n";
echo $bar->getModifiers() . "\n";
echo implode(' ', Reflection::getModifierNames($bar->getModifiers()));
```

以上例程的输出类似于：

    Modifiers for method foo():
    261
    final public static
    Modifiers for method bar():
    65792
    public

### 参见

-   <span class="methodname">ReflectionClass::getModifiers</span>
-   <span
    class="methodname">ReflectionClassConstant::getModifiers</span>
-   <span class="methodname">ReflectionMethod::getModifiers</span>
-   <span class="methodname">ReflectionProperty::getModifiers</span>

简介
----

<span class="classname">ReflectionClass</span>
类报告了一个类的有关信息。

类摘要
------

**ReflectionClass**

<span class="ooclass"> class **ReflectionClass** </span> <span
class="oointerface">implements <span
class="interfacename">Reflector</span> </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionClass::IS_IMPLICIT_ABSTRACT` <span class="initializer"> =
16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionClass::IS_EXPLICIT_ABSTRACT` <span class="initializer"> =
32</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionClass::IS_FINAL` <span class="initializer"> = 64</span> ;

/\* 属性 \*/

<span class="modifier">public</span> `$name` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$argument`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">export</span> ( <span class="methodparam"><span
class="type">mixed</span> `$argument`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$return`<span
class="initializer"> = false</span></span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getConstant</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getConstants</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionMethod</span> <span
class="methodname">getConstructor</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getDefaultProperties</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getDocComment</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getEndLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionExtension</span> <span
class="methodname">getExtension</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getExtensionName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getFileName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getInterfaceNames</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getInterfaces</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionMethod</span> <span
class="methodname">getMethod</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getMethods</span> (\[ <span
class="methodparam"><span class="type">int</span> `$filter`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getModifiers</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getNamespaceName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">getParentClass</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getProperties</span> (\[ <span
class="methodparam"><span class="type">int</span> `$filter`</span> \] )

<span class="modifier">public</span> <span
class="type">ReflectionProperty</span> <span
class="methodname">getProperty</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="type">ReflectionClassConstant</span> <span
class="methodname">getReflectionConstant</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getReflectionConstants</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getShortName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getStartLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getStaticProperties</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getStaticPropertyValue</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`&$def_value`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getTraitAliases</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getTraitNames</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getTraits</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasConstant</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasMethod</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasProperty</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">implementsInterface</span> ( <span
class="methodparam"><span class="type">string</span> `$interface`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">inNamespace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isAbstract</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isAnonymous</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isCloneable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isFinal</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isInstance</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isInstantiable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isInterface</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isInternal</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isIterable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isIterateable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isSubclassOf</span> ( <span
class="methodparam"><span class="type">string</span> `$class`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isTrait</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isUserDefined</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">newInstance</span> ( <span
class="methodparam"><span class="type">mixed</span> `$args`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$...`</span>
\] )

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">newInstanceArgs</span> (\[ <span
class="methodparam"><span class="type">array</span> `$args`</span> \] )

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">newInstanceWithoutConstructor</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setStaticPropertyValue</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

属性
----

`name`  
类的名称。只读，并在尝试赋值的时候会抛出 <span
class="classname">ReflectionException</span>。

预定义常量
----------

ReflectionClass 修饰符
----------------------

**`ReflectionClass::IS_IMPLICIT_ABSTRACT`**  
指示了类是一个<a href="/language/oop5/abstract.html" class="link">抽象类（abstract）</a>，
因为它有抽象（abstract）方法。

**`ReflectionClass::IS_EXPLICIT_ABSTRACT`**  
指示了类是一个<a href="/language/oop5/abstract.html" class="link">抽象类（abstract）</a>，
因为它已明确定义。

**`ReflectionClass::IS_FINAL`**  
指示这是一个 <a href="/language/oop5/final.html" class="link">final</a>
类。

ReflectionClass::\_\_construct
==============================

初始化 ReflectionClass 类

### 说明

<span class="modifier">public</span> <span
class="methodname">ReflectionClass::\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$argument`</span> )

初始化新的 <span class="classname">ReflectionClass</span> 对象。

### 参数

`argument`  
既可以是包含类名的字符串（<span
class="type">string</span>）也可以是对象（<span
class="type">object</span>）。

### 返回值

返回初始化完成后的 <span class="classname">ReflectionClass</span> 实例。

### 错误／异常

如果要反射的 Class 不存在，抛出异常 <span
class="classname">ReflectionException</span>。

### 范例

**示例 \#1 ReflectionClass 的基本用法**

``` php
<?php
Reflection::export(new ReflectionClass('Exception'));
?>
```

以上例程的输出类似于：

    Class [ <internal:Core> class Exception ] {

      - Constants [0] {
      }

      - Static properties [0] {
      }

      - Static methods [0] {
      }

      - Properties [7] {
        Property [ <default> protected $message ]
        Property [ <default> private $string ]
        Property [ <default> protected $code ]
        Property [ <default> protected $file ]
        Property [ <default> protected $line ]
        Property [ <default> private $trace ]
        Property [ <default> private $previous ]
      }

      - Methods [10] {
        Method [ <internal:Core> final private method __clone ] {
        }

        Method [ <internal:Core, ctor> public method __construct ] {

          - Parameters [3] {
            Parameter #0 [ <optional> $message ]
            Parameter #1 [ <optional> $code ]
            Parameter #2 [ <optional> $previous ]
          }
        }

        Method [ <internal:Core> final public method getMessage ] {
        }

        Method [ <internal:Core> final public method getCode ] {
        }

        Method [ <internal:Core> final public method getFile ] {
        }

        Method [ <internal:Core> final public method getLine ] {
        }

        Method [ <internal:Core> final public method getTrace ] {
        }

        Method [ <internal:Core> final public method getPrevious ] {
        }

        Method [ <internal:Core> final public method getTraceAsString ] {
        }

        Method [ <internal:Core> public method __toString ] {
        }
      }
    }

### 参见

-   <span class="methodname">ReflectionObject::\_\_construct</span>
-   <a href="/language/oop5/decon.html#language.oop5.decon.constructor" class="link">Constructors</a>

ReflectionClass::export
=======================

导出一个类

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">ReflectionClass::export</span> ( <span
class="methodparam"><span class="type">mixed</span> `$argument`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$return`<span class="initializer"> = false</span></span> \] )

导出一个反射后的类。

### 参数

`argument`  
导出的反射。

`return`  
设为 **`TRUE`** 时返回导出结果，设为 **`FALSE`**（默认值）则忽略返回。

### 返回值

如果参数 `return` 设为 **`TRUE`**，导出结果将作为 <span
class="type">string</span> 返回，否则返回 **`NULL`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::export</span>
的基本用法**

``` php
<?php
class Apple {
    public $var1;
    public $var2 = 'Orange';

    public function type() {
        return 'Apple';
    }
}
ReflectionClass::export('Apple');
?>
```

以上例程的输出类似于：

    Class [ <user> class Apple ] {
      @@ php shell code 1-8

      - Constants [0] {
      }

      - Static properties [0] {
      }

      - Static methods [0] {
      }

      - Properties [2] {
        Property [ <default> public $var1 ]
        Property [ <default> public $var2 ]
      }

      - Methods [1] {
        Method [ <user> public method type ] {
          @@ php shell code 5 - 7
        }
      }
    }

### 参见

-   <span class="methodname">ReflectionClass::getName</span>

ReflectionClass::getConstant
============================

获取定义过的一个常量

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ReflectionClass::getConstant</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

获取定义过的一个常量。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  
常量的名称。

### 返回值

常量的值。

### 参见

-   <span class="methodname">ReflectionClass::getConstants</span>

ReflectionClass::getConstants
=============================

获取一组常量

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getConstants</span> ( <span
class="methodparam">void</span> )

获取某个类的全部已定义的常量，不管可见性如何定义。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

常量的<span
class="type">数组</span>，常量名是数组的键，常量的值是数组的值。

### 参见

-   <span class="methodname">ReflectionClass::getConstant</span>

ReflectionClass::getConstructor
===============================

获取类的构造函数

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionMethod</span> <span
class="methodname">ReflectionClass::getConstructor</span> ( <span
class="methodparam">void</span> )

获取已反射的类的构造函数。

### 参数

此函数没有参数。

### 返回值

一个 <span class="classname">ReflectionMethod</span>
对象，反射了类的构造函数，或者当类不存在构造函数时返回 **`NULL`**。

### 范例

**示例 \#1 <span
class="methodname">ReflectionClass::getConstructor</span> 的基本用法**

``` php
<?php
$class = new ReflectionClass('ReflectionClass');
$constructor = $class->getConstructor();
var_dump($constructor);
?>
```

以上例程会输出：

    object(ReflectionMethod)#2 (2) {
      ["name"]=>
      string(11) "__construct"
      ["class"]=>
      string(15) "ReflectionClass"
    }

### 参见

-   <span class="methodname">ReflectionClass::getName</span>

ReflectionClass::getDefaultProperties
=====================================

获取默认属性

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getDefaultProperties</span> (
<span class="methodparam">void</span> )

获取类的默认属性（包括了继承的属性）。

> **Note**:
>
> This method only works for static properties when used on internal
> classes. The default value of a static class property can not be
> tracked when using this method on user defined classes.

### 参数

此函数没有参数。

### 返回值

默认属性的<span
class="type">数组</span>，其键是属性的名称，其值是属性的默认值或者在属性没有默认值时是
**`NULL`**。 这个函数不区分静态和非静态属性，也不考虑可见性修饰符。

### 范例

**示例 \#1 <span
class="methodname">ReflectionClass::getDefaultProperties</span> 例子**

``` php
<?php
class Bar {
    protected $inheritedProperty = 'inheritedDefault';
}

class Foo extends Bar {
    public $property = 'propertyDefault';
    private $privateProperty = 'privatePropertyDefault';
    public static $staticProperty = 'staticProperty';
    public $defaultlessProperty;
}

$reflectionClass = new ReflectionClass('Foo');
var_dump($reflectionClass->getDefaultProperties());
?>
```

以上例程会输出：

    array(5) {
       ["staticProperty"]=>
       string(14) "staticProperty"
       ["property"]=>
       string(15) "propertyDefault"
       ["privateProperty"]=>
       string(22) "privatePropertyDefault"
       ["defaultlessProperty"]=>
       NULL
       ["inheritedProperty"]=>
       string(16) "inheritedDefault"
    }

### 参见

-   <span class="methodname">ReflectionClass::getProperties</span>
-   <span class="methodname">ReflectionClass::getStaticProperties</span>
-   <span class="methodname">ReflectionClass::getProperty</span>

ReflectionClass::getDocComment
==============================

获取文档注释

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::getDocComment</span> ( <span
class="methodparam">void</span> )

从一个类中获取文档注释。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

如果存在则返回文档注释，否则返回 **`FALSE`**。

### 范例

**示例 \#1 <span
class="methodname">ReflectionClass::getDocComment</span> 例子**

``` php
<?php
/** 
* A test class
*
* @param  foo bar
* @return baz
*/
class TestClass { }

$rc = new ReflectionClass('TestClass');
var_dump($rc->getDocComment())
?>
```

以上例程会输出：

    string(55) "/** 
    * A test class
    *
    * @param  foo bar
    * @return baz
    */"

### 参见

-   <span class="methodname">ReflectionClass::getName</span>

ReflectionClass::getEndLine
===========================

获取最后一行的行数

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionClass::getEndLine</span> ( <span
class="methodparam">void</span> )

从用户定义的类获取其最后一行的行数。

### 参数

此函数没有参数。

### 返回值

返回用户定义的类最后一行的行数，如果未知则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::getEndLine</span>
例子**

``` php
<?php
// Test Class
class TestClass { }

$rc = new ReflectionClass('TestClass');

echo $rc->getEndLine();
?>
```

以上例程会输出：

    3

### 参见

-   <span class="methodname">ReflectionClass::getStartLine</span>

ReflectionClass::getExtension
=============================

根据已定义的类获取所在扩展的 <span
class="classname">ReflectionExtension</span> 对象

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionExtension</span> <span
class="methodname">ReflectionClass::getExtension</span> ( <span
class="methodparam">void</span> )

获取已定义类的扩展的 <span class="classname">ReflectionExtension</span>
对象。

### 参数

此函数没有参数。

### 返回值

类所处的扩展的 <span class="classname">ReflectionExtension</span>
对象的表示，如果是用户定义的类则返回 **`NULL`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::getExtension</span>
的基本用法**

``` php
<?php
$class = new ReflectionClass('ReflectionClass');
$extension = $class->getExtension();
var_dump($extension);
?>
```

以上例程会输出：

    object(ReflectionExtension)#2 (1) {
      ["name"]=>
      string(10) "Reflection"
    }

### 参见

-   <span class="methodname">ReflectionClass::getExtensionName</span>

ReflectionClass::getExtensionName
=================================

获取定义的类所在的扩展的名称

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::getExtensionName</span> (
<span class="methodparam">void</span> )

获取定义的类所在的扩展的名称。

### 参数

此函数没有参数。

### 返回值

获取定义的类所在的扩展的名称，如果是用户定义的类，则返回 **`FALSE`**。

### 范例

**示例 \#1 <span
class="methodname">ReflectionClass::getExtensionName</span> 的基本用法**

``` php
<?php
$class = new ReflectionClass('ReflectionClass');
$extension = $class->getExtensionName();
var_dump($extension);
?>
```

以上例程会输出：

    string(10) "Reflection"

### 参见

-   <span class="methodname">ReflectionClass::getExtension</span>

ReflectionClass::getFileName
============================

获取定义类的文件名

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::getFileName</span> ( <span
class="methodparam">void</span> )

获取类被定义的文件的文件名。

### 参数

此函数没有参数。

### 返回值

返回类所定义的文件名。如果这个类是在 PHP 核心或 PHP 扩展中定义的，则返回
**`FALSE`**。

### 参见

-   <span class="methodname">ReflectionClass::getExtensionName</span>

ReflectionClass::getInterfaceNames
==================================

获取接口（interface）名称

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getInterfaceNames</span> (
<span class="methodparam">void</span> )

获取接口（interface）名称。

### 参数

此函数没有参数。

### 返回值

一个数值数组，接口（interface）的名称是数组的值。

### 范例

**示例 \#1 <span
class="methodname">ReflectionClass::getInterfaceNames</span> 例子**

``` php
<?php
interface Foo { }

interface Bar { }

class Baz implements Foo, Bar { }

$rc1 = new ReflectionClass("Baz");

print_r($rc1->getInterfaceNames());
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => Foo
        [1] => Bar
    )

### 参见

-   <span class="methodname">ReflectionClass::getInterfaces</span>

ReflectionClass::getInterfaces
==============================

获取接口

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getInterfaces</span> ( <span
class="methodparam">void</span> )

获取接口。

### 参数

此函数没有参数。

### 返回值

接口的关联<span
class="type">数组</span>，数组键是接口（interface）的名称，数组的值是
<span class="classname">ReflectionClass</span> 对象。

### 范例

**示例 \#1 <span
class="methodname">ReflectionClass::getInterfaces</span> 例子**

``` php
<?php
interface Foo { }

interface Bar { }

class Baz implements Foo, Bar { }

$rc1 = new ReflectionClass("Baz");

print_r($rc1->getInterfaces());
?>
```

以上例程的输出类似于：

    Array
    (
        [Foo] => ReflectionClass Object
            (
                [name] => Foo
            )

        [Bar] => ReflectionClass Object
            (
                [name] => Bar
            )

    )

### 参见

-   <span class="methodname">ReflectionClass::getInterfaceNames</span>

ReflectionClass::getMethod
==========================

获取一个类方法的 <span class="classname">ReflectionMethod</span>。

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionMethod</span> <span
class="methodname">ReflectionClass::getMethod</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

获取一个类方法的 <span class="classname">ReflectionMethod</span>。

### 参数

`name`  
要反射的方法名称。

### 返回值

一个 <span class="classname">ReflectionMethod</span>。

### 错误／异常

如果方法不存在则会抛出 <span
class="classname">ReflectionException</span> 异常。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::getMethod</span>
的基本用法**

``` php
<?php
$class = new ReflectionClass('ReflectionClass');
$method = $class->getMethod('getMethod');
var_dump($method);
?>
```

以上例程会输出：

    object(ReflectionMethod)#2 (2) {
      ["name"]=>
      string(9) "getMethod"
      ["class"]=>
      string(15) "ReflectionClass"
    }

### 参见

-   <span class="methodname">ReflectionClass::getMethods</span>

ReflectionClass::getMethods
===========================

获取方法的数组

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getMethods</span> (\[ <span
class="methodparam"><span class="type">int</span> `$filter`</span> \] )

获取类的方法的一个数组。

### 参数

`filter`  
过滤结果为仅包含某些属性的方法。默认不过滤。

**`ReflectionMethod::IS_STATIC`**、 **`ReflectionMethod::IS_PUBLIC`**、
**`ReflectionMethod::IS_PROTECTED`**、
**`ReflectionMethod::IS_PRIVATE`**、
**`ReflectionMethod::IS_ABSTRACT`**、 **`ReflectionMethod::IS_FINAL`**
的按位或（OR），就会返回*任意*满足条件的属性。

> **Note**: <span class="simpara"> 请注意：其他位操作，例如 *\~*
> 无法按预期运行。这个例子也就是说，无法获取所有的非静态方法。 </span>

### 返回值

包含每个方法 <span class="classname">ReflectionMethod</span> 对象的<span
class="type">数组</span>。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::getMethods</span>
的基本用法**

``` php
<?php
class Apple {
    public function firstMethod() { }
    final protected function secondMethod() { }
    private static function thirdMethod() { }
}

$class = new ReflectionClass('Apple');
$methods = $class->getMethods();
var_dump($methods);
?>
```

以上例程会输出：

    array(3) {
      [0]=>
      &object(ReflectionMethod)#2 (2) {
        ["name"]=>
        string(11) "firstMethod"
        ["class"]=>
        string(5) "Apple"
      }
      [1]=>
      &object(ReflectionMethod)#3 (2) {
        ["name"]=>
        string(12) "secondMethod"
        ["class"]=>
        string(5) "Apple"
      }
      [2]=>
      &object(ReflectionMethod)#4 (2) {
        ["name"]=>
        string(11) "thirdMethod"
        ["class"]=>
        string(5) "Apple"
      }
    }

**示例 \#2 从 <span
class="methodname">ReflectionClass::getMethods</span> 中过滤结果**

``` php
<?php
class Apple {
    public function firstMethod() { }
    final protected function secondMethod() { }
    private static function thirdMethod() { }
}

$class = new ReflectionClass('Apple');
$methods = $class->getMethods(ReflectionMethod::IS_STATIC | ReflectionMethod::IS_FINAL);
var_dump($methods);
?>
```

以上例程会输出：

    array(2) {
      [0]=>
      &object(ReflectionMethod)#2 (2) {
        ["name"]=>
        string(12) "secondMethod"
        ["class"]=>
        string(5) "Apple"
      }
      [1]=>
      &object(ReflectionMethod)#3 (2) {
        ["name"]=>
        string(11) "thirdMethod"
        ["class"]=>
        string(5) "Apple"
      }
    }

### 参见

-   <span class="methodname">ReflectionClass::getMethod</span>
-   <span class="function">get\_class\_methods</span>

ReflectionClass::getModifiers
=============================

获取类的修饰符

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionClass::getModifiers</span> ( <span
class="methodparam">void</span> )

返回这个类访问修饰符的位字段。

### 参数

此函数没有参数。

### 返回值

返回
<a href="/class/reflectionclass.html#ReflectionClass%20修饰符" class="link">修饰符常量</a>
的位掩码。

### 参见

-   <span class="methodname">ReflectionClass::getProperties</span>
-   <span class="methodname">Reflection::getModifierNames</span>

ReflectionClass::getName
========================

获取类名

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::getName</span> ( <span
class="methodparam">void</span> )

获取类的名称。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The class name.

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::getName</span>
例子**

``` php
<?php
namespace A\B;

class Foo { }

$function = new \ReflectionClass('stdClass');

var_dump($function->inNamespace());
var_dump($function->getName());
var_dump($function->getNamespaceName());
var_dump($function->getShortName());

$function = new \ReflectionClass('A\\B\\Foo');

var_dump($function->inNamespace());
var_dump($function->getName());
var_dump($function->getNamespaceName());
var_dump($function->getShortName());
?>
```

以上例程会输出：

    bool(false)
    string(8) "stdClass"
    string(0) ""
    string(8) "stdClass"

    bool(true)
    string(7) "A\B\Foo"
    string(3) "A\B"
    string(3) "Foo"

### 参见

-   <span class="methodname">ReflectionClass::getNamespaceName</span>

ReflectionClass::getNamespaceName
=================================

获取命名空间的名称

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::getNamespaceName</span> (
<span class="methodparam">void</span> )

获取命名空间（namespace）的名称。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

命名空间的名称。

### 范例

**示例 \#1 <span
class="methodname">ReflectionClass::getNamespaceName</span> 例子**

``` php
<?php
namespace A\B;

class Foo { }

$class = new \ReflectionClass('stdClass');

var_dump($class->inNamespace());
var_dump($class->getName());
var_dump($class->getNamespaceName());
var_dump($class->getShortName());

$class = new \ReflectionClass('A\\B\\Foo');

var_dump($class->inNamespace());
var_dump($class->getName());
var_dump($class->getNamespaceName());
var_dump($class->getShortName());
?>
```

以上例程会输出：

    bool(false)
    string(8) "stdClass"
    string(0) ""
    string(8) "stdClass"

    bool(true)
    string(7) "A\B\Foo"
    string(3) "A\B"
    string(3) "Foo"

### 参见

-   <span class="methodname">ReflectionClass::getParentClass</span>
-   <a href="/language/namespaces.html" class="link">namespaces</a>

ReflectionClass::getParentClass
===============================

获取父类

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">ReflectionClass::getParentClass</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

一个 <span class="classname">ReflectionClass</span>。

### 参见

-   <span class="methodname">ReflectionClass::\_\_construct</span>

ReflectionClass::getProperties
==============================

获取一组属性

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getProperties</span> (\[ <span
class="methodparam"><span class="type">int</span> `$filter`</span> \] )

获取反射过的属性。

### 参数

`filter`  
可选的过滤器，过滤为所需类型的属性。它使用
<a href="/class/reflectionproperty.html#ReflectionProperty%20修饰符" class="link">ReflectionProperty 常量</a>
来配置，默认获取所有类型的属性。

### 返回值

<span class="classname">ReflectionProperty</span> 对象的数组。

### 范例

**示例 \#1 <span class="function">ReflectionClass::getProperties</span>
过滤例子**

这个例子延时了可选 `filter` 参数的用法，例子里实际上忽略了私有属性。

``` php
<?php
class Foo {
    public    $foo  = 1;
    protected $bar  = 2;
    private   $baz  = 3;
}

$foo = new Foo();

$reflect = new ReflectionClass($foo);
$props   = $reflect->getProperties(ReflectionProperty::IS_PUBLIC | ReflectionProperty::IS_PROTECTED);

foreach ($props as $prop) {
    print $prop->getName() . "\n";
}

var_dump($props);

?>
```

以上例程的输出类似于：

    foo
    bar
    array(2) {
      [0]=>
      object(ReflectionProperty)#3 (2) {
        ["name"]=>
        string(3) "foo"
        ["class"]=>
        string(3) "Foo"
      }
      [1]=>
      object(ReflectionProperty)#4 (2) {
        ["name"]=>
        string(3) "bar"
        ["class"]=>
        string(3) "Foo"
      }
    }

### 参见

-   <span class="methodname">ReflectionClass::getProperty</span>
-   <span class="classname">ReflectionProperty</span>
-   <a href="/class/reflectionproperty.html#ReflectionProperty%20修饰符" class="link">ReflectionProperty 修饰符常量</a>

ReflectionClass::getProperty
============================

获取类的一个属性的 <span class="classname">ReflectionProperty</span>

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionProperty</span> <span
class="methodname">ReflectionClass::getProperty</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

获取类的一个属性的 <span class="classname">ReflectionProperty</span>。

### 参数

`name`  
属性名。

### 返回值

一个 <span class="classname">ReflectionProperty</span>。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::getProperty</span>
的基本用法**

``` php
<?php
$class = new ReflectionClass('ReflectionClass');
$property = $class->getProperty('name');
var_dump($property);
?>
```

以上例程会输出：

    object(ReflectionProperty)#2 (2) {
      ["name"]=>
      string(4) "name"
      ["class"]=>
      string(15) "ReflectionClass"
    }

### 参见

-   <span class="methodname">ReflectionClass::getProperties</span>

ReflectionClass::getReflectionConstant
======================================

Gets a <span class="classname">ReflectionClassConstant</span> for a
class's constant

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionClassConstant</span> <span
class="methodname">ReflectionClass::getReflectionConstant</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Gets a <span class="classname">ReflectionClassConstant</span> for a
class's property.

### 参数

`name`  
The class constant name.

### 返回值

A <span class="classname">ReflectionClassConstant</span>.

### 参见

-   <span
    class="methodname">ReflectionClass::getReflectionConstants</span>
-   <span class="classname">ReflectionClassConstant</span>

ReflectionClass::getReflectionConstants
=======================================

Gets class constants

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getReflectionConstants</span>
( <span class="methodparam">void</span> )

Retrieves reflected constants.

### 参数

此函数没有参数。

### 返回值

An array of <span class="classname">ReflectionClassConstant</span>
objects.

### 范例

**示例 \#1 Basic <span
class="function">ReflectionClass::getReflectionConstants</span>
example**

``` php
<?php
class Foo {
    public    const FOO  = 1;
    protected const BAR  = 2;
    private   const BAZ  = 3;
}

$foo = new Foo();

$reflect = new ReflectionClass($foo);
$consts  = $reflect->getReflectionConstants();

foreach ($consts as $const) {
    print $const->getName() . "\n";
}

var_dump($consts);

?>
```

以上例程的输出类似于：

    FOO
    BAR
    BAZ
    array(3) {
      [0]=>
      object(ReflectionClassConstant)#3 (2) {
        ["name"]=>
        string(3) "FOO"
        ["class"]=>
        string(3) "Foo"
      }
      [1]=>
      object(ReflectionClassConstant)#4 (2) {
        ["name"]=>
        string(3) "BAR"
        ["class"]=>
        string(3) "Foo"
      }
      [2]=>
      object(ReflectionClassConstant)#5 (2) {
        ["name"]=>
        string(3) "BAZ"
        ["class"]=>
        string(3) "Foo"
      }
    }

### 参见

-   <span
    class="methodname">ReflectionClass::getReflectionConstant</span>
-   <span class="classname">ReflectionClassConstant</span>

ReflectionClass::getShortName
=============================

获取短名

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::getShortName</span> ( <span
class="methodparam">void</span> )

获取类的短名，就是不含命名空间（namespace）的那一部分。

### 参数

此函数没有参数。

### 返回值

类的短名。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::getShortName</span>
例子**

``` php
<?php
namespace A\B;

class Foo { }

$function = new \ReflectionClass('stdClass');

var_dump($function->inNamespace());
var_dump($function->getName());
var_dump($function->getNamespaceName());
var_dump($function->getShortName());

$function = new \ReflectionClass('A\\B\\Foo');

var_dump($function->inNamespace());
var_dump($function->getName());
var_dump($function->getNamespaceName());
var_dump($function->getShortName());
?>
```

以上例程会输出：

    bool(false)
    string(8) "stdClass"
    string(0) ""
    string(8) "stdClass"

    bool(true)
    string(7) "A\B\Foo"
    string(3) "A\B"
    string(3) "Foo"

### 参见

-   <span class="methodname">ReflectionClass::getName</span>

ReflectionClass::getStartLine
=============================

获取起始行号

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionClass::getStartLine</span> ( <span
class="methodparam">void</span> )

获取起始的行号。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

起始的行号，类型是 <span class="type">integer</span> 的。

### 参见

-   <span class="methodname">ReflectionClass::getEndLine</span>

ReflectionClass::getStaticProperties
====================================

获取静态（static）属性

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getStaticProperties</span> (
<span class="methodparam">void</span> )

获取静态（static）属性。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

静态（static）的属性，类型是 <span class="type">array</span>。

### 参见

-   <span
    class="methodname">ReflectionClass::getStaticPropertyValue</span>
-   <span
    class="methodname">ReflectionClass::setStaticPropertyValue</span>

ReflectionClass::getStaticPropertyValue
=======================================

获取静态（static）属性的值

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ReflectionClass::getStaticPropertyValue</span>
( <span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `&$def_value`</span> \] )

获取这个类里静态（static）属性的值。

### 参数

`name`  
静态属性的名称，来返回它的值。

`def_value`  
假如类没有定义 `name` 的 static 属性，将返回一个默认值。
如果属性不存在，并且省略了此参数，将会抛出 <span
class="classname">ReflectionException</span> 。

### 返回值

静态属性的值。

### 范例

**示例 \#1 <span
class="methodname">ReflectionClass::getStaticPropertyValue</span>
的基本用法**

``` php
<?php
class Apple {
    public static $color = 'Red';
}

$class = new ReflectionClass('Apple');
var_dump($class->getStaticPropertyValue('color'));
?>
```

以上例程会输出：

    string(3) "Red"

### 参见

-   <span class="methodname">ReflectionClass::getStaticProperties</span>
-   <span
    class="methodname">ReflectionClass::setStaticPropertyValue</span>

ReflectionClass::getTraitAliases
================================

返回 trait 别名的一个数组

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getTraitAliases</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

返回了一个数组，新的方法名位于键中，原始名称（格式是
*"TraitName::original"*）位于数组的值中。 出现一个错误的情况下返回
**`NULL`**。

ReflectionClass::getTraitNames
==============================

返回这个类所使用 traits 的名称的数组

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getTraitNames</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

返回的数组的值包含了 trait 的名称。 出现错误的情况下返回 **`NULL`**。

ReflectionClass::getTraits
==========================

返回这个类所使用的 traits 数组

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getTraits</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

返回了一个数组，键是 trait 的名称，值是 trait 实例的 <span
class="classname">ReflectionClass</span>。 出现错误的情况下返回
**`NULL`**。

ReflectionClass::hasConstant
============================

检查常量是否已经定义

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::hasConstant</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

检查类中是否已经定义了指定的常量。

### 参数

`name`  
要被检查的常量名称。

### 返回值

如果已定义返回 **`TRUE`**，否则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::hasConstant</span>
例子**

``` php
<?php
class Foo {
    const c1 = 1;
}

$class = new ReflectionClass("Foo");

var_dump($class->hasConstant("c1"));
var_dump($class->hasConstant("c2"));
?>
```

以上例程的输出类似于：

    bool(true)
    bool(false)

### 参见

-   <span class="methodname">ReflectionClass::hasMethod</span>
-   <span class="methodname">ReflectionClass::hasProperty</span>

ReflectionClass::hasMethod
==========================

检查方法是否已定义

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::hasMethod</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

检查一个类中指定的方法是否已定义。

### 参数

`name`  
要检查的方法的名称。

### 返回值

如果有这个方法返回 **`TRUE`**，否则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::hasMethod</span>
例子**

``` php
<?php
Class C {
    public function publicFoo() {
        return true;
    }

    protected function protectedFoo() {
        return true;
    }

    private function privateFoo() {
        return true;
    }

    static function staticFoo() {
        return true;
    }
}

$rc = new ReflectionClass("C");

var_dump($rc->hasMethod('publicFoo'));

var_dump($rc->hasMethod('protectedFoo'));

var_dump($rc->hasMethod('privateFoo'));

var_dump($rc->hasMethod('staticFoo'));

// C should not have method bar
var_dump($rc->hasMethod('bar'));

// Method names are case insensitive
var_dump($rc->hasMethod('PUBLICfOO'));
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(true)
    bool(true)
    bool(false)
    bool(true)

### 参见

-   <span class="methodname">ReflectionClass::hasConstant</span>
-   <span class="methodname">ReflectionClass::hasProperty</span>

ReflectionClass::hasProperty
============================

检查属性是否已定义

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::hasProperty</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

检查指定的属性是否已定义。

### 参数

`name`  
待检查的属性的名称。

### 返回值

如果有这个属性返回 **`TRUE`**，否则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::hasProperty</span>
例子**

``` php
<?php
class Foo {
    public    $p1;
    protected $p2;
    private   $p3;

}

$obj = new ReflectionObject(new Foo());

var_dump($obj->hasProperty("p1"));
var_dump($obj->hasProperty("p2"));
var_dump($obj->hasProperty("p3"));
var_dump($obj->hasProperty("p4"));
?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    bool(true)
    bool(false)

### 参见

-   <span class="methodname">ReflectionClass::hasConstant</span>
-   <span class="methodname">ReflectionClass::hasMethod</span>

ReflectionClass::implementsInterface
====================================

接口的实现

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::implementsInterface</span> (
<span class="methodparam"><span class="type">string</span>
`$interface`</span> )

检查它是否实现了一个接口（interface）。

### 参数

`interface`  
接口（interface）的名称。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">ReflectionClass::isInterface</span>
-   <span class="methodname">ReflectionClass::isSubclassOf</span>
-   <span class="function">interface\_exists</span>
-   <a href="/language/oop5/interfaces.html" class="link">Object Interfaces</a>

ReflectionClass::inNamespace
============================

检查是否位于命名空间中

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::inNamespace</span> ( <span
class="methodparam">void</span> )

检查这个类是否定义于一个命名空间中里。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::inNamespace</span>
例子**

``` php
<?php
namespace A\B;

class Foo { }

$function = new \ReflectionClass('stdClass');

var_dump($function->inNamespace());
var_dump($function->getName());
var_dump($function->getNamespaceName());
var_dump($function->getShortName());

$function = new \ReflectionClass('A\\B\\Foo');

var_dump($function->inNamespace());
var_dump($function->getName());
var_dump($function->getNamespaceName());
var_dump($function->getShortName());
?>
```

以上例程会输出：

    bool(false)
    string(8) "stdClass"
    string(0) ""
    string(8) "stdClass"

    bool(true)
    string(7) "A\B\Foo"
    string(3) "A\B"
    string(3) "Foo"

### 参见

-   <span class="methodname">ReflectionClass::getNamespaceName</span>
-   <a href="/language/namespaces.html" class="link">PHP Namespaces</a>

ReflectionClass::isAbstract
===========================

检查类是否是抽象类（abstract）

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isAbstract</span> ( <span
class="methodparam">void</span> )

检查这个类是否是抽象类（abstract）。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::isAbstract</span>
例子**

``` php
<?php
class          TestClass { }
abstract class TestAbstractClass { }

$testClass     = new ReflectionClass('TestClass');
$abstractClass = new ReflectionClass('TestAbstractClass');

var_dump($testClass->isAbstract());
var_dump($abstractClass->isAbstract());
?>
```

以上例程会输出：

    bool(false)
    bool(true)

### 参见

-   <span class="methodname">ReflectionClass::isInterface</span>
-   <a href="/language/oop5/abstract.html" class="link">类的抽象</a>

ReflectionClass::isAnonymous
============================

检查类是否是匿名类

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isAnonymous</span> ( <span
class="methodparam">void</span> )

检查类是否是匿名类。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::isAnonymous</span>
example**

``` php
<?php
class TestClass {}
$anonClass = new class {};

$normalClass = new ReflectionClass('TestClass');
$anonClass  = new ReflectionClass($anonClass);

var_dump($normalClass->isAnonymous());
var_dump($anonClass->isAnonymous());

?>
```

以上例程会输出：

    bool(false)
    bool(true)

### 参见

-   <span class="methodname">ReflectionClass::isFinal</span>

ReflectionClass::isCloneable
============================

返回了一个类是否可复制

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isCloneable</span> ( <span
class="methodparam">void</span> )

返回了这个类是否可复制。

### 参数

此函数没有参数。

### 返回值

如果这个类可以复制返回 **`TRUE`**，否则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::isCloneable</span>
的基本用法**

``` php
<?php
class NotCloneable {
    public $var1;
    
    private function __clone() {
    }
}

class Cloneable {
    public $var1;
}

$notCloneable = new ReflectionClass('NotCloneable');
$cloneable = new ReflectionClass('Cloneable');

var_dump($notCloneable->isCloneable());
var_dump($cloneable->isCloneable());
?>
```

以上例程会输出：

    bool(false)
    bool(true)

ReflectionClass::isFinal
========================

检查类是否声明为 final

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isFinal</span> ( <span
class="methodparam">void</span> )

检查类是否声明为 final。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::isFinal</span>
例子**

``` php
<?php
class       TestClass { }
final class TestFinalClass { }

$normalClass = new ReflectionClass('TestClass');
$finalClass  = new ReflectionClass('TestFinalClass');

var_dump($normalClass->isFinal());
var_dump($finalClass->isFinal());

?>
```

以上例程会输出：

    bool(false)
    bool(true)

### 参见

-   <span class="methodname">ReflectionClass::isAbstract</span>
-   <a href="/language/oop5/final.html" class="link">Final 关键字</a>

ReflectionClass::isInstance
===========================

检查类的实例

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isInstance</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

检查对象是否为一个类的实例。

### 参数

`object`  
待比较的对象。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::isInstance</span>
相关例子**

``` php
<?php
// Example usage
$class = new ReflectionClass('Foo');

if ($class->isInstance($arg)) {
    echo "Yes";
}

// Equivalent to
if ($arg instanceof Foo) {
    echo "Yes";
}

// Equivalent to
if (is_a($arg, 'Foo')) {
    echo "Yes";
}
?>
```

以上例程的输出类似于：

    Yes
    Yes
    Yes

### 参见

-   <span class="methodname">ReflectionClass::isInterface</span>
-   <a href="/language/operators/type.html" class="link">类型运算符（instanceof）</a>
-   <a href="/language/oop5/interfaces.html" class="link">对象接口</a>
-   <span class="function">is\_a</span>

ReflectionClass::isInstantiable
===============================

检查类是否可实例化

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isInstantiable</span> ( <span
class="methodparam">void</span> )

检查这个类是否可实例化。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span
class="methodname">ReflectionClass::isInstantiable</span> 例子**

``` php
<?php
class C { }

interface iface {
    function f1();
}

class ifaceImpl implements iface {
    function f1() {}
}

abstract class abstractClass {
    function f1() { }
    abstract function f2();
}

class D extends abstractClass {
    function f2() { }
}

class privateConstructor {
    private function __construct() { }
}

$classes = array(
    "C",
    "iface",
    "ifaceImpl",
    "abstractClass",
    "D",
    "privateConstructor",
);

foreach($classes  as $class ) {
    $reflectionClass = new ReflectionClass($class);
    echo "Is $class instantiable?  ";
    var_dump($reflectionClass->IsInstantiable()); 
}

?>
```

以上例程会输出：

    Is C instantiable?  bool(true)
    Is iface instantiable?  bool(false)
    Is ifaceImpl instantiable?  bool(true)
    Is abstractClass instantiable?  bool(false)
    Is D instantiable?  bool(true)
    Is privateConstructor instantiable?  bool(false)

### 参见

-   <span class="methodname">ReflectionClass::isInstance</span>

ReflectionClass::isInterface
============================

检查类是否是一个接口（interface）

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isInterface</span> ( <span
class="methodparam">void</span> )

检查类是否是一个接口（interface）。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::isInterface</span>
基本用法**

``` php
<?php
interface SomeInterface {
    public function interfaceMethod();
}

$class = new ReflectionClass('SomeInterface');
var_dump($class->isInterface());
?>
```

以上例程会输出：

    bool(true)

### 参见

-   <span class="methodname">ReflectionClass::isInstance</span>

ReflectionClass::isInternal
===========================

检查类是否由扩展或核心在内部定义

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isInternal</span> ( <span
class="methodparam">void</span> )

检查类是否由扩展或核心在内部定义，与用户定义相反。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::isInternal</span>
的基本用法**

``` php
<?php
$internalclass = new ReflectionClass('ReflectionClass');

class Apple {}
$userclass = new ReflectionClass('Apple');

var_dump($internalclass->isInternal());
var_dump($userclass->isInternal());
?>
```

以上例程会输出：

    bool(true)
    bool(false)

### 参见

-   <span class="methodname">ReflectionClass::isUserDefined</span>

ReflectionClass::isIterable
===========================

Check whether this class is iterable

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isIterable</span> ( <span
class="methodparam">void</span> )

Check whether this class is iterable (i.e. can be used inside
<a href="/control-structures/foreach.html" class="link">foreach</a>).

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Basic <span
class="methodname">ReflectionClass::isIterable</span> Usage**

``` php
<?php

class IteratorClass implements Iterator {
    public function __construct() { }
    public function key() { }
    public function current() { }
    function next() { }
    function valid() { }
    function rewind() { }
}
class DerivedClass extends IteratorClass { }
class NonIterator { }

function dump_iterable($class) {
    $reflection = new ReflectionClass($class);
    var_dump($reflection->isIterable());
}

$classes = array("ArrayObject", "IteratorClass", "DerivedClass", "NonIterator");

foreach ($classes as $class) {
    echo "Is $class iterable? ";
    dump_iterable($class);
}
?>
```

以上例程会输出：

    Is ArrayObject iterable? bool(true)
    Is IteratorClass iterable? bool(true)
    Is DerivedClass iterable? bool(true)
    Is NonIterator iterable? bool(false)

### 参见

-   <span class="methodname">ReflectionClass::\_\_construct</span>

ReflectionClass::isIterateable
==============================

检查是否可迭代（iterateable）

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isIterateable</span> ( <span
class="methodparam">void</span> )

检查一个类是否可迭代（iterateable）。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span
class="methodname">ReflectionClass::isIterateable</span> 例子**

``` php
<?php

class IteratorClass implements Iterator {
    public function __construct() { }
    public function key() { }
    public function current() { }
    function next() { }
    function valid() { }
    function rewind() { }
}
class DerivedClass extends IteratorClass { }
class NonIterator { }

function dump_iterateable($class) {
    $reflection = new ReflectionClass($class);
    var_dump($reflection->isIterateable());
}

$classes = array("ArrayObject", "IteratorClass", "DerivedClass", "NonIterator");

foreach ($classes as $class) {
    echo "Is $class iterateable? ";
    dump_iterateable($class);
}
?>
```

以上例程会输出：

    Is ArrayObject iterateable? bool(true)
    Is IteratorClass iterateable? bool(true)
    Is DerivedClass iterateable? bool(true)
    Is NonIterator iterateable? bool(false)

### 参见

-   <span class="methodname">ReflectionClass::\_\_construct</span>

ReflectionClass::isSubclassOf
=============================

检查是否为一个子类

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isSubclassOf</span> ( <span
class="methodparam"><span class="type">string</span> `$class`</span> )

检查一个类是否为指定类的子类，或者实现了指定的接口。

### 参数

`class`  
被检查的类名。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">ReflectionClass::isInterface</span>
-   <span class="methodname">ReflectionClass::implementsInterface</span>
-   <span class="function">is\_subclass\_of</span>
-   <span class="function">get\_parent\_class</span>

ReflectionClass::isTrait
========================

返回了是否为一个 trait

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isTrait</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

如果是 trait 返回 **`TRUE`**，否则返回 **`FALSE`**。
在出现错误的情况下，将会返回 **`NULL`**。

ReflectionClass::isUserDefined
==============================

检查是否由用户定义的

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isUserDefined</span> ( <span
class="methodparam">void</span> )

检查一个类是否由用户定义，和内置相对。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">ReflectionClass::isInternal</span>

ReflectionClass::newInstance
============================

从指定的参数创建一个新的类实例

### 说明

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">ReflectionClass::newInstance</span> ( <span
class="methodparam"><span class="type">mixed</span> `$args`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$...`</span>
\] )

创建类的新的实例。给出的参数将会传递到类的构造函数。

### 参数

`args`  
接受可变数目的参数，用于传递到类的构造函数，和 <span
class="function">call\_user\_func</span> 很相似。

### 返回值

### 错误／异常

如果类的构造函数不是 public 的将会导致一个 <span
class="classname">ReflectionException</span>。

当 `args` 指定了一个或多个参数，而类不具有构造函数时,将导致一个 <span
class="classname">ReflectionException</span>。

### 参见

-   <span class="methodname">ReflectionClass::newInstanceArgs</span>
-   <span
    class="methodname">ReflectionClass::newInstanceWithoutConstructor</span>

ReflectionClass::newInstanceArgs
================================

从给出的参数创建一个新的类实例。

### 说明

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">ReflectionClass::newInstanceArgs</span> (\[
<span class="methodparam"><span class="type">array</span> `$args`</span>
\] )

创建一个类的新实例，给出的参数将传递到类的构造函数。

### 参数

`args`  
这个参数以 <span class="type">array</span> 形式传递到类的构造函数。

### 返回值

返回类的新实例。

### 范例

**示例 \#1 <span
class="methodname">ReflectionClass::newInstanceArgs</span> 的基本用法**

``` php
<?php
$class = new ReflectionClass('ReflectionFunction');
$instance = $class->newInstanceArgs(array('substr'));
var_dump($instance);
?>
```

以上例程会输出：

    object(ReflectionFunction)#2 (1) {
      ["name"]=>
      string(6) "substr"
    }

### 错误／异常

如果类的构造函数不是 public 的将导致产生一个 <span
class="classname">ReflectionException</span>。

当 `args` 指定了一个或多个参数，而类不具有构造函数时,将导致一个 <span
class="classname">ReflectionException</span>。

### 参见

-   <span class="methodname">ReflectionClass::newInstance</span>
-   <span
    class="methodname">ReflectionClass::newInstanceWithoutConstructor</span>

ReflectionClass::newInstanceWithoutConstructor
==============================================

创建一个新的类实例而不调用它的构造函数

### 说明

<span class="modifier">public</span> <span class="type">object</span>
<span
class="methodname">ReflectionClass::newInstanceWithoutConstructor</span>
( <span class="methodparam">void</span> )

创建一个新的类的实例而不调用它的构造函数。

### 参数

### 返回值

### 更新日志

| 版本  | 说明                                                                                                                               |
|-------|------------------------------------------------------------------------------------------------------------------------------------|
| 5.6.0 | All internal classes can now be instantiated except for those declared <a href="/language/oop5/final.html" class="link">final</a>. |

### 错误／异常

如果这个类是一个不能不调用构造函数来实例化的内置类，将导致一个 <span
class="classname">ReflectionException</span>。在 PHP 5.6.0
及更高版本中，此异常仅限于
<a href="/language/oop5/final.html" class="link">final</a> 的内置类。

### 参见

-   <span class="methodname">ReflectionClass::newInstance</span>
-   <span class="methodname">ReflectionClass::newInstanceArgs</span>

ReflectionClass::setStaticPropertyValue
=======================================

设置静态属性的值

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ReflectionClass::setStaticPropertyValue</span>
( <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

设置静态属性的值。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  
属性的名称。

`value`  
属性的值。

### 返回值

没有返回值。

### 参见

-   <span
    class="methodname">ReflectionClass::getStaticPropertyValue</span>

ReflectionClass::\_\_toString
=============================

返回 ReflectionClass 对象字符串的表示形式。

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::\_\_toString</span> ( <span
class="methodparam">void</span> )

返回 ReflectionClass 对象字符串的表示形式。

### 参数

此函数没有参数。

### 返回值

ReflectionClass 实例的一个字符串表示形式。

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::\_\_toString</span>
例子**

``` php
<?php
$reflectionClass = new ReflectionClass('Exception');
echo $reflectionClass->__toString();
?>
```

以上例程会输出：

    Class [ <internal:Core> class Exception ] {

      - Constants [0] {
      }

      - Static properties [0] {
      }

      - Static methods [0] {
      }

      - Properties [7] {
        Property [ <default> protected $message ]
        Property [ <default> private $string ]
        Property [ <default> protected $code ]
        Property [ <default> protected $file ]
        Property [ <default> protected $line ]
        Property [ <default> private $trace ]
        Property [ <default> private $previous ]
      }

      - Methods [10] {
        Method [ <internal:Core> final private method __clone ] {
        }

        Method [ <internal:Core, ctor> public method __construct ] {

          - Parameters [3] {
            Parameter #0 [ <optional> $message ]
            Parameter #1 [ <optional> $code ]
            Parameter #2 [ <optional> $previous ]
          }
        }

        Method [ <internal:Core> final public method getMessage ] {
        }

        Method [ <internal:Core> final public method getCode ] {
        }

        Method [ <internal:Core> final public method getFile ] {
        }

        Method [ <internal:Core> final public method getLine ] {
        }

        Method [ <internal:Core> final public method getTrace ] {
        }

        Method [ <internal:Core> final public method getPrevious ] {
        }

        Method [ <internal:Core> final public method getTraceAsString ] {
        }

        Method [ <internal:Core> public method __toString ] {
        }
      }
    }

### 参见

-   <span class="methodname">ReflectionClass::export</span>
-   <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>

简介
----

The <span class="classname">ReflectionClassConstant</span> class reports
information about a class constant.

类摘要
------

**ReflectionClassConstant**

<span class="ooclass"> class **ReflectionClassConstant** </span> <span
class="oointerface">implements <span
class="interfacename">Reflector</span> </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$name` ;

<span class="modifier">public</span> `$class` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$class`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">export</span> ( <span class="methodparam"><span
class="type">mixed</span> `$class`</span> , <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$return`</span> \] )

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">getDeclaringClass</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getDocComment</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getModifiers</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getValue</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isPrivate</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isProtected</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isPublic</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

属性
----

`name`  
Name of the class constant. Read-only, throws <span
class="classname">ReflectionException</span> in attempt to write.

`class`  
Name of the class where the class constant is defined. Read-only, throws
<span class="classname">ReflectionException</span> in attempt to write.

ReflectionClassConstant::\_\_construct
======================================

Constructs a ReflectionClassConstant

### 说明

<span class="modifier">public</span> <span
class="methodname">ReflectionClassConstant::\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$class`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

Constructs a new <span class="classname">ReflectionClassConstant</span>
object.

### 参数

`class`  
Either a <span class="type">string</span> containing the name of the
class to reflect, or an <span class="type">object</span>.

`name`  
The name of the class constant.

### 返回值

Returns constructed <span
class="classname">ReflectionClassConstant</span> instance.

### 错误／异常

Throws an <span class="classname">Exception</span> in case the given
class constant does not exist.

### 参见

-   <a href="/language/oop5/decon.html#language.oop5.decon.constructor" class="link">Constructors</a>

ReflectionClassConstant::export
===============================

Export

**Warning**

本函数已自 PHP 7.4.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">ReflectionClassConstant::export</span> ( <span
class="methodparam"><span class="type">mixed</span> `$class`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$return`</span> \] )

Exports a reflection.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`class`  
导出的反射。

`name`  
The class constant name.

`return`  
设为 **`TRUE`** 时返回导出结果，设为 **`FALSE`**（默认值）则忽略返回。

### 返回值

### 参见

-   <span
    class="methodname">ReflectionClassConstant::\_\_toString</span>

ReflectionClassConstant::getDeclaringClass
==========================================

Gets declaring class

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">ReflectionClassConstant::getDeclaringClass</span> (
<span class="methodparam">void</span> )

Gets the declaring class.

### 参数

此函数没有参数。

### 返回值

A <span class="classname">ReflectionClass</span> object.

ReflectionClassConstant::getDocComment
======================================

Gets doc comments

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClassConstant::getDocComment</span> (
<span class="methodparam">void</span> )

Gets doc comments from a class constant.

### 参数

此函数没有参数。

### 返回值

The doc comment if it exists, otherwise **`FALSE`**

ReflectionClassConstant::getModifiers
=====================================

Gets the class constant modifiers

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionClassConstant::getModifiers</span> ( <span
class="methodparam">void</span> )

Returns a bitfield of the access modifiers for this class constant.

### 参数

此函数没有参数。

### 返回值

A numeric representation of the modifiers. The actual meanings of these
modifiers are described in the
<a href="/class/reflectionmethod.html#ReflectionMethod%20修饰符" class="link">predefined constants</a>.

### 参见

-   <span class="methodname">Reflection::getModifierNames</span>

ReflectionClassConstant::getName
================================

Get name of the constant

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClassConstant::getName</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the constant's name.

ReflectionClassConstant::getValue
=================================

Gets value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ReflectionClassConstant::getValue</span> (
<span class="methodparam">void</span> )

Gets the class constant's value.

### 参数

此函数没有参数。

### 返回值

The value of the class constant.

ReflectionClassConstant::isPrivate
==================================

Checks if class constant is private

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClassConstant::isPrivate</span> (
<span class="methodparam">void</span> )

Checks if the class constant is private.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the class constant is private, otherwise **`FALSE`**

### 参见

-   <span class="methodname">ReflectionClassConstant::isPublic</span>
-   <span class="methodname">ReflectionClassConstant::isProtected</span>

ReflectionClassConstant::isProtected
====================================

Checks if class constant is protected

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClassConstant::isProtected</span> (
<span class="methodparam">void</span> )

Checks if the class constant is protected.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the class constant is protected, otherwise **`FALSE`**

### 参见

-   <span class="methodname">ReflectionClassConstant::isPublic</span>
-   <span class="methodname">ReflectionClassConstant::isPrivate</span>

ReflectionClassConstant::isPublic
=================================

Checks if class constant is public

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClassConstant::isPublic</span> (
<span class="methodparam">void</span> )

Checks if the class constant is public.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the class constant is public, otherwise **`FALSE`**

### 参见

-   <span class="methodname">ReflectionClassConstant::isPrivate</span>
-   <span class="methodname">ReflectionClassConstant::isProtected</span>

ReflectionClassConstant::\_\_toString
=====================================

Returns the string representation of the ReflectionClassConstant object

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClassConstant::\_\_toString</span> (
<span class="methodparam">void</span> )

Returns the string representation of the ReflectionClassConstant object.

### 参数

此函数没有参数。

### 返回值

A string representation of this <span
class="classname">ReflectionClassConstant</span> instance.

### 参见

-   <span class="methodname">ReflectionClassConstant::export</span>
-   <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>

简介
----

类摘要
------

**ReflectionZendExtension**

<span class="ooclass"> class **ReflectionZendExtension** </span> <span
class="oointerface">implements <span
class="interfacename">Reflector</span> </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$name` ;

/\* 方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">\_\_clone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">export</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$return`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getAuthor</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getCopyright</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getURL</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getVersion</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

属性
----

`name`  
扩展的名称。只读，并在尝试赋值的时候抛出 <span
class="classname">ReflectionException</span>。

ReflectionZendExtension::\_\_clone
==================================

Clone handler

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">ReflectionZendExtension::\_\_clone</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

ReflectionZendExtension::\_\_construct
======================================

Constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">ReflectionZendExtension::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

ReflectionZendExtension::export
===============================

Export

**Warning**

本函数已自 PHP 7.4.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">ReflectionZendExtension::export</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$return`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

`return`  

### 返回值

### 参见

-   <span
    class="methodname">ReflectionClassConstant::\_\_toString</span>

ReflectionZendExtension::getAuthor
==================================

Gets author

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionZendExtension::getAuthor</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

ReflectionZendExtension::getCopyright
=====================================

Gets copyright

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionZendExtension::getCopyright</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

ReflectionZendExtension::getName
================================

Gets name

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionZendExtension::getName</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

ReflectionZendExtension::getURL
===============================

Gets URL

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionZendExtension::getURL</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

ReflectionZendExtension::getVersion
===================================

Gets version

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionZendExtension::getVersion</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

ReflectionZendExtension::\_\_toString
=====================================

To string handler

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionZendExtension::\_\_toString</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

<span class="classname">ReflectionExtension</span>
报告了一个扩展（extension）的有关信息。

类摘要
------

**ReflectionExtension**

<span class="ooclass"> class **ReflectionExtension** </span> <span
class="oointerface">implements <span
class="interfacename">Reflector</span> </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$name` ;

/\* 方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">\_\_clone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">export</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> \[, <span
class="methodparam"><span class="type">string</span> `$return`<span
class="initializer"> = false</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getClasses</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getClassNames</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getConstants</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getDependencies</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getFunctions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getINIEntries</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getVersion</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">info</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isPersistent</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isTemporary</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

属性
----

`name`  
扩展的名称，和 <span
class="methodname">ReflectionExtension::getName</span>
方法所返回的一样。

ReflectionExtension::\_\_clone
==============================

Clones

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">ReflectionExtension::\_\_clone</span> ( <span
class="methodparam">void</span> )

clone方法阻止实例克隆。反射类实例不允许被克隆。

### 参数

此函数没有参数。

### 返回值

没有返回值，如果被调用将产生fatal错误。

### 参见

-   <span class="methodname">ReflectionExtension::\_\_construct</span>
-   <a href="/language/oop5/cloning.html" class="link">Object cloning</a>

ReflectionExtension::\_\_construct
==================================

Constructs a ReflectionExtension

### 说明

<span class="modifier">public</span> <span
class="methodname">ReflectionExtension::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Construct a <span class="classname">ReflectionExtension</span> <span
class="type">object</span>.

### 参数

`name`  
扩展的名称。

### 返回值

A <span class="classname">ReflectionExtension</span> <span
class="type">object</span>.

### 范例

**示例 \#1 <span class="classname">ReflectionExtension</span> example**

``` php
<?php
$ext = new ReflectionExtension('Reflection');

printf('Extension: %s (version: %s)', $ext->getName(), $ext->getVersion());
?>
```

以上例程的输出类似于：

    Extension: Reflection (version: $Revision: 338648 $)

### 参见

-   <span class="methodname">ReflectionExtension::info</span>
-   <a href="/language/oop5/decon.html#language.oop5.decon.constructor" class="link">Constructors</a>

ReflectionExtension::export
===========================

Export

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">ReflectionExtension::export</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$return`<span class="initializer"> = false</span></span> \] )

导出可以被反射的扩展。输出格式同CLI argument *--re \[extension\]*.

### 参数

`name`  
导出的反射。

`return`  
设为 **`TRUE`** 时返回导出结果，设为 **`FALSE`**（默认值）则忽略返回。

### 返回值

如果参数 `return` 设为 **`TRUE`**，导出结果将作为 <span
class="type">string</span> 返回，否则返回 **`NULL`**。

### 参见

-   <span class="methodname">ReflectionExtension::info</span>

ReflectionExtension::getClasses
===============================

Gets classes

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionExtension::getClasses</span> ( <span
class="methodparam">void</span> )

从扩展中获取类列表。

### 参数

此函数没有参数。

### 返回值

返回一个<span
class="classname">ReflectionClass</span>对象数组，包括扩展中所有类。如果扩展中没有类声明，将返回空数组。

### 范例

**示例 \#1 <span
class="methodname">ReflectionExtension::getClasses</span> example**

``` php
<?php
$ext = new ReflectionExtension('XMLWriter');
var_dump($ext->getClasses());
?>
```

以上例程的输出类似于：

    array(1) {
      ["XMLWriter"]=>
      &object(ReflectionClass)#2 (1) {
        ["name"]=>
        string(9) "XMLWriter"
      }
    }

### 参见

-   <span class="methodname">ReflectionExtension::getClassNames</span>

ReflectionExtension::getClassNames
==================================

获取类名称

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionExtension::getClassNames</span> (
<span class="methodparam">void</span> )

获取扩展中的类名称列表。

### 参数

此函数没有参数。

### 返回值

返回类名称数组。如果扩展中没有类声明，将返回空数组。

### 范例

**示例 \#1 <span
class="methodname">ReflectionExtension::getClassNames</span> example**

``` php
<?php
$ext = new ReflectionExtension('XMLWriter');
var_dump($ext->getClassNames());
?>
```

以上例程的输出类似于：

    array(1) {
      [0]=>
      string(9) "XMLWriter"
    }

### 参见

-   <span class="methodname">ReflectionExtension::getClasses</span>
-   <span class="methodname">ReflectionExtension::getName</span>

ReflectionExtension::getConstants
=================================

获取常量

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionExtension::getConstants</span> (
<span class="methodparam">void</span> )

获取扩展中定义的常量。

### 参数

此函数没有参数。

### 返回值

返回一个以常量名称为索引的数组。

### 范例

**示例 \#1 <span
class="methodname">ReflectionExtension::getConstants</span> example**

``` php
<?php
$ext = new ReflectionExtension('DOM');

print_r($ext->getConstants());
?>
```

以上例程的输出类似于：

    Array
    (
        [XML_ELEMENT_NODE] => 1
        [XML_ATTRIBUTE_NODE] => 2
        [XML_TEXT_NODE] => 3
        [XML_CDATA_SECTION_NODE] => 4
        [XML_ENTITY_REF_NODE] => 5
        [XML_ENTITY_NODE] => 6
        [XML_PI_NODE] => 7
        [XML_COMMENT_NODE] => 8
        [XML_DOCUMENT_NODE] => 9
        [XML_DOCUMENT_TYPE_NODE] => 10
        [XML_DOCUMENT_FRAG_NODE] => 11
        [XML_NOTATION_NODE] => 12
        [XML_HTML_DOCUMENT_NODE] => 13
        [XML_DTD_NODE] => 14
        [XML_ELEMENT_DECL_NODE] => 15
        [XML_ATTRIBUTE_DECL_NODE] => 16
        [XML_ENTITY_DECL_NODE] => 17
        [XML_NAMESPACE_DECL_NODE] => 18
        [XML_LOCAL_NAMESPACE] => 18
        [XML_ATTRIBUTE_CDATA] => 1
        [XML_ATTRIBUTE_ID] => 2
        [XML_ATTRIBUTE_IDREF] => 3
        [XML_ATTRIBUTE_IDREFS] => 4
        [XML_ATTRIBUTE_ENTITY] => 6
        [XML_ATTRIBUTE_NMTOKEN] => 7
        [XML_ATTRIBUTE_NMTOKENS] => 8
        [XML_ATTRIBUTE_ENUMERATION] => 9
        [XML_ATTRIBUTE_NOTATION] => 10
        [DOM_PHP_ERR] => 0
        [DOM_INDEX_SIZE_ERR] => 1
        [DOMSTRING_SIZE_ERR] => 2
        [DOM_HIERARCHY_REQUEST_ERR] => 3
        [DOM_WRONG_DOCUMENT_ERR] => 4
        [DOM_INVALID_CHARACTER_ERR] => 5
        [DOM_NO_DATA_ALLOWED_ERR] => 6
        [DOM_NO_MODIFICATION_ALLOWED_ERR] => 7
        [DOM_NOT_FOUND_ERR] => 8
        [DOM_NOT_SUPPORTED_ERR] => 9
        [DOM_INUSE_ATTRIBUTE_ERR] => 10
        [DOM_INVALID_STATE_ERR] => 11
        [DOM_SYNTAX_ERR] => 12
        [DOM_INVALID_MODIFICATION_ERR] => 13
        [DOM_NAMESPACE_ERR] => 14
        [DOM_INVALID_ACCESS_ERR] => 15
        [DOM_VALIDATION_ERR] => 16
    )

### 参见

-   <span class="methodname">ReflectionExtension::getINIEntries</span>

ReflectionExtension::getDependencies
====================================

获取依赖

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionExtension::getDependencies</span> (
<span class="methodparam">void</span> )

获取依赖，包括必需的、冲突的、可选的。 Gets dependencies, by listing
both required and conflicting dependencies.

### 参数

此函数没有参数。

### 返回值

返回一个以依赖的扩展名称为索引的数组，每一项的取值为
*Required*、*Optional* 或者 *Conflicts*。

### 范例

**示例 \#1 <span
class="methodname">ReflectionExtension::getDependencies</span> example**

``` php
<?php
$dom = new ReflectionExtension('dom');

print_r($dom->getDependencies());
?>
```

以上例程的输出类似于：

    Array
    (
        [libxml] => Required
        [domxml] => Conflicts
    )

### 参见

-   <span class="methodname">ReflectionClass::getVersion</span>

ReflectionExtension::getFunctions
=================================

获取扩展中的函数

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionExtension::getFunctions</span> (
<span class="methodparam">void</span> )

获取扩展中定义的函数。

### 参数

此函数没有参数。

### 返回值

返回一个<span
class="classname">ReflectionFunction</span>对象数组，数组索引为函数名。如果扩展中没有定义函数，将返回空数组。

### 范例

**示例 \#1 <span
class="methodname">ReflectionExtension::getFunctions</span> example**

``` php
<?php
$dom = new ReflectionExtension('SimpleXML');

print_r($dom->getFunctions());
?>
```

以上例程的输出类似于：

    Array
    (
        [simplexml_load_file] => ReflectionFunction Object
            (
                [name] => simplexml_load_file
            )

        [simplexml_load_string] => ReflectionFunction Object
            (
                [name] => simplexml_load_string
            )

        [simplexml_import_dom] => ReflectionFunction Object
            (
                [name] => simplexml_import_dom
            )

    )

### 参见

-   <span class="methodname">ReflectionExtension::getClasses</span>
-   <span class="function">get\_extension\_funcs</span>

ReflectionExtension::getINIEntries
==================================

获取ini配置

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionExtension::getINIEntries</span> (
<span class="methodparam">void</span> )

获取扩展在ini配置文件中的配置。

### 参数

此函数没有参数。

### 返回值

返回一个数组，数组索引是配置名称，值是配置值。

### 范例

**示例 \#1 <span
class="methodname">ReflectionExtension::getINIEntries</span> example**

``` php
<?php
$ext = new ReflectionExtension('mysql');

print_r($ext->getINIEntries());
?>
```

以上例程的输出类似于：

    Array
    (
        [mysql.allow_persistent] => 1
        [mysql.max_persistent] => -1
        [mysql.max_links] => -1
        [mysql.default_host] => 
        [mysql.default_user] => 
        [mysql.default_password] => 
        [mysql.default_port] => 
        [mysql.default_socket] => 
        [mysql.connect_timeout] => 60
        [mysql.trace_mode] => 
        [mysql.allow_local_infile] => 1
        [mysql.cache_size] => 2000
    )

### 参见

-   <span class="function">ini\_get\_all</span>
-   <span class="methodname">ReflectionExtension::getConstants</span>

ReflectionExtension::getName
============================

获取扩展名称

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionExtension::getName</span> ( <span
class="methodparam">void</span> )

获取扩展名称。

### 参数

此函数没有参数。

### 返回值

扩展名称。

### 范例

**示例 \#1 <span class="methodname">ReflectionExtension::getName</span>
example**

``` php
<?php
$ext = new ReflectionExtension('mysqli');
var_dump($ext->getName());
?>
```

以上例程的输出类似于：

    string(6) "mysqli"

### 参见

-   <span class="methodname">ReflectionExtension::getClassNames</span>

ReflectionExtension::getVersion
===============================

获取扩展版本号

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionExtension::getVersion</span> ( <span
class="methodparam">void</span> )

获取扩展的版本号。

### 参数

此函数没有参数。

### 返回值

扩展的版本号。

### 范例

**示例 \#1 <span
class="methodname">ReflectionExtension::getVersion</span> example**

``` php
<?php
$ext = new ReflectionExtension('mysqli');
var_dump($ext->getVersion());
?>
```

以上例程的输出类似于：

    string(3) "0.1"

### 参见

-   <span class="methodname">ReflectionExtension::info</span>

ReflectionExtension::info
=========================

输出扩展信息

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ReflectionExtension::info</span> ( <span
class="methodparam">void</span> )

输出“<span class="function">phpinfo</span>”信息中的扩展信息。

### 参数

此函数没有参数。

### 返回值

扩展信息。

### 范例

**示例 \#1 <span class="methodname">ReflectionExtension::info</span>
example**

``` php
<?php
$ext = new ReflectionExtension('mysqli');
$ext->info();
?>
```

以上例程的输出类似于：

    mysqli

    MysqlI Support => enabled
    Client API library version => mysqlnd 5.0.5-dev - 081106 - $Revision: 339009 $
    Active Persistent Links => 0
    Inactive Persistent Links => 0
    Active Links => 0
    Persistent cache => enabled
    put_hits => 0
    put_misses => 0
    get_hits => 0
    get_misses => 0
    size => 2000
    free_items => 2000
    references => 2

    Directive => Local Value => Master Value
    mysqli.max_links => Unlimited => Unlimited
    mysqli.max_persistent => Unlimited => Unlimited
    mysqli.allow_persistent => On => On
    mysqli.default_host => no value => no value
    mysqli.default_user => no value => no value
    mysqli.default_pw => no value => no value
    mysqli.default_port => 3306 => 3306
    mysqli.default_socket => no value => no value
    mysqli.reconnect => Off => Off
    mysqli.allow_local_infile => On => On
    mysqli.cache_size => 2000 => 2000

### 参见

-   <span class="methodname">ReflectionExtension::getName</span>
-   <span class="function">phpinfo</span>

ReflectionExtension::isPersistent
=================================

返回扩展是否持久化载入

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ReflectionExtension::isPersistent</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

扩展在<a href="/ini/core.html#ini.extension" class="link"><em>extension</em></a>配置中被载入返回**`TRUE`**
，否则返回 **`FALSE`**。

### 参见

-   <span class="methodname">ReflectionExtension::isTemporary</span>

ReflectionExtension::isTemporary
================================

返回扩展是否是临时载入

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ReflectionExtension::isTemporary</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

如果扩展被<span class="function">dl</span>载入则返回**`TRUE`**
，否则返回 **`FALSE`** 。

### 参见

-   <span class="methodname">ReflectionExtension::isPersistent</span>

ReflectionExtension::\_\_toString
=================================

To string

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionExtension::\_\_toString</span> (
<span class="methodparam">void</span> )

以<span class="type">string</span>形式返回扩展的反射信息。同 <span
class="methodname">ReflectionExtension::export</span>`return`参数设置为**`TRUE`**。

### 参数

此函数没有参数。

### 返回值

返回扩展的反射信息，同 <span
class="methodname">ReflectionExtension::export</span>。

### 参见

-   <span class="methodname">ReflectionExtension::\_\_construct</span>
-   <span class="methodname">ReflectionExtension::export</span>
-   <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>

简介
----

<span class="classname">ReflectionFunction</span>
类报告了一个函数的有关信息。

类摘要
------

**ReflectionFunction**

<span class="ooclass"> class **ReflectionFunction** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**ReflectionFunctionAbstract** </span> <span
class="oointerface">implements <span
class="interfacename">Reflector</span> </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionFunction::IS_DEPRECATED` <span class="initializer"> =
262144</span> ;

/\* 属性 \*/

<span class="modifier">public</span> `$name` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$name`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">export</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> \[, <span
class="methodparam"><span class="type">string</span> `$return`</span> \]
)

<span class="modifier">public</span> <span class="type">Closure</span>
<span class="methodname">getClosure</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">invoke</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">invokeArgs</span> ( <span
class="methodparam"><span class="type">array</span> `$args`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isDisabled</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">ReflectionFunctionAbstract::\_\_clone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">ReflectionFunctionAbstract::getClosureScopeClass</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">object</span>
<span
class="methodname">ReflectionFunctionAbstract::getClosureThis</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">ReflectionFunctionAbstract::getDocComment</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionFunctionAbstract::getEndLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionExtension</span> <span
class="methodname">ReflectionFunctionAbstract::getExtension</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">ReflectionFunctionAbstract::getExtensionName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionFunctionAbstract::getFileName</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionFunctionAbstract::getName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">ReflectionFunctionAbstract::getNamespaceName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionFunctionAbstract::getNumberOfParameters</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionFunctionAbstract::getNumberOfRequiredParameters</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span
class="methodname">ReflectionFunctionAbstract::getParameters</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionType</span> <span
class="methodname">ReflectionFunctionAbstract::getReturnType</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionFunctionAbstract::getShortName</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionFunctionAbstract::getStartLine</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span
class="methodname">ReflectionFunctionAbstract::getStaticVariables</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">ReflectionFunctionAbstract::hasReturnType</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::inNamespace</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isClosure</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isDeprecated</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isGenerator</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isInternal</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">ReflectionFunctionAbstract::isUserDefined</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isVariadic</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">ReflectionFunctionAbstract::returnsReference</span> (
<span class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">ReflectionFunctionAbstract::\_\_toString</span> (
<span class="methodparam">void</span> )

}

属性
----

`name`  
函数的名称。只读，并在尝试赋值的时候会抛出 <span
class="classname">ReflectionException</span>。

预定义常量
----------

ReflectionFunction 修饰符
-------------------------

**`ReflectionFunction::IS_DEPRECATED`**  
指示了不建议使用的函数。

ReflectionFunction::\_\_construct
=================================

Constructs a ReflectionFunction object

### 说明

<span class="modifier">public</span> <span
class="methodname">ReflectionFunction::\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$name`</span> )

Constructs a <span class="classname">ReflectionFunction</span> object.

### 参数

`name`  
The name of the function to reflect or a
<a href="/functions/anonymous.html" class="link">closure</a>.

### 返回值

没有返回值。

### 错误／异常

A <span class="classname">ReflectionException</span> if the `name`
parameter does not contain a valid function.

### 范例

**示例 \#1 <span
class="methodname">ReflectionFunction::\_\_construct</span> example**

``` php
<?php
/**
 * A simple counter
 *
 * @return    int
 */
function counter1()
{
    static $c = 0;
    return ++$c;
}

/**
 * Another simple counter
 *
 * @return    int
 */
$counter2 = function()
{
    static $d = 0;
    return ++$d;

};

function dumpReflectionFunction($func)
{
    // Print out basic information
    printf(
        "\n\n===> The %s function '%s'\n".
        "     declared in %s\n".
        "     lines %d to %d\n",
        $func->isInternal() ? 'internal' : 'user-defined',
        $func->getName(),
        $func->getFileName(),
        $func->getStartLine(),
        $func->getEndline()
    );

    // Print documentation comment
    printf("---> Documentation:\n %s\n", var_export($func->getDocComment(), 1));

    // Print static variables if existant
    if ($statics = $func->getStaticVariables())
    {
        printf("---> Static variables: %s\n", var_export($statics, 1));
    }
}

// Create an instance of the ReflectionFunction class
dumpReflectionFunction(new ReflectionFunction('counter1'));
dumpReflectionFunction(new ReflectionFunction($counter2));
?>
```

以上例程的输出类似于：

    ===> The user-defined function 'counter1'
         declared in Z:\reflectcounter.php
         lines 7 to 11
    ---> Documentation:
     '/**
     * A simple counter
     *
     * @return    int
     */'
    ---> Static variables: array (
      'c' => 0,
    )


    ===> The user-defined function '{closure}'
         declared in Z:\reflectcounter.php
         lines 18 to 23
    ---> Documentation:
     '/**
     * Another simple counter
     *
     * @return    int
     */'
    ---> Static variables: array (
      'd' => 0,
    )

### 参见

-   <span class="methodname">ReflectionMethod::\_\_construct</span>
-   <a href="/language/oop5/decon.html#language.oop5.decon.constructor" class="link">Constructors</a>

ReflectionFunction::export
==========================

Exports function

**Warning**

本函数已自 PHP 7.4.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">ReflectionFunction::export</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$return`</span> \] )

Exports a Reflected function.

### 参数

`name`  
导出的反射。

`return`  
设为 **`TRUE`** 时返回导出结果，设为 **`FALSE`**（默认值）则忽略返回。

### 返回值

如果参数 `return` 设为 **`TRUE`**，导出结果将作为 <span
class="type">string</span> 返回，否则返回 **`NULL`**。

### 参见

-   <span class="methodname">ReflectionFunction::invoke</span>
-   <span class="methodname">ReflectionFunction::\_\_toString</span>

ReflectionFunction::getClosure
==============================

Returns a dynamically created closure for the function

### 说明

<span class="modifier">public</span> <span class="type">Closure</span>
<span class="methodname">ReflectionFunction::getClosure</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns <span class="classname">Closure</span>. Returns **`NULL`** in
case of an error.

ReflectionFunction::invoke
==========================

Invokes function

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ReflectionFunction::invoke</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...`</span> \] )

Invokes a reflected function.

### 参数

`...`  
The passed in argument list. It accepts a variable number of arguments
which are passed to the function much like <span
class="function">call\_user\_func</span> is.

### 返回值

Returns the result of the invoked function call.

### 范例

**示例 \#1 <span class="methodname">ReflectionFunction::invoke</span>
example**

``` php
<?php
function title($title, $name)
{
    return sprintf("%s. %s\r\n", $title, $name);
}

$function = new ReflectionFunction('title');

echo $function->invoke('Dr', 'Phil');
?>
```

以上例程会输出：

    Dr. Phil

### 注释

> **Note**:
>
> 如果函数有参数需为引用，那么它们必须以引用方式传入。

### 参见

-   <span class="methodname">ReflectionFunction::export</span>
-   <a href="/language/oop5/magic.html#object.invoke" class="link">__invoke()</a>
-   <span class="function">call\_user\_func</span>

ReflectionFunction::invokeArgs
==============================

Invokes function args

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ReflectionFunction::invokeArgs</span> ( <span
class="methodparam"><span class="type">array</span> `$args`</span> )

Invokes the function and pass its arguments as array.

### 参数

`args`  
The passed arguments to the function as an array, much like <span
class="function">call\_user\_func\_array</span> works.

### 返回值

Returns the result of the invoked function

### 范例

**示例 \#1 <span
class="methodname">ReflectionFunction::invokeArgs</span> example**

``` php
<?php
function title($title, $name)
{
    return sprintf("%s. %s\r\n", $title, $name);
}

$function = new ReflectionFunction('title');

echo $function->invokeArgs(array('Dr', 'Phil'));
?>
```

以上例程会输出：

    Dr. Phil

**示例 \#2 <span
class="methodname">ReflectionFunction::invokeArgs</span> with references
example**

``` php
<?php
function get_false_conditions(array $conditions, array &$false_conditions)
{
    foreach ($conditions as $condition) {
        if (!$condition) {
            $false_conditions[] = $condition;
        }
    }
}

$function_ref     = new ReflectionFunction('get_false_conditions');

$conditions       = array(true, false, -1, 0, 1);
$false_conditions = array();

$function_ref->invokeArgs(array($conditions, &$false_conditions));

var_dump($false_conditions);
?>
```

以上例程会输出：

    array(2) {
      [0]=>
      bool(false)
      [1]=>
      int(0)
    }

### 注释

> **Note**:
>
> 如果函数有参数需为引用，那么它们必须以引用方式传入。

### 参见

-   <span class="methodname">ReflectionFunction::invoke</span>
-   <span
    class="methodname">ReflectionFunctionAbstract::getNumberOfParameters</span>
-   <a href="/language/oop5/magic.html#object.invoke" class="link">__invoke()</a>
-   <span class="function">call\_user\_func\_array</span>

ReflectionFunction::isDisabled
==============================

Checks if function is disabled

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunction::isDisabled</span> ( <span
class="methodparam">void</span> )

Checks if the function is disabled, via the
<a href="/ini/core.html#ini.disable-functions" class="link">disable_functions</a>
directive.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if it's disable, otherwise **`FALSE`**

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::isUserDefined</span>
-   <a href="/ini/core.html#ini.disable-functions" class="link">disable_functions directive</a>

ReflectionFunction::\_\_toString
================================

To string

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionFunction::\_\_toString</span> ( <span
class="methodparam">void</span> )

To string.

### 参数

此函数没有参数。

### 返回值

Returns <span class="methodname">ReflectionFunction::export</span>-like
output for the function.

### 范例

**示例 \#1 <span
class="methodname">ReflectionFunction::\_\_toString</span> example**

``` php
<?php
function title($title, $name)
{
    return sprintf("%s. %s\r\n", $title, $name);
}

echo new ReflectionFunction('title');
?>
```

以上例程的输出类似于：

    Function [ <user> function title ] {
      @@ Command line code 1 - 1

      - Parameters [2] {
        Parameter #0 [ <required> $title ]
        Parameter #1 [ <required> $name ]
      }
    }

### 参见

-   <span class="methodname">ReflectionFunction::export</span>
-   <span class="methodname">ReflectionClass::clone</span>
-   <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>

简介
----

<span class="classname">ReflectionFunction</span>
的父类，详情请阅读它的描述。

类摘要
------

**ReflectionFunctionAbstract**

<span class="ooclass"> class **ReflectionFunctionAbstract** </span>
<span class="oointerface">implements <span
class="interfacename">Reflector</span> </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$name` ;

/\* 方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">\_\_clone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">getClosureScopeClass</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">getClosureThis</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getDocComment</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getEndLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionExtension</span> <span
class="methodname">getExtension</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getExtensionName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getFileName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getNamespaceName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getNumberOfParameters</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getNumberOfRequiredParameters</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getParameters</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionType</span> <span
class="methodname">getReturnType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getShortName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getStartLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getStaticVariables</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasReturnType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">inNamespace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isClosure</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isDeprecated</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isGenerator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isInternal</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isUserDefined</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isVariadic</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">returnsReference</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

属性
----

`name`  
函数的名称。只读，尝试赋值的时候将会抛出 <span
class="classname">ReflectionException</span>。

ReflectionFunctionAbstract::\_\_clone
=====================================

复制函数

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">ReflectionFunctionAbstract::\_\_clone</span> ( <span
class="methodparam">void</span> )

复制函数

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

### 参见

-   <a href="/language/oop5/cloning.html" class="link">Object cloning</a>

ReflectionFunctionAbstract::getClosureScopeClass
================================================

Returns the scope associated to the closure

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">ReflectionFunctionAbstract::getClosureScopeClass</span>
( <span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns the class on success or **`NULL`** on failure.

ReflectionFunctionAbstract::getClosureThis
==========================================

返回本身的匿名函数

### 说明

<span class="modifier">public</span> <span class="type">object</span>
<span
class="methodname">ReflectionFunctionAbstract::getClosureThis</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

返回 `$this` 指向，产生错误返回 **`NULL`**

ReflectionFunctionAbstract::getDocComment
=========================================

获取注释内容

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">ReflectionFunctionAbstract::getDocComment</span> (
<span class="methodparam">void</span> )

获取函数的注释文本

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

如果存在注释文本返回其内容，否则返回 **`FALSE`**

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getStartLine</span>

ReflectionFunctionAbstract::getEndLine
======================================

获取结束行号

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionFunctionAbstract::getEndLine</span> ( <span
class="methodparam">void</span> )

获取结束行号

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

获取用户定义函数的结束行号，如果未知返回 **`FALSE`**

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getStartLine</span>

ReflectionFunctionAbstract::getExtension
========================================

获取扩展信息

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionExtension</span> <span
class="methodname">ReflectionFunctionAbstract::getExtension</span> (
<span class="methodparam">void</span> )

获取函数的扩展信息

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

返回 <span class="classname">ReflectionExtension</span>
对象，包含扩展信息

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getExtensionName</span>

ReflectionFunctionAbstract::getExtensionName
============================================

获取扩展名称

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">ReflectionFunctionAbstract::getExtensionName</span> (
<span class="methodparam">void</span> )

获取扩展名称

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

返回扩展名称

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getExtension</span>

ReflectionFunctionAbstract::getFileName
=======================================

获取文件名称

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionFunctionAbstract::getFileName</span>
( <span class="methodparam">void</span> )

获取函数定义的文件名称

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The file name.

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getNamespaceName</span>

ReflectionFunctionAbstract::getName
===================================

获取函数名称

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionFunctionAbstract::getName</span> (
<span class="methodparam">void</span> )

获取函数名称

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

返回函数名称

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getExtensionName</span>
-   <span
    class="methodname">ReflectionFunctionAbstract::isUserDefined</span>

ReflectionFunctionAbstract::getNamespaceName
============================================

获取命名空间

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">ReflectionFunctionAbstract::getNamespaceName</span> (
<span class="methodparam">void</span> )

获取类定义所属的命名空间

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

返回命名空间

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getFileName</span>
-   <a href="/language/namespaces.html" class="link">namespaces</a>

ReflectionFunctionAbstract::getNumberOfParameters
=================================================

获取参数数目

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionFunctionAbstract::getNumberOfParameters</span>
( <span class="methodparam">void</span> )

获取函数定义的参数数目，包括可选参数

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

参数的个数

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getNumberOfRequiredParameters</span>
-   <span class="function">func\_num\_args</span>

ReflectionFunctionAbstract::getNumberOfRequiredParameters
=========================================================

获取必须输入参数个数

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionFunctionAbstract::getNumberOfRequiredParameters</span>
( <span class="methodparam">void</span> )

获取函数定义中，必须输入的参数个数

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

必须输入的参数个数

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getNumberOfParameters</span>

ReflectionFunctionAbstract::getParameters
=========================================

获取参数

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span
class="methodname">ReflectionFunctionAbstract::getParameters</span> (
<span class="methodparam">void</span> )

通过 <span class="type">ReflectionParameter</span> 数组返回参数列表

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

一组 <span class="classname">ReflectionParameter</span> 对象表示每一参数

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getNumberOfParameters</span>
-   <span class="function">func\_get\_args</span>

ReflectionFunctionAbstract::getReturnType
=========================================

Gets the specified return type of a function

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionType</span> <span
class="methodname">ReflectionFunctionAbstract::getReturnType</span> (
<span class="methodparam">void</span> )

Gets the specified return type of a reflected function.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="classname">ReflectionType</span> object if a
return type is specified, **`NULL`** otherwise.

### 范例

**示例 \#1 <span
class="methodname">ReflectionFunctionAbstract::getReturnType</span>
example**

``` php
<?php

function to_int($param) : int {
    return (int) $param;
}

$reflection1 = new ReflectionFunction('to_int');
echo $reflection1->getReturnType();
```

以上例程会输出：

    int

**示例 \#2 Usage on built-in functions**

``` php
<?php

$reflection2 = new ReflectionFunction('array_merge');

var_dump($reflection2->getReturnType());
```

以上例程会输出：

    null

This is because many internal functions do not have types specified for
their parameters or return values. It is therefore best to avoid using
this method on built-in functions.

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::hasReturnType</span>
-   <span class="methodname">ReflectionType::\_\_toString</span>

ReflectionFunctionAbstract::getShortName
========================================

获取函数短名称

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionFunctionAbstract::getShortName</span>
( <span class="methodparam">void</span> )

获取函数的段名称 (没有命名空间定义)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

函数短名称

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getNamespaceName</span>
-   <a href="/language/namespaces.html" class="link">namespaces</a>

ReflectionFunctionAbstract::getStartLine
========================================

获取开始行号

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionFunctionAbstract::getStartLine</span> (
<span class="methodparam">void</span> )

获取函数定义的开始行号

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

开始行号

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getEndLine</span>

ReflectionFunctionAbstract::getStaticVariables
==============================================

获取静态变量

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span
class="methodname">ReflectionFunctionAbstract::getStaticVariables</span>
( <span class="methodparam">void</span> )

获取静态变量

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

返回一个静态变量的 <span class="type">array</span>

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getParameters</span>

ReflectionFunctionAbstract::hasReturnType
=========================================

Checks if the function has a specified return type

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">ReflectionFunctionAbstract::hasReturnType</span> (
<span class="methodparam">void</span> )

Checks whether the reflected function has a return type specified.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the function is a specified return type, otherwise
**`FALSE`**.

### 范例

**示例 \#1 <span
class="methodname">ReflectionFunctionAbstract::hasReturnType</span>
example**

``` php
<?php

function to_int($param) : int {
    return (int) $param;
}

$reflection1 = new ReflectionFunction('to_int');
var_dump($reflection1->hasReturnType());
```

以上例程会输出：

    bool(true)

**示例 \#2 Usage on built-in functions**

``` php
<?php

$reflection2 = new ReflectionFunction('array_merge');

var_dump($reflection2->hasReturnType());
```

以上例程会输出：

    bool(false)

This is because many internal functions do not have types specified for
their parameters or return values. It is therefore best to avoid using
this method on built-in functions.

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getReturnType</span>

ReflectionFunctionAbstract::inNamespace
=======================================

检查是否处于命名空间

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::inNamespace</span>
( <span class="methodparam">void</span> )

检查函数是否在命名空间内定义

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

在命名空间内返回 **`TRUE`**，否则返回 **`FALSE`**

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getNamespaceName</span>
-   <a href="/language/namespaces.html" class="link">namespaces</a>

ReflectionFunctionAbstract::isClosure
=====================================

检查是否是匿名函数

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isClosure</span> (
<span class="methodparam">void</span> )

检查是否是匿名函数

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

匿名函数返回 **`TRUE`**，否则返回 **`FALSE`**

### 参见

-   <span class="methodname">ReflectionFunctionAbstract::</span>

ReflectionFunctionAbstract::isDeprecated
========================================

检查是否已经弃用

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isDeprecated</span>
( <span class="methodparam">void</span> )

检查函数是否已经被弃用

### 参数

此函数没有参数。

### 返回值

弃用返回 **`TRUE`**，否则返回 **`FALSE`**

### 范例

**示例 \#1 <span
class="methodname">ReflectionFunctionAbstract::isDeprecated</span>
example**

``` php
<?php
$rf = new ReflectionFunction('ereg');
var_dump($rf->isDeprecated());
?>
```

以上例程会输出：

    bool(true)

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getDocComment</span>

ReflectionFunctionAbstract::isGenerator
=======================================

判断函数是否是一个生成器函数

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isGenerator</span>
( <span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

生成器函数返回 **`TRUE`**，否则返回 **`FALSE`** on failure.

ReflectionFunctionAbstract::isInternal
======================================

判断函数是否是内置函数

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isInternal</span> (
<span class="methodparam">void</span> )

判断函数是否是内置函数，与用户自定义函数相反

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

内置函数返回 **`TRUE`**，否则返回 **`FALSE`**

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::isUserDefined</span>

ReflectionFunctionAbstract::isUserDefined
=========================================

检查是否是用户定义

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">ReflectionFunctionAbstract::isUserDefined</span> (
<span class="methodparam">void</span> )

检查函数是否是用户自定义，也就是说不是 PHP 自己内置函数

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

用户自定义函数返回 **`TRUE`**，否则返回 **`FALSE`**

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::isInternal</span>

ReflectionFunctionAbstract::isVariadic
======================================

Checks if the function is variadic

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isVariadic</span> (
<span class="methodparam">void</span> )

Checks if the function is
<a href="/functions/arguments.html#functions.variable-arg-list.new" class="link">variadic</a>.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the function is variadic, otherwise **`FALSE`**.

ReflectionFunctionAbstract::returnsReference
============================================

检查是否返回参考信息

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">ReflectionFunctionAbstract::returnsReference</span> (
<span class="methodparam">void</span> )

检查是否返回参考信息

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

返回参考信息返回 **`TRUE`**，否则返回 **`FALSE`**

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::isClosure</span>

ReflectionFunctionAbstract::\_\_toString
========================================

字符串化

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">ReflectionFunctionAbstract::\_\_toString</span> (
<span class="methodparam">void</span> )

To string.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The string.

### 参见

-   <span class="methodname">ReflectionClass::clone</span>
-   <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>

简介
----

<span class="classname">ReflectionMethod</span>
类报告了一个方法的有关信息。

类摘要
------

**ReflectionMethod**

<span class="ooclass"> class **ReflectionMethod** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**ReflectionFunctionAbstract** </span> <span
class="oointerface">implements <span
class="interfacename">Reflector</span> </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionMethod::IS_STATIC` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionMethod::IS_PUBLIC` <span class="initializer"> = 256</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionMethod::IS_PROTECTED` <span class="initializer"> = 512</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionMethod::IS_PRIVATE` <span class="initializer"> = 1024</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionMethod::IS_ABSTRACT` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionMethod::IS_FINAL` <span class="initializer"> = 4</span> ;

/\* 属性 \*/

<span class="modifier">public</span> `$name` ;

<span class="modifier">public</span> `$class` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$class`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">export</span> ( <span class="methodparam"><span
class="type">string</span> `$class`</span> , <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$return`<span
class="initializer"> = false</span></span> \] )

<span class="modifier">public</span> <span class="type">Closure</span>
<span class="methodname">getClosure</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">getDeclaringClass</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getModifiers</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionMethod</span> <span
class="methodname">getPrototype</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">invoke</span> ( <span class="methodparam"><span
class="type">object</span> `$object`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$parameter`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...`</span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">invokeArgs</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> ,
<span class="methodparam"><span class="type">array</span> `$args`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isAbstract</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isConstructor</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isDestructor</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isFinal</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isPrivate</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isProtected</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isPublic</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isStatic</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setAccessible</span> ( <span
class="methodparam"><span class="type">bool</span> `$accessible`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">ReflectionFunctionAbstract::\_\_clone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">ReflectionFunctionAbstract::getClosureScopeClass</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">object</span>
<span
class="methodname">ReflectionFunctionAbstract::getClosureThis</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">ReflectionFunctionAbstract::getDocComment</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionFunctionAbstract::getEndLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionExtension</span> <span
class="methodname">ReflectionFunctionAbstract::getExtension</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">ReflectionFunctionAbstract::getExtensionName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionFunctionAbstract::getFileName</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionFunctionAbstract::getName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">ReflectionFunctionAbstract::getNamespaceName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionFunctionAbstract::getNumberOfParameters</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionFunctionAbstract::getNumberOfRequiredParameters</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span
class="methodname">ReflectionFunctionAbstract::getParameters</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionType</span> <span
class="methodname">ReflectionFunctionAbstract::getReturnType</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionFunctionAbstract::getShortName</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionFunctionAbstract::getStartLine</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span
class="methodname">ReflectionFunctionAbstract::getStaticVariables</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">ReflectionFunctionAbstract::hasReturnType</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::inNamespace</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isClosure</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isDeprecated</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isGenerator</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isInternal</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">ReflectionFunctionAbstract::isUserDefined</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionFunctionAbstract::isVariadic</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">ReflectionFunctionAbstract::returnsReference</span> (
<span class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">ReflectionFunctionAbstract::\_\_toString</span> (
<span class="methodparam">void</span> )

}

属性
----

`name`  
Method name

`class`  
Class name

预定义常量
----------

ReflectionMethod 修饰符
-----------------------

**`ReflectionMethod::IS_STATIC`**  
指示一个方法是静态（static）的。

**`ReflectionMethod::IS_PUBLIC`**  
指示一个方法是 public 的。

**`ReflectionMethod::IS_PROTECTED`**  
指示一个方法是 protected 的。

**`ReflectionMethod::IS_PRIVATE`**  
指示一个方法是 private 的。

**`ReflectionMethod::IS_ABSTRACT`**  
指示一个方法是 abstract 的。

**`ReflectionMethod::IS_FINAL`**  
指示一个方法是 final 的。

ReflectionMethod::\_\_construct
===============================

ReflectionMethod 的构造函数

### 说明

<span class="modifier">public</span> <span
class="methodname">ReflectionMethod::\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$class`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

<span class="modifier">public</span> <span
class="methodname">ReflectionMethod::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$class_method`</span> )

构造一个新的 <span class="classname">ReflectionMethod</span>

### 参数

`class`  
包含方法的类名称或者这个类的一个实例

`name`  
方法的名称

`class_method`  
类名称和方法名称，之间使用 *::* 分隔

### 返回值

没有返回值。

### 错误／异常

如果指定的方法不存在，那么抛出一个 <span
class="classname">ReflectionException</span>

### 范例

**示例 \#1 <span
class="methodname">ReflectionMethod::\_\_construct</span> example**

``` php
<?php
class Counter
{
    private static $c = 0;

    /**
     * Increment counter
     *
     * @final
     * @static
     * @access  public
     * @return  int
     */
    final public static function increment()
    {
        return ++self::$c;
    }
}

// Create an instance of the ReflectionMethod class
$method = new ReflectionMethod('Counter', 'increment');

// Print out basic information
printf(
    "===> The %s%s%s%s%s%s%s method '%s' (which is %s)\n" .
    "     declared in %s\n" .
    "     lines %d to %d\n" .
    "     having the modifiers %d[%s]\n",
        $method->isInternal() ? 'internal' : 'user-defined',
        $method->isAbstract() ? ' abstract' : '',
        $method->isFinal() ? ' final' : '',
        $method->isPublic() ? ' public' : '',
        $method->isPrivate() ? ' private' : '',
        $method->isProtected() ? ' protected' : '',
        $method->isStatic() ? ' static' : '',
        $method->getName(),
        $method->isConstructor() ? 'the constructor' : 'a regular method',
        $method->getFileName(),
        $method->getStartLine(),
        $method->getEndline(),
        $method->getModifiers(),
        implode(' ', Reflection::getModifierNames($method->getModifiers()))
);

// 打印注释文档
printf("---> Documentation:\n %s\n", var_export($method->getDocComment(), 1));

// 打印存在的静态变量
if ($statics= $method->getStaticVariables()) {
    printf("---> Static variables: %s\n", var_export($statics, 1));
}

// 执行方法
printf("---> Invocation results in: ");
var_dump($method->invoke(NULL));
?>
```

以上例程的输出类似于：

    ===> The user-defined final public static method 'increment' (which is a regular method)
         declared in /Users/philip/cvs/phpdoc/test.php
         lines 14 to 17
         having the modifiers 261[final public static]
    ---> Documentation:
     '/**
         * Increment counter
         *
         * @final
         * @static
         * @access  public
         * @return  int
         */'
    ---> Invocation results in: int(1)

### 参见

-   <span class="methodname">ReflectionMethod::export</span>
-   <a href="/language/oop5/decon.html#language.oop5.decon.constructor" class="link">Constructors</a>

ReflectionMethod::export
========================

输出一个回调方法

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">ReflectionMethod::export</span> ( <span
class="methodparam"><span class="type">string</span> `$class`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$return`<span class="initializer"> =
false</span></span> \] )

Exports a ReflectionMethod.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`class`  
类名称

`name`  
方法名称

`return`  
设为 **`TRUE`** 时返回导出结果，设为 **`FALSE`**（默认值）则忽略返回。

### 返回值

如果参数 `return` 设为 **`TRUE`**，导出结果将作为 <span
class="type">string</span> 返回，否则返回 **`NULL`**。

### 参见

-   <span class="methodname">ReflectionMethod::\_\_construct</span>
-   <span class="methodname">ReflectionMethod::\_\_toString</span>

ReflectionMethod::getClosure
============================

返回一个动态建立的方法调用接口，译者注：可以使用这个返回值直接调用非公开方法。

### 说明

<span class="modifier">public</span> <span class="type">Closure</span>
<span class="methodname">ReflectionMethod::getClosure</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`object`  
不可以使用静态方法，需要其他类型的方法

### 返回值

返回 <span class="classname">Closure</span> 如果产生任何错误返回
**`NULL`**

ReflectionMethod::getDeclaringClass
===================================

获取反射函数调用参数的类表达

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">ReflectionMethod::getDeclaringClass</span> ( <span
class="methodparam">void</span> )

获取反射函数参数的一个表达类。
译者注：应该是将这个方法作为一个类返回，他的参数将成为类属性，
执行内容变成什么不知道，下面的范例能够说明一些问题

### 参数

此函数没有参数。

### 返回值

返回 <span class="classname">ReflectionClass</span>
对象，其中包含这个方法。

### 范例

**示例 \#1 <span
class="methodname">ReflectionMethod::getDeclaringClass</span> example**

``` php
<?php
class HelloWorld {

    protected function sayHelloTo($name) {
        return 'Hello ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod(new HelloWorld(), 'sayHelloTo');
var_dump($reflectionMethod->getDeclaringClass());
?>
```

以上例程会输出：

    object(ReflectionClass)#2 (1) {
      ["name"]=>
      string(10) "HelloWorld"
    }

### 参见

-   <span class="methodname">ReflectionMethod::isAbstract</span>

ReflectionMethod::getModifiers
==============================

获取方法的修饰符

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionMethod::getModifiers</span> ( <span
class="methodparam">void</span> )

返回一个方法的修饰符，返回值是一个位标

### 参数

此函数没有参数。

### 返回值

使用一个数字表示方法修饰符，具体数字的含义可以参考
<a href="/class/reflectionmethod.html#ReflectionMethod%20修饰符" class="link">predefined constants</a>
中的说明。

### 范例

**示例 \#1 <span
class="methodname">ReflectionMethod::getModifiers</span> example**

``` php
<?php
class Testing
{
    final public static function foo()
    {
        return;
    }
    public function bar()
    {
        return;
    }
}

$foo = new ReflectionMethod('Testing', 'foo');

echo "Modifiers for method foo():\n";
echo $foo->getModifiers() . "\n";
echo implode(' ', Reflection::getModifierNames($foo->getModifiers())) . "\n";

$bar = new ReflectionMethod('Testing', 'bar');

echo "Modifiers for method bar():\n";
echo $bar->getModifiers() . "\n";
echo implode(' ', Reflection::getModifierNames($bar->getModifiers()));
?>
```

以上例程的输出类似于：

    Modifiers for method foo():
    261
    final public static
    Modifiers for method bar():
    65792
    public

### 参见

-   <span class="methodname">Reflection::getModifierNames</span>

ReflectionMethod::getPrototype
==============================

返回方法原型 (如果存在)

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionMethod</span> <span
class="methodname">ReflectionMethod::getPrototype</span> ( <span
class="methodparam">void</span> )

返回方法原型

### 参数

此函数没有参数。

### 返回值

方法原型的一个 <span class="classname">ReflectionMethod</span> 实例

### 错误／异常

如果方法没有原型，产生一个 <span
class="classname">ReflectionException</span>

### 范例

**示例 \#1 <span
class="methodname">ReflectionMethod::getPrototype</span> example**

``` php
<?php
class Hello {

    public function sayHelloTo($name) {
        return 'Hello ' . $name;
    }

}
class HelloWorld extends Hello {

    public function sayHelloTo($name) {
        return 'Hello world: ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod('HelloWorld', 'sayHelloTo');
var_dump($reflectionMethod->getPrototype());
?>
```

以上例程会输出：

    object(ReflectionMethod)#2 (2) {
      ["name"]=>
      string(10) "sayHelloTo"
      ["class"]=>
      string(5) "Hello"
    }

### 参见

-   <span class="methodname">ReflectionMethod::getModifiers</span>

ReflectionMethod::invoke
========================

Invoke

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ReflectionMethod::invoke</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$parameter`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$...`</span> \]\] )

执行一个反射的方法。

### 参数

`object`  
如果执行的方法是静态类，那么这个参数传送 <span
class="type">null</span>。

`parameter`  
0，或者传送给方法的参数列表。可以通过这个参数，给方法传送大量的参数。

### 返回值

返回方法的返回值

### 错误／异常

如果 `object` 并没有包含一个可以使用的类实例，那么将产生 一个 <span
class="classname">ReflectionException</span>。

如果方法调用失败，也会产生一个 <span
class="classname">ReflectionException</span>。

### 范例

**示例 \#1 <span class="methodname">ReflectionMethod::invoke</span>
example**

``` php
<?php
class HelloWorld {

    public function sayHelloTo($name) {
        return 'Hello ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod('HelloWorld', 'sayHelloTo');
echo $reflectionMethod->invoke(new HelloWorld(), 'Mike');
?>
```

以上例程会输出：

    Hello Mike

### 注释

> **Note**:
>
> 如果函数有参数需为引用，那么它们必须以引用方式传入。

### 参见

-   <span class="methodname">ReflectionMethod::invokeArgs</span>
-   <a href="/language/oop5/magic.html#object.invoke" class="link">__invoke()</a>
-   <span class="function">call\_user\_func</span>

ReflectionMethod::invokeArgs
============================

带参数执行

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ReflectionMethod::invokeArgs</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> ,
<span class="methodparam"><span class="type">array</span> `$args`</span>
)

使用数组给方法传送参数，并执行他。

### 参数

`object`  
调用方法的对象，如果是静态对象，设置为 <span class="type">null</span>

`args`  
使用 <span class="type">array</span> 传送的方法参数。

### 返回值

返回方法返回值

### 错误／异常

如果 `object` 指定的实例无法执行方法，那么产生 <span
class="classname">ReflectionException</span> 异常。

如果方法调用失败，产生 <span
class="classname">ReflectionException</span>

### 范例

**示例 \#1 <span class="methodname">ReflectionMethod::invokeArgs</span>
example**

``` php
<?php
class HelloWorld {

    public function sayHelloTo($name) {
        return 'Hello ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod('HelloWorld', 'sayHelloTo');
echo $reflectionMethod->invokeArgs(new HelloWorld(), array('Mike'));
?>
```

以上例程会输出：

    Hello Mike

### 注释

> **Note**:
>
> 如果函数有参数需为引用，那么它们必须以引用方式传入。

### 参见

-   <span class="methodname">ReflectionMethod::invoke</span>
-   <a href="/language/oop5/magic.html#object.invoke" class="link">__invoke()</a>
-   <span class="function">call\_user\_func\_array</span>

ReflectionMethod::isAbstract
============================

判断方法是否是抽象方法

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionMethod::isAbstract</span> ( <span
class="methodparam">void</span> )

判断方法是否是抽象方法

### 参数

此函数没有参数。

### 返回值

如果是抽象方法返回 **`TRUE`**，否则返回 **`FALSE`**

### 参见

-   <span class="methodname">ReflectionMethod::getDeclaringClass</span>

ReflectionMethod::isConstructor
===============================

判断方法是否是构造方法

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionMethod::isConstructor</span> ( <span
class="methodparam">void</span> )

判断方法是否是构造方法

### 参数

此函数没有参数。

### 返回值

如果是构造方法返回 **`TRUE`**，否则返回 **`FALSE`**

### 参见

-   <span class="methodname">ReflectionMethod::\_\_construct</span>
-   <span class="methodname">ReflectionMethod::isAbstract</span>
-   <span class="methodname">ReflectionMethod::isDestructor</span>

ReflectionMethod::isDestructor
==============================

判断方法是否是析构方法

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionMethod::isDestructor</span> ( <span
class="methodparam">void</span> )

判断方法是否是析构方法

### 参数

此函数没有参数。

### 返回值

如果是析构方法返回 **`TRUE`**，否则返回 **`FALSE`**

### 参见

-   <span class="methodname">ReflectionMethod::isConstructor</span>

ReflectionMethod::isFinal
=========================

判断方法是否定义 final

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionMethod::isFinal</span> ( <span
class="methodparam">void</span> )

判断方法是否定义 final

### 参数

此函数没有参数。

### 返回值

如果是 final 返回 **`TRUE`**，否则返回 **`FALSE`**

### 参见

-   <span class="methodname">ReflectionMethod::isStatic</span>

ReflectionMethod::isPrivate
===========================

判断方法是否是私有方法

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionMethod::isPrivate</span> ( <span
class="methodparam">void</span> )

判断方法是否是私有方法

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

私有方法返回 **`TRUE`**，否则返回 **`FALSE`**

### 参见

-   <span class="methodname">ReflectionMethod::isPublic</span>

ReflectionMethod::isProtected
=============================

判断方法是否是保护方法 (protected)

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionMethod::isProtected</span> ( <span
class="methodparam">void</span> )

判断方法是否是保护方法

### 参数

此函数没有参数。

### 返回值

保护方法返回 **`TRUE`**，否则返回 **`FALSE`**

### 参见

-   <span class="methodname">ReflectionMethod::isPrivate</span>

ReflectionMethod::isPublic
==========================

判断方法是否是公开方法

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionMethod::isPublic</span> ( <span
class="methodparam">void</span> )

判断方法是否是公开方法

### 参数

此函数没有参数。

### 返回值

公开方法返回 **`TRUE`**，否则返回 **`FALSE`**

### 参见

-   <span class="methodname">ReflectionMethod::isPrivate</span>

ReflectionMethod::isStatic
==========================

判断方法是否是静态方法

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionMethod::isStatic</span> ( <span
class="methodparam">void</span> )

判断方法是否是静态方法

### 参数

此函数没有参数。

### 返回值

静态方法返回 **`TRUE`**，否则返回 **`FALSE`**

### 参见

-   <span class="methodname">ReflectionMethod::isFinal</span>

ReflectionMethod::setAccessible
===============================

设置方法是否访问

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ReflectionMethod::setAccessible</span> ( <span
class="methodparam"><span class="type">bool</span> `$accessible`</span>
)

设置方法是否可以访问，例如通过设置可以访问能够执行私有方法和保护方法

### 参数

`accessible`  
可以访问设置 **`TRUE`**，否则设置 **`FALSE`**

### 返回值

没有返回值。

### 参见

-   <span class="methodname">ReflectionMethod::isPrivate</span>
-   <span class="methodname">ReflectionMethod::isProtected</span>

ReflectionMethod::\_\_toString
==============================

返回反射方法对象的字符串表达

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionMethod::\_\_toString</span> ( <span
class="methodparam">void</span> )

返回反射方法对象的字符串表达

### 参数

此函数没有参数。

### 返回值

<span class="classname">ReflectionMethod</span>
实例的字符串表达，也就是字符串

### 范例

**示例 \#1 <span
class="methodname">ReflectionMethod::\_\_toString</span> example**

``` php
<?php
class HelloWorld {

    public function sayHelloTo($name) {
        return 'Hello ' . $name;
    }

}

$reflectionMethod = new ReflectionMethod(new HelloWorld(), 'sayHelloTo');
echo $reflectionMethod;
?>
```

以上例程会输出：

    Method [ <user> public method sayHelloTo ] {
      @@ /var/www/examples/reflection.php 16 - 18

      - Parameters [1] {
        Parameter #0 [ <required> $name ]
      }
    }

### 参见

-   <span class="methodname">ReflectionMethod::export</span>
-   <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>

简介
----

<span class="classname">ReflectionObject</span> 类报告了一个对象（<span
class="type">object</span>）的相关信息。

类摘要
------

**ReflectionObject**

<span class="ooclass"> class **ReflectionObject** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**ReflectionClass** </span> <span class="oointerface">implements <span
class="interfacename">Reflector</span> </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionObject::IS_IMPLICIT_ABSTRACT` <span class="initializer"> =
16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionObject::IS_EXPLICIT_ABSTRACT` <span class="initializer"> =
32</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionObject::IS_FINAL` <span class="initializer"> = 64</span> ;

/\* 属性 \*/

<span class="modifier">public</span> `$name` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">object</span> `$argument`</span>
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">export</span> ( <span class="methodparam"><span
class="type">string</span> `$argument`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$return`</span> \] )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">ReflectionClass::\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$argument`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">ReflectionClass::export</span> ( <span
class="methodparam"><span class="type">mixed</span> `$argument`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$return`<span class="initializer"> = false</span></span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ReflectionClass::getConstant</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getConstants</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionMethod</span> <span
class="methodname">ReflectionClass::getConstructor</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getDefaultProperties</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::getDocComment</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionClass::getEndLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionExtension</span> <span
class="methodname">ReflectionClass::getExtension</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::getExtensionName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::getFileName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getInterfaceNames</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getInterfaces</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionMethod</span> <span
class="methodname">ReflectionClass::getMethod</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getMethods</span> (\[ <span
class="methodparam"><span class="type">int</span> `$filter`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionClass::getModifiers</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::getNamespaceName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">ReflectionClass::getParentClass</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getProperties</span> (\[ <span
class="methodparam"><span class="type">int</span> `$filter`</span> \] )

<span class="modifier">public</span> <span
class="type">ReflectionProperty</span> <span
class="methodname">ReflectionClass::getProperty</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="type">ReflectionClassConstant</span> <span
class="methodname">ReflectionClass::getReflectionConstant</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getReflectionConstants</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::getShortName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionClass::getStartLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getStaticProperties</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ReflectionClass::getStaticPropertyValue</span>
( <span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `&$def_value`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getTraitAliases</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getTraitNames</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionClass::getTraits</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::hasConstant</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::hasMethod</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::hasProperty</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::implementsInterface</span> (
<span class="methodparam"><span class="type">string</span>
`$interface`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::inNamespace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isAbstract</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isAnonymous</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isCloneable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isFinal</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isInstance</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isInstantiable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isInterface</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isInternal</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isIterable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isIterateable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isSubclassOf</span> ( <span
class="methodparam"><span class="type">string</span> `$class`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isTrait</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionClass::isUserDefined</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">ReflectionClass::newInstance</span> ( <span
class="methodparam"><span class="type">mixed</span> `$args`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$...`</span>
\] )

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">ReflectionClass::newInstanceArgs</span> (\[
<span class="methodparam"><span class="type">array</span> `$args`</span>
\] )

<span class="modifier">public</span> <span class="type">object</span>
<span
class="methodname">ReflectionClass::newInstanceWithoutConstructor</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ReflectionClass::setStaticPropertyValue</span>
( <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionClass::\_\_toString</span> ( <span
class="methodparam">void</span> )

}

属性
----

`name`  
对象的类名。只读，在尝试赋值的时候会抛出 <span
class="classname">ReflectionException</span>。

ReflectionObject::\_\_construct
===============================

Constructs a ReflectionObject

### 说明

<span class="modifier">public</span> <span
class="methodname">ReflectionObject::\_\_construct</span> ( <span
class="methodparam"><span class="type">object</span> `$argument`</span>
)

Constructs a <span class="classname">ReflectionObject</span>.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`argument`  
An object instance.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">ReflectionObject::export</span>
-   <a href="/language/oop5/decon.html#language.oop5.decon.constructor" class="link">Constructors</a>

ReflectionObject::export
========================

Export

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">ReflectionObject::export</span> ( <span
class="methodparam"><span class="type">string</span> `$argument`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$return`</span> \] )

Exports a reflection.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`argument`  
导出的反射。

`return`  
设为 **`TRUE`** 时返回导出结果，设为 **`FALSE`**（默认值）则忽略返回。

### 返回值

如果参数 `return` 设为 **`TRUE`**，导出结果将作为 <span
class="type">string</span> 返回，否则返回 **`NULL`**。

### 参见

-   <span class="methodname">ReflectionObject::\_\_construct</span>

简介
----

<span class="classname">ReflectionParameter</span>
取回了函数或方法参数的相关信息。

要自行检查函数的参数，首先创建一个 <span
class="classname">ReflectionFunction</span> 或 <span
class="classname">ReflectionMethod</span> 的实例，然后使用它们的 <span
class="methodname">ReflectionFunctionAbstract::getParameters</span>
方法来获取参数的数组。

类摘要
------

**ReflectionParameter**

<span class="ooclass"> class **ReflectionParameter** </span> <span
class="oointerface">implements <span
class="interfacename">Reflector</span> </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$name` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">allowsNull</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">canBePassedByValue</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">\_\_clone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">callable</span>
`$function`</span> , <span class="methodparam"><span
class="type">mixed</span> `$parameter`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">export</span> ( <span class="methodparam"><span
class="type">string</span> `$function`</span> , <span
class="methodparam"><span class="type">string</span> `$parameter`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$return`</span> \] )

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">getClass</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">getDeclaringClass</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionFunctionAbstract</span> <span
class="methodname">getDeclaringFunction</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getDefaultValue</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getDefaultValueConstantName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getPosition</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionType</span> <span
class="methodname">getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isArray</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isCallable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isDefaultValueAvailable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isDefaultValueConstant</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isOptional</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isPassedByReference</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isVariadic</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

属性
----

`name`  
参数的名称。只读，在尝试赋值的时候会抛出 <span
class="classname">ReflectionException</span>。

ReflectionParameter::allowsNull
===============================

Checks if null is allowed

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionParameter::allowsNull</span> ( <span
class="methodparam">void</span> )

Checks whether the parameter allows **`NULL`**.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if **`NULL`** is allowed, otherwise **`FALSE`**

### 参见

-   <span class="methodname">ReflectionParameter::isOptional</span>

ReflectionParameter::canBePassedByValue
=======================================

Returns whether this parameter can be passed by value

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionParameter::canBePassedByValue</span>
( <span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the parameter can be passed by value, **`FALSE`**
otherwise. Returns **`NULL`** in case of an error.

ReflectionParameter::\_\_clone
==============================

Clone

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">ReflectionParameter::\_\_clone</span> ( <span
class="methodparam">void</span> )

Clones.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

### 参见

-   <span class="methodname">ReflectionParameter::toString</span>
-   <a href="/language/oop5/cloning.html" class="link">Object cloning</a>

ReflectionParameter::\_\_construct
==================================

Construct

### 说明

<span class="modifier">public</span> <span
class="methodname">ReflectionParameter::\_\_construct</span> ( <span
class="methodparam"><span class="type">callable</span>
`$function`</span> , <span class="methodparam"><span
class="type">mixed</span> `$parameter`</span> )

Constructs a <span class="classname">ReflectionParameter</span>
instance.

### 参数

`function`  
The function to reflect parameters from.

`parameter`  
Either an <span class="type">integer</span> specifying the position of
the parameter (starting with zero), or a the parameter name as <span
class="type">string</span>.

### 返回值

没有返回值。

### 范例

**示例 \#1 Using the <span class="classname">ReflectionParameter</span>
class**

``` php
<?php
function foo($a, $b, $c) { }
function bar(Exception $a, &$b, $c) { }
function baz(ReflectionFunction $a, $b = 1, $c = null) { }
function abc() { }

$reflect = new ReflectionFunction('foo');

echo $reflect;

foreach ($reflect->getParameters() as $i => $param) {
    printf(
        "-- Parameter #%d: %s {\n".
        "   Class: %s\n".
        "   Allows NULL: %s\n".
        "   Passed to by reference: %s\n".
        "   Is optional?: %s\n".
        "}\n",
        $i, // $param->getPosition() can be used from PHP 5.2.3
        $param->getName(),
        var_export($param->getClass(), 1),
        var_export($param->allowsNull(), 1),
        var_export($param->isPassedByReference(), 1),
        $param->isOptional() ? 'yes' : 'no'
    );
}
?>
```

以上例程的输出类似于：

    Function [ <user> function foo ] {
      @@ /Users/philip/cvs/phpdoc/a 2 - 2

      - Parameters [3] {
        Parameter #0 [ <required> $a ]
        Parameter #1 [ <required> $b ]
        Parameter #2 [ <required> $c ]
      }
    }
    -- Parameter #0: a {
       Class: NULL
       Allows NULL: true
       Passed to by reference: false
       Is optional?: no
    }
    -- Parameter #1: b {
       Class: NULL
       Allows NULL: true
       Passed to by reference: false
       Is optional?: no
    }
    -- Parameter #2: c {
       Class: NULL
       Allows NULL: true
       Passed to by reference: false
       Is optional?: no
    }

### 参见

-   <span
    class="methodname">ReflectionFunctionAbstract::getParameters</span>
-   <span class="methodname">ReflectionFunction::\_\_construct</span>
-   <span class="methodname">ReflectionMethod::\_\_construct</span>
-   <a href="/language/oop5/decon.html#language.oop5.decon.constructor" class="link">Constructors</a>

ReflectionParameter::export
===========================

Exports

**Warning**

本函数已自 PHP 7.4.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">ReflectionParameter::export</span> ( <span
class="methodparam"><span class="type">string</span> `$function`</span>
, <span class="methodparam"><span class="type">string</span>
`$parameter`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$return`</span> \] )

Exports.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`function`  
The function name.

`parameter`  
The parameter name.

`return`  
设为 **`TRUE`** 时返回导出结果，设为 **`FALSE`**（默认值）则忽略返回。

### 返回值

The exported reflection.

### 参见

-   <span class="methodname">ReflectionParameter::\_\_toString</span>

ReflectionParameter::getClass
=============================

获得类型提示类。

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">ReflectionParameter::getClass</span> ( <span
class="methodparam">void</span> )

获取参数的类型提示类，类型为<span
class="classname">ReflectionClass</span>对象。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

一个 <span class="classname">ReflectionClass</span> 对象。

### 范例

**示例 \#1 使用 <span class="classname">ReflectionParameter</span> 类**

``` php
<?php
function foo(Exception $a) { }

$functionReflection = new ReflectionFunction('foo');
$parameters = $functionReflection->getParameters();
$aParameter = $parameters[0];

echo $aParameter->getClass()->name;
?>
```

以上例程会输出：

    Exception

### 参见

-   <span
    class="methodname">ReflectionParameter::getDeclaringClass</span>

ReflectionParameter::getDeclaringClass
======================================

Gets declaring class

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">ReflectionParameter::getDeclaringClass</span> ( <span
class="methodparam">void</span> )

Gets the declaring class.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

A <span class="classname">ReflectionClass</span> object or **`NULL`** if
called on function.

### 范例

**示例 \#1 Getting the class that declared the method**

``` php
<?php
class Foo
{
    public function bar(\DateTime $datetime)
    {
    }
}

class Baz extends Foo
{
}

$param = new \ReflectionParameter(['Baz', 'bar'], 0); 

var_dump($param->getDeclaringClass());
```

以上例程会输出：

    object(ReflectionClass)#2 (1) {
      ["name"]=>
      string(3) "Foo"
    }

### 参见

-   <span class="methodname">ReflectionParameter::getClass</span>

ReflectionParameter::getDeclaringFunction
=========================================

Gets declaring function

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionFunctionAbstract</span> <span
class="methodname">ReflectionParameter::getDeclaringFunction</span> (
<span class="methodparam">void</span> )

Gets the declaring function.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

A <span class="classname">ReflectionFunction</span> object.

### 参见

-   <span
    class="methodname">ReflectionParameter::getDeclaringClass</span>

ReflectionParameter::getDefaultValue
====================================

Gets default parameter value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ReflectionParameter::getDefaultValue</span> (
<span class="methodparam">void</span> )

Gets the default value of the parameter for any user-defined or internal
function or method. If the parameter is not optional a <span
class="classname">ReflectionException</span> will be thrown.

### 参数

此函数没有参数。

### 返回值

The parameters default value.

### 更新日志

| 版本  | 说明                                                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | This method now allows getting the default value of parameters of built-in functions and built-in class methods. Previously, a <span class="classname">ReflectionException</span> was thrown. |

### 范例

**示例 \#1 Getting default values of function parameters**

``` php
<?php
function foo($test, $bar = 'baz')
{
    echo $test . $bar;
}

$function = new ReflectionFunction('foo');

foreach ($function->getParameters() as $param) {
    echo 'Name: ' . $param->getName() . PHP_EOL;
    if ($param->isOptional()) {
        echo 'Default value: ' . $param->getDefaultValue() . PHP_EOL;
    }
    echo PHP_EOL;
}
?>
```

以上例程会输出：

    Name: test

    Name: bar
    Default value: baz

### 参见

-   <span class="methodname">ReflectionParameter::isOptional</span>
-   <span
    class="methodname">ReflectionParameter::isDefaultValueAvailable</span>
-   <span
    class="methodname">ReflectionParameter::getDefaultValueConstantName</span>
-   <span
    class="methodname">ReflectionParameter::isPassedByReference</span>

ReflectionParameter::getDefaultValueConstantName
================================================

Returns the default value's constant name if default value is constant
or null

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span
class="methodname">ReflectionParameter::getDefaultValueConstantName</span>
( <span class="methodparam">void</span> )

Returns the default value's constant name of the parameter of any
user-defined or internal function or method, if default value is
constant or null. If the parameter is not optional a <span
class="classname">ReflectionException</span> will be thrown.

### 参数

此函数没有参数。

### 返回值

Returns string on success or **`NULL`** on failure.

### 更新日志

| 版本  | 说明                                                                                                                                                                                             |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | This method now allows getting the default values' constant names of built-in functions and built-in class methods. Previously, a <span class="classname">ReflectionException</span> was thrown. |

### 范例

**示例 \#1 Getting default values' constant names of function
parameters**

``` php
<?php
function foo($test, $bar = PHP_INT_MIN)
{
    echo $test . $bar;
}

$function = new ReflectionFunction('foo');

foreach ($function->getParameters() as $param) {
    echo 'Name: ' . $param->getName() . PHP_EOL;
    if ($param->isOptional()) {
        echo 'Default value: ' . $param->getDefaultValueConstantName() . PHP_EOL;
    }
    echo PHP_EOL;
}
?>
```

以上例程会输出：

    Name: test

    Name: bar
    Default value: PHP_INT_MIN

### 参见

-   <span class="methodname">ReflectionParameter::isOptional</span>
-   <span
    class="methodname">ReflectionParameter::isDefaultValueConstant</span>
-   <span class="methodname">ReflectionParameter::getDefaultValue</span>

ReflectionParameter::getName
============================

Gets parameter name

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionParameter::getName</span> ( <span
class="methodparam">void</span> )

Gets the name of the parameter.

### 参数

此函数没有参数。

### 返回值

The name of the reflected parameter.

### 参见

-   <span class="methodname">ReflectionParameter::getValue</span>

ReflectionParameter::getPosition
================================

Gets parameter position

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionParameter::getPosition</span> ( <span
class="methodparam">void</span> )

Gets the position of the parameter.

### 参数

此函数没有参数。

### 返回值

The position of the parameter, left to right, starting at position \#0.

### 参见

-   <span class="methodname">ReflectionParameter::getName</span>

ReflectionParameter::getType
============================

Gets a parameter's type

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionType</span> <span
class="methodname">ReflectionParameter::getType</span> ( <span
class="methodparam">void</span> )

Gets the associated type of a parameter.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="classname">ReflectionType</span> object if a
parameter type is specified, **`NULL`** otherwise.

### 范例

**示例 \#1 <span class="methodname">ReflectionParameter::getType</span>
Usage as of PHP 7.1.0**

As of PHP 7.1.0, <span
class="methodname">ReflectionType::\_\_toString</span> is deprecated,
and <span class="methodname">ReflectionParameter::getType</span> *may*
return an instance of <span
class="classname">ReflectionNamedType</span>. To get the name of the
parameter type, <span class="methodname">ReflectionNamedType</span> is
available in this case.

``` php
<?php
function someFunction(int $param, $param2) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParams = $reflectionFunc->getParameters();
$reflectionType1 = $reflectionParams[0]->getType();
$reflectionType2 = $reflectionParams[1]->getType();

assert($reflectionType1 instanceof ReflectionNamedType);
echo $reflectionType1->getName(), PHP_EOL;
var_dump($reflectionType2);
?>
```

以上例程会输出：

    int
    NULL

**示例 \#2 <span class="methodname">ReflectionParameter::getType</span>
Usage before PHP 7.1.0**

``` php
<?php
function someFunction(int $param, $param2) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParams = $reflectionFunc->getParameters();
$reflectionType1 = $reflectionParams[0]->getType();
$reflectionType2 = $reflectionParams[1]->getType();

echo $reflectionType1, PHP_EOL;
var_dump($reflectionType2);
?>
```

以上例程在 PHP 7.0 中的输出：

    int
    NULL

### 参见

-   <span class="methodname">ReflectionParameter::hasType</span>
-   <span class="methodname">ReflectionType::\_\_toString</span>

ReflectionParameter::hasType
============================

Checks if parameter has a type

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionParameter::hasType</span> ( <span
class="methodparam">void</span> )

Checks if the parameter has a type associated with it.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if a type is specified, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="methodname">ReflectionParameter::hasType</span>
example**

``` php
<?php
function someFunction(string $param, $param2 = null) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParams = $reflectionFunc->getParameters();

var_dump($reflectionParams[0]->hasType());
var_dump($reflectionParams[1]->hasType());
```

以上例程的输出类似于：

    bool(true)
    bool(false)

### 参见

-   <span class="methodname">ReflectionParameter::getType</span>

ReflectionParameter::isArray
============================

Checks if parameter expects an array

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionParameter::isArray</span> ( <span
class="methodparam">void</span> )

Checks if the parameter expects an array.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if an <span class="type">array</span> is expected,
**`FALSE`** otherwise.

### 参见

-   <span class="methodname">ReflectionParameter::isOptional</span>

ReflectionParameter::isCallable
===============================

Returns whether parameter MUST be callable

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionParameter::isCallable</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the parameter is <span
class="type">callable</span>, **`FALSE`** if it is not or **`NULL`** on
failure.

ReflectionParameter::isDefaultValueAvailable
============================================

检查是否有默认值。

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">ReflectionParameter::isDefaultValueAvailable</span> (
<span class="methodparam">void</span> )

检查参数是否有默认值。

### 参数

此函数没有参数。

### 返回值

如果有默认值返回，**`TRUE`** if a default value is available, 否则返回
**`FALSE`**

### 参见

-   <span class="methodname">ReflectionParameter::getDefaultValue</span>
-   <span class="methodname">ReflectionParameter::getName</span>

ReflectionParameter::isDefaultValueConstant
===========================================

Returns whether the default value of this parameter is a constant

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">ReflectionParameter::isDefaultValueConstant</span> (
<span class="methodparam">void</span> )

Returns whether the default value of this parameter is a constant.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the default value is constant, and **`FALSE`**
otherwise.

### 参见

-   <span
    class="methodname">ReflectionParameter::getDefaultValueConstantName</span>
-   <span
    class="methodname">ReflectionParameter::isDefaultValueAvailable</span>

ReflectionParameter::isOptional
===============================

Checks if optional

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionParameter::isOptional</span> ( <span
class="methodparam">void</span> )

Checks if the parameter is optional.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the parameter is optional, otherwise **`FALSE`**

### 参见

-   <span class="methodname">ReflectionParameter::getName</span>

ReflectionParameter::isPassedByReference
========================================

Checks if passed by reference

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionParameter::isPassedByReference</span>
( <span class="methodparam">void</span> )

Checks if the parameter is passed in by reference.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the parameter is passed in by reference, otherwise
**`FALSE`**

### 参见

-   <span class="methodname">ReflectionParameter::getName</span>

ReflectionParameter::isVariadic
===============================

Checks if the parameter is variadic

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionParameter::isVariadic</span> ( <span
class="methodparam">void</span> )

Checks if the parameter was declared as a
<a href="/functions/arguments.html#functions.variable-arg-list.new" class="link">variadic parameter</a>.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the parameter is variadic, otherwise **`FALSE`**.

ReflectionParameter::\_\_toString
=================================

To string

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionParameter::\_\_toString</span> (
<span class="methodparam">void</span> )

To string.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

### 参见

-   <span class="methodname">ReflectionParameter::export</span>
-   <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>

简介
----

<span class="classname">ReflectionProperty</span>
类报告了类的属性的相关信息。

类摘要
------

**ReflectionProperty**

<span class="ooclass"> class **ReflectionProperty** </span> <span
class="oointerface">implements <span
class="interfacename">Reflector</span> </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionProperty::IS_STATIC` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionProperty::IS_PUBLIC` <span class="initializer"> = 256</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionProperty::IS_PROTECTED` <span class="initializer"> =
512</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ReflectionProperty::IS_PRIVATE` <span class="initializer"> =
1024</span> ;

/\* 属性 \*/

<span class="modifier">public</span> `$name` ;

<span class="modifier">public</span> `$class` ;

/\* 方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">\_\_clone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$class`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">export</span> ( <span class="methodparam"><span
class="type">mixed</span> `$class`</span> , <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$return`</span> \] )

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">getDeclaringClass</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getDocComment</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getModifiers</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">?ReflectionType</span> <span
class="methodname">getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getValue</span> (\[ <span
class="methodparam"><span class="type">object</span> `$object`</span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isDefault</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isInitialized</span> (\[ <span
class="methodparam"><span class="type">object</span> `$object`</span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isPrivate</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isProtected</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isPublic</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isStatic</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setAccessible</span> ( <span
class="methodparam"><span class="type">bool</span> `$accessible`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setValue</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

属性
----

`name`  
属性的名称。只读，在尝试赋值的时候抛出 <span
class="classname">ReflectionException</span>。

`class`  
定义的属性所在的类。只读，在尝试赋值的时候抛出 <span
class="classname">ReflectionException</span>。

预定义常量
----------

ReflectionProperty 修饰符
-------------------------

**`ReflectionProperty::IS_STATIC`**  
指示了 <a href="/language/oop5/static.html" class="link">static</a>
的属性。

**`ReflectionProperty::IS_PUBLIC`**  
指示了 <a href="/language/oop5/visibility.html" class="link">public</a>
的属性。

**`ReflectionProperty::IS_PROTECTED`**  
指示了
<a href="/language/oop5/visibility.html" class="link">protected</a>
的属性。

**`ReflectionProperty::IS_PRIVATE`**  
指示了 <a href="/language/oop5/visibility.html" class="link">private</a>
的属性。

ReflectionProperty::\_\_clone
=============================

Clone

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">ReflectionProperty::\_\_clone</span> ( <span
class="methodparam">void</span> )

Clones.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

### 参见

-   <span class="methodname">ReflectionProperty::export</span>
-   <a href="/language/oop5/cloning.html" class="link">Object cloning</a>

ReflectionProperty::\_\_construct
=================================

Construct a ReflectionProperty object

### 说明

<span class="modifier">public</span> <span
class="methodname">ReflectionProperty::\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$class`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`class`  
The class name, that contains the property.

`name`  
The name of the property being reflected.

### 返回值

没有返回值。

### 错误／异常

Trying to get or set private or protected class property's values will
result in an exception being thrown.

### 范例

**示例 \#1 <span
class="methodname">ReflectionProperty::\_\_construct</span> example**

``` php
<?php
class Str
{
    public $length  = 5;
}

// Create an instance of the ReflectionProperty class
$prop = new ReflectionProperty('Str', 'length');

// Print out basic information
printf(
    "===> The%s%s%s%s property '%s' (which was %s)\n" .
    "     having the modifiers %s\n",
        $prop->isPublic() ? ' public' : '',
        $prop->isPrivate() ? ' private' : '',
        $prop->isProtected() ? ' protected' : '',
        $prop->isStatic() ? ' static' : '',
        $prop->getName(),
        $prop->isDefault() ? 'declared at compile-time' : 'created at run-time',
        var_export(Reflection::getModifierNames($prop->getModifiers()), 1)
);

// Create an instance of Str
$obj= new Str();

// Get current value
printf("---> Value is: ");
var_dump($prop->getValue($obj));

// Change value
$prop->setValue($obj, 10);
printf("---> Setting value to 10, new value is: ");
var_dump($prop->getValue($obj));

// Dump object
var_dump($obj);
?>
```

以上例程的输出类似于：

    ===> The public property 'length' (which was declared at compile-time)
         having the modifiers array (
      0 => 'public',
    )
    ---> Value is: int(5)
    ---> Setting value to 10, new value is: int(10)
    object(Str)#2 (1) {
      ["length"]=>
      int(10)
    }

**示例 \#2 Getting value from private and protected properties using
<span class="classname">ReflectionProperty</span> class**

``` php
<?php

class Foo {
    public $x = 1;
    protected $y = 2;
    private $z = 3;
}

$obj = new Foo;

$prop = new ReflectionProperty('Foo', 'y');
$prop->setAccessible(true); /* As of PHP 5.3.0 */
var_dump($prop->getValue($obj)); // int(2)

$prop = new ReflectionProperty('Foo', 'z');
$prop->setAccessible(true); /* As of PHP 5.3.0 */
var_dump($prop->getValue($obj)); // int(2)

?>
```

以上例程的输出类似于：

    int(2)
    int(3)

### 参见

-   <span class="methodname">ReflectionProperty::getName</span>
-   <a href="/language/oop5/decon.html#language.oop5.decon.constructor" class="link">Constructors</a>

ReflectionProperty::export
==========================

Export

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">ReflectionProperty::export</span> ( <span
class="methodparam"><span class="type">mixed</span> `$class`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$return`</span> \] )

Exports a reflection.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`argument`  
导出的反射。

`name`  
The property name.

`return`  
设为 **`TRUE`** 时返回导出结果，设为 **`FALSE`**（默认值）则忽略返回。

### 返回值

### 参见

-   <span class="methodname">ReflectionProperty::\_\_toString</span>

ReflectionProperty::getDeclaringClass
=====================================

Gets declaring class

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionClass</span> <span
class="methodname">ReflectionProperty::getDeclaringClass</span> ( <span
class="methodparam">void</span> )

Gets the declaring class.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

A <span class="classname">ReflectionClass</span> object.

### 参见

-   <span class="methodname">ReflectionProperty::getName</span>

ReflectionProperty::getDocComment
=================================

Gets the property doc comment

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionProperty::getDocComment</span> (
<span class="methodparam">void</span> )

Gets the doc comment for a property.

### 参数

此函数没有参数。

### 返回值

The property doc comment.

### 范例

**示例 \#1 <span
class="methodname">ReflectionProperty::getDocComment</span> example**

``` php
<?php
class Str
{
    /**
     * @var int  The length of the string
     */
    public $length = 5;
}

$prop = new ReflectionProperty('Str', 'length');

var_dump($prop->getDocComment());

?>
```

以上例程的输出类似于：

    string(53) "/**
         * @var int  The length of the string
         */"

**示例 \#2 Multiple property declarations**

If multiple property declarations are preceeded by a single doc comment,
the doc comment refers to the first property only.

``` php
<?php
class Foo
{
    /** @var string */
    public $a, $b;
}
$class = new \ReflectionClass('Foo');
foreach ($class->getProperties() as $property) {
    echo $property->getName() . ': ' . var_export($property->getDocComment(), true) . PHP_EOL;
}
?>
```

以上例程会输出：

    a: '/** @var string */'
    b: false

### 参见

-   <span class="methodname">ReflectionProperty::getModifiers</span>
-   <span class="methodname">ReflectionProperty::getName</span>
-   <span class="methodname">ReflectionProperty::getValue</span>

ReflectionProperty::getModifiers
================================

Gets the property modifiers

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionProperty::getModifiers</span> ( <span
class="methodparam">void</span> )

Gets the modifiers.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

A numeric representation of the modifiers.

### 参见

-   <span class="methodname">ReflectionProperty::isPrivate</span>
-   <span class="methodname">Reflection::getModifierNames</span>

ReflectionProperty::getName
===========================

Gets property name

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionProperty::getName</span> ( <span
class="methodparam">void</span> )

Gets the properties name.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The name of the reflected property.

### 参见

-   <span class="methodname">ReflectionProperty::getValue</span>

ReflectionProperty::getType
===========================

Gets a property's type

### 说明

<span class="modifier">public</span> <span
class="type">?ReflectionType</span> <span
class="methodname">ReflectionProperty::getType</span> ( <span
class="methodparam">void</span> )

Gets the associated type of a property.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="classname">ReflectionType</span> if the property
has a type, and **`NULL`** otherwise.

### 范例

**示例 \#1 <span class="methodname">ReflectionProperty::getType</span>
example**

``` php
<?php
class User
{
    public string $name;
}

$rp = new ReflectionProperty('User', 'name');
echo $rp->getType()->getName();
?>
```

以上例程会输出：

    string

### 参见

-   <span class="methodname">ReflectionProperty::hasType</span>
-   <span class="methodname">ReflectionProperty::isInitialized</span>

ReflectionProperty::getValue
============================

Gets value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ReflectionProperty::getValue</span> (\[ <span
class="methodparam"><span class="type">object</span> `$object`</span> \]
)

Gets the property's value.

### 参数

`object`  
If the property is non-static an object must be provided to fetch the
property from. If you want to fetch the default property without
providing an object use <span
class="methodname">ReflectionClass::getDefaultProperties</span> instead.

### 返回值

The current value of the property.

### 错误／异常

Throws a <span class="classname">ReflectionException</span> if the
property is inaccessible. You can make a protected or private property
accessible using <span
class="methodname">ReflectionProperty::setAccessible</span>.

### 范例

**示例 \#1 <span class="methodname">ReflectionProperty::getValue</span>
example**

``` php
<?php
class Foo {
    public static $staticProperty = 'foobar';
    
    public $property = 'barfoo';
    protected $privateProperty = 'foofoo';
}

$reflectionClass = new ReflectionClass('Foo');

var_dump($reflectionClass->getProperty('staticProperty')->getValue());
var_dump($reflectionClass->getProperty('property')->getValue(new Foo));

$reflectionProperty = $reflectionClass->getProperty('privateProperty');
$reflectionProperty->setAccessible(true);
var_dump($reflectionProperty->getValue(new Foo));
?>
```

以上例程会输出：

    string(6) "foobar"
    string(6) "barfoo"
    string(6) "foofoo"

### 参见

-   <span class="methodname">ReflectionProperty::setValue</span>
-   <span class="methodname">ReflectionProperty::setAccessible</span>
-   <span
    class="methodname">ReflectionClass::getDefaultProperties</span>
-   <span
    class="methodname">ReflectionClass::getStaticPropertyValue</span>

ReflectionProperty::hasType
===========================

Checks if property has a type

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionProperty::hasType</span> ( <span
class="methodparam">void</span> )

Checks if the property has a type associated with it.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if a type is specified, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="methodname">ReflectionProperty::hasType</span>
example**

``` php
<?php
class User
{
    public string $name;
}

$rp = new ReflectionProperty('User', 'name');
var_dump($rp->hasType());
?>
```

以上例程会输出：

    bool(true)

### 参见

-   <span class="methodname">ReflectionProperty::getType</span>
-   <span class="methodname">ReflectionProperty::isInitialized</span>

ReflectionProperty::isDefault
=============================

Checks if property is a default property

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionProperty::isDefault</span> ( <span
class="methodparam">void</span> )

Checks whether the property was declared at compile-time, or whether the
property was dynamically declared at run-time.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the property was declared at compile-time, or **`FALSE`**
if it was created at run-time.

### 范例

**示例 \#1 <span class="methodname">ReflectionClass::isDefault</span>
example**

``` php
<?php
class Foo {
    public $bar;
}

$o = new Foo();
$o->bar = 42;
$o->baz = 42;

$ro = new ReflectionObject($o);
var_dump($ro->getProperty('bar')->isDefault());
var_dump($ro->getProperty('baz')->isDefault());
?>
```

以上例程会输出：

    bool(true)
    bool(false)

### 参见

-   <span class="methodname">ReflectionProperty::getValue</span>

ReflectionProperty::isInitialized
=================================

Checks whether a property is initialized

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionProperty::isInitialized</span> (\[
<span class="methodparam"><span class="type">object</span>
`$object`</span> \] )

Checks whether a property is initialized.

### 参数

`object`  
If the property is non-static an object must be provided to fetch the
property from.

### 返回值

Returns **`FALSE`** for typed properties prior to initialization, and
for properties that have been explicitly <span
class="function">unset</span>. For all other properties **`TRUE`** will
be returned.

### 错误／异常

Throws a <span class="classname">ReflectionException</span> if the
property is inaccessible. You can make a protected or private property
accessible using <span
class="methodname">ReflectionProperty::setAccessible</span>.

### 范例

**示例 \#1 <span
class="methodname">ReflectionProperty::isInitialized</span> example**

``` php
<?php
class User
{
    public string $name;
}

$rp = new ReflectionProperty('User', 'name');
$user = new User;
var_dump($rp->isInitialized($user));
$user->name = 'Nikita';
var_dump($rp->isInitialized($user));
?>
```

以上例程会输出：

    bool(false)
    bool(true)

### 参见

-   <span class="methodname">ReflectionProperty::hasType</span>

ReflectionProperty::isPrivate
=============================

Checks if property is private

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionProperty::isPrivate</span> ( <span
class="methodparam">void</span> )

Checks whether the property is private.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the property is private, **`FALSE`** otherwise.

### 参见

-   <span class="methodname">ReflectionProperty::isPublic</span>
-   <span class="methodname">ReflectionProperty::isProtected</span>
-   <span class="methodname">ReflectionProperty::isStatic</span>

ReflectionProperty::isProtected
===============================

Checks if property is protected

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionProperty::isProtected</span> ( <span
class="methodparam">void</span> )

Checks whether the property is protected.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the property is protected, **`FALSE`** otherwise.

### 参见

-   <span class="methodname">ReflectionProperty::isPublic</span>
-   <span class="methodname">ReflectionProperty::isPrivate</span>
-   <span class="methodname">ReflectionProperty::isStatic</span>

ReflectionProperty::isPublic
============================

Checks if property is public

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionProperty::isPublic</span> ( <span
class="methodparam">void</span> )

Checks whether the property is public.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the property is public, **`FALSE`** otherwise.

### 参见

-   <span class="methodname">ReflectionProperty::isProtected</span>
-   <span class="methodname">ReflectionProperty::isPrivate</span>
-   <span class="methodname">ReflectionProperty::isStatic</span>

ReflectionProperty::isStatic
============================

Checks if property is static

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionProperty::isStatic</span> ( <span
class="methodparam">void</span> )

Checks whether the property is static.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the property is static, **`FALSE`** otherwise.

### 参见

-   <span class="methodname">ReflectionProperty::isPublic</span>
-   <span class="methodname">ReflectionProperty::isProtected</span>
-   <span class="methodname">ReflectionProperty::isPrivate</span>

ReflectionProperty::setAccessible
=================================

Set property accessibility

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ReflectionProperty::setAccessible</span> (
<span class="methodparam"><span class="type">bool</span>
`$accessible`</span> )

Sets a property to be accessible. For example, it may allow protected
and private properties to be accessed.

### 参数

`accessible`  
**`TRUE`** to allow accessibility, or **`FALSE`**.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">ReflectionProperty::isPrivate</span>
-   <span class="methodname">ReflectionProperty::isProtected</span>

ReflectionProperty::setValue
============================

Set property value

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ReflectionProperty::setValue</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ReflectionProperty::setValue</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

Sets (changes) the property's value.

### 参数

`object`  
If the property is non-static an object must be provided to change the
property on. If the property is static this parameter is left out and
only `value` needs to be provided.

`value`  
The new value.

### 返回值

没有返回值。

### 错误／异常

Throws a <span class="classname">ReflectionException</span> if the
property is inaccessible. You can make a protected or private property
accessible using <span
class="methodname">ReflectionProperty::setAccessible</span>.

### 范例

**示例 \#1 <span class="methodname">ReflectionProperty::setValue</span>
example**

``` php
<?php
class Foo {
    public static $staticProperty;
    
    public $property;
    protected $privateProperty;
}

$reflectionClass = new ReflectionClass('Foo');

$reflectionClass->getProperty('staticProperty')->setValue('foo');
var_dump(Foo::$staticProperty);

$foo = new Foo;

$reflectionClass->getProperty('property')->setValue($foo, 'bar');
var_dump($foo->property);

$reflectionProperty = $reflectionClass->getProperty('privateProperty');
$reflectionProperty->setAccessible(true);
$reflectionProperty->setValue($foo, 'foobar');
var_dump($reflectionProperty->getValue($foo));
?>
```

以上例程会输出：

    string(3) "foo"
    string(3) "bar"
    string(6) "foobar"

### 参见

-   <span class="methodname">ReflectionProperty::getValue</span>
-   <span class="methodname">ReflectionProperty::setAccessible</span>
-   <span
    class="methodname">ReflectionClass::setStaticPropertyValue</span>

ReflectionProperty::\_\_toString
================================

To string

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionProperty::\_\_toString</span> ( <span
class="methodparam">void</span> )

To string.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

### 参见

-   <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>

简介
----

<span class="classname">ReflectionType</span>
类用于获取函数、类方法的参数或者返回值的类型。

类摘要
------

**ReflectionType**

<span class="ooclass"> class **ReflectionType** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">allowsNull</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isBuiltin</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

ReflectionType::allowsNull
==========================

Checks if null is allowed

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionType::allowsNull</span> ( <span
class="methodparam">void</span> )

Checks whether the parameter allows **`NULL`**.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if **`NULL`** is allowed, otherwise **`FALSE`**

### 范例

**示例 \#1 <span class="methodname">ReflectionType::allowsNull</span>
example**

``` php
<?php
function someFunction(string $param, StdClass $param2 = null) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParams = $reflectionFunc->getParameters();

var_dump($reflectionParams[0]->getType()->allowsNull());
var_dump($reflectionParams[1]->getType()->allowsNull());
```

以上例程的输出类似于：

    bool(false)
    bool(true)

### 参见

-   <span class="methodname">ReflectionType::isBuiltin</span>
-   <span class="methodname">ReflectionType::\_\_toString</span>
-   <span class="methodname">ReflectionParameter::getType</span>

ReflectionType::isBuiltin
=========================

Checks if it is a built-in type

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ReflectionType::isBuiltin</span> ( <span
class="methodparam">void</span> )

Checks if the type is a built-in type in PHP.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if it's a built-in type, otherwise **`FALSE`**

### 范例

**示例 \#1 <span class="methodname">ReflectionType::isBuiltin</span>
example**

``` php
<?php
class SomeClass {}

function someFunction(string $param, SomeClass $param2, StdClass $param3) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParams = $reflectionFunc->getParameters();

var_dump($reflectionParams[0]->getType()->isBuiltin());
var_dump($reflectionParams[1]->getType()->isBuiltin());
var_dump($reflectionParams[2]->getType()->isBuiltin());
```

以上例程的输出类似于：

    bool(true)
    bool(false)
    bool(false)

Note that the <span class="methodname">ReflectionType::isBuiltin</span>
method does not distinguish between internal and custom classes. To make
this distinction, the <span
class="methodname">ReflectionClass::isInternal</span> method should be
used on the returned class name.

### 参见

-   <span class="methodname">ReflectionType::allowsNull</span>
-   <span class="methodname">ReflectionType::\_\_toString</span>
-   <span class="methodname">ReflectionClass::isInternal</span>
-   <span class="methodname">ReflectionParameter::getType</span>

ReflectionType::\_\_toString
============================

To string

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionType::\_\_toString</span> ( <span
class="methodparam">void</span> )

Gets the parameter type name.

### 参数

此函数没有参数。

### 返回值

Returns the type of the parameter.

### 范例

**示例 \#1 <span class="methodname">ReflectionType::\_\_toString</span>
example**

``` php
<?php
function someFunction(string $param) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParam = $reflectionFunc->getParameters()[0];

echo $reflectionParam->getType();
```

以上例程的输出类似于：

    string

### 更新日志

| 版本  | 说明                                                                              |
|-------|-----------------------------------------------------------------------------------|
| 7.1.0 | <span class="methodname">ReflectionType::\_\_toString</span> has been deprecated. |

### 参见

-   <span class="methodname">ReflectionNamedType::getName</span>
-   <span class="methodname">ReflectionType::allowsNull</span>
-   <span class="methodname">ReflectionType::isBuiltin</span>
-   <span class="methodname">ReflectionParameter::getType</span>

简介
----

<span
class="classname">ReflectionGenerator</span>类用于获取生成器的信息。

类摘要
------

**ReflectionGenerator**

<span class="ooclass"> class **ReflectionGenerator** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">Generator</span>
`$generator`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getExecutingFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Generator</span>
<span class="methodname">getExecutingGenerator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getExecutingLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReflectionFunctionAbstract</span> <span
class="methodname">getFunction</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">getThis</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getTrace</span> (\[ <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = DEBUG\_BACKTRACE\_PROVIDE\_OBJECT</span></span>
\] )

}

ReflectionGenerator::\_\_construct
==================================

Constructs a ReflectionGenerator object

### 说明

<span class="modifier">public</span> <span
class="methodname">ReflectionGenerator::\_\_construct</span> ( <span
class="methodparam"><span class="type">Generator</span>
`$generator`</span> )

Constructs a <span class="classname">ReflectionGenerator</span> object.

### 参数

`generator`  
A generator object.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span
class="methodname">ReflectionGenerator::\_\_construct</span> example**

``` php
<?php

function gen()
{
    yield 1;
}

$gen = gen();

$reflectionGen = new ReflectionGenerator($gen);

echo <<< output
{$reflectionGen->getFunction()->name}
Line: {$reflectionGen->getExecutingLine()}
File: {$reflectionGen->getExecutingFile()}
output;
```

以上例程的输出类似于：

    gen
    Line: 5
    File: /path/to/file/example.php

### 参见

-   <span class="methodname">ReflectionGenerator::getFunction</span>
-   <span
    class="methodname">ReflectionGenerator::getExecutingLine</span>
-   <span
    class="methodname">ReflectionGenerator::getExecutingFile</span>

ReflectionGenerator::getExecutingFile
=====================================

Gets the file name of the currently executing generator

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ReflectionGenerator::getExecutingFile</span> (
<span class="methodparam">void</span> )

Get the full path and file name of the currently executing generator.

### 参数

此函数没有参数。

### 返回值

Returns the full path and file name of the currently executing
generator.

### 范例

**示例 \#1 <span
class="methodname">ReflectionGenerator::getExecutingFile</span>
example**

``` php
<?php

class GenExample
{
    public function gen()
    {
        yield 1;
    }
}

$gen = (new GenExample)->gen();

$reflectionGen = new ReflectionGenerator($gen);

echo "File: {$reflectionGen->getExecutingFile()}";
```

以上例程的输出类似于：

    File: /path/to/file/example.php

### 参见

-   <span
    class="methodname">ReflectionGenerator::getExecutingLine</span>
-   <span
    class="methodname">ReflectionGenerator::getExecutingGenerator</span>

ReflectionGenerator::getExecutingGenerator
==========================================

Gets the executing <span class="classname">Generator</span> object

### 说明

<span class="modifier">public</span> <span class="type">Generator</span>
<span
class="methodname">ReflectionGenerator::getExecutingGenerator</span> (
<span class="methodparam">void</span> )

Get the executing <span class="classname">Generator</span> object

### 参数

此函数没有参数。

### 返回值

Returns the currently executing <span class="classname">Generator</span>
object.

### 范例

**示例 \#1 <span
class="methodname">ReflectionGenerator::getExecutingGenerator</span>
example**

``` php
<?php

class GenExample
{
    public function gen()
    {
        yield 1;
    }
}

$gen = (new GenExample)->gen();

$reflectionGen = new ReflectionGenerator($gen);

$gen2 = $reflectionGen->getExecutingGenerator();

var_dump($gen2 === $gen);
var_dump($gen2->current());
```

以上例程的输出类似于：

    bool(true)
    int(1);

### 参见

-   <span
    class="methodname">ReflectionGenerator::getExecutingLine</span>
-   <span
    class="methodname">ReflectionGenerator::getExecutingFile</span>

ReflectionGenerator::getExecutingLine
=====================================

Gets the currently executing line of the generator

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ReflectionGenerator::getExecutingLine</span> ( <span
class="methodparam">void</span> )

Get the currently executing line number of the generator.

### 参数

此函数没有参数。

### 返回值

Returns the line number of the currently executing statement in the
generator.

### 范例

**示例 \#1 <span
class="methodname">ReflectionGenerator::getExecutingLine</span>
example**

``` php
<?php

class GenExample
{
    public function gen()
    {
        yield 1;
    }
}

$gen = (new GenExample)->gen();

$reflectionGen = new ReflectionGenerator($gen);

echo "Line: {$reflectionGen->getExecutingLine()}";
```

以上例程的输出类似于：

    Line: 7

### 参见

-   <span
    class="methodname">ReflectionGenerator::getExecutingGenerator</span>
-   <span
    class="methodname">ReflectionGenerator::getExecutingFile</span>

ReflectionGenerator::getFunction
================================

Gets the function name of the generator

### 说明

<span class="modifier">public</span> <span
class="type">ReflectionFunctionAbstract</span> <span
class="methodname">ReflectionGenerator::getFunction</span> ( <span
class="methodparam">void</span> )

Enables the function name of the generator to be obtained by returning a
class derived from <span
class="classname">ReflectionFunctionAbstract</span>.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="classname">ReflectionFunctionAbstract</span>
class. This will be <span class="classname">ReflectionFunction</span>
for functions, or <span class="classname">ReflectionMethod</span> for
methods.

### 范例

**示例 \#1 <span
class="methodname">ReflectionGenerator::getFunction</span> example**

``` php
<?php

function gen()
{
    yield 1;
}

$gen = gen();

$reflectionGen = new ReflectionGenerator($gen);

var_dump($reflectionGen->getFunction());
```

以上例程的输出类似于：

    object(ReflectionFunction)#3 (1) {
      ["name"]=>
      string(3) "gen"
    }

### 参见

-   <span class="methodname">ReflectionGenerator::getThis</span>
-   <span class="methodname">ReflectionGenerator::getTrace</span>

ReflectionGenerator::getThis
============================

Gets the *$this* value of the generator

### 说明

<span class="modifier">public</span> <span class="type">object</span>
<span class="methodname">ReflectionGenerator::getThis</span> ( <span
class="methodparam">void</span> )

Get the *$this* value that the generator has access to.

### 参数

此函数没有参数。

### 返回值

Returns the *$this* value, or **`NULL`** if the generator was not
created in a class context.

### 范例

**示例 \#1 <span class="methodname">ReflectionGenerator::getThis</span>
example**

``` php
<?php

class GenExample
{
    public function gen()
    {
        yield 1;
    }
}

$gen = (new GenExample)->gen();

$reflectionGen = new ReflectionGenerator($gen);

var_dump($reflectionGen->getThis());
```

以上例程的输出类似于：

    object(GenExample)#3 (0) {
    }

### 参见

-   <span class="methodname">ReflectionGenerator::getFunction</span>
-   <span class="methodname">ReflectionGenerator::getTrace</span>

ReflectionGenerator::getTrace
=============================

Gets the trace of the executing generator

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ReflectionGenerator::getTrace</span> (\[ <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = DEBUG\_BACKTRACE\_PROVIDE\_OBJECT</span></span>
\] )

Get the trace of the currently executing generator.

### 参数

`options`  
The value of `options` can be any of the following flags.

| Option                               | Description                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| **`DEBUG_BACKTRACE_PROVIDE_OBJECT`** | Default.                                                                 |
| **`DEBUG_BACKTRACE_IGNORE_ARGS`**    | Don't include the argument information for functions in the stack trace. |

### 返回值

Returns the trace of the currently executing generator.

### 范例

**示例 \#1 <span class="methodname">ReflectionGenerator::getTrace</span>
example**

``` php
<?php
function foo() {
    yield 1;
}

function bar()
{
    yield from foo();
}

function baz()
{
    yield from bar();
}

$gen = baz();
$gen->valid(); // start the generator

var_dump((new ReflectionGenerator($gen))->getTrace());
```

以上例程的输出类似于：

    array(2) {
      [0]=>
      array(4) {
        ["file"]=>
        string(18) "example.php"
        ["line"]=>
        int(8)
        ["function"]=>
        string(3) "foo"
        ["args"]=>
        array(0) {
        }
      }
      [1]=>
      array(4) {
        ["file"]=>
        string(18) "example.php"
        ["line"]=>
        int(12)
        ["function"]=>
        string(3) "bar"
        ["args"]=>
        array(0) {
        }
      }
    }

### 参见

-   <span class="methodname">ReflectionGenerator::getFunction</span>
-   <span class="methodname">ReflectionGenerator::getThis</span>

简介
----

<span class="classname">Reflector</span>
是一个接口，被所有可导出的反射类所实现（implement）。

类摘要
------

**Reflector**

<span class="ooclass"> class **Reflector** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">export</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

Reflector::export
=================

Exports

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Reflector::export</span> ( <span
class="methodparam">void</span> )

输出。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

### 参见

-   <span class="methodname">Reflection::\_\_toString</span>

Reflector::\_\_toString
=======================

转化成字符串

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Reflector::\_\_toString</span> ( <span
class="methodparam">void</span> )

转化成字符串。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

### 参见

-   <span class="methodname">ReflectionProperty::export</span>
-   <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>

简介
----

ReflectionException 类。

类摘要
------

**ReflectionException**

<span class="ooclass"> class **ReflectionException** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}
