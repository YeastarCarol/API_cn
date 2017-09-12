# 查询单个或多个队列

通过本接口可以查询单个或多个队列的详细信息，如：队列号码，队列名称，静态坐席，动态坐席等。多个查询的时，查询参数用逗号隔开。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/queue/query?token=6cad9cee6e2ad94570636e7b3690aeb2](https://192.168.5.150:8088/api/v1.0.0/queue/query?token=6cad9cee6e2ad94570636e7b3690aeb2)

**请求示例：**

{"queueid": "6701"}

**请求参数说明：**

1.不带参数表示查询所有；

2.带参数可查询的单个或多个，多个需用‘ , ’隔开。如：{"queueid": "6500,6501,6502"}。

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;queueid&gt; | string | 查询单个或多个队列 | 6202 |

**响应示例：**

{"status":"Success","queues":\[{"queuenumber":"6701","password":"","queuename":"6701","ringstrategy":"Ring All","failoveraction":"Hang up","agents":"1001,1002,1003,1004,1005,1006,","agenttimeout":"30","agentannounce":"\[None\]","wrapuptime":"30","ringinuse":"on","retry":"30","musiconhold":"\[None\]","maxwaittime":"1800","joinempty":"off","leavewhenempty":"on","joinannounce":"\[None\]","announcepos":"on","announcefreq":"30","announceholdtime":"on","userannounce":"\[None\]","userannouncefreq":"30","breakoutkey":"None","satisfactionsurvey":"None","idannouncement":"None"}\]}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| \[queues\] | object | 队列 | N/A |
| &lt;queuenumber&gt; | int | 队列号码 | 6701 |
| &lt;queuename&gt; | string | 队列名称 | Productteam |
| &lt;password&gt; | string | 加入动态坐席的密码 | 123456 |
| &lt;ringstrategy&gt; | string | 响铃策略 | Ring All, Least Recent, Fewest Calls, Random, Rrmemory, Linear |
| &lt;failoveraction&gt; | string | 呼入失败目的地 | Hang up |
| \[agents\] | string | 固定座席 | 1000，1001 |
| &lt;agenttimeout&gt; | string | 坐席响铃时间 | 30 |
| &lt;agentannounce&gt; | string | 坐席应答提示音 | \[None\] |
| &lt;wrapuptime&gt; | int | 休息时间 | 30 |
| &lt;ringinuse&gt; | string | 使用中振铃 | on |
| &lt;retry&gt; | int | 重试间隔时间 | 30 |
| &lt;musiconhold&gt; | string | 等待音乐 | \[None\] |
| &lt;maxwaittime&gt; | int | 最大等待时间 | 30 |
| &lt;joinempty&gt; | string | 无座席时允许呼入 | \[None\] |
| &lt;leavewhenempty&gt; | string | 无座席时结束等待 | on |
| \[joinannounce\] | string | 进入队列提示音 | \[None\] |
| &lt;announcepos&gt; | string | 公告当前位置 | on |
| &lt;announcefreq&gt; | string | 用户公告频率 | 30 |
| &lt;announceholdtime&gt; | int | 公告等待时间 | 30 |
| &lt;userannounce&gt; | string | 系统公告提示音 | \[None\] |
| &lt;userannouncefreq&gt; | int | 系统公告频率 | 30 |
| \[breakoutkey\] | string | 按键DTMF | None |
| \[breakoutaction\] | string | 按键目标 |  |
| \[breakoutdest\] | string | 按键目标的最终目的地 |  |
| \[idannouncement\] | string | 报工号提示音 | None |
| \[satisfactionsurvey\] | string | 满意度调查 | None |

**可能出现的错误码：**10013，30001

