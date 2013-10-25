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
返回对象的status : 0:未读 1:已读

******

#2、设置通知已读(签收)#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/notice/20119/read?uid=12&t=&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **消息ID**: 例中的**20119**
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

#5、各种消息是否有新内容(time传0不计算）#

URL
====
[ex] 

各种消息是否有新内容(time传0不计算）
http://192.168.100.48:1092/v3/msg/hasnew?uid=12&t=&notic=1375608440613&topic=1375608440613&chat=1375608440613&friend=1375608440613&version=4

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====
notice 是否有新通知（底部菜单）
topic 我的课程小组里是否有新话题（底部菜单）
topic4me 是否有新的跟我相关的话题，回复我的或AT我的（消息-话题）
chat 是否有新私信
friendRequest 是否有新好友请求
course 是否有新课程
release 是否有新版本

相关说明
===


******
