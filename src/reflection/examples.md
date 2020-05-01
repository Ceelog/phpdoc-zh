范例
====

在反射文档中存在很多例子，通常位于每个类的 \_\_construct 文档中。

**示例 \#1 Shell 里的一个反射例子（一个终端）**

``` shell
$ php --rf strlen
$ php --rc finfo
$ php --re json
$ php --ri dom
```

以上例程的输出类似于：

    Function [ <internal:Core> function strlen ] {

      - Parameters [1] {
        Parameter #0 [ <required> $str ]
      }
    }

    Class [ <internal:fileinfo> class finfo ] {

      - Constants [0] {
      }

      - Static properties [0] {
      }

      - Static methods [0] {
      }

      - Properties [0] {
      }

      - Methods [4] {
        Method [ <internal:fileinfo, ctor> public method finfo ] {

          - Parameters [2] {
            Parameter #0 [ <optional> $options ]
            Parameter #1 [ <optional> $arg ]
          }
        }

        Method [ <internal:fileinfo> public method set_flags ] {

          - Parameters [1] {
            Parameter #0 [ <required> $options ]
          }
        }

        Method [ <internal:fileinfo> public method file ] {

          - Parameters [3] {
            Parameter #0 [ <required> $filename ]
            Parameter #1 [ <optional> $options ]
            Parameter #2 [ <optional> $context ]
          }
        }

        Method [ <internal:fileinfo> public method buffer ] {

          - Parameters [3] {
            Parameter #0 [ <required> $string ]
            Parameter #1 [ <optional> $options ]
            Parameter #2 [ <optional> $context ]
          }
        }
      }
    }

    Extension [ <persistent> extension #23 json version 1.2.1 ] {

      - Constants [10] {
        Constant [ integer JSON_HEX_TAG ] { 1 }
        Constant [ integer JSON_HEX_AMP ] { 2 }
        Constant [ integer JSON_HEX_APOS ] { 4 }
        Constant [ integer JSON_HEX_QUOT ] { 8 }
        Constant [ integer JSON_FORCE_OBJECT ] { 16 }
        Constant [ integer JSON_ERROR_NONE ] { 0 }
        Constant [ integer JSON_ERROR_DEPTH ] { 1 }
        Constant [ integer JSON_ERROR_STATE_MISMATCH ] { 2 }
        Constant [ integer JSON_ERROR_CTRL_CHAR ] { 3 }
        Constant [ integer JSON_ERROR_SYNTAX ] { 4 }
      }

      - Functions {
        Function [ <internal:json> function json_encode ] {

          - Parameters [2] {
            Parameter #0 [ <required> $value ]
            Parameter #1 [ <optional> $options ]
          }
        }
        Function [ <internal:json> function json_decode ] {

          - Parameters [3] {
            Parameter #0 [ <required> $json ]
            Parameter #1 [ <optional> $assoc ]
            Parameter #2 [ <optional> $depth ]
          }
        }
        Function [ <internal:json> function json_last_error ] {

          - Parameters [0] {
          }
        }
      }
    }

    dom

    DOM/XML => enabled
    DOM/XML API Version => 20031129
    libxml Version => 2.7.3
    HTML Support => enabled
    XPath Support => enabled
    XPointer Support => enabled
    Schema Support => enabled
    RelaxNG Support => enabled
