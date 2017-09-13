# IVR拨打分机

通过本端口可让IVR呼叫分机，从而实现：

1.向分机播放语音文件；

2.检查分机输入的按键信息，且按键满足IVR配置的按键事件后，IPPBX会将按键信息报告给应用服务器。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/ivr/dial\_extension?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/ivr/dial_extension?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"ivrid": "6500","extid": "1002","autoanswer":"no"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;ivrid&gt; | string | IVR号码 | 6500 |
| &lt;extid&gt; | string | 要呼叫的分机号 | 1002 |
| &lt;autoanswer&gt; | string | 是否自动接听\(只针对SIP线路有效，且需要话机支持，此参数不带则默认为不自动应答\) | yes/no |

**响应示例：**

{"status":"Success","callid":"1495700350.261"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | IVR拨打分机结果 | Success或者Failed |
| &lt;callid&gt; | string | 该通通话的id | 1495700350.261 |

**可能出现的错误码：**10004，10006，10012，30001

