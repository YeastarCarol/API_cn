# 查询闹铃

通过本接口可查询分机已经存在的闹铃的信息。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/wakeupcall/query?token=7d20390952e15eb72b0a1df7172de65c){version}[/wakeupcall/query?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/wakeupcall/query?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"extid": "1000"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;extid&gt; | string | 分机号 | 1000 |

**响应示例：**

{"status":"Success","wakeups":\[{"extid":"1000","wakeup":\[{"time":"00:45","type":"onetime","prompt":"macroform-cold\_day","repeats":"3","repeatinterval":"5"}\]}\]

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 查询闹铃结果 | Success或者Failed |
| &lt;extid&gt; | int | 分机号 | 1000 |
| &lt;wakeup&gt; | object | 对象 |  |
| &lt;time&gt; | string | 时间 | 00:45 |
| &lt;type&gt; | string | 类型，当设置为onetime时，闹铃完所设置的重复次数之后该条闹铃将被自动删除 | 范围：onetime, everyday, custom |
| \[weekdays\] | string | 类型为自定义时的选项 | 范围：1,2,3,4,5,6,0  1-6表示周一到周六，0：为周日 |
| \[repeats\] | string | 闹铃的重复次数 | 范围：1,2,3 |
| \[repeatinterval\] | string | 重复时间，设置好重复次数和重复时间后，话机响铃一次后，间隔所设置的重复时间后会再次响铃 | 5（单位分钟） |
| \[prompt\] | string | 闹铃提示音 | 此提示音必须为自定义提示音，不加字段则用系统默认的macroform-cold\_day提示音 |



