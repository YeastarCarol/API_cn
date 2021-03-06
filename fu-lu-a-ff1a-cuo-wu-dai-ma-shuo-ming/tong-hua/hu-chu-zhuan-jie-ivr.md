# 呼出转接IVR

通过本接口可将呼出的通话转接到IVR，从而实现：

1.向通话方播放语音文件

2.检查通话方输入的按键信息，当按键满足IVR配置的按键事件后，IPPBX会将按键信息报告给应用服务器。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/outbound/transfer_ivr?token=7d20390952e15eb72b0a1df7172de65c){version}[/outbound/transfer\_ivr?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/outbound/transfer_ivr?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"outboundid": "1495700976.276","ivrid": "6500"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;outboundid&gt; | string | 呼出编号 | 1495700976.276 |
| &lt;ivrid&gt; | int | IVR号码 | 6500 |

**响应示例：**

{"status":"Success","callid":"1495700976.275"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 呼出转接IVR结果 | Success或者Failed |
| &lt;callid&gt; | string | 该通通话的id | 1495700976.275 |

**可能出现的错误码：**10004，10007，10012，30001

