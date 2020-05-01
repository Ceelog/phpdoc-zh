Implemented as a SAPI module, phpdbg can exert complete control over the
environment without impacting the functionality or performance of your
code.

phpdbg aims to be a lightweight, powerful, easy to use debugging
platform for PHP. It offers the following features:

-   <span class="simpara">Step-Through Debugging</span>
-   <span class="simpara">Flexible Breakpoints (Class Method, Function,
    File:Line, Address, Opcode)</span>
-   <span class="simpara">Easy Access to PHP with built-in eval()</span>
-   <span class="simpara">Userland API</span>
-   <span class="simpara">SAPI Agnostic - Easily Integrated</span>
-   <span class="simpara">PHP Configuration File Support</span>
-   <span class="simpara">JIT Super Globals - Set Your Own !!</span>
-   <span class="simpara">Optional readline Support - Comfortable
    Terminal Operation</span>
-   <span class="simpara">Easy Operation - See Help :)</span>

| Option | Example Argument   | Description                                                                       |
|--------|--------------------|-----------------------------------------------------------------------------------|
| -c     | -c/my/php.ini      | Set php.ini file to load                                                          |
| -d     | -dmemory\_limit=4G | Set a php.ini directive                                                           |
| -n     |                    | Disable default php.ini                                                           |
| -q     |                    | Suppress welcome banner                                                           |
| -v     |                    | Enable oplog output                                                               |
| -b     |                    | Disable color                                                                     |
| -i     | -imy.init          | Set .phpdbginit file                                                              |
| -I     |                    | Ignore default .phpdbginit                                                        |
| -O     | -Omy.oplog         | Set oplog output file                                                             |
| -r     |                    | Run execution context                                                             |
| -rr    |                    | Run execution context and quit after execution (not respecting breakpoints)       |
| -e     |                    | Generate extended information for debugger/profiler                               |
| -E     |                    | Enable step through eval, careful!                                                |
| -s     | -s=, -s=foo        | Read code to execute from stdin with an optional delimiter                        |
| -S     | -Scli              | Override SAPI name, careful!                                                      |
|        |                    |                                                                                   |
| -l     | -l4000             | Setup remote console ports                                                        |
| -a     | -a192.168.0.3      | Setup remote console bind address                                                 |
| -x     |                    | Enable xml output (instead of normal text output)                                 |
| -p     | -p, -p=func, -p\*  | Output opcodes and quit                                                           |
| -h     |                    | Print the help overview                                                           |
| -V     |                    | Print version number                                                              |
| --     | -- arg1 arg2       | Use to delimit phpdbg arguments and php $argv; append any $argv argument after it |
