#1、提交异常信息#

URL
====
[ex] http://192.168.100.48:1092/v3/exceptioin/client/log/save

###支持格式 `JSON`

###HTTP请求方式 `POST`

参数说明
====

+ **用户ID**: `uid` 
+ **Token**: `t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）
+ **客户端自定义异常类型**: `eventtype`  （String，类型）
+ **客户端操作系统版本呢**: `osversion`  （String，类型）
+ **异常类名**: `classname`  （String，类型）
+ **异常消息**: `message` 

相关说明（参数说明）
===
**异常消息**: `message` （该参数请详尽的，尽可能的提交完成的异常堆栈；如果是Android客户端，详尽的收集硬件设备信息并提交）

******
