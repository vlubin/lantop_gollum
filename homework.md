#1、查看作业列表的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/1/homework/list?uid=5&from=0&t=89D8FA86DDE18B59&client=1&type=1

###URL `http://192.168.100.48:1092/v3/course/{cid}/homework/list?uid=5&from=0&t=89D8FA86DDE18B59&client=1&type=1`

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **课程ID**: `cid`
+ **用户类型**: `type` (用户类型，1：教师；2或不传该参数时为学生)
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
+ **作业数**: homeworkCount` (int类型, URL参数type=1，为教师的时候，显示作业数)
+ **作业进度**: `homeworkProgress` (int类型，百分比, URL参数type=2或不传的时候(type=0)为学生，显示百分比)
+ **作业列表**: `homeworks` 

作业列表字段如下：
+ **是否完成**: `finished` (0,未完成; 1,已完成)
+ **是否过期**: `overdue` (0,未过期; 1,已过期)

******

#2、作业的习题列表的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/1/homework/1/exercises?uid=5&from=0&t=89D8FA86DDE18B59&client=1

###URL `http://192.168.100.48:1092/v3/course/{cid}/homework/{hwid}/exercises?uid=5&from=0&t=t&client=1`

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid`
+ **作业ID**: `hwid`
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
====
JSON字段描述:
+ **作业信息**: `homework` (JSON Object finished， 0未完成；1，已完成)
+ **作业信息**: `homework` (JSON Object overdue,未过期; 1,已过期，该接口也作为上一组，下一组作业的习题列表，因此通过该字段判断是否显示重新答题的按钮，需要结合finished字段同时使用：1、如果曾完成的作业，没有过期，那么可以反复答题；2、如果曾完成，但已经过期，不能再重新答题；3、如果曾未答题，但已过期，那么仅能答题一次)

+ **作业的习题列表**: `exercises` (JSON Array)
+ **作业习题主键**: `id` (int)
+ **作业主键**: `homeworkId' (int）
+ **习题标题**: `title' (java.lang.String）
+ **习题类型**:'type'（int，习题类型：0，单选；1，多选；2，是非判断题）
+ **本题分数**:'score'（int）
+ **本题解析**:'explanation'（答题解析）
+ **作业的资源**:'resourceUrl'（type=1,表示资源是图片；url是资源的路径;thumbnailUrl是缩略图）
+ **答题选项**:'addition'（答题选项：id, 顺序； description， 答题选项内容；如果为是非题的话，那么该字段为null）
+ **答案**:'answer'（id:答案顺序，answer：Y，正确答案； N，错误答案；如果为是非题的话，那么该字段为取值范围为Y或N）
+ **作业的资源**:'explanationResourceUrl'（type=1,表示资源是图片；url是资源的路径;thumbnailUrl是缩略图）



******


#3、提交作业的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/homework/submit

###支持格式 `JSON`

###HTTP请求方式 `POST`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid`
+ **作业ID**: `hwid`
+ **正确答题数**: `correct`
+ **答题得分**: `score`
+ **答案**: `answer` (JSON 格式的字符串:[{id:1, answer:"1"},{id:2, answer:"1,2,4"},{id:3, answer:"Y"}] )
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
JSON字段描述:
+ **作业ID**:'id'（int）
+ **作业下的习题数**:'exerciseCount'（int）
+ **作业总分**:'totalScore'（int）
+ **正确答题数**:'correctCount'（int）
+ **答题得分**:'score'（int）
+ **实际得分**:'realScore'（int，如果作业过期，会有一定的规则）
+ **得分率**:'scoringAverage'（int，显示百分比）
+ **作业是否完成**: `finished` (int: 0, 未完成; 1, 已完成)
+ **作业是否过期**: `overdue' (int: 0, 未过期; 1, 已过期）
+ **上一个作业主键**: `previousHomeworkId' (int, 如果为0表示，第一个，没有上一组了）
+ **下一个作业主键**: `nextHomeworkId' (int, 如果为0表示最后一个，没有下一组了）
+ **作业提交时间**: `submitTime' (java.lang.String）
+ **参入该作业的我的好友列表**:'friends'

******


#4、查看作业结果的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/1/homework/1/result?uid=5&t=89D8FA86DDE18B59&client=1

###URL `http://192.168.100.48:1092/v3/course/{cid}/homework/{hwid}/result?uid=5&t=t&client=1`

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid`
+ **作业Id**: `hwid` (int, 作业ID)
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
JSON字段描述: 同提交作业的接口相同

******