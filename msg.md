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
[ex] http://192.168.100.48:1092/v3/msg/notice/20119/read?uid=12&t=&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **消息ID**: /notice/**20119**/
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

#消息-私信#
#5、取我的私信分组列表信息#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/chat/group?uid=12&p=1&from=1375601464938

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **时间戳**：`from`  
+ **分页**: `p`

相关说明
===
from 上一次取该列表的时间，用于判断分组私信是否有更新

******

#6、取与某个好友的私信列表#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/chat/with154/page?uid=12&p=2

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid`  
+ **分页**: `p`

相关说明
===
with154 154为对方ID

******

#7、发送文本私信#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/chat/with154/sendtext?uid=12&t=&content=hello

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **加密验证**：`t`  
+ **内容**: `content`

相关说明
===
with154 154为对方ID

******

#8、发送带图片的私信#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/chat/with154/send?uid=12&t=

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **加密验证**：`t`  

相关说明
===
+ @FormDataParam("file" ) InputStream uploadedInputStream,
+ @FormDataParam("file" ) FormDataContentDisposition fileDetail,
+ @FormDataParam ("content") String content

******

#9、各种消息是否有新内容(time传0不计算）#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/hasnewuid=12&t=&notice=1375608440613&
topic=1375608440613&chat=1375608440613&friend=1375608440613
###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====
？？？

相关说明
===
+ @param fromTimestampOfNotice
+ @param fromTimestampOfTopic
+ @param fromTimestampOfChat
+ @param fromTimestampOfFriendRequest

******


