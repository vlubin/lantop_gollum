#话题-Action(行为)集合#

#1、新增话题#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/act/topic/add?uid=12&t=&course=1&content=hello%20world

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `course`
+ **加密验证**：`t`  
+ **内容**: `content`

相关说明
===
+ 返回插入记录的ID

******


#2、回复主题话题#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/act/topic/11704/reply?uid=154&t=&content=this%20is%20reply

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **加密验证**：`t`  
+ **内容**: `content`

相关说明
===
+ topic/11704 11704主话题ID
+ 返回插入记录的ID

******


#3、回复话题的回复#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/act/topic/11704/11705/reply?uid=154&t=&content=this%20is%20reply%20of%20reply

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **加密验证**：`t`  
+ **内容**: `content`

相关说明
===
+ topic/11704/11705 
+ 11704主题的ID
+ 11705主题的回复的ID
+ 返回插入记录的ID

******


#4、删除话题或回复#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/act/topic/11713/delete?uid=154&t=

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **加密验证**：`t`  

相关说明
===
+ topic/11713 11713-删除的记录ID
+ 返回 1成功 0失败

******
#5、自由讨论举报#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/act/topic/11713/feedback?uid=154&t=&type=2&content=feedback

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **加密验证**：`t`  
+ **内容**: `content`
+ **类型**: `type` (1垃圾广告；2虚假中奖；3淫秽色情；4敏感信息；5不实信息；6泄露他人隐私；7人身攻击；8内容抄袭；9冒充他人；10骚扰他人)

相关说明
===
+ topic/11713 11713-举报的记录ID
+ 返回1成功0失败


******
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