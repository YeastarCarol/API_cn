# 修改闹铃

通过本接口可对分机已存在的闹铃进行修改。

**说明：**只能单个分机操作。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/wakeupcall/update?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/wakeupcall/update?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"extid":"1000","time":"00:45","wakeup":\[{"time":"11:00","type":"onetime","repeats":"3","repeatinterval":"5"}\]}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;extid&gt; | int | 分机号 | 1000 |
| \[time\] | string | 要修改的时间 | 11:00 |
| \[wakeup\] | object |  |  |
| \[time\] | string | 时间 | 11:22 |
| \[type\] | string | 类型 | 范围：onetime, everyday, custom |
| \[weekdays\] | string | 类型为自定义时的选项 | 范围：1,2,3,4,5,6,0                1-6:周一到周六，0：为周日 |
| \[repeats\] | string | 重复次数 | 范围：1,2,3 |
| \[repeatinterval\] | string | 重复时间 | 5（单位分钟） |
| \[prompt\] | string | 闹铃提示音 | helloworld必须为自定义提示音 |

**响应示例：**

{"status":"Success"}

可能出现的错误码：100021，10020，30001

