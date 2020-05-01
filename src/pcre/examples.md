范例
====

**示例 \#1 合法模式示例**

-   <span class="simpara">*/\<\\/\\w+\>/*</span>
-   <span class="simpara">*\|(\\d{3})-\\d+\|Sm*</span>
-   <span class="simpara">*/^(?i)php\[34\]/*</span>
-   <span class="simpara">*{^\\s+(\\s+)?$}*</span>

**示例 \#2 非法模式示例**

-   <span class="simpara"> */href='(.\*)'* - 缺失结束分隔符 </span>
-   <span class="simpara"> */\\w+\\s\*\\w+/J* - 未知模式修饰符"J"
    </span>
-   <span class="simpara"> *1-\\d3-\\d3-\\d4\|* - 缺失开始分隔符 </span>
