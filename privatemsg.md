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

#3、取与某个好友的私信列表#

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

#4、发送文本私信#

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

#5、发送带图片的私信#

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