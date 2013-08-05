#校方通知#

#1、取跟我相关的校方通知#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/notice/page?uid=12&t=&p=198

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **加密验证**：`t`  
+ **分页**: `p`

相关说明
===
无

******

#2、设置通知已读(签收)#

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
+ 20119 - 消息ID

******

#3、取投票数据#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/notice/19758/vote/get?uid=12&t=

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **加密验证**：`token`  

相关说明
===
+ 19758 - 消息ID

******

#4、提交投票结果#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/notice/19758/vote/2988/submit?uid=12&t=&option=A

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **加密验证**：`t`  
+ **投票结果**: `option`

相关说明
===
+ 19758 - 消息ID
+ 2988 - 投票ID（对应取投票数据接口的voteId字段）
+ option=A - 投票的选项（对应取投票数据接口的options.value字段）

******


