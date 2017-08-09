# 来电受理

如果中继的API功能开关配置为来电接听控制模式INVITE事件时，则每当有电话呼叫该中继，PBX就会将用于描述该事件的API报告消息------推送给应用服务器，并等待应用服务器在规定时间（默认10秒）内对该来电进行控制。**应用服务器可以对外线来电进行如下类型的控制：**

**accept：**如果应用服务器希望PBX继续受理该来电，则调用Accept API，PBX将会让该来电进入后续处理流程；

**refuse：**如果应用服务器希望PBX拒接该来电（如来电为黑名单内的号码），则调用Refuse API，PBX将直接挂断该来电；

·**超时处理机制：**

如果应用服务器未在规定时间内对该来电进行控制，则默认为应用服务器希望PBX继续受理该来电，即按Accept处理，则来电将会到对应呼入路由的目的地。

**请求方式：**POST

**请求地址：**

**1.Accept：**

[https://192.168.5.150:8088/api/v1.0.0/inbound/accept?token=15bc7e4a0934023e79a557e15ff1f69e](https://192.168.5.150:8088/api/v1.0.0/inbound/accept?token=15bc7e4a0934023e79a557e15ff1f69e)

**2.refuse：**

https://192.168.5.150:8088 /api/v1.0.0/inbound/refuse?token=15bc7e4a0934023e79a557e15ff1f69e

**请求示例：**

{"inboundid": "1495703883.314"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| **&lt;inboundid&gt;** | int | 接受该来电编号通话 | 1495703883.314 |

**响应示例：**

{"status":"Success"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| **&lt;accept&gt;** | String | 来电受理结果 | Success或者Failed |

**可能出现的错误码：**10004，10007，30001
