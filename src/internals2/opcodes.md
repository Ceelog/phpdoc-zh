Zend Engine 2 操作码列表
========================

**目录**

-   [Opcode Descriptions and Examples](/internals2/opcodes/list.html)
    -   [ADD](/internals2/opcodes/add.html)
    -   [ADD\_ARRAY\_ELEMENT](/internals2/opcodes/add-array-element.html)
    -   [ADD\_CHAR](/internals2/opcodes/add-char.html)
    -   [ADD\_INTERFACE](/internals2/opcodes/add-interface.html)
    -   [ADD\_STRING](/internals2/opcodes/add-string.html)
    -   [ADD\_VAR](/internals2/opcodes/add-var.html)
    -   [ASSIGN](/internals2/opcodes/assign.html)
    -   [ASSIGN\_ADD](/internals2/opcodes/assign-add.html)
    -   [ASSIGN\_BW\_AND](/internals2/opcodes/assign-bw-and.html)
    -   [ASSIGN\_BW\_OR](/internals2/opcodes/assign-bw-or.html)
    -   [ASSIGN\_BW\_XOR](/internals2/opcodes/assign-bw-xor.html)
    -   [ASSIGN\_CONCAT](/internals2/opcodes/assign-concat.html)
    -   [ASSIGN\_DIM](/internals2/opcodes/assign-dim.html)
    -   [ASSIGN\_DIV](/internals2/opcodes/assign-div.html)
    -   [ASSIGN\_MOD](/internals2/opcodes/assign-mod.html)
    -   [ASSIGN\_MUL](/internals2/opcodes/assign-mul.html)
    -   [ASSIGN\_OBJ](/internals2/opcodes/assign-obj.html)
    -   [ASSIGN\_REF](/internals2/opcodes/assign-ref.html)
    -   [ASSIGN\_SL](/internals2/opcodes/assign-sl.html)
    -   [ASSIGN\_SR](/internals2/opcodes/assign-sr.html)
    -   [ASSIGN\_SUB](/internals2/opcodes/assign-sub.html)
    -   [BEGIN\_SILENCE](/internals2/opcodes/begin-silence.html)
    -   [BOOL](/internals2/opcodes/bool.html)
    -   [BOOL\_NOT](/internals2/opcodes/bool-not.html)
    -   [BOOL\_XOR](/internals2/opcodes/bool-xor.html)
    -   [BRK](/internals2/opcodes/brk.html)
    -   [BW\_AND](/internals2/opcodes/bw-and.html)
    -   [BW\_NOT](/internals2/opcodes/bw-not.html)
    -   [BW\_OR](/internals2/opcodes/bw-or.html)
    -   [BW\_XOR](/internals2/opcodes/bw-xor.html)
    -   [CASE](/internals2/opcodes/case.html)
    -   [CAST](/internals2/opcodes/cast.html)
    -   [CATCH](/internals2/opcodes/catch.html)
    -   [CLONE](/internals2/opcodes/clone.html)
    -   [CONCAT](/internals2/opcodes/concat.html)
    -   [CONT](/internals2/opcodes/cont.html)
    -   [DECLARE\_CLASS](/internals2/opcodes/declare-class.html)
    -   [DECLARE\_CONST](/internals2/opcodes/declare-const.html)
    -   [DECLARE\_FUNCTION](/internals2/opcodes/declare-function.html)
    -   [DECLARE\_INHERITED\_CLASS](/internals2/opcodes/declare-inherited-class.html)
    -   [DECLARE\_INHERITED\_CLASS\_DELAYED](/internals2/opcodes/declare-inherited-class-delayed.html)
    -   [DIV](/internals2/opcodes/div.html)
    -   [DO\_FCALL](/internals2/opcodes/do-fcall.html)
    -   [DO\_FCALL\_BY\_NAME](/internals2/opcodes/do-fcall-by-name.html)
    -   [ECHO](/internals2/opcodes/echo.html)
    -   [END\_SILENCE](/internals2/opcodes/end-silence.html)
    -   [EXIT](/internals2/opcodes/exit.html)
    -   [EXT\_FCALL\_BEGIN](/internals2/opcodes/ext-fcall-begin.html)
    -   [EXT\_FCALL\_END](/internals2/opcodes/ext-fcall-end.html)
    -   [EXT\_NOP](/internals2/opcodes/ext-nop.html)
    -   [EXT\_STMT](/internals2/opcodes/ext-stmt.html)
    -   [FE\_FETCH](/internals2/opcodes/fe-fetch.html)
    -   [FE\_RESET](/internals2/opcodes/fe-reset.html)
    -   [FETCH\_CLASS](/internals2/opcodes/fetch-class.html)
    -   [FETCH\_CONSTANT](/internals2/opcodes/fetch-constant.html)
    -   [FETCH\_DIM\_FUNC\_ARG](/internals2/opcodes/fetch-dim-func-arg.html)
    -   [FETCH\_DIM\_IS](/internals2/opcodes/fetch-dim-is.html)
    -   [FETCH\_DIM\_R](/internals2/opcodes/fetch-dim-r.html)
    -   [FETCH\_DIM\_RW](/internals2/opcodes/fetch-dim-rw.html)
    -   [FETCH\_DIM\_TMP\_VAR](/internals2/opcodes/fetch-dim-tmp-var.html)
    -   [FETCH\_DIM\_UNSET](/internals2/opcodes/fetch-dim-unset.html)
    -   [FETCH\_DIM\_W](/internals2/opcodes/fetch-dim-w.html)
    -   [FETCH\_FUNC\_ARG](/internals2/opcodes/fetch-func-arg.html)
    -   [FETCH\_IS](/internals2/opcodes/fetch-is.html)
    -   [FETCH\_OBJ\_FUNC\_ARG](/internals2/opcodes/fetch-obj-func-arg.html)
    -   [FETCH\_OBJ\_IS](/internals2/opcodes/fetch-obj-is.html)
    -   [FETCH\_OBJ\_R](/internals2/opcodes/fetch-obj-r.html)
    -   [FETCH\_OBJ\_RW](/internals2/opcodes/fetch-obj-rw.html)
    -   [FETCH\_OBJ\_UNSET](/internals2/opcodes/fetch-obj-unset.html)
    -   [FETCH\_OBJ\_W](/internals2/opcodes/fetch-obj-w.html)
    -   [FETCH\_R](/internals2/opcodes/fetch-r.html)
    -   [FETCH\_RW](/internals2/opcodes/fetch-rw.html)
    -   [FETCH\_UNSET](/internals2/opcodes/fetch-unset.html)
    -   [FETCH\_W](/internals2/opcodes/fetch-w.html)
    -   [FREE](/internals2/opcodes/free.html)
    -   [GOTO](/internals2/opcodes/goto.html)
    -   [HANDLE\_EXCEPTION](/internals2/opcodes/handle-exception.html)
    -   [INCLUDE\_OR\_EVAL](/internals2/opcodes/include-or-eval.html)
    -   [INIT\_ARRAY](/internals2/opcodes/init-array.html)
    -   [INIT\_FCALL\_BY\_NAME](/internals2/opcodes/init-fcall-by-name.html)
    -   [INIT\_METHOD\_CALL](/internals2/opcodes/init-method-call.html)
    -   [INIT\_NS\_FCALL\_BY\_NAME](/internals2/opcodes/init-ns-fcall-by-name.html)
    -   [INIT\_STATIC\_METHOD\_CALL](/internals2/opcodes/init-static-method-call.html)
    -   [INIT\_STRING](/internals2/opcodes/init-string.html)
    -   [INSTANCEOF](/internals2/opcodes/instanceof.html)
    -   [IS\_EQUAL](/internals2/opcodes/is-equal.html)
    -   [IS\_IDENTICAL](/internals2/opcodes/is-identical.html)
    -   [IS\_NOT\_EQUAL](/internals2/opcodes/is-not-equal.html)
    -   [IS\_NOT\_IDENTICAL](/internals2/opcodes/is-not-identical.html)
    -   [IS\_SMALLER](/internals2/opcodes/is-smaller.html)
    -   [IS\_SMALLER\_OR\_EQUAL](/internals2/opcodes/is-smaller-or-equal.html)
    -   [ISSET\_ISEMPTY\_DIM\_OBJ](/internals2/opcodes/isset-isempty-dim-obj.html)
    -   [ISSET\_ISEMPTY\_PROP\_OBJ](/internals2/opcodes/isset-isempty-prop-obj.html)
    -   [ISSET\_ISEMPTY\_VAR](/internals2/opcodes/isset-isempty-var.html)
    -   [JMP](/internals2/opcodes/jmp.html)
    -   [JMPNZ](/internals2/opcodes/jmpnz.html)
    -   [JMPNZ\_EX](/internals2/opcodes/jmpnz-ex.html)
    -   [JMPZ](/internals2/opcodes/jmpz.html)
    -   [JMPZ\_EX](/internals2/opcodes/jmpz-ex.html)
    -   [JMPZNZ](/internals2/opcodes/jmpznz.html)
    -   [MOD](/internals2/opcodes/mod.html)
    -   [MUL](/internals2/opcodes/mul.html)
    -   [NEW](/internals2/opcodes/new.html)
    -   [NOP](/internals2/opcodes/nop.html)
    -   [POST\_DEC](/internals2/opcodes/post-dec.html)
    -   [POST\_DEC\_OBJ](/internals2/opcodes/post-dec-obj.html)
    -   [POST\_INC](/internals2/opcodes/post-inc.html)
    -   [POST\_INC\_OBJ](/internals2/opcodes/post-inc-obj.html)
    -   [PRE\_DEC](/internals2/opcodes/pre-dec.html)
    -   [PRE\_DEC\_OBJ](/internals2/opcodes/pre-dec-obj.html)
    -   [PRE\_INC](/internals2/opcodes/pre-inc.html)
    -   [PRE\_INC\_OBJ](/internals2/opcodes/pre-inc-obj.html)
    -   [PRINT](/internals2/opcodes/print.html)
    -   [QM\_ASSIGN](/internals2/opcodes/qm-assign.html)
    -   [RAISE\_ABSTRACT\_ERROR](/internals2/opcodes/raise-abstract-error.html)
    -   [RECV](/internals2/opcodes/recv.html)
    -   [RECV\_INIT](/internals2/opcodes/recv-init.html)
    -   [RETURN](/internals2/opcodes/return.html)
    -   [RETURN\_BY\_REF](/internals2/opcodes/return-by-ref.html)
    -   [SEND\_REF](/internals2/opcodes/send-ref.html)
    -   [SEND\_VAL](/internals2/opcodes/send-val.html)
    -   [SEND\_VAR](/internals2/opcodes/send-var.html)
    -   [SEND\_VAR\_NO\_REF](/internals2/opcodes/send-var-no-ref.html)
    -   [SL](/internals2/opcodes/sl.html)
    -   [SR](/internals2/opcodes/sr.html)
    -   [SUB](/internals2/opcodes/sub.html)
    -   [SWITCH\_FREE](/internals2/opcodes/switch-free.html)
    -   [THROW](/internals2/opcodes/throw.html)
    -   [TICKS](/internals2/opcodes/ticks.html)
    -   [UNSET\_DIM](/internals2/opcodes/unset-dim.html)
    -   [UNSET\_OBJ](/internals2/opcodes/unset-obj.html)
    -   [UNSET\_VAR](/internals2/opcodes/unset-var.html)
    -   [USER\_OPCODE](/internals2/opcodes/user-opcode.html)
    -   [VERIFY\_ABSTRACT\_CLASS](/internals2/opcodes/verify-abstract-class.html)
    -   [ZEND\_DECLARE\_LAMBDA\_FUNCTION](/internals2/opcodes/zend-declare-lambda-function.html)
    -   [ZEND\_JMP\_SET](/internals2/opcodes/zend-jmp-set.html)

