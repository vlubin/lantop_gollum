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
+ **关键字**: `key`   （搜索条件：姓名，模糊查询，当为NULL或""时，无结果集）
+ **分页页码**: `p` 页码从1开始
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ **搜索范围**：`ydxy_user.enableWkt=1, 搜索关键字：ydxy_user.name`

****

#10、好友邀请：获取同班同学列表#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/classmate/list?uid=5&p=1&t=89D8FA86DDE18B59&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 我的ID
+ **分页页码**: `p` 页码从1开始
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明(JSON View描述)
===
+ **状态**：`status` (-1,不接受好友请求[直接弹出提示]； 0，邀请[显示邀请的按钮，点击调用下面邀请接口]；1，添加[调用添加好友请求的接口]；2，好友[显示已经添加的TextView])

****

#11、好友邀请：获取同校师生列表#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/schoolmate/list?uid=5&p=1&t=89D8FA86DDE18B59&client=1&search=张三

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 我的ID
+ **分页页码**: `p` 页码从1开始
+ **加密验证**：`t`  
+ **搜索姓名**：`search`  (搜索好友的姓名，模糊匹配)
+ **客户端类型**: `client`  （1，Android; 2，iOS）

JSON View描述
===
+ **状态**：`status` (-1,不接受好友请求[显示添加按钮，直接弹出提示]； 0，邀请[显示邀请的按钮，点击调用下面邀请接口]；1，添加[显示添加按钮，调用添加好友请求的接口]；2，好友[显示已经添加的TextView])

相关说明
===
该接口返回的数据不包含我所属班级的用户

****

#12、提起好友邀请#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/invitation/request?uid=5&receiver=7&t=89D8FA86DDE18B59&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 我的ID
+ **接收者ID**: `receiver` 我邀请的用户的ID
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

JSON View描述
===
+ **短信内容**：`message` (调用该接口后，该字段是通过手机发送到被邀请人的手机上，<b>通过用户自己的手机发出的短信内容</b>)

相关说明
===
只有在邀请的列表中，返回的字段 status=0时才调用该接口。

****

#13、At课程给好友时，返回好友列表 ，以及课程的编辑或创建老师#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/at/list?uid=5&cid=126&t=89D8FA86DDE18B59&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 我的ID
+ **课程ID**: `cid` 课程ID
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

JSON View描述
===
+ **课程编辑老师列表**: `teachers` (课程编辑老师列表)
+ **好友列表**: `friends` (我的好友列表)

****

#14、好友邀请列表中，搜索已经正在使用微课堂的用户并添加为好友#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/invitation/search?uid=5&key=s&p=1&t=89D8FA86DDE18B59&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 我的ID
+ **关键字**: `key`   （搜索条件：姓名，模糊查询，当为NULL或""时，无结果集）
+ **分页页码**: `p` 页码从1开始
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ **状态**：`status` （1，非好友，显示添加按钮；2，已是好友，显示已添加）


****
