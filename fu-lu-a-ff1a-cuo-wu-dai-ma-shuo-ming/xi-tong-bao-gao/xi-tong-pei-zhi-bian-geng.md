# 系统配置变更

当IPPBX的配置发生变化时，IPPBX会向应用服务器推送该报告，以便于应用服务器及时更新和同步IPPBX的相关配置。

目前只支持报告分机和中继的配置变更，且只报告哪个分机或哪个中继配置有变更，具体变更信息需用户自己去网页查看。

**报告示例：**

{"action":"ConfigChange","type":"trunk","trunkname":"SIP-142","operation":"del"}

**报告参数说明：**

| **参数名称** | **类型** | **参数说明** | **参数值举例** |
| :--- | :--- | :--- | :--- |
| &lt;configchange&gt; | string | 配置变更 | N/A |
| &lt;type&gt; | string | 类型 | trunk,extension |
| &lt;trunkname&gt; | string | 配置有变更的中继名称 | SIP-142 |
| &lt;operation&gt; | string | 操作 | add,del,update |



