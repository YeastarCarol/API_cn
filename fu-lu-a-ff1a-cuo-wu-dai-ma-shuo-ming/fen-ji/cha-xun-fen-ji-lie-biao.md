# 查询分机列表

通过本接口可以查询到S系列IPPBX上分机列表的基本信息，如：分机名、分机号、分机状态、类型等。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/extensionlist/query?token=6cad9cee6e2ad94570636e7b3690aeb2){version}[/extensionlist/query?token=6cad9cee6e2ad94570636e7b3690aeb2](https://192.168.5.150:8088/api/v1.0.0/extensionlist/query?token=6cad9cee6e2ad94570636e7b3690aeb2)

**请求参数说明：**

无参数，直接发送查询分机列表的请求即可。

**响应示例：**

{"status":"Success","extlist":\[{"extnumber":"1000","status":"Registered","type":"SIP","username":"Jayson","agentid":""},{"extnumber":"1001","status":"Unavailable","type":"SIP","username":"Erwin Co","agentid":""},{"extnumber":"1010","status":"Unavailable","type":"SIP","username":"lulu","agentid":""},{"extnumber":"1101","status":"Registered","type":"SIP","username":"Ina Zoiper","agentid":""},{"extnumber":"1102","status":"Registered","type":"SIP","username":"Ina Eyebeam","agentid":""},{"extnumber":"1103","status":"Unavailable","type":"SIP","username":"1103","agentid":""},{"extnumber":"1104","status":"Unavailable","type":"SIP","username":"1104","agentid":""},{"extnumber":"1105","status":"Unavailable","type":"SIP","username":"1105","agentid":""},{"extnumber":"3002","status":"unavailable","type":"SIP","username":"3002","agentid":""}\]}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;extlist&gt; | Object | 分机对象 |  |
| &lt;extnumber&gt; | string | 分机号 | 1000 |
| &lt;status&gt; | string | 分机当前状态 | Unavailable, Registered, Ringing, Busy, Hold, Malfunction, Idle, Fxsnoport |
| &lt;type&gt; | string | 分机类型 | SIP, FXS |
| \[port\] | string | 分机端口，当分机为模拟分机时则显示该项。 | Span1\_Port3 |
| &lt;username&gt; | string | 用户名 | Ina Tang |
| \[agentid\] | string | 报工号时要播报的号码。此参数默认为空，表示播报分机号。 | 6103 |

**可能出现的错误码：**30001

