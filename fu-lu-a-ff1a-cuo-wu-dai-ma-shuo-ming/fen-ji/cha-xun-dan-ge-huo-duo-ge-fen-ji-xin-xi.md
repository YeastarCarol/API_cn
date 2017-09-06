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
| &lt;extid&gt; | string | 查询单个或多个分机信息 | 1000 |

**响应示例：**

{"status":"Success","extinfos":\[{"extnumber":"1000","username":"1000","status":"Idle","type":"FXS","port":"Span2-Port1","callerid":"1000","registername":"","registerpassword":"Yeastar202","maxregistrations":"1","loginpassword":"27499b15c12640fd2dbb237bd23da850","email":"","moblie":"","language":"System Default","hasvoicemail":"on","enablevmtoemail":"off","vmsecret":"1000","alwaysforward":"off","noanswerforward":"on","ntransferto":"Voicemail","ntransferprefix":"","busyforward":"on","btransferto":"Voicemail","btransferprefix":"","ringsimultaneous":"off","mobileprefix":"","enablemobile":"off","allowbeingmonitored":"off","monitormode":"Disabled","ringtimeout":"30","maxduration":"Follow System","dnd":"off","callrestriction":"off"}\]}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;extinfos&gt; | Object | 对象 |  |
| &lt;extnumber&gt; | string | 分机号 | 1000 |
| &lt;username&gt; | string | 用户名 | Ina Tang |
| &lt;status&gt; | string | 分机当前状态 | Unavailable, Registered, Ringing, Busy, Hold, Malfunction, Idle, Fxsnoport |
| &lt;type&gt; | string | 分机类型 | SIP,FXS |
| &lt;port&gt; | string | 分机端口 | Span1\_Port3 |
| &lt;callerid&gt; | string | 来电显示号码 | 1000 |
| &lt;registername&gt; | string | 注册名称 | 1000 |
| &lt;registerpassword&gt; | string | 注册密码 | 明文显示 |
| &lt;maxregistrations&gt; | int | 同时注册数 | 5 |
| \[loginpassword\] | string | 用户密码 | MD5加密后显示 |
| \[email\] | string | 邮件地址 | ina@yeastar.com |
| \[mobile\] | string | 电话号码 | 134899999999 |
| \[language\] | string | 提示音语言 | Systemdefault |
| \[hasvoicemail\] | string | 是否启用语音邮箱 | On：开启 off：关闭 |
| \[vmsecret\] | int | 语音邮箱密码 | 3000 |
| \[enablevmtoemail\] | string | 是否发送语音邮件到邮箱 | On：开启 off：关闭 |
| \[alwaysforward\] | string | 总是转移开关 | On：开启 off：关闭 |
| \[atransferto\]                        \[atransferext\]                       \[atransferprefix\]                    \[atransfernum\] | string | 总是转移目的地 | Voicemail:   voicemail          Extension: ext1000Mobile Number: mobile139999999 Custom Number: number9+5923333 |
| \[noanswerforward\] | string | 无应答转移开关 | On：开启 off：关闭 |
| \[ntransferto\]                        \[ntransferext\]                       \[ntransferprefix\]                  \[ntransfernum\] | string | 无应答转移目的地 | Voicemail: voicemail            Extension: ext1000Mobile Number: mobile139999999 Custom Number: number9+5923333 |
| \[busyforward\] | string | 忙时转移开关 | On：开启 off：关闭 |
| \[btransferto\]                        \[btransferext\]                      \[btransferprefix\]                  \[btransfernum\] | string | 忙时转移目的地 | Voicemail: voicemail           Extension: ext1000Mobile Number: mobile13999999   Custom Number: number9+5923333 |
| \[enablemobile\] | string | 移动分机开关 | On：开启 off：关闭 |
| \[ringsimultaneous\] | string | 移动分机同振 | On：开启 off：关闭 |
| \[mobileprefix\] | string | 移动分机呼出前缀 | 空或者具体前缀 |
| \[allowbeingmonitored\] | string | 允许被监听 | On：开启 off：关闭 |
| \[monitormode\] | string | 监听模式 | 可选项：Disable, Extensive, Listen, Whisper, Barge-in |
| \[ringtimeout\] | string | 响铃超时 | 30 |
| \[maxduration\] | string | 最大通话时长 | 600 |
| \[dnd\] | string | 免打扰的开关 | On：开启 off：关闭 |
| \[callrestriction\] | string | 外呼限制 | On：开启 off：关闭 |
| \[inbound\] | object | 来电，呼入的外线通话 | N/A |
| &lt;inboundid&gt; | int | 来电的编号，依据该参数对来电进行转接、查询、挂断等操作 | 156785 |
| &lt;from&gt; | string | 主叫号码 | 1000 |
| &lt;to&gt; | string | 被叫号码 | 5003 |
| \[ext\|outer\] | object | 来电的通话方，可能为分机、去电 | 6500 |
| \[status\] | string | 通话状态 | Talking：通话进行中            Progress：呼叫处理中       Wait:呼叫等待中 |
| &lt;trunk&gt; | string | 呼入时通过的中继名 | Sip-trunk |
| \[outbound\] | osbject | 去电，呼出到外线的通话 | N/A |
| &lt;outboundid&gt; | int | 去电的编号，依据该参数对来电进行转接、查询、挂断等操作 | 1 |
| &lt;from&gt; | string | 主叫号码 | 1000 |
| &lt;to&gt; | string | 被叫号码 | 5003 |
| &lt;trunk&gt; | string | 呼出时通过的中继名 | Sip-trunk |
| \[status\] | string | 通话状态 | Talking：通话进行中           Progress：呼叫处理中       Wait:呼叫等待中 |
| &lt;agentid&gt; | string | 报工号时播报的号码 | 6362 |

**可能出现的错误码：**30001

