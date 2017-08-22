# **通过GSM中继发送短信**

通过GSM外线给外部号码发送短信。

应用场景：拨打人工服务的时候，人工可按某个键直接把要查询的具体内容发到你手机上。

说明：信息内容字符限制为最多1000个汉字，即2000个字符，不能包含表情。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.1/sms/send?token=42af22de1f4b884950310d132232b4b5](https://192.168.5.150:8088/api/v1.0.1/sms/send?token=42af22de1f4b884950310d132232b4b5)

**请求示例：**

{"trunk":"GSM-trunk","phonenumber":"18396210850","message":"%E4%BD%A0%E5%A5%BD "}

**注：短信内容必须经过URL编码。可参考：**[http://tool.oschina.net/encode?type=4](http://tool.oschina.net/encode?type=4)

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;phonenumber&gt; | string | 手机号码 | 1804630\*\*\*\* |
| &lt;message&gt; | string | 信息内容\(需经过URL编码\) | %E4%BD%A0%E5%A5%BD |
| &lt;trunk&gt; | string | 使用的GSM中继名 | GSM-trunk |

**响应示例：**

**指令发送正确：**{"status":"Success","smsid":"18396210850-1502874159"}

**短信发送成功：**{"status":"Success","smsid":"18396210850-1502874159"}

**短信发送失败：**{"action":"sms-send","status":"Failed","smsid":"18396210850-1502874159"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 请求结果 | Success或者Failed |

**可能出现的错误码：**10027

