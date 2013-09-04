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

#话题-GET集合#


#6、取跟我相关的话题（最新话题）列表#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/topics?uid=5&t=&p=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **页码**: `p`

相关说明
===
p=1 页码
isMyCourse （0否1是），用于判断课程点击进入课程介绍页还是课程的话题列表页
下同
******


#7、取公开的话题（发掘话题）列表#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/topics/all?uid=12&t=&p=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **页码**: `p`
+ **加密验证**：`t`  

相关说明
===
无

******
#8、取课程相关的话题列表（话题 - 课程）#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/topics/course/2?uid=5&t=&p=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **页码**: `p`
+ **加密验证**：`t`  

相关说明
===
+ course/2? 2-课程ID

******


#9、取用户创建的话题列表（用户信息 - 话题）#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/topics/user/154?uid=12&t=&p=38

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **页码**: `p`
+ **加密验证**：`t`  

相关说明
===
+ user/5? 5-用户ID

******

#10、取话题的回复列表#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/topic/11050/replies?uid=12&t=&p=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **页码**: `p`
+ **加密验证**：`t`  

相关说明
===
+ topic/11050 11050-话题ID

******

#11、消息 - 话题- 回复我的#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/topic/me/replies?uid=12&t=&p=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **页码**: `p`
+ **加密验证**：`t`  

相关说明
===

******

#12、消息 - 话题- @我的#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/topic/me/at?uid=154&t=&p=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **页码**: `p`
+ **加密验证**：`t`  

相关说明
===

******


#13、话题和回复列表（用户消息 - 回复我的和at我的 -进入单个话题）#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/topic/11994?uid=1&t=&p=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **页码**: `p`
+ **加密验证**：`t`  

相关说明
===

******
#14、取课程相关的话题列表包含话题总数（话题 -课程）#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/topics/ios/course/2?uid=5&t=89D8FA86DDE18B59&p=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **页码**: `p`
+ **加密验证**：`t`  

相关说明
===
+ course/2? 2-课程ID

android 已经调用#8，IOS用此接口，android可以考虑转换用该接口，放弃#8
******


******
#15、新增话题（带图片）#

URL
====
[ex] http://192.168.100.48:1092/v3/sns/act/topic/add/withpic?uid=12&t=

###支持格式 `JSON`

###HTTP请求方式 `POST`

参数说明
====

+ **用户ID**: `uid` 
+ **页码**: `p`
+ **加密验证**：`t`  

@FormDataParam("uid") int userId, @FormDataParam("t") String token,
			@FormDataParam("file") InputStream uploadedInputStream,
			@FormDataParam("file") FormDataContentDisposition fileDetail,
			@FormDataParam("course") int courseId,
			@FormDataParam("content") String content);

相关说明
===

******


