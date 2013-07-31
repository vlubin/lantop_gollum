#1、我的个人主页接口#

URL
====
[ex] http://192.168.100.48:1092/v3/user/my/home?uid=5&from=0&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
无

******


#2、好友(以及查看好友的好友)的个人主页接口#

URL
====
[ex] http://192.168.100.48:1092/v3/user/friend/home?uid=5&fid=12&from=0&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **好友ID**: `fid` 
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
无

******

#3、用户登录#

URL
====
[ex] http://192.168.100.48:1092/v3/user/login?loginname=18616568180&password=e10adc3949ba59abbe56e057f20f883e&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **登录名**: `loginname` (用户的手机号码)
+ **密码**: `password`   （MD5加密）
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
注意，该接口规则：先查询用户名，如果存在记录则使用，否则查询手机号码。
老师：type == 1，T
学生：type == 2，S

******