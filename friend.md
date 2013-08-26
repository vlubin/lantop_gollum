#1、获取我的好友列表#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/list?uid=5&from=0&t=t&client=1

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
[ex] http://192.168.100.48:1092/v3/friend/other/list?uid=5&fid=5&p=1&from=0&t=t&client=1

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
无

****

#3、推荐的好友列表#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/recommend/list?uid=5&p=3&from=0&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `fid` 
+ **分页页码**: `p` 
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ 该接口用于推荐的好友列表，每页显示8个，分页显示



****


#4、添加好友发起请求#

URL
====
[ex] http://192.168.100.48:1092/v3/friend/relation/5/7/add?from=0&t=t&client=1

### 接口参数 'http://192.168.100.48:1092/v3/friend/relation/{uid}/{fid}/add?from=0&t=t&client=1'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **发起人ID**: `uid` 
+ **目标好友ID**: `fid` 
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
[ex] http://192.168.100.48:1092/v3/friend/relation/7/5/agree?from=0&t=t&client=1

### 接口参数 'http://192.168.100.48:1092/v3/friend/relation/{uid}/{fid}/agree?from=0&t=t&client=1'

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
[ex] http://192.168.100.48:1092/v3/friend/relation/5/7/refuse?from=0&t=t&client=1

### 接口参数 'http://192.168.100.48:1092/v3/friend/relation/{uid}/{fid}/refuse?from=0&t=t&client=1'

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
[ex] http://192.168.100.48:1092/v3/friend/relation/5/7/delete?from=0&t=t&client=1

### 接口参数 'http://192.168.100.48:1092/v3/friend/relation/{uid}/{fid}/delete?from=0&t=t&client=1'

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
[ex] http://192.168.100.48:1092/v3/friend/request/list?uid=5&p=1&from=0&t=t&client=1

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
