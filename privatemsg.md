#1、通过私信分享课程的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/chat/with154/share205?uid=5&t=89D8FA86DDE18B59&client=1

URL 'http://192.168.100.48:1092/v3/msg/chat/with{fid}/share{cid}?uid=5&t=89D8FA86DDE18B59&client=1'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 用户ID
+ **课程ID**: `fid` 好友ID
+ **课程ID**: `cid` 课程ID
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
如果成功，返回私信ID

******

#2、取我的私信分组列表信息#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/chat/group?uid=5&p=1&from=1375601464938&t=89D8FA86DDE18B59

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **时间戳**：`from` 
+ **分页**: `p` (从1开始)

相关说明
===
from 上一次取该列表的时间，用于判断分组私信是否有更新

******

#3、取与某个好友的私信列表#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/chat/with154/page?uid=5&p=1&t=89D8FA86DDE18B59

URL 'http://192.168.100.48:1092/v3/msg/chat/with{fuid}/page?uid=5&p=1&t=89D8FA86DDE18B59'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid`  
+ **分页**: `p`
+ **好友ID**: `fuid`

相关说明
===
with154 154为对方ID

******

#4、发送文本私信#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/chat/with7/sendtext?uid=5&t=89D8FA86DDE18B59&content=hello

URL 'http://192.168.100.48:1092/v3/msg/chat/with{receiver}/sendtext?uid=5&t=89D8FA86DDE18B59&content=hello'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **加密验证**：`t`  
+ **内容**: `content`
+ **接受者(好友)ID**：`receiver`  

相关说明
===
with154 154为对方ID

******

#5、发送带图片的私信#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/chat/with7/send?uid=5&t=89D8FA86DDE18B59

URL 'http://192.168.100.48:1092/v3/msg/chat/with{receiver}/send?uid=5&t=89D8FA86DDE18B59'

###支持格式 `JSON`

###HTTP请求方式 `POST`

参数说明
====

+ **用户ID**: `uid` 
+ **加密验证**：`t`  
+ **接受者(好友)ID**：`receiver`  

相关说明
===
+ @FormDataParam("file" ) InputStream uploadedInputStream,
+ @FormDataParam("file" ) FormDataContentDisposition fileDetail,
+ @FormDataParam ("content") String content

******

#6、<u>更新的私信为已读（该接口废弃）</u>#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/chat/with154/readed?uid=5&t=89D8FA86DDE18B59&client=1

URL 'http://192.168.100.48:1092/v3/msg/chat/with{fid}/readed?uid=5&t=89D8FA86DDE18B59&client=1'

###支持格式 `JSON`

###HTTP请求方式 `POST`

参数说明
====

+ **用户ID**: `uid` 
+ **接受者(好友)ID**：`fid`
+ **加密验证**：`t`  
+ **客户端类型**：`client` （1，Android； 2，IOS）

相关说明
===
接口执行成功后，返回1

******

#7、删除我与某好友整组的私信#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/chat/with154/group/delete?uid=5&client=1&t=89D8FA86DDE18B59

URL 'http://192.168.100.48:1092/v3/msg/chat//with{fid}/group/delete?uid=5&client=1&t=89D8FA86DDE18B59'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **好友ID**：`fid`
+ **加密验证**：`t`  
+ **客户端类型**：`client` （1，Android； 2，IOS）

相关说明
===
接口执行成功后，返回1

******

#8、删除我与某好友的某一条的私信#

URL
====
[ex] http://192.168.100.48:1092/v3/msg/chat/with154/chat20000/delete?uid=5&client=1&t=89D8FA86DDE18B59

URL 'http://192.168.100.48:1092/v3/msg/chat/with{fid}/chat{cid}/delete?uid=5&client=1&t=89D8FA86DDE18B59'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **好友ID**：`fid`
+ **私信ID**：`cid`
+ **加密验证**：`t`  
+ **客户端类型**：`client` （1，Android； 2，IOS）

相关说明
===
接口执行成功后，返回1

******

