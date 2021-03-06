# 给外线播放提示音

通过本接口可给外线号码播放提示音，IPPBX拨打外线，外线响铃接起后，听到提示音。支持多段提示音拼接播放。请求时多段提示音用‘+’号连接。注：该提示音文件名不能为纯数字，也不能有‘+’号。

**前提条件：**所有的提示音必须为已经上传至IPPBX的自定义提示音。

**说明：**PSTN外线拨出去时，不管终端话机有没有接起线路已经接通，这属于特殊情况，此接口对PSTN无效。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/outbound/playprompt?token=7d20390952e15eb72b0a1df7172de65c){version}[/outbound/playprompt?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/outbound/playprompt?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"outto": "41000","prompt":"hello111","fromext":"1000"}

{ "outto": "1000000","prompt":"1+queue1+queue2","autoanswer":"no"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;outto&gt; | string | 外线号码 | 41000 |
| &lt;prompt&gt; | string | 自定义音乐 | hello111 |
| \[fromext\] | int | 借用呼出权限的分机号 | 1000 |

**响应示例：**

{"status":"Success","callid":"1495701728.300"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 外线播放提示音结果 | Success或者Failed |

**可能出现的错误码：**10004，10023，10015，10006，30001

