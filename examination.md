#1、查看课程考试的JSON接口#

URL
====
[ex] http://192.168.100.48:1092/v3/course/24/exam/list?uid=5&from=0&t=t&client=1

###URL `http://192.168.100.48:1092/v3/course/{cid}/exam/list?uid=5&from=0&t=t&client=1`

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
+ **考试数**: `examinationCount` 
+ **考试列表**: `examinations` ，考试列表字段如下：
+ **文档格式**: `format` (取url字段的lastindexOf("."), 如果字段url为null，那么建议处理为未知)
+ **文档版本**: `version` (如果大于本地的version，那么为更新的)
+ **文档地址**: `url` (完整资源路径地址)
+ **文档大小**: `size`

******