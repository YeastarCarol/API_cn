# 挂断来电（强拆）

通过本接口可以指定挂断外线呼入到IPPBX系统的通话。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/inbound/hangup?token=7d20390952e15eb72b0a1df7172de65c){version}[/inbound/hangup?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/inbound/hangup?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"inboundid": "1495698510.206"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;inboundid&gt; | string | 挂断指定来电的id | 1495698510.206 |

**响应示例：**

{"status":"Success"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 挂断来电结果 | Success或者Failed |

**可能出现的错误码：**10007，10004，30001

