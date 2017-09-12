# 查询来电

通过本接口可以查询当前通过外线呼入IPPBX系统的所有通话的详细信息，如：主叫，被叫，通话状态，通过的中继等。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/inbound/query?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/inbound/query?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"inboundid": "1495698433.203"}

**请求参数说明：**

1.不带参数表示查询所有来电；

2.带参数可单个或多个查询来电，多个时需用‘ , ’隔开。

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;inboundid&gt; | string | 查询所有来电 | N/A |

**响应参数：**

{"status":"Success","inbound":\[{"inboundid":"1495698433.203","from":"1000","to":"1002","trunk":"SIP-142","status":"Talking","callee":\[{"extid":"1002"}\]}\]}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| \[inbound\] | object | 来电，为由外线呼入的外部通话 | N/A |
| &lt;inboundid&gt; | int | 来电的编号，通过该参数对来电进行转接、查询、挂断等操作 | 1 |
| &lt;from&gt; | string | 主叫号码 | 1000 |
| &lt;to&gt; | string | 被叫号码 | 5003 |
| \[callee\] | object | 来电的通话方，可能为分机、IVR、去电 | 1005 |
| &lt;trunk&gt; | string | 呼入时通过的中继名 | SIP\_142 |
| &lt;status&gt; | string | 通话状态 | Talking：通话进行中             Progress：呼叫处理中          Wait:呼叫等待中 |

**可能出现的错误码：**30001

