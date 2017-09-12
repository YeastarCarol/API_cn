# 查询去电

通过本接口可以查询当前IPPBX系统分机通过外线呼出的所有通话的详细信息，如：主叫，被叫，通话状态，通过的中继，目的地等。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/outbound/query?token=6cad9cee6e2ad94570636e7b3690aeb2](https://192.168.5.150:8088/api/v1.0.0/outbound/query?token=6cad9cee6e2ad94570636e7b3690aeb2)

**请求示例：**

{"outboundid": "1495705009.316"}

**请求参数说明：**

1.不带参数表示查询所有去电；

2.带参数可查询单个或多个去电，多个需用 ‘ , ’ 隔开。

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;outboundid&gt; | string | 查询所有去电 | N/A |

**响应示例：**

{"status":"Success","outbound":\[{"outboundid":"1495705009.316","from":"1002","to":"41000","trunk":"SIP-142","status":"Talking"}\]}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;outbound&gt; | object | 去电，为呼出到外线的外部通话 | N/A |
| &lt;outboundid&gt; | string | 去电的编号，通过该参数对去电进行转接、查询、挂断等操作 | 1495705009.316 |
| &lt;from&gt; | string | 主叫号码 | 1000 |
| &lt;to&gt; | string | 被叫号码 | 41000 |
| &lt;trunk&gt; | string | 呼出时通过的中继名称 | SIP-142 |
| \[status\] | string | 通话状态 | Talking：通话进行中            Progress：呼叫处理中          Wait:呼叫等待中 |

**可能出现的错误码：**30001

