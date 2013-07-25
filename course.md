#1、查看课程详细资料JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/list/infos?uid=5&cid=28&from=0&t=t&client=1

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

#2、课程分类列表接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/category/list?from=0&t=t&client=1

###支持格式 `Paramater`

###HTTP请求方式 `GET`

参数说明
====

+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`token`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
无

******

#3、获取我已经添加到我课程小组中的课程接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/myselected/list?uid=5&from=0&t=t&client=1

###支持格式 `Paramater`

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

******

#4、将课程添加到我的课程小组的接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/list/add?uid=5&cid=28&from=0&t=t&client=1

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
返回1成功，否则失败

******

#5、将课程从我已经添加的小组中删除的接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/list/delete?uid=5&cid=28&from=0&t=t&client=1

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
返回1成功，否则失败

******

#6、课程首页的推荐课程/活动列表#

URL
====
[ex] http://192.168.100.48:1092/v3/course/recommend

###支持格式 `Paramater`

###HTTP请求方式 `GET`

相关说明
===
type 1课程 2活动

******

#7、给课程评分#

URL
====
[ex] http://192.168.100.48:1092/v3/course/comment?uid=1&t=222&course=1&star=1


###支持格式 `Paramater`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `course`
+ **加密验证**：`token` 
+ **星级**： `star`

相关说明
===
star 5*

******

#8、分享课程给我的好友#

URL
====
[ex] http://192.168.100.48:1092/v3/course/share?uid=1&t=1&course=1&receiver=1

###支持格式 ``

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `course`
+ **加密验证**：`token`  
+ **?**：`receiver`  

相关说明
===
无

******
