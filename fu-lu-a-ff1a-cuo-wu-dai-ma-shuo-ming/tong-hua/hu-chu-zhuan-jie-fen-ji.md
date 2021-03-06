# 呼出转接分机

通过本接口可将呼出到外线的通话（已从IPPBX通过呼出到外线的通话）转接给分机，从而使两者能够建立通话。

说明：不管外线号码是在响铃还是接通的状态皆可转移其他分机。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/outbound/transfer_extension?token=7d20390952e15eb72b0a1df7172de65c){version}[/outbound/transfer\_extension?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/outbound/transfer_extension?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"outboundid": "1495700976.276","extid": "1003"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;outboundid&gt; | string | 呼出编号 | 1495700976.276 |
| &lt;extid&gt; | int | 转接目的地的分机号 | 1000 |

**响应示例：**

{"status":"Success","callid":"1495700976.275"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 呼出转接分机结果 | Success或者Failed |
| &lt;callid&gt; | string | 该通通话的id | 1495700976.275 |

**可能出现的错误码：**10004，10006，10007，30001

