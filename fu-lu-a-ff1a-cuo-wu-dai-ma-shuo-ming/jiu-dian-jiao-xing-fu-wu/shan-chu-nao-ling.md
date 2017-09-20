# 删除闹铃

通过本接口可删除某个分机存在的闹铃。

**说明：**只能单个分机操作。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/wakeupcall/delete?token=7d20390952e15eb72b0a1df7172de65c){version}[/wakeupcall/delete?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/wakeupcall/delete?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"extid": "1000","time":"11:00"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;extid&gt; | string | 分机号 | 1000 |
| \[time\] | string | 有带该参数则只删除指定的时间，不带该参数则删除该分机所有闹铃信息。 | 11:00 |

**响应示例：**

{"status":"Success"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 删除闹铃结果 | Success或者Failed |

**可能出现的错误码：**10021，30001

