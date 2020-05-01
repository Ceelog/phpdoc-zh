Yet Another Framework
=====================

**目录**

-   [简介](/intro/yaf.html)
-   [安装／配置](/yaf/setup.html)
    -   [需求](/yaf/setup.html#需求)
    -   [安装](/yaf/setup.html#安装)
    -   [运行时配置](/yaf/setup.html#运行时配置)
    -   [资源类型](/yaf/setup.html#资源类型)
-   [预定义常量](/yaf/constants.html)
-   [范例](/yaf/tutorials.html)
-   [应用配置](/yaf/appconfig.html)
-   [Yaf\_Application](/class/yaf-application.html) — The
    Yaf\_Application class
    -   [Yaf\_Application::app](/class/yaf-application.html#Yaf_Application::app)
        — 获取当前的Yaf\_Application实例
    -   [Yaf\_Application::bootstrap](/class/yaf-application.html#Yaf_Application::bootstrap)
        — 调用bootstrap
    -   [Yaf\_Application::clearLastError](/class/yaf-application.html#Yaf_Application::clearLastError)
        — 清除最后的错误信息
    -   [Yaf\_Application::\_\_construct](/class/yaf-application.html#Yaf_Application::__construct)
        — Yaf\_Application的构造函数
    -   [Yaf\_Application::\_\_destruct](/class/yaf-application.html#Yaf_Application::__destruct)
        — 析构函数
    -   [Yaf\_Application::environ](/class/yaf-application.html#Yaf_Application::environ)
        — 获取当前Yaf\_Application的环境名
    -   [Yaf\_Application::execute](/class/yaf-application.html#Yaf_Application::execute)
        — 运行回调函数
    -   [Yaf\_Application::getAppDirectory](/class/yaf-application.html#Yaf_Application::getAppDirectory)
        — 获取应用的目录
    -   [Yaf\_Application::getConfig](/class/yaf-application.html#Yaf_Application::getConfig)
        — 获取 Yaf\_Config\_Abstract 的实例
    -   [Yaf\_Application::getDispatcher](/class/yaf-application.html#Yaf_Application::getDispatcher)
        — 获取 Yaf\_Dispatcher 的实例
    -   [Yaf\_Application::getLastErrorMsg](/class/yaf-application.html#Yaf_Application::getLastErrorMsg)
        — 获取最近产生的错误的错误信息
    -   [Yaf\_Application::getLastErrorNo](/class/yaf-application.html#Yaf_Application::getLastErrorNo)
        — 获取最后产生的错误的错误代码
    -   [Yaf\_Application::getModules](/class/yaf-application.html#Yaf_Application::getModules)
        — 获取在配置文件中申明的模块
    -   [Yaf\_Application::run](/class/yaf-application.html#Yaf_Application::run)
        — 运行 Yaf\_Application
    -   [Yaf\_Application::setAppDirectory](/class/yaf-application.html#Yaf_Application::setAppDirectory)
        — 改变应用目录
-   [Yaf\_Bootstrap\_Abstract](/class/yaf-bootstrap-abstract.html) — The
    Yaf\_Bootstrap\_Abstract class
-   [Yaf\_Dispatcher](/class/yaf-dispatcher.html) — Yaf\_Dispatcher 类
    -   [Yaf\_Dispatcher::autoRender](/class/yaf-dispatcher.html#Yaf_Dispatcher::autoRender)
        — 开启/关闭自动渲染功能
    -   [Yaf\_Dispatcher::catchException](/class/yaf-dispatcher.html#Yaf_Dispatcher::catchException)
        — 开启/关闭自动异常捕获功能
    -   [Yaf\_Dispatcher::\_\_construct](/class/yaf-dispatcher.html#Yaf_Dispatcher::__construct)
        — Yaf\_Dispatcher 构造函数
    -   [Yaf\_Dispatcher::disableView](/class/yaf-dispatcher.html#Yaf_Dispatcher::disableView)
        — 关闭自动渲染
    -   [Yaf\_Dispatcher::dispatch](/class/yaf-dispatcher.html#Yaf_Dispatcher::dispatch)
        — 分发请求
    -   [Yaf\_Dispatcher::enableView](/class/yaf-dispatcher.html#Yaf_Dispatcher::enableView)
        — 开启自动渲染
    -   [Yaf\_Dispatcher::flushInstantly](/class/yaf-dispatcher.html#Yaf_Dispatcher::flushInstantly)
        — 打开关闭自动响应
    -   [Yaf\_Dispatcher::getApplication](/class/yaf-dispatcher.html#Yaf_Dispatcher::getApplication)
        — 获取当前的Yaf\_Application实例
    -   [Yaf\_Dispatcher::getDefaultAction](/class/yaf-dispatcher.html#Yaf_Dispatcher::getDefaultAction)
        — Retrive the default action name
    -   [Yaf\_Dispatcher::getDefaultController](/class/yaf-dispatcher.html#Yaf_Dispatcher::getDefaultController)
        — Retrive the default controller name
    -   [Yaf\_Dispatcher::getDefaultModule](/class/yaf-dispatcher.html#Yaf_Dispatcher::getDefaultModule)
        — Retrive the default module name
    -   [Yaf\_Dispatcher::getInstance](/class/yaf-dispatcher.html#Yaf_Dispatcher::getInstance)
        — 获取当前的Yaf\_Dispatcher实例
    -   [Yaf\_Dispatcher::getRequest](/class/yaf-dispatcher.html#Yaf_Dispatcher::getRequest)
        — 获取当前的请求实例
    -   [Yaf\_Dispatcher::getRouter](/class/yaf-dispatcher.html#Yaf_Dispatcher::getRouter)
        — 获取路由器
    -   [Yaf\_Dispatcher::initView](/class/yaf-dispatcher.html#Yaf_Dispatcher::initView)
        — 初始化视图引擎并返回它
    -   [Yaf\_Dispatcher::registerPlugin](/class/yaf-dispatcher.html#Yaf_Dispatcher::registerPlugin)
        — 注册一个插件
    -   [Yaf\_Dispatcher::returnResponse](/class/yaf-dispatcher.html#Yaf_Dispatcher::returnResponse)
        — The returnResponse purpose
    -   [Yaf\_Dispatcher::setDefaultAction](/class/yaf-dispatcher.html#Yaf_Dispatcher::setDefaultAction)
        — 设置路由的默认动作
    -   [Yaf\_Dispatcher::setDefaultController](/class/yaf-dispatcher.html#Yaf_Dispatcher::setDefaultController)
        — 设置路由的默认控制器
    -   [Yaf\_Dispatcher::setDefaultModule](/class/yaf-dispatcher.html#Yaf_Dispatcher::setDefaultModule)
        — 设置路由的默认模块
    -   [Yaf\_Dispatcher::setErrorHandler](/class/yaf-dispatcher.html#Yaf_Dispatcher::setErrorHandler)
        — 设置错误处理函数
    -   [Yaf\_Dispatcher::setRequest](/class/yaf-dispatcher.html#Yaf_Dispatcher::setRequest)
        — The setRequest purpose
    -   [Yaf\_Dispatcher::setView](/class/yaf-dispatcher.html#Yaf_Dispatcher::setView)
        — 设置视图引擎
    -   [Yaf\_Dispatcher::throwException](/class/yaf-dispatcher.html#Yaf_Dispatcher::throwException)
        — 开启/关闭异常抛出
-   [Yaf\_Config\_Abstract](/class/yaf-config-abstract.html) — The
    Yaf\_Config\_Abstract class
    -   [Yaf\_Config\_Abstract::get](/class/yaf-config-abstract.html#Yaf_Config_Abstract::get)
        — Getter
    -   [Yaf\_Config\_Abstract::readonly](/class/yaf-config-abstract.html#Yaf_Config_Abstract::readonly)
        — 寻找只读配置
    -   [Yaf\_Config\_Abstract::set](/class/yaf-config-abstract.html#Yaf_Config_Abstract::set)
        — Setter
    -   [Yaf\_Config\_Abstract::toArray](/class/yaf-config-abstract.html#Yaf_Config_Abstract::toArray)
        — 转换为数组
-   [Yaf\_Config\_Ini](/class/yaf-config-ini.html) — The
    Yaf\_Config\_Ini class
    -   [Yaf\_Config\_Ini::\_\_construct](/class/yaf-config-ini.html#Yaf_Config_Ini::__construct)
        — 构造函数
    -   [Yaf\_Config\_Ini::count](/class/yaf-config-ini.html#Yaf_Config_Ini::count)
        — 返回配置的节数量
    -   [Yaf\_Config\_Ini::current](/class/yaf-config-ini.html#Yaf_Config_Ini::current)
        — 返回当前节点
    -   [Yaf\_Config\_Ini::\_\_get](/class/yaf-config-ini.html#Yaf_Config_Ini::__get)
        — 读取节点配置
    -   [Yaf\_Config\_Ini::\_\_isset](/class/yaf-config-ini.html#Yaf_Config_Ini::__isset)
        — 检查节点是否存在
    -   [Yaf\_Config\_Ini::key](/class/yaf-config-ini.html#Yaf_Config_Ini::key)
        — 返回当前元素的键
    -   [Yaf\_Config\_Ini::next](/class/yaf-config-ini.html#Yaf_Config_Ini::next)
        — 向前移动到下一个元素
    -   [Yaf\_Config\_Ini::offsetExists](/class/yaf-config-ini.html#Yaf_Config_Ini::offsetExists)
        — 检查一个偏移位置是否存在
    -   [Yaf\_Config\_Ini::offsetGet](/class/yaf-config-ini.html#Yaf_Config_Ini::offsetGet)
        — 获取一个偏移位置的值
    -   [Yaf\_Config\_Ini::offsetSet](/class/yaf-config-ini.html#Yaf_Config_Ini::offsetSet)
        — 设置一个偏移位置的值
    -   [Yaf\_Config\_Ini::offsetUnset](/class/yaf-config-ini.html#Yaf_Config_Ini::offsetUnset)
        — 复位一个偏移位置的值
    -   [Yaf\_Config\_Ini::readonly](/class/yaf-config-ini.html#Yaf_Config_Ini::readonly)
        — 检查配置是否只读
    -   [Yaf\_Config\_Ini::rewind](/class/yaf-config-ini.html#Yaf_Config_Ini::rewind)
        — 检查当前位置是否有效
    -   [Yaf\_Config\_Ini::\_\_set](/class/yaf-config-ini.html#Yaf_Config_Ini::__set)
        — The \_\_set purpose
    -   [Yaf\_Config\_Ini::toArray](/class/yaf-config-ini.html#Yaf_Config_Ini::toArray)
        — 转换为数组的格式
    -   [Yaf\_Config\_Ini::valid](/class/yaf-config-ini.html#Yaf_Config_Ini::valid)
        — 检查迭代器是否有效
-   [Yaf\_Config\_Simple](/class/yaf-config-simple.html) — The
    Yaf\_Config\_Simple class
    -   [Yaf\_Config\_Simple::\_\_construct](/class/yaf-config-simple.html#Yaf_Config_Simple::__construct)
        — 构造函数
    -   [Yaf\_Config\_Simple::count](/class/yaf-config-simple.html#Yaf_Config_Simple::count)
        — 返回配置的节数量
    -   [Yaf\_Config\_Simple::current](/class/yaf-config-simple.html#Yaf_Config_Simple::current)
        — 返回当前节点
    -   [Yaf\_Config\_Simple::\_\_get](/class/yaf-config-simple.html#Yaf_Config_Simple::__get)
        — 读取节点配置
    -   [Yaf\_Config\_Simple::\_\_isset](/class/yaf-config-simple.html#Yaf_Config_Simple::__isset)
        — 检查节点是否存在
    -   [Yaf\_Config\_Simple::key](/class/yaf-config-simple.html#Yaf_Config_Simple::key)
        — 返回当前元素的键
    -   [Yaf\_Config\_Simple::next](/class/yaf-config-simple.html#Yaf_Config_Simple::next)
        — 向前移动到下一个元素
    -   [Yaf\_Config\_Simple::offsetExists](/class/yaf-config-simple.html#Yaf_Config_Simple::offsetExists)
        — 检查一个偏移位置是否存在
    -   [Yaf\_Config\_Simple::offsetGet](/class/yaf-config-simple.html#Yaf_Config_Simple::offsetGet)
        — 获取一个偏移位置的值
    -   [Yaf\_Config\_Simple::offsetSet](/class/yaf-config-simple.html#Yaf_Config_Simple::offsetSet)
        — 设置一个偏移位置的值
    -   [Yaf\_Config\_Simple::offsetUnset](/class/yaf-config-simple.html#Yaf_Config_Simple::offsetUnset)
        — 复位一个偏移位置的值
    -   [Yaf\_Config\_Simple::readonly](/class/yaf-config-simple.html#Yaf_Config_Simple::readonly)
        — 检查配置是否只读
    -   [Yaf\_Config\_Simple::rewind](/class/yaf-config-simple.html#Yaf_Config_Simple::rewind)
        — 检查当前位置是否有效
    -   [Yaf\_Config\_Simple::\_\_set](/class/yaf-config-simple.html#Yaf_Config_Simple::__set)
        — 设置节点配置
    -   [Yaf\_Config\_Simple::toArray](/class/yaf-config-simple.html#Yaf_Config_Simple::toArray)
        — 转换为数组的格式
    -   [Yaf\_Config\_Simple::valid](/class/yaf-config-simple.html#Yaf_Config_Simple::valid)
        — 检查迭代器是否有效
-   [Yaf\_Controller\_Abstract](/class/yaf-controller-abstract.html) —
    The Yaf\_Controller\_Abstract class
    -   [Yaf\_Controller\_Abstract::\_\_construct](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::__construct)
        — Yaf\_Controller\_Abstract constructor
    -   [Yaf\_Controller\_Abstract::display](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::display)
        — The display purpose
    -   [Yaf\_Controller\_Abstract::forward](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::forward)
        — The forward purpose
    -   [Yaf\_Controller\_Abstract::getInvokeArg](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::getInvokeArg)
        — The getInvokeArg purpose
    -   [Yaf\_Controller\_Abstract::getInvokeArgs](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::getInvokeArgs)
        — The getInvokeArgs purpose
    -   [Yaf\_Controller\_Abstract::getModuleName](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::getModuleName)
        — 获取当前控制器所属的模块名
    -   [Yaf\_Controller\_Abstract::getName](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::getName)
        — Get self name
    -   [Yaf\_Controller\_Abstract::getRequest](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::getRequest)
        — The getRequest purpose
    -   [Yaf\_Controller\_Abstract::getResponse](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::getResponse)
        — The getResponse purpose
    -   [Yaf\_Controller\_Abstract::getView](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::getView)
        — 获取当前的视图引擎
    -   [Yaf\_Controller\_Abstract::getViewpath](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::getViewpath)
        — The getViewpath purpose
    -   [Yaf\_Controller\_Abstract::init](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::init)
        — 控制器初始化
    -   [Yaf\_Controller\_Abstract::initView](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::initView)
        — The initView purpose
    -   [Yaf\_Controller\_Abstract::redirect](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::redirect)
        — The redirect purpose
    -   [Yaf\_Controller\_Abstract::render](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::render)
        — 渲染视图模板
    -   [Yaf\_Controller\_Abstract::setViewpath](/class/yaf-controller-abstract.html#Yaf_Controller_Abstract::setViewpath)
        — The setViewpath purpose
-   [Yaf\_Action\_Abstract](/class/yaf-action-abstract.html) — The
    Yaf\_Action\_Abstract class
    -   [Yaf\_Action\_Abstract::execute](/class/yaf-action-abstract.html#Yaf_Action_Abstract::execute)
        — 执行动作
    -   [Yaf\_Action\_Abstract::getController](/class/yaf-action-abstract.html#Yaf_Action_Abstract::getController)
        — 得到控制器实例
    -   [Yaf\_Action\_Abstract::getControllerName](/class/yaf-action-abstract.html#Yaf_Action_Abstract::getControllerName)
        — Get controller name
-   [Yaf\_View\_Interface](/class/yaf-view-interface.html) — The
    Yaf\_View\_Interface class
    -   [Yaf\_View\_Interface::assign](/class/yaf-view-interface.html#Yaf_View_Interface::assign)
        — 为视图引擎分配一个模板变量
    -   [Yaf\_View\_Interface::display](/class/yaf-view-interface.html#Yaf_View_Interface::display)
        — 渲染一个视图模板, 并直接输出给请求端
    -   [Yaf\_View\_Interface::getScriptPath](/class/yaf-view-interface.html#Yaf_View_Interface::getScriptPath)
        — The getScriptPath purpose
    -   [Yaf\_View\_Interface::render](/class/yaf-view-interface.html#Yaf_View_Interface::render)
        — 渲染一个视图模板
    -   [Yaf\_View\_Interface::setScriptPath](/class/yaf-view-interface.html#Yaf_View_Interface::setScriptPath)
        — The setScriptPath purpose
-   [Yaf\_View\_Simple](/class/yaf-view-simple.html) — The
    Yaf\_View\_Simple Class
    -   [Yaf\_View\_Simple::assign](/class/yaf-view-simple.html#Yaf_View_Simple::assign)
        — 为视图引擎分配一个模板变量
    -   [Yaf\_View\_Simple::assignRef](/class/yaf-view-simple.html#Yaf_View_Simple::assignRef)
        — The assignRef purpose
    -   [Yaf\_View\_Simple::clear](/class/yaf-view-simple.html#Yaf_View_Simple::clear)
        — Clear Assigned values
    -   [Yaf\_View\_Simple::\_\_construct](/class/yaf-view-simple.html#Yaf_View_Simple::__construct)
        — Constructor of Yaf\_View\_Simple
    -   [Yaf\_View\_Simple::display](/class/yaf-view-simple.html#Yaf_View_Simple::display)
        — 渲染一个视图模板, 并直接输出给请求端
    -   [Yaf\_View\_Simple::eval](/class/yaf-view-simple.html#Yaf_View_Simple::eval)
        — 渲染模板
    -   [Yaf\_View\_Simple::\_\_get](/class/yaf-view-simple.html#Yaf_View_Simple::__get)
        — 获取视图引擎的一个模板变量值
    -   [Yaf\_View\_Simple::getScriptPath](/class/yaf-view-simple.html#Yaf_View_Simple::getScriptPath)
        — 获取模板目录
    -   [Yaf\_View\_Simple::\_\_isset](/class/yaf-view-simple.html#Yaf_View_Simple::__isset)
        — The \_\_isset purpose
    -   [Yaf\_View\_Simple::render](/class/yaf-view-simple.html#Yaf_View_Simple::render)
        — 渲染模板
    -   [Yaf\_View\_Simple::\_\_set](/class/yaf-view-simple.html#Yaf_View_Simple::__set)
        — 为视图引擎分配一个模板变量
    -   [Yaf\_View\_Simple::setScriptPath](/class/yaf-view-simple.html#Yaf_View_Simple::setScriptPath)
        — 设置模板的目录
-   [Yaf\_Loader](/class/yaf-loader.html) — The Yaf\_Loader class
    -   [Yaf\_Loader::autoload](/class/yaf-loader.html#Yaf_Loader::autoload)
        — The autoload purpose
    -   [Yaf\_Loader::clearLocalNamespace](/class/yaf-loader.html#Yaf_Loader::clearLocalNamespace)
        — The clearLocalNamespace purpose
    -   [Yaf\_Loader::\_\_construct](/class/yaf-loader.html#Yaf_Loader::__construct)
        — The \_\_construct purpose
    -   [Yaf\_Loader::getInstance](/class/yaf-loader.html#Yaf_Loader::getInstance)
        — The getInstance purpose
    -   [Yaf\_Loader::getLibraryPath](/class/yaf-loader.html#Yaf_Loader::getLibraryPath)
        — get the library path
    -   [Yaf\_Loader::getLocalNamespace](/class/yaf-loader.html#Yaf_Loader::getLocalNamespace)
        — The getLocalNamespace purpose
    -   [Yaf\_Loader::getNamespacePath](/class/yaf-loader.html#Yaf_Loader::getNamespacePath)
        — Retieve path of a registered namespace
    -   [Yaf\_Loader::getLocalNamespace](/class/yaf-loader.html#Yaf_Loader::getLocalNamespace)
        — Retrive all register namespaces info
    -   [Yaf\_Loader::import](/class/yaf-loader.html#Yaf_Loader::import)
        — The import purpose
    -   [Yaf\_Loader::isLocalName](/class/yaf-loader.html#Yaf_Loader::isLocalName)
        — The isLocalName purpose
    -   [Yaf\_Loader::registerLocalNamespace](/class/yaf-loader.html#Yaf_Loader::registerLocalNamespace)
        — 注册本地类前缀
    -   [Yaf\_Loader::registerNamespace](/class/yaf-loader.html#Yaf_Loader::registerNamespace)
        — Register namespace with searching path
    -   [Yaf\_Loader::setLibraryPath](/class/yaf-loader.html#Yaf_Loader::setLibraryPath)
        — 改变library路径
-   [Yaf\_Plugin\_Abstract](/class/yaf-plugin-abstract.html) — The
    Yaf\_Plugin\_Abstract class
    -   [Yaf\_Plugin\_Abstract::dispatchLoopShutdown](/class/yaf-plugin-abstract.html#Yaf_Plugin_Abstract::dispatchLoopShutdown)
        — The dispatchLoopShutdown purpose
    -   [Yaf\_Plugin\_Abstract::dispatchLoopStartup](/class/yaf-plugin-abstract.html#Yaf_Plugin_Abstract::dispatchLoopStartup)
        — The dispatchLoopStartup purpose
    -   [Yaf\_Plugin\_Abstract::postDispatch](/class/yaf-plugin-abstract.html#Yaf_Plugin_Abstract::postDispatch)
        — The postDispatch purpose
    -   [Yaf\_Plugin\_Abstract::preDispatch](/class/yaf-plugin-abstract.html#Yaf_Plugin_Abstract::preDispatch)
        — The preDispatch purpose
    -   [Yaf\_Plugin\_Abstract::preResponse](/class/yaf-plugin-abstract.html#Yaf_Plugin_Abstract::preResponse)
        — The preResponse purpose
    -   [Yaf\_Plugin\_Abstract::routerShutdown](/class/yaf-plugin-abstract.html#Yaf_Plugin_Abstract::routerShutdown)
        — The routerShutdown purpose
    -   [Yaf\_Plugin\_Abstract::routerStartup](/class/yaf-plugin-abstract.html#Yaf_Plugin_Abstract::routerStartup)
        — RouterStartup hook
-   [Yaf\_Registry](/class/yaf-registry.html) — The Yaf\_Registry class
    -   [Yaf\_Registry::\_\_construct](/class/yaf-registry.html#Yaf_Registry::__construct)
        — Yaf\_Registry implements singleton
    -   [Yaf\_Registry::del](/class/yaf-registry.html#Yaf_Registry::del)
        — Remove an item from registry
    -   [Yaf\_Registry::get](/class/yaf-registry.html#Yaf_Registry::get)
        — Retrieve an item from registry
    -   [Yaf\_Registry::has](/class/yaf-registry.html#Yaf_Registry::has)
        — Check whether an item exists
    -   [Yaf\_Registry::set](/class/yaf-registry.html#Yaf_Registry::set)
        — Add an item into registry
-   [Yaf\_Request\_Abstract](/class/yaf-request-abstract.html) — The
    Yaf\_Request\_Abstract class
    -   [Yaf\_Request\_Abstract::clearParams](/class/yaf-request-abstract.html#Yaf_Request_Abstract::clearParams)
        — Remove all params
    -   [Yaf\_Request\_Abstract::getActionName](/class/yaf-request-abstract.html#Yaf_Request_Abstract::getActionName)
        — The getActionName purpose
    -   [Yaf\_Request\_Abstract::getBaseUri](/class/yaf-request-abstract.html#Yaf_Request_Abstract::getBaseUri)
        — The getBaseUri purpose
    -   [Yaf\_Request\_Abstract::getControllerName](/class/yaf-request-abstract.html#Yaf_Request_Abstract::getControllerName)
        — The getControllerName purpose
    -   [Yaf\_Request\_Abstract::getEnv](/class/yaf-request-abstract.html#Yaf_Request_Abstract::getEnv)
        — 取得ENV变量的值
    -   [Yaf\_Request\_Abstract::getException](/class/yaf-request-abstract.html#Yaf_Request_Abstract::getException)
        — The getException purpose
    -   [Yaf\_Request\_Abstract::getLanguage](/class/yaf-request-abstract.html#Yaf_Request_Abstract::getLanguage)
        — The getLanguage purpose
    -   [Yaf\_Request\_Abstract::getMethod](/class/yaf-request-abstract.html#Yaf_Request_Abstract::getMethod)
        — The getMethod purpose
    -   [Yaf\_Request\_Abstract::getModuleName](/class/yaf-request-abstract.html#Yaf_Request_Abstract::getModuleName)
        — The getModuleName purpose
    -   [Yaf\_Request\_Abstract::getParam](/class/yaf-request-abstract.html#Yaf_Request_Abstract::getParam)
        — The getParam purpose
    -   [Yaf\_Request\_Abstract::getParams](/class/yaf-request-abstract.html#Yaf_Request_Abstract::getParams)
        — The getParams purpose
    -   [Yaf\_Request\_Abstract::getRequestUri](/class/yaf-request-abstract.html#Yaf_Request_Abstract::getRequestUri)
        — The getRequestUri purpose
    -   [Yaf\_Request\_Abstract::getServer](/class/yaf-request-abstract.html#Yaf_Request_Abstract::getServer)
        — 返回SERVER变量的值
    -   [Yaf\_Request\_Abstract::isCli](/class/yaf-request-abstract.html#Yaf_Request_Abstract::isCli)
        — The isCli purpose
    -   [Yaf\_Request\_Abstract::isDispatched](/class/yaf-request-abstract.html#Yaf_Request_Abstract::isDispatched)
        — The isDispatched purpose
    -   [Yaf\_Request\_Abstract::isGet](/class/yaf-request-abstract.html#Yaf_Request_Abstract::isGet)
        — The isGet purpose
    -   [Yaf\_Request\_Abstract::isHead](/class/yaf-request-abstract.html#Yaf_Request_Abstract::isHead)
        — The isHead purpose
    -   [Yaf\_Request\_Abstract::isOptions](/class/yaf-request-abstract.html#Yaf_Request_Abstract::isOptions)
        — The isOptions purpose
    -   [Yaf\_Request\_Abstract::isPost](/class/yaf-request-abstract.html#Yaf_Request_Abstract::isPost)
        — The isPost purpose
    -   [Yaf\_Request\_Abstract::isPut](/class/yaf-request-abstract.html#Yaf_Request_Abstract::isPut)
        — The isPut purpose
    -   [Yaf\_Request\_Abstract::isRouted](/class/yaf-request-abstract.html#Yaf_Request_Abstract::isRouted)
        — The isRouted purpose
    -   [Yaf\_Request\_Abstract::isXmlHttpRequest](/class/yaf-request-abstract.html#Yaf_Request_Abstract::isXmlHttpRequest)
        — The isXmlHttpRequest purpose
    -   [Yaf\_Request\_Abstract::setActionName](/class/yaf-request-abstract.html#Yaf_Request_Abstract::setActionName)
        — The setActionName purpose
    -   [Yaf\_Request\_Abstract::setBaseUri](/class/yaf-request-abstract.html#Yaf_Request_Abstract::setBaseUri)
        — The setBaseUri purpose
    -   [Yaf\_Request\_Abstract::setControllerName](/class/yaf-request-abstract.html#Yaf_Request_Abstract::setControllerName)
        — The setControllerName purpose
    -   [Yaf\_Request\_Abstract::setDispatched](/class/yaf-request-abstract.html#Yaf_Request_Abstract::setDispatched)
        — The setDispatched purpose
    -   [Yaf\_Request\_Abstract::setModuleName](/class/yaf-request-abstract.html#Yaf_Request_Abstract::setModuleName)
        — The setModuleName purpose
    -   [Yaf\_Request\_Abstract::setParam](/class/yaf-request-abstract.html#Yaf_Request_Abstract::setParam)
        — The setParam purpose
    -   [Yaf\_Request\_Abstract::setRequestUri](/class/yaf-request-abstract.html#Yaf_Request_Abstract::setRequestUri)
        — The setRequestUri purpose
    -   [Yaf\_Request\_Abstract::setRouted](/class/yaf-request-abstract.html#Yaf_Request_Abstract::setRouted)
        — The setRouted purpose
-   [Yaf\_Request\_Http](/class/yaf-request-http.html) — The
    Yaf\_Request\_Http class
    -   [Yaf\_Request\_Http::\_\_construct](/class/yaf-request-http.html#Yaf_Request_Http::__construct)
        — The \_\_construct purpose
    -   [Yaf\_Request\_Http::get](/class/yaf-request-http.html#Yaf_Request_Http::get)
        — 从客户端返回变量
    -   [Yaf\_Request\_Http::getCookie](/class/yaf-request-http.html#Yaf_Request_Http::getCookie)
        — 返回Cookie变量
    -   [Yaf\_Request\_Http::getFiles](/class/yaf-request-http.html#Yaf_Request_Http::getFiles)
        — The getFiles purpose
    -   [Yaf\_Request\_Http::getPost](/class/yaf-request-http.html#Yaf_Request_Http::getPost)
        — 返回POST变量
    -   [Yaf\_Request\_Http::getQuery](/class/yaf-request-http.html#Yaf_Request_Http::getQuery)
        — fetch a query parameter
    -   [Yaf\_Request\_Http::getRaw](/class/yaf-request-http.html#Yaf_Request_Http::getRaw)
        — Retrieve Raw request body
    -   [Yaf\_Request\_Http::getRequest](/class/yaf-request-http.html#Yaf_Request_Http::getRequest)
        — The getRequest purpose
    -   [Yaf\_Request\_Http::isXmlHttpRequest](/class/yaf-request-http.html#Yaf_Request_Http::isXmlHttpRequest)
        — 是否为Ajax请求
-   [Yaf\_Request\_Simple](/class/yaf-request-simple.html) — The
    Yaf\_Request\_Simple class
    -   [Yaf\_Request\_Simple::\_\_construct](/class/yaf-request-simple.html#Yaf_Request_Simple::__construct)
        — The \_\_construct purpose
    -   [Yaf\_Request\_Simple::get](/class/yaf-request-simple.html#Yaf_Request_Simple::get)
        — The get purpose
    -   [Yaf\_Request\_Simple::getCookie](/class/yaf-request-simple.html#Yaf_Request_Simple::getCookie)
        — The getCookie purpose
    -   [Yaf\_Request\_Simple::getFiles](/class/yaf-request-simple.html#Yaf_Request_Simple::getFiles)
        — The getFiles purpose
    -   [Yaf\_Request\_Simple::getPost](/class/yaf-request-simple.html#Yaf_Request_Simple::getPost)
        — The getPost purpose
    -   [Yaf\_Request\_Simple::getQuery](/class/yaf-request-simple.html#Yaf_Request_Simple::getQuery)
        — The getQuery purpose
    -   [Yaf\_Request\_Simple::getRequest](/class/yaf-request-simple.html#Yaf_Request_Simple::getRequest)
        — The getRequest purpose
    -   [Yaf\_Request\_Simple::isXmlHttpRequest](/class/yaf-request-simple.html#Yaf_Request_Simple::isXmlHttpRequest)
        — The isXmlHttpRequest purpose
-   [Yaf\_Response\_Abstract](/class/yaf-response-abstract.html) — The
    Yaf\_Response\_Abstract class
    -   [Yaf\_Response\_Abstract::appendBody](/class/yaf-response-abstract.html#Yaf_Response_Abstract::appendBody)
        — 往已有的响应body后附加新的内容
    -   [Yaf\_Response\_Abstract::clearBody](/class/yaf-response-abstract.html#Yaf_Response_Abstract::clearBody)
        — 清除已经设置的响应body
    -   [Yaf\_Response\_Abstract::clearHeaders](/class/yaf-response-abstract.html#Yaf_Response_Abstract::clearHeaders)
        — The clearHeaders purpose
    -   [Yaf\_Response\_Abstract::\_\_construct](/class/yaf-response-abstract.html#Yaf_Response_Abstract::__construct)
        — The \_\_construct purpose
    -   [Yaf\_Response\_Abstract::\_\_destruct](/class/yaf-response-abstract.html#Yaf_Response_Abstract::__destruct)
        — The \_\_destruct purpose
    -   [Yaf\_Response\_Abstract::getBody](/class/yaf-response-abstract.html#Yaf_Response_Abstract::getBody)
        — 获取已经设置的响应body
    -   [Yaf\_Response\_Abstract::getHeader](/class/yaf-response-abstract.html#Yaf_Response_Abstract::getHeader)
        — The getHeader purpose
    -   [Yaf\_Response\_Abstract::prependBody](/class/yaf-response-abstract.html#Yaf_Response_Abstract::prependBody)
        — The prependBody purpose
    -   [Yaf\_Response\_Abstract::response](/class/yaf-response-abstract.html#Yaf_Response_Abstract::response)
        — send response
    -   [Yaf\_Response\_Abstract::setAllHeaders](/class/yaf-response-abstract.html#Yaf_Response_Abstract::setAllHeaders)
        — The setAllHeaders purpose
    -   [Yaf\_Response\_Abstract::setBody](/class/yaf-response-abstract.html#Yaf_Response_Abstract::setBody)
        — 设置响应的Body
    -   [Yaf\_Response\_Abstract::setHeader](/class/yaf-response-abstract.html#Yaf_Response_Abstract::setHeader)
        — The setHeader purpose
    -   [Yaf\_Response\_Abstract::setRedirect](/class/yaf-response-abstract.html#Yaf_Response_Abstract::setRedirect)
        — The setRedirect purpose
    -   [Yaf\_Response\_Abstract::\_\_toString](/class/yaf-response-abstract.html#Yaf_Response_Abstract::__toString)
        — The \_\_toString purpose
-   [Yaf\_Route\_Interface](/class/yaf-route-interface.html) — The
    Yaf\_Route\_Interface class
    -   [Yaf\_Route\_Interface::assemble](/class/yaf-route-interface.html#Yaf_Route_Interface::assemble)
        — 将指定路由规则组合成一个url
    -   [Yaf\_Route\_Interface::route](/class/yaf-route-interface.html#Yaf_Route_Interface::route)
        — route a request
-   [Yaf\_Route\_Map](/class/yaf-route-map.html) — The Yaf\_Route\_Map
    class
    -   [Yaf\_Route\_Map::assemble](/class/yaf-route-map.html#Yaf_Route_Map::assemble)
        — 组合url
    -   [Yaf\_Route\_Map::\_\_construct](/class/yaf-route-map.html#Yaf_Route_Map::__construct)
        — The \_\_construct purpose
    -   [Yaf\_Route\_Map::route](/class/yaf-route-map.html#Yaf_Route_Map::route)
        — The route purpose
-   [Yaf\_Route\_Regex](/class/yaf-route-regex.html) — The
    Yaf\_Route\_Regex class
    -   [Yaf\_Route\_Regex::assemble](/class/yaf-route-regex.html#Yaf_Route_Regex::assemble)
        — 组合url
    -   [Yaf\_Route\_Regex::\_\_construct](/class/yaf-route-regex.html#Yaf_Route_Regex::__construct)
        — The \_\_construct purpose
    -   [Yaf\_Route\_Regex::route](/class/yaf-route-regex.html#Yaf_Route_Regex::route)
        — The route purpose
-   [Yaf\_Route\_Rewrite](/class/yaf-route-rewrite.html) — The
    Yaf\_Route\_Rewrite class
    -   [Yaf\_Route\_Rewrite::assemble](/class/yaf-route-rewrite.html#Yaf_Route_Rewrite::assemble)
        — 组合url
    -   [Yaf\_Route\_Rewrite::\_\_construct](/class/yaf-route-rewrite.html#Yaf_Route_Rewrite::__construct)
        — The \_\_construct purpose
    -   [Yaf\_Route\_Rewrite::route](/class/yaf-route-rewrite.html#Yaf_Route_Rewrite::route)
        — The route purpose
-   [Yaf\_Router](/class/yaf-router.html) — The Yaf\_Router class
    -   [Yaf\_Router::addConfig](/class/yaf-router.html#Yaf_Router::addConfig)
        — 向Router中添加配置文件中定义的路由
    -   [Yaf\_Router::addRoute](/class/yaf-router.html#Yaf_Router::addRoute)
        — 往Router中添加新的路由
    -   [Yaf\_Router::\_\_construct](/class/yaf-router.html#Yaf_Router::__construct)
        — Yaf\_Router constructor
    -   [Yaf\_Router::getCurrentRoute](/class/yaf-router.html#Yaf_Router::getCurrentRoute)
        — 取得当前有效的路由名
    -   [Yaf\_Router::getRoute](/class/yaf-router.html#Yaf_Router::getRoute)
        — The getRoute purpose
    -   [Yaf\_Router::getRoutes](/class/yaf-router.html#Yaf_Router::getRoutes)
        — The getRoutes purpose
    -   [Yaf\_Router::route](/class/yaf-router.html#Yaf_Router::route) —
        The route purpose
-   [Yaf\_Route\_Simple](/class/yaf-route-simple.html) — The
    Yaf\_Route\_Simple class
    -   [Yaf\_Route\_Simple::assemble](/class/yaf-route-simple.html#Yaf_Route_Simple::assemble)
        — 组合url
    -   [Yaf\_Route\_Simple::\_\_construct](/class/yaf-route-simple.html#Yaf_Route_Simple::__construct)
        — Yaf\_Route\_Simple constructor
    -   [Yaf\_Route\_Simple::route](/class/yaf-route-simple.html#Yaf_Route_Simple::route)
        — Route a request
-   [Yaf\_Route\_Static](/class/yaf-route-static.html) — The
    Yaf\_Route\_Static class
    -   [Yaf\_Route\_Static::assemble](/class/yaf-route-static.html#Yaf_Route_Static::assemble)
        — 组合url
    -   [Yaf\_Route\_Static::match](/class/yaf-route-static.html#Yaf_Route_Static::match)
        — The match purpose
    -   [Yaf\_Route\_Static::route](/class/yaf-route-static.html#Yaf_Route_Static::route)
        — Route a request
-   [Yaf\_Route\_Supervar](/class/yaf-route-supervar.html) — The
    Yaf\_Route\_Supervar class
    -   [Yaf\_Route\_Supervar::assemble](/class/yaf-route-supervar.html#Yaf_Route_Supervar::assemble)
        — 组合url
    -   [Yaf\_Route\_Supervar::\_\_construct](/class/yaf-route-supervar.html#Yaf_Route_Supervar::__construct)
        — The \_\_construct purpose
    -   [Yaf\_Route\_Supervar::route](/class/yaf-route-supervar.html#Yaf_Route_Supervar::route)
        — The route purpose
-   [Yaf\_Session](/class/yaf-session.html) — The Yaf\_Session class
    -   [Yaf\_Session::\_\_construct](/class/yaf-session.html#Yaf_Session::__construct)
        — The \_\_construct purpose
    -   [Yaf\_Session::count](/class/yaf-session.html#Yaf_Session::count)
        — The count purpose
    -   [Yaf\_Session::current](/class/yaf-session.html#Yaf_Session::current)
        — The current purpose
    -   [Yaf\_Session::del](/class/yaf-session.html#Yaf_Session::del) —
        The del purpose
    -   [Yaf\_Session::\_\_get](/class/yaf-session.html#Yaf_Session::__get)
        — The \_\_get purpose
    -   [Yaf\_Session::getInstance](/class/yaf-session.html#Yaf_Session::getInstance)
        — The getInstance purpose
    -   [Yaf\_Session::has](/class/yaf-session.html#Yaf_Session::has) —
        The has purpose
    -   [Yaf\_Session::\_\_isset](/class/yaf-session.html#Yaf_Session::__isset)
        — The \_\_isset purpose
    -   [Yaf\_Session::key](/class/yaf-session.html#Yaf_Session::key) —
        The key purpose
    -   [Yaf\_Session::next](/class/yaf-session.html#Yaf_Session::next)
        — The next purpose
    -   [Yaf\_Session::offsetExists](/class/yaf-session.html#Yaf_Session::offsetExists)
        — The offsetExists purpose
    -   [Yaf\_Session::offsetGet](/class/yaf-session.html#Yaf_Session::offsetGet)
        — The offsetGet purpose
    -   [Yaf\_Session::offsetSet](/class/yaf-session.html#Yaf_Session::offsetSet)
        — The offsetSet purpose
    -   [Yaf\_Session::offsetUnset](/class/yaf-session.html#Yaf_Session::offsetUnset)
        — The offsetUnset purpose
    -   [Yaf\_Session::rewind](/class/yaf-session.html#Yaf_Session::rewind)
        — The rewind purpose
    -   [Yaf\_Session::\_\_set](/class/yaf-session.html#Yaf_Session::__set)
        — The \_\_set purpose
    -   [Yaf\_Session::start](/class/yaf-session.html#Yaf_Session::start)
        — The start purpose
    -   [Yaf\_Session::\_\_unset](/class/yaf-session.html#Yaf_Session::__unset)
        — The \_\_unset purpose
    -   [Yaf\_Session::valid](/class/yaf-session.html#Yaf_Session::valid)
        — The valid purpose
-   [Yaf\_Exception](/class/yaf-exception.html) — The Yaf\_Exception
    class
    -   [Yaf\_Exception::\_\_construct](/class/yaf-exception.html#Yaf_Exception::__construct)
        — The \_\_construct purpose
    -   [Yaf\_Exception::getPrevious](/class/yaf-exception.html#Yaf_Exception::getPrevious)
        — The getPrevious purpose
-   [Yaf\_Exception\_TypeError](/class/yaf-exception-typeerror.html) —
    The Yaf\_Exception\_TypeError class
-   [Yaf\_Exception\_StartupError](/class/yaf-exception-startuperror.html)
    — The Yaf\_Exception\_StartupError class
-   [Yaf\_Exception\_DispatchFailed](/class/yaf-exception-dispatchfailed.html)
    — The Yaf\_Exception\_DispatchFailed class
-   [Yaf\_Exception\_RouterFailed](/class/yaf-exception-routerfailed.html)
    — The Yaf\_Exception\_RouterFailed class
-   [Yaf\_Exception\_LoadFailed](/class/yaf-exception-loadfailed.html) —
    The Yaf\_Exception\_LoadFailed class
-   [Yaf\_Exception\_LoadFailed\_Module](/class/yaf-exception-loadfailed-module.html)
    — The Yaf\_Exception\_LoadFailed\_Module class
-   [Yaf\_Exception\_LoadFailed\_Controller](/class/yaf-exception-loadfailed-controller.html)
    — The Yaf\_Exception\_LoadFailed\_Controller class
-   [Yaf\_Exception\_LoadFailed\_Action](/class/yaf-exception-loadfailed-action.html)
    — The Yaf\_Exception\_LoadFailed\_Action class
-   [Yaf\_Exception\_LoadFailed\_View](/class/yaf-exception-loadfailed-view.html)
    — The Yaf\_Exception\_LoadFailed\_View class

简介
----

<span
class="classname">Yaf\_Application</span>为应用提供了一个辅助设施。
它提供了可重用的资源，常见的和模块化的引导类，还有依赖的检查。

> **Note**:
>
> <span class="classname">Yaf\_Application</span>实现了单例模式。 <span
> class="classname">Yaf\_Application</span>不能够被序列化和反序列化，
> 因为当你尝试使用PHPUnit来为Yaf写一些测试用例的时候会造成一些不必要的麻烦。
>
> 你可以使用PHPUnit的@backupGlobals注释来控制全局变量的备份和恢复操作，
> 从而可以解决这个问题。

类摘要
------

**Yaf\_Application**

<span class="ooclass"> <span class="modifier">final</span> class
**Yaf\_Application** </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$config` ;

<span class="modifier">protected</span> `$dispatcher` ;

<span class="modifier">protected</span> <span
class="modifier">static</span> `$_app` ;

<span class="modifier">protected</span> `$_modules` ;

<span class="modifier">protected</span> `$_running` ;

<span class="modifier">protected</span> `$_environ` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">app</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">bootstrap</span> (\[ <span
class="methodparam"><span class="type">Yaf\_Bootstrap\_Abstract</span>
`$bootstrap`</span> \] )

<span class="modifier">public</span> <span
class="type">Yaf\_Application</span> <span
class="methodname">clearLastError</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$config`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$envrion`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">environ</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">execute</span> ( <span
class="methodparam"><span class="type">callable</span> `$entry`</span> ,
<span class="methodparam"><span class="type">string</span> `$...`</span>
)

<span class="modifier">public</span> <span
class="type">Yaf\_Application</span> <span
class="methodname">getAppDirectory</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Config\_Abstract</span> <span
class="methodname">getConfig</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">getDispatcher</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getLastErrorMsg</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getLastErrorNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getModules</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">run</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Application</span> <span
class="methodname">setAppDirectory</span> ( <span
class="methodparam"><span class="type">string</span> `$directory`</span>
)

}

属性
----

`config`  

`dispatcher`  

`_app`  

`_modules`  

`_running`  

`_environ`  

Yaf\_Application::app
=====================

获取当前的<span class="classname">Yaf\_Application</span>实例

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Yaf\_Application::app</span> ( <span
class="methodparam">void</span> )

返回<span class="classname">Yaf\_Application</span>的实例， 也可以使用
<span
class="methodname">Yaf\_Dispatcher::getApplication</span>来得到<span
class="classname">Yaf\_Application</span>的实例 <span
class="methodname">Yaf\_Dispatcher::getApplication</span>.

### 参数

此函数没有参数。

### 返回值

返回值为一个<span class="classname">Yaf\_Application</span>的实例，
如果在调用之前没有初始化一个<span
class="classname">Yaf\_Application</span>实例的话，它将返回NULL

### 参见

-   <span class="methodname">Yaf\_Dispatcher::getApplication</span>

Yaf\_Application::bootstrap
===========================

调用bootstrap

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Application::bootstrap</span> (\[ <span
class="methodparam"><span class="type">Yaf\_Bootstrap\_Abstract</span>
`$bootstrap`</span> \] )

指示Yaf\_Application去寻找Bootstrap，并按照声明的顺序，执行所有在Bootstrap类中定义的以\_init开头的方法。
如果没有提供变量bootstrap，Yaf默认会去application.directory中寻找Bootstrap。

### 参数

`bootstrap`  
A <span class="classname">Yaf\_Bootstrap\_Abstract</span> instance

### 返回值

<span class="classname">Yaf\_Application</span> instance

### 范例

**示例 \#1 <span class="function">A Bootstrap</span>example**

``` php
<?php
/**
 * This file should be under the APPLICATION_PATH . "/application/"(which was defined in the config passed to Yaf_Application).
 * and named Bootstrap.php,  so the Yaf_Application can find it 
 */
class Bootstrap extends Yaf_Bootstrap_Abstract {
    function _initConfig(Yaf_Dispatcher $dispatcher) {
        echo "1st called\n";
    }

    function _initPlugin($dispatcher) {
        echo "2nd called\n";
    }
}
?>
```

**示例 \#2 <span
class="function">Yaf\_Application::bootstrap</span>example**

``` php
<?php

defined('APPLICATION_PATH')                  // APPLICATION_PATH will be used in the ini config file
    || define('APPLICATION_PATH', __DIR__)); //__DIR__ was introduced after PHP 5.3

$application = new Yaf_Application(APPLICATION_PATH.'/conf/application.ini');
$application->bootstrap();
?>
```

以上例程的输出类似于：

    1st called
    2nd called

### 参见

-   <span class="classname">Yaf\_Bootstrap\_Abstract</span>

Yaf\_Application::clearLastError
================================

清除最后的错误信息

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Application</span> <span
class="methodname">Yaf\_Application::clearLastError</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Application::clearLastError</span>example**

``` php
<?php
function error_handler($errno, $errstr, $errfile, $errline) {
   Yaf_Application::app()->clearLastError();
   var_dump(Yaf_Application::app()->getLastErrorNo());
}
 
$config = array(                   
 "application" => array(
   "directory" => "/tmp/notexists",
     "dispatcher" => array(
       "throwException" => 0, //trigger error instead of throw exception when error occure
      ),
  ),
);
  
$app = new Yaf_Application($config);
$app->getDispatcher()->setErrorHandler("error_handler", E_RECOVERABLE_ERROR);
$app->run();
?>
```

以上例程的输出类似于：

    int(0)

Yaf\_Application::\_\_construct
===============================

Yaf\_Application的构造函数

### 说明

<span class="modifier">public</span> <span
class="methodname">Yaf\_Application::\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$config`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$envrion`</span> \] )

初始化一个 <span class="classname">Yaf\_Application</span>.

### 参数

`config`  
关联数组的配置, 或者一个指向ini格式的配置文件的路径的字符串。

如果是一个ini配置文件，那配置文件中应该有一个定义了<a href="/yaf/setup.html#" class="link">yaf.environ</a>
的配置节。这个在生产环境中是默认的。

> **Note**:
>
> 如果你使用了ini配置文件作为你应用配置的容器，你需要打开<a href="/yaf/setup.html#" class="link">yaf.cache_config</a>
> 来提升性能。

And the config entry(and there default value) list blow:

**示例 \#1 A ini config file example**

``` ini
[product]
;this one should alway be defined, and have no default value
application.directory=APPLICATION_PATH

;following configs have default value, you may no need to define them
application.library = APPLICATION_PATH . "/library"
application.dispatcher.throwException=1
application.dispatcher.catchException=1

application.baseUri=""

;the php script ext name
ap.ext=php

;the view template ext name
ap.view.ext=phtml

ap.dispatcher.defaultModuel=Index
ap.dispatcher.defaultController=Index
ap.dispatcher.defaultAction=index

;defined modules
ap.modules=Index
```

`envrion`  
Which section will be loaded as the final config

### 返回值

### 范例

**示例 \#2 <span
class="function">Yaf\_Application::\_\_construct</span>example**

``` php
<?php
defined('APPLICATION_PATH')                  // APPLICATION_PATH will be used in the ini config file
    || define('APPLICATION_PATH', __DIR__)); //__DIR__ was introduced after PHP 5.3

$application = new Yaf_Application(APPLICATION_PATH.'/conf/application.ini');
$application->bootstrap()->run();
?>
```

以上例程的输出类似于：

**示例 \#3 <span
class="function">Yaf\_Application::\_\_construct</span>example**

``` php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
$application->bootstrap()->run();
?>
```

以上例程的输出类似于：

### 参见

-   <span class="classname">Yaf\_Config\_Ini</span>

Yaf\_Application::\_\_destruct
==============================

析构函数

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Application::\_\_destruct</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Yaf\_Application::environ
=========================

获取当前Yaf\_Application的环境名

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Application::environ</span> ( <span
class="methodparam">void</span> )

返回当前Yaf\_Application的环境名，它被定义在yaf.environ，默认值为"product"。

### 参数

此函数没有参数。

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Application::environ</span>example**

``` php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
print_r($application->environ());
?>
```

以上例程的输出类似于：

    product

Yaf\_Application::execute
=========================

运行回调函数

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Application::execute</span> ( <span
class="methodparam"><span class="type">callable</span> `$entry`</span> ,
<span class="methodparam"><span class="type">string</span> `$...`</span>
)

这个方法通常用于在cron任务中运行Yaf\_Application。
在cron任务中也可以使用autoloader和Bootstrap机制。

### 参数

`entry`  
一个有效的回调函数

`...`  
零个或者多个要传递给函数的参数。

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Application::execute</span>example**

``` php
<?php
function main($argc, $argv) {
}

$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
$application->execute("main", $argc,  $argv);
?>
```

以上例程的输出类似于：

Yaf\_Application::getAppDirectory
=================================

获取应用的目录

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Application</span> <span
class="methodname">Yaf\_Application::getAppDirectory</span> ( <span
class="methodparam">void</span> )

### 参数

`directory`  

### 返回值

Yaf\_Application::getConfig
===========================

获取 Yaf\_Config\_Abstract 的实例

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Config\_Abstract</span> <span
class="methodname">Yaf\_Application::getConfig</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

<span class="classname">Yaf\_Config\_Abstract</span> 的实例

### 范例

**示例 \#1 <span
class="function">Yaf\_Application::getConfig</span>example**

``` php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
print_r($application->getConfig());
?>
```

以上例程的输出类似于：

    Yaf_Config_Simple Object
    (
        [_config:protected] => Array
            (
                [application] => Array
                    (
                        [directory] => /home/laruence/local/www/htdocs/application
                    )

            )

        [_readonly:protected] => 1
    )

Yaf\_Application::getDispatcher
===============================

获取 Yaf\_Dispatcher 的实例

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Application::getDispatcher</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Application::getDispatcher</span>example**

``` php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
print_r($application->getDispatcher());
?>
```

以上例程的输出类似于：

    Yaf_Dispatcher Object
    (
        [_router:protected] => Yaf_Router Object
            (
                [_routes:protected] => Array
                    (
                        [_default] => Yaf_Route_Static Object
                            (
                            )

                    )

                [_current:protected] => 
            )

        [_view:protected] => 
        [_request:protected] => Yaf_Request_Http Object
            (
                [module] => 
                [controller] => 
                [action] => 
                [method] => Cli
                [params:protected] => Array
                    (
                    )

                [language:protected] => 
                [_exception:protected] => 
                [_base_uri:protected] => 
                [uri:protected] => 
                [dispatched:protected] => 
                [routed:protected] => 
            )

        [_plugins:protected] => Array
            (
            )

        [_auto_render:protected] => 1
        [_return_response:protected] => 
        [_instantly_flush:protected] => 
        [_default_module:protected] => Index
        [_default_controller:protected] => Index
        [_default_action:protected] => index
        [_response] => Yaf_Response_Cli Object
            (
                [_header:protected] => Array
                    (
                    )

                [_body:protected] => 
                [_sendheader:protected] => 
            )

    )

Yaf\_Application::getLastErrorMsg
=================================

获取最近产生的错误的错误信息

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Application::getLastErrorMsg</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Application::getLastErrorMsg</span>example**

``` php
<?php
function error_handler($errno, $errstr, $errfile, $errline) {
   var_dump(Yaf_Application::app()->getLastErrorMsg());
}

$config = array(                   
 "application" => array(
   "directory" => "/tmp/notexists",
     "dispatcher" => array(
       "throwException" => 0, //trigger error instead of throw exception when error occure
      ),
  ),
);

$app = new Yaf_Application($config);
$app->getDispatcher()->setErrorHandler("error_handler", E_RECOVERABLE_ERROR);
$app->run();
?>
```

以上例程的输出类似于：

    string(69) "Could not find controller script /tmp/notexists/controllers/Index.php"

Yaf\_Application::getLastErrorNo
================================

获取最后产生的错误的错误代码

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Yaf\_Application::getLastErrorNo</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Application::getLastErrorNo</span>example**

``` php
<?php
function error_handler($errno, $errstr, $errfile, $errline) {
   var_dump(Yaf_Application::app()->getLastErrorNo());
   var_dump(Yaf_Application::app()->getLastErrorNo() == YAF_ERR_NOTFOUND_CONTROLLER);
}

$config = array(
  "application" => array(
   "directory" => "/tmp/notexists",
     "dispatcher" => array(
       "throwException" => 0, //trigger error instead of throw exception when error occure
      ),
  ),
);

$app = new Yaf_Application($config);
$app->getDispatcher()->setErrorHandler("error_handler", E_RECOVERABLE_ERROR);
$app->run();
?>
```

以上例程的输出类似于：

    int(516)
    bool(true)

Yaf\_Application::getModules
============================

获取在配置文件中申明的模块

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Yaf\_Application::getModules</span> ( <span
class="methodparam">void</span> )

获取在配置文件中声明的模块，如果没有声明，它的默认值将是"Index"。

### 参数

此函数没有参数。

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Application::getModules</span>example**

``` php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
print_r($application->getModules());
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => Index
    )

Yaf\_Application::run
=====================

运行 Yaf\_Application

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Application::run</span> ( <span
class="methodparam">void</span> )

运行一个Yaf\_Application，开始接受并处理请求，分发路由，做出相应的响应。最终将响应返回给客户端。

### 参数

此函数没有参数。

### 返回值

Yaf\_Application::setAppDirectory
=================================

改变应用目录

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Application</span> <span
class="methodname">Yaf\_Application::setAppDirectory</span> ( <span
class="methodparam"><span class="type">string</span> `$directory`</span>
)

### 参数

`directory`  

### 返回值

简介
----

Bootstrap是用来在Application运行(run)之前做一些初始化工作的机制.

你可以通过继承<span class="classname">Yaf\_Bootstrap\_Abstract</span>
来定义自己的Bootstrap类.

在Bootstrap类中所有以"\_init"开头的公有的方法, 都会被按照定义顺序依次在
<span class="methodname">Yaf\_Application::bootstrap</span>
被调用的时刻调用.

范例
----

**示例 \#1 Bootstrap example**

``` php
<?php
   /* bootstrap class should be defined under ./application/Bootstrap.php */
   class Bootstrap extends Yaf_Bootstrap_Abstract {
        public function _initConfig(Yaf_Dispatcher $dispatcher) {
            var_dump(__METHOD__);
        }
        public function _initPlugin(Yaf_Dispatcher $dispatcher) {
            var_dump(__METHOD__);
        }
   }

   $config = array(
       "application" => array(
           "directory" => dirname(__FILE__) . "/application/",
       ),
   );
 
   $app = new Yaf_Application($config);
   $app->bootstrap();
?>
```

以上例程的输出类似于：

    string(22) "Bootstrap::_initConfig"
    string(22) "Bootstrap::_initPlugin"

类摘要
------

**Yaf\_Bootstrap\_Abstract**

<span class="ooclass"> <span class="modifier">abstract</span> class
**Yaf\_Bootstrap\_Abstract** </span> {

/\* 属性 \*/

/\* 方法 \*/

}

简介
----

<span
class="classname">Yaf\_Dispatcher</span>用于初始化处理请求的运行环境,
它协调路由来的请求, 并分发和执行发现的动作, 然后收集动作产生的响应,
输出响应给请求者, 并在整个过程完成以后返回响应.

<span class="classname">Yaf\_Dispatcher</span>是单例模式运行的,
也就是说自始至终只生成一个<span
class="classname">Yaf\_Dispatcher</span>实例, 因此,
可以把它看成是在分发过程中生成的对象的注册表,
可以从中获取到分发过程中产生的对象.

类摘要
------

**Yaf\_Dispatcher**

<span class="ooclass"> <span class="modifier">final</span> class
**Yaf\_Dispatcher** </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_router` ;

<span class="modifier">protected</span> `$_view` ;

<span class="modifier">protected</span> `$_request` ;

<span class="modifier">protected</span> `$_plugins` ;

<span class="modifier">protected</span> <span
class="modifier">static</span> `$_instance` ;

<span class="modifier">protected</span> `$_auto_render` ;

<span class="modifier">protected</span> `$_return_response` ;

<span class="modifier">protected</span> `$_instantly_flush` ;

<span class="modifier">protected</span> `$_default_module` ;

<span class="modifier">protected</span> `$_default_controller` ;

<span class="modifier">protected</span> `$_default_action` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">autoRender</span> ( <span class="methodparam"><span
class="type">bool</span> `$flag`</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">catchException</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$flag`</span> \] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">disableView</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Response\_Abstract</span> <span
class="methodname">dispatch</span> ( <span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">enableView</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">flushInstantly</span> ( <span
class="methodparam"><span class="type">bool</span> `$flag`</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Application</span> <span
class="methodname">getApplication</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getDefaultAction</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getDefaultController</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getDefaultModule</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Yaf\_Dispatcher</span>
<span class="methodname">getInstance</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Request\_Abstract</span> <span
class="methodname">getRequest</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Router</span> <span
class="methodname">getRouter</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_View\_Interface</span> <span
class="methodname">initView</span> ( <span class="methodparam"><span
class="type">string</span> `$templates_dir`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span> \]
)

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">registerPlugin</span> ( <span
class="methodparam"><span class="type">Yaf\_Plugin\_Abstract</span>
`$plugin`</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">returnResponse</span> ( <span
class="methodparam"><span class="type">bool</span> `$flag`</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">setDefaultAction</span> ( <span
class="methodparam"><span class="type">string</span> `$action`</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">setDefaultController</span> ( <span
class="methodparam"><span class="type">string</span>
`$controller`</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">setDefaultModule</span> ( <span
class="methodparam"><span class="type">string</span> `$module`</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">setErrorHandler</span> ( <span
class="methodparam"><span class="type">call</span> `$callback`</span> ,
<span class="methodparam"><span class="type">int</span>
`$error_types`</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">setRequest</span> ( <span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">setView</span> ( <span class="methodparam"><span
class="type">Yaf\_View\_Interface</span> `$view`</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">throwException</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$flag`</span> \] )

}

属性
----

`_router`  

`_view`  

`_request`  

`_plugins`  

`_instance`  

`_auto_render`  

`_return_response`  

`_instantly_flush`  

`_default_module`  

`_default_controller`  

`_default_action`  

Yaf\_Dispatcher::autoRender
===========================

开启/关闭自动渲染功能

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Dispatcher::autoRender</span> ( <span
class="methodparam"><span class="type">bool</span> `$flag`</span> )

在开启的情况下(Yaf默认开启)，action执行完成以后，<span
class="classname">Yaf\_Dispatcher</span>
会自动调用view引擎去渲染该action对应的视图模板。
你也可以通过调用这个函数并将 `flag` 参数的值设为TRUE来人工干预它。

> **Note**:
>
> 你可以在一个action中仅仅返回FALSE来阻止当前action对应视图的自动渲染

### 参数

`flag`  
bool

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Dispatcher::autoRender</span>example**

``` php
<?php
class IndexController extends Yaf_Controller_Abstract {
     /* init method will be called as soon as a controller is initialized */ 
     public function init() {
         if ($this->getRequest()->isXmlHttpRequest()) {
             //do not call render for ajax request
             //we will outpu a json string
             Yaf_Dispatcher::getInstance()->autoRender(FALSE);
         }
     } 

}
?>
```

以上例程的输出类似于：

Yaf\_Dispatcher::catchException
===============================

开启/关闭自动异常捕获功能

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Dispatcher::catchException</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$flag`</span> \] )

当 application.dispatcher.throwException 开启的时候（你也可以通过调用
<span class="methodname">Yaf\_Dispatcher::throwException(TRUE)</span>
来开启它），Yaf将会抛出异常而不是触发异常发生。

如果开启了 <span
class="methodname">Yaf\_Dispatcher::catchException</span>
（可以通过设置<a href="/yaf/appconfig.html#" class="link">application.dispatcher.catchException</a>来开启），并且在你定义了异常处理的controller的情况下，Yaf会将所有未捕获的异常交给Error
Controller的Error Action来处理。

### 参数

`flag`  
bool

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Dispatcher::catchException</span>example**

``` php
/* if you defined a ErrorController like following */
<?php
class ErrorController extends Yaf_Controller_Abstract {
     /** 
      * you can also call to Yaf_Request_Abstract::getException to get the 
      * un-caught exception.
      */
     public function error($exception) {
        /* error occurs */
        switch ($exception->getCode()) {
            case YAF_ERR_NOTFOUND_MODULE:
            case YAF_ERR_NOTFOUND_CONTROLLER:
            case YAF_ERR_NOTFOUND_ACTION:
            case YAF_ERR_NOTFOUND_VIEW:
                echo 404, ":", $exception->getMessage();
                break;
            default :
                $message = $exception->getMessage();
                echo 0, ":", $exception->getMessage();
                break;
        }
     } 
}
?>
```

以上例程的输出类似于：

    /* now if some error occur, assuming access a non-exists controller(or you can throw a exception yourself): */
    404:Could not find controller script **/application/controllers/No-exists-controller.php

### 参见

-   <span class="methodname">Yaf\_Dispatcher::throwException</span>
-   <span class="methodname">Yaf\_Dispatcher::setErrorHandler</span>

Yaf\_Dispatcher::\_\_construct
==============================

Yaf\_Dispatcher 构造函数

### 说明

<span class="modifier">public</span> <span
class="methodname">Yaf\_Dispatcher::\_\_construct</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Yaf\_Dispatcher::disableView
============================

关闭自动渲染

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Dispatcher::disableView</span> ( <span
class="methodparam">void</span> )

在一些用户自己会输出信息的情况下使用。

> **Note**:
>
> 你可以在一个action中仅仅返回FALSE来阻止当前action对应视图的自动渲染

### 参数

此函数没有参数。

### 返回值

Yaf\_Dispatcher::dispatch
=========================

分发请求

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Response\_Abstract</span> <span
class="methodname">Yaf\_Dispatcher::dispatch</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> )

<span class="classname">Yaf\_Dispatcher</span>
的这个方法做的工作很繁重.它需要一个request对象。

分发过程有三个不同的事件：

-   路由
-   分发
-   响应

The dispatch process has three distinct events:

-   Routing
-   Dispatching
-   Response

路由只发生一次，当dispatch()被调用的时候，需要使用请求对象中的值。分发发生在一个循环中；一个请求可能会分发出多个action，
或者controller或者一个plugin可能重置请求对象来强制分发其他的action（参见
<span class="classname">Yaf\_Plugin\_Abstract</span>）。
当所有都执行完毕，<span class="classname">Yaf\_Dispatcher</span>
会返回一个响应。

### 参数

`request`  

### 返回值

Yaf\_Dispatcher::enableView
===========================

开启自动渲染

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Dispatcher::enableView</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Yaf\_Dispatcher::flushInstantly
===============================

打开关闭自动响应

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Dispatcher::flushInstantly</span> ( <span
class="methodparam"><span class="type">bool</span> `$flag`</span> )

### 参数

`flag`  

### 返回值

Yaf\_Dispatcher::getApplication
===============================

获取当前的Yaf\_Application实例

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Application</span> <span
class="methodname">Yaf\_Dispatcher::getApplication</span> ( <span
class="methodparam">void</span> )

Retrive the <span class="classname">Yaf\_Application</span> instance.
same as <span class="methodname">Yaf\_Application::app</span>.
获取当前的Yaf\_Application实例。跟 <span
class="methodname">Yaf\_Application::app</span> 相同。

### 参数

此函数没有参数。

### 返回值

### 参见

-   <span class="methodname">Yaf\_Application::app</span>

Yaf\_Dispatcher::getDefaultAction
=================================

Retrive the default action name

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Dispatcher::getDefaultAction</span> (
<span class="methodparam">void</span> )

get the default action name

### 参数

此函数没有参数。

### 返回值

<span class="type">string</span>, default action name, default is
"index"

Yaf\_Dispatcher::getDefaultController
=====================================

Retrive the default controller name

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Dispatcher::getDefaultController</span> (
<span class="methodparam">void</span> )

get the default controller name

### 参数

此函数没有参数。

### 返回值

<span class="type">string</span>, default controller name, default is
"Index"

Yaf\_Dispatcher::getDefaultModule
=================================

Retrive the default module name

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Dispatcher::getDefaultModule</span> (
<span class="methodparam">void</span> )

get the default module name

### 参数

此函数没有参数。

### 返回值

<span class="type">string</span>, module name, default is "Index"

Yaf\_Dispatcher::getInstance
============================

获取当前的Yaf\_Dispatcher实例

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Yaf\_Dispatcher</span>
<span class="methodname">Yaf\_Dispatcher::getInstance</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Yaf\_Dispatcher::getRequest
===========================

获取当前的请求实例

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Request\_Abstract</span> <span
class="methodname">Yaf\_Dispatcher::getRequest</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Yaf\_Dispatcher::getRouter
==========================

获取路由器

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Router</span> <span
class="methodname">Yaf\_Dispatcher::getRouter</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Yaf\_Dispatcher::initView
=========================

初始化视图引擎并返回它

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_View\_Interface</span> <span
class="methodname">Yaf\_Dispatcher::initView</span> ( <span
class="methodparam"><span class="type">string</span>
`$templates_dir`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`</span> \] )

### 参数

`templates_dir`  

`options`  

### 返回值

Yaf\_Dispatcher::registerPlugin
===============================

注册一个插件

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Dispatcher::registerPlugin</span> ( <span
class="methodparam"><span class="type">Yaf\_Plugin\_Abstract</span>
`$plugin`</span> )

<span class="classname">Yaf\_Bootstrap\_Abstract</span>).
注册一个插件（参见 <span
class="classname">Yaf\_Plugin\_Abstract</span>）。

### 参数

`plugin`  

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Dispatcher::registerPlugin</span>example**

``` php
<?php
class Bootstrap extends Yaf_Bootstrap_Abstract {
  public function _initPlugin(Yaf_Dispatcher $dispatcher) {
    /**
    * Yaf assumes plugin scripts under [application.directory] .  "/plugins" 
    * for this case, it will be:
    * [application.directory] . "/plugins/" . "User" . [application.ext]
    */ 
    $user = new UserPlugin();
    $dispatcher->registerPlugin($user);
  }
}
?>
```

### 参见

-   <span class="classname">Yaf\_Plugin\_Abstract</span>

<!-- -->

-   <span class="classname">Yaf\_Bootstrap\_Abstract</span>

Yaf\_Dispatcher::returnResponse
===============================

The returnResponse purpose

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Dispatcher::returnResponse</span> ( <span
class="methodparam"><span class="type">bool</span> `$flag`</span> )

### 参数

`flag`  

### 返回值

Yaf\_Dispatcher::setDefaultAction
=================================

设置路由的默认动作

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Dispatcher::setDefaultAction</span> ( <span
class="methodparam"><span class="type">string</span> `$action`</span> )

### 参数

`action`  

### 返回值

Yaf\_Dispatcher::setDefaultController
=====================================

设置路由的默认控制器

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Dispatcher::setDefaultController</span> ( <span
class="methodparam"><span class="type">string</span>
`$controller`</span> )

### 参数

`controller`  

### 返回值

Yaf\_Dispatcher::setDefaultModule
=================================

设置路由的默认模块

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Dispatcher::setDefaultModule</span> ( <span
class="methodparam"><span class="type">string</span> `$module`</span> )

### 参数

`module`  

### 返回值

Yaf\_Dispatcher::setErrorHandler
================================

设置错误处理函数

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Dispatcher::setErrorHandler</span> ( <span
class="methodparam"><span class="type">call</span> `$callback`</span> ,
<span class="methodparam"><span class="type">int</span>
`$error_types`</span> )

设置错误处理函数，一般在<a href="/yaf/appconfig.html#" class="link">application.dispatcher.throwException</a>关闭的情况下，Yaf会在出错的时候触发错误，这个时候，如果设置了错误处理函数，则会把控制交给错误处理函数处理。

因此，当错误发生的时候这个错误处理函数将被调用。

### 参数

`callback`  
错误处理的回调函数

`error_types`  

### 返回值

### 参见

-   <span class="methodname">Yaf\_Dispatcher::throwException</span>
-   <span class="methodname">Yaf\_Application::getLastErrorNo</span>
-   <span class="methodname">Yaf\_Application::getLastErrorMsg</span>

Yaf\_Dispatcher::setRequest
===========================

The setRequest purpose

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Dispatcher::setRequest</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> )

### 参数

`plugin`  

### 返回值

Yaf\_Dispatcher::setView
========================

设置视图引擎

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Dispatcher::setView</span> ( <span
class="methodparam"><span class="type">Yaf\_View\_Interface</span>
`$view`</span> )

如果你想使用自己的视图引擎代替 <span
class="classname">Yaf\_View\_Simple</span> ，
这个函数会帮你解决这个问题。

### 参数

`view`  
A Yaf\_View\_Interface instance

### 返回值

### 范例

**示例 \#1 <span class="function">A custom View engine</span>example**

``` php
<?php
require "/path/to/smarty/Smarty.class.php";

class Smarty_Adapter implements Yaf_View_Interface
{
    /**
     * Smarty object
     * @var Smarty
     */
    public $_smarty;
 
    /**
     * Constructor
     *
     * @param string $tmplPath
     * @param array $extraParams
     * @return void
     */
    public function __construct($tmplPath = null, $extraParams = array()) {
        $this->_smarty = new Smarty;
 
        if (null !== $tmplPath) {
            $this->setScriptPath($tmplPath);
        }
 
        foreach ($extraParams as $key => $value) {
            $this->_smarty->$key = $value;
        }
    }
 
    /**
     * Set the path to the templates
     *
     * @param string $path The directory to set as the path.
     * @return void
     */
    public function setScriptPath($path)
    {
        if (is_readable($path)) {
            $this->_smarty->template_dir = $path;
            return;
        }
 
        throw new Exception('Invalid path provided');
    }
 
    /**
     * Assign a variable to the template
     *
     * @param string $key The variable name.
     * @param mixed $val The variable value.
     * @return void
     */
    public function __set($key, $val)
    {
        $this->_smarty->assign($key, $val);
    }
 
    /**
     * Allows testing with empty() and isset() to work
     *
     * @param string $key
     * @return boolean
     */
    public function __isset($key)
    {
        return (null !== $this->_smarty->get_template_vars($key));
    }
 
    /**
     * Allows unset() on object properties to work
     *
     * @param string $key
     * @return void
     */
    public function __unset($key)
    {
        $this->_smarty->clear_assign($key);
    }
 
    /**
     * Assign variables to the template
     *
     * Allows setting a specific key to the specified value, OR passing
     * an array of key => value pairs to set en masse.
     *
     * @see __set()
     * @param string|array $spec The assignment strategy to use (key or
     * array of key => value pairs)
     * @param mixed $value (Optional) If assigning a named variable,
     * use this as the value.
     * @return void
     */
    public function assign($spec, $value = null) {
        if (is_array($spec)) {
            $this->_smarty->assign($spec);
            return;
        }
 
        $this->_smarty->assign($spec, $value);
    }
 
    /**
     * Clear all assigned variables
     *
     * Clears all variables assigned to Yaf_View either via
     * {@link assign()} or property overloading
     * ({@link __get()}/{@link __set()}).
     *
     * @return void
     */
    public function clearVars() {
        $this->_smarty->clear_all_assign();
    }
 
    /**
     * Processes a template and returns the output.
     *
     * @param string $name The template to process.
     * @return string The output.
     */
    public function render($name, $value = NULL) {
        return $this->_smarty->fetch($name);
    }

    public function display($name, $value = NULL) {
        echo $this->_smarty->fetch($name);
    }

}
?>
```

**示例 \#2 <span
class="function">Yaf\_Dispatcher::setView</span>example**

``` php
<?php
class Bootstrap extends Yaf_Bootstrap_Abstract {

    /**
     * there are some config for smarty in the config:
     *
     * smarty.left_delimiter   = "{{"
     * smarty.right_delimiter  = "}}"
     * smarty.template_dir     = APPLICATION_PATH "/views/scripts/"
     * smarty.compile_dir      = APPLICATION_PATH "/views/templates_c/"
     * smarty.cache_dir        = APPLICATION_PATH "/views/templates_d/"
     *
     */
    public function _initConfig() {
        $config = Yaf_Application::app()->getConfig();
        Yaf_Registry::set("config", $config);
    }

    public function _initLocalName() {
        /** we put class Smarty_Adapter under the local library directory */
        Yaf_Loader::getInstance()->registerLocalNamespace('Smarty');
    }

    public function _initSmarty(Yaf_Dispatcher $dispatcher) {
        $smarty = new Smarty_Adapter(null, Yaf_Registry::get("config")->get("smarty"));
        $dispatcher->setView($smarty);
        /* now the Smarty view engine become the default view engine of Yaf */
    }
}
?>
```

### 参见

-   <span class="classname">Yaf\_View\_Interface</span>
-   <span class="classname">Yaf\_View\_Simple</span>

Yaf\_Dispatcher::throwException
===============================

开启/关闭异常抛出

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Dispatcher</span> <span
class="methodname">Yaf\_Dispatcher::throwException</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$flag`</span> \] )

当意外的错误发生的时候，开启/关闭异常抛出。
当开启的时候，Yaf将会抛出异常而不是触发可捕捉的错误。

你也可以使用
<a href="/yaf/appconfig.html#" class="link">application.dispatcher.throwException</a>来达到相同的目的。

### 参数

`flag`  
bool

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Dispatcher::throwexception</span>example**

``` php
<?php

$config = array(
    'application' => array(
        'directory' => dirname(__FILE__),
    ),
);
$app = new Yaf_Application($config);

$app->getDispatcher()->throwException(true);

try {
    $app->run();
} catch (Yaf_Exception $e) {
    var_dump($e->getMessage());
}
?>
```

以上例程的输出类似于：

    string(59) "Could not find controller script /tmp/controllers/Index.php"

**示例 \#2 <span
class="function">Yaf\_Dispatcher::throwexception</span>example**

``` php
<?php

$config = array(
    'application' => array(
        'directory' => dirname(__FILE__),
    ),
);
$app = new Yaf_Application($config);

$app->getDispatcher()->throwException(false);

$app->run();
?>
```

以上例程的输出类似于：

    PHP Catchable fatal error:  Yaf_Application::run(): Could not find controller script /tmp/controllers/Index.php in /tmp/1.php on line 12

### 参见

-   <span class="methodname">Yaf\_Dispatcher::catchException</span>
-   <span class="classname">Yaf\_Exception</span>

简介
----

类摘要
------

**Yaf\_Config\_Abstract**

<span class="ooclass"> <span class="modifier">abstract</span> class
**Yaf\_Config\_Abstract** </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_config` ;

<span class="modifier">protected</span> `$_readonly` ;

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">get</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">readonly</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="type">Yaf\_Config\_Abstract</span> <span
class="methodname">set</span> ( <span class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">array</span> <span
class="methodname">toArray</span> ( <span
class="methodparam">void</span> )

}

属性
----

`_config`  

`_readonly`  

Yaf\_Config\_Abstract::get
==========================

Getter

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Yaf\_Config\_Abstract::get</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Abstract::readonly
===============================

寻找只读配置

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">Yaf\_Config\_Abstract::readonly</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Abstract::set
==========================

Setter

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="type">Yaf\_Config\_Abstract</span> <span
class="methodname">Yaf\_Config\_Abstract::set</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Abstract::toArray
==============================

转换为数组

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">array</span> <span
class="methodname">Yaf\_Config\_Abstract::toArray</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

Yaf\_Config\_Ini允许开发者通过嵌套的对象属性语法在应用程序中用熟悉的INI格式存储和读取配置数据。
INI格式在提供拥有配置数据键的等级结构和配置数据节之间的继承能力方面具有专长。
配置数据等级结构通过用点或者句号(.)分离键值。
一个节可以扩展或者通过在节的名称之后带一个冒号(:)和被继承的配置数据的节的名称来从另一个节继承。

> **Note**:
>
> Yaf\_Config\_Ini利用PHP的函数parse\_ini\_file()来解析配置文件的。
> 请仔细查看这个函数的文档，注意它的一些特殊用途。以及它传递给Yaf\_Config\_Ini的一些比如
> "TRUE", "FALSE","yes", "no", 和"NULL"的特殊值的处理方式

类摘要
------

**Yaf\_Config\_Ini**

<span class="ooclass"> class **Yaf\_Config\_Ini** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Config\_Abstract** </span> <span class="oointerface">implements
<span class="interfacename">Iterator</span> </span> <span
class="oointerface">, <span class="interfacename">Traversable</span>
</span> <span class="oointerface">, <span
class="interfacename">ArrayAccess</span> </span> <span
class="oointerface">, <span class="interfacename">Countable</span>
</span> {

/\* 属性 \*/

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$config_file`</span> \[, <span class="methodparam"><span
class="type">string</span> `$section`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">count</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_get</span> (\[ <span
class="methodparam"><span class="type">string</span> `$name`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_isset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetExists</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetGet</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetSet</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetUnset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">readonly</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_set</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">toArray</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Yaf\_Config\_Abstract::get</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">Yaf\_Config\_Abstract::readonly</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="type">Yaf\_Config\_Abstract</span> <span
class="methodname">Yaf\_Config\_Abstract::set</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">array</span> <span
class="methodname">Yaf\_Config\_Abstract::toArray</span> ( <span
class="methodparam">void</span> )

}

属性
----

`_config`  

`_readonly`  

范例
----

**示例 \#1 <span class="function">Yaf\_Config\_Ini</span>example**

这个例子说明了使用Yaf\_Config\_Ini从一个INI配置文件中获取配置数据的基本用法。
这个例子中既有生产环境的配置方法也有演示环境的配置方法。
因为演示环境的配置跟生产环境的非常类似，所以演示环境的配置继承了生产环境的配置。
在复杂的情况下，决定是任意的，也可以写成相反的。在更复杂的情况下，生产环境继承自演示环境不是不可能的。
假设，以下配置数据都包含在/path/to/config.ini中：

``` ini
; Production site configuration data
[production]
webhost                  = www.example.com
database.adapter         = pdo_mysql
database.params.host     = db.example.com
database.params.username = dbuser
database.params.password = secret
database.params.dbname   = dbname
 
; Staging site configuration data inherits from production and
; overrides values as necessary
[staging : production]
database.params.host     = dev.example.com
database.params.username = devuser
database.params.password = devsecret
```

``` php
<?php
$config = new Yaf_Config_Ini('/path/to/config.ini', 'staging');
 
var_dump($config->database->params->host); 
var_dump($config->database->params->dbname);
var_dump($config->get("database.params.username"));
?>
```

以上例程的输出类似于：

    string(15) "dev.example.com"
    string(6) "dbname"
    string(7) "devuser

Yaf\_Config\_Ini::\_\_construct
===============================

构造函数

### 说明

<span class="modifier">public</span> <span
class="methodname">Yaf\_Config\_Ini::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$config_file`</span> \[, <span class="methodparam"><span
class="type">string</span> `$section`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`config_file`  

`section`  

### 返回值

Yaf\_Config\_Ini::count
=======================

返回配置的节数量

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::count</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Ini::current
=========================

返回当前节点

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::current</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Ini::\_\_get
=========================

读取节点配置

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::\_\_get</span> (\[ <span
class="methodparam"><span class="type">string</span> `$name`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Config\_Ini::\_\_isset
===========================

检查节点是否存在

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::\_\_isset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Config\_Ini::key
=====================

返回当前元素的键

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::key</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Ini::next
======================

向前移动到下一个元素

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::next</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Ini::offsetExists
==============================

检查一个偏移位置是否存在

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::offsetExists</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Config\_Ini::offsetGet
===========================

获取一个偏移位置的值

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::offsetGet</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Config\_Ini::offsetSet
===========================

设置一个偏移位置的值

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::offsetSet</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

`value`  

### 返回值

Yaf\_Config\_Ini::offsetUnset
=============================

复位一个偏移位置的值

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::offsetUnset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Config\_Ini::readonly
==========================

检查配置是否只读

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::readonly</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Ini::rewind
========================

检查当前位置是否有效

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::rewind</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Ini::\_\_set
=========================

The \_\_set purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::\_\_set</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

`value`  

### 返回值

Yaf\_Config\_Ini::toArray
=========================

转换为数组的格式

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::toArray</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Ini::valid
=======================

检查迭代器是否有效

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Ini::valid</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

Yaf\_Config\_Simple 是 Yad\_Config\_ini
的简洁版本，只允许传入数组进行初始化，并提供了设置readonly的参数。

类摘要
------

**Yaf\_Config\_Simple**

<span class="ooclass"> class **Yaf\_Config\_Simple** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Config\_Abstract** </span> <span class="oointerface">implements
<span class="interfacename">Iterator</span> </span> <span
class="oointerface">, <span class="interfacename">Traversable</span>
</span> <span class="oointerface">, <span
class="interfacename">ArrayAccess</span> </span> <span
class="oointerface">, <span class="interfacename">Countable</span>
</span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_readonly` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$config_file`</span> \[, <span class="methodparam"><span
class="type">string</span> `$section`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">count</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_get</span> (\[ <span
class="methodparam"><span class="type">string</span> `$name`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_isset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetExists</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetGet</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetSet</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetUnset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">readonly</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_set</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">toArray</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Yaf\_Config\_Abstract::get</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">Yaf\_Config\_Abstract::readonly</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="type">Yaf\_Config\_Abstract</span> <span
class="methodname">Yaf\_Config\_Abstract::set</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">array</span> <span
class="methodname">Yaf\_Config\_Abstract::toArray</span> ( <span
class="methodparam">void</span> )

}

属性
----

`_config`  

`_readonly`  

Yaf\_Config\_Simple::\_\_construct
==================================

构造函数

### 说明

<span class="modifier">public</span> <span
class="methodname">Yaf\_Config\_Simple::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$config_file`</span> \[, <span class="methodparam"><span
class="type">string</span> `$section`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`config_file`  

`section`  

### 返回值

Yaf\_Config\_Simple::count
==========================

返回配置的节数量

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::count</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Simple::current
============================

返回当前节点

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::current</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Simple::\_\_get
============================

读取节点配置

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::\_\_get</span> (\[ <span
class="methodparam"><span class="type">string</span> `$name`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Config\_Simple::\_\_isset
==============================

检查节点是否存在

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::\_\_isset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Config\_Simple::key
========================

返回当前元素的键

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::key</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Simple::next
=========================

向前移动到下一个元素

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::next</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Simple::offsetExists
=================================

检查一个偏移位置是否存在

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::offsetExists</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Config\_Simple::offsetGet
==============================

获取一个偏移位置的值

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::offsetGet</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Config\_Simple::offsetSet
==============================

设置一个偏移位置的值

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::offsetSet</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

`value`  

### 返回值

Yaf\_Config\_Simple::offsetUnset
================================

复位一个偏移位置的值

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::offsetUnset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Config\_Simple::readonly
=============================

检查配置是否只读

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::readonly</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Simple::rewind
===========================

检查当前位置是否有效

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::rewind</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Simple::\_\_set
============================

设置节点配置

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::\_\_set</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

`value`  

### 返回值

Yaf\_Config\_Simple::toArray
============================

转换为数组的格式

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::toArray</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Config\_Simple::valid
==========================

检查迭代器是否有效

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Config\_Simple::valid</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

<span class="classname">Yaf\_Controller\_Abstract</span>
是Yaf的MVC体系的核心部分。 MVC是指Model-View-Controller,
是一个用于分离应用逻辑和表现逻辑的设计模式。

每个用户自定义controller都应当继承<span
class="classname">Yaf\_Controller\_Abstract</span>。

你会发现在你自己的controller中无法定义\_\_construct方法。因此，<span
class="classname">Yaf\_Controller\_Abstract</span>
提供了一个魔术方法Yaf\_Controller\_Abstract::init()。

如果在你自己的controller里面已经定义了一个init()方法，当你的controller被实例化的时候，它将被调用。

Action可能需要参数，当一个请求来到的时候，在路由中如果请求的参数有相同名称的变量（例如：
<span class="methodname">Yaf\_Request\_Abstract::getParam</span>），
Yaf将把他们传递给action方法（see <span
class="methodname">Yaf\_Action\_Abstract::execute</span>）。

类摘要
------

**Yaf\_Controller\_Abstract**

<span class="ooclass"> <span class="modifier">abstract</span> class
**Yaf\_Controller\_Abstract** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$actions` ;

<span class="modifier">protected</span> `$_module` ;

<span class="modifier">protected</span> `$_name` ;

<span class="modifier">protected</span> `$_request` ;

<span class="modifier">protected</span> `$_response` ;

<span class="modifier">protected</span> `$_invoke_args` ;

<span class="modifier">protected</span> `$_view` ;

/\* 方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">protected</span> <span class="type">bool</span>
<span class="methodname">display</span> ( <span
class="methodparam"><span class="type">string</span> `$tpl`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$parameters`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">forward</span> ( <span
class="methodparam"><span class="type">string</span> `$module`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$controller`</span> \[, <span class="methodparam"><span
class="type">string</span> `$action`</span> \[, <span
class="methodparam"><span class="type">array</span> `$paramters`</span>
\]\]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getInvokeArg</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getInvokeArgs</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getModuleName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Request\_Abstract</span> <span
class="methodname">getRequest</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Response\_Abstract</span> <span
class="methodname">getResponse</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_View\_Interface</span> <span
class="methodname">getView</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getViewpath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">init</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">initView</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`</span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">redirect</span> ( <span
class="methodparam"><span class="type">string</span> `$url`</span> )

<span class="modifier">protected</span> <span class="type">string</span>
<span class="methodname">render</span> ( <span class="methodparam"><span
class="type">string</span> `$tpl`</span> \[, <span
class="methodparam"><span class="type">array</span> `$parameters`</span>
\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setViewpath</span> ( <span
class="methodparam"><span class="type">string</span>
`$view_directory`</span> )

}

属性
----

`actions`  
你也可以通过使用这个值和 <span
class="classname">Yaf\_Action\_Abstract</span>
在一个单独的PHP脚本中定义action函数。

**示例 \#1 在一个独立的文件中定义action**

``` php
<?php
class IndexController extends Yaf_Controller_Abstract {
    protected $actions = array(
        /** now dummyAction is defined in a separate file */
        "dummy" => "actions/Dummy_action.php",
    );

    /* action method may have arguments */
    public indexAction($name, $id) {
       assert($name == $this->getRequest()->getParam("name"));
       assert($id   == $this->_request->getParam("id"));
    }
}
?>
```

**示例 \#2 Dummy\_action.php**

``` php
<?php
class DummyAction extends Yaf_Action_Abstract {
    /* a action class shall define this method  as the entry point */
    public execute() {
    }
}
?>
```

`_module`  
模块名

`_name`  

`_request`  
当前的请求实例

`_response`  

`_invoke_args`  

`_view`  
视图引擎

Yaf\_Controller\_Abstract::\_\_construct
========================================

Yaf\_Controller\_Abstract constructor

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">Yaf\_Controller\_Abstract::\_\_construct</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Yaf\_Controller\_Abstract::display
==================================

The display purpose

### 说明

<span class="modifier">protected</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Controller\_Abstract::display</span> (
<span class="methodparam"><span class="type">string</span> `$tpl`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$parameters`</span> \] )

### 参数

`tpl`  

`parameters`  

### 返回值

Yaf\_Controller\_Abstract::forward
==================================

The forward purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::forward</span> (
<span class="methodparam"><span class="type">string</span>
`$module`</span> \[, <span class="methodparam"><span
class="type">string</span> `$controller`</span> \[, <span
class="methodparam"><span class="type">string</span> `$action`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$paramters`</span> \]\]\] )

将当前的请求转交给另外的Action.

> **Note**:
>
> 调用 <span
> class="methodname">Yaf\_Controller\_Abstract::forward</span>以后,
> 不会直接立即跳转到目的Action执行, 而是会在当前的Action执行完成后,
> 下一轮的DispatchLoop中, 交给目的Action.
>
> 所以, 如果你希望立即跳转到目的Action,
> 那么请使用return结束当前的执行流程.

### 参数

`module`  
要跳转的目的Action的Module, 如果是NULL, 则默认Module会被采用.

`controller`  
要跳转的目的Action的Controller, 如果是NULL, 则默认Controller会被采用.

`action`  
要跳转的目的Action.

`paramters`  
跳转参数, 可以在目的Action中通过 <span
class="methodname">Yaf\_Request\_Abstrace::getParam</span>来获取.

### 范例

**示例 \#1 <span
class="function">Yaf\_Controller\_Abstract::forward</span>例子**

``` php
<?php
class IndexController extends Yaf_Controller_Abstract
{
    public function indexAction(){   
         $logined = $_SESSION["login"];
         if (!$logined) {
             $this->forward("login", array("from" => "Index")); // 跳转到login Action
             return FALSE;  // return立即结束当前的执行流程, 跳转到目的Action
                            // 而这里的FALSE是告诉Yaf不要自动渲染这个Action的视图
         }

         // other processes
    }

    public function loginAction() {
         echo "login, redirected from ", $this->_request->getParam("from") , " action";
    }
}
?>
```

以上例程的输出类似于：

       login, redirected from Index action

### 返回值

return FALSE on failure

### 参见

-   <span class="methodname">Yaf\_Request\_Abstrace::getParam</span>

Yaf\_Controller\_Abstract::getInvokeArg
=======================================

The getInvokeArg purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::getInvokeArg</span>
( <span class="methodparam"><span class="type">string</span>
`$name`</span> )

### 参数

`name`  

### 返回值

Yaf\_Controller\_Abstract::getInvokeArgs
========================================

The getInvokeArgs purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::getInvokeArgs</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Yaf\_Controller\_Abstract::getModuleName
========================================

获取当前控制器所属的模块名

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Controller\_Abstract::getModuleName</span>
( <span class="methodparam">void</span> )

获取当前控制器所属的模块名

### 参数

此函数没有参数。

### 返回值

Yaf\_Controller\_Abstract::getName
==================================

Get self name

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Controller\_Abstract::getName</span> (
<span class="methodparam">void</span> )

get the controller's name

### 参数

此函数没有参数。

### 返回值

<span class="type">string</span>, controller name

Yaf\_Controller\_Abstract::getRequest
=====================================

The getRequest purpose

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Request\_Abstract</span> <span
class="methodname">Yaf\_Controller\_Abstract::getRequest</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Yaf\_Controller\_Abstract::getResponse
======================================

The getResponse purpose

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Response\_Abstract</span> <span
class="methodname">Yaf\_Controller\_Abstract::getResponse</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Yaf\_Controller\_Abstract::getView
==================================

获取当前的视图引擎

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_View\_Interface</span> <span
class="methodname">Yaf\_Controller\_Abstract::getView</span> ( <span
class="methodparam">void</span> )

获取当前的视图引擎

### 参数

此函数没有参数。

### 返回值

Yaf\_Controller\_Abstract::getViewpath
======================================

The getViewpath purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::getViewpath</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Yaf\_Controller\_Abstract::init
===============================

控制器初始化

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::init</span> ( <span
class="methodparam">void</span> )

<span class="methodname">Yaf\_Controller\_Abstract::\_\_construct</span>
是final类型，所以用户不能重载它。但是用户可以定义 <span
class="methodname">Yaf\_Controller\_Abstract::init</span>，该函数会在控制器对象实例化之后被调用。

### 参数

此函数没有参数。

### 返回值

### 参见

-   <span
    class="methodname">Yaf\_Controller\_Abstract::\_\_construct</span>

Yaf\_Controller\_Abstract::initView
===================================

The initView purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::initView</span> (\[
<span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

### 参数

`options`  

### 返回值

Yaf\_Controller\_Abstract::redirect
===================================

The redirect purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::redirect</span> (
<span class="methodparam"><span class="type">string</span> `$url`</span>
)

### 参数

`url`  

### 返回值

Yaf\_Controller\_Abstract::render
=================================

渲染视图模板

### 说明

<span class="modifier">protected</span> <span class="type">string</span>
<span class="methodname">Yaf\_Controller\_Abstract::render</span> (
<span class="methodparam"><span class="type">string</span> `$tpl`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$parameters`</span> \] )

### 参数

`tpl`  

`parameters`  

### 返回值

Yaf\_Controller\_Abstract::setViewpath
======================================

The setViewpath purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::setViewpath</span> (
<span class="methodparam"><span class="type">string</span>
`$view_directory`</span> )

### 参数

`view_directory`  

### 返回值

简介
----

在Yaf中一个action可以采用单独定义<span
class="classname">Yaf\_Action\_Abstract</span>来实现。
亦即，一个action方法也可以是一个<span
class="classname">Yaf\_Action\_Abstract</span>的派生类

Yaf需要一个可以被它所调用的入口点（比如PHP
5.3，它有一个新的魔术方法\_\_invoke，但是Yaf不只支持PHP 5.3+，
所以Yaf需要另一个魔术方法来执行完成这样的任务），所以在你自己的动作类里面必须要实现抽象方法
<span class="methodname">Yaf\_Action\_Abstract::execute</span>

类摘要
------

**Yaf\_Action\_Abstract**

<span class="ooclass"> class **Yaf\_Action\_Abstract** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Controller\_Abstract** </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_controller` ;

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span><span class="type">mixed</span> <span
class="methodname">execute</span> (\[ <span class="methodparam"><span
class="type">mixed</span> `$arg`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$...`</span> \]\] )

<span class="modifier">public</span><span
class="type">Yaf\_Controller\_Abstract</span> <span
class="methodname">getController</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getControllerName</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">Yaf\_Controller\_Abstract::\_\_construct</span> (
<span class="methodparam">void</span> )

<span class="modifier">protected</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Controller\_Abstract::display</span> (
<span class="methodparam"><span class="type">string</span> `$tpl`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$parameters`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::forward</span> (
<span class="methodparam"><span class="type">string</span>
`$module`</span> \[, <span class="methodparam"><span
class="type">string</span> `$controller`</span> \[, <span
class="methodparam"><span class="type">string</span> `$action`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$paramters`</span> \]\]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::getInvokeArg</span>
( <span class="methodparam"><span class="type">string</span>
`$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::getInvokeArgs</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Controller\_Abstract::getModuleName</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Controller\_Abstract::getName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Request\_Abstract</span> <span
class="methodname">Yaf\_Controller\_Abstract::getRequest</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Response\_Abstract</span> <span
class="methodname">Yaf\_Controller\_Abstract::getResponse</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_View\_Interface</span> <span
class="methodname">Yaf\_Controller\_Abstract::getView</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::getViewpath</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::init</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::initView</span> (\[
<span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::redirect</span> (
<span class="methodparam"><span class="type">string</span> `$url`</span>
)

<span class="modifier">protected</span> <span class="type">string</span>
<span class="methodname">Yaf\_Controller\_Abstract::render</span> (
<span class="methodparam"><span class="type">string</span> `$tpl`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$parameters`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Controller\_Abstract::setViewpath</span> (
<span class="methodparam"><span class="type">string</span>
`$view_directory`</span> )

}

属性
----

`_module`  

`_name`  

`_request`  

`_response`  

`_invoke_args`  

`_view`  

`_controller`  

Yaf\_Action\_Abstract::execute
==============================

执行动作

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span><span class="type">mixed</span> <span
class="methodname">Yaf\_Action\_Abstract::execute</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$arg`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$...`</span>
\]\] )

<span class="methodname">Yaf\_Action\_Abstract::execute</span>
可能会有参数

> **Note**:
>
> 从请求返回的值可能是不安全的，在使用之前你需要对它们过滤一遍。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Action\_Abstract::execute</span>example**

``` php
<?php
/** 
 * A controller example
 */
class ProductController extends Yaf_Controller_Abstract {
      protected $actions = array(
          "index" => "actions/Index.php",
      );
}
?>
```

**示例 \#2 <span
class="function">Yaf\_Action\_Abstract::execute</span>example**

``` php
<?php
/** 
 * ListAction
 */
class ListAction extends Yaf_Action_Abstract {
     public function execute ($name, $id) {
         assert($name == $this->getRequest()->getParam("name"));
         assert($id   == $this->getRequest()->getParam("id"));
     }
}
?>
```

以上例程的输出类似于：

    /**
     * Now assuming we are using the Yaf_Route_Static route 
     * for request: http://yourdomain/product/list/name/yaf/id/22
     * will result:
     */
     bool(true)
     bool(true)

### 参见

-   

Yaf\_Action\_Abstract::getController
====================================

得到控制器实例

### 说明

<span class="modifier">public</span><span
class="type">Yaf\_Controller\_Abstract</span> <span
class="methodname">Yaf\_Action\_Abstract::getController</span> ( <span
class="methodparam">void</span> )

返回控制器对象。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Action\_Abstract::getControllerName
========================================

Get controller name

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Action\_Abstract::getControllerName</span>
( <span class="methodparam">void</span> )

get the controller's name

### 参数

此函数没有参数。

### 返回值

<span class="type">string</span>, controller name

简介
----

Yaf给用户提供一个了一个可扩展的、可自定的视图引擎接口，用户可以使用自己的视图引擎来代替Yaf内置的<span
class="classname">Yaf\_View\_Simple</span>。下面是一个关于怎么实现的例子，请看
<span class="methodname">Yaf\_Dispatcher::setView</span>。

类摘要
------

**Yaf\_View\_Interface**

<span class="ooclass"> class **Yaf\_View\_Interface** </span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">assign</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> \[, <span
class="methodparam"><span class="type">string</span> `$value`</span> \]
)

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">display</span> ( <span class="methodparam"><span
class="type">string</span> `$tpl`</span> \[, <span
class="methodparam"><span class="type">array</span> `$tpl_vars`</span>
\] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">getScriptPath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">render</span> ( <span class="methodparam"><span
class="type">string</span> `$tpl`</span> \[, <span
class="methodparam"><span class="type">array</span> `$tpl_vars`</span>
\] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">setScriptPath</span> ( <span
class="methodparam"><span class="type">string</span>
`$template_dir`</span> )

}

Yaf\_View\_Interface::assign
============================

为视图引擎分配一个模板变量

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">Yaf\_View\_Interface::assign</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \] )

为视图引擎分配一个模板变量,
在视图模板中可以直接通过${$name}获取模板变量值

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

`value`  

### 返回值

Yaf\_View\_Interface::display
=============================

渲染一个视图模板, 并直接输出给请求端

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">Yaf\_View\_Interface::display</span> ( <span
class="methodparam"><span class="type">string</span> `$tpl`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$tpl_vars`</span> \] )

渲染一个视图模板, 并直接输出给请求端

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`tpl`  

`tpl_vars`  

### 返回值

Yaf\_View\_Interface::getScriptPath
===================================

The getScriptPath purpose

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Yaf\_View\_Interface::getScriptPath</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_View\_Interface::render
============================

渲染一个视图模板

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">Yaf\_View\_Interface::render</span> ( <span
class="methodparam"><span class="type">string</span> `$tpl`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$tpl_vars`</span> \] )

渲染一个视图模板, 得到结果

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`tpl`  

`tpl_vars`  

### 返回值

Yaf\_View\_Interface::setScriptPath
===================================

The setScriptPath purpose

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Yaf\_View\_Interface::setScriptPath</span> ( <span
class="methodparam"><span class="type">string</span>
`$template_dir`</span> )

设置模板的基目录，这通常通过<span
class="classname">Yaf\_Dispatcher</span>调用。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`template_dir`  
模板目录的绝对路径，默认的<span
class="classname">Yaf\_Dispatcher</span>会设置此目录为<a href="/yaf/appconfig.html#" class="link">application.directory</a>
. "/views".

### 返回值

简介
----

<span class="classname">Yaf\_View\_Simple</span>
这是Yaf内建的一个模板引擎，是个简单而快速的模板引擎，只支持PHP脚本

类摘要
------

**Yaf\_View\_Simple**

<span class="ooclass"> class **Yaf\_View\_Simple** </span> <span
class="oointerface">implements <span
class="interfacename">Yaf\_View\_Interface</span> </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_tpl_vars` ;

<span class="modifier">protected</span> `$_tpl_dir` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">assign</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">assignRef</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`&$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">clear</span> (\[ <span
class="methodparam"><span class="type">string</span> `$name`</span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$tempalte_dir`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">display</span> ( <span
class="methodparam"><span class="type">string</span> `$tpl`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$tpl_vars`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">eval</span> ( <span class="methodparam"><span
class="type">string</span> `$tpl_content`</span> \[, <span
class="methodparam"><span class="type">array</span> `$tpl_vars`</span>
\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_get</span> (\[ <span
class="methodparam"><span class="type">string</span> `$name`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getScriptPath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_isset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">render</span> ( <span class="methodparam"><span
class="type">string</span> `$tpl`</span> \[, <span
class="methodparam"><span class="type">array</span> `$tpl_vars`</span>
\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_set</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setScriptPath</span> ( <span
class="methodparam"><span class="type">string</span>
`$template_dir`</span> )

}

属性
----

`_tpl_vars`  

`_tpl_dir`  

Yaf\_View\_Simple::assign
=========================

为视图引擎分配一个模板变量

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_View\_Simple::assign</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> \] )

为视图引擎分配一个模板变量

### 参数

`name`  
字符串或者数组

如果为字符串, 则$value不能为空

`value`  
mixed value

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_View\_Simple::assign</span>example**

``` php
<?php
class IndexController extends Yaf_Controller_Abstract {
    public function indexAction() {
        $this->getView()->assign("foo", "bar");
        $this->_view->assign( array( "key" => "value", "name" => "value"));
    }
?>
```

**示例 \#2 <span class="function">template</span>example**

``` php
<html>
 <head>
  <title><?php echo $foo; ?></title>
 </head>  
<body>
  <?php 
    foreach ($this->_tpl_vars as $name => value) {
         echo $$name; // or echo $this->_tpl_vars[$name];
    }
  ?>
</body>
</html>
```

### 参见

-   <span class="methodname">Yaf\_View\_Simple::assignRef</span>
-   <span class="methodname">Yaf\_View\_Interface::clear</span>
-   <span class="methodname">Yaf\_View\_Simple::\_\_set</span>

Yaf\_View\_Simple::assignRef
============================

The assignRef purpose

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_View\_Simple::assignRef</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`&$value`</span> )

不同于 <span
class="methodname">Yaf\_View\_Simple::assign</span>，这个方法传递一个引用变量给模板引擎

### 参数

`name`  
一个字符串的名字，被用来传递值给模板。

`value`  
mixed value

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_View\_Simple::assignRef</span>example**

``` php
<?php
class IndexController extends Yaf_Controller_Abstract {
    public function indexAction() {
        $value = "bar";
        $this->getView()->assign("foo", $value);

        /* plz note that there was a bug before Yaf 2.1.4, 
         * which make following output "bar";
         */
        $dummy = $this->getView()->render("index/index.phtml");
        echo $value;

        //prevent the auto-render
        Yaf_Dispatcher::getInstance()->autoRender(FALSE);
    }
?>
```

**示例 \#2 <span class="function">template</span>example**

``` php
<html>
 <head>
  <title><?php echo $foo;  $foo = "changed"; ?></title>
 </head>  
<body>
</body>
</html>
```

以上例程的输出类似于：

    /* access the index controller will result: */
    changed

### 参见

-   <span class="methodname">Yaf\_View\_Simple::assign</span>
-   <span class="methodname">Yaf\_View\_Simple::\_\_set</span>

Yaf\_View\_Simple::clear
========================

Clear Assigned values

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_View\_Simple::clear</span> (\[ <span
class="methodparam"><span class="type">string</span> `$name`</span> \] )

清除指定的变量

### 参数

`name`  
分派的变量名

如果为空，将会清除所有的变量

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_View\_Simple::clear</span>example**

``` php
<?php
class IndexController extends Yaf_Controller_Abstract {
    public function indexAction() {
        $this->getView()->clear("foo")->clear("bar"); // clear "foo" and "bar"
        $this->_view->clear(); //clear all assigned variables
    }
?>
```

### 参见

-   <span class="methodname">Yaf\_View\_Simple::assignRef</span>
-   <span class="methodname">Yaf\_View\_Interface::assign</span>
-   <span class="methodname">Yaf\_View\_Simple::\_\_set</span>

Yaf\_View\_Simple::\_\_construct
================================

Constructor of Yaf\_View\_Simple

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">Yaf\_View\_Simple::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$tempalte_dir`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`</span> \] )

### 参数

`tempalte_dir`  
模板的基本路劲，默认为APPLICATOIN . "/views"

`options`  
``` parameters
Options for the engine, as of Yaf 2.1.13, you can use short tag
      "<?=$var?>" in your template(regardless of "short_open_tag"), 
      so comes a option named "short_tag",  you can switch this off 
      to prevent use short_tag in template.
```

### 范例

**示例 \#1 <span
class="function">Yaf\_View\_Simple::\_\_constructor</span>example**

``` php
<?php
   define ("TEMPLATE_DIRECTORY", APPLICATOIN_PATH . '/views');
   $view = new Yaf_View_Simple(TEMPLATE_DIRECTORY, array(
                           'short_tag' => false //doesn't allow use short tag in template
   ));
?>
```

### 返回值

Yaf\_View\_Simple::display
==========================

渲染一个视图模板, 并直接输出给请求端

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_View\_Simple::display</span> ( <span
class="methodparam"><span class="type">string</span> `$tpl`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$tpl_vars`</span> \] )

渲染一个视图模板, 并直接输出给请求端

### 参数

`tpl`  

`tpl_vars`  

### 返回值

Yaf\_View\_Simple::eval
=======================

渲染模板

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_View\_Simple::eval</span> ( <span
class="methodparam"><span class="type">string</span>
`$tpl_content`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tpl_vars`</span> \] )

渲染一个字符串模板，然后返回结果。

### 参数

`tpl_content`  
string template

`tpl_vars`  

### 返回值

Yaf\_View\_Simple::\_\_get
==========================

获取视图引擎的一个模板变量值

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_View\_Simple::\_\_get</span> (\[ <span
class="methodparam"><span class="type">string</span> `$name`</span> \] )

获取视图引擎的一个模板变量值

> **Note**:
>
> 从2.1.11以后，参数可以为空

### 参数

`name`  
分配的变量名

如果为空，所有传递的变量都会被返回

### 返回值

Yaf\_View\_Simple::getScriptPath
================================

获取模板目录

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_View\_Simple::getScriptPath</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Yaf\_View\_Simple::\_\_isset
============================

The \_\_isset purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_View\_Simple::\_\_isset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

### 参数

`name`  

### 返回值

Yaf\_View\_Simple::render
=========================

渲染模板

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_View\_Simple::render</span> ( <span
class="methodparam"><span class="type">string</span> `$tpl`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$tpl_vars`</span> \] )

渲染一个视图模板, 得到结果

### 参数

`tpl`  

`tpl_vars`  

### 返回值

Yaf\_View\_Simple::\_\_set
==========================

为视图引擎分配一个模板变量

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_View\_Simple::\_\_set</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

这是一个更简单并且用来替代 <span
class="methodname">Yaf\_View\_Simple::assign</span> 的方法

### 参数

`name`  
一个字符串值的名字

`value`  
Mixed value.

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_View\_Simple::\_\_set</span>example**

``` php
<?php
class IndexController extends Yaf_Controller_Abstract {
    public function indexAction() {
        $this->getView()->foo = "bar"; // same as assign("foo", "bar");
    }
?>
```

### 参见

-   <span class="methodname">Yaf\_View\_Simple::assignRef</span>
-   <span class="methodname">Yaf\_View\_Interface::assign</span>

Yaf\_View\_Simple::setScriptPath
================================

设置模板的目录

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_View\_Simple::setScriptPath</span> ( <span
class="methodparam"><span class="type">string</span>
`$template_dir`</span> )

### 参数

`template_dir`  

### 返回值

简介
----

<span class="classname">Yaf\_Loader</span>
类为Yaf提供了自动加载功能的全面解决方案。

在第一次使用的时候，将检索 <span
class="classname">Yaf\_Application</span> 的实例， <span
class="classname">Yaf\_Loader</span>
实现了单利模式，并使用spl\_autoload注册它自己。 通过 <span
class="methodname">Yaf\_Loader::getInstance</span> 返回它的实例

<span class="classname">Yaf\_Loader</span>
加载一个类时仅仅尝试一次，如果失败了，
后面的操作将取决于<a href="/yaf/setup.html#" class="link">yaf.use_spl_auload</a>，
如果这个配置项为On， <span
class="methodname">Yaf\_Loader::autoload</span> 将会返回FALSE，
从而把机会让给其他的自动加载功能。如果这个配置项为Off（默认）， <span
class="methodname">Yaf\_Loader::autoload</span> 将会返回TRUE，
最重要的是将会抛出一个非常有用的警告（对于找出一个类加载失败非常有用）。

> **Note**:
>
> 请保持yaf.use\_spl\_autoload保持关闭，除非有一些library有自己的autoload机制，并且是无法改写的。

默认情况下，<span class="classname">Yaf\_Loader</span>
收集所有library(类定义的脚本)储存进在
php.ini(yaf.library)定义的<a href="/yaf/setup.html#" class="link">global library directory</a>之中。

如果你想使用 <span class="classname">Yaf\_Loader</span>
搜索本地类（库）（定义在application.ini， 默认情况下，它是
<a href="/yaf/appconfig.html#" class="link">application.directory</a> .
"/libraray"）， 你需要使用 <span
class="methodname">Yaf\_Loader::registerLocalNameSpace</span>
注册本地类前缀。

让我们来看看一些例子（假设 APPLICATION\_PATH 是
<a href="/yaf/appconfig.html#" class="link">application.directory</a>）：

**示例 \#1 Config example**

``` shell
// Assuming the following configure in php.ini:
yaf.libraray = "/global_dir"

//Assuming the following configure in application.ini
application.libraray = APPLICATION_PATH "/library"
```

假设以下本地名称空间已被注册：

**示例 \#2 注册本地命名空间**

``` php
<?php
class Bootstrap extends Yaf_Bootstrap_Abstract{
     public function _initLoader($dispatcher) {
          Yaf_Loader::getInstance()->registerLocalNameSpace(array("Foo", "Bar"));
     }
?>
```

自动加载例子：

**示例 \#3 加载类**

``` shell
class Foo_Bar_Test =>
  // APPLICATION_PATH/library/Foo/Bar/Test.php
  
class GLO_Name  =>
  // /global_dir/Glo/Name.php
 
class BarNon_Test
  // /global_dir/Barnon/Test.php
```

在PHP 5.3中，你可以使用命名空间：

**示例 \#4 加载命名空间类**

``` shell
class \Foo\Bar\Dummy =>
   // APPLICATION_PATH/library/Foo/Bar/Dummy.php

class \FooBar\Bar\Dummy =>
   // /global_dir/FooBar/Bar/Dummy.php
```

你可能会注意到所有文件夹名字的首字母是大写的，你可以通过在php.ini中设置
<a href="/yaf/setup.html#" class="link">yaf.lowcase_path</a> = On
来将它们小写。

<span class="classname">Yaf\_Loader</span>
也是设计来加载MVC类，响应的规则如下：

**示例 \#5 MVC类加载例子**

``` shell
Controller Classes =>
// APPLICATION_PATH/controllers/

Model Classes =>
// APPLICATION_PATH/models/

Plugin Classes =>
// APPLICATION_PATH/plugins/
```

Yaf 通过识别一个类的后缀（这个是默认的，你也可以通过改变配置项
<a href="/yaf/setup.html#" class="link">yaf.name_suffix</a>
来将它改为通过前缀识别）来决定它是否是一个MVC类：

**示例 \#6 MVC 类区别**

``` shell
Controller Classes =>
    // ***Controller

Model Classes =>
    // ***Model

Plugin Classes =>
    // ***Plugin
```

some examples:

**示例 \#7 MVC loading example**

``` shell
class IndexController
    // APPLICATION_PATH/controllers/Index.php

class DataModel =>
   // APPLICATION_PATH/models/Data.php

class DummyPlugin =>
  // APPLICATION_PATH/plugins/Dummy.php

class A_B_TestModel =>
  // APPLICATION_PATH/models/A/B/Test.php
```

该目录将受 <a href="/yaf/setup.html#" class="link">yaf.lowcase_path</a>
的影响。

类摘要
------

**Yaf\_Loader**

<span class="ooclass"> class **Yaf\_Loader** </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_local_ns` ;

<span class="modifier">protected</span> `$_library` ;

<span class="modifier">protected</span> `$_global_library` ;

<span class="modifier">static</span> `$_instance` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">autoload</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clearLocalNamespace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">private</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">getInstance</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Loader</span> <span
class="methodname">getLibraryPath</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$is_global`<span
class="initializer"> = false</span></span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getLocalNamespace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getNamespacePath</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaces`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getNamespaces</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">import</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isLocalName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">registerLocalNamespace</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$prefix`</span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">registerNamespace</span> ( <span
class="methodparam"><span class="type">string\|array</span>
`$namespaces`</span> \[, <span class="methodparam"><span
class="type">string</span> `$path`</span> \] )

<span class="modifier">public</span> <span
class="type">Yaf\_Loader</span> <span
class="methodname">setLibraryPath</span> ( <span
class="methodparam"><span class="type">string</span> `$directory`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$is_global`<span class="initializer"> = false</span></span> \] )

}

属性
----

`_local_ns`  

`_library`  
默认情况下，它的值是
<a href="/yaf/appconfig.html#" class="link">application.directory</a> .
"/library"， 你可以通过修改application.ini(application.library)或者调用
<span class="methodname">Yaf\_Loader::setLibraryPath</span> 改变它。

`_global_library`  

`_instance`  

Yaf\_Loader::autoload
=====================

The autoload purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Loader::autoload</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Loader::clearLocalNamespace
================================

The clearLocalNamespace purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Loader::clearLocalNamespace</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Loader::\_\_construct
==========================

The \_\_construct purpose

### 说明

<span class="modifier">private</span> <span
class="methodname">Yaf\_Loader::\_\_construct</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Loader::getInstance
========================

The getInstance purpose

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Yaf\_Loader::getInstance</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Loader::getLibraryPath
===========================

get the library path

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Loader</span> <span
class="methodname">Yaf\_Loader::getLibraryPath</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$is_global`<span
class="initializer"> = false</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Loader::getLocalNamespace
==============================

The getLocalNamespace purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Loader::getLocalNamespace</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Loader::getNamespacePath
=============================

Retieve path of a registered namespace

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Loader::getNamespacePath</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaces`</span> )

retrieve path of a registered namespace

### 参数

`namespace`  
a string of namespace.

### 返回值

<span class="type">string</span> path, if the namespace is not
registered, then **`NULL`** default library will be returned

### 范例

**示例 \#1 <span
class="function">Yaf\_Loader::registerNamespace</span>example**

``` php
<?php
$loader = Yaf_Loader::getInstance("/var/application/lib");
$loader->registerNamespace("\Vendor\PHP", "/var/lib/php");

$loader->getNamespacePath("\Vendor\PHP"); // '/var/lib/php'
$loader->getNamespacePath("\Vendor\JSP"); // '/var/application/lib'

?>
```

Yaf\_Loader::getLocalNamespace
==============================

Retrive all register namespaces info

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Yaf\_Loader::getNamespaces</span> ( <span
class="methodparam">void</span> )

get registered namespaces info

### 参数

此函数没有参数。

### 返回值

<span class="type">array</span>

Yaf\_Loader::import
===================

The import purpose

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Yaf\_Loader::import</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Loader::isLocalName
========================

The isLocalName purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Loader::isLocalName</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Loader::registerLocalNamespace
===================================

注册本地类前缀

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Loader::registerLocalNamespace</span> (\[
<span class="methodparam"><span class="type">mixed</span>
`$prefix`</span> \] )

register local class prefix

### 参数

`prefix`  
字符串或者是数组格式的类名前缀，所有拥有和这些前缀相同前缀的类将被加载到本地library路径。

### 返回值

bool

### 范例

**示例 \#1 <span
class="function">Yaf\_Loader::registerLocalNamespace</span>example**

``` php
<?php
$loader = Yaf_Loader::getInstance('/local/library/', '/global/library');
$loader->registerLocalNamespace("Baidu");
$loader->registerLocalNamespace(array("Sina", "Weibo");

$loader->autoload("Baidu_Name"); // search in '/local/library/'
$loader->autoload("Sina");       // search '/local/library/'
$loader->autoload("Global_Name");// search in '/global/library/'
$loader->autoload("Foo_Bar");    // search in '/global/library/'

?>
```

Yaf\_Loader::registerNamespace
==============================

Register namespace with searching path

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Loader::registerNamespace</span> ( <span
class="methodparam"><span class="type">string\|array</span>
`$namespaces`</span> \[, <span class="methodparam"><span
class="type">string</span> `$path`</span> \] )

Register a namespace with searching path, <span
class="classname">Yaf\_Loader</span> searchs classes under this
namespace in path, the one is also could be configureded via
<a href="/yaf/appconfig.html#" class="link">application.library.directory.namespace</a>(in
application.ini);

> **Note**:
>
> Yaf still think underline as folder separator.

### 参数

`namespace`  
a string of namespace, or a array of namespaces with paths.

`path`  
a string of path, it it better to use abosolute path here for
performance

### 返回值

bool

### 范例

**示例 \#1 <span
class="function">Yaf\_Loader::registerNamespace</span>example**

``` php
<?php
$loader = Yaf_Loader::getInstance();
$loader->registerNamespace("\Vendor\PHP", "/var/lib/php");
$loader->registerNamespace(array(
     "\Vendor\ASP" => "/var/lib/asp",
     "\Vendor\JSP" => "/usr/lib/vendor/",
));

$loader->autoload("\Vendor\PHP\Dummy");   //load '/var/lib/php/Dummy.php'
$loader->autoload("\Vendor\PHP\Foo_Bar"); //load '/var/lib/php/Foo/Bar.php'
$loader->autoload("\Vendor\JSP\Dummy");   //load '/usr/lib/vendor/Dummy.php'

?>
```

Yaf\_Loader::setLibraryPath
===========================

改变library路径

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Loader</span> <span
class="methodname">Yaf\_Loader::setLibraryPath</span> ( <span
class="methodparam"><span class="type">string</span> `$directory`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$is_global`<span class="initializer"> = false</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

Plugins 可以让你轻松地定制和扩展框架

插件(Plugins)是一个类。 基于组件定义的类会有所变化 --
你可能需要去实现这些接口。 但实际上，该插件(Plugin)本身就是一个类。

一个插件(plugin)会被 <span
class="methodname">Yaf\_Dispatcher::registerPlugin</span>加载到Yaf框架中，
在框架注册(registerd)后，插件(plugin)类中定义方法将会在恰当的时间被该接口执行。

范例
----

**示例 \#1 Plugin example**

``` php
<?php
   /* bootstrap class should be defined under ./application/Bootstrap.php */
   class Bootstrap extends Yaf_Bootstrap_Abstract {
        public function _initPlugin(Yaf_Dispatcher $dispatcher) {
            /* register a plugin */
            $dispatcher->registerPlugin(new TestPlugin());
        }
   }

   /* plugin class should be placed under ./application/plugins/ */
   class TestPlugin extends Yaf_Plugin_Abstract {
        public function routerStartup(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
            /* 在路由之前执行,这个钩子里，你可以做url重写等功能 */
            var_dump("routerStartup");
        }
        public function routerShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
           /* 路由完成后，在这个钩子里，你可以做登陆检测等功能*/
            var_dump("routerShutdown");
        }
        public function dispatchLoopStartup(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
            var_dump("dispatchLoopStartup");
        }
        public function preDispatch(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
            var_dump("preDispatch");
        }
        public function postDispatch(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
            var_dump("postDispatch");
        }
        public function dispatchLoopShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
            /* final hoook
               in this hook user can do loging or implement layout */
            var_dump("dispatchLoopShutdown");
        }
   }

   Class IndexController extends Yaf_Controller_Abstract {
        public function indexAction() {
            return FALSE; //prevent rendering
        }
   }

   $config = array(
       "application" => array(
           "directory" => dirname(__FILE__) . "/application/",
       ),
   );
 
   $app = new Yaf_Application($config);
   $app->bootstrap()->run();
?>
```

以上例程的输出类似于：

    string(13) "routerStartup"
    string(14) "routerShutdown"
    string(19) "dispatchLoopStartup"
    string(11) "preDispatch"
    string(12) "postDispatch"
    string(20) "dispatchLoopShutdown"

类摘要
------

**Yaf\_Plugin\_Abstract**

<span class="ooclass"> class **Yaf\_Plugin\_Abstract** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">dispatchLoopShutdown</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> , <span class="methodparam"><span
class="type">Yaf\_Response\_Abstract</span> `$response`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">dispatchLoopStartup</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> , <span class="methodparam"><span
class="type">Yaf\_Response\_Abstract</span> `$response`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">postDispatch</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> , <span class="methodparam"><span
class="type">Yaf\_Response\_Abstract</span> `$response`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">preDispatch</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> , <span class="methodparam"><span
class="type">Yaf\_Response\_Abstract</span> `$response`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">preResponse</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> , <span class="methodparam"><span
class="type">Yaf\_Response\_Abstract</span> `$response`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">routerShutdown</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> , <span class="methodparam"><span
class="type">Yaf\_Response\_Abstract</span> `$response`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">routerStartup</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> , <span class="methodparam"><span
class="type">Yaf\_Response\_Abstract</span> `$response`</span> )

}

Yaf\_Plugin\_Abstract::dispatchLoopShutdown
===========================================

The dispatchLoopShutdown purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span
class="methodname">Yaf\_Plugin\_Abstract::dispatchLoopShutdown</span> (
<span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> , <span
class="methodparam"><span class="type">Yaf\_Response\_Abstract</span>
`$response`</span> )

这个方式是Yaf插件钩子系统中最后的一个钩子，如果一个用户插件实现了这个方法，它将在分发循环结束之后触发。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  

`response`  

### 返回值

### 参见

-   <span class="methodname">Yaf\_Plugin\_Abstract::routerStartup</span>
-   <span
    class="methodname">Yaf\_Plugin\_Abstract::routerShutdown</span>
-   <span
    class="methodname">Yaf\_Plugin\_Abstract::dispatchLoopStartup</span>
-   <span class="methodname">Yaf\_Plugin\_Abstract::preDispatch</span>
-   <span class="methodname">Yaf\_Plugin\_Abstract::postDispatch</span>

Yaf\_Plugin\_Abstract::dispatchLoopStartup
==========================================

The dispatchLoopStartup purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span
class="methodname">Yaf\_Plugin\_Abstract::dispatchLoopStartup</span> (
<span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> , <span
class="methodparam"><span class="type">Yaf\_Response\_Abstract</span>
`$response`</span> )

这个钩子将在分发循环开始之前触发。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  

`response`  

### 返回值

Yaf\_Plugin\_Abstract::postDispatch
===================================

The postDispatch purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Plugin\_Abstract::postDispatch</span> (
<span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> , <span
class="methodparam"><span class="type">Yaf\_Response\_Abstract</span>
`$response`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  

`response`  

### 返回值

Yaf\_Plugin\_Abstract::preDispatch
==================================

The preDispatch purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Plugin\_Abstract::preDispatch</span> (
<span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> , <span
class="methodparam"><span class="type">Yaf\_Response\_Abstract</span>
`$response`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  

`response`  

### 返回值

Yaf\_Plugin\_Abstract::preResponse
==================================

The preResponse purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Plugin\_Abstract::preResponse</span> (
<span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> , <span
class="methodparam"><span class="type">Yaf\_Response\_Abstract</span>
`$response`</span> )

这个钩子在响应(Yaf\_Response)前被触发

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  

`response`  

### 返回值

Yaf\_Plugin\_Abstract::routerShutdown
=====================================

The routerShutdown purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Plugin\_Abstract::routerShutdown</span> (
<span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> , <span
class="methodparam"><span class="type">Yaf\_Response\_Abstract</span>
`$response`</span> )

这个钩子在路由结束之后触发，通常被用于登陆检查。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  

`response`  

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Plugin\_Abstract::routerShutdown</span>example**

``` php
<?php
class UserInitPlugin extends Yaf_Plugin_Abstract {

    public function routerShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
        $controller = $request->getControllerName();

        /**
         * Use access controller is unecessary for APIs
         */
        if (in_array(strtolower($controller), array(
            'api',  
        ))) {
            return TRUE;
        }
       
        if (Yaf_Session::getInstance()->has("login")) {
            return TRUE;
        }
 
        /* Use access check failed, need to login */
        $response->redirect("http://yourdomain.com/login/");
        return FALSE;
    }
?>
```

### 参见

-   <span class="methodname">Yaf\_Plugin\_Abstract::routerStartup</span>
-   <span
    class="methodname">Yaf\_Plugin\_Abstract::dispatchLoopStartup</span>
-   <span class="methodname">Yaf\_Plugin\_Abstract::preDispatch</span>
-   <span class="methodname">Yaf\_Plugin\_Abstract::postDispatch</span>
-   <span
    class="methodname">Yaf\_Plugin\_Abstract::dispatchLoopShutdown</span>

Yaf\_Plugin\_Abstract::routerStartup
====================================

RouterStartup hook

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Plugin\_Abstract::routerStartup</span> (
<span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> , <span
class="methodparam"><span class="type">Yaf\_Response\_Abstract</span>
`$response`</span> )

这个是Yaf插件的勾子系统最早被触发的的一个方法，如果一个用户插件实现了这个方法，它将在路由之前触发。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  

`response`  

### 返回值

### 参见

-   <span
    class="methodname">Yaf\_Plugin\_Abstract::routerShutdown</span>
-   <span
    class="methodname">Yaf\_Plugin\_Abstract::dispatchLoopStartup</span>
-   <span class="methodname">Yaf\_Plugin\_Abstract::preDispatch</span>
-   <span class="methodname">Yaf\_Plugin\_Abstract::postDispatch</span>
-   <span
    class="methodname">Yaf\_Plugin\_Abstract::dispatchLoopShutdown</span>

简介
----

<span class="classname">Yaf\_Registry</span>,
对象注册表(或称对象仓库)是一个用于在整个应用空间(application
space)内存储对象和值的容器.
通过把对象存储在其中,我们可以在整个项目的任何地方使用同一个对象.这种机制相当于一种全局存储.
我们可以通过<span
class="classname">Yaf\_Registry</span>类的静态方法来使用对象注册表.
另外,由于该类是一个数组对象,你可以使用数组形式来访问其中的类方法

类摘要
------

**Yaf\_Registry**

<span class="ooclass"> class **Yaf\_Registry** </span> {

/\* 属性 \*/

<span class="modifier">static</span> `$_instance` ;

<span class="modifier">protected</span> `$_entries` ;

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">del</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">get</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">has</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">set</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

}

属性
----

`_instance`  

`_entries`  

Yaf\_Registry::\_\_construct
============================

Yaf\_Registry implements singleton

### 说明

<span class="methodname">Yaf\_Registry::\_\_construct</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Yaf\_Registry::del
==================

Remove an item from registry

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Yaf\_Registry::del</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

删除存在于注册表中的一个项目

### 参数

`name`  

### 返回值

Yaf\_Registry::get
==================

Retrieve an item from registry

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">Yaf\_Registry::get</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

获取注册表中寄存的项

### 参数

`name`  

### 返回值

Yaf\_Registry::has
==================

Check whether an item exists

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">Yaf\_Registry::has</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

查询某一项目是否存在于注册表中

### 参数

`name`  

### 返回值

Yaf\_Registry::set
==================

Add an item into registry

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">Yaf\_Registry::set</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

往全局注册表添加一个新的项

### 参数

`name`  

`value`  

### 返回值

简介
----

类摘要
------

**Yaf\_Request\_Abstract**

<span class="ooclass"> class **Yaf\_Request\_Abstract** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">string</span>
`Yaf_Request_Abstract::SCHEME_HTTP` <span class="initializer"> =
http</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`Yaf_Request_Abstract::SCHEME_HTTPS` <span class="initializer"> =
https</span> ;

/\* 属性 \*/

<span class="modifier">public</span> `$module` ;

<span class="modifier">public</span> `$controller` ;

<span class="modifier">public</span> `$action` ;

<span class="modifier">public</span> `$method` ;

<span class="modifier">protected</span> `$params` ;

<span class="modifier">protected</span> `$language` ;

<span class="modifier">protected</span> `$_exception` ;

<span class="modifier">protected</span> `$_base_uri` ;

<span class="modifier">protected</span> `$uri` ;

<span class="modifier">protected</span> `$dispatched` ;

<span class="modifier">protected</span> `$routed` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">clearParams</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getActionName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getBaseUri</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getControllerName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getEnv</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> \[, <span
class="methodparam"><span class="type">string</span> `$default`</span>
\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getException</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getLanguage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getMethod</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getModuleName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getParam</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getParams</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getRequestUri</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getServer</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isCli</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isDispatched</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isGet</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isHead</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isOptions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isPost</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isPut</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isRouted</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isXmlHttpRequest</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setActionName</span> ( <span
class="methodparam"><span class="type">string</span> `$action`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setBaseUri</span> ( <span
class="methodparam"><span class="type">string</span> `$uir`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setControllerName</span> ( <span
class="methodparam"><span class="type">string</span>
`$controller`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setDispatched</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setModuleName</span> ( <span
class="methodparam"><span class="type">string</span> `$module`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setParam</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setRequestUri</span> ( <span
class="methodparam"><span class="type">string</span> `$uir`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setRouted</span> (\[ <span
class="methodparam"><span class="type">string</span> `$flag`</span> \] )

}

属性
----

`module`  

`controller`  

`action`  

`method`  

`params`  

`language`  

`_exception`  

`_base_uri`  

`uri`  

`dispatched`  

`routed`  

预定义常量
----------

**`Yaf_Request_Abstract::SCHEME_HTTP`**  

**`Yaf_Request_Abstract::SCHEME_HTTPS`**  

Yaf\_Request\_Abstract::clearParams
===================================

Remove all params

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Request\_Abstract::clearParams</span> (
<span class="methodparam">void</span> )

Remove all params set by router, or <span
class="methodname">Yaf\_Request\_Abstract::setParam</span>

### 参数

此函数没有参数。

### 返回值

<span class="type">boolean</span>

### 参见

-   <span class="methodname">Yaf\_Request\_Abstract::isHead</span>
-   <span class="methodname">Yaf\_Request\_Abstract::isGet</span>
-   <span class="methodname">Yaf\_Request\_Abstract::isPost</span>
-   <span class="methodname">Yaf\_Request\_Abstract::isPut</span>
-   <span class="methodname">Yaf\_Request\_Abstract::isOptions</span>
-   <span
    class="methodname">Yaf\_Request\_Abstract::isXmlHTTPRequest</span>

Yaf\_Request\_Abstract::getActionName
=====================================

The getActionName purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getActionName</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::getBaseUri
==================================

The getBaseUri purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getBaseUri</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::getControllerName
=========================================

The getControllerName purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span
class="methodname">Yaf\_Request\_Abstract::getControllerName</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::getEnv
==============================

取得ENV变量的值

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getEnv</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

取得ENV变量的值

### 参数

`name`  
the variable name

`default`  
如果这个参数被提供了，当参数找不到的时候它将被返回

### 返回值

### 参见

-   <span class="classname">Yaf\_Request\_Abstract::getServer</span>
-   <span class="classname">Yaf\_Request\_Abstract::getParam</span>

Yaf\_Request\_Abstract::getException
====================================

The getException purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getException</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::getLanguage
===================================

The getLanguage purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getLanguage</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::getMethod
=================================

The getMethod purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getMethod</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::getModuleName
=====================================

The getModuleName purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getModuleName</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::getParam
================================

The getParam purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getParam</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

`default`  

### 返回值

Yaf\_Request\_Abstract::getParams
=================================

The getParams purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getParams</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::getRequestUri
=====================================

The getRequestUri purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getRequestUri</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::getServer
=================================

返回SERVER变量的值

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getServer</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$default`</span> \] )

返回SERVER变量的值

### 参数

`name`  
the variable name

`default`  
如果提供这个参数，在没找到变量值时候此参数的值将被返回

### 返回值

### 参见

-   <span class="classname">Yaf\_Request\_Abstract::getParam</span>
-   <span class="classname">Yaf\_Request\_Abstract::getEnv</span>

Yaf\_Request\_Abstract::isCli
=============================

The isCli purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isCli</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::isDispatched
====================================

The isDispatched purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isDispatched</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::isGet
=============================

The isGet purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isGet</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::isHead
==============================

The isHead purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isHead</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::isOptions
=================================

The isOptions purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isOptions</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::isPost
==============================

The isPost purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isPost</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::isPut
=============================

The isPut purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isPut</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::isRouted
================================

The isRouted purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isRouted</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::isXmlHttpRequest
========================================

The isXmlHttpRequest purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isXmlHttpRequest</span>
( <span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::setActionName
=====================================

The setActionName purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setActionName</span> (
<span class="methodparam"><span class="type">string</span>
`$action`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`action`  

### 返回值

Yaf\_Request\_Abstract::setBaseUri
==================================

The setBaseUri purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setBaseUri</span> (
<span class="methodparam"><span class="type">string</span> `$uir`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`uir`  

### 返回值

Yaf\_Request\_Abstract::setControllerName
=========================================

The setControllerName purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span
class="methodname">Yaf\_Request\_Abstract::setControllerName</span> (
<span class="methodparam"><span class="type">string</span>
`$controller`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`controller`  

### 返回值

Yaf\_Request\_Abstract::setDispatched
=====================================

The setDispatched purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setDispatched</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Abstract::setModuleName
=====================================

The setModuleName purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setModuleName</span> (
<span class="methodparam"><span class="type">string</span>
`$module`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`module`  

### 返回值

Yaf\_Request\_Abstract::setParam
================================

The setParam purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setParam</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

`value`  

### 返回值

Yaf\_Request\_Abstract::setRequestUri
=====================================

The setRequestUri purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setRequestUri</span> (
<span class="methodparam"><span class="type">string</span> `$uir`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`uir`  

### 返回值

Yaf\_Request\_Abstract::setRouted
=================================

The setRouted purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setRouted</span> (\[
<span class="methodparam"><span class="type">string</span>
`$flag`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`flag`  

### 返回值

简介
----

类摘要
------

**Yaf\_Request\_Http**

<span class="ooclass"> class **Yaf\_Request\_Http** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Request\_Abstract** </span> {

/\* 属性 \*/

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">get</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> \[, <span
class="methodparam"><span class="type">string</span> `$default`</span>
\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getCookie</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getFiles</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getPost</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getQuery</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getRaw</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getRequest</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isXmlHttpRequest</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Request\_Abstract::clearParams</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getActionName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getBaseUri</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span
class="methodname">Yaf\_Request\_Abstract::getControllerName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getEnv</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getException</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getLanguage</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getMethod</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getModuleName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getParam</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getParams</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getRequestUri</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getServer</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$default`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isCli</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isDispatched</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isGet</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isHead</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isOptions</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isPost</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isPut</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isRouted</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isXmlHttpRequest</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setActionName</span> (
<span class="methodparam"><span class="type">string</span>
`$action`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setBaseUri</span> (
<span class="methodparam"><span class="type">string</span> `$uir`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span
class="methodname">Yaf\_Request\_Abstract::setControllerName</span> (
<span class="methodparam"><span class="type">string</span>
`$controller`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setDispatched</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setModuleName</span> (
<span class="methodparam"><span class="type">string</span>
`$module`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setParam</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setRequestUri</span> (
<span class="methodparam"><span class="type">string</span> `$uir`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setRouted</span> (\[
<span class="methodparam"><span class="type">string</span>
`$flag`</span> \] )

}

属性
----

`module`  

`controller`  

`action`  

`method`  

`params`  

`language`  

`_exception`  

`_base_uri`  

`uri`  

`dispatched`  

`routed`  

Yaf\_Request\_Http::\_\_construct
=================================

The \_\_construct purpose

### 说明

<span class="methodname">Yaf\_Request\_Http::\_\_construct</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Http::get
=======================

从客户端返回变量

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Yaf\_Request\_Http::get</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

从客户端返回变量，这个方法将从请求参数中寻找参数`name`，如果没有找到的话，将从POST,
GET, Cookie, Server中寻找

### 参数

`name`  
the variable name

`default`  
如果提供了此参数，当变量在未被找到的情况下，它将被返回

### 返回值

### 参见

-   <span class="classname">Yaf\_Request\_Http::getQuery</span>
-   <span class="classname">Yaf\_Request\_Http::getPost</span>
-   <span class="classname">Yaf\_Request\_Http::getCookie</span>
-   <span class="classname">Yaf\_Request\_Http::getServer</span>
-   <span class="classname">Yaf\_Request\_Http::getParam</span>

Yaf\_Request\_Http::getCookie
=============================

返回Cookie变量

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Yaf\_Request\_Http::getCookie</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

返回Cookie变量

### 参数

`name`  
the cookie name

`default`  
如果提供了此参数，当变量在未被找到的情况下，提供的参数将被返回

### 返回值

### 参见

-   <span class="classname">Yaf\_Request\_Http::get</span>
-   <span class="classname">Yaf\_Request\_Http::getQuery</span>
-   <span class="classname">Yaf\_Request\_Http::getPost</span>
-   <span class="classname">Yaf\_Request\_Http::getServer</span>
-   <span class="classname">Yaf\_Request\_Http::getParam</span>

Yaf\_Request\_Http::getFiles
============================

The getFiles purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Http::getFiles</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Http::getPost
===========================

返回POST变量

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Yaf\_Request\_Http::getPost</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

返回POST变量

### 参数

`name`  
the variable name

`default`  
如果提供了此参数，当变量在未被找到的情况下，提供的参数将被返回

### 返回值

### 参见

-   <span class="classname">Yaf\_Request\_Http::get</span>
-   <span class="classname">Yaf\_Request\_Http::getQuery</span>
-   <span class="classname">Yaf\_Request\_Http::getCookie</span>
-   <span class="classname">Yaf\_Request\_Http::getServer</span>
-   <span class="classname">Yaf\_Request\_Http::getParam</span>

Yaf\_Request\_Http::getQuery
============================

fetch a query parameter

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Yaf\_Request\_Http::getQuery</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

返回Get变量

### 参数

`name`  
the variable name

`default`  
如果提供了此参数，当变量在未被找到的情况下，提供的参数将被返回

### 返回值

### 参见

-   <span class="classname">Yaf\_Request\_Http::get</span>
-   <span class="classname">Yaf\_Request\_Http::getPost</span>
-   <span class="classname">Yaf\_Request\_Http::getCookie</span>
-   <span class="classname">Yaf\_Request\_Http::getServer</span>
-   <span class="classname">Yaf\_Request\_Http::getParam</span>

Yaf\_Request\_Http::getRaw
==========================

Retrieve Raw request body

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Yaf\_Request\_Http::getRaw</span> ( <span
class="methodparam">void</span> )

Retrieve Raw request body

### 参数

此函数没有参数。

### 返回值

Return string on success, FALSE on failure.

### 参见

-   <span class="methodname">Yaf\_Request\_Http::get</span>
-   <span class="methodname">Yaf\_Request\_Http::getPost</span>
-   <span class="methodname">Yaf\_Request\_Http::getCookie</span>
-   <span class="methodname">Yaf\_Request\_Http::getQuery</span>
-   <span class="methodname">Yaf\_Request\_Abstract::getServer</span>
-   <span class="methodname">Yaf\_Request\_Abstract::getParam</span>

Yaf\_Request\_Http::getRequest
==============================

The getRequest purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Http::getRequest</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Http::isXmlHttpRequest
====================================

是否为Ajax请求

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Request\_Http::isXmlHttpRequest</span> (
<span class="methodparam">void</span> )

检查请求是否是Ajax请求

> **Note**:
>
> 这个方法取决于请求报头：HTTP\_X\_REQUESTED\_WITH，一些Javascript库在做Ajax请求时候不设置这个报文头。

### 参数

此函数没有参数。

### 返回值

简介
----

<span class="classname">Yaf\_Request\_Simple</span>
特别的被用于测试。例如：CLI模式下模拟一些特殊的要求

类摘要
------

**Yaf\_Request\_Simple**

<span class="ooclass"> class **Yaf\_Request\_Simple** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Request\_Abstract** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">string</span>
`Yaf_Request_Simple::SCHEME_HTTP` <span class="initializer"> =
http</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`Yaf_Request_Simple::SCHEME_HTTPS` <span class="initializer"> =
https</span> ;

/\* 属性 \*/

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">get</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getCookie</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getFiles</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getPost</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getQuery</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getRequest</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isXmlHttpRequest</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Request\_Abstract::clearParams</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getActionName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getBaseUri</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span
class="methodname">Yaf\_Request\_Abstract::getControllerName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getEnv</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getException</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getLanguage</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getMethod</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getModuleName</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getParam</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$default`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getParams</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getRequestUri</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::getServer</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$default`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isCli</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isDispatched</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isGet</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isHead</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isOptions</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isPost</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isPut</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isRouted</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::isXmlHttpRequest</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setActionName</span> (
<span class="methodparam"><span class="type">string</span>
`$action`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setBaseUri</span> (
<span class="methodparam"><span class="type">string</span> `$uir`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span
class="methodname">Yaf\_Request\_Abstract::setControllerName</span> (
<span class="methodparam"><span class="type">string</span>
`$controller`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setDispatched</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setModuleName</span> (
<span class="methodparam"><span class="type">string</span>
`$module`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setParam</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setRequestUri</span> (
<span class="methodparam"><span class="type">string</span> `$uir`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Abstract::setRouted</span> (\[
<span class="methodparam"><span class="type">string</span>
`$flag`</span> \] )

}

属性
----

`module`  

`controller`  

`action`  

`method`  

`params`  

`language`  

`_exception`  

`_base_uri`  

`uri`  

`dispatched`  

`routed`  

预定义常量
----------

**`Yaf_Request_Simple::SCHEME_HTTP`**  

**`Yaf_Request_Simple::SCHEME_HTTPS`**  

Yaf\_Request\_Simple::\_\_construct
===================================

The \_\_construct purpose

### 说明

<span class="methodname">Yaf\_Request\_Simple::\_\_construct</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Simple::get
=========================

The get purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Simple::get</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Simple::getCookie
===============================

The getCookie purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Simple::getCookie</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Simple::getFiles
==============================

The getFiles purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Simple::getFiles</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Simple::getPost
=============================

The getPost purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Simple::getPost</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Simple::getQuery
==============================

The getQuery purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Simple::getQuery</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Simple::getRequest
================================

The getRequest purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Simple::getRequest</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Request\_Simple::isXmlHttpRequest
======================================

The isXmlHttpRequest purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Request\_Simple::isXmlHttpRequest</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

类摘要
------

**Yaf\_Response\_Abstract**

<span class="ooclass"> class **Yaf\_Response\_Abstract** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">string</span>
`Yaf_Response_Abstract::DEFAULT_BODY` <span class="initializer"> =
"content"</span> ;

/\* 属性 \*/

<span class="modifier">protected</span> `$_header` ;

<span class="modifier">protected</span> `$_body` ;

<span class="modifier">protected</span> `$_sendheader` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">appendBody</span> ( <span
class="methodparam"><span class="type">string</span> `$content`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$key`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">clearBody</span> (\[ <span
class="methodparam"><span class="type">string</span> `$key`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clearHeaders</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getBody</span> (\[ <span
class="methodparam"><span class="type">string</span> `$key`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getHeader</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">prependBody</span> ( <span
class="methodparam"><span class="type">string</span> `$content`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$key`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">response</span> ( <span
class="methodparam">void</span> )

<span class="modifier">protected</span> <span class="type">void</span>
<span class="methodname">setAllHeaders</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setBody</span> ( <span
class="methodparam"><span class="type">string</span> `$content`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$key`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setHeader</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setRedirect</span> ( <span
class="methodparam">void</span> )

<span class="modifier">private</span> <span class="type">void</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

属性
----

`_header`  

`_body`  

`_sendheader`  

Yaf\_Response\_Abstract::appendBody
===================================

往已有的响应body后附加新的内容

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Response\_Abstract::appendBody</span> (
<span class="methodparam"><span class="type">string</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">string</span> `$key`</span> \] )

往已有的响应body后附加新的内容

### 参数

`body`  
content string

`key`  
响应内容的key，你可以设置一个键值对，如果你没有具体的设置的话，系统默认使用Yaf\_Response\_Abstract::DEFAULT\_BODY

> **Note**:
>
> this parameter is introduced as of 2.2.0

### 返回值

bool

### 范例

**示例 \#1 <span
class="function">Yaf\_Response\_Abstract::appendBody</span>example**

``` php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Hello")->prependBody(" World");

echo $response;
?>
```

以上例程的输出类似于：

    Hello World

### 参见

-   <span class="classname">Yaf\_Config\_Ini</span>

### 参见

-   <span class="methodname">Yaf\_Response\_Abstract::getBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::setBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::prependBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::clearBody</span>

Yaf\_Response\_Abstract::clearBody
==================================

清除已经设置的响应body

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Response\_Abstract::clearBody</span> (\[
<span class="methodparam"><span class="type">string</span> `$key`</span>
\] )

清除已经设置的响应body

### 参数

`key`  
the content key, if you don't specific, then all contents will be
cleared. 如果你没选择具体清除哪个key所对应的内容，那所有内容将被清除

> **Note**:
>
> this parameter is introduced as of 2.2.0

### 返回值

### 参见

-   <span class="methodname">Yaf\_Response\_Abstract::setBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::appendBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::prependBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::getBody</span>

Yaf\_Response\_Abstract::clearHeaders
=====================================

The clearHeaders purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Response\_Abstract::clearHeaders</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Response\_Abstract::\_\_construct
======================================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">Yaf\_Response\_Abstract::\_\_construct</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Response\_Abstract::\_\_destruct
=====================================

The \_\_destruct purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Response\_Abstract::\_\_destruct</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Response\_Abstract::getBody
================================

获取已经设置的响应body

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Yaf\_Response\_Abstract::getBody</span> (\[
<span class="methodparam"><span class="type">string</span> `$key`</span>
\] )

获取已经设置的响应body

### 参数

`key`  
body所对应的key，如果你没指定key，系统默认使用Yaf\_Response\_Abstract::DEFAULT\_BODY。如果你传入一个NULL，所有的内容将会以数组形式被返回。

> **Note**:
>
> this parameter is introduced as of 2.2.0

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Response\_Abstract::getBody</span>example**

``` php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Hello")->setBody(" World", "footer");

var_dump($response->getBody()); //default 
var_dump($response->getBody(Yaf_Response_Abstract::DEFAULT_BODY)); //same as above
var_dump($response->getBody("footer"));
var_dump($response->getBody(NULL)); //get all
?>
```

以上例程的输出类似于：

    string(5) "Hello"
    string(5) "Hello"
    string(6) " World"
    array(2) {
      ["content"]=>
      string(5) "Hello"
      ["footer"]=>
      string(6) " World"
    }

### 参见

-   <span class="methodname">Yaf\_Response\_Abstract::setBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::appendBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::prependBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::clearBody</span>

Yaf\_Response\_Abstract::getHeader
==================================

The getHeader purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Response\_Abstract::getHeader</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Response\_Abstract::prependBody
====================================

The prependBody purpose

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Response\_Abstract::prependBody</span> (
<span class="methodparam"><span class="type">string</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">string</span> `$key`</span> \] )

往已有的响应body前插入新的内容

### 参数

`body`  
content string

`key`  
body所对应的key，你可以设置一个body的键值对，如果你没有指定key，系统默认使用Yaf\_Response\_Abstract::DEFAULT\_BODY

> **Note**:
>
> this parameter is introduced as of 2.2.0

### 返回值

bool

### 范例

**示例 \#1 <span
class="function">Yaf\_Response\_Abstract::prependBody</span>example**

``` php
<?php
$response = new Yaf_Response_Http();

$response->setBody("World")->prependBody("Hello ");

echo $response;
?>
```

以上例程的输出类似于：

    Hello World

### 参见

-   <span class="methodname">Yaf\_Response\_Abstract::getBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::setBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::appendBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::clearBody</span>

Yaf\_Response\_Abstract::response
=================================

send response

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Response\_Abstract::response</span> (
<span class="methodparam">void</span> )

send response

### 参数

此函数没有参数。

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Response\_Abstract::response</span>example**

``` php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Hello")->setBody(" World", "footer");

$response->response();
?>
```

以上例程的输出类似于：

    Hello World

### 参见

-   <span class="methodname">Yaf\_Response\_Abstract::setBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::clearBody</span>

Yaf\_Response\_Abstract::setAllHeaders
======================================

The setAllHeaders purpose

### 说明

<span class="modifier">protected</span> <span class="type">void</span>
<span class="methodname">Yaf\_Response\_Abstract::setAllHeaders</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Response\_Abstract::setBody
================================

设置响应的Body

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Response\_Abstract::setBody</span> ( <span
class="methodparam"><span class="type">string</span> `$content`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$key`</span> \] )

设置响应的Body

### 参数

`body`  
content string

`key`  
body所对应的key，你可以设置一个body的键值对，如果你没有指定key，系统默认使用Yaf\_Response\_Abstract::DEFAULT\_BODY

> **Note**:
>
> this parameter is introduced as of 2.2.0

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Response\_Abstract::setBody</span>example**

``` php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Hello")->setBody(" World", "footer");

print_r($response);
echo $response;
?>
```

以上例程的输出类似于：

    Yaf_Response_Http Object
    (
        [_header:protected] => Array
            (
            )

        [_body:protected] => Array
            (
                [content] => Hello
                [footer] =>  World
            )

        [_sendheader:protected] => 1
        [_response_code:protected] => 200
    )
    Hello World

### 参见

-   <span class="methodname">Yaf\_Response\_Abstract::getBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::appendBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::prependBody</span>
-   <span class="methodname">Yaf\_Response\_Abstract::clearBody</span>

Yaf\_Response\_Abstract::setHeader
==================================

The setHeader purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Response\_Abstract::setHeader</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Response\_Abstract::setRedirect
====================================

The setRedirect purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Response\_Abstract::setRedirect</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Response\_Abstract::\_\_toString
=====================================

The \_\_toString purpose

### 说明

<span class="modifier">private</span> <span class="type">void</span>
<span class="methodname">Yaf\_Response\_Abstract::\_\_toString</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

<span
class="classname">Yaf\_Route\_Interface</span>是Yaf路由协议的标准接口,
它的存在使得用户可以自定义路由协议

类摘要
------

**Yaf\_Route\_Interface**

<span class="ooclass"> class **Yaf\_Route\_Interface** </span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">assemble</span> ( <span class="methodparam"><span
class="type">array</span> `$info`</span> \[, <span
class="methodparam"><span class="type">array</span> `$query`</span> \] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">route</span> ( <span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> )

}

Yaf\_Route\_Interface::assemble
===============================

将指定路由规则组合成一个url

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">Yaf\_Route\_Interface::assemble</span> ( <span
class="methodparam"><span class="type">array</span> `$info`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

这个方法会将指定的参数加上自定义的参数组合成一个url

所有route必须结合其路由规则来实现这个方法

### 参数

`info`  

`query`  

### 返回值

Yaf\_Route\_Interface::route
============================

route a request

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">Yaf\_Route\_Interface::route</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> )

<span class="methodname">Yaf\_Route\_Interface::route</span>
是用户自定义路由唯一需要实现的方法。

如果这个方法返回TRUE，那么路由进程将会中止。否则，<span
class="classname">Yaf\_Router</span>
将会调用路由堆栈中的下一个路由来路由请求。

这个方法会设置路由的结果给参数请求，通过调用 <span
class="methodname">Yaf\_Request\_Abstract::setControllerName</span>，
<span class="methodname">Yaf\_Request\_Abstract::setActionName</span> 和
<span class="methodname">Yaf\_Request\_Abstract::setModuleName</span>

这个方法也需要调用 <span
class="methodname">Yaf\_Request\_Abstract::setRouted</span>做最后的请求路由。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  
A <span class="classname">Yaf\_Request\_Abstract</span> instance.

### 返回值

简介
----

类摘要
------

**Yaf\_Route\_Map**

<span class="ooclass"> class **Yaf\_Route\_Map** </span> <span
class="oointerface">implements <span
class="interfacename">Yaf\_Route\_Interface</span> </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_ctl_router` ;

<span class="modifier">protected</span> `$_delimeter` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">assemble</span> ( <span class="methodparam">
<span class="type">array</span> `$info` </span> \[, <span
class="methodparam"> <span class="type">array</span> `$query` </span> \]
)

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$controller_prefer`<span class="initializer"> = false</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`$delimiter`<span class="initializer"> = ''</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">route</span> ( <span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> )

}

属性
----

`_ctl_router`  

`_delimeter`  

Yaf\_Route\_Map::assemble
=========================

组合url

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Route\_Map::assemble</span> ( <span
class="methodparam"> <span class="type">array</span> `$info` </span> \[,
<span class="methodparam"> <span class="type">array</span> `$query`
</span> \] )

根据指定参数和自定义参数将map这个route组合成一个url

### 参数

`info`  
需要传入一个数组，数组的key可以为:a或者:c，:a表示action，:c表示controller。

当map
route初始化时，controller\_prefer为false时，这个参数需要传入:c。当controller\_prefer
为true时，这个参数需要传入:a。

`query`  
用户自定义的query string，将根据此路由规则拼接在url中

### 范例

**示例 \#1 <span
class="function">Yaf\_Route\_Map::assemble</span>example**

``` php
<?php

$router = new Yaf_Router();

$route  = new Yaf_Route_Map();

$router->addRoute("map", $route);

var_dump($router->getRoute('map')->assemble(
                        array(
                                ':c' => 'foo_bar'
                        ),
                        array(
                                'tkey1' => 'tval1',
                                'tkey2' => 'tval2'
                        )
                   )
);

$route = new Yaf_Route_Map(true, '_');
$router->addRoute("map", $route);

var_dump($router->getRoute('map')->assemble(
                        array(
                                ':a' => 'foo_bar'
                        ),
                        array(
                                'tkey1' => 'tval1',
                                'tkey2' => 'tval2'
                        )
                   )
);
```

以上例程的输出类似于：

    string(%d) "/foo/bar?tkey1=tval1&tkey2=tval2"
    string(%d) "/foo/bar/_/tkey1/tval1/tkey2/tval2"

### 返回值

Yaf\_Route\_Map::\_\_construct
==============================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">Yaf\_Route\_Map::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$controller_prefer`<span class="initializer"> = false</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`$delimiter`<span class="initializer"> = ''</span></span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`controller_prefer`  
结果是否应该考虑作为controller或action

`delimiter`  

### 返回值

### 范例

**示例 \#1 <span class="function">Yaf\_Route\_Map</span>example**

``` php
<?php
   /**
    * Add a map route to Yaf_Router route stack
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_Map());
?>
```

以上例程的输出类似于：

    /* for http://yourdomain.com/product/foo/bar
     * route will result in following values:
     */
    array(
      "controller" => "product_foo_bar",
    )

**示例 \#2 <span class="function">Yaf\_Route\_Map</span>example**

``` php
<?php
   /**
    * Add a map route to Yaf_Router route stack
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_Map(true, "_"));
?>
```

以上例程的输出类似于：

    /* for http://yourdomain.com/user/list/_/foo/22
     * route will result in following values:
     */
    array(
        "action" => "user_list",
    )

    /**
     * and request parameters:
     */
    array(
      "foo"   => 22,
    )

**示例 \#3 <span class="function">Yaf\_Route\_Map</span>example**

``` php
<?php
   /**
    * Add a map route to Yaf_Router route stack by calling addconfig
    */
    $config = array(
        "name" => array(
           "type"  => "map",         //Yaf_Route_Map route
           "controllerPrefer" => FALSE,
           "delimiter"        => "#!", 
           ),
    );
    Yaf_Dispatcher::getInstance()->getRouter()->addConfig(
        new Yaf_Config_Simple($config));
?>
```

### 参见

-   <span class="methodname">Yaf\_Router::addRoute</span>
-   <span class="classname">Yaf\_Route\_Static</span>
-   <span class="classname">Yaf\_Route\_Supervar</span>
-   <span class="classname">Yaf\_Route\_Simple</span>
-   <span class="classname">Yaf\_Route\_Regex</span>
-   <span class="classname">Yaf\_Route\_Rewrite</span>

Yaf\_Route\_Map::route
======================

The route purpose

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Route\_Map::route</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  

### 返回值

简介
----

<span class="classname">Yaf\_Route\_Regex</span>
是Yaf内置的路由中最灵活的。

类摘要
------

**Yaf\_Route\_Regex**

<span class="ooclass"> class **Yaf\_Route\_Regex** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Route\_Interface** </span> <span class="oointerface">implements
<span class="interfacename">Yaf\_Route\_Interface</span> </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_route` ;

<span class="modifier">protected</span> `$_default` ;

<span class="modifier">protected</span> `$_maps` ;

<span class="modifier">protected</span> `$_verify` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">assemble</span> ( <span
class="methodparam"><span class="type">array</span> `$info`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$match`</span> ,
<span class="methodparam"><span class="type">array</span>
`$route`</span> \[, <span class="methodparam"><span
class="type">array</span> `$map`</span> \[, <span
class="methodparam"><span class="type">array</span> `$verify`</span>
\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">route</span> ( <span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> )

/\* 继承的方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">Yaf\_Route\_Interface::assemble</span> ( <span
class="methodparam"><span class="type">array</span> `$info`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">Yaf\_Route\_Interface::route</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> )

}

属性
----

`_route`  

`_default`  

`_maps`  

`_verify`  

Yaf\_Route\_Regex::assemble
===========================

组合url

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Route\_Regex::assemble</span> ( <span
class="methodparam"><span class="type">array</span> `$info`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

根据指定参数和自定义参数将regex这个route组合成一个url

在regex
route使用assemble需要在初始化时指定reverse参数，否则将不能正常工作

### 参数

`info`  
需要传入一个数组，数组的key可以为:a、:c、:m，:a表示action，:c表示controller，:m表示module。

`query`  
用户自定义的query string，将根据此路由规则拼接在url中

### 范例

**示例 \#1 <span
class="function">Yaf\_Route\_Regex::assemble</span>example**

``` php
<?php

$router = new Yaf_Router();

$route  = new Yaf_Route_Regex(
            "#^/product/([^/]+)/([^/])+#",
            array(
                'controller' => "product",  //route to product controller,
                ),
            array(),
            array(),
            '/:m/:c/:a'
        );

$router->addRoute("regex", $route);

var_dump($router->getRoute('regex')->assemble(
            array(
                ':m' => 'module',
                ':c' => 'controller',
                ':a' => 'action'
                ),
            array(
                'tkey1' => 'tval1',
                'tkey2' =>
                'tval2'
                )
            )
        );
```

以上例程的输出类似于：

    string(49) "/module/controller/action?tkey1=tval1&tkey2=tval2"

### 返回值

Yaf\_Route\_Regex::\_\_construct
================================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">Yaf\_Route\_Regex::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$match`</span> ,
<span class="methodparam"><span class="type">array</span>
`$route`</span> \[, <span class="methodparam"><span
class="type">array</span> `$map`</span> \[, <span
class="methodparam"><span class="type">array</span> `$verify`</span>
\]\] )

### 参数

`match`  
一个完整的正则表达式，用来匹配一个请求的uri，如果不能匹配，<span
class="classname">Yaf\_Route\_Regex</span> 将返回FALSE。

`route`  
当路由正则匹配成功请求uri时，<span
class="classname">Yaf\_Route\_Regex</span>将会用它来决定哪一个m/c/a被路由。

在这个数组中无论是m/c/a都是最优的，如果你没有提供一个明确的值，它将会以默认方式被路由。
另外, 你也可以使用map的结果作为m/c/a的结果.

`map`  
将匹配到的结果捕捉放到一个已经命名好的数组中。

`verify`  

### 返回值

### 范例

**示例 \#1 <span class="function">Yaf\_Route\_Regex</span>example**

``` php
<?php
   /**
    * Add a regex route to Yaf_Router route stack
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_Regex(
           "#^/product/([^/]+)/([^/])+#", //match request uri leading "/product"
           array(
               'controller' => "product",  //route to product controller,
           ),
           array(
              1 => "name",   // now you can call $request->getParam("name")
              2 => "id",     // to get the first captrue in the match pattern.
           )
        )
    );
?>
```

**示例 \#2 <span class="function">Yaf\_Route\_Regex(as of
2.3.0)</span>example**

``` php
<?php
   /**
    *  使用动态的controller
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_Regex(
           "#^/product/([^/]+)/([^/])+#", //match request uri leading "/product"
           array(
              'controller' => ":name",  //使用上面匹配的:name, 也就是$1作为controller
           ),
           array(
              1 => "name",   // now you can call $request->getParam("name")
              2 => "id",     // to get the first captrue in the match pattern.
           )
        )
    );
?>
```

**示例 \#3 <span class="function">Yaf\_Route\_Regex</span>example**

``` php
<?php
   /**
    * Add a regex route to Yaf_Router route stack by calling addconfig
    */
    $config = array(
        "name" => array(
           "type"  => "regex",          //Yaf_Route_Regex route
           "match" => "#(.*)#",         //match arbitrary request uri
           "route" => array(
               'controller' => "product",  //route to product controller,
               'action'     => "dummy",    //route to dummy action
           ),
           "map" => array(
              1 => "uri",   // now you can call $request->getParam("uri")
           ),
        ),
    );
    Yaf_Dispatcher::getInstance()->getRouter()->addConfig(
        new Yaf_Config_Simple($config));
?>
```

### 参见

-   <span class="methodname">Yaf\_Router::addRoute</span>
-   <span class="methodname">Yaf\_Router::addConfig</span>
-   <span class="classname">Yaf\_Route\_Static</span>
-   <span class="classname">Yaf\_Route\_Supervar</span>
-   <span class="classname">Yaf\_Route\_Simple</span>
-   <span class="classname">Yaf\_Route\_Rewrite</span>
-   <span class="classname">Yaf\_Route\_Map</span>

Yaf\_Route\_Regex::route
========================

The route purpose

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Route\_Regex::route</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> )

路由一个传进来的请求。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  

### 返回值

如果正则表达式是 <span
class="methodname">Yaf\_Route\_Regex::\_construct</span>的第一个参数，并且匹配了请求uri，返回TRUE，否则返回FALSE。

简介
----

类摘要
------

**Yaf\_Route\_Rewrite**

<span class="ooclass"> class **Yaf\_Route\_Rewrite** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Route\_Interface** </span> <span class="oointerface">implements
<span class="interfacename">Yaf\_Route\_Interface</span> </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_route` ;

<span class="modifier">protected</span> `$_default` ;

<span class="modifier">protected</span> `$_verify` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">assemble</span> ( <span
class="methodparam"><span class="type">array</span> `$info`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$match`</span> ,
<span class="methodparam"><span class="type">array</span>
`$route`</span> \[, <span class="methodparam"><span
class="type">array</span> `$verify`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">route</span> ( <span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> )

/\* 继承的方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">Yaf\_Route\_Interface::assemble</span> ( <span
class="methodparam"><span class="type">array</span> `$info`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">Yaf\_Route\_Interface::route</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> )

}

属性
----

`_route`  

`_default`  

`_verify`  

Yaf\_Route\_Rewrite::assemble
=============================

组合url

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Route\_Rewrite::assemble</span> ( <span
class="methodparam"><span class="type">array</span> `$info`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

根据指定参数和自定义参数将rewrite这个route组合成一个url

### 参数

`info`  
需要传入一个数组，数组中每个key必须和初始化rewrite
route时$match参数中的带冒号的参数名一致

`query`  
用户自定义的query string，将根据此路由规则拼接在url中

### 范例

**示例 \#1 <span
class="function">Yaf\_Route\_Rewrite::assemble</span>example**

``` php
router = new Yaf_Router();

$route  = new Yaf_Route_Rewrite(
                "/product/:name/:id/*",
                array(
                        'controller' => "product",
                ),
                array()
);

$router->addRoute("rewrite", $route);

var_dump($router->getRoute('rewrite')->assemble(
                        array(
                                ':name' => 'foo',
                                ':id' => 'bar',
                                ':tmpkey1' => 'tmpval1'
                        ),
                        array(
                                'tkey1' => 'tval1',
                                'tkey2' => 'tval2'
                             )
                        )
);
```

以上例程的输出类似于：

    string(57) "/product/foo/bar/tmpkey1/tmpval1/?tkey1=tval1&tkey2=tval2"

### 返回值

Yaf\_Route\_Rewrite::\_\_construct
==================================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">Yaf\_Route\_Rewrite::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$match`</span> ,
<span class="methodparam"><span class="type">array</span>
`$route`</span> \[, <span class="methodparam"><span
class="type">array</span> `$verify`</span> \] )

### 参数

`match`  
一个类似正则表达式，会被用来匹配一个请求的uri，如果匹配失败，<span
class="classname">Yaf\_Route\_Rewrite</span> 会返回FALSE。

`route`  
当路由正则匹配成功请求uri时，<span
class="classname">Yaf\_Route\_Rewrite</span>
将会用它来决定哪一个m/c/a被路由。

在这个数组中无论是m/c/a都是最优的，如果你没有提供一个明确的值，它将会以默认方式被路由。

`verify`  

### 返回值

### 范例

**示例 \#1 <span class="function">Yaf\_Route\_Rewrite</span>example**

``` php
<?php
   /**
    * Add a rewrite route to Yaf_Router route stack
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_rewrite(
           "/product/:name/:id/*", //match request uri leading "/product"
           array(
               'controller' => "product",  //route to product controller,
           ),
        )
    );
?>
```

以上例程的输出类似于：

    /* for http://yourdomain.com/product/foo/22/foo/bar
     * route will result in following values:
     */
    array(
      "controller" => "product",
      "module"     => "index", //(default)
      "action"     => "index", //(default)
    )

    /**
     * and request parameters:
     */
    array(
      "name" => "foo",
      "id"   => 22,
      "foo"  => bar
    )

**示例 \#2 <span class="function">Yaf\_Route\_Rewrite</span>example**

``` php
<?php
   /**
    * Add a rewrite route to Yaf_Router route stack by calling addconfig
    */
    $config = array(
        "name" => array(
           "type"  => "rewrite",        //Yaf_Route_Rewrite route
           "match" => "/user-list/:id", //match only /user/list/?/
           "route" => array(
               'controller' => "user",  //route to user controller,
               'action'     => "list",  //route to list action
           ),
        ),
    );
    Yaf_Dispatcher::getInstance()->getRouter()->addConfig(
        new Yaf_Config_Simple($config));
?>
```

以上例程的输出类似于：

    /* for http://yourdomain.com/user-list/22
     * route will result in following values:
     */
    array(
      "controller" => "user",
      "action"     => "list",
      "module"     => "index", //(default)
    )

    /**
     * and request parameters:
     */
    array(
      "id"   => 22,
    )

**示例 \#3 <span class="function">Yaf\_Route\_Rewrite(as of
2.3.0)</span>example**

``` php
<?php
   /**
    * 使用动态结果作为action名
    */
    $config = array(
        "name" => array(
           "type"  => "rewrite",        //Yaf_Route_Rewrite route
           "match" => "/user-list/:a/:id", //match only /user-list/开头的
           "route" => array(
               'controller' => "user",  //route to user controller,
               'action'     => ":a",  //使用动态的action
           ),
        ),
    );
    Yaf_Dispatcher::getInstance()->getRouter()->addConfig(
        new Yaf_Config_Simple($config));
?>
```

以上例程的输出类似于：

    /* for http://yourdomain.com/user-list/list/22
     * route will result in following values:
     */
    array(
      "controller" => "user",
      "action"     => "list",
      "module"     => "index", //(default)
    )

    /**
     * and request parameters:
     */
    array(
      "id"   => 22,
    )

### 参见

-   <span class="methodname">Yaf\_Router::addRoute</span>
-   <span class="methodname">Yaf\_Router::addConfig</span>
-   <span class="classname">Yaf\_Route\_Static</span>
-   <span class="classname">Yaf\_Route\_Supervar</span>
-   <span class="classname">Yaf\_Route\_Simple</span>
-   <span class="classname">Yaf\_Route\_Regex</span>
-   <span class="classname">Yaf\_Route\_Map</span>

Yaf\_Route\_Rewrite::route
==========================

The route purpose

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Route\_Rewrite::route</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  

### 返回值

简介
----

<span
class="classname">Yaf\_Router</span>是标准的框架路由.路由是一个拿到URI端点（URL中的URI的一部分）然后分解参数得到哪一个module,
controller, 和action需要接受请求。module, controller,
和action，还有一些其他的参数是打包在一个<span
class="classname">Yaf\_Request\_Abstract</span>的对象中，然后通过<span
class="classname">Yaf\_Dispatcher</span>来处理的。路由只发生一次:最初接到请求并且在第一个controller分发之前。
<span class="classname">Yaf\_Router</span>
是设计来允许使用纯PHP结构的类似功能模块的跳转。它非常松散的基于Ruby on
Rails的路由，并且不需要你提前就知道webserver
URL跳转的相关知识。它是设计来处理一个Apache 跳转模块的规则（一个） <span
class="classname">Yaf\_Router</span>是设计来允许mod\_rewrite

**示例 \#1 Apache的跳转规则**

``` conf
RewriteEngine on
RewriteRule !\.(js|ico|gif|jpg|png|css|html)$ index.php
```

or (preferred):

**示例 \#2 Apache的跳转规则**

``` conf
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} -s [OR]
RewriteCond %{REQUEST_FILENAME} -l [OR]
RewriteCond %{REQUEST_FILENAME} -d
RewriteRule ^.*$ - [NC,L]
RewriteRule ^.*$ index.php [NC,L]
```

如果使用Lighttpd，下面的跳转规则是有效的：

**示例 \#3 Lighttpd的跳转规则**

``` conf
url.rewrite-once = (
  ".*\?(.*)$" => "/index.php?$1",
  ".*\.(js|ico|gif|jpg|png|css|html)$" => "$0",
  "" => "/index.php"
)
```

如果使用Nginx，下面的跳转规则是有效的：

**示例 \#4 Nginx的跳转规则**

``` conf
server {
  listen ****;
  server_name  yourdomain.com;
  root   document_root;
  index  index.php index.html;

  if (!-e $request_filename) {
    rewrite ^/(.*)  /index.php/$1 last;
  }
}
```

默认路由
--------

Yaf\_Router预设了一个默认路由，它将以controller/action的形式匹配URIs。此外，一个module的名字可以被指定为第一路径元素，允许URIs设置为module/controller/action的形式。最后，它也会匹配一些URI中额外附加的参数，默认形式是controller/action/var1/value1/var2/value2。

> **Note**:
>
> Module的名字必须要定义在配置中，就application.module="Index,Foo,Bar"而言，在这种情况下，仅仅index,
> foo 和
> bar能被考虑作为为一个module的名称。如果没有在配置文件中定义，那么Yaf使用默认的module名字“Index”。

如何匹配这些路由的一些例子：

**示例 \#5 <span class="classname">Yaf\_Route\_Static</span>(default
route)example**

``` conf
// Assuming the following configure:
$conf = array(
   "application" => array(
      "modules" => "Index,Blog",
   ),
);

Controller only:
http://example/news
    controller == news
Action only(when defined yaf.action_prefer=1 in php.ini)
    action  == news
 
Invalid module maps to controller name:
http://example/foo
    controller == foo
 
Module + controller:
http://example/blog/archive
    module     == blog
    controller == archive
 
Module + controller + action:
http://example/blog/archive/list
    module     == blog
    controller == archive
    action     == list
 
Module + controller + action + params:
http://example/blog/archive/list/sort/alpha/date/desc
    module     == blog
    controller == archive
    action     == list
    sort       == alpha
    date       == desc
```

类摘要
------

**Yaf\_Router**

<span class="ooclass"> class **Yaf\_Router** </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_routes` ;

<span class="modifier">protected</span> `$_current` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addConfig</span> ( <span
class="methodparam"><span class="type">Yaf\_Config\_Abstract</span>
`$config`</span> )

<span class="modifier">public</span> <span
class="type">Yaf\_Router</span> <span class="methodname">addRoute</span>
( <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">Yaf\_Route\_Abstract</span> `$route`</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getCurrentRoute</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getRoute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getRoutes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">route</span> ( <span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> )

}

属性
----

`_routes`  

`_current`  

Yaf\_Router::addConfig
======================

向Router中添加配置文件中定义的路由

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Router::addConfig</span> ( <span
class="methodparam"><span class="type">Yaf\_Config\_Abstract</span>
`$config`</span> )

将application.ini中定义的路由规则添加到<span
class="classname">Yaf\_Router</span>的路由栈中

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

### 范例

**示例 \#1 <span class="function">application.ini</span>example**

``` ini
;the order is very important, the prior one will be called first

;a rewrite route match request /product/*/*
routes.route_name.type="rewrite"
routes.route_name.match="/product/:name/:value"
routes.route_name.route.controller=product
routes.route_name.route.action=info

;a regex route match request /list/*/*
routes.route_name1.type="regex"
routes.route_name1.match="#^list/([^/]*)/([^/]*)#"
routes.route_name1.route.controller=Index
routes.route_name1.route.action=action
routes.route_name1.map.1=name
routes.route_name1.map.2=value

;a simple route match /**?c=controller&a=action&m=module
routes.route_name2.type="simple"
routes.route_name2.controller=c
routes.route_name2.module=m
routes.route_name2.action=a

;a simple router match /**?r=PATH_INFO
routes.route_name3.type="supervar"
routes.route_name3.varname=r

;a map route match any request to controller
routes.route_name4.type="map"
routes.route_name4.controllerPrefer=TRUE
routes.route_namer.delimiter="#!"
```

**示例 \#2 <span
class="function">Yaf\_Dispatcher::autoConfig</span>example**

``` php
<?php
class Bootstrap extends Yaf_Bootstrap_Abstract{
    public function _initConfig() {
        $config = Yaf_Application::app()->getConfig();
        Yaf_Registry::set("config", $config);
    }

    public function _initRoute(Yaf_Dispatcher $dispatcher) {
        $router = $dispatcher->getRouter();
        /**
         * we can add some pre-defined routes in application.ini
         */
        $router->addConfig(Yaf_Registry::get("config")->routes);
    }
?>
```

### 参见

-   <span class="methodname">Yaf\_Router::addRoute</span>
-   <span class="classname">Yaf\_Route\_Static</span>
-   <span class="classname">Yaf\_Route\_Supervar</span>
-   <span class="classname">Yaf\_Route\_Simple</span>
-   <span class="classname">Yaf\_Route\_Regex</span>
-   <span class="classname">Yaf\_Route\_Rewrite</span>
-   <span class="classname">Yaf\_Route\_Map</span>

Yaf\_Router::addRoute
=====================

往Router中添加新的路由

### 说明

<span class="modifier">public</span> <span
class="type">Yaf\_Router</span> <span
class="methodname">Yaf\_Router::addRoute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">Yaf\_Route\_Abstract</span>
`$route`</span> )

默认地，Yaf\_Router使用<span
class="classname">Yaf\_Route\_Static</span>作为它的默认的路由。你可以通过调用这个方法往Router的堆栈中添加一个新的路由

在路由栈中，新的路由规则会比老的规则先调用，如果新路由规则返回TRUE，那么路由进程将会结束。否则，老的规则将会被调用。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

### 范例

**示例 \#1 <span
class="function">Yaf\_Dispatcher::autoRender</span>example**

``` php
<?php
class Bootstrap extends Yaf_Bootstrap_Abstract{
    public function _initConfig() {
        $config = Yaf_Application::app()->getConfig();
        Yaf_Registry::set("config", $config);
    }

    public function _initRoute(Yaf_Dispatcher $dispatcher) {
        $router = $dispatcher->getRouter();
        /**
         * we can add some pre-defined routes in application.ini
         */
        $router->addConfig(Yaf_Registry::get("config")->routes);
        /**
         * add a Rewrite route, then for a request uri: 
         * http://***/product/list/22/foo
         * will be matched by this route, and result:
         *
         *  [module] => 
         *  [controller] => product
         *  [action] => info
         *  [method] => GET
         *  [params:protected] => Array
         *      (
         *          [id] => 22
         *          [name] => foo
         *      )
         * 
         */
        $route  = new Yaf_Route_Rewrite(
            "/product/list/:id/:name",
            array(
                "controller" => "product",
                "action"     => "info",
            )
        ); 
        
        $router->addRoute('dummy', $route);
    }
?>
```

### 参见

-   <span class="methodname">Yaf\_Router::addConfig</span>
-   <span class="classname">Yaf\_Route\_Static</span>
-   <span class="classname">Yaf\_Route\_Supervar</span>
-   <span class="classname">Yaf\_Route\_Simple</span>
-   <span class="classname">Yaf\_Route\_Regex</span>
-   <span class="classname">Yaf\_Route\_Rewrite</span>
-   <span class="classname">Yaf\_Route\_Map</span>

Yaf\_Router::\_\_construct
==========================

Yaf\_Router constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">Yaf\_Router::\_\_construct</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Router::getCurrentRoute
============================

取得当前有效的路由名

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Router::getCurrentRoute</span> ( <span
class="methodparam">void</span> )

获取当前路由进程中正在起作用的路由名

> **Note**:
>
> 你需要在路由进程结束之后调用此方法，在这之前，这个方法会一直返回NULL

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

String，当前起效的路由的名字

### 范例

**示例 \#1 注册一些路由到Bootstrap**

``` php
<?php
class Bootstrap extends Yaf_Bootstrap_Abstract{
    public function _initConfig() {
        $config = Yaf_Application::app()->getConfig();
        Yaf_Registry::set("config", $config);
    }

    public function _initRoute(Yaf_Dispatcher $dispatcher) {
        $router = $dispatcher->getRouter();
        $rewrite_route  = new Yaf_Route_Rewrite(
            "/product/list/:page",
            array(
                "controller" => "product",
                "action"     => "list",
            )
        ); 

        $regex_route  = new Yaf_Route_Rewrite(
            "#^/product/info/(\d+)",
            array(
                "controller" => "product",
                "action"     => "info",
            )
        ); 
        
        $router->addRoute('rewrite', $rewrite_route)->addRoute('regex', $regex_route);
    } 

    /**
     * register plugin 
     */
    public function __initPlugins(Yaf_Dispatcher $dispatcher) {
        $dispatcher->registerPlugin(new DummyPlugin());
    }
?>
```

**示例 \#2 plugin Dummy.php (under
<a href="/yaf/appconfig.html#" class="link">application.directory</a>/plugins)**

``` php
<?php
class DummyPlugin extends Yaf_Plugin_Abstract {

    public function routerShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
         var_dump(Yaf_Dispatcher::getInstance()->getRouter()->getCurrentRoute());
    }
?>
?>
```

以上例程的输出类似于：

    /* for http://yourdomain.com/product/list/1
     * DummyPlugin will output:
     */
    string(7) "rewrite"

    /* for http://yourdomain.com/product/info/34
     * DummyPlugin will output:
     */
    string(5) "regex"

    /* for other request URI
     * DummyPlugin will output:
     */
    string(8) "_default"

### 参见

-   <span class="classname">Yaf\_Bootstrap\_Abstract</span>
-   <span class="classname">Yaf\_Plugin\_Abstract</span>
-   <span class="methodname">Yaf\_Router::addRoute</span>

Yaf\_Router::getRoute
=====================

The getRoute purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Router::getRoute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Router::getRoutes
======================

The getRoutes purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Router::getRoutes</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Router::route
==================

The route purpose

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Router::route</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

<span class="classname">Yaf\_Route\_Simple</span> 会匹配请求中的query
string，然后找到路由信息。

你需要做的只是告诉 <span
class="classname">Yaf\_Route\_Simple</span>，在$\_GET中哪个是Module，哪个是Controller，哪个是Action。

<span class="methodname">Yaf\_Route\_Simple::route</span>
总是会返回TRUE，所以把<span
class="classname">Yaf\_Route\_Simple</span>放在路由堆栈前面是很重要的，否则其他所有的路由都可能不会被调用到。

类摘要
------

**Yaf\_Route\_Simple**

<span class="ooclass"> class **Yaf\_Route\_Simple** </span> <span
class="oointerface">implements <span
class="interfacename">Yaf\_Route\_Interface</span> </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$controller` ;

<span class="modifier">protected</span> `$module` ;

<span class="modifier">protected</span> `$action` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">assemble</span> ( <span
class="methodparam"><span class="type">array</span> `$info`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$module_name`</span> , <span class="methodparam"><span
class="type">string</span> `$controller_name`</span> , <span
class="methodparam"><span class="type">string</span>
`$action_name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">route</span> ( <span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> )

}

属性
----

`controller`  

`module`  

`action`  

Yaf\_Route\_Simple::assemble
============================

组合url

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Route\_Simple::assemble</span> ( <span
class="methodparam"><span class="type">array</span> `$info`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

根据指定参数和自定义参数将simple这个route组合成一个url

### 参数

`info`  
需要传入一个数组，数组中每个key可为:m、:c、:a，:m代表module，:c代表controller,
:a代表action

`query`  
用户自定义的query string，将根据此路由规则拼接在url中

### 范例

**示例 \#1 <span
class="function">Yaf\_Route\_Simple::assemble</span>example**

``` php
<?php

$router = new Yaf_Router();

$route  = new Yaf_Route_Simple('m', 'c', 'a');

$router->addRoute("simple", $route);

var_dump($router->getRoute('simple')->assemble(
            array(
                ':a' => 'yafaction',
                'tkey' => 'tval',
                ':c' => 'yafcontroller',
                ':m' => 'yafmodule'
                ),
            array(
                'tkey1' => 'tval1',
                'tkey2' => 'tval2'
                )
            ));
```

以上例程的输出类似于：

    string(64) "?m=yafmodule&c=yafcontroller&a=yafaction&tkey1=tval1&tkey2=tval2"

### 返回值

Yaf\_Route\_Simple::\_\_construct
=================================

Yaf\_Route\_Simple constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">Yaf\_Route\_Simple::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$module_name`</span> , <span class="methodparam"><span
class="type">string</span> `$controller_name`</span> , <span
class="methodparam"><span class="type">string</span>
`$action_name`</span> )

<span class="classname">Yaf\_Route\_Simple</span>将从query
string中获得路由信息。这个构造函数的参数会被作为键到$\_GET中去寻找路由信息。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`module_name`  
module信息的键名。

`controller_name`  
controller信息的键名。

`action_name`  
action信息的键名。

### 返回值

总是返回TRUE

### 范例

**示例 \#1 <span
class="function">Yaf\_Route\_Simple::route</span>example**

``` php
<?php
   $route = new Yaf_Route_Simple("m", "controller", "act");
   Yaf_Router::getInstance()->addRoute("simple", $route);
?>
```

**示例 \#2 <span
class="function">Yaf\_Route\_Simple::route</span>example**

``` bash
Request: http://yourdomain.com/path/?controller=a&act=b
=> module = default(index), controller = a, action = b

Request: http://yourdomain.com/path
=> module = default(index), controller = default(index), action = default(index)
```

### 参见

-   <span class="methodname">Yaf\_Route\_Supervar::route</span>
-   <span class="methodname">Yaf\_Route\_Static::route</span>
-   <span class="methodname">Yaf\_Route\_Regex::route</span>
-   <span class="methodname">Yaf\_Route\_Rewrite::route</span>
-   <span class="methodname">Yaf\_Route\_Map::route</span>

Yaf\_Route\_Simple::route
=========================

Route a request

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Route\_Simple::route</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> )

see <span class="methodname">Yaf\_Route\_Simple::\_\_construct</span>

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  

### 返回值

always be TRUE

### 参见

-   <span class="methodname">Yaf\_Route\_Supervar::route</span>
-   <span class="methodname">Yaf\_Route\_Static::route</span>
-   <span class="methodname">Yaf\_Route\_Regex::route</span>
-   <span class="methodname">Yaf\_Route\_Rewrite::route</span>
-   <span class="methodname">Yaf\_Route\_Map::route</span>

简介
----

默认的，<span class="classname">Yaf\_Router</span> 只有一个<span
class="classname">Yaf\_Route\_Static</span> 作为它默认的路由

<span class="classname">Yaf\_Route\_Static</span> 旨在处理80%的要求。

请注意：实例化 <span class="classname">Yaf\_Route\_Static</span>
是没有必要的，也没必要将它加入<span
class="classname">Yaf\_Router</span>的路由堆栈，因为在<span
class="classname">Yaf\_Router</span>的路由堆栈中总是存在它的一个实例，并且总是在最后被调用。

类摘要
------

**Yaf\_Route\_Static**

<span class="ooclass"> class **Yaf\_Route\_Static** </span> <span
class="oointerface">implements <span
class="interfacename">Yaf\_Router</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">assemble</span> ( <span
class="methodparam"><span class="type">array</span> `$info`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">match</span> ( <span class="methodparam"><span
class="type">string</span> `$uri`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">route</span> ( <span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> )

}

Yaf\_Route\_Static::assemble
============================

组合url

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Route\_Static::assemble</span> ( <span
class="methodparam"><span class="type">array</span> `$info`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

根据指定参数和自定义参数将static这个route组合成一个url

### 参数

`info`  
需要传入一个数组，数组中每个key可为:m、:c、:a，:m代表module，:c代表controller,
:a代表action

`query`  
用户自定义的query string，将根据此路由规则拼接在url中

### 范例

**示例 \#1 <span
class="function">Yaf\_Route\_Static::assemble</span>example**

``` php
<?php

$router = new Yaf_Router();

$route  = new Yaf_Route_Static();

$router->addRoute("static", $route);

var_dump($router->getRoute('static')->assemble(
            array(
                ':a' => 'yafaction',
                'tkey' => 'tval',
                ':c' => 'yafcontroller',
                ':m' => 'yafmodule'
            ),
        )
);

var_dump($router->getRoute('static')->assemble(
            array(
                ':a' => 'yafaction',
                'tkey' => 'tval',
                ':c' => 'yafcontroller',
                ':m' => 'yafmodule'
            ),
            array(
                'tkey1' => 'tval1',
                'tkey2' => 'tval2'
            )
        )
);
```

以上例程的输出类似于：

    string(%d) "/yafmodule/yafcontroller/yafaction"
    string(%d) "/yafmodule/yafcontroller/yafaction?tkey1=tval1&tkey2=tval2"

### 返回值

Yaf\_Route\_Static::match
=========================

The match purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Route\_Static::match</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`uri`  

### 返回值

Yaf\_Route\_Static::route
=========================

Route a request

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Route\_Static::route</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  

### 返回值

总是返回TRUE

### 范例

**示例 \#1 <span
class="function">Yaf\_Route\_Static::route</span>example**

``` shell
// assuming there is only one module defined:Index
Request: http://yourdomain.com/a/b
=> module = index, controller=a, action=b

//assuming ap.action_prefer = On
Request: http://yourdomain.com/b
=> module = default(index), controller = default(index), action = b

//assuming ap.action_prefer = Off
Request: http://yourdomain.com/b
=> module = default(index), controller = b, action = default(index)


Request: http://yourdomain.com/a/b/foo/bar/test/a/id/4
=> module = default(index), controller = a, action = b, request parameters: foo = bar, test = a, id = 4
```

### 参见

-   <span class="methodname">Yaf\_Route\_Supervar::route</span>
-   <span class="methodname">Yaf\_Route\_Simple::route</span>
-   <span class="methodname">Yaf\_Route\_Regex::route</span>
-   <span class="methodname">Yaf\_Route\_Rewrite::route</span>
-   <span class="methodname">Yaf\_Route\_Map::route</span>

简介
----

类摘要
------

**Yaf\_Route\_Supervar**

<span class="ooclass"> class **Yaf\_Route\_Supervar** </span> <span
class="oointerface">implements <span
class="interfacename">Yaf\_Route\_Interface</span> </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_var_name` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">assemble</span> ( <span
class="methodparam"><span class="type">array</span> `$info`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$supervar_name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">route</span> ( <span class="methodparam"><span
class="type">Yaf\_Request\_Abstract</span> `$request`</span> )

}

属性
----

`_var_name`  

Yaf\_Route\_Supervar::assemble
==============================

组合url

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yaf\_Route\_Supervar::assemble</span> ( <span
class="methodparam"><span class="type">array</span> `$info`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

根据指定参数和自定义参数将supervar这个route组合成一个url

### 参数

`info`  
需要传入一个数组，数组中每个key可为:m、:c、:a，:m代表module，:c代表controller,
:a代表action

`query`  
用户自定义的query string，将根据此路由规则拼接在url中

### 范例

**示例 \#1 <span
class="function">Yaf\_Route\_Supervar::assemble</span>example**

``` php
<?php

$router = new Yaf_Router();

$route  = new Yaf_Route_Supervar('r');

$router->addRoute("supervar", $route);

var_dump($router->getRoute('supervar')->assemble(
        array(
              ':a' => 'yafaction',
              'tkey' => 'tval',
              ':c' => 'yafcontroller',
              ':m' => 'yafmodule'
        ),
        array(
              'tkey1' => 'tval1',
              'tkey2' => 'tval2'
        )
));

try {
var_dump($router->getRoute('supervar')->assemble(
        array(
              ':a' => 'yafaction',
              'tkey' => 'tval',
              ':m' => 'yafmodule'
        ),
        array(
              'tkey1' => 'tval1',
              'tkey2' => 'tval2',
              1 => array(),
        )
));
} catch (Exception $e) {
    var_dump($e->getMessage());
}
```

以上例程的输出类似于：

    string(%d) "?r=/yafmodule/yafcontroller/yafaction&tkey1=tval1&tkey2=tval2"
    string(%d) "You need to specify the controller by ':c'"

### 返回值

Yaf\_Route\_Supervar::\_\_construct
===================================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">Yaf\_Route\_Supervar::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$supervar_name`</span> )

<span class="classname">Yaf\_Route\_Supervar</span> 类似于 <span
class="classname">Yaf\_Route\_Static</span>，不同的是<span
class="classname">Yaf\_Route\_Supervar</span> 在query string
中寻找路劲信息，参数 `supervar_name` 是建。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`supervar_name`  
键名

### 返回值

### 范例

**示例 \#1 <span class="function">Yaf\_Route\_Supervar</span>example**

``` php
<?php
   /**
    * Add a supervar route to Yaf_Router route stack
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_Supervar("r"));
    );
?>
```

以上例程的输出类似于：

    /** for request: http://yourdomain.com/xx/oo/?r=/ctr/act/var/value
      * will result in following:
      */
      array (
        "module"   => index(default),
        "controller" => ctr,
        "action"     => act,
        "params"     => array(
              "var" => value,
         )
      )

### 参见

-   <span class="methodname">Yaf\_Router::addRoute</span>
-   <span class="methodname">Yaf\_Router::addConfig</span>
-   <span class="classname">Yaf\_Route\_Static</span>
-   <span class="classname">Yaf\_Route\_Regex</span>
-   <span class="classname">Yaf\_Route\_Simple</span>
-   <span class="classname">Yaf\_Route\_Rewrite</span>
-   <span class="classname">Yaf\_Route\_Map</span>

Yaf\_Route\_Supervar::route
===========================

The route purpose

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yaf\_Route\_Supervar::route</span> ( <span
class="methodparam"><span class="type">Yaf\_Request\_Abstract</span>
`$request`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`request`  

### 返回值

如果在$\_GET中有键（在 <span
class="methodname">Yaf\_Route\_Supervar::\_\_construct</span>中定义），返回TRUE，否则返回FALSE。

简介
----

类摘要
------

**Yaf\_Session**

<span class="ooclass"> class **Yaf\_Session** </span> <span
class="oointerface">implements <span
class="interfacename">Iterator</span> </span> <span
class="oointerface">, <span class="interfacename">Traversable</span>
</span> <span class="oointerface">, <span
class="interfacename">ArrayAccess</span> </span> <span
class="oointerface">, <span class="interfacename">Countable</span>
</span> {

/\* 属性 \*/

<span class="modifier">protected</span> <span
class="modifier">static</span> `$_instance` ;

<span class="modifier">protected</span> `$_session` ;

<span class="modifier">protected</span> `$_started` ;

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">count</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">del</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_get</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">getInstance</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">has</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_isset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetExists</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetGet</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetSet</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetUnset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_set</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_unset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

属性
----

`_instance`  

`_session`  

`_started`  

Yaf\_Session::\_\_construct
===========================

The \_\_construct purpose

### 说明

<span class="methodname">Yaf\_Session::\_\_construct</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Session::count
===================

The count purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::count</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Session::current
=====================

The current purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::current</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Session::del
=================

The del purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::del</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Session::\_\_get
=====================

The \_\_get purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::\_\_get</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Session::getInstance
=========================

The getInstance purpose

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Yaf\_Session::getInstance</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Session::has
=================

The has purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::has</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Session::\_\_isset
=======================

The \_\_isset purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::\_\_isset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Session::key
=================

The key purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::key</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Session::next
==================

The next purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::next</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Session::offsetExists
==========================

The offsetExists purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::offsetExists</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Session::offsetGet
=======================

The offsetGet purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::offsetGet</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Session::offsetSet
=======================

The offsetSet purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::offsetSet</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

`value`  

### 返回值

Yaf\_Session::offsetUnset
=========================

The offsetUnset purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::offsetUnset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Session::rewind
====================

The rewind purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::rewind</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Session::\_\_set
=====================

The \_\_set purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::\_\_set</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

`value`  

### 返回值

Yaf\_Session::start
===================

The start purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::start</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Session::\_\_unset
=======================

The \_\_unset purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::\_\_unset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`name`  

### 返回值

Yaf\_Session::valid
===================

The valid purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Session::valid</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

类摘要
------

**Yaf\_Exception**

<span class="ooclass"> class **Yaf\_Exception** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$message` ;

<span class="modifier">protected</span> `$code` ;

<span class="modifier">protected</span> `$previous` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getPrevious</span> ( <span
class="methodparam">void</span> )

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

属性
----

`message`  

`code`  

`file`  

`line`  

`previous`  

Yaf\_Exception::\_\_construct
=============================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">Yaf\_Exception::\_\_construct</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Yaf\_Exception::getPrevious
===========================

The getPrevious purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

类摘要
------

**Yaf\_Exception\_TypeError**

<span class="ooclass"> class **Yaf\_Exception\_TypeError** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Exception** </span> {

/\* 属性 \*/

/\* 方法 \*/

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">Yaf\_Exception::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

}

简介
----

类摘要
------

**Yaf\_Exception\_StartupError**

<span class="ooclass"> class **Yaf\_Exception\_StartupError** </span>
<span class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Exception** </span> {

/\* 属性 \*/

/\* 方法 \*/

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">Yaf\_Exception::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

}

简介
----

类摘要
------

**Yaf\_Exception\_DispatchFailed**

<span class="ooclass"> class **Yaf\_Exception\_DispatchFailed** </span>
<span class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Exception** </span> {

/\* 属性 \*/

/\* 方法 \*/

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">Yaf\_Exception::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

}

简介
----

类摘要
------

**Yaf\_Exception\_RouterFailed**

<span class="ooclass"> class **Yaf\_Exception\_RouterFailed** </span>
<span class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Exception** </span> {

/\* 属性 \*/

/\* 方法 \*/

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">Yaf\_Exception::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

}

简介
----

类摘要
------

**Yaf\_Exception\_LoadFailed**

<span class="ooclass"> class **Yaf\_Exception\_LoadFailed** </span>
<span class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Exception** </span> {

/\* 属性 \*/

/\* 方法 \*/

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">Yaf\_Exception::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

}

简介
----

类摘要
------

**Yaf\_Exception\_LoadFailed\_Module**

<span class="ooclass"> class **Yaf\_Exception\_LoadFailed\_Module**
</span> <span class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Exception\_LoadFailed** </span> {

/\* 属性 \*/

/\* 方法 \*/

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">Yaf\_Exception::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

}

简介
----

类摘要
------

**Yaf\_Exception\_LoadFailed\_Controller**

<span class="ooclass"> class **Yaf\_Exception\_LoadFailed\_Controller**
</span> <span class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Exception\_LoadFailed** </span> {

/\* 属性 \*/

/\* 方法 \*/

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">Yaf\_Exception::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

}

简介
----

类摘要
------

**Yaf\_Exception\_LoadFailed\_Action**

<span class="ooclass"> class **Yaf\_Exception\_LoadFailed\_Action**
</span> <span class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Exception\_LoadFailed** </span> {

/\* 属性 \*/

/\* 方法 \*/

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">Yaf\_Exception::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

}

简介
----

类摘要
------

**Yaf\_Exception\_LoadFailed\_View**

<span class="ooclass"> class **Yaf\_Exception\_LoadFailed\_View**
</span> <span class="ooclass"> <span class="modifier">extends</span>
**Yaf\_Exception\_LoadFailed** </span> {

/\* 属性 \*/

/\* 方法 \*/

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">Yaf\_Exception::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yaf\_Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

}
