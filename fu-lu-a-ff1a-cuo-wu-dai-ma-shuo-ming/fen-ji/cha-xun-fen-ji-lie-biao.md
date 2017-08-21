# 查询分机列表

通过本接口可以查询到S系列IPPBX上分机列表的基本信息，如：分机名、分机号、分机状态、类型等。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/extensionlist/query?token=6cad9cee6e2ad94570636e7b3690aeb2](https://192.168.5.150:8088/api/v1.0.0/extensionlist/query?token=6cad9cee6e2ad94570636e7b3690aeb2)

**请求参数说明：**

无参数，直接发送查询分机列表的请求即可。

**响应示例：**

{"status":"Success","extlist":\[{"extnumber":"1000","status":"Idle","type":"FXS","port":"Span2-Port1","username":"1000"},{"extnumber":"1001","status":"Idle","type":"FXS","port":"Span2-Port2","username":"1001"},{"extnumber":"1002","status":"Registered","type":"SIP","username":"Amy"},{"extnumber":"1003","status":"Registered","type":"SIP","username":"1003"},{"extnumber":"1004","status":"Registered","type":"SIP","username":"1004"},{"extnumber":"1005","status":"Registered","type":"IAX","username":"1005"},{"extnumber":"1006","status":"Unavailable","type":"SIP","username":"Lisa"}\]}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;extlist&gt; | Object | 分机对象 |  |
| &lt;extnumber&gt; | string | 分机号 | 1000 |
| &lt;status&gt; | string | 分机当前状态 | Unavailable, Registered, Ringing, Busy, Hold, Malfunction, Idle, Fxsnoport |
| &lt;type&gt; | string | 分机类型 | SIP, FXS |
| \[port\] | string | 分机端口 | Span1\_Port3 |
| &lt;username&gt; | string | 分机名 | Ina Tang |

**可能出现的错误码：**30001

