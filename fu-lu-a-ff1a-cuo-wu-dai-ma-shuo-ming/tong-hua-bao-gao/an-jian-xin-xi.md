# 按键信息

该事件用于报告用户输入的按键信息。

呼叫（来电/去电/分机）转接到IVR并接通的情况下，当用户按键满足IVR的按键事件时，IPPBX向应用服务器推送该事件。

**报告示例：**

{"action":"DTMF","callid":"1495705009.315","outbound":{"from":"1002","to":"41000","trunk":"SIP-142","outboundid":"1495705009.316"},"info":"\#"}

**报告参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;action&gt; | string | 按键事件 | DTMF |
| &lt;callid&gt; | string | 该通通话的id | 1495707950.331 |
| \[inbound\|outbound\] | object | 来电或去电 |  |
| &lt;trunk&gt; | string | 通过的中继名称 | sip-142 |
| &lt;inboundid&gt; | string | 来电编号 | 1495707950.331 |
| &lt;from&gt; | string | 原始主叫号码 | 1000 |
| &lt;to&gt; | string | 原始被叫号码 | 1002 |
| &lt;info&gt; | string | 按键信息 | \# |



