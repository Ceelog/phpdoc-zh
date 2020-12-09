Attributes overview
-------------------

Attributes allow to add structured, machine-readable metadata
information on declarations in code: Classes, methods, functions,
parameters, properties and class constants can be the target of an
attribute. The metadata defined by attributes can then be inspected at
runtime using the
<a href="/book/reflection.html" class="link">Reflection APIs</a>.
Attributes could therefore be thought of as a configuration language
embedded directly into code.

With attributes the generic implementation of a feature and its concrete
use in an application can be decoupled. In a way it is comparable to
interfaces and their implementations. But where interfaces and
implementations are about code, attributes are about annotating extra
information and configuration. Interfaces can be implemented by classes,
yet attributes can also be declared on methods, functions, parameters,
properties and class constants. As such they are more flexible than
interfaces.

A simple example of attribute usage is to convert an interface that has
optional methods to use attributes. Lets assume an *ActionHandler*
interface representing an operation in an application, where some
implementations of an action handler require setup and others do not.
Instead of requiring all classes that implement *ActionHandler* to
implement a method *setUp()*, we use an attribute that can be used
instead. One benefit of this approach is that we can use the attribute
several times.

**示例 \#1 Implementing optional methods of an interface with
Attributes**

``` php
<?php
interface ActionHandler
{
    public function execute();
}

#[Attribute]
class SetUp {}

class CopyFile implements ActionHandler
{
    public string $fileName;
    public string $targetDirectory;

    #[SetUp]
    public function fileExists()
    {
        if (!file_exists($this->fileName)) {
            throw new RuntimeException("File does not exist");
        }
    }

    #[SetUp]
    public function targetDirectoryExists()
    {
        mkdir($this->targetDirectory);
    }

    public function execute()
    {
        copy($this->fileName, $this->targetDirectory . '/' . basename($this->fileName));
    }
}

function executeAction(ActionHandler $actionHandler)
{
    $reflection = new ReflectionObject($actionHandler);

    foreach ($reflection->getMethods() as $method) {
        $attributes = $method->getAttributes(SetUp::class);

        if (count($attributes) > 0) {
            $methodName = $method->getName();

            $actionHandler->$methodName();
        }
    }

    $actionHandler->execute();
}

$copyAction = new CopyFile();
$copyAction->fileName = "/tmp/foo.jpg";
$copyAction->targetDirectory = "/home/user";

executeAction($copyAction);
```
