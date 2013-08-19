#1、查看作业列表的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/1/homework/list?uid=5&from=0&t=t&client=1

###URL `http://192.168.100.48:1092/v3/course/{cid}/homework/list?uid=5&from=0&t=t&client=1`

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid`
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`token`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
无

******

#2、查看作业的习题列表的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/homework/1/exercises?uid=5&from=0&t=t&client=1

###URL `http://192.168.100.48:1092/v3/course/homework/{hwid}/exercises?uid=5&from=0&t=t&client=1`

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **作业ID**: `hwid`
+ **时间戳**: `from`   （Timestamp类型的）
+ **加密验证**：`token`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
JSON字段描述:
+ **作业习题主键**: `id` (int)
+ **作业主键**: `homeworkId' (int）
+ **作业主键**: `title' (java.lang.String）
+ **习题类型**:'type'（int，习题类型：0，单选；1，多选；2，是非判断题）
+ **本题分数**:'scoreAmount'（int）
+ **本题解析**:'explanation'（答题解析）
+ **答题选项**:'addition'（答题选项：id, 顺序； description， 答题选项内容；如果为是非题的话，那么该字段为null）
+ **答案**:'answer'（id:答案顺序，answer：Y，正确答案； N，错误答案；如果为是非题的话，那么该字段为取值范围为Y或N）



******


#3、提交作业并返回结果的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/1/homework/1/result?uid=5&totalScore=100&score=70&t=t&client=1

###URL `http://192.168.100.48:1092/v3/course/{cid}/homework/{hwid}/result?uid=5&totalScore=100&score=70&t=t&client=1`

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **课程ID**: `cid`
+ **作业ID**: `hwid`
+ **作业总分**: `totalScore`
+ **答题得分**: `score`
+ **加密验证**：`t`  
+ **客户端类型**: `client`  （1，Android; 2，iOS）

相关说明
===
JSON字段描述:
+ **作业ID**:'id'（int）
+ **作业是否完成**: `finished` (int: 0, 未完成; 1, 已完成)
+ **作业是否过期**: `overdue' (int: 0, 未过期; 1, 已过期）
+ **作业主键**: `submitTime' (java.lang.String）
+ **参入该作业的我的好友列表**:'friends'

******