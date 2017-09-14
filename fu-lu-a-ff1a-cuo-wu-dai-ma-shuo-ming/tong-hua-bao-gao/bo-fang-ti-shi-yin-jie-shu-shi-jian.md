# 播放提示音结束事件

该事件用于报告给分机及外线播放提示音结束时的事件。

**报告示例：**

**给分机播放提示音结束事件：**

{"action":"PlayPromptEnd","callid":"1495780325.384","ext":{"extid":"1002"},"prompt":"appletest"}

**给外线播放提示音结束事件：**

{"action":"PlayPromptEnd","callid":"1505352996.281","outbound":{"trunkname":"Apple\_test"},"prompt":"appletest"}

**报告参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;action&gt; | string | 播放提示音结束事件 | PlayPromptEnd |
| &lt;promtp&gt; | string | 播放的提示音文件 | appletest |
| &lt;callid&gt; | string | 该通通话的id | 1495780325.384 |
| \[outbound\] | object | 来电或去电 |  |
| &lt;trunkname&gt; | string | 通过的中继名称 | sip-142 |



