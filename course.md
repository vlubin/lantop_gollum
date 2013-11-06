#1、查看课程详细资料JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/list/infos?uid=5&cid=28&from=0&t=89D8FA86DDE18B59&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid`
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明(部分JSON字段含义)
===
+ **是否已经选择**: `selected` (是否添加到我的课程小组中：-1，不可添加，不可删除；1，已添加；0，未添加)
+ **课程开放类型**: `openType` (0，必修课；1，授权课；2，公开课)
+ **是否能评分**: `canCommentStar` (0，否；1，可以)

******

#2、课程分类列表接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/category/list?uid=5&from=0&t=89D8FA86DDE18B59&client=1

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

#3、获取我已经添加到我课程小组中的课程接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/myselected/list?uid=5&from=0&t=89D8FA86DDE18B59&client=1&search=英语

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）
+ **搜索关键字**: `search`  （按课程名搜索，如果为null，取全部）

相关说明
===
无

******

#4、将课程添加到我的课程小组的接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/list/add?uid=5&cid=28&from=0&t=89D8FA86DDE18B59&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid`
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
返回1成功，否则失败

******

#5、将课程从我已经添加的小组中删除的接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/list/delete?uid=5&cid=28&from=0&t=89D8FA86DDE18B59&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid`
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
返回1成功，否则失败

******

#6、课程首页的推荐课程/活动列表#

URL
====
[ex] http://192.168.100.48:1092/v3/course/recommend

###支持格式 `JSON`

###HTTP请求方式 `GET`

相关说明
===
type 1课程 2活动

******

#7、给课程评分#

URL
====
[ex] http://192.168.100.48:1092/v3/course/comment?uid=5&t=89D8FA86DDE18B59&course=1&star=1


###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `course`
+ **加密验证**：`t` 
+ **星级**： `star`

相关说明
===
star 5*

******

#8、分享课程给我的好友#

URL
====
[ex] http://192.168.100.48:1092/v3/course/share?uid=1&t=1&course=1&receiver=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `course`
+ **加密验证**：`t`  
+ **?**：`receiver`  

相关说明
===
无

******

#9、课程小组全部公开课列表#

URL
====
[ex] http://192.168.100.48:1092/v3/course/open/list/c0?uid=5&t=89D8FA86DDE18B59&p=1&order=0&client=1&search=英语&open=0

### URL格式 'http://192.168.100.48:1092/v3/course/open/list/c{category}?uid=5&t=89D8FA86DDE18B59&p=1&order=0&client=1'&search=英语

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程分类ID**: `category` （如果为0，取全部）
+ **加密验证**：`t`  
+ **分页页码**：`p` ，从1开始 
+ **排序**：`order` （0按课程创建时间排序；1，最多下载；2，最多关注；3，最高评分 ）
+ **客户端类型**: `client`  （1，Android; 2，iOS）
+ **课程名搜索**: `search`  （为null时，分页列表所有，否则按照参数指定的内容检索）
+ **搜索公开课类型**: `open`  （0，默认，所有；1，授权课；2，完全公开课）
相关说明
===
无

******


#10、好友的课程小组#

URL
====
[ex] http://192.168.100.48:1092/v3/course/other/list?uid=5&fid=5&p=1&from=0&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **好友ID**: `fid` 
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **分页页码**：`p` ，从1开始 
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
无

******


#11、课程成员(成员排行)#

URL
====
[ex] http://192.168.100.48:1092/v3/course/ranking/list?uid=5&cid=2&p=1&from=0&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid` 
+ **页码**: `p`        （从1开始）
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t` 
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
无

******


#12、有更新的课程ID列表#

URL
====
[ex] http://192.168.100.48:1092/v3/course/updates?uid=5&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **加密验证**：`t` 
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
返回的是需要显示两点的课程的ID列表

******


#13、有更新的课程ID列表#

URL
====
[ex] http://192.168.100.48:1092/v3/course/27/update?uid=5&t=t&client=1

http://192.168.100.48:1092/v3/course/{cid}/update?uid=5&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid` 
+ **加密验证**：`t` 
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ **考试Tab上是否要显示亮点**: `examination`  (0, 没有更新，不显示，1，有更新显示)
+ **作业Tab上是否要显示亮点**: `homework` (0, 没有更新，不显示，1，有更新显示)
+ **课件Tab上是否要显示亮点**: `courseware` (0, 没有更新，不显示，1，有更新显示)

******