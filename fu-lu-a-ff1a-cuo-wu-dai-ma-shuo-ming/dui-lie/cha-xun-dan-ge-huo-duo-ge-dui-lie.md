# 查询单个或多个队列

通过本接口可以查询单个或多个队列详细信息，如：队列号码，队列名称，静态坐席，动态坐席等。多个查询的时，查询参数用逗号隔开。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/queue/query?token=6cad9cee6e2ad94570636e7b3690aeb2](https://192.168.5.150:8088/api/v1.0.0/queue/query?token=6cad9cee6e2ad94570636e7b3690aeb2)

**请求示例：**

{"queueid": "6701"}

**请求参数说明：**

1.不带参数表示查询所有；

2.带参数可查询的单个或多个，多个需用‘，’隔开。如：{"ivrid": "6500,6501,6502"}。

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| **&lt;queueid&gt;** | String | 查询单个或多个队列 | 6202 |

**响应示例：**

{"status":"Success","queues":\[{"queuenumber":"6701","password":"","queuename":"6700","ringstrategy":"Ring All","failoveraction":"Hang up\[None\]","agents":"1000,1001,1002,1003,1004,1005,1006,","agenttimeout":"30","agentannounce":"\[None\]","wrapuptime":"30","ringinuse":"on","retry":"30","musiconhold":"\[None\]","maxwaittime":"1800","joinempty":"off","leavewhenempty":"on","joinannounce":"\[None\]","announcepos":"on","announcefreq":"30","announceholdtime":"on","userannounce":"","userannouncefreq":"30","breakoutkey":"None"}\]}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| **\[queues\]** | object | 队列 | N/A |
| **&lt;queuenumber&gt;** | int | 队列号码 | 6701 |
| **&lt;queuename&gt;** | String | 队列名称 | Productteam |
| **&lt;password&gt;** | String | 加入动态坐席的密码 | 123456 |
| **&lt;ringstrategy&gt;** | String | 响铃策略 | 全部响铃，线性响铃，顺序响铃，最近最少被叫响铃，最少接通响铃，随机响铃 |
| **&lt;failoveraction&gt;** | String | 呼入失败目的地 | Hang up |
| **\[agents\]** | string | 固定座席 | 1000，1001 |
| **&lt;agenttimeout&gt;** | String | 坐席响铃时间 | 30 |
| **&lt;agentannounce&gt;** | String | 坐席应答提示音 | \[None\] |
| **&lt;wrapuptime&gt;** | Int | 休息时间 | 30 |
| **&lt;ringinuse&gt;** | String | 使用中振铃 | on |
| **&lt;retry&gt;** | Int | 重试间隔时间 | 30 |
| **&lt;musiconhold&gt;** | String | 等待音乐 | \[None\] |
| **&lt;maxwaittime&gt;** | Int | 最大等待时间 | 30 |
| **&lt;joinempty&gt;** | String | 无座席时允许呼入 | \[None\] |
| **&lt;leavewhenempty&gt;** | String | 无座席时结束等待 | on |
| **\[joinannounce\]** | String | 进入队列提示音 | \[None\] |
| **&lt;announcepos&gt;** | String | 公告当前位置 | on |
| **&lt;announcefreq&gt;** | String | 用户公告频率 | 30 |
| **&lt;announceholdtime&gt;** | Int | 公告等待时间 | 30 |
| **&lt;userannounce&gt;** | String | 系统公告提示音 | \[None\] |
| **&lt;userannouncefreq&gt;** | Int | 系统公告频率 | 30 |
| **\[breakoutkey\]** | String | 按键DTMF | None |
| **\[breakoutaction\]** | String | 按键目标 |  |
| **\[breakoutdest\]** | String | 按键目标的最终目的地 |  |

**可能出现的错误码：**10013，30001

