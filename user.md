#1、我的个人主页接口#

URL
====
[ex] http://192.168.100.48:1092/v3/user/my/home?uid=5&from=0&t=t&client=1

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


#2、好友(以及查看好友的好友)的个人主页接口#

URL
====
[ex] http://192.168.100.48:1092/v3/user/friend/home?uid=5&fid=12&from=0&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **好友ID**: `fid` 
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
无

******

#3、用户登录#

URL
====
[ex] http://192.168.100.48:1092/v3/user/login?loginname=18616568180&password=e10adc3949ba59abbe56e057f20f883e&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **登录名**: `loginname` (用户的手机号码)
+ **密码**: `password`   （MD5加密）
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ 注意，该接口规则：先查询用户名，如果存在记录则使用，否则查询手机号码。
+ 老师：type == 1，T
+ 学生：type == 2，S

******

#4、LandingPage#

URL
====
[ex] http://192.168.100.48:1092/v3/user/config/get?uid=5&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **Token**: `t`   
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ 该接口在Landing时，取用户的配置接口，以及Landing Image URL等。

******

#5、我的隐私设置#

URL
====
[ex] http://192.168.100.48:1092/v3/user/privacy/setting?uid=5&dp=2&dt=2&dm=2&t=t&client=1

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **个人资料**: `dp` (是否在个人主页上公开个人资料：0， 不公开； 1， 全部公开； 2，好友可见)
+ **我的动态**: `dt` (是否显示我的动态：0， 不公开； 1， 全部公开； 2，好友可见)
+ **默认的主菜单**: `dm` (进入应用时，默认的主菜单：0，课程:我的课程小组； 1，课程:课程小组； 2，最新话题)
+ **Token**: `t`   
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
无

******

#6、用户反馈建议#

URL
====
[ex] http://192.168.100.48:1092/v3/user/5/feedback?content=abcdefg&t=t&client=1

### `http://192.168.100.48:1092/v3/user/{uid}/feedback?content=abcdefg&t=t&client=1`

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **意见反馈内容**: `content` (是否在个人主页上公开个人资料：0， 不公开； 1， 全部公开； 2，好友可见)
+ **Token**: `t`   
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
无

******


#7、更新个人设置#

URL
====
[ex] http://localhost:8082/v3/user/profile/update

###支持格式 `JSON`

###HTTP请求方式 `POST`

参数说明
====

+ **用户ID**: `uid` 
+ **意见反馈内容**: `gender` (性别：0未知；1男；2女)
+ **意见反馈内容**: `birthday` (时间格式：yyyy-MM-dd)
+ **城市代码**: `city`
+ **Token**: `t`   
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ 更新用户生日、所在城市、性别，以及用户ICON（两个ICON, icon:100 * 100像素的，iconLarge:130*130像素）
+ POST数据类型：multipart/form-data

******