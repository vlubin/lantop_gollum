******



#日志-记录用户登录信息#

URL
====
[ex] http://192.168.100.48:1092/v3/trace/login?uid=12&t=token&device=device_number&os=ios7&brand=apple&client=2&version=4

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====
device 手机端设备号
os 手机操作系统版本
brand 手机品牌等信息
client 客户端类型（1 - android学生2 -IOS学生）
version 安装的客户端版本号


相关说明
===
无

******

#日志-下载课件#

URL
====
[ex] http://192.168.100.48:1092/v3/trace/course/1/courseware/2/download?uid=12&t=token&device=device_number

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

相关说明
===
无


******
#日志-打开课件#


URL
====
[ex] http://192.168.100.48:1092/v3/trace/course/1/courseware/2/open?uid=12&t=token&device=device_number

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

相关说明
===
无

******


#日志-课程-作业下载#

URL
====
[ex] http://192.168.100.48:1092/v3/trace/course/1/exam/1/download?uid=5&t=89D8FA86DDE18B59&&device=device_number

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====
+ **课程ID**: `cid` 
+ **考试ID**: `examId` 
+ **用户ID**: `uid` 
+ **Token**: `t` 
+ **设备号**: `device` 

相关说明
===
无

******


