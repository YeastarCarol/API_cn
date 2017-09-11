# 配置单个分机信息

通过本接口可以对单个分机进行配置，如：分机号、分机名、同时注册数、邮箱、移动分机等。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/extension/update?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/extension/update?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"extid": "1002","username": "Amy"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;extensionupdate&gt; | string | 配置单个分机信息 | N/A |
| &lt;extid&gt; | string | 确定要配置的分机号 | 1001 |
| \[extnumber\] | string | 修改后的分机号 | 1000 |
| \[username\] | string | 用户名 | 数字或字母，最大31位，可为空 |
| \[callerid\] | string | 分机来电显示名称 | 数字字母，最大31位，可为空 |
| \[registername\] | string | 注册名称 | 数字字母，最大31位，不为空 |
| \[registerpassword\] | string | 注册密码 | 限制;&\"\'\&lt;&gt;\|\（空字符也不行）最大31位，不为空 |
| \[maxregistrations\] | string | 同时注册数 | 范围1, 2, 3, 4, 5 |
| \[loginpassword\] | string | 用户密码 | 限制;&\"\'\&lt;&gt;\|\（空字符也不行）最少6位，最大63位 |
| \[email\] | string | 邮件地址 | apple@yeastar.com |
| \[mobile\] | string | 电话号码 | 最大31位，数字当呼叫转移到用户手机或者启用移动分机时，不可为空 |
| \[hasvoicemail\] | string | 语音邮箱开关 | on：开启 off：关闭 |
| \[enablevmtoemail\] | string | 是否发送语音邮件到邮箱 | on：开启 off：关闭 |
| \[vmsecret\] | string | 语音邮箱密码 | 数字，最大63位 |
| \[alwaysforward\] | string | 总是转移开关 | on：开启 off：关闭 |
| \[atransferto\] | string | 总是转移目的地 | 可选项：Voicemail, Extension, Mobile Number, Custom Number |
| \[atransferext\] | string | 目的地为分机时的分机id | 3002 |
| \[atransferprefix\] | string | 目的地为自定义号码或用户手机时的呼出前缀 | 数字，最大7位 |
| \[atransfernum\] | string | 目的地为自定义号码或用户手机时的呼出号码 | 数字，最大15位，转移目的地Custom Number不为空 |
| \[noanswerforward\] | string | 无应答转移开关 | on：开启 off：关闭 |
| \[ntransferto\] | string | 无应答转移目的地 | 可选项：Voicemail, Extension, Mobile Number, Custom Number |
| \[ntransferext\] | string | 目的地为分机时的分机id | 3002 |
| \[ntransferprefix\] | string | 目的地为自定义号码或用户手机时的呼出前缀 | 数字，最大15位，转移目的地Custom Number不为空 |
| \[ntransfernum\] | string | 目的地为自定义号码或用户手机时的号码 | 数字，最大15位，不为空 |
| \[busyforward\] | string | 忙时转移开关 | on：开启 off：关闭 |
| \[btransferto\] | string | 忙时转移目的地 | 可选项：Voicemail, Extension, Mobile Number, Custom Number |
| \[btransferext\] | string | 目的地为分机时的分机id | 3002 |
| \[btransferprefix\] | string | 目的地为自定义号码或用户手机时的呼出前缀 | 数字，最大7位 |
| \[btransfernum\] | string | 目的地为自定义号码或用户手机时的呼出号码 | 数字，最大15位，转移目的地Custom Number不为空 |
| \[enablemobile\] | string | 移动分机开关 | on：开启 off：关闭 |
| \[ringsimultaneous\] | string | 移动分机同振 | on：开启 off：关闭 |
| \[mobileprefix\] | string | 移动分机呼出前缀 | 数字，最大7位 |
| \[allowbeingmonitored\] | string | 允许被监听 | on：开启 off：关闭 |
| \[monitormode\] | string | 监听别人的方式 | 可选项：Disabled, Extensive, Listen, Whisper, Barge-in |
| \[ringtimeout\] | string | 响铃超时 | 15, 30, 60, 120, 300 |
| \[maxduration\] | string | 最大通话时长 | 可选项：Follow System, Unlimited, 60, 300, 600, 900, 1800, 3600, 6000 |
| \[dnd\] | string | 免打扰的开关 | on：开启 off：关闭 |
| \[callrestriction\] | string | 外呼限制 | on：开启 off：关闭 |
| \[agentid\] | string | 报工号时要播报的号码，。非必填项，为空的时候则默认播报分机号。 | 6932 |

**可能出现的错误码：**10006，10007

