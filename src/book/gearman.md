Gearman
=======

**目录**

-   [简介](/intro/gearman.html)
-   [安装／配置](/gearman/setup.html)
    -   [需求](/gearman/setup.html#需求)
    -   [安装](/gearman/setup.html#安装)
    -   [运行时配置](/gearman/setup.html#运行时配置)
    -   [资源类型](/gearman/setup.html#资源类型)
-   [预定义常量](/gearman/constants.html)
-   [范例](/gearman/examples.html)
    -   [Basic usage](/gearman/examples.html#Basic%20usage)
    -   [Basic Gearman client and worker,
        background](/gearman/examples.html#Basic%20Gearman%20client%20and%20worker,%20background)
    -   [Basic Gearman client and worker, submitting
        tasks](/gearman/examples.html#Basic%20Gearman%20client%20and%20worker,%20submitting%20tasks)
-   [GearmanClient](/class/gearmanclient.html) — The GearmanClient class
    -   [GearmanClient::addOptions](/class/gearmanclient.html#GearmanClient::addOptions)
        — Add client options
    -   [GearmanClient::addServer](/class/gearmanclient.html#GearmanClient::addServer)
        — Add a job server to the client
    -   [GearmanClient::addServers](/class/gearmanclient.html#GearmanClient::addServers)
        — Add a list of job servers to the client
    -   [GearmanClient::addTask](/class/gearmanclient.html#GearmanClient::addTask)
        — Add a task to be run in parallel
    -   [GearmanClient::addTaskBackground](/class/gearmanclient.html#GearmanClient::addTaskBackground)
        — Add a background task to be run in parallel
    -   [GearmanClient::addTaskHigh](/class/gearmanclient.html#GearmanClient::addTaskHigh)
        — Add a high priority task to run in parallel
    -   [GearmanClient::addTaskHighBackground](/class/gearmanclient.html#GearmanClient::addTaskHighBackground)
        — Add a high priority background task to be run in parallel
    -   [GearmanClient::addTaskLow](/class/gearmanclient.html#GearmanClient::addTaskLow)
        — Add a low priority task to run in parallel
    -   [GearmanClient::addTaskLowBackground](/class/gearmanclient.html#GearmanClient::addTaskLowBackground)
        — Add a low priority background task to be run in parallel
    -   [GearmanClient::addTaskStatus](/class/gearmanclient.html#GearmanClient::addTaskStatus)
        — Add a task to get status
    -   [GearmanClient::clearCallbacks](/class/gearmanclient.html#GearmanClient::clearCallbacks)
        — Clear all task callback functions
    -   [GearmanClient::clone](/class/gearmanclient.html#GearmanClient::clone)
        — Create a copy of a GearmanClient object
    -   [GearmanClient::\_\_construct](/class/gearmanclient.html#GearmanClient::__construct)
        — Create a GearmanClient instance
    -   [GearmanClient::context](/class/gearmanclient.html#GearmanClient::context)
        — Get the application context
    -   [GearmanClient::data](/class/gearmanclient.html#GearmanClient::data)
        — Get the application data (deprecated)
    -   [GearmanClient::do](/class/gearmanclient.html#GearmanClient::do)
        — Run a single task and return a result \[deprecated\]
    -   [GearmanClient::doBackground](/class/gearmanclient.html#GearmanClient::doBackground)
        — Run a task in the background
    -   [GearmanClient::doHigh](/class/gearmanclient.html#GearmanClient::doHigh)
        — Run a single high priority task
    -   [GearmanClient::doHighBackground](/class/gearmanclient.html#GearmanClient::doHighBackground)
        — Run a high priority task in the background
    -   [GearmanClient::doJobHandle](/class/gearmanclient.html#GearmanClient::doJobHandle)
        — Get the job handle for the running task
    -   [GearmanClient::doLow](/class/gearmanclient.html#GearmanClient::doLow)
        — Run a single low priority task
    -   [GearmanClient::doLowBackground](/class/gearmanclient.html#GearmanClient::doLowBackground)
        — Run a low priority task in the background
    -   [GearmanClient::doNormal](/class/gearmanclient.html#GearmanClient::doNormal)
        — Run a single task and return a result
    -   [GearmanClient::doStatus](/class/gearmanclient.html#GearmanClient::doStatus)
        — Get the status for the running task
    -   [GearmanClient::echo](/class/gearmanclient.html#GearmanClient::echo)
        — Send data to all job servers to see if they echo it back
        \[deprecated\]
    -   [GearmanClient::error](/class/gearmanclient.html#GearmanClient::error)
        — Returns an error string for the last error encountered
    -   [GearmanClient::getErrno](/class/gearmanclient.html#GearmanClient::getErrno)
        — Get an errno value
    -   [GearmanClient::jobStatus](/class/gearmanclient.html#GearmanClient::jobStatus)
        — Get the status of a background job
    -   [GearmanClient::ping](/class/gearmanclient.html#GearmanClient::ping)
        — Send data to all job servers to see if they echo it back
    -   [GearmanClient::removeOptions](/class/gearmanclient.html#GearmanClient::removeOptions)
        — Remove client options
    -   [GearmanClient::returnCode](/class/gearmanclient.html#GearmanClient::returnCode)
        — Get the last Gearman return code
    -   [GearmanClient::runTasks](/class/gearmanclient.html#GearmanClient::runTasks)
        — Run a list of tasks in parallel
    -   [GearmanClient::setClientCallback](/class/gearmanclient.html#GearmanClient::setClientCallback)
        — Callback function when there is a data packet for a task
        (deprecated)
    -   [GearmanClient::setCompleteCallback](/class/gearmanclient.html#GearmanClient::setCompleteCallback)
        — Set a function to be called on task completion
    -   [GearmanClient::setContext](/class/gearmanclient.html#GearmanClient::setContext)
        — Set application context
    -   [GearmanClient::setCreatedCallback](/class/gearmanclient.html#GearmanClient::setCreatedCallback)
        — Set a callback for when a task is queued
    -   [GearmanClient::setData](/class/gearmanclient.html#GearmanClient::setData)
        — Set application data (deprecated)
    -   [GearmanClient::setDataCallback](/class/gearmanclient.html#GearmanClient::setDataCallback)
        — Callback function when there is a data packet for a task
    -   [GearmanClient::setExceptionCallback](/class/gearmanclient.html#GearmanClient::setExceptionCallback)
        — Set a callback for worker exceptions
    -   [GearmanClient::setFailCallback](/class/gearmanclient.html#GearmanClient::setFailCallback)
        — Set callback for job failure
    -   [GearmanClient::setOptions](/class/gearmanclient.html#GearmanClient::setOptions)
        — Set client options
    -   [GearmanClient::setStatusCallback](/class/gearmanclient.html#GearmanClient::setStatusCallback)
        — Set a callback for collecting task status
    -   [GearmanClient::setTimeout](/class/gearmanclient.html#GearmanClient::setTimeout)
        — Set socket I/O activity timeout
    -   [GearmanClient::setWarningCallback](/class/gearmanclient.html#GearmanClient::setWarningCallback)
        — Set a callback for worker warnings
    -   [GearmanClient::setWorkloadCallback](/class/gearmanclient.html#GearmanClient::setWorkloadCallback)
        — Set a callback for accepting incremental data updates
    -   [GearmanClient::timeout](/class/gearmanclient.html#GearmanClient::timeout)
        — Get current socket I/O activity timeout value
-   [GearmanJob](/class/gearmanjob.html) — The GearmanJob class
    -   [GearmanJob::complete](/class/gearmanjob.html#GearmanJob::complete)
        — Send the result and complete status (deprecated)
    -   [GearmanJob::\_\_construct](/class/gearmanjob.html#GearmanJob::__construct)
        — Create a GearmanJob instance
    -   [GearmanJob::data](/class/gearmanjob.html#GearmanJob::data) —
        Send data for a running job (deprecated)
    -   [GearmanJob::exception](/class/gearmanjob.html#GearmanJob::exception)
        — Send exception for running job (deprecated)
    -   [GearmanJob::fail](/class/gearmanjob.html#GearmanJob::fail) —
        Send fail status (deprecated)
    -   [GearmanJob::functionName](/class/gearmanjob.html#GearmanJob::functionName)
        — Get function name
    -   [GearmanJob::handle](/class/gearmanjob.html#GearmanJob::handle)
        — Get the job handle
    -   [GearmanJob::returnCode](/class/gearmanjob.html#GearmanJob::returnCode)
        — Get last return code
    -   [GearmanJob::sendComplete](/class/gearmanjob.html#GearmanJob::sendComplete)
        — Send the result and complete status
    -   [GearmanJob::sendData](/class/gearmanjob.html#GearmanJob::sendData)
        — Send data for a running job
    -   [GearmanJob::sendException](/class/gearmanjob.html#GearmanJob::sendException)
        — Send exception for running job (exception)
    -   [GearmanJob::sendFail](/class/gearmanjob.html#GearmanJob::sendFail)
        — Send fail status
    -   [GearmanJob::sendStatus](/class/gearmanjob.html#GearmanJob::sendStatus)
        — Send status
    -   [GearmanJob::sendWarning](/class/gearmanjob.html#GearmanJob::sendWarning)
        — Send a warning
    -   [GearmanJob::setReturn](/class/gearmanjob.html#GearmanJob::setReturn)
        — Set a return value
    -   [GearmanJob::status](/class/gearmanjob.html#GearmanJob::status)
        — Send status (deprecated)
    -   [GearmanJob::unique](/class/gearmanjob.html#GearmanJob::unique)
        — Get the unique identifier
    -   [GearmanJob::warning](/class/gearmanjob.html#GearmanJob::warning)
        — Send a warning (deprecated)
    -   [GearmanJob::workload](/class/gearmanjob.html#GearmanJob::workload)
        — Get workload
    -   [GearmanJob::workloadSize](/class/gearmanjob.html#GearmanJob::workloadSize)
        — Get size of work load
-   [GearmanTask](/class/gearmantask.html) — The GearmanTask class
    -   [GearmanTask::\_\_construct](/class/gearmantask.html#GearmanTask::__construct)
        — Create a GearmanTask instance
    -   [GearmanTask::create](/class/gearmantask.html#GearmanTask::create)
        — Create a task (deprecated)
    -   [GearmanTask::data](/class/gearmantask.html#GearmanTask::data) —
        Get data returned for a task
    -   [GearmanTask::dataSize](/class/gearmantask.html#GearmanTask::dataSize)
        — Get the size of returned data
    -   [GearmanTask::function](/class/gearmantask.html#GearmanTask::function)
        — Get associated function name (deprecated)
    -   [GearmanTask::functionName](/class/gearmantask.html#GearmanTask::functionName)
        — Get associated function name
    -   [GearmanTask::isKnown](/class/gearmantask.html#GearmanTask::isKnown)
        — Determine if task is known
    -   [GearmanTask::isRunning](/class/gearmantask.html#GearmanTask::isRunning)
        — Test whether the task is currently running
    -   [GearmanTask::jobHandle](/class/gearmantask.html#GearmanTask::jobHandle)
        — Get the job handle
    -   [GearmanTask::recvData](/class/gearmantask.html#GearmanTask::recvData)
        — Read work or result data into a buffer for a task
    -   [GearmanTask::returnCode](/class/gearmantask.html#GearmanTask::returnCode)
        — Get the last return code
    -   [GearmanTask::sendData](/class/gearmantask.html#GearmanTask::sendData)
        — Send data for a task (deprecated)
    -   [GearmanTask::sendWorkload](/class/gearmantask.html#GearmanTask::sendWorkload)
        — Send data for a task
    -   [GearmanTask::taskDenominator](/class/gearmantask.html#GearmanTask::taskDenominator)
        — Get completion percentage denominator
    -   [GearmanTask::taskNumerator](/class/gearmantask.html#GearmanTask::taskNumerator)
        — Get completion percentage numerator
    -   [GearmanTask::unique](/class/gearmantask.html#GearmanTask::unique)
        — Get the unique identifier for a task
    -   [GearmanTask::uuid](/class/gearmantask.html#GearmanTask::uuid) —
        Get the unique identifier for a task (deprecated)
-   [GearmanWorker](/class/gearmanworker.html) — The GearmanWorker class
    -   [GearmanWorker::addFunction](/class/gearmanworker.html#GearmanWorker::addFunction)
        — Register and add callback function
    -   [GearmanWorker::addOptions](/class/gearmanworker.html#GearmanWorker::addOptions)
        — Add worker options
    -   [GearmanWorker::addServer](/class/gearmanworker.html#GearmanWorker::addServer)
        — Add a job server
    -   [GearmanWorker::addServers](/class/gearmanworker.html#GearmanWorker::addServers)
        — Add job servers
    -   [GearmanWorker::clone](/class/gearmanworker.html#GearmanWorker::clone)
        — Create a copy of the worker
    -   [GearmanWorker::\_\_construct](/class/gearmanworker.html#GearmanWorker::__construct)
        — Create a GearmanWorker instance
    -   [GearmanWorker::echo](/class/gearmanworker.html#GearmanWorker::echo)
        — Test job server response
    -   [GearmanWorker::error](/class/gearmanworker.html#GearmanWorker::error)
        — Get the last error encountered
    -   [GearmanWorker::getErrno](/class/gearmanworker.html#GearmanWorker::getErrno)
        — Get errno
    -   [GearmanWorker::options](/class/gearmanworker.html#GearmanWorker::options)
        — Get worker options
    -   [GearmanWorker::register](/class/gearmanworker.html#GearmanWorker::register)
        — Register a function with the job server
    -   [GearmanWorker::removeOptions](/class/gearmanworker.html#GearmanWorker::removeOptions)
        — Remove worker options
    -   [GearmanWorker::returnCode](/class/gearmanworker.html#GearmanWorker::returnCode)
        — Get last Gearman return code
    -   [GearmanWorker::setId](/class/gearmanworker.html#GearmanWorker::setId)
        — Give the worker an identifier so it can be tracked when asking
        gearmand for the list of available workers
    -   [GearmanWorker::setOptions](/class/gearmanworker.html#GearmanWorker::setOptions)
        — Set worker options
    -   [GearmanWorker::setTimeout](/class/gearmanworker.html#GearmanWorker::setTimeout)
        — Set socket I/O activity timeout
    -   [GearmanWorker::timeout](/class/gearmanworker.html#GearmanWorker::timeout)
        — Get socket I/O activity timeout
    -   [GearmanWorker::unregister](/class/gearmanworker.html#GearmanWorker::unregister)
        — Unregister a function name with the job servers
    -   [GearmanWorker::unregisterAll](/class/gearmanworker.html#GearmanWorker::unregisterAll)
        — Unregister all function names with the job servers
    -   [GearmanWorker::wait](/class/gearmanworker.html#GearmanWorker::wait)
        — Wait for activity from one of the job servers
    -   [GearmanWorker::work](/class/gearmanworker.html#GearmanWorker::work)
        — Wait for and perform jobs
-   [GearmanException](/class/gearmanexception.html) — The
    GearmanException class

简介
----

Represents a class for connecting to a Gearman job server and making
requests to perform some function on provided data. The function
performed must be one registered by a Gearman worker and the data passed
is opaque to the job server.

类摘要
------

**GearmanClient**

<span class="ooclass"> class **GearmanClient** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addOptions</span> ( <span
class="methodparam"><span class="type">int</span> `$options`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addServer</span> (\[ <span
class="methodparam"><span class="type">string</span> `$host`<span
class="initializer"> = 127.0.0.1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 4730</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addServers</span> (\[ <span
class="methodparam"><span class="type">string</span> `$servers`<span
class="initializer"> = 127.0.0.1:4730</span></span> \] )

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span class="methodname">addTask</span>
( <span class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$context`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$unique`</span> \]\] )

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">addTaskBackground</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$context`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$unique`</span> \]\] )

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">addTaskHigh</span> ( <span class="methodparam"><span
class="type">string</span> `$function_name`</span> , <span
class="methodparam"><span class="type">string</span> `$workload`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`&$context`</span> \[, <span class="methodparam"><span
class="type">string</span> `$unique`</span> \]\] )

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">addTaskHighBackground</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$context`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$unique`</span> \]\] )

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">addTaskLow</span> ( <span class="methodparam"><span
class="type">string</span> `$function_name`</span> , <span
class="methodparam"><span class="type">string</span> `$workload`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`&$context`</span> \[, <span class="methodparam"><span
class="type">string</span> `$unique`</span> \]\] )

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">addTaskLowBackground</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$context`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$unique`</span> \]\] )

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">addTaskStatus</span> ( <span
class="methodparam"><span class="type">string</span>
`$job_handle`</span> \[, <span class="methodparam"><span
class="type">string</span> `&$context`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">clearCallbacks</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">GearmanClient</span> <span class="methodname">clone</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">context</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">data</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">do</span> ( <span class="methodparam"><span
class="type">string</span> `$function_name`</span> , <span
class="methodparam"><span class="type">string</span> `$workload`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$unique`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">doBackground</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">string</span> `$unique`</span> \]
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">doHigh</span> ( <span class="methodparam"><span
class="type">string</span> `$function_name`</span> , <span
class="methodparam"><span class="type">string</span> `$workload`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$unique`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">doHighBackground</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">string</span> `$unique`</span> \]
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">doJobHandle</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">doLow</span> ( <span class="methodparam"><span
class="type">string</span> `$function_name`</span> , <span
class="methodparam"><span class="type">string</span> `$workload`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$unique`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">doLowBackground</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">string</span> `$unique`</span> \]
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">doNormal</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">string</span> `$unique`</span> \]
)

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">doStatus</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">echo</span> ( <span class="methodparam"><span
class="type">string</span> `$workload`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">error</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getErrno</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">jobStatus</span> ( <span
class="methodparam"><span class="type">string</span>
`$job_handle`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ping</span> ( <span class="methodparam"><span
class="type">string</span> `$workload`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">removeOptions</span> ( <span
class="methodparam"><span class="type">int</span> `$options`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">returnCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">runTasks</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setClientCallback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setCompleteCallback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setContext</span> ( <span
class="methodparam"><span class="type">string</span> `$context`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setCreatedCallback</span> ( <span
class="methodparam"><span class="type">string</span> `$callback`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setData</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setDataCallback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setExceptionCallback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setFailCallback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setOptions</span> ( <span
class="methodparam"><span class="type">int</span> `$options`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setStatusCallback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$timeout`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setWarningCallback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setWorkloadCallback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">timeout</span> ( <span
class="methodparam">void</span> )

}

GearmanClient::addOptions
=========================

Add client options

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::addOptions</span> ( <span
class="methodparam"><span class="type">int</span> `$options`</span> )

Adds one or more options to those already set.

### 参数

`options`  
The options to add. One of the following constants, or a combination of
them using the bitwise OR operator (“\|”):
**`GEARMAN_CLIENT_GENERATE_UNIQUE`**, **`GEARMAN_CLIENT_NON_BLOCKING`**,
**`GEARMAN_CLIENT_UNBUFFERED_RESULT`** or
**`GEARMAN_CLIENT_FREE_TASKS`**.

### 返回值

Always returns **`TRUE`**.

GearmanClient::addServer
========================

Add a job server to the client

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::addServer</span> (\[ <span
class="methodparam"><span class="type">string</span> `$host`<span
class="initializer"> = 127.0.0.1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 4730</span></span> \]\] )

Adds a job server to a list of servers that can be used to run a task.
No socket I/O happens here; the server is simply added to the list.

### 参数

`host`  
任务服务器主机名。

`port`  
任务服务器端口号。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Adding two job servers**

``` php
<?php

# Create our client object.
$gmclient= new GearmanClient();

# Add two job servers, the first on the default 4730 port
$gmclient->addServer("10.0.0.1"); 
$gmclient->addServer("10.0.0.2", 7003);

?>
```

### 参见

-   <span class="methodname">GearmanClient::addServers</span>

GearmanClient::addServers
=========================

Add a list of job servers to the client

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::addServers</span> (\[ <span
class="methodparam"><span class="type">string</span> `$servers`<span
class="initializer"> = 127.0.0.1:4730</span></span> \] )

Adds a list of job servers that can be used to run a task. No socket I/O
happens here; the servers are simply added to the full list of servers.

### 参数

`servers`  
A comma-separated list of servers, each server specified in the format
'*host:port*'.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Add two job servers**

``` php
<?php

# Create our client object.
$gmclient= new GearmanClient();

# Add multiple job servers, the first on the default 4730 port
$gmclient->addServers("10.0.0.1,10.0.0.2:7003");

?>
```

### 参见

-   <span class="methodname">GearmanClient::addServer</span>

GearmanClient::addTask
======================

Add a task to be run in parallel

### 说明

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">GearmanClient::addTask</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$context`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$unique`</span> \]\] )

Adds a task to be run in parallel with other tasks. Call this method for
all the tasks to be run in parallel, then call <span
class="methodname">GearmanClient::runTasks</span> to perform the work.
Note that enough workers need to be available for the tasks to all run
in parallel.

### 参数

`function_name`  
由程序自动执行的已注册函数。

`workload`  
被处理的序列化数据。

`context`  
与任务关联的应用程序上下文。

`unique`  
用于标识特定任务的唯一性 ID。

### 返回值

A <span class="classname">GearmanTask</span> object or **`FALSE`** if
the task could not be added.

### 范例

**示例 \#1 Basic submission of two tasks**

``` php
<?php

# Create our gearman client
$gmclient= new GearmanClient(); 

# add the default job server
$gmclient->addServer(); 

# set a function to be called when the work is complete
$gmclient->setCompleteCallback("complete"); 

# add a task to perform the "reverse" function on the string "Hello World!"
$gmclient->addTask("reverse", "Hello World!", null, "1"); 

# add another task to perform the "reverse" function on the string "!dlroW olleH"
$gmclient->addTask("reverse", "!dlroW olleH", null, "2"); 

# run the tasks
$gmclient->runTasks(); 

function complete($task) 
{ 
  print "COMPLETE: " . $task->unique() . ", " . $task->data() . "\n"; 
}

?>
```

以上例程的输出类似于：

    COMPLETE: 2, Hello World!
    COMPLETE: 1, !dlroW olleH

**示例 \#2 Basic submission of two tasks with passing application
context**

``` php
<?php

$client = new GearmanClient();
$client->addServer();

# set a function to be called when the work is complete
$client->setCompleteCallback("reverse_complete");

# Add some tasks for a placeholder of where to put the results
$results = array();
$client->addTask("reverse", "Hello World!", &$results, "t1");
$client->addTask("reverse", "!dlroW olleH", &$results, "t2");

$client->runTasks();

# The results should now be filled in from the callbacks
foreach ($results as $id => $result)
   echo $id . ": " . $result['handle'] . ", " . $result['data'] . "\n";


function reverse_complete($task, $results)
{
   $results[$task->unique()] = array("handle"=>$task->jobHandle(), "data"=>$task->data());
}

?>
```

以上例程的输出类似于：

    t2: H.foo:21, Hello World!
    t1: H:foo:22, !dlroW olleH

### 参见

-   <span class="methodname">GearmanClient::addTaskHigh</span>
-   <span class="methodname">GearmanClient::addTaskLow</span>
-   <span class="methodname">GearmanClient::addTaskBackground</span>
-   <span class="methodname">GearmanClient::addTaskHighBackground</span>
-   <span class="methodname">GearmanClient::addTaskLowBackground</span>
-   <span class="methodname">GearmanClient::runTasks</span>

GearmanClient::addTaskBackground
================================

Add a background task to be run in parallel

### 说明

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">GearmanClient::addTaskBackground</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$context`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$unique`</span> \]\] )

Adds a background task to be run in parallel with other tasks. Call this
method for all the tasks to be run in parallel, then call <span
class="methodname">GearmanClient::runTasks</span> to perform the work.

### 参数

`function_name`  
由程序自动执行的已注册函数。

`workload`  
被处理的序列化数据。

`context`  
与任务关联的应用程序上下文。

`unique`  
用于标识特定任务的唯一性 ID。

### 返回值

A <span class="classname">GearmanTask</span> object or **`FALSE`** if
the task could not be added.

### 范例

**示例 \#1 Two tasks, one background and one not**

This example illustrates the difference between running a background
task and a normal task. The client adds two tasks to execute the same
function, but one is added with <span
class="methodname">addTaskBackground</span>. A callback is set so that
progress of the job can be tracked. A simple worker with an artificial
delay reports on the job progress and the client picks this up through
the callback. Two workers are run for this example. Note that the
background task does not show in the client output.

``` php
<?php

# The client script

# create our gearman client
$gmc= new GearmanClient();

# add the default job server
$gmc->addServer();

# set a couple of callbacks so we can track progress
$gmc->setCompleteCallback("reverse_complete");
$gmc->setStatusCallback("reverse_status");

# add a task for the "reverse" function
$task= $gmc->addTask("reverse", "Hello World!", null, "1");

# add another task, but this one to run in the background
$task= $gmc->addTaskBackground("reverse", "!dlroW olleH", null, "2");

if (! $gmc->runTasks())
{
    echo "ERROR " . $gmc->error() . "\n";
    exit;
}

echo "DONE\n";

function reverse_status($task)
{
    echo "STATUS: " . $task->unique() . ", " . $task->jobHandle() . " - " . $task->taskNumerator() . 
         "/" . $task->taskDenominator() . "\n";
}

function reverse_complete($task)
{
    echo "COMPLETE: " . $task->unique() . ", " . $task->data() . "\n";
}

?>
```

``` php
<?php

# The worker script

echo "Starting\n";

# Create our worker object.
$gmworker= new GearmanWorker();

# Add default server (localhost).
$gmworker->addServer();

# Register function "reverse" with the server.
$gmworker->addFunction("reverse", "reverse_fn");

print "Waiting for job...\n";
while($gmworker->work())
{
  if ($gmworker->returnCode() != GEARMAN_SUCCESS)
  {
    echo "return_code: " . $gmworker->returnCode() . "\n";
    break;
  }
}

function reverse_fn($job)
{
  echo "Received job: " . $job->handle() . "\n";

  $workload = $job->workload();
  $workload_size = $job->workloadSize();

  echo "Workload: $workload ($workload_size)\n";

  # This status loop is not needed, just showing how it works
  for ($x= 0; $x < $workload_size; $x++)
  {
    echo "Sending status: " . ($x + 1) . "/$workload_size complete\n";
    $job->sendStatus($x+1, $workload_size);
    $job->sendData(substr($workload, $x, 1));
    sleep(1);
  }

  $result= strrev($workload);
  echo "Result: $result\n";

  # Return what we want to send back to the client.
  return $result;
}

?>
```

Worker output for two workers running:

    Received job: H:foo.local:65
    Workload: !dlroW olleH (12)
    1/12 complete
    Received job: H:foo.local:66
    Workload: Hello World! (12)
    Sending status: 1/12 complete
    Sending status: 2/12 complete
    Sending status: 2/12 complete
    Sending status: 3/12 complete
    Sending status: 3/12 complete
    Sending status: 4/12 complete
    Sending status: 4/12 complete
    Sending status: 5/12 complete
    Sending status: 5/12 complete
    Sending status: 6/12 complete
    Sending status: 6/12 complete
    Sending status: 7/12 complete
    Sending status: 7/12 complete
    Sending status: 8/12 complete
    Sending status: 8/12 complete
    Sending status: 9/12 complete
    Sending status: 9/12 complete
    Sending status: 10/12 complete
    Sending status: 10/12 complete
    Sending status: 11/12 complete
    Sending status: 11/12 complete
    Sending status: 12/12 complete
    Sending status: 12/12 complete
    Result: !dlroW olleH
    Result: Hello World!

Client output:

    STATUS: 1, H:foo.local:66 - 1/12
    STATUS: 1, H:foo.local:66 - 2/12
    STATUS: 1, H:foo.local:66 - 3/12
    STATUS: 1, H:foo.local:66 - 4/12
    STATUS: 1, H:foo.local:66 - 5/12
    STATUS: 1, H:foo.local:66 - 6/12
    STATUS: 1, H:foo.local:66 - 7/12
    STATUS: 1, H:foo.local:66 - 8/12
    STATUS: 1, H:foo.local:66 - 9/12
    STATUS: 1, H:foo.local:66 - 10/12
    STATUS: 1, H:foo.local:66 - 11/12
    STATUS: 1, H:foo.local:66 - 12/12
    COMPLETE: 1, !dlroW olleH
    DONE

### 参见

-   <span class="methodname">GearmanClient::addTask</span>
-   <span class="methodname">GearmanClient::addTaskHigh</span>
-   <span class="methodname">GearmanClient::addTaskLow</span>
-   <span class="methodname">GearmanClient::addTaskHighBackground</span>
-   <span class="methodname">GearmanClient::addTaskLowBackground</span>
-   <span class="methodname">GearmanClient::runTasks</span>

GearmanClient::addTaskHigh
==========================

Add a high priority task to run in parallel

### 说明

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">GearmanClient::addTaskHigh</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$context`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$unique`</span> \]\] )

Adds a high priority task to be run in parallel with other tasks. Call
this method for all the high priority tasks to be run in parallel, then
call <span class="methodname">GearmanClient::runTasks</span> to perform
the work. Tasks with a high priority will be selected from the queue
before those of normal or low priority.

### 参数

`function_name`  
由程序自动执行的已注册函数。

`workload`  
被处理的序列化数据。

`context`  
与任务关联的应用程序上下文。

`unique`  
用于标识特定任务的唯一性 ID。

### 返回值

A <span class="classname">GearmanTask</span> object or **`FALSE`** if
the task could not be added.

### 范例

**示例 \#1 A high priority task along with two normal tasks**

A high priority task is included among two other tasks. A single worker
is available, so that tasks are run one at a time, with the high
priority task run first.

``` php
<?php

# create the gearman client
$gmc= new GearmanClient();

# add the default job server
$gmc->addServer();

# set the callback for when the job is complete
$gmc->setCompleteCallback("reverse_complete");

# add tasks, one of which is high priority
$task= $gmc->addTask("reverse", "Hello World!", null, "1");
$task= $gmc->addTaskHigh("reverse", "!dlroW olleH", null, "2");
$task= $gmc->addTask("reverse", "Hello World!", null, "3");

if (! $gmc->runTasks())
{
    echo "ERROR " . $gmc->error() . "\n";
    exit;
}
echo "DONE\n";

function reverse_complete($task)
{
    echo "COMPLETE: " . $task->unique() . ", " . $task->data() . "\n";
}

?>
```

以上例程的输出类似于：

    COMPLETE: 2, Hello World!
    COMPLETE: 3, !dlroW olleH
    COMPLETE: 1, !dlroW olleH
    DONE

### 参见

-   <span class="methodname">GearmanClient::addTask</span>
-   <span class="methodname">GearmanClient::addTaskLow</span>
-   <span class="methodname">GearmanClient::addTaskBackground</span>
-   <span class="methodname">GearmanClient::addTaskHighBackground</span>
-   <span class="methodname">GearmanClient::addTaskLowBackground</span>
-   <span class="methodname">GearmanClient::runTasks</span>

GearmanClient::addTaskHighBackground
====================================

Add a high priority background task to be run in parallel

### 说明

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">GearmanClient::addTaskHighBackground</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$context`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$unique`</span> \]\] )

Adds a high priority background task to be run in parallel with other
tasks. Call this method for all the tasks to be run in parallel, then
call <span class="methodname">GearmanClient::runTasks</span> to perform
the work. Tasks with a high priority will be selected from the queue
before those of normal or low priority.

### 参数

`function_name`  
由程序自动执行的已注册函数。

`workload`  
被处理的序列化数据。

`context`  
与任务关联的应用程序上下文。

`unique`  
用于标识特定任务的唯一性 ID。

### 返回值

A <span class="classname">GearmanTask</span> object or **`FALSE`** if
the task could not be added.

### 参见

-   <span class="methodname">GearmanClient::addTask</span>
-   <span class="methodname">GearmanClient::addTaskHigh</span>
-   <span class="methodname">GearmanClient::addTaskLow</span>
-   <span class="methodname">GearmanClient::addTaskBackground</span>
-   <span class="methodname">GearmanClient::addTaskLowBackground</span>
-   <span class="methodname">GearmanClient::runTasks</span>

GearmanClient::addTaskLow
=========================

Add a low priority task to run in parallel

### 说明

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">GearmanClient::addTaskLow</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$context`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$unique`</span> \]\] )

Adds a low priority background task to be run in parallel with other
tasks. Call this method for all the tasks to be run in parallel, then
call <span class="methodname">GearmanClient::runTasks</span> to perform
the work. Tasks with a low priority will be selected from the queue
after those of normal or low priority.

### 参数

`function_name`  
由程序自动执行的已注册函数。

`workload`  
被处理的序列化数据。

`context`  
与任务关联的应用程序上下文。

`unique`  
用于标识特定任务的唯一性 ID。

### 返回值

A <span class="classname">GearmanTask</span> object or **`FALSE`** if
the task could not be added.

### 范例

**示例 \#1 A low priority task along with two normal tasks**

A low priority task is included among two other tasks. A single worker
is available, so that tasks are run one at a time, with the low priority
task run last.

``` php
<?php

# create the gearman client
$gmc= new GearmanClient();

# add the default job server
$gmc->addServer();

# set the callback for when the job is complete
$gmc->setCompleteCallback("reverse_complete");

# add tasks, one of which is low priority
$task= $gmc->addTask("reverse", "Hello World!", null, "1");
$task= $gmc->addTaskLow("reverse", "!dlroW olleH", null, "2");
$task= $gmc->addTask("reverse", "Hello World!", null, "3");

if (! $gmc->runTasks())
{
    echo "ERROR " . $gmc->error() . "\n";
    exit;
}
echo "DONE\n";

function reverse_complete($task)
{
    echo "COMPLETE: " . $task->unique() . ", " . $task->data() . "\n";
}

?>
```

以上例程的输出类似于：

    COMPLETE: 3, !dlroW olleH
    COMPLETE: 1, !dlroW olleH
    COMPLETE: 2, Hello World!
    DONE

### 参见

-   <span class="methodname">GearmanClient::addTask</span>
-   <span class="methodname">GearmanClient::addTaskHigh</span>
-   <span class="methodname">GearmanClient::addTaskBackground</span>
-   <span class="methodname">GearmanClient::addTaskHighBackground</span>
-   <span class="methodname">GearmanClient::addTaskLowBackground</span>
-   <span class="methodname">GearmanClient::runTasks</span>

GearmanClient::addTaskLowBackground
===================================

Add a low priority background task to be run in parallel

### 说明

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">GearmanClient::addTaskLowBackground</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$context`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$unique`</span> \]\] )

Adds a low priority background task to be run in parallel with other
tasks. Call this method for all the tasks to be run in parallel, then
call <span class="methodname">GearmanClient::runTasks</span> to perform
the work. Tasks with a low priority will be selected from the queue
after those of normal or high priority.

### 参数

`function_name`  
由程序自动执行的已注册函数。

`workload`  
被处理的序列化数据。

`context`  
与任务关联的应用程序上下文。

`unique`  
用于标识特定任务的唯一性 ID。

### 返回值

A <span class="classname">GearmanTask</span> object or **`FALSE`** if
the task could not be added.

### 参见

-   <span class="methodname">GearmanClient::addTask</span>
-   <span class="methodname">GearmanClient::addTaskHigh</span>
-   <span class="methodname">GearmanClient::addTaskLow</span>
-   <span class="methodname">GearmanClient::addTaskBackground</span>
-   <span class="methodname">GearmanClient::addTaskHighBackground</span>
-   <span class="methodname">GearmanClient::runTasks</span>

GearmanClient::addTaskStatus
============================

Add a task to get status

### 说明

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">GearmanClient::addTaskStatus</span> ( <span
class="methodparam"><span class="type">string</span>
`$job_handle`</span> \[, <span class="methodparam"><span
class="type">string</span> `&$context`</span> \] )

Used to request status information from the Gearman server, which will
call the specified status callback (set using <span
class="methodname">GearmanClient::setStatusCallback</span>).

### 参数

`job_handle`  
The job handle for the task to get status for

`context`  
Data to be passed to the status callback, generally a reference to an
array or object

### 返回值

A <span class="classname">GearmanTask</span> object.

### 范例

**示例 \#1 Monitor completion of multiple background tasks**

An artificial delay is introduced in the worker in this example to
simulate a long running process. There is only one worker running for
this example.

``` php
<?php

/* create our object */
$gmclient= new GearmanClient();

/* add the default server */
$gmclient->addServer();

/* start some background jobs and save the handles */
$handles = array();
$handles[0] = $gmclient->doBackground("reverse", "Hello World!");
$handles[1] = $gmclient->doBackground("reverse", "!dlroW olleH");

$gmclient->setStatusCallback("reverse_status");

/* Poll the server to see when those background jobs finish; */
/* a better method would be to use event callbacks */
do
{
   /* Use the context variable to track how many tasks have completed */
   $done = 0;
   $gmclient->addTaskStatus($handles[0], &$done);
   $gmclient->addTaskStatus($handles[1], &$done);
   $gmclient->runTasks();
   echo "Done: $done\n";
   sleep(1);
}
while ($done != 2);

function reverse_status($task, $done)
{
   if (!$task->isKnown())
      $done++;
}

?>
```

以上例程的输出类似于：

    Done: 0
    Done: 0
    Done: 0
    Done: 0
    Done: 0
    Done: 0
    Done: 0
    Done: 0
    Done: 0
    Done: 0
    Done: 0
    Done: 0
    Done: 1
    Done: 1
    Done: 1
    Done: 1
    Done: 1
    Done: 1
    Done: 1
    Done: 1
    Done: 1
    Done: 1
    Done: 1
    Done: 1
    Done: 2

### 参见

-   <span class="methodname">GearmanClient::setStatusCallback</span>

GearmanClient::clearCallbacks
=============================

Clear all task callback functions

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::clearCallbacks</span> ( <span
class="methodparam">void</span> )

Clears all the task callback functions that have previously been set.

### 参数

此函数没有参数。

### 返回值

Always returns **`TRUE`**.

### 参见

-   <span class="methodname">GearmanClient::setDataCallback</span>
-   <span class="methodname">GearmanClient::setCompleteCallback</span>
-   <span class="methodname">GearmanClient::setCreatedCallback</span>
-   <span class="methodname">GearmanClient::setExceptionCallback</span>
-   <span class="methodname">GearmanClient::setFailCallback</span>
-   <span class="methodname">GearmanClient::setStatusCallback</span>
-   <span class="methodname">GearmanClient::setWarningCallback</span>
-   <span class="methodname">GearmanClient::setWorkloadCallback</span>

GearmanClient::clone
====================

Create a copy of a <span class="classname">GearmanClient</span> object

### 说明

<span class="modifier">public</span> <span
class="type">GearmanClient</span> <span
class="methodname">GearmanClient::clone</span> ( <span
class="methodparam">void</span> )

Creates a copy of a <span class="classname">GearmanClient</span> object.

### 参数

此函数没有参数。

### 返回值

A <span class="classname">GearmanClient</span> on success, **`FALSE`**
on failure.

GearmanClient::\_\_construct
============================

Create a GearmanClient instance

### 说明

<span class="modifier">public</span> <span
class="methodname">GearmanClient::\_\_construct</span> ( <span
class="methodparam">void</span> )

Creates a <span class="classname">GearmanClient</span> instance
representing a client that connects to the job server and submits tasks
to complete.

### 参数

此函数没有参数。

### 返回值

A <span class="classname">GearmanClient</span> object.

### 参见

-   <span class="methodname">GearmanClient::clone</span>

GearmanClient::context
======================

Get the application context

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanClient::context</span> ( <span
class="methodparam">void</span> )

Get the application context previously set with <span
class="methodname">GearmanClient::setContext</span>.

### 参数

此函数没有参数。

### 返回值

The same context data structure set with <span
class="methodname">GearmanClient::setContext</span>

### 参见

-   <span class="methodname">GearmanClient::setContext</span>

GearmanClient::data
===================

Get the application data (deprecated)

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanClient::data</span> ( <span
class="methodparam">void</span> )

Get the application data previously set with <span
class="methodname">GearmanClient::setData</span>.

> **Note**:
>
> This method was replaced by <span
> class="methodname">GearmanClient::setContext</span> in the 0.6.0
> release of the Gearman extension.

### 参数

此函数没有参数。

### 返回值

The same string data set with <span
class="methodname">GearmanClient::setData</span>

### 参见

-   <span class="methodname">GearmanClient::setData</span>

GearmanClient::do
=================

Run a single task and return a result \[deprecated\]

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanClient::do</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">string</span> `$unique`</span> \]
)

The <span class="methodname">GearmanClient::do</span> method is
deprecated as of pecl/gearman 1.0.0. Use <span
class="methodname">GearmanClient::doNormal</span>.

### 参数

`function_name`  
由程序自动执行的已注册函数。

`workload`  
被处理的序列化数据。

`unique`  
用于标识特定任务的唯一性 ID。

### 返回值

A string representing the results of running a task.

### 范例

**示例 \#1 Simple job submission with immediate return**

``` php
<?php

# Client code

echo "Starting\n";

# Create our client object.
$gmclient= new GearmanClient();

# Add default server (localhost).
$gmclient->addServer();

echo "Sending job\n";

$result = $gmclient->doNormal("reverse", "Hello!");

echo "Success: $result\n";

?>
```

``` php
<?php

echo "Starting\n";

# Create our worker object.
$gmworker= new GearmanWorker();

# Add default server (localhost).
$gmworker->addServer();

# Register function "reverse" with the server. Change the worker function to
# "reverse_fn_fast" for a faster worker with no output.
$gmworker->addFunction("reverse", "reverse_fn");

print "Waiting for job...\n";
while($gmworker->work())
{
  if ($gmworker->returnCode() != GEARMAN_SUCCESS)
  {
    echo "return_code: " . $gmworker->returnCode() . "\n";
    break;
  }
}

function reverse_fn($job)
{
  return strrev($job->workload());
}

?>
```

以上例程的输出类似于：

    Starting
    Sending job
    Success: !olleH

**示例 \#2 Submitting a job and retrieving incremental status**

A job is submitted and the script loops to retrieve status information.
The worker has an artificial delay which results in a long running job
and sends status and data as processing occurs. Each subsequent call to
<span class="methodname">GearmanClient::do</span> produces status
information on the running job.

``` php
<?php

# Client code

# Create our client object.
$gmclient= new GearmanClient();

# Add default server (localhost).
$gmclient->addServer();

echo "Sending job\n";

# Send reverse job
do
{
  $result = $gmclient->doNormal("reverse", "Hello!");
  # Check for various return packets and errors.

  switch($gmclient->returnCode())
  {
    case GEARMAN_WORK_DATA:
      echo "Data: $result\n";
      break;
    case GEARMAN_WORK_STATUS:
      list($numerator, $denominator)= $gmclient->doStatus();
      echo "Status: $numerator/$denominator complete\n";
      break;
    case GEARMAN_WORK_FAIL:
      echo "Failed\n";
      exit;
    case GEARMAN_SUCCESS:
      break;
    default:
      echo "RET: " . $gmclient->returnCode() . "\n";
      echo "Error: " . $gmclient->error() . "\n";
      echo "Errno: " . $gmclient->getErrno() . "\n";
      exit;
  }
}
while($gmclient->returnCode() != GEARMAN_SUCCESS);

echo "Success: $result\n";

?>
```

``` php
<?php

# Worker code

echo "Starting\n";

# Create our worker object.
$gmworker= new GearmanWorker();

# Add default server (localhost).
$gmworker->addServer();

# Register function "reverse" with the server.
$gmworker->addFunction("reverse", "reverse_fn");

print "Waiting for job...\n";
while($gmworker->work())
{
  if ($gmworker->returnCode() != GEARMAN_SUCCESS)
  {
    echo "return_code: " . $gmworker->returnCode() . "\n";
    break;
  }
}

function reverse_fn($job)
{
  echo "Received job: " . $job->handle() . "\n";

  $workload = $job->workload();
  $workload_size = $job->workloadSize();

  echo "Workload: $workload ($workload_size)\n";

  # This status loop is not needed, just showing how it works
  for ($x= 0; $x < $workload_size; $x++)
  {
    echo "Sending status: " + $x + 1 . "/$workload_size complete\n";
    $job->sendStatus($x+1, $workload_size);
    $job->sendData(substr($workload, $x, 1));
    sleep(1);
  }

  $result= strrev($workload);
  echo "Result: $result\n";

  # Return what we want to send back to the client.
  return $result;
}

?>
```

以上例程的输出类似于：

Worker output:

    Starting
    Waiting for job...
    Received job: H:foo.local:106
    Workload: Hello! (6)
    1/6 complete
    2/6 complete
    3/6 complete
    4/6 complete
    5/6 complete
    6/6 complete
    Result: !olleH

Client output:

    Starting
    Sending job
    Status: 1/6 complete
    Data: H
    Status: 2/6 complete
    Data: e
    Status: 3/6 complete
    Data: l
    Status: 4/6 complete
    Data: l
    Status: 5/6 complete
    Data: o
    Status: 6/6 complete
    Data: !
    Success: !olleH

### 参见

-   <span class="methodname">GearmanClient::doHigh</span>
-   <span class="methodname">GearmanClient::doLow</span>
-   <span class="methodname">GearmanClient::doBackground</span>
-   <span class="methodname">GearmanClient::doHighBackground</span>
-   <span class="methodname">GearmanClient::doLowBackground</span>

GearmanClient::doBackground
===========================

Run a task in the background

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanClient::doBackground</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">string</span> `$unique`</span> \]
)

Runs a task in the background, returning a job handle which can be used
to get the status of the running task.

### 参数

`function_name`  
由程序自动执行的已注册函数。

`workload`  
被处理的序列化数据。

`unique`  
用于标识特定任务的唯一性 ID。

### 返回值

The job handle for the submitted task.

### 范例

**示例 \#1 Submit and monitor a background job**

The worker in this example has an artificial delay introduced to mimic a
long running job. The client script periodically checks the status of
the running job.

``` php
<?php

/* create our object */
$gmclient= new GearmanClient();

/* add the default server */
$gmclient->addServer();

/* run reverse client */
$job_handle = $gmclient->doBackground("reverse", "this is a test");

if ($gmclient->returnCode() != GEARMAN_SUCCESS)
{
  echo "bad return code\n";
  exit;
}

$done = false;
do
{
   sleep(3);
   $stat = $gmclient->jobStatus($job_handle);
   if (!$stat[0]) // the job is known so it is not done
      $done = true;
   echo "Running: " . ($stat[1] ? "true" : "false") . ", numerator: " . $stat[2] . ", denominator: " . $stat[3] . "\n";
}
while(!$done);

echo "done!\n";

?>
```

以上例程的输出类似于：

    Running: true, numerator: 3, denominator: 14
    Running: true, numerator: 6, denominator: 14
    Running: true, numerator: 9, denominator: 14
    Running: true, numerator: 12, denominator: 14
    Running: false, numerator: 0, denominator: 0
    done!

### 参见

-   <span class="methodname">GearmanClient::doNormal</span>
-   <span class="methodname">GearmanClient::doHigh</span>
-   <span class="methodname">GearmanClient::doLow</span>
-   <span class="methodname">GearmanClient::doHighBackground</span>
-   <span class="methodname">GearmanClient::doLowBackground</span>

GearmanClient::doHigh
=====================

Run a single high priority task

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanClient::doHigh</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">string</span> `$unique`</span> \]
)

Runs a single high priority task and returns a string representation of
the result. It is up to the <span class="classname">GearmanClient</span>
and <span class="classname">GearmanWorker</span> to agree on the format
of the result. High priority tasks will get precedence over normal and
low priority tasks in the job queue.

### 参数

`function_name`  
由程序自动执行的已注册函数。

`workload`  
被处理的序列化数据。

`unique`  
用于标识特定任务的唯一性 ID。

### 返回值

A string representing the results of running a task.

### 参见

-   <span class="methodname">GearmanClient::doNormal</span>
-   <span class="methodname">GearmanClient::doLow</span>
-   <span class="methodname">GearmanClient::doBackground</span>
-   <span class="methodname">GearmanClient::doHighBackground</span>
-   <span class="methodname">GearmanClient::doLowBackground</span>

GearmanClient::doHighBackground
===============================

Run a high priority task in the background

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanClient::doHighBackground</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">string</span> `$unique`</span> \]
)

Runs a high priority task in the background, returning a job handle
which can be used to get the status of the running task. High priority
tasks take precedence over normal and low priority tasks in the job
queue.

### 参数

`function_name`  
由程序自动执行的已注册函数。

`workload`  
被处理的序列化数据。

`unique`  
用于标识特定任务的唯一性 ID。

### 返回值

The job handle for the submitted task.

### 参见

-   <span class="methodname">GearmanClient::doNormal</span>
-   <span class="methodname">GearmanClient::doHigh</span>
-   <span class="methodname">GearmanClient::doLow</span>
-   <span class="methodname">GearmanClient::doBackground</span>
-   <span class="methodname">GearmanClient::doLowBackground</span>

GearmanClient::doJobHandle
==========================

Get the job handle for the running task

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanClient::doJobHandle</span> ( <span
class="methodparam">void</span> )

Gets that job handle for a running task. This should be used between
repeated <span class="methodname">GearmanClient::doNormal</span> calls.
The job handle can then be used to get information on the task.

### 参数

此函数没有参数。

### 返回值

The job handle for the running task.

### 参见

-   <span class="methodname">GearmanClient::jobStatus</span>

GearmanClient::doLow
====================

Run a single low priority task

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanClient::doLow</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">string</span> `$unique`</span> \]
)

Runs a single low priority task and returns a string representation of
the result. It is up to the <span class="classname">GearmanClient</span>
and <span class="classname">GearmanWorker</span> to agree on the format
of the result. Normal and high priority tasks will get precedence over
low priority tasks in the job queue.

### 参数

`function_name`  
由程序自动执行的已注册函数。

`workload`  
被处理的序列化数据。

`unique`  
用于标识特定任务的唯一性 ID。

### 返回值

A string representing the results of running a task.

### 参见

-   <span class="methodname">GearmanClient::doNormal</span>
-   <span class="methodname">GearmanClient::doHigh</span>
-   <span class="methodname">GearmanClient::doBackground</span>
-   <span class="methodname">GearmanClient::doHighBackground</span>
-   <span class="methodname">GearmanClient::doLowBackground</span>

GearmanClient::doLowBackground
==============================

Run a low priority task in the background

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanClient::doLowBackground</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">string</span> `$unique`</span> \]
)

Runs a low priority task in the background, returning a job handle which
can be used to get the status of the running task. Normal and high
priority tasks take precedence over low priority tasks in the job queue.

### 参数

`function_name`  
由程序自动执行的已注册函数。

`workload`  
被处理的序列化数据。

`unique`  
用于标识特定任务的唯一性 ID。

### 返回值

The job handle for the submitted task.

### 参见

-   <span class="methodname">GearmanClient::doNormal</span>
-   <span class="methodname">GearmanClient::doHigh</span>
-   <span class="methodname">GearmanClient::doLow</span>
-   <span class="methodname">GearmanClient::doBackground</span>
-   <span class="methodname">GearmanClient::doHighBackground</span>

GearmanClient::doNormal
=======================

Run a single task and return a result

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanClient::doNormal</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$workload`</span> \[, <span
class="methodparam"><span class="type">string</span> `$unique`</span> \]
)

Runs a single task and returns a string representation of the result. It
is up to the <span class="classname">GearmanClient</span> and <span
class="classname">GearmanWorker</span> to agree on the format of the
result.

### 参数

`function_name`  
由程序自动执行的已注册函数。

`workload`  
被处理的序列化数据。

`unique`  
用于标识特定任务的唯一性 ID。

### 返回值

A string representing the results of running a task.

### 范例

**示例 \#1 Simple job submission with immediate return**

``` php
<?php

?>
```

``` php
<?php

# Client code

echo "Starting\n";

# Create our client object.
$gmclient= new GearmanClient();

# Add default server (localhost).
$gmclient->addServer();

echo "Sending job\n";

$result = $gmclient->doNormal("reverse", "Hello!");

echo "Success: $result\n";

?>
```

``` php
<?php

echo "Starting\n";

# Create our worker object.
$gmworker= new GearmanWorker();

# Add default server (localhost).
$gmworker->addServer();

# Register function "reverse" with the server. Change the worker function to
# "reverse_fn_fast" for a faster worker with no output.
$gmworker->addFunction("reverse", "reverse_fn");

print "Waiting for job...\n";
while($gmworker->work())
{
  if ($gmworker->returnCode() != GEARMAN_SUCCESS)
  {
    echo "return_code: " . $gmworker->returnCode() . "\n";
    break;
  }
}

function reverse_fn($job)
{
  return strrev($job->workload());
}

?>
```

以上例程的输出类似于：

    Starting
    Sending job
    Success: !olleH

**示例 \#2 Submitting a job and retrieving incremental status**

A job is submitted and the script loops to retrieve status information.
The worker has an artificial delay which results in a long running job
and sends status and data as processing occurs. Each subsequent call to
<span class="methodname">GearmanClient::doNormal</span> produces status
information on the running job.

``` php
<?php

# Client code

# Create our client object.
$gmclient= new GearmanClient();

# Add default server (localhost).
$gmclient->addServer();

echo "Sending job\n";

# Send reverse job
do
{
  $result = $gmclient->doNormal("reverse", "Hello!");
  # Check for various return packets and errors.

  switch($gmclient->returnCode())
  {
    case GEARMAN_WORK_DATA:
      echo "Data: $result\n";
      break;
    case GEARMAN_WORK_STATUS:
      list($numerator, $denominator)= $gmclient->doStatus();
      echo "Status: $numerator/$denominator complete\n";
      break;
    case GEARMAN_WORK_FAIL:
      echo "Failed\n";
      exit;
    case GEARMAN_SUCCESS:
      break;
    default:
      echo "RET: " . $gmclient->returnCode() . "\n";
      echo "Error: " . $gmclient->error() . "\n";
      echo "Errno: " . $gmclient->getErrno() . "\n";
      exit;
  }
}
while($gmclient->returnCode() != GEARMAN_SUCCESS);

echo "Success: $result\n";

?>
```

``` php
<?php

# Worker code

echo "Starting\n";

# Create our worker object.
$gmworker= new GearmanWorker();

# Add default server (localhost).
$gmworker->addServer();

# Register function "reverse" with the server.
$gmworker->addFunction("reverse", "reverse_fn");

print "Waiting for job...\n";
while($gmworker->work())
{
  if ($gmworker->returnCode() != GEARMAN_SUCCESS)
  {
    echo "return_code: " . $gmworker->returnCode() . "\n";
    break;
  }
}

function reverse_fn($job)
{
  echo "Received job: " . $job->handle() . "\n";

  $workload = $job->workload();
  $workload_size = $job->workloadSize();

  echo "Workload: $workload ($workload_size)\n";

  # This status loop is not needed, just showing how it works
  for ($x= 0; $x < $workload_size; $x++)
  {
    echo "Sending status: " + $x + 1 . "/$workload_size complete\n";
    $job->sendStatus($x+1, $workload_size);
    $job->sendData(substr($workload, $x, 1));
    sleep(1);
  }

  $result= strrev($workload);
  echo "Result: $result\n";

  # Return what we want to send back to the client.
  return $result;
}

?>
```

以上例程的输出类似于：

Worker output:

    Starting
    Waiting for job...
    Received job: H:foo.local:106
    Workload: Hello! (6)
    1/6 complete
    2/6 complete
    3/6 complete
    4/6 complete
    5/6 complete
    6/6 complete
    Result: !olleH

Client output:

    Starting
    Sending job
    Status: 1/6 complete
    Data: H
    Status: 2/6 complete
    Data: e
    Status: 3/6 complete
    Data: l
    Status: 4/6 complete
    Data: l
    Status: 5/6 complete
    Data: o
    Status: 6/6 complete
    Data: !
    Success: !olleH

### 参见

-   <span class="methodname">GearmanClient::doHigh</span>
-   <span class="methodname">GearmanClient::doLow</span>
-   <span class="methodname">GearmanClient::doBackground</span>
-   <span class="methodname">GearmanClient::doHighBackground</span>
-   <span class="methodname">GearmanClient::doLowBackground</span>

GearmanClient::doStatus
=======================

Get the status for the running task

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">GearmanClient::doStatus</span> ( <span
class="methodparam">void</span> )

Returns the status for the running task. This should be used between
repeated <span class="methodname">GearmanClient::doNormal</span> calls.

### 参数

此函数没有参数。

### 返回值

An array representing the percentage completion given as a fraction,
with the first element the numerator and the second element the
denomintor.

### 范例

**示例 \#1 Get the status of a long running job**

The worker in this example has an artificial delay added during
processing of the string to be reversed. After each delay it calls <span
class="methodname">GearmanJob::status</span> which the client then picks
up.

``` php
<?php

echo "Starting\n";

# Create our client object.
$gmclient= new GearmanClient();

# Add default server (localhost).
$gmclient->addServer();

echo "Sending job\n";

# Send reverse job
do
{
  $result = $gmclient->doNormal("reverse", "Hello!");

  # Check for various return packets and errors.
  switch($gmclient->returnCode())
  {
    case GEARMAN_WORK_DATA:
      break;
    case GEARMAN_WORK_STATUS:
      # get the current job status
      list($numerator, $denominator)= $gmclient->doStatus();
      echo "Status: $numerator/$denominator complete\n";
      break;
    case GEARMAN_WORK_FAIL:
      echo "Failed\n";
      exit;
    case GEARMAN_SUCCESS:
      break;
    default:
      echo "RET: " . $gmclient->returnCode() . "\n";
      exit;
  }
}
while($gmclient->returnCode() != GEARMAN_SUCCESS);

echo "Success: $result\n";

?>
```

以上例程的输出类似于：

    Starting
    Sending job
    Status: 1/6 complete
    Status: 2/6 complete
    Status: 3/6 complete
    Status: 4/6 complete
    Status: 5/6 complete
    Status: 6/6 complete
    Success: !olleH

### 参见

-   <span class="methodname">GearmanClient::doNormal</span>
-   <span class="methodname">GearmanJob::status</span>

GearmanClient::echo
===================

Send data to all job servers to see if they echo it back \[deprecated\]

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::echo</span> ( <span
class="methodparam"><span class="type">string</span> `$workload`</span>
)

The <span class="methodname">GearmanClient::echo</span> method is
deprecated as of pecl/gearman 1.0.0. Use <span
class="methodname">GearmanClient::ping</span>.

### 参数

`workload`  
Some arbitrary serialized data to be echo back

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

GearmanClient::error
====================

Returns an error string for the last error encountered

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanClient::error</span> ( <span
class="methodparam">void</span> )

Returns an error string for the last error encountered.

### 参数

此函数没有参数。

### 返回值

A human readable error string.

### 参见

-   <span class="methodname">GearmanClient::getErrno</span>

GearmanClient::getErrno
=======================

Get an errno value

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanClient::getErrno</span> ( <span
class="methodparam">void</span> )

Value of errno in the case of a GEARMAN\_ERRNO return value.

### 参数

此函数没有参数。

### 返回值

A valid Gearman errno.

### 参见

-   <span class="methodname">GearmanClient::error</span>

GearmanClient::jobStatus
========================

gearman\_job\_status
====================

Get the status of a background job

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">GearmanClient::jobStatus</span> ( <span
class="methodparam"><span class="type">string</span>
`$job_handle`</span> )

Gets the status for a background job given a job handle. The status
information will specify whether the job is known, whether the job is
currently running, and the percentage completion.

### 参数

`job_handle`  
由 Gearman 服务器指派的工作句柄。

### 返回值

An array containing status information for the job corresponding to the
supplied job handle. The first array element is a boolean indicating
whether the job is even known, the second is a boolean indicating
whether the job is still running, and the third and fourth elements
correspond to the numerator and denominator of the fractional completion
percentage, respectively.

### 范例

**示例 \#1 Monitor the status of a long running background job**

``` php
<?php

/* create our object */
$gmclient= new GearmanClient();

/* add the default server */
$gmclient->addServer();

/* run reverse client */
$job_handle = $gmclient->doBackground("reverse", "this is a test");

if ($gmclient->returnCode() != GEARMAN_SUCCESS)
{
  echo "bad return code\n";
  exit;
}

$done = false;
do
{
   sleep(3);
   $stat = $gmclient->jobStatus($job_handle);
   if (!$stat[0]) // the job is known so it is not done
      $done = true;
   echo "Running: " . ($stat[1] ? "true" : "false") . ", numerator: " . $stat[2] . ", denomintor: " . $stat[3] . "\n";
}
while(!$done);

echo "done!\n";

?>
```

以上例程的输出类似于：

    Running: true, numerator: 3, denomintor: 14
    Running: true, numerator: 6, denomintor: 14
    Running: true, numerator: 9, denomintor: 14
    Running: true, numerator: 12, denomintor: 14
    Running: false, numerator: 0, denomintor: 0
    done!

### 参见

-   <span class="methodname">GearmanClient::doStatus</span>

GearmanClient::ping
===================

Send data to all job servers to see if they echo it back

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::ping</span> ( <span
class="methodparam"><span class="type">string</span> `$workload`</span>
)

Sends some arbitrary data to all job servers to see if they echo it
back. The data sent is not used or processed in any other way. Primarily
used for testing and debugging.

### 参数

`workload`  
Some arbitrary serialized data to be echo back

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

GearmanClient::removeOptions
============================

Remove client options

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::removeOptions</span> ( <span
class="methodparam"><span class="type">int</span> `$options`</span> )

Removes (unsets) one or more options.

### 参数

`options`  
The options to be removed (unset)

### 返回值

Always returns **`TRUE`**.

GearmanClient::returnCode
=========================

Get the last Gearman return code

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanClient::returnCode</span> ( <span
class="methodparam">void</span> )

Returns the last Gearman return code.

### 参数

此函数没有参数。

### 返回值

A valid Gearman return code.

GearmanClient::runTasks
=======================

Run a list of tasks in parallel

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::runTasks</span> ( <span
class="methodparam">void</span> )

For a set of tasks previously added with <span
class="methodname">GearmanClient::addTask</span>, <span
class="methodname">GearmanClient::addTaskHigh</span>, <span
class="methodname">GearmanClient::addTaskLow</span>, <span
class="methodname">GearmanClient::addTaskBackground</span>, <span
class="methodname">GearmanClient::addTaskHighBackground</span>, or <span
class="methodname">GearmanClient::addTaskLowBackground</span>, this call
starts running the tasks in parallel.

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanClient::addTask</span>

GearmanClient::setClientCallback
================================

Callback function when there is a data packet for a task (deprecated)

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">GearmanClient::setClientCallback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Sets the callback function for accepting data packets for a task. The
callback function should take a single argument, a <span
class="classname">GearmanTask</span> object.

> **Note**:
>
> This method has been replaced by <span
> class="methodname">GearmanClient::setDataCallback</span> in the 0.6.0
> release of the Gearman extension.

### 参数

`callback`  
A function or method to call

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanClient::setCompleteCallback</span>
-   <span class="methodname">GearmanClient::setCreatedCallback</span>
-   <span class="methodname">GearmanClient::setDataCallback</span>
-   <span class="methodname">GearmanClient::setExceptionCallback</span>
-   <span class="methodname">GearmanClient::setFailCallback</span>
-   <span class="methodname">GearmanClient::setStatusCallback</span>
-   <span class="methodname">GearmanClient::setWarningCallback</span>
-   <span class="methodname">GearmanClient::setWorkloadCallback</span>

GearmanClient::setCompleteCallback
==================================

Set a function to be called on task completion

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::setCompleteCallback</span> (
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Use to set a function to be called when a <span
class="classname">GearmanTask</span> is completed, or when <span
class="methodname">GearmanJob::sendComplete</span> is invoked by a
worker (whichever happens first).

This callback executes only when executing a <span
class="classname">GearmanTask</span> using <span
class="methodname">GearmanClient::runTasks</span>. It is not used for
individual jobs.

### 参数

`callback`  
A function to be called

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanClient::setDataCallback</span>
-   <span class="methodname">GearmanClient::setCreatedCallback</span>
-   <span class="methodname">GearmanClient::setExceptionCallback</span>
-   <span class="methodname">GearmanClient::setFailCallback</span>
-   <span class="methodname">GearmanClient::setStatusCallback</span>
-   <span class="methodname">GearmanClient::setWarningCallback</span>
-   <span class="methodname">GearmanClient::setWorkloadCallback</span>

GearmanClient::setContext
=========================

Set application context

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::setContext</span> ( <span
class="methodparam"><span class="type">string</span> `$context`</span> )

Sets an arbitrary string to provide application context that can later
be retrieved by <span class="methodname">GearmanClient::context</span>.

### 参数

`context`  
Arbitrary context data

### 返回值

Always returns **`TRUE`**.

### 参见

-   <span class="methodname">GearmanClient::context</span>

GearmanClient::setCreatedCallback
=================================

Set a callback for when a task is queued

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::setCreatedCallback</span> (
<span class="methodparam"><span class="type">string</span>
`$callback`</span> )

Sets a function to be called when a task is received and queued by the
Gearman job server. The callback should accept a single argument, a
<span class="classname">GearmanTask</span> object.

### 参数

`callback`  
A function to call

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanClient::setDataCallback</span>
-   <span class="methodname">GearmanClient::setCompleteCallback</span>
-   <span class="methodname">GearmanClient::setExceptionCallback</span>
-   <span class="methodname">GearmanClient::setFailCallback</span>
-   <span class="methodname">GearmanClient::setStatusCallback</span>
-   <span class="methodname">GearmanClient::setWarningCallback</span>
-   <span class="methodname">GearmanClient::setWorkloadCallback</span>

GearmanClient::setData
======================

Set application data (deprecated)

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::setData</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

Sets some arbitrary application data that can later be retrieved by
<span class="methodname">GearmanClient::data</span>.

> **Note**:
>
> This method has been replaced by <span
> class="methodname">GearmanCient::setContext</span> in the 0.6.0
> release of the Gearman extension.

### 参数

`data`  

### 返回值

Always returns **`TRUE`**.

### 参见

-   <span class="methodname">GearmanClient::data</span>

GearmanClient::setDataCallback
==============================

Callback function when there is a data packet for a task

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::setDataCallback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Sets the callback function for accepting data packets for a task. The
callback function should take a single argument, a <span
class="classname">GearmanTask</span> object.

### 参数

`callback`  
A function or method to call

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanClient::setCompleteCallback</span>
-   <span class="methodname">GearmanClient::setCreatedCallback</span>
-   <span class="methodname">GearmanClient::setExceptionCallback</span>
-   <span class="methodname">GearmanClient::setFailCallback</span>
-   <span class="methodname">GearmanClient::setStatusCallback</span>
-   <span class="methodname">GearmanClient::setWarningCallback</span>
-   <span class="methodname">GearmanClient::setWorkloadCallback</span>

GearmanClient::setExceptionCallback
===================================

Set a callback for worker exceptions

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::setExceptionCallback</span> (
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Specifies a function to call when a worker for a task sends an
exception.

### 参数

`callback`  
Function to call when the worker throws an exception

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanClient::setDataCallback</span>
-   <span class="methodname">GearmanClient::setCompleteCallback</span>
-   <span class="methodname">GearmanClient::setCreatedCallback</span>
-   <span class="methodname">GearmanClient::setFailCallback</span>
-   <span class="methodname">GearmanClient::setStatusCallback</span>
-   <span class="methodname">GearmanClient::setWarningCallback</span>
-   <span class="methodname">GearmanClient::setWorkloadCallback</span>

GearmanClient::setFailCallback
==============================

Set callback for job failure

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::setFailCallback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Sets the callback function to be used when a task does not complete
successfully. The function should accept a single argument, a <span
class="classname">GearmanTask</span> object.

### 参数

`callback`  
A function to call

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanClient::setDataCallback</span>
-   <span class="methodname">GearmanClient::setCompleteCallback</span>
-   <span class="methodname">GearmanClient::setCreatedCallback</span>
-   <span class="methodname">GearmanClient::setExceptionCallback</span>
-   <span class="methodname">GearmanClient::setStatusCallback</span>
-   <span class="methodname">GearmanClient::setWarningCallback</span>
-   <span class="methodname">GearmanClient::setWorkloadCallback</span>

GearmanClient::setOptions
=========================

Set client options

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::setOptions</span> ( <span
class="methodparam"><span class="type">int</span> `$options`</span> )

Sets one or more client options.

### 参数

`options`  
The options to be set

### 返回值

Always returns **`TRUE`**.

GearmanClient::setStatusCallback
================================

Set a callback for collecting task status

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::setStatusCallback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Sets a callback function used for getting updated status information
from a worker. The function should accept a single argument, a <span
class="classname">GearmanTask</span> object.

### 参数

`callback`  
A function to call

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanClient::setDataCallback</span>
-   <span class="methodname">GearmanClient::setCompleteCallback</span>
-   <span class="methodname">GearmanClient::setCreatedCallback</span>
-   <span class="methodname">GearmanClient::setExceptionCallback</span>
-   <span class="methodname">GearmanClient::setFailCallback</span>
-   <span class="methodname">GearmanClient::setWarningCallback</span>
-   <span class="methodname">GearmanClient::setWorkloadCallback</span>

GearmanClient::setTimeout
=========================

Set socket I/O activity timeout

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::setTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$timeout`</span> )

Sets the timeout for socket I/O activity.

### 参数

`timeout`  
An interval of time in milliseconds

### 返回值

Always returns **`TRUE`**.

GearmanClient::setWarningCallback
=================================

Set a callback for worker warnings

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::setWarningCallback</span> (
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Sets a function to be called when a worker sends a warning. The callback
should accept a single argument, a <span
class="classname">GearmanTask</span> object.

### 参数

`callback`  
A function to call

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanClient::setDataCallback</span>
-   <span class="methodname">GearmanClient::setCompleteCallback</span>
-   <span class="methodname">GearmanClient::setCreatedCallback</span>
-   <span class="methodname">GearmanClient::setExceptionCallback</span>
-   <span class="methodname">GearmanClient::setFailCallback</span>
-   <span class="methodname">GearmanClient::setStatusCallback</span>
-   <span class="methodname">GearmanClient::setWorkloadCallback</span>

GearmanClient::setWorkloadCallback
==================================

Set a callback for accepting incremental data updates

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanClient::setWorkloadCallback</span> (
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Sets a function to be called when a worker needs to send back data prior
to job completion. A worker can do this when it needs to send updates,
send partial results, or flush data during long running jobs. The
callback should accept a single argument, a <span
class="classname">GearmanTask</span> object.

### 参数

`callback`  
A function to call

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanClient::setDataCallback</span>
-   <span class="methodname">GearmanClient::setCompleteCallback</span>
-   <span class="methodname">GearmanClient::setCreatedCallback</span>
-   <span class="methodname">GearmanClient::setExceptionCallback</span>
-   <span class="methodname">GearmanClient::setFailCallback</span>
-   <span class="methodname">GearmanClient::setStatusCallback</span>
-   <span class="methodname">GearmanClient::setWarningCallback</span>

GearmanClient::timeout
======================

Get current socket I/O activity timeout value

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanClient::timeout</span> ( <span
class="methodparam">void</span> )

Returns the timeout in milliseconds to wait for I/O activity.

### 参数

此函数没有参数。

### 返回值

Timeout in milliseconds to wait for I/O activity. A negative value means
an infinite timeout.

### 参见

-   <span class="methodname">GearmanClient::setTimeout</span>

简介
----

类摘要
------

**GearmanJob**

<span class="ooclass"> class **GearmanJob** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">complete</span> ( <span
class="methodparam"><span class="type">string</span> `$result`</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">data</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">exception</span> ( <span
class="methodparam"><span class="type">string</span> `$exception`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">fail</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">functionName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">handle</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">returnCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sendComplete</span> ( <span
class="methodparam"><span class="type">string</span> `$result`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sendData</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sendException</span> ( <span
class="methodparam"><span class="type">string</span> `$exception`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sendFail</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sendStatus</span> ( <span
class="methodparam"><span class="type">int</span> `$numerator`</span> ,
<span class="methodparam"><span class="type">int</span>
`$denominator`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sendWarning</span> ( <span
class="methodparam"><span class="type">string</span> `$warning`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setReturn</span> ( <span
class="methodparam"><span class="type">int</span>
`$gearman_return_t`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">status</span> ( <span class="methodparam"><span
class="type">int</span> `$numerator`</span> , <span
class="methodparam"><span class="type">int</span> `$denominator`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">unique</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">warning</span> ( <span
class="methodparam"><span class="type">string</span> `$warning`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">workload</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">workloadSize</span> ( <span
class="methodparam">void</span> )

}

GearmanJob::complete
====================

Send the result and complete status (deprecated)

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanJob::complete</span> ( <span
class="methodparam"><span class="type">string</span> `$result`</span> )

Sends result data and the complete status update for this job.

> **Note**:
>
> This method has been replaced by <span
> class="methodname">GearmanJob::sendComplete</span> in the 0.6.0
> release of the Gearman extension.

### 参数

`result`  
Serialized result data.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanJob::sendFail</span>
-   <span class="methodname">GearmanJob::setReturn</span>

GearmanJob::\_\_construct
=========================

Create a GearmanJob instance

### 说明

<span class="modifier">public</span> <span
class="methodname">GearmanJob::\_\_construct</span> ( <span
class="methodparam">void</span> )

Creates a <span class="classname">GearmanJob</span> instance
representing a job the worker is to complete.

### 参数

此函数没有参数。

### 返回值

A <span class="classname">GearmanJob</span> object.

GearmanJob::data
================

Send data for a running job (deprecated)

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanJob::data</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

Sends data to the job server (and any listening clients) for this job.

> **Note**:
>
> This method has been replaced by <span
> class="methodname">GearmanJob::sendData</span> in the 0.6.0 release of
> the Gearman extension.

### 参数

`data`  
Arbitrary serialized data.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanJob::workload</span>
-   <span class="methodname">GearmanTask::data</span>

GearmanJob::exception
=====================

Send exception for running job (deprecated)

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanJob::exception</span> ( <span
class="methodparam"><span class="type">string</span> `$exception`</span>
)

Sends the supplied exception when this job is running.

> **Note**:
>
> This method has been replaced by <span
> class="methodname">GearmanJob::sendException</span> in the 0.6.0
> release of the Gearman extension.

### 参数

`exception`  
An exception description.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanJob::setReturn</span>
-   <span class="methodname">GearmanJob::sendStatus</span>
-   <span class="methodname">GearmanJob::sendWarning</span>

GearmanJob::fail
================

Send fail status (deprecated)

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanJob::fail</span> ( <span
class="methodparam">void</span> )

Sends failure status for this job, indicating that the job failed in a
known way (as opposed to failing due to a thrown exception).

> **Note**:
>
> This method has been replaced by <span
> class="methodname">GearmanJob::sendFail</span> in the 0.6.0 release of
> the Gearman extension.

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanJob::sendException</span>
-   <span class="methodname">GearmanJob::setReturn</span>
-   <span class="methodname">GearmanJob::sendStatus</span>
-   <span class="methodname">GearmanJob::sendWarning</span>

GearmanJob::functionName
========================

Get function name

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanJob::functionName</span> ( <span
class="methodparam">void</span> )

Returns the function name for this job. This is the function the work
will execute to perform the job.

### 参数

此函数没有参数。

### 返回值

The name of a function.

### 参见

-   <span class="methodname">GearmanTask::function</span>

GearmanJob::handle
==================

Get the job handle

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanJob::handle</span> ( <span
class="methodparam">void</span> )

Returns the opaque job handle assigned by the job server.

### 参数

此函数没有参数。

### 返回值

An opaque job handle.

### 参见

-   <span class="methodname">GearmanTask::jobHandle</span>

GearmanJob::returnCode
======================

Get last return code

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanJob::returnCode</span> ( <span
class="methodparam">void</span> )

Returns the last return code issued by the job server.

### 参数

此函数没有参数。

### 返回值

A valid Gearman return code.

### 参见

-   <span class="methodname">GearmanTask::returnCode</span>

GearmanJob::sendComplete
========================

Send the result and complete status

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanJob::sendComplete</span> ( <span
class="methodparam"><span class="type">string</span> `$result`</span> )

Sends result data and the complete status update for this job.

### 参数

`result`  
Serialized result data.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanJob::sendFail</span>
-   <span class="methodname">GearmanJob::setReturn</span>

GearmanJob::sendData
====================

Send data for a running job

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanJob::sendData</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

Sends data to the job server (and any listening clients) for this job.

### 参数

`data`  
Arbitrary serialized data.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanJob::workload</span>
-   <span class="methodname">GearmanTask::data</span>

GearmanJob::sendException
=========================

Send exception for running job (exception)

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanJob::sendException</span> ( <span
class="methodparam"><span class="type">string</span> `$exception`</span>
)

Sends the supplied exception when this job is running.

### 参数

`exception`  
An exception description.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanJob::setReturn</span>
-   <span class="methodname">GearmanJob::sendStatus</span>
-   <span class="methodname">GearmanJob::sendWarning</span>

GearmanJob::sendFail
====================

Send fail status

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanJob::sendFail</span> ( <span
class="methodparam">void</span> )

Sends failure status for this job, indicating that the job failed in a
known way (as opposed to failing due to a thrown exception).

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanJob::sendException</span>
-   <span class="methodname">GearmanJob::setReturn</span>
-   <span class="methodname">GearmanJob::sendStatus</span>
-   <span class="methodname">GearmanJob::sendWarning</span>

GearmanJob::sendStatus
======================

Send status

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanJob::sendStatus</span> ( <span
class="methodparam"><span class="type">int</span> `$numerator`</span> ,
<span class="methodparam"><span class="type">int</span>
`$denominator`</span> )

Sends status information to the job server and any listening clients.
Use this to specify what percentage of the job has been completed.

### 参数

`numerator`  
The numerator of the precentage completed expressed as a fraction.

`denominator`  
The denominator of the precentage completed expressed as a fraction.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanClient::jobStatus</span>
-   <span class="methodname">GearmanTask::taskDenominator</span>
-   <span class="methodname">GearmanTask::taskNumerator</span>

GearmanJob::sendWarning
=======================

Send a warning

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanJob::sendWarning</span> ( <span
class="methodparam"><span class="type">string</span> `$warning`</span> )

Sends a warning for this job while it is running.

### 参数

`warning`  
A warning message.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanJob::sendComplete</span>
-   <span class="methodname">GearmanJob::sendException</span>
-   <span class="methodname">GearmanJob::sendFail</span>

GearmanJob::setReturn
=====================

Set a return value

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanJob::setReturn</span> ( <span
class="methodparam"><span class="type">int</span>
`$gearman_return_t`</span> )

Sets the return value for this job, indicates how the job completed.

### 参数

`gearman_return_t`  
A valid Gearman return value.

### 返回值

Description...

GearmanJob::status
==================

Send status (deprecated)

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanJob::status</span> ( <span
class="methodparam"><span class="type">int</span> `$numerator`</span> ,
<span class="methodparam"><span class="type">int</span>
`$denominator`</span> )

Sends status information to the job server and any listening clients.
Use this to specify what percentage of the job has been completed.

> **Note**:
>
> This method has been replaced by <span
> class="methodname">GearmanJob::sendStatus</span> in the 0.6.0 release
> of the Gearman extenstion.

### 参数

`numerator`  
The numerator of the precentage completed expressed as a fraction.

`denominator`  
The denominator of the precentage completed expressed as a fraction.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanClient::jobStatus</span>
-   <span class="methodname">GearmanTask::taskDenominator</span>
-   <span class="methodname">GearmanTask::taskNumerator</span>

GearmanJob::unique
==================

Get the unique identifier

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanJob::unique</span> ( <span
class="methodparam">void</span> )

Returns the unique identifiter for this job. The identifier is assigned
by the client.

### 参数

此函数没有参数。

### 返回值

An opaque unique identifier.

### 参见

-   <span class="methodname">GearmanClient::do</span>
-   <span class="methodname">GearmanTask::uuid</span>

GearmanJob::warning
===================

Send a warning (deprecated)

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanJob::warning</span> ( <span
class="methodparam"><span class="type">string</span> `$warning`</span> )

Sends a warning for this job while it is running.

> **Note**:
>
> This method has been replaced by <span
> class="methodname">GearmanJob::sendWarning</span> in the 0.6.0 release
> of the Gearman extension.

### 参数

`warning`  
A warning messages.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">GearmanJob::sendComplete</span>
-   <span class="methodname">GearmanJob::sendException</span>
-   <span class="methodname">GearmanJob::sendFail</span>

GearmanJob::workload
====================

Get workload

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanJob::workload</span> ( <span
class="methodparam">void</span> )

Returns the workload for the job. This is serialized data that is to be
processed by the worker.

### 参数

此函数没有参数。

### 返回值

Serialized data.

### 参见

-   <span class="methodname">GearmanClient::do</span>
-   <span class="methodname">GearmanJob::workloadSize</span>

GearmanJob::workloadSize
========================

Get size of work load

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanJob::workloadSize</span> ( <span
class="methodparam">void</span> )

Returns the size of the job's work load (the data the worker is to
process) in bytes.

### 参数

此函数没有参数。

### 返回值

The size in bytes.

### 参见

-   <span class="methodname">GearmanJob::workload</span>

简介
----

类摘要
------

**GearmanTask**

<span class="ooclass"> class **GearmanTask** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span class="methodname">create</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">data</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">dataSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">function</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">functionName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isKnown</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isRunning</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">jobHandle</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">recvData</span> ( <span
class="methodparam"><span class="type">int</span> `$data_len`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">returnCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">sendData</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">sendWorkload</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">taskDenominator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">taskNumerator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">unique</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">uuid</span> ( <span
class="methodparam">void</span> )

}

GearmanTask::\_\_construct
==========================

Create a GearmanTask instance

### 说明

<span class="modifier">public</span> <span
class="methodname">GearmanTask::\_\_construct</span> ( <span
class="methodparam">void</span> )

Creates a <span class="classname">GearmanTask</span> instance
representing a task to be submitted to a job server.

### 参数

此函数没有参数。

### 返回值

A <span class="classname">GearmanTask</span> object.

GearmanTask::create
===================

Create a task (deprecated)

### 说明

<span class="modifier">public</span> <span
class="type">GearmanTask</span> <span
class="methodname">GearmanTask::create</span> ( <span
class="methodparam">void</span> )

Returns a new <span class="classname">GearmanTask</span> object.

> **Note**:
>
> This method was removed in the 0.6.0 version of the Gearman extension.

### 参数

此函数没有参数。

### 返回值

A <span class="classname">GearmanTask</span> oject 或者在失败时返回
**`FALSE`**.

GearmanTask::data
=================

Get data returned for a task

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanTask::data</span> ( <span
class="methodparam">void</span> )

Returns data being returned for a task by a worker.

### 参数

此函数没有参数。

### 返回值

The serialized data, or **`FALSE`** if no data is present.

### 参见

-   <span class="methodname">GearmanTask::dataSize</span>

GearmanTask::dataSize
=====================

Get the size of returned data

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanTask::dataSize</span> ( <span
class="methodparam">void</span> )

Returns the size of the data being returned for a task.

### 参数

此函数没有参数。

### 返回值

The data size, or **`FALSE`** if there is no data.

### 参见

-   <span class="methodname">GearmanTask::data</span>

GearmanTask::function
=====================

Get associated function name (deprecated)

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanTask::function</span> ( <span
class="methodparam">void</span> )

Returns the name of the function this task is associated with, i.e., the
function the Gearman worker calls.

> **Note**:
>
> This method has been replaced by <span
> class="methodname">GearmanTask::functionName</span> in the 0.6.0
> release of the Gearman extension.

### 参数

此函数没有参数。

### 返回值

A function name.

GearmanTask::functionName
=========================

Get associated function name

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanTask::functionName</span> ( <span
class="methodparam">void</span> )

Returns the name of the function this task is associated with, i.e., the
function the Gearman worker calls.

### 参数

此函数没有参数。

### 返回值

A function name.

GearmanTask::isKnown
====================

Determine if task is known

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanTask::isKnown</span> ( <span
class="methodparam">void</span> )

Gets the status information for whether or not this task is known to the
job server.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the task is known, **`FALSE`** otherwise.

GearmanTask::isRunning
======================

Test whether the task is currently running

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanTask::isRunning</span> ( <span
class="methodparam">void</span> )

Indicates whether or not this task is currently running.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the task is running, **`FALSE`** otherwise.

GearmanTask::jobHandle
======================

gearman\_job\_handle
====================

Get the job handle

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanTask::jobHandle</span> ( <span
class="methodparam">void</span> )

Returns the job handle for this task.

### 参数

此函数没有参数。

### 返回值

The opaque job handle.

### 参见

-   <span class="methodname">GearmanClient::doJobHandle</span>

GearmanTask::recvData
=====================

Read work or result data into a buffer for a task

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">GearmanTask::recvData</span> ( <span
class="methodparam"><span class="type">int</span> `$data_len`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`data_len`  
Length of data to be read.

### 返回值

An array whose first element is the length of data read and the second
is the data buffer. Returns **`FALSE`** if the read failed.

### 参见

-   <span class="methodname">GearmanTask::sendData</span>

GearmanTask::returnCode
=======================

Get the last return code

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanTask::returnCode</span> ( <span
class="methodparam">void</span> )

Returns the last Gearman return code for this task.

### 参数

此函数没有参数。

### 返回值

A valid Gearman return code.

### 参见

-   <span class="methodname">GearmanClient::returnCode</span>

GearmanTask::sendData
=====================

Send data for a task (deprecated)

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanTask::sendData</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`data`  
Data to send to the worker.

### 返回值

The length of data sent, or **`FALSE`** if the send failed.

### 参见

-   <span class="methodname">GearmanTask::recvData</span>

GearmanTask::sendWorkload
=========================

Send data for a task

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanTask::sendWorkload</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`data`  
Data to send to the worker.

### 返回值

The length of data sent, or **`FALSE`** if the send failed.

### 参见

-   <span class="methodname">GearmanTask::recvData</span>

GearmanTask::taskDenominator
============================

Get completion percentage denominator

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanTask::taskDenominator</span> ( <span
class="methodparam">void</span> )

Returns the denominator of the percentage of the task that is complete
expressed as a fraction.

### 参数

此函数没有参数。

### 返回值

A number between 0 and 100, or **`FALSE`** if cannot be determined.

### 参见

-   <span class="methodname">GearmanTask::taskNumerator</span>

GearmanTask::taskNumerator
==========================

Get completion percentage numerator

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanTask::taskNumerator</span> ( <span
class="methodparam">void</span> )

Returns the numerator of the percentage of the task that is complete
expressed as a fraction.

### 参数

此函数没有参数。

### 返回值

A number between 0 and 100, or **`FALSE`** if cannot be determined.

### 参见

-   <span class="methodname">GearmanTask::taskDenominator</span>

GearmanTask::unique
===================

Get the unique identifier for a task

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanTask::unique</span> ( <span
class="methodparam">void</span> )

Returns the unique identifier for this task. This is assigned by the
<span class="classname">GearmanClient</span>, as opposed to the job
handle which is set by the Gearman job server.

### 参数

此函数没有参数。

### 返回值

The unique identifier, or **`FALSE`** if no identifier is assigned.

### 参见

-   <span class="methodname">GearmanClient::do</span>
-   <span class="methodname">GearmanClient::addTask</span>

GearmanTask::uuid
=================

Get the unique identifier for a task (deprecated)

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanTask::uuid</span> ( <span
class="methodparam">void</span> )

Returns the unique identifier for this task. This is assigned by the
<span class="classname">GearmanClient</span>, as opposed to the job
handle which is set by the Gearman job server.

> **Note**:
>
> This method has been replaced by <span
> class="methodname">GearmanTask::unique</span> in the 0.6.0 release of
> the Gearman extension.

### 参数

此函数没有参数。

### 返回值

The unique identifier, or **`FALSE`** if no identifier is assigned.

### 参见

-   <span class="methodname">GearmanClient::do</span>
-   <span class="methodname">GearmanClient::addTask</span>

简介
----

类摘要
------

**GearmanWorker**

<span class="ooclass"> class **GearmanWorker** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addFunction</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$function`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$context`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timeout`</span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addOptions</span> ( <span
class="methodparam"><span class="type">int</span> `$option`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addServer</span> (\[ <span
class="methodparam"><span class="type">string</span> `$host`<span
class="initializer"> = 127.0.0.1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 4730</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addServers</span> ( <span
class="methodparam"><span class="type">string</span> `$servers`<span
class="initializer"> = 127.0.0.1:4730</span></span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clone</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">echo</span> ( <span class="methodparam"><span
class="type">string</span> `$workload`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">error</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getErrno</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">options</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">register</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timeout`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">removeOptions</span> ( <span
class="methodparam"><span class="type">int</span> `$option`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">returnCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setId</span> ( <span class="methodparam"><span
class="type">string</span> `$id`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setOptions</span> ( <span
class="methodparam"><span class="type">int</span> `$option`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$timeout`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">timeout</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">unregister</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">unregisterAll</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">wait</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">work</span> ( <span
class="methodparam">void</span> )

}

GearmanWorker::addFunction
==========================

Register and add callback function

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::addFunction</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$function`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$context`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timeout`</span> \]\] )

Registers a function name with the job server and specifies a callback
corresponding to that function. Optionally specify extra application
context data to be used when the callback is called and a timeout.

### 参数

`function_name`  
The name of a function to register with the job server

`function`  
A callback that gets called when a job for the registered function name
is submitted

`context`  
A reference to arbitrary application context data that can be modified
by the worker function

`timeout`  
An interval of time in seconds

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Simple worker making use of extra application context data**

``` php
<?php

# get a gearman worker
$worker= new GearmanWorker(); 

# add the default server (localhost)
$worker->addServer(); 

# define a variable to hold application data
$count= 0; 

# add the "reverse" function
$worker->addFunction("reverse", "reverse_cb", $count);

# start the worker
while ($worker->work());

function reverse_cb($job, &$count) 
{ 
  $count++; 
  return "$count: " . strrev($job->workload()); 
} 

?>
```

Running a client that submits two jobs for the reverse function would
have output similar to the following:

    1: olleh
    2: dlrow

### 参见

-   <span class="methodname">GearmanClient::do</span>

GearmanWorker::addOptions
=========================

Add worker options

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::addOptions</span> ( <span
class="methodparam"><span class="type">int</span> `$option`</span> )

Adds one or more options to the options previously set.

### 参数

`option`  
The options to be added

### 返回值

Always returns **`TRUE`**.

### 参见

-   <span class="methodname">GearmanWorker::options</span>
-   <span class="methodname">GearmanClient::setOptions</span>
-   <span class="methodname">GearmanClient::removeOptions</span>

GearmanWorker::addServer
========================

Add a job server

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::addServer</span> (\[ <span
class="methodparam"><span class="type">string</span> `$host`<span
class="initializer"> = 127.0.0.1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 4730</span></span> \]\] )

Adds a job server to this worker. This goes into a list of servers than
can be used to run jobs. No socket I/O happens here.

### 参数

`host`  
任务服务器主机名。

`port`  
任务服务器端口号。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Add alternate Gearman servers**

``` php
<?php
$worker= new GearmanWorker(); 
$worker->addServer("10.0.0.1"); 
$worker->addServer("10.0.0.2", 7003);
?>
```

### 参见

-   <span class="methodname">GearmanWorker::addServers</span>

GearmanWorker::addServers
=========================

Add job servers

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::addServers</span> ( <span
class="methodparam"><span class="type">string</span> `$servers`<span
class="initializer"> = 127.0.0.1:4730</span></span> )

Adds one or more job servers to this worker. These go into a list of
servers that can be used to run jobs. No socket I/O happens here.

### 参数

`servers`  
A comma separated list of job servers in the format host:port. If no
port is specified, it defaults to 4730.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Add two job servers**

``` php
<?php

$worker= new GearmanWorker(); 
$worker->addServers("10.0.0.1,10.0.0.2:7003");

?>
```

### 参见

-   <span class="methodname">GearmanWorker::addServer</span>

GearmanWorker::clone
====================

Create a copy of the worker

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">GearmanWorker::clone</span> ( <span
class="methodparam">void</span> )

Creates a copy of the worker.

### 参数

此函数没有参数。

### 返回值

A <span class="classname">GearmanWorker</span> object

GearmanWorker::\_\_construct
============================

Create a GearmanWorker instance

### 说明

<span class="modifier">public</span> <span
class="methodname">GearmanWorker::\_\_construct</span> ( <span
class="methodparam">void</span> )

Creates a <span class="classname">GearmanWorker</span> instance
representing a worker that connects to the job server and accepts tasks
to run.

### 参数

此函数没有参数。

### 返回值

A <span class="classname">GearmanWorker</span> object

### 参见

-   <span class="methodname">GearmanWorker::clone</span>

GearmanWorker::echo
===================

Test job server response

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::echo</span> ( <span
class="methodparam"><span class="type">string</span> `$workload`</span>
)

Sends data to all job servers to see if they echo it back. This is a
test function to see if job servers are responding properly.

### 参数

`workload`  
Arbitrary serialized data

### 返回值

Standard Gearman return value.

### 参见

-   <span class="methodname">GearmanClient::echo</span>

GearmanWorker::error
====================

Get the last error encountered

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">GearmanWorker::error</span> ( <span
class="methodparam">void</span> )

Returns an error string for the last error encountered.

### 参数

此函数没有参数。

### 返回值

An error string.

### 参见

-   <span class="methodname">GearmanWorker::getErrno</span>

GearmanWorker::getErrno
=======================

Get errno

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanWorker::getErrno</span> ( <span
class="methodparam">void</span> )

Returns the value of errno in the case of a GEARMAN\_ERRNO return value.

### 参数

此函数没有参数。

### 返回值

A valid errno.

### 参见

-   <span class="methodname">GearmanWorker::error</span>

GearmanWorker::options
======================

Get worker options

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanWorker::options</span> ( <span
class="methodparam">void</span> )

Gets the options previously set for the worker.

### 参数

此函数没有参数。

### 返回值

The options currently set for the worker.

### 参见

-   <span class="methodname">GearmanWorker::setOptions</span>

GearmanWorker::register
=======================

Register a function with the job server

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::register</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timeout`</span> \] )

Registers a function name with the job server with an optional timeout.
The timeout specifies how many seconds the server will wait before
marking a job as failed. If the timeout is set to zero, there is no
timeout.

### 参数

`function_name`  
The name of a function to register with the job server

`timeout`  
An interval of time in seconds

### 返回值

A standard Gearman return value.

### 参见

-   <span class="methodname">GearmanWorker::unregister</span>
-   <span class="methodname">GearmanWorker::unregisterAll</span>

GearmanWorker::removeOptions
============================

Remove worker options

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::removeOptions</span> ( <span
class="methodparam"><span class="type">int</span> `$option`</span> )

Removes (unsets) one or more worker options.

### 参数

`option`  
The options to be removed (unset)

### 返回值

Always returns **`TRUE`**.

### 参见

-   <span class="methodname">GearmanWorker::options</span>
-   <span class="methodname">GearmanWorker::setOptions</span>
-   <span class="methodname">GearmanWorker::addOptions</span>

GearmanWorker::returnCode
=========================

Get last Gearman return code

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanWorker::returnCode</span> ( <span
class="methodparam">void</span> )

Returns the last Gearman return code.

### 参数

此函数没有参数。

### 返回值

A valid Gearman return code.

### 参见

-   <span class="methodname">GearmanWorker::error</span>
-   <span class="methodname">GearmanWorker::getErrno</span>

GearmanWorker::setId
====================

Give the worker an identifier so it can be tracked when asking gearmand
for the list of available workers

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::setId</span> ( <span
class="methodparam"><span class="type">string</span> `$id`</span> )

Assigns the worker an identifier.

### 参数

`id`  
A string identifier.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">GearmanWorker::setId</span> example**

Set an identifier for a simple worker.

``` php
<?php
$worker= new GearmanWorker();
$worker->setId('test');
?>
```

以上例程的输出类似于：

    Run the following command:
    gearadmin --workers

    Output:
    30 ::3a3a:3361:3361:3a33%976303667 - : test

GearmanWorker::setOptions
=========================

Set worker options

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::setOptions</span> ( <span
class="methodparam"><span class="type">int</span> `$option`</span> )

Sets one or more options to the supplied value.

### 参数

`option`  
The options to be set

### 返回值

Always returns **`TRUE`**.

### 参见

-   <span class="methodname">GearmanWorker::options</span>
-   <span class="methodname">GearmanWorker::addOptions</span>
-   <span class="methodname">GearmanWorker::removeOptions</span>
-   <span class="methodname">GearmanClient::setOptions</span>

GearmanWorker::setTimeout
=========================

Set socket I/O activity timeout

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::setTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$timeout`</span> )

Sets the interval of time to wait for socket I/O activity.

### 参数

`timeout`  
An interval of time in milliseconds. A negative value indicates an
infinite timeout.

### 返回值

Always returns **`TRUE`**.

### 范例

**示例 \#1 A simple worker with a 5 second timeout**

``` php
<?php

echo "Starting\n";

# Create our worker object.
$gmworker= new GearmanWorker();

# Add default server (localhost).
$gmworker->addServer();

# Register function "reverse" with the server.
$gmworker->addFunction("reverse", "reverse_fn");

# Set the timeout to 5 seconds
$gmworker->setTimeout(5000);

echo "Waiting for job...\n";
while(@$gmworker->work() || $gmworker->returnCode() == GEARMAN_TIMEOUT)
{
  if ($gmworker->returnCode() == GEARMAN_TIMEOUT)
  {
    # Normally one would want to do something useful here ...
    echo "Timeout. Waiting for next job...\n";
    continue;
  }

  if ($gmworker->returnCode() != GEARMAN_SUCCESS)
  {
    echo "return_code: " . $gmworker->returnCode() . "\n";
    break;
  }
}

echo "Done\n";

function reverse_fn($job)
{
  return strrev($job->workload());
}

?>
```

Running the worker with no submitted jobs will generate output that
looks like the following:

    Starting
    Waiting for job...
    Timeout. Waiting for next job...
    Timeout. Waiting for next job...
    Timeout. Waiting for next job...

### 参见

-   <span class="methodname">GearmanWorker::timeout</span>

GearmanWorker::timeout
======================

Get socket I/O activity timeout

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">GearmanWorker::timeout</span> ( <span
class="methodparam">void</span> )

Returns the current time to wait, in milliseconds, for socket I/O
activity.

### 参数

此函数没有参数。

### 返回值

A time period is milliseconds. A negative value indicates an infinite
timeout.

### 参见

-   <span class="methodname">GearmanWorker::setTimeout</span>

GearmanWorker::unregister
=========================

Unregister a function name with the job servers

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::unregister</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> )

Unregisters a function name with the job servers ensuring that no more
jobs (for that function) are sent to this worker.

### 参数

`function_name`  
The name of a function to register with the job server

### 返回值

A standard Gearman return value.

### 参见

-   <span class="methodname">GearmanWorker::register</span>
-   <span class="methodname">GearmanWorker::unregisterAll</span>

GearmanWorker::unregisterAll
============================

Unregister all function names with the job servers

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::unregisterAll</span> ( <span
class="methodparam">void</span> )

Unregisters all previously registered functions, ensuring that no more
jobs are sent to this worker.

### 参数

此函数没有参数。

### 返回值

A standard Gearman return value.

### 参见

-   <span class="methodname">GearmanWorker::register</span>
-   <span class="methodname">GearmanWorker::unregister</span>

GearmanWorker::wait
===================

Wait for activity from one of the job servers

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::wait</span> ( <span
class="methodparam">void</span> )

Causes the worker to wait for activity from one of the Gearman job
servers when operating in non-blocking I/O mode. On failure, issues a
**`E_WARNING`** with the last Gearman error encountered.

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Running worker in non-blocking mode**

``` php
<?php

echo "Starting\n";

# Create our worker object
$worker= new GearmanWorker();

# Make the worker non-blocking
$worker->addOptions(GEARMAN_WORKER_NON_BLOCKING); 

# Add the default server (localhost, port 4730)
$worker->addServer(); 

# Add our reverse function
$worker->addFunction('reverse', 'reverse_fn');

# Try to grab a job
while (@$worker->work() ||
       $worker->returnCode() == GEARMAN_IO_WAIT ||
       $worker->returnCode() == GEARMAN_NO_JOBS)
{
  if ($worker->returnCode() == GEARMAN_SUCCESS)
    continue;

  echo "Waiting for next job...\n";
  if (!@$worker->wait()) 
  { 
    if ($worker->returnCode() == GEARMAN_NO_ACTIVE_FDS) 
    { 
      # We are not connected to any servers, so wait a bit before 
      # trying to reconnect. 
      sleep(5); 
      continue; 
    } 
    break; 
  } 
} 

echo "Worker Error: " . $worker->error() . "\n";

function reverse_fn($job)
{
  return strrev($job->workload());
}


?>
```

### 参见

-   <span class="methodname">GearmanWorker::work</span>

GearmanWorker::work
===================

Wait for and perform jobs

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">GearmanWorker::work</span> ( <span
class="methodparam">void</span> )

Waits for a job to be assigned and then calls the appropriate callback
function. Issues an **`E_WARNING`** with the last Gearman error if the
return code is not one of **`GEARMAN_SUCCESS`**, **`GEARMAN_IO_WAIT`**,
or **`GEARMAN_WORK_FAIL`**.

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">GearmanWorker::work</span> example**

``` php
<?php

# create the worker
$worker = new GearmanWorker(); 

# add the default job server (localhost)
$worker->addServer(); 

# add the reverse function
$worker->addFunction("reverse", "my_reverse_function"); 

# start te worker listening for job submissions
while ($worker->work()); 
 
function my_reverse_function($job) 
{ 
  return strrev($job->workload()); 
}

?>
```

### 参见

-   <span class="methodname">GearmanWorker::addFunction</span>

简介
----

类摘要
------

**GearmanException**

<span class="ooclass"> class **GearmanException** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 方法 \*/

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
