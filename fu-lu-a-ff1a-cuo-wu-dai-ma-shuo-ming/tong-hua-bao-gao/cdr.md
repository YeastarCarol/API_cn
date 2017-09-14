# CDR

当一通通话结束后，IPPBX向应用服务器实时推送该事件报告。

**报告示例：**

1.**分机内部互打CDR事件**：

{"action":"NewCdr","callid":"1495779310.371","timestart":"2017-05-25 22:15:10","callfrom":"1002","callto":"1000","desttrunkname":"","callduraction":"3","talkduraction":"2","status":"ANSWERED","type":"Internal"}

**2.分机拨打外线CDR：**

{"action":"NewCdr","callid":"1505352615.274","timestart":"2017-09-14 09:30:15","callfrom":"1000","callto":"91000","desttrunkname":"Apple\_test","callduraction":"29","talkduraction":"29","status":"ANSWERED","type":"Outbound","pincode":"1000","recording":"20170914093038-1505352615.274-1000-91000-Outbound.wav"}

**3.外线呼入到分机：**

{"action":"NewCdr","callid":"1505352445.265","timestart":"2017-09-14 09:27:25","callfrom":"102","callto":"1000","srctrunkname":"Apple\_test","callduraction":"38","talkduraction":"29","status":"ANSWERED","type":"Inbound","recording":"20170914092747-1505352445.265-102-1000-Inbound.wav"}

**报告参数说明**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;cdrid&gt; | string | CDR编号 | 123456789 |
| &lt;callid&gt; | string | 通话唯一标识 | 2000 |
| \[timestart\] | string | 开始时间 | 2017-05-25 22:26:20 |
| \[callfrom\] | string | 主叫号码 | 1000 |
| \[callto\] | string | 被叫号码 | 18000000 |
| \[callduraction\] | string | 通话时长 | 18 |
| \[talkduraction\] | string | 接听时长 | 9 |
| \[srctrunkname\] | string | 源中继名称 | Apple\_test |
| \[dstrunkname\] | string | 目的中继名称 | Apple\_test |
| \[status\] | string | 通话状态 | ANSWERED,  NOANSWER,   FAILED,VOICEMAIL |
| \[type\] | string | 通话类型 | Inbound, Outbound, Internal, Callback, Transfer |
| \[pincode\] | int | 密码 | 1000 |
| \[recording\] | string | 全局录音文件名 | 20170914092747-1505352445.265-102-1000-Inbound.wav |



