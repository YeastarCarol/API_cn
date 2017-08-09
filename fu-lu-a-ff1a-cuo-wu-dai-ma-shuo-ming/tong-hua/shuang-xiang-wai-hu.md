

# 双向外呼

通过本接口可让PBX依次向外发起两路呼叫，并以PBX作为中间点建立连接，从而实现两个外部电话之间建立通话。

**操作**

先拨打主叫，主叫摘机后听到回铃音，然后再呼被叫，被叫响铃，被叫摘机后双方建立通话。

**条件**

1.需借助一个分机的呼出路由权限呼出

2.至少要有两条空闲可用的中继资源；

3.两路都需要匹配呼出路由呼出

**请求方式：**POST

**请求地址：**https://192.168.5.150:8088/api/v1.0.0/outbound/dial\_outbound?token=7d20390952e15eb72b0a1df7172de65c

**请求示例：**

{"caller": "1002","outto": "41000","fromext": "1000"}

**请求参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| **&lt;caller&gt;** | String | 呼出的外线号码\(匹配呼出规则\) | 1002 |
| **&lt;outto&gt;** | String | 外线号码\(匹配呼出规则\) | 41000 |
| **&lt;fromext&gt;** | String | 采用哪个分机的权限 | 1000 |

**响应示例：**

{"status":"Success","callid":"1495701633.295"}

**响应参数说明：**

| 参数名称 | 类型 | 参数说明 | 参数值举例 |
| :--- | :--- | :--- | :--- |
| **&lt;status&gt;** | String | 双向外呼结果 | Success或者Failed |
| **&lt;callid&gt;** | String | 通话唯一标识符 | 1495701633.295 |

**可能出现的错误码：**10004，10006，10012，30001

 s
