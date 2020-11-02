预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

Return values. Always check <span
class="methodname">GearmanClient::error</span> or <span
class="methodname">GearmanWorker</span> for a string error, as it may
contain more details:

**`GEARMAN_SUCCESS`** (<span class="type">int</span>)  
<span class="simpara"> Whatever action was taken was successful. </span>

**`GEARMAN_IO_WAIT`** (<span class="type">int</span>)  
<span class="simpara"> When in non-blocking mode, an event is hit that
would have blocked. </span>

**`GEARMAN_ERRNO`** (<span class="type">int</span>)  
<span class="simpara"> A system error. Check <span
class="methodname">GearmanClient::errno</span> or <span
class="methodname">GearmanWorker::errno</span> for the system error code
that was returned. </span>

**`GEARMAN_NO_ACTIVE_FDS`** (<span class="type">int</span>)  
<span class="simpara"> <span
class="methodname">GearmanClient::wait</span> or <span
class="methodname">GearmanWorker</span> was called with no connections.
</span>

**`GEARMAN_UNEXPECTED_PACKET`** (<span class="type">int</span>)  
<span class="simpara"> Indicates something going very wrong in gearmand.
Applies only to <span class="classname">GearmanWorker</span>. </span>

**`GEARMAN_GETADDRINFO`** (<span class="type">int</span>)  
<span class="simpara"> DNS resolution failed (invalid host, port, etc).
</span>

**`GEARMAN_NO_SERVERS`** (<span class="type">int</span>)  
<span class="simpara"> Did not call <span
class="methodname">GearmanClient::addServer</span> before submitting
jobs or tasks. </span>

**`GEARMAN_LOST_CONNECTION`** (<span class="type">int</span>)  
<span class="simpara"> Lost a connection during a request. </span>

**`GEARMAN_MEMORY_ALLOCATION_FAILURE`** (<span class="type">int</span>)  
<span class="simpara"> Memory allocation failed (ran out of memory).
</span>

**`GEARMAN_SERVER_ERROR`** (<span class="type">int</span>)  
<span class="simpara"> Something went wrong in the Gearman server and it
could not handle the request gracefully. </span>

**`GEARMAN_WORK_DATA`** (<span class="type">int</span>)  
<span class="simpara"> Notice return code obtained with <span
class="methodname">GearmanClient::returnCode</span> when using <span
class="methodname">GearmanClient::do</span>. Sent to update the client
with data from a running job. A worker uses this when it needs to send
updates, send partial results, or flush data during long running jobs.
</span>

**`GEARMAN_WORK_WARNING`** (<span class="type">int</span>)  
<span class="simpara"> Notice return code obtained with <span
class="methodname">GearmanClient::returnCode</span> when using <span
class="methodname">GearmanClient::do</span>. Updates the client with a
warning. The behavior is just like **`GEARMAN_WORK_DATA`**, but should
be treated as a warning instead of normal response data. </span>

**`GEARMAN_WORK_STATUS`** (<span class="type">int</span>)  
<span class="simpara"> Notice return code obtained with <span
class="methodname">GearmanClient::returnCode</span> when using <span
class="methodname">GearmanClient::do</span>. Sent to update the status
of a long running job. Use <span
class="methodname">GearmanClient::doStatus</span> to obtain the
percentage complete of the task. </span>

**`GEARMAN_WORK_EXCEPTION`** (<span class="type">int</span>)  
<span class="simpara"> Notice return code obtained with <span
class="methodname">GearmanClient::returnCode</span> when using <span
class="methodname">GearmanClient::do</span>. Indicates that a job failed
with a given exception. </span>

**`GEARMAN_WORK_FAIL`** (<span class="type">int</span>)  
<span class="simpara"> Notice return code obtained with <span
class="methodname">GearmanClient::returnCode</span> when using <span
class="methodname">GearmanClient::do</span>. Indicates that the job
failed. </span>

**`GEARMAN_COULD_NOT_CONNECT`** (<span class="type">int</span>)  
<span class="simpara"> Failed to connect to servers. </span>

**`GEARMAN_INVALID_FUNCTION_NAME`** (<span class="type">int</span>)  
<span class="simpara"> Trying to register a function name of NULL or
using the callback interface without specifying callbacks. </span>

