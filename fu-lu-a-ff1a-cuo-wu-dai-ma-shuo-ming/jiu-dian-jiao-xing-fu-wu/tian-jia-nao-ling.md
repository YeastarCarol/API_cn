# 添加闹铃

通过本接口可以给分机设置闹铃。

说明：支持多个分机一起添加闹铃相同的闹铃，且一次只能添加一个闹铃，如一次添加多个则只有第一个生效。如需多个分机添加同一个闹铃，则分机之间使用逗号隔开。

如：{"extid":"1000,1001","wakeup":\[{"time":"00:45","type":"onetime","repeats":"3","repeatinterval":"5"}\]}

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/wakeupcall/create?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/wakeupcall/create?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"extid":"1000","wakeup":\[{"time":"00:45","type":"onetime","repeats":"3","repeatinterval":"5"}\]}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;extid&gt; | string | 分机号 | 1000 |
| &lt;wakeup&gt; | object | 对象 |  |
| &lt;time&gt; | string | 时间 | 11:22 |
| &lt;type&gt; | string | 类型，当设置为onetime时，闹铃完所设置的重复次数之后该条闹铃将被自动删除 | 范围：onetime, every day, custom |
| \[weekdays\] | string | 类型为自定义时的选项 | 范围：1234560  1-6表示周一到周六，0：为周日 |
| \[repeats\] | string | 闹铃的重复次数 | 范围：1，2，3 |
| \[repeatinterval\] | string | 重复时间，设置好重复次数和重复时间后，话机响铃一次后，间隔所设置的重复时间后会再次响铃 | 5（单位分钟） |
| \[prompt\] | string | 闹铃提示音 | helloworld必须为自定义提示音，不加字段则用默认macroform-cold\_day |

**响应示例：**

{"status":"Success"}

**可能出现的错误码：**10006，10020，30001

