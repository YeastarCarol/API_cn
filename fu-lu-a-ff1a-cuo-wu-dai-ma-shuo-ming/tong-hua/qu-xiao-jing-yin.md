# 取消静音

通过被接口可将被静音的分机取消静音。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/extension/unmute?token=7d20390952e15eb72b0a1df7172de65c){version}[/extension/unmute?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/extension/unmute?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"extid": "1000"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;extid&gt; | int | 要解除静音的分机号 | 1000 |

**响应示例：**

{"status":"Success"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 解除分机静音结果 | Success或者Failed |

**可能出现的错误码：**10004，10007，30001

