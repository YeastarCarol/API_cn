# 查询中继列表

通过本接口可查询所有中继的基本信息，如：中继名、中继状态、中继类型等。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/trunklist/query?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/trunklist/query?token=7d20390952e15eb72b0a1df7172de65c)

**请求参数说明：**

无参数，直接发送查询中继列表请求即可。

**响应示例：**

{"status":"Success","trunklist":\[{"trunkname":"DIGIT1","status":"Down","type":"E1","port":"Span1-Port1"},{"trunkname":"FXO2-3","status":"Idle","type":"FXO","port":"Span2-Port3"},{"trunkname":"FXO2-4","status":"Fault","type":"FXO","port":"Span2-Port4"},{"trunkname":"BRI2-5","status":"Fault","type":"BRI","port":"Span2-Port5"},{"trunkname":"BRI2-6","status":"Fault","type":"BRI","port":"Span2-Port6"},{"trunkname":"GSM2-7","status":"No SIM","type":"GSM","port":"Span2-Port7"},{"trunkname":"SIP-142","status":"Registered","type":"SIP"}\]}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;trunklist&gt; | object | 对象 |  |
| &lt;trunkname&gt; | string | 中继名 | Sip trunk test |
| &lt;status&gt; | string | 中继当前状态 | Fault |
| &lt;type&gt; | string | 中继类型 | SIP, FXO,GSM,BRI,E1 |
| \[port\] | string | 中继端口 | Span1\_Port3 |

**可能出现的错误码：**30001

**附：各类型中继可能的状态**

| FXO中继 | BRI/E1/T1/J1 | GSM/CDMA/UMTS | SIP/IAX |
| :--- | :--- | :--- | :--- |
| 1.Fault                                     2.Idle                                      3.Busy | 1.Fault                                  2.Alarm                                 3.Down                                   4.Up | 1.Poweroff                           2.Alarm                                 3.No SIM                               4.No Signal                           5.Pin Error                            6.Unregister                        7.Busy                                  8.Idle | 1.Registering                         2.Failure                               3.Registered \(Unmonitored\)                                           4.Disable                              5.Unknown |



