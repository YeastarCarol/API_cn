# CDR

CDR是指PBX对一路通话从开始到结束的记录和统计的报告

当一通通话释放后，PBX向应用服务器实时推送该报告。

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
| **&lt;cdrid&gt;** | String | CDR编号 | 123456789 |
| **\[callid\]** | String | 通话唯一标识 | 2000 |
| **\[timestart\]** | [String]() | 开始时间 | 2017-05-25 22:26:20 |
| **\[callfrom\]** | String | 主叫号码 | 1000 |
| **\[callto\]** | String | 被叫号码 | 18000000 |
| **\[callduraction\]** | String | 通话时长 | 18 |
| **\[talkduraction\]** | String | 接听时长 | 9 |
| **\[srctrunkname\]** | String | 源中继名称 | Sps129 |
| **\[dstrunkname\]** | String | 目的中继名称 | Sps128 |
| **\[status\]** | String | 通话状态 | ANSWEREDNOANSWERFAILEDVOICEMAIL |
| **\[type\]** | String | 通话类型 | Inbound, Outbound, Internal, Callback, Transfer |
| **\[pincode\]** | Int | 密码 | 122 |





