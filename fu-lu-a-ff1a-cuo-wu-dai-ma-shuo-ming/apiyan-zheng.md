# API验证

## 登录

S系列IPPBX API采用用户名和密码的方式验证，只有用户名和密码验证通过的应用服务器，API才会处理其发送的请求。

注：密码需用户自己使用MD5加密之后的32位小写密码进行验证。如果密码连续错误五次，则该第三方应用的IP将会被锁10分钟。

请求方式：POST

请求地址：[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/login){version}[/login](https://192.168.5.150:8088/api/v1.0.0/login)

请求示例：

{"username": "api","password": "2d7257a528679d01a19c70e3fa773620","port": "8260"}

请求参数说明：

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| &lt;username&gt; | string | 在IPPBX 二次开发接口界面设置的用户名。 | api |
| &lt;password&gt; | string | 在IPPBX二次开发接口界面设置的密码。 | MD5加密之后的32位小写密码 |
| &lt;port&gt; | string | 端口号，此端口号为第三方应用用于监听API发送的事件报告的端口号。 | 0&lt;port&lt;65536 |
| \[url\] | string | API应用方的URL。跟在IP地址后面用来指定API向第三方应用发送事件报告的具体路径。如果不带此参数，则默认向第三方应用的IP地址发送事件报告。 |  |

响应示例：

{"status":"Success","token":"48a7d7481a5355aa4fb5dc285edeb40e"}

响应参数说明：

| 参数名称 | 类型 | 参数说明 | 参数值举例&lt;status&gt; |
| :--- | :--- | :--- | :--- |
| &lt;status&gt; | string | 请求状态 | Success，Failure |
| &lt;token&gt; | string | 调用接口凭证，所有的API请求都需用到该token。 | 1ec8bde364f8e37c0dd14f476fba114c |

注：所有的API请求都需要带上登录返回的token，且该token有效时长为30分钟，30分钟内如果API和第三方应用没有任何事件交互（如：第三方应用发送API请求），则该token将被IPPBX系统清除。可通过心跳包接口延长token的有效时长，每发送一次心跳包可使token的有效时长延长30分钟。

可能出现的错误码：20003

## 心跳包

当连接IPPBX的第三方应用的IP地址、监听端口或者URL有变更的时候，可通过API的心跳包接口对IP, Port, URL进行更新。同时当第三方应用和API没有事件交互的时候，可利用此接口定期发送请求从而更新token的有效时长，避免token在1800秒超时后被清除，造成事件不会上报以及请求失败。

注：发送一次心跳包请求可使token的有效时长延长1800秒。

请求方式：POST

请求地址：[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/heartbeat?token=48a7d7481a5355aa4fb5dc285edeb40e){version}[/heartbeat?token=48a7d7481a5355aa4fb5dc285edeb40e](https://192.168.5.150:8088/api/v1.0.0/heartbeat?token=48a7d7481a5355aa4fb5dc285edeb40e)

请求示例：

{"ipaddr": "192.168.5.150","port": "8260","url":"1112121212"}

请求参数说明：

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| \[ipaddr\] | string | 第三方应用变更后的IP地址。 | 192.168.5.150 |
| \[port\] | string | 第三方应用变更后的监听端口。 | 0&lt;port&lt;65536 |
| \[url\] | string | 第三方应用变更后的URL。 |  |

响应示例：

{"status":"Success"}

## 退出登录

注：请求示例中的token为登录时所返回的token。

请求方式：POST

请求示例：

[https://192.168.5.150:8088/api/](https://192.168.5.150:8088/api/v1.0.0/logout?token=48a7d7481a5355aa4fb5dc285edeb40e){version}[/logout?token=48a7d7481a5355aa4fb5dc285edeb40e](https://192.168.5.150:8088/api/v1.0.0/logout?token=48a7d7481a5355aa4fb5dc285edeb40e)

响应示例：

{"status":"Success"}

