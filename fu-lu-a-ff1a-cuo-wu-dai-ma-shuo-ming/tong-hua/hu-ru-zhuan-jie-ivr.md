# 呼入转接IVR

通过本接口可将来电转接到IVR。

说明：不管来电是在响铃还是正在通话的状态皆可将通话转移至IVR

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/inbound/transfer_ivr?token=7d20390952e15eb72b0a1df7172de65c){version}[/inbound/transfer\_ivr?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/inbound/transfer_ivr?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"inboundid": "1495698591.209","ivrid": "6500"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;inboundid&gt; | string | 呼入来电编号 | 1495698591.209 |
| &lt;ivrid&gt; | int | 转接目的地的IVR号码 | 6500 |

**响应示例：**

{"status":"Success","callid":"1495698591.209"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 呼入转接IVR结果 | Success或者Failed |
| &lt;callid&gt; | string | 该通通话的id | 1495698591.209 |

**可能出现的错误码：**10004，10006，10012，30001

