# **通过GSM中继发送短信**

通过GSM外线给外部号码发送短信。

应用场景：拨打人工服务的时候，人工可按某个键直接把要查询的具体内容发到你手机上。

说明：信息内容字符限制为最多1000个汉字，即2000个字符，不能包含表情。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.1/sms/send?token=42af22de1f4b884950310d132232b4b5){version}[/sms/send?token=42af22de1f4b884950310d132232b4b5](https://192.168.5.150:8088/api/v1.0.1/sms/send?token=42af22de1f4b884950310d132232b4b5)

**请求示例：**

{"trunk":"GSM-trunk","phonenumber":"18396210850","message":"%E4%BD%A0%E5%A5%BD "}

**注：短信内容必须经过URL编码。中文可参考：**[http://tool.oschina.net/encode?type=4](http://tool.oschina.net/encode?type=4)

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;phonenumber&gt; | string | 手机号码 | 1804630\*\*\*\* |
| &lt;message&gt; | string | 信息内容\(需经过URL编码\) | %E4%BD%A0%E5%A5%BD |
| &lt;trunk&gt; | string | 使用的GSM中继名 | GSM-trunk |

**响应示例：**

**请求发送正确：**{"status":"Success","smsid":"18396210850-1502874159"}

**短信发送成功：**{"action":"sms-send","status":"Succeed","smsid":"18396210850-1502874445"}

**短信发送失败：**{"action":"sms-send","status":"Failed","smsid":"18396210850-1502874159"}

注：此请求会有产生两条响应，一条表明发送的请求是否正确，一条则表明短信是否发送成功。

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;action&gt; | object | 表明该条响应是短信发送的结果 | sms-send |
| &lt;status&gt; | string | 请求结果 | Success或者Failed |
| &lt;smsid&gt; | string | 每条短信的唯一标识 | 18396210850-1502874159 |

**可能出现的错误码：**10027

