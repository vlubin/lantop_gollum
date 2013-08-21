#1、课件列表的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/27/coursewares?uid=5&from=0&t=t&client=1

### 'http://192.168.100.48:1092/v3/course/{cid}/coursewares?uid=5&from=0&t=t&client=1'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid`
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`token`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明(返回的JSON字段)
===
+ **学习进度**: `courseProgress`  （int类型）
+ **课件类型**: `type`  （1，课件; 2，习题；3，课件+习题）
+ **课件版本**: `version`  （int类型，如果大于本地，那么该课件为更新）
+ **课件习题的得分率**: `scoringAverage`  （如果课件类型为2，或3时需要用到此字段）


******


#2、课件帧列表多媒体数据的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/courseware/1/frames?uid=5&from=0&t=t&client=1

### 'http://192.168.100.48:1092/v3/course/courseware/{cwid}/frames?uid=5&from=0&t=t&client=1'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课件ID**: `cwid`
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`token`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明(返回的JSON字段)
===
+ **资源的路径**: `resourceUrl`  （当资源类型为MP4，或MP3时，作为下载资源的路径）
+ **MP3资源的路径**: `audioUrl`  （如果资源类型为MP3时，作为下载资源的路径，此时背景图的路径为：resourceUrl）
+ **缩略图**: `thumbimgUrl`  （各资源的缩略图）
+ **资源类型**: `resourceType`  （资源类型：ZIP(不作为帧，如果有，需要下载)，JPG，MP3，MP3+JPG，MP4）
+ **视频资源的图片**: `videoImgUrl`  （视频播放之前的背景图）
+ **资源大小**: `size`  （资源大小，但不是准确的）
+ **课件帧顺序**: `serialNumber`  （升序排序，如果为-1的话，那么为图片压缩包，不作为帧）

******