# 查询闹铃

通过本接口可查询已经存在的闹铃的信息。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/wakeupcall/query?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/wakeupcall/query?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"extid": "1000"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;extid&gt; | string | 分机号 | 1000 |

**响应示例：**

{"status":"Success","wakeups":\[{"extid":"1000","wakeup":\[{"time":"00:45","type":"onetime","prompt":"macroform-cold\_day","repeats":"3","repeatinterval":"5"}\]}\]

**响应参数说明同添加闹铃请求参数说明**

