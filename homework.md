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
JSON字段描述
"id": 1,(习题主键，int)
"originalId": 1,
"homeworkId": 1,（主页ID，int）
"title": "我的练习题",
"type": 0, （int，习题类型：0，单选；1，多选；2，是非判断题）
"scoreAmount": 10,（int，本题分数）
"explanation": null,（答题解析）
"addition": [
    {
        "id": 1,（答案顺序）
        "description": "dfsadsa"（答案）
    },
    {
        "id": 2,
        "description": "dasdsa"
    },
    {
        "id": 3,
        "description": "dsadsa"
    },
    {
        "id": 4,
        "description": "dsadsa"
    }

],
"answer": [
    "Y",（正确答案）
    "N",
    "N",
    "N"

]

******