**`GEARMAN_INVALID_WORKER_FUNCTION`** (<span class="type">int</span>)  
<span class="simpara"> Trying to register a function with a NULL
callback function. </span>

**`GEARMAN_NO_REGISTERED_FUNCTIONS`** (<span class="type">int</span>)  
<span class="simpara"> When a worker gets a job for a function it did
not register. </span>

**`GEARMAN_NO_JOBS`** (<span class="type">int</span>)  
<span class="simpara"> For a non-blocking worker, when <span
class="methodname">GearmanWorker::work</span> does not have any active
jobs. </span>

**`GEARMAN_ECHO_DATA_CORRUPTION`** (<span class="type">int</span>)  
<span class="simpara"> After <span
class="methodname">GearmanClient::echo</span> or <span
class="methodname">GearmanWorker::echo</span> the data returned doesn't
match the data sent. </span>

**`GEARMAN_NEED_WORKLOAD_FN`** (<span class="type">int</span>)  
<span class="simpara"> When the client opted to stream the workload of a
task, but did not specify a workload callback function. </span>

**`GEARMAN_PAUSE`** (<span class="type">int</span>)  
<span class="simpara"> For the non-blocking client task interface, can
be returned from the task callback to "pause" the call and return from
<span class="methodname">GearmanClient::runTasks</span>. Call <span
class="methodname">GearmanClient::runTasks</span> again to continue.
</span>

**`GEARMAN_UNKNOWN_STATE`** (<span class="type">int</span>)  
<span class="simpara"> Internal client/worker state error. </span>

**`GEARMAN_SEND_BUFFER_TOO_SMALL`** (<span class="type">int</span>)  
<span class="simpara"> Internal error: trying to flush more data in one
atomic chunk than is possible due to hard-coded buffer sizes. </span>

**`GEARMAN_TIMEOUT`** (<span class="type">int</span>)  
<span class="simpara"> Hit the timeout limit set by the client/worker.
</span>

<span class="classname">GearmanClient</span> options:

**`GEARMAN_CLIENT_GENERATE_UNIQUE`** (<span class="type">int</span>)  
<span class="simpara"> Generate a unique id (UUID) for each task.
</span>

**`GEARMAN_CLIENT_NON_BLOCKING`** (<span class="type">int</span>)  
<span class="simpara"> Run the cient in a non-blocking mode. </span>

**`GEARMAN_CLIENT_UNBUFFERED_RESULT`** (<span class="type">int</span>)  
<span class="simpara"> Allow the client to read data in chunks rather
than have the library buffer the entire data result and pass that back.
</span>

**`GEARMAN_CLIENT_FREE_TASKS`** (<span class="type">int</span>)  
<span class="simpara"> Automatically free task objects once they are
complete. This is the default setting in this extension to prevent
memory leaks. </span>

<span class="classname">GearmanWorker</span> options:

**`GEARMAN_WORKER_NON_BLOCKING`** (<span class="type">int</span>)  
<span class="simpara"> Run the worker in non-blocking mode. </span>

**`GEARMAN_WORKER_GRAB_UNIQ`** (<span class="type">int</span>)  
<span class="simpara"> Return the client assigned unique ID in addition
to the job handle. </span>

Base Gearman configuration:

**`GEARMAN_DEFAULT_TCP_HOST`** (<span class="type">string</span>)  
<span class="simpara"> </span>

**`GEARMAN_DEFAULT_TCP_PORT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`GEARMAN_DEFAULT_SOCKET_TIMEOUT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`GEARMAN_DEFAULT_SOCKET_SEND_SIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`GEARMAN_DEFAULT_SOCKET_RECV_SIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`GEARMAN_MAX_ERROR_SIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`GEARMAN_PACKET_HEADER_SIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`GEARMAN_JOB_HANDLE_SIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`GEARMAN_OPTION_SIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`GEARMAN_UNIQUE_SIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`GEARMAN_MAX_COMMAND_ARGS`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`GEARMAN_ARGS_BUFFER_SIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`GEARMAN_SEND_BUFFER_SIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`GEARMAN_RECV_BUFFER_SIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`GEARMAN_WORKER_WAIT_TIMEOUT`** (<span class="type">int</span>)  
<span class="simpara"> </span>
