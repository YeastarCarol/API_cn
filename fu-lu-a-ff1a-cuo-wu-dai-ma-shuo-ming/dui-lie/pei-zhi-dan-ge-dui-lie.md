# 配置单个队列

通过本接口可对单个队列进行配置。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/v1.0.0/queue/update?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/queue/update?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"queueid": "6701","queuenumber":"6701"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| **&lt;queueid&gt;** | int | 请求时的队列号码 | 6200 |
| **\[queuenumber\]** | int | 修改后的队列号码 | 6200 |
| **\[queuename\]** | String | 队列名称 | 限制:!$\(\)\/\#;,\\"=&lt;&gt;&'\`^%@{}\|\（空字符也不行）最大31位，不为空 |
| **\[password\]** | String | 加入动态坐席的密码 | 数字，最大127位 |
| **\[ringstrategy\]** | String | 响铃策略 | 可选项：Ring All, Least Recent, Fewest Calls, Random, Rrmemory, Linear |
| **\[failoveraction\]** | String | 呼入失败目的地 | 可选项：Hang up, Extension, Voicemail, IVR, Ring Group, Queue, Conference, Fax to Email, Dial by Name |
| **\[failoverdest\]** | String | 呼入失败目的地 |  |
| **\[agents\]** | string | 固定座席 | 1000，1001 |
| **\[agenttimeout\]** | Int | 坐席响铃时间 | 范围：10, 20, 30, 40, 50 |
| **\[wrapuptime\]** | Int | 休息时间 | 范围：10, 20, 30, 40, 50 |
| **\[ringinuse\]** | String | 使用中振铃 | On：开启 off：关闭 |
| **\[retry\]** | Int | 重试间隔时间 | 范围：10, 20, 30, 40, 50 |
| **\[maxwaittime\]** | Int | 最大等待时间 | 范围：300, 600, 900, 1200, 1800 |
| **\[joinempty\]** | String | 无座席时允许呼入 | On：开启 off：关闭 |
| **\[leavewhenempty\]** | String | 无座席时结束等待 | On：开启 off：关闭 |
| **\[announcepos\]** | String | 公告当前位置 | On：开启 off：关闭 |
| **\[announcefreq\]** | String | 用户公告频率 | 范围：0, 15, 30, 45, 60, 120, 180, 240, 300, 600, 1200 |
| **\[announceholdtime\]** | Int | 公告等待时间 | On：开启 off：关闭 |
| **\[userannouncefreq\]** | Int | 系统公告频率 | 范围：0, 15, 30, 45, 60, 120, 180, 240, 300, 600, 1200 |
| **\[breakoutkey\]** | String | 按键DTMF | 范围：None, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, \*, \# |
| **\[breakoutaction\]** | String | 按键目标 | 可选项：Hang up, Extension, Voicemail, IVR, Ring Group, Queue, Conference, Fax to Email, Dial by Name |
| **\[breakoutdest\]** | String | 按键目标的最终目的地 |  |

**响应示例：**

{"status":"Success"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| **&lt;status&gt;** | String | IVR设置结果 | Success或者Failed |

**可能出现的错误码：**10013，10019，30001

;

