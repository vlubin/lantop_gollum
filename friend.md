#1、获取我的好友列表#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/list?uid=5&from=0&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`token`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
无

****


#2、好友的好友列表#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/other/list?fid=5&p=1&from=0&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **好友ID**: `fid` 
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）
+ **分页页码**: `p`  （从1开始） 

相关说明
===
无

****

#3、推荐的好友列表#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/recommend/list?uid=5&p=3&from=0&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `fid` 
+ **分页页码**: `p` 
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ 该接口用于推荐的好友列表，每页显示8个，分页显示