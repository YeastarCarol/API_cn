# 配置单个队列

通过本接口可对单个队列进行配置。

**请求方式：**POST

**请求地址：**[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/queue/update?token=7d20390952e15eb72b0a1df7172de65c){version}[/queue/update?token=7d20390952e15eb72b0a1df7172de65c](https://192.168.5.150:8088/api/v1.0.0/queue/update?token=7d20390952e15eb72b0a1df7172de65c)

**请求示例：**

{"queueid": "6701","queuenumber":"6701"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;queueid&gt; | int | 请求时的队列号码 | 6200 |
| \[queuenumber\] | int | 修改后的队列号码 | 6200 |
| \[queuename\] | string | 队列名称 | 限制: ! $ \( \) / \# ; , \[ \] \ "= &lt; &gt;& ' \` ^ % @ { } &#124; （空字符也不行）最大31位，不为空 |
| \[password\] | string | 加入动态坐席的密码 | 数字，最大127位 |
| \[ringstrategy\] | string | 响铃策略 | 可选项：Ring All, Least Recent, Fewest Calls, Random, Rrmemory, Linear |
| \[failoveraction\] | string | 呼入失败目的地 | 可选项：Hang up, Extension, Voicemail, IVR, Ring Group, Queue, Conference, Fax to Email, Dial by Name |
| \[failoverdest\] | string | 呼入失败目的地 |  |
| \[agents\] | string | 固定座席 | 1000，1001 |
| \[agenttimeout\] | int | 坐席响铃时间 | 范围：10, 20, 30, 40, 50 |
| \[wrapuptime\] | int | 休息时间 | 范围：10, 20, 30, 40, 50 |
| \[ringinuse\] | string | 使用中振铃 | on：开启 off：关闭 |
| \[retry\] | int | 重试间隔时间 | 范围：10, 20, 30, 40, 50 |
| \[maxwaittime\] | int | 最大等待时间 | 范围：300, 600, 900, 1200, 1800 |
| \[joinempty\] | string | 无座席时允许呼入 | on：开启 off：关闭 |
| \[leavewhenempty\] | string | 无座席时结束等待 | on：开启 off：关闭 |
| \[announcepos\] | string | 公告当前位置 | on：开启 off：关闭 |
| \[announcefreq\] | string | 用户公告频率 | 范围：0, 15, 30, 45, 60, 120, 180, 240, 300, 600, 1200 |
| \[announceholdtime\] | int | 公告等待时间 | on：开启 off：关闭 |
| \[userannouncefreq\] | int | 系统公告频率 | 范围：0, 15, 30, 45, 60, 120, 180, 240, 300, 600, 1200 |
| \[breakoutkey\] | string | 按键DTMF | 范围：None, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, \*, \# |
| \[breakoutaction\] | string | 按键目标 | 可选项：Hang up, Extension, Voicemail, IVR, Ring Group, Queue, Conference, Fax to Email, Dial by Name |
| \[breakoutdest\] | string | 按键目标的最终目的地 |  |
| \[idannouncement\] | string | 报工号提示音文件名。没有设置则默认不播报。此字段默认为none。注：查询队列的时候此参数为必须返回参数。 | None |
| \[satisfactionsurvey\] | string | 满意度调查需要播放的提示音文件名。没有设置则默认不播报。此字段默认为none。 | None |

**响应示例：**

{"status":"Success"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 队列设置结果 | Success或者Failed |

**可能出现的错误码：**10013，10019，30001

