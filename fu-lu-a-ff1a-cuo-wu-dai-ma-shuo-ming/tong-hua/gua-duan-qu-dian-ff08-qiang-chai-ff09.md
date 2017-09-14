# 挂断去电（强拆）

通过本接口可以指定挂断IPPBX通过外线呼出的通话。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/outbound/hangup?token=6cad9cee6e2ad94570636e7b3690aeb2){version}[/outbound/hangup?token=6cad9cee6e2ad94570636e7b3690aeb2](https://192.168.5.150:8088/api/v1.0.0/outbound/hangup?token=6cad9cee6e2ad94570636e7b3690aeb2)

**请求示例：**

{"outboundid": "1495705264.322"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;outboundid&gt; | string | 挂断指定呼出的通话的id | 1495705264.322 |

**响应参数说明：**

{"status":"Success"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 挂断去电结果 | Success或者Failed |

**可能出现的错误码：**10007，10004，30001



