# CDR

当一通通话结束后，IPPBX向应用服务器实时推送该事件报告。

**报告示例：**

1.**分机内部互打CDR事件**：

{"action":"NewCdr","callid":"1495779310.371","timestart":"2017-05-25 22:15:10","callfrom":"1002","callto":"1000","desttrunkname":"","callduraction":"3","talkduraction":"2","status":"ANSWERED","type":"Internal"}

**2.分机拨打外线CDR：**

{"action":"NewCdr","callid":"1495779454.374","timestart":"2017-05-25 22:17:34","callfrom":"1002","callto":"41004","desttrunkname":"sip-142","callduraction":"4","talkduraction":"4","status":"ANSWERED","type":"Outbound"}

**3.外线呼入到分机：**

{"action":"NewCdr","callid":"1495779821.377","timestart":"2017-05-25 22:23:41","callfrom":"1000","callto":"1002","srctrunkname":"sip-142","callduraction":"18","talkduraction":"9","status":"ANSWERED","type":"Inbound"}

**报告参数说明**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;cdrid&gt; | string | CDR编号 | 123456789 |
| \[callid\] | string | 通话唯一标识 | 2000 |
| \[timestart\] | string | 开始时间 | 2017-05-25 22:26:20 |
| \[callfrom\] | string | 主叫号码 | 1000 |
| \[callto\] | string | 被叫号码 | 18000000 |
| \[callduraction\] | string | 通话时长 | 18 |
| \[talkduraction\] | string | 接听时长 | 9 |
| \[srctrunkname\] | string | 源中继名称 | Sps129 |
| \[dstrunkname\] | string | 目的中继名称 | Sps128 |
| \[status\] | string | 通话状态 | ANSWERED,  NOANSWER,   FAILED,VOICEMAIL |
| \[type\] | string | 通话类型 | Inbound, Outbound, Internal, Callback, Transfer |
| \[pincode\] | int | 密码 | 122 |
| \[recording\] | string | 全局录音文件名 | hello001 |



