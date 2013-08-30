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

#3、课件习题列表的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/1/courseware/26/exercise/list?uid=5&from=0&t=t&client=1

### 'http://192.168.100.48:1092/v3/course/{cid}/courseware/{cwid}/exercise/list?uid=5&from=0&t=t&client=1'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid`
+ **课件ID**: `cwid`
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明(返回的JSON字段)
===
+ **课件ID**: `coursewareId`
+ **课件名**: `courseName`
+ **课件版本**: `version`
+ **习题列表**: `exercises`


习题列表的JSON字段:
===
+ **习题ID**: `id`  
+ **习题标题**: `title`  
+ **习题类型**: `type`  （int，习题类型：0，单选；1，多选；2，是非判断题）
+ **视频资源的图片**: `score`  （视频播放之前的背景图）
+ **答题解析**: `explanation`  （答题解析）
+ **课件帧顺序**: `addition`  （答题选项：id, 顺序； description， 答题选项内容；如果为是非题的话，那么该字段为null）
+ **课件帧顺序**: `answer`  （id:答案顺序，answer：Y，正确答案； N，错误答案；如果为是非题的话，那么该字段为取值范围为Y或N）

******


#4、提交课件习题并返回的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/1/courseware/26/exercise/submit?uid=5&type=2&correct=4&score=35&t=t&client=1

### 'http://192.168.100.48:1092/v3/course/{cid}/courseware/{cwid}/exercise/submit?uid=5&type=1&correct=4&score=35&t=t&client=1'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid`
+ **课件ID**: `cwid`
+ **课件类型**: `type` (1，多媒体；2，习题；3，多媒体+习题)
+ **正确答题数**: `correct`   （int）
+ **答题得分**: `score`   （int, 习题得分）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明(返回的JSON字段)
===
+ **课件ID**: `id`  
+ **课件习题数**: `exerciseCount`  
+ **正确答题数**: `correctCount` 
+ **本次答题得分率**: `scoringAverage`  （int，百分比）
+ **上一组习题的课件ID**: `previousCoursewareId`  （视频播放之前的背景图）
+ **下一组习题的课件ID**: `nextCoursewareId`  （答题解析）
+ **参入答题的好友**: `friends`  （答题选项：id, 顺序； description， 答题选项内容；如果为是非题的话，那么该字段为null）

******


#5、查看课件习题答题结果的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/654/courseware/773/exercise/result?uid=5&t=t&client=1

### 'http://192.168.100.48:1092/v3/course/{cid}/courseware/{cwid}/exercise/result?uid=5&t=t&client=1'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid`
+ **课件ID**: `cwid`
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明(返回的JSON字段)
===
返回的JSON字段与提交课件系统的接口返回字段相同，字段含义相同

******