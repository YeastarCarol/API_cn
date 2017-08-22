# 呼叫转移

当呼叫在IPPBX内部发生转移时，IPPBX向应用服务器推送该事件报告。

此转移只代表分机操作的转移，如：\*03，\*3，follow me等转移。API控制的转移不报告。

**报告示例：**

{"action":"Tranfer","callid":"1494834266.75","inbound":{"from":"3009","to":"2002","trunk":"DIGIT1","inboundid":"1494834266.75"}}

