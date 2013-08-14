#1、更新密码#

URL
====
[ex] http://192.168.100.48:1092/v3/user/password/update?uid=5&password=5f560d46fc03bd4f9f8ead5e0bc65ec9&newpassword=e10adc3949ba59abbe56e057f20f883e&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **原密码**: `password`
+ **新密码**: `newpassword`   （Timestamp类型的）
+ **加密验证**：`token`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
无

******

#2、根据重置码重置密码#

URL
====
[ex] http://192.168.100.48:1092/v3/user/password/reset?loginname=18616568180&password=5f560d46fc03bd4f9f8ead5e0bc65ec9&code=123456&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **登录名**: `loginname` （手机号码或用户名）
+ **新密码**: `password`
+ **重置码**: `code`   （Timestamp类型的）
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
无

******

#3、发送重置码#

URL
====
[ex] http://192.168.100.48:1092/v3/user/activation/sendcode?phone=18616568180&type=2&ip=192.168.1.15 

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **手机号码**: `phone` 
+ **类型**: `type`	（1，发送激活码；2，遗忘密码发送重置码）
+ **时间戳**: `ip`   （客户端的IP）

相关说明
===
无

******