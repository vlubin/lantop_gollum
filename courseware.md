#1、课件列表的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/27/coursewares?uid=5&from=0&t=t&client=1

### 'http://192.168.100.48:1092/v3/course/{cid}/coursewares?uid=5&from=0&t=t&client=1'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid`
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`token`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
无

******