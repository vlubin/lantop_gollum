#1、检测是否有新版本升级#

URL
====
[ex] http://192.168.100.48:1092/v3/upgrade/1/detection?uid=5&client=1&t=89D8FA86DDE18B59


URL 'http://192.168.100.48:1092/v3/upgrade/{version}/detection?uid=5&client=1&t=t'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **当前手机的版本**: `version`  （int，类型）
+ **客户端类型**: `client`  （1，Android; 2，iOS）
+ **加密验证**：`t`  

相关说明（JSON）
===
+ **新版本的更新描述**: `description` 
+ **返回的最近版本**: `versionCode`  （int，类型）
+ **是否有升级**: `hasUpgrade`  （boolean: true, false）
+ **APP 资源地址**：`url` (提供给Android, IOS可能用不上)

******

#2、记录用户升级历史#

URL
====
[ex] http://192.168.100.48:1092/v3/upgrade/2/history/save?uid=5&client=1&t=89D8FA86DDE18B59
URL 'http://192.168.100.48:1092/v3/upgrade/{version}/history/save?uid=5&client=1&t=t'

###支持格式 `JSON`

###HTTP请求方式 `GET`

参数说明
====

+ **用户ID**: `uid` 
+ **最新版本**: `version`  （int，上一个接口返回的版本号）
+ **客户端类型**: `client`  （1，Android; 2，iOS）
+ **加密验证**：`t`  

相关说明
===
无

******