# 查询单个或多个分机信息

通过本接口可以查询单个或者多个分机的详细信息，如：高级配置信息等。当发送查询多个分机请求的时候，请求参数需用逗号隔开。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/extension/query?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/extension/query?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"extid": "1000"}

**请求参数说明：**

1.不带参数表示查询所有。

2.带参数可查询的单个或多个，多个需用‘ , ’隔开。如：{"extid": "1000,1001,1002"}

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;extid&gt; | string | 要查询分机的分机号 | 1000 |

**响应示例：**

{"status":"Success","extinfos":\[{"extnumber":"1000","username":"Jayson","status":"Registered","type":"SIP","callerid":"1000","registername":"1000","registerpassword":"xMn5W4Gs","maxregistrations":"1","loginpassword":"5e12ba8dd1083a7f946e457cf3c18779","email":"","moblie":"","language":"System Default","hasvoicemail":"on","enablevmtoemail":"off","vmsecret":"1000","alwaysforward":"off","noanswerforward":"on","ntransferto":"Voicemail","ntransferprefix":"","busyforward":"on","btransferto":"Voicemail","btransferprefix":"","ringsimultaneous":"off","mobileprefix":"","enablemobile":"off","allowbeingmonitored":"off","monitormode":"Disabled","ringtimeout":"30","maxduration":"Follow System","dnd":"off","callrestriction":"off","agentid":""}\]}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;extinfos&gt; | object | 对象 |  |
| &lt;extnumber&gt; | string | 分机号 | 1000 |
| &lt;username&gt; | string | 用户名 | Ina Tang |
| &lt;status&gt; | string | 分机当前状态 | Unavailable, Registered, Ringing, Busy, Hold, Malfunction, Idle, Fxsnoport |
| &lt;type&gt; | string | 分机类型 | SIP,FXS |
| \[port\] | string | 分机端口号 | Span1\_Port3 |
| &lt;callerid&gt; | string | 来电显示号码 | 1000 |
| &lt;registername&gt; | string | 注册名称 | 1000 |
| &lt;registerpassword&gt; | string | 注册密码 | 明文显示 |
| &lt;maxregistrations&gt; | int | 同时注册数 | 5 |
| &lt;loginpassword&gt; | string | 用户密码 | MD5加密后显示 |
| &lt;email&gt; | string | 邮件地址 | ina@yeastar.com |
| &lt;mobile&gt; | string | 电话号码 | 134899999999 |
| &lt;language&gt; | string | 提示音语言 | Systemdefault |
| &lt;hasvoicemail&gt; | string | 是否启用语音邮箱 | on：开启 off：关闭 |
| &lt;vmsecret&gt; | int | 语音邮箱密码 | 3000 |
| &lt;enablevmtoemail&gt; | string | 是否发送语音邮件到邮箱 | on：开启 off：关闭 |
| &lt;alwaysforward&gt; | string | 总是转移开关 | on：开启 off：关闭 |
| \[atransferto\]                        \[atransferext\]                       \[atransferprefix\]                    \[atransfernum\] | string | 总是转移目的地 | Voicemail:  Voicemail          Extension: Extension 1000Mobile Number: Mobile139999999                                 Custom Number: Number9+5923333 |
| \[noanswerforward\] | string | 无应答转移开关 | on：开启 off：关闭 |
| \[ntransferto\]                        \[ntransferext\]                       \[ntransferprefix\]                  \[ntransfernum\] | string | 无应答转移目的地 | Voicemail: Voicemail            Extension: 1000                  Mobile Number: Mobile139999999                                 Custom Number: Number9+5923333 |
| \[busyforward\] | string | 忙时转移开关 | on：开启 off：关闭 |
| \[btransferto\]                        \[btransferext\]                      \[btransferprefix\]                  \[btransfernum\] | string | 忙时转移目的地 | Voicemail: Voicemail           Extension: Ext1000            Mobile Number: Mobile13999999                                    Custom Number: Number95923333 |
| &lt;enablemobile&gt; | string | 移动分机开关 | on：开启 off：关闭 |
| \[ringsimultaneous\] | string | 移动分机同振 | on：开启 off：关闭 |
| \[mobileprefix\] | string | 移动分机呼出前缀 | 空或者具体前缀 |
| &lt;allowbeingmonitored&gt; | string | 允许被监听 | on：开启 off：关闭 |
| &lt;monitormode&gt; | string | 监听模式 | 可选项：Disable, Extensive, Listen, Whisper, Barge-in |
| &lt;ringtimeout&gt; | string | 响铃超时 | 30 |
| &lt;maxduration&gt; | string | 最大通话时长 | 600 |
| &lt;dnd&gt; | string | 免打扰的开关 | on：开启 off：关闭 |
| &lt;callrestriction&gt; | string | 外呼限制 | on：开启 off：关闭 |
| &lt;agentid&gt; | string | 报工号时所要播报的号码，默认为空，播报分机号。如有设置，则播报所设置的号码。 | 6362 |
| \[inbound\] | object | 来电，呼入的外线通话 | N/A |
| &lt;inboundid&gt; | string | 来电的编号，依据该参数对来电进行转接、查询、挂断等操作 | 156785 |
| &lt;from&gt; | string | 主叫号码 | 1000 |
| &lt;to&gt; | string | 被叫号码 | 5003 |
| \[ext\|outer\] | object | 来电的通话方，可能为分机、去电 | 6500 |
| &lt;status&gt; | string | 通话状态 | Talking：通话进行中            Progress：呼叫处理中       Wait:呼叫等待中 |
| &lt;trunk&gt; | string | 呼入时通过的中继名 | Sip-trunk |
| \[outbound\] | object | 去电，呼出到外线的通话 | N/A |
| &lt;outboundid&gt; | string | 去电的编号，依据该参数对来电进行转接、查询、挂断等操作 | 1 |
| &lt;from&gt; | string | 主叫号码 | 1000 |
| &lt;to&gt; | string | 被叫号码 | 5003 |
| &lt;trunk&gt; | string | 呼出时通过的中继名 | Sip-trunk |
| &lt;status&gt; | string | 通话状态 | Talking：通话进行中           Progress：呼叫处理中       Wait:呼叫等待中 |

**可能出现的错误码：**30001

