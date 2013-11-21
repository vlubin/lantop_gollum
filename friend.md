#1、获取我的好友列表#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/list?uid=5&from=0&t=89D8FA86DDE18B59&client=1

###支持格式 `JSON`

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

****


#2、好友的好友列表#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/other/list?uid=5&fid=5&p=1&from=0&t=89D8FA86DDE18B59&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid`
+ **好友ID**: `fid` 
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）
+ **分页页码**: `p`  （从1开始） 

相关说明
===
查看别人的好友，给全量(200条分页)，否则好友列表右侧的字母排序无意义

****

#3、推荐的好友列表(学生和教师)#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/recommend/list?uid=5&from=0&t=89D8FA86DDE18B59&client=1&type=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `fid` 
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）
+ **用户类型**: `type`  （1，为教师，不传该参数时为学生）

相关说明
===
随机返回8个推荐的学生，8个推荐的教师



****


#4、添加好友发起请求#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/relation/add?uid=5&fid=1,2,3,4,6,7&from=0&t=89D8FA86DDE18B59&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **发起人ID**: `uid` 
+ **目标好友ID**: `fid` (多个好友ID：使用半角的,隔开)
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ 添加好友，返回status=0, 成功，返回-999操作失败
+ 该接口返回相应的提示信息



****


#5、同意好友的请求#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/relation/5/agree?uid=7&from=0&t=89D8FA86DDE18B59&client=1

### 接口参数 'http://192.168.100.48:1092/v3/friend/relation/{fid}/agree?uid=7&from=0&t=89D8FA86DDE18B59&client=1'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 我的ID
+ **好友ID**: `fid` 我同意的发起人ID
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ 同意好友的请求，返回status=1, 成功，返回-999操作失败
+ 该接口返回相应的提示信息



****


#6、拒绝好友的请求#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/relation/7/refuse?uid=5&from=0&t=89D8FA86DDE18B59&client=1

### 接口参数 'http://192.168.100.48:1092/v3/friend/relation/{fid}/refuse?uid=5from=0&t=89D8FA86DDE18B59&client=1'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 我的ID
+ **好友ID**: `fid` 我拒绝的发起人ID
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ 拒绝好友的请求，返回status=3, 成功，返回-999操作失败
+ 该接口返回相应的提示信息



****


#7、删除好友#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/relation/7/delete?uid=5&from=0&t=89D8FA86DDE18B59&client=1

### 接口参数 'http://192.168.100.48:1092/v3/friend/relation/{fid}/delete?uid=5&from=0&t=89D8FA86DDE18B59&client=1'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 我的ID
+ **好友ID**: `fid` 我要删除的好友的ID
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ 删除，返回status=5, 成功，返回-999操作失败
+ 该接口返回相应的提示信息

****


#8、获取好友发送添加请求列表#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/request/list?uid=5&p=1&from=0&t=89D8FA86DDE18B59&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 我的ID
+ **分页页码**: `p` 页码从1开始
+ **时间戳**: `from`   （Timestamp类型的，如果本地时间戳为null，传0）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ 传入真实时间戳

****

#9、搜索已经使用客户端的用户（好友）列表#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/search?uid=5&key=s&p=1&t=89D8FA86DDE18B59&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 我的ID
+ **关键字**: `key`   （搜索条件，模糊查询，当为NULL或""时，无结果集）
+ **分页页码**: `p` 页码从1开始
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ **搜索范围**：`ydxy_user.enableWkt=1,ydxy_user.name`

****
