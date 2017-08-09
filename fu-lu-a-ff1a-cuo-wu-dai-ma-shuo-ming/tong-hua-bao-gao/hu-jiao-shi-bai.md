

# 呼叫失败

该事件通常作为API请求的响应消息出现，特殊情况下，PBX也会推送该事件消息。

呼叫失败的定义为：只要是被叫方未接通的状况都定义为呼叫失败，转到语音留言算已接通。

不管是API控制的呼叫还是手动拨号的呼叫，只要呼叫失败都会触发。

**报告示例：**

**1.分机没有呼叫权限：**

{"action":"CallFailed","reason":"NO Outbound Restriction","callid":"1495420603.349"}

**2.被叫开启DND：**

{"action":"CallFailed","reason":"DND","callid":"1495186077.229","ext":{"extid":"1005"}}

**3.外线不可用：**

{"action":"CallFailed","reason":"Line unreachable","callid":"1495184155.216","ext":{"extid":"1002"}}

**4.分机A打分机B，B拒接（call forward禁用）：**

{"action":"CallFailed","reason":"User busy","callid":"1495770583.355"}

#### 



