# IVR拨打外线

通过本接口可使IVR向外部电话发起呼叫，从而实现：

1.当外线接通后，向其播放语音文件

2.检查外部电话输入的按键信息，且按键满足IVR配置的按键事件后，IPPBX会将按键信息报告给应用服务器。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/ivr/dial\_outbound?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/ivr/dial_outbound?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"ivrid": "6500","outto": "41000","fromext": "1000"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| **&lt;ivrid&gt;** | String | IVR号码 | 6500 |
| **&lt;outto&gt;** | String | 呼出的被叫号码\(匹配呼出规则\) | 41000 |
| **&lt;fromext&gt;** | String | 采用哪个分机的权限 | 1000 |

**响应示例：**

{"status":"Success","callid":"1495700406.266"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| **&lt;status&gt;** | String | IVR拨打外线结果 | Success或者Failed |
| **&lt;callid&gt;** | String | 通话唯一标识符 | 1495700406.266 |



