# 满意度调查结果事件

进行满意度调查时，当收到用户的按键信息后，API主动向应用服务器发送满意度调查的结果。

**报告示例：**

{"action":"satisfaction","surveyresult":"1","callid":"1504460713.60"}

**报告参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;action&gt; | string | 满意度调查结果事件 | satisfaction |
| &lt;surveyresult&gt; | string | 满意度调查按键结果 | 1 |
| &lt;callid&gt; | string | 该通通话的id | 1504460713.60 |



