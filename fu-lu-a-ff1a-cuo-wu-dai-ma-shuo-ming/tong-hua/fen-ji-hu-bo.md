# 分机互拨

通过本接口可以让一个分机呼叫另一个分机，从而使两者能够建立通话。

发送分机A拨分机B的请求后，分机A先响铃，摘机后，分机B响铃。如果开启了自动应答，则主叫方直接听到回铃音，被叫方响铃。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/extension/dial_extension?token=7d20390952e15eb72b0a1df7172de65c){version}[/extension/dial\_extension?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/extension/dial_extension?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"caller": "1000","callee": "1002","autoanswer":"no"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;caller&gt; | string | 主叫分机 | 1000 |
| &lt;callee&gt; | string | 被叫分机 | 1002 |
| \[autoanswer\] | string | 是否自动接听[\(]()只针对SIP线路有效，且需要话机支持，此参数不带则默认为不自动应答\) | yes/no |

**响应示例：**

{"status":"Success","callid":"1505193218.96"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 分机拨打分机结果 | Success或者Failed |
| \[callid\] | string | 该通通话的id | 1505193218.96 |

**可能出现的错误代码：**10004，10006，30001

