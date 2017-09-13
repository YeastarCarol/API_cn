# 来电呼入

在开启中继的“来电接听控制”情况下，当来电通过该中继呼入时，在IPPBX应答该来电后，会向应用服务器推送INCOMING事件。

**报告示例：**

{"action":"Incoming","callid":"1495707950.331","inbound":{"from":"1000","to":"1002","trunk":"sip-142","inboundid":"1495707950.331"}}

**报告参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;action&gt; | string | 来电呼入 | Incoming |
| &lt;callid&gt; | string | 该通通话的id | 1495707950.331 |
| &lt;inbound&gt; | object | 来电 |  |
| &lt;trunk&gt; | string | 通过的中继名称 | sip-142 |
| &lt;inboundid&gt; | string | 来电编号 | 1495707950.331 |
| &lt;from&gt; | string | 原始主叫号码 | 1000 |
| &lt;to&gt; | string | 原始被叫号码 | 1002 |