此页列出并收录了由 Zend Engine 2 解析 PHP 文件而生成的全部Opcode。使用
vld 扩展(参见
<a href="https://pecl.php.net/package/vld" class="link external">» https://pecl.php.net/package/vld</a>)的
PHP 文件的Opcode可能会被丢弃。

| 编号 | 名称                                                                                                | 是否有例子代码 |
|------|-----------------------------------------------------------------------------------------------------|----------------|
| 0    | <a href="/internals2/opcodes/nop.html" class="xref">NOP</a>                                         | 是             |
| 1    | <a href="/internals2/opcodes/add.html" class="xref">ADD</a>                                         | 是             |
| 2    | <a href="/internals2/opcodes/sub.html" class="xref">SUB</a>                                         | 是             |
| 3    | <a href="/internals2/opcodes/mul.html" class="xref">MUL</a>                                         | 是             |
| 4    | <a href="/internals2/opcodes/div.html" class="xref">DIV</a>                                         | 是             |
| 5    | <a href="/internals2/opcodes/mod.html" class="xref">MOD</a>                                         | 是             |
| 6    | <a href="/internals2/opcodes/sl.html" class="xref">SL</a>                                           | 是             |
| 7    | <a href="/internals2/opcodes/sr.html" class="xref">SR</a>                                           | 是             |
| 8    | <a href="/internals2/opcodes/concat.html" class="xref">CONCAT</a>                                   | 是             |
| 9    | <a href="/internals2/opcodes/bw-or.html" class="xref">BW_OR</a>                                     | 是             |
| 10   | <a href="/internals2/opcodes/bw-and.html" class="xref">BW_AND</a>                                   | 是             |
| 11   | <a href="/internals2/opcodes/bw-xor.html" class="xref">BW_XOR</a>                                   | 是             |
| 12   | <a href="/internals2/opcodes/bw-not.html" class="xref">BW_NOT</a>                                   | 是             |
| 13   | <a href="/internals2/opcodes/bool-not.html" class="xref">BOOL_NOT</a>                               | 是             |
| 14   | <a href="/internals2/opcodes/bool-xor.html" class="xref">BOOL_XOR</a>                               | 是             |
| 15   | <a href="/internals2/opcodes/is-identical.html" class="xref">IS_IDENTICAL</a>                       | 是             |
| 16   | <a href="/internals2/opcodes/is-not-identical.html" class="xref">IS_NOT_IDENTICAL</a>               | 是             |
| 17   | <a href="/internals2/opcodes/is-equal.html" class="xref">IS_EQUAL</a>                               | 是             |
| 18   | <a href="/internals2/opcodes/is-not-equal.html" class="xref">IS_NOT_EQUAL</a>                       | 是             |
| 19   | <a href="/internals2/opcodes/is-smaller.html" class="xref">IS_SMALLER</a>                           | 是             |
| 20   | <a href="/internals2/opcodes/is-smaller-or-equal.html" class="xref">IS_SMALLER_OR_EQUAL</a>         | 是             |
| 21   | <a href="/internals2/opcodes/cast.html" class="xref">CAST</a>                                       | 是             |
| 22   | <a href="/internals2/opcodes/qm-assign.html" class="xref">QM_ASSIGN</a>                             | 是             |
| 23   | <a href="/internals2/opcodes/assign-add.html" class="xref">ASSIGN_ADD</a>                           | 是             |
| 24   | <a href="/internals2/opcodes/assign-sub.html" class="xref">ASSIGN_SUB</a>                           | 是             |
| 25   | <a href="/internals2/opcodes/assign-mul.html" class="xref">ASSIGN_MUL</a>                           | 是             |
| 26   | <a href="/internals2/opcodes/assign-div.html" class="xref">ASSIGN_DIV</a>                           | 是             |
| 27   | <a href="/internals2/opcodes/assign-mod.html" class="xref">ASSIGN_MOD</a>                           | 是             |
| 28   | <a href="/internals2/opcodes/assign-sl.html" class="xref">ASSIGN_SL</a>                             | 是             |
| 29   | <a href="/internals2/opcodes/assign-sr.html" class="xref">ASSIGN_SR</a>                             | 是             |
| 30   | <a href="/internals2/opcodes/assign-concat.html" class="xref">ASSIGN_CONCAT</a>                     | 是             |
| 31   | <a href="/internals2/opcodes/assign-bw-or.html" class="xref">ASSIGN_BW_OR</a>                       | 是             |
| 32   | <a href="/internals2/opcodes/assign-bw-and.html" class="xref">ASSIGN_BW_AND</a>                     | 是             |
| 33   | <a href="/internals2/opcodes/assign-bw-xor.html" class="xref">ASSIGN_BW_XOR</a>                     | 是             |
| 34   | <a href="/internals2/opcodes/pre-inc.html" class="xref">PRE_INC</a>                                 | 是             |
| 35   | <a href="/internals2/opcodes/pre-dec.html" class="xref">PRE_DEC</a>                                 | 是             |
| 36   | <a href="/internals2/opcodes/post-inc.html" class="xref">POST_INC</a>                               | 是             |
| 37   | <a href="/internals2/opcodes/post-dec.html" class="xref">POST_DEC</a>                               | 是             |
| 38   | <a href="/internals2/opcodes/assign.html" class="xref">ASSIGN</a>                                   | 是             |
| 39   | <a href="/internals2/opcodes/assign-ref.html" class="xref">ASSIGN_REF</a>                           | 是             |
| 40   | <a href="/internals2/opcodes/echo.html" class="xref">ECHO</a>                                       | 是             |
| 41   | <a href="/internals2/opcodes/print.html" class="xref">PRINT</a>                                     | 是             |
| 42   | 未收录                                                                                              | 否             |
| 43   | <a href="/internals2/opcodes/jmpz.html" class="xref">JMPZ</a>                                       | 是             |
| 44   | <a href="/internals2/opcodes/jmpnz.html" class="xref">JMPNZ</a>                                     | 是             |
| 45   | <a href="/internals2/opcodes/jmpznz.html" class="xref">JMPZNZ</a>                                   | 是             |
| 46   | <a href="/internals2/opcodes/jmpz-ex.html" class="xref">JMPZ_EX</a>                                 | 是             |
| 47   | <a href="/internals2/opcodes/jmpnz-ex.html" class="xref">JMPNZ_EX</a>                               | 是             |
| 48   | <a href="/internals2/opcodes/case.html" class="xref">CASE</a>                                       | 是             |
| 49   | <a href="/internals2/opcodes/switch-free.html" class="xref">SWITCH_FREE</a>                         | 是             |
| 50   | <a href="/internals2/opcodes/brk.html" class="xref">BRK</a>                                         | 是             |
| 51   | 未收录                                                                                              | 否             |
| 52   | <a href="/internals2/opcodes/bool.html" class="xref">BOOL</a>                                       | 是             |
| 53   | <a href="/internals2/opcodes/init-string.html" class="xref">INIT_STRING</a>                         | 是             |
| 54   | <a href="/internals2/opcodes/add-char.html" class="xref">ADD_CHAR</a>                               | 是             |
| 55   | <a href="/internals2/opcodes/add-string.html" class="xref">ADD_STRING</a>                           | 是             |
| 56   | <a href="/internals2/opcodes/add-var.html" class="xref">ADD_VAR</a>                                 | 是             |
| 57   | <a href="/internals2/opcodes/begin-silence.html" class="xref">BEGIN_SILENCE</a>                     | 是             |
| 58   | <a href="/internals2/opcodes/end-silence.html" class="xref">END_SILENCE</a>                         | 是             |
| 59   | <a href="/internals2/opcodes/init-fcall-by-name.html" class="xref">INIT_FCALL_BY_NAME</a>           | 是             |
| 60   | <a href="/internals2/opcodes/do-fcall.html" class="xref">DO_FCALL</a>                               | 是             |
| 61   | <a href="/internals2/opcodes/do-fcall-by-name.html" class="xref">DO_FCALL_BY_NAME</a>               | 是             |
| 62   | <a href="/internals2/opcodes/return.html" class="xref">RETURN</a>                                   | 是             |
| 63   | <a href="/internals2/opcodes/recv.html" class="xref">RECV</a>                                       | 是             |
| 64   | <a href="/internals2/opcodes/recv-init.html" class="xref">RECV_INIT</a>                             | 是             |
| 65   | <a href="/internals2/opcodes/send-val.html" class="xref">SEND_VAL</a>                               | 是             |
| 66   | <a href="/internals2/opcodes/send-var.html" class="xref">SEND_VAR</a>                               | 是             |
| 67   | <a href="/internals2/opcodes/send-ref.html" class="xref">SEND_REF</a>                               | 是             |
| 68   | <a href="/internals2/opcodes/new.html" class="xref">NEW</a>                                         | 是             |
| 69   | 未收录                                                                                              | 否             |
| 70   | <a href="/internals2/opcodes/free.html" class="xref">FREE</a>                                       | 是             |
| 71   | <a href="/internals2/opcodes/init-array.html" class="xref">INIT_ARRAY</a>                           | 是             |
| 72   | <a href="/internals2/opcodes/add-array-element.html" class="xref">ADD_ARRAY_ELEMENT</a>             | 是             |
| 73   | <a href="/internals2/opcodes/include-or-eval.html" class="xref">INCLUDE_OR_EVAL</a>                 | 是             |
| 74   | <a href="/internals2/opcodes/unset-var.html" class="xref">UNSET_VAR</a>                             | 是             |
| 75   | <a href="/internals2/opcodes/unset-dim.html" class="xref">UNSET_DIM</a>                             | 是             |
| 76   | <a href="/internals2/opcodes/unset-obj.html" class="xref">UNSET_OBJ</a>                             | 是             |
| 77   | <a href="/internals2/opcodes/fe-reset.html" class="xref">FE_RESET</a>                               | 是             |
| 78   | <a href="/internals2/opcodes/fe-fetch.html" class="xref">FE_FETCH</a>                               | 是             |
| 79   | <a href="/internals2/opcodes/exit.html" class="xref">EXIT</a>                                       | 是             |
| 80   | <a href="/internals2/opcodes/fetch-r.html" class="xref">FETCH_R</a>                                 | 是             |
| 81   | <a href="/internals2/opcodes/fetch-dim-r.html" class="xref">FETCH_DIM_R</a>                         | 是             |
| 82   | <a href="/internals2/opcodes/fetch-obj-r.html" class="xref">FETCH_OBJ_R</a>                         | 是             |
| 83   | <a href="/internals2/opcodes/fetch-w.html" class="xref">FETCH_W</a>                                 | 是             |
| 84   | <a href="/internals2/opcodes/fetch-dim-w.html" class="xref">FETCH_DIM_W</a>                         | 是             |
| 85   | <a href="/internals2/opcodes/fetch-obj-w.html" class="xref">FETCH_OBJ_W</a>                         | 是             |
| 86   | <a href="/internals2/opcodes/fetch-rw.html" class="xref">FETCH_RW</a>                               | 是             |
| 87   | <a href="/internals2/opcodes/fetch-dim-rw.html" class="xref">FETCH_DIM_RW</a>                       | 是             |
| 88   | <a href="/internals2/opcodes/fetch-obj-rw.html" class="xref">FETCH_OBJ_RW</a>                       | 是             |
| 89   | <a href="/internals2/opcodes/fetch-is.html" class="xref">FETCH_IS</a>                               | 是             |
| 90   | <a href="/internals2/opcodes/fetch-dim-is.html" class="xref">FETCH_DIM_IS</a>                       | 否             |
| 91   | <a href="/internals2/opcodes/fetch-obj-is.html" class="xref">FETCH_OBJ_IS</a>                       | 否             |
| 92   | <a href="/internals2/opcodes/fetch-func-arg.html" class="xref">FETCH_FUNC_ARG</a>                   | 是             |
| 93   | <a href="/internals2/opcodes/fetch-dim-func-arg.html" class="xref">FETCH_DIM_FUNC_ARG</a>           | 是             |
| 94   | <a href="/internals2/opcodes/fetch-obj-func-arg.html" class="xref">FETCH_OBJ_FUNC_ARG</a>           | 是             |
| 95   | <a href="/internals2/opcodes/fetch-unset.html" class="xref">FETCH_UNSET</a>                         | 否             |
| 96   | <a href="/internals2/opcodes/fetch-dim-unset.html" class="xref">FETCH_DIM_UNSET</a>                 | 否             |
| 97   | <a href="/internals2/opcodes/fetch-obj-unset.html" class="xref">FETCH_OBJ_UNSET</a>                 | 否             |
| 98   | <a href="/internals2/opcodes/fetch-dim-tmp-var.html" class="xref">FETCH_DIM_TMP_VAR</a>             | 是             |
| 99   | <a href="/internals2/opcodes/fetch-constant.html" class="xref">FETCH_CONSTANT</a>                   | 是             |
| 100  | 未收录                                                                                              | 否             |
| 101  | <a href="/internals2/opcodes/ext-stmt.html" class="xref">EXT_STMT</a>                               | 否             |
| 102  | <a href="/internals2/opcodes/ext-fcall-begin.html" class="xref">EXT_FCALL_BEGIN</a>                 | 否             |
| 103  | <a href="/internals2/opcodes/ext-fcall-end.html" class="xref">EXT_FCALL_END</a>                     | 否             |
| 104  | <a href="/internals2/opcodes/ext-nop.html" class="xref">EXT_NOP</a>                                 | 否             |
| 105  | <a href="/internals2/opcodes/ticks.html" class="xref">TICKS</a>                                     | 是             |
| 106  | <a href="/internals2/opcodes/send-var-no-ref.html" class="xref">SEND_VAR_NO_REF</a>                 | 否             |
| 107  | <a href="/internals2/opcodes/catch.html" class="xref">CATCH</a>                                     | 是             |
| 108  | <a href="/internals2/opcodes/throw.html" class="xref">THROW</a>                                     | 是             |
| 109  | <a href="/internals2/opcodes/fetch-class.html" class="xref">FETCH_CLASS</a>                         | 是             |
| 110  | <a href="/internals2/opcodes/clone.html" class="xref">CLONE</a>                                     | 是             |
| 111  | 未收录                                                                                              | 否             |
| 112  | <a href="/internals2/opcodes/init-method-call.html" class="xref">INIT_METHOD_CALL</a>               | 是             |
| 113  | <a href="/internals2/opcodes/init-static-method-call.html" class="xref">INIT_STATIC_METHOD_CALL</a> | 是             |
| 114  | <a href="/internals2/opcodes/isset-isempty-var.html" class="xref">ISSET_ISEMPTY_VAR</a>             | 是             |
| 115  | <a href="/internals2/opcodes/isset-isempty-dim-obj.html" class="xref">ISSET_ISEMPTY_DIM_OBJ</a>     | 是             |
| 116  | 未收录                                                                                              | 否             |
| 117  | 未收录                                                                                              | 否             |
| 118  | 未收录                                                                                              | 否             |
| 119  | 未收录                                                                                              | 否             |
| 120  | 未收录                                                                                              | 否             |
| 121  | 未收录                                                                                              | 否             |
| 122  | 未收录                                                                                              | 否             |
| 123  | 未收录                                                                                              | 否             |
| 124  | 未收录                                                                                              | 否             |
| 125  | 未收录                                                                                              | 否             |
| 126  | 未收录                                                                                              | 否             |
| 127  | 未收录                                                                                              | 否             |
| 128  | 未收录                                                                                              | 否             |
| 129  | 未收录                                                                                              | 否             |
| 130  | 未收录                                                                                              | 否             |
| 131  | 未收录                                                                                              | 否             |
| 132  | <a href="/internals2/opcodes/pre-inc-obj.html" class="xref">PRE_INC_OBJ</a>                         | 是             |
| 133  | <a href="/internals2/opcodes/pre-dec-obj.html" class="xref">PRE_DEC_OBJ</a>                         | 是             |
| 134  | <a href="/internals2/opcodes/post-inc-obj.html" class="xref">POST_INC_OBJ</a>                       | 是             |
| 135  | <a href="/internals2/opcodes/post-dec-obj.html" class="xref">POST_DEC_OBJ</a>                       | 是             |
| 136  | <a href="/internals2/opcodes/assign-obj.html" class="xref">ASSIGN_OBJ</a>                           | 是             |
| 137  | 未收录                                                                                              | 否             |
| 138  | <a href="/internals2/opcodes/instanceof.html" class="xref">INSTANCEOF</a>                           | 是             |
| 139  | <a href="/internals2/opcodes/declare-class.html" class="xref">DECLARE_CLASS</a>                     | 是             |
| 140  | <a href="/internals2/opcodes/declare-inherited-class.html" class="xref">DECLARE_INHERITED_CLASS</a> | 是             |
| 141  | <a href="/internals2/opcodes/declare-function.html" class="xref">DECLARE_FUNCTION</a>               | 是             |
| 142  | <a href="/internals2/opcodes/raise-abstract-error.html" class="xref">RAISE_ABSTRACT_ERROR</a>       | 是             |
| 143  | 未收录                                                                                              | 否             |
| 144  | <a href="/internals2/opcodes/add-interface.html" class="xref">ADD_INTERFACE</a>                     | 否             |
| 145  | 未收录                                                                                              | 否             |
| 146  | <a href="/internals2/opcodes/verify-abstract-class.html" class="xref">VERIFY_ABSTRACT_CLASS</a>     | 否             |
| 147  | <a href="/internals2/opcodes/assign-dim.html" class="xref">ASSIGN_DIM</a>                           | 是             |
| 148  | <a href="/internals2/opcodes/isset-isempty-prop-obj.html" class="xref">ISSET_ISEMPTY_PROP_OBJ</a>   | 是             |
| 149  | <a href="/internals2/opcodes/handle-exception.html" class="xref">HANDLE_EXCEPTION</a>               | 是             |
| 150  | <a href="/internals2/opcodes/user-opcode.html" class="xref">USER_OPCODE</a>                         | 否             |
| 152  | ZEND\_JMP\_SET                                                                                      | 否             |
| 153  | ZEND\_DECLARE\_LAMBDA\_FUNCTION                                                                     | 否             |
