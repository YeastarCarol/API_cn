# 呼叫转移

当呼叫在IPPBX内部发生转移时，IPPBX向应用服务器推送该事件报告。

此转移只代表分机操作的转移，如：\*03，\*3，follow me等转移。API控制的转移不报告。

**报告示例：**

{"action":"Tranfer","callid":"1505291815.120","ext":{"extid":"1000"},"inbound":{"from":"102","to":"1000","trunk":"Apple\_test","inboundid":"1505291815.120"}}

**报告参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;action&gt; | string | 状态 | Transfer |
| \[extid\] | string | 发起转移的分机号 | 1002 |
| \[inboundid&#124;outbound\] | string | 来电或去电编号 | 1495771030.366 |
| \[from\] | string | 来电的原始主叫号码 | 1806354000 |
| \[to\] | string | 来电的原始被叫号码 | 1237456 |
| &lt;callid&gt; | string | 该通通话的id | 1495771030.365 |



