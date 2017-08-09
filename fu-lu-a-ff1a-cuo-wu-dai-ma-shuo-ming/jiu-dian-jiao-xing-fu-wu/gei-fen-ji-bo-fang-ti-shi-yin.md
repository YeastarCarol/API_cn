

# 给分机播放音乐

说明：只能单个分机操作

**请求方式：**POST（HTTPS）

**请求地址：**https://192.168.5.150:8088/api/v1.0.0/extension/playprompt?token=7d20390952e15eb72b0a1df7172de65c

**请求示例：**

{"extid": "1000","prompt":"111","autoanswer":"no"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| **&lt;extid&gt;** | String | 分机号 | 1000 |
| **&lt;prompt&gt;** | String | 自定义音乐 | 111必须为自定义提示音 |
| **\[autoanswer\]** | String | 自动接听 | yes/no |

**响应示例：**

{"status":"Success","callid":"1495697869.171"}

**可能出现的错误码：**10004，10023，10015，10006，30001

