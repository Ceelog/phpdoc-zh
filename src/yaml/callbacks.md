Callbacks
=========

**目录**

-   [Parse callbacks](/yaml/callbacks.html#Parse%20callbacks)
-   [Emit callbacks](/yaml/callbacks.html#Emit%20callbacks)

Parse callbacks
---------------

Parse <span class="type">callbacks</span> are invoked by <span
class="function">yaml\_parse</span>, <span
class="function">yaml\_parse\_file</span> or <span
class="function">yaml\_parse\_url</span> functions when a registered
YAML tag is encountered. The callback is passed the tagged entity's
value, the tag, and flags indicating the scalar entity style. The
callback must return the data that the YAML parser should emit for this
entity.

**示例 \#1 Parse callback example**

``` php
<?php
/**
 * Parsing callback for yaml tag.
 * @param mixed $value Data from yaml file
 * @param string $tag Tag that triggered callback
 * @param int $flags Scalar entity style (see YAML_*_SCALAR_STYLE)
 * @return mixed Value that YAML parser should emit for the given value
 */
function tag_callback ($value, $tag, $flags) {
  var_dump(func_get_args()); // debugging
  return "Hello {$value}";
}

$yaml = <<<YAML
greeting: !example/hello World
YAML;

$result = yaml_parse($yaml, 0, $ndocs, array(
    '!example/hello' => 'tag_callback',
  ));

var_dump($result);
?>
```

以上例程的输出类似于：

    array(3) {
      [0]=>
      string(5) "World"
      [1]=>
      string(14) "!example/hello"
      [2]=>
      int(1)
    }
    array(1) {
      ["greeting"]=>
      string(11) "Hello World"
    }

Emit callbacks
--------------

Emit callbacks are invoked when an instance of a registered class is
emitted by <span class="function">yaml\_emit</span> or <span
class="function">yaml\_emit\_file</span>. The callback is passed the
object to be emitted. The callback must return an array having two keys:
"*tag*" and "*data*". The value associated with the "*tag*" key must be
a string to be used as the YAML tag in the output. The value associated
with the "*data*" key will be encoded as YAML and emitted in place of
the intercepted object.

**示例 \#1 Emit callback example**

``` php
<?php
class EmitExample {
  public $data;    // data may be in any pecl/yaml suitable type

  public function __construct ($d) {
    $this->data = $d;
  }

  /**
   * Yaml emit callback function, referred on yaml_emit call by class name.
   *
   * Expected to return an array with 2 values:
   *   - 'tag': custom tag for this serialization
   *   - 'data': value to convert to yaml (array, string, bool, number)
   *
   * @param object $obj Object to be emitted
   * @return array Tag and surrogate data to emit
   */
  public static function yamlEmit (EmitExample $obj) {
    return array(
      'tag' => '!example/emit',
      'data' => $obj->data,
    );
  }
}

$emit_callbacks = array(
  'EmitExample' => array('EmitExample', 'yamlEmit')
);

$t = new EmitExample(array('a','b','c'));
$yaml = yaml_emit(
  array(
    'example' => $t,
  ),
  YAML_ANY_ENCODING,
  YAML_ANY_BREAK,
  $emit_callbacks
);
var_dump($yaml);
?>
```

以上例程的输出类似于：

    string(43) "---
    example: !example/emit
    - a
    - b
    - c
    ...
    "
