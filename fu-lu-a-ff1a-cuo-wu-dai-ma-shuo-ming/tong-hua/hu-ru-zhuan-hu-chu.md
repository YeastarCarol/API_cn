# 呼入转呼出

通过本接口可让外线来电转接至外线，从而实现两个外部电话能够以IPPBX为中转站建立通话。

外呼前要保证至少有一条及以上的空闲可用中继，且需借用某个分机的路由权限匹配呼出路由的呼出规则呼出。

说明：不管来电是在响铃还是正在通话的状态皆可转移至外线。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/inbound/transfer_outbound?token=7d20390952e15eb72b0a1df7172de65c){version}[/inbound/transfer\_outbound?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/inbound/transfer_outbound?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"inboundid": "1495698843.215","outto": "22003","fromext": "1000"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;inboundid&gt; | string | 呼入来电编号 | 1495698843.215 |
| &lt;outto&gt; | string | 转移到的外线号码 | 22003 |
| &lt;fromext&gt; | string | 采用哪个分机的呼出权限 | 1000 |

**响应示例：**

{"status":"Success","callid":"1495698843.215"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 呼入转接外线结果 | Success或者Failed |
| &lt;callid&gt; | string | 该通通话的id | 1495698843.215 |

**可能出现的错误码：**10004，10006，10007，30001

