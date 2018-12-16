Archery
============
项目基于[archer](https://github.com/jly8866/archer)，优化了工作流、权限、项目、配置管理等一系列模块，支持手机端申请和审核
## 资源（项目）组管理 
支持自定义资源组，管理资源组和关联对象，资源组成员之间审批流程、实例配置、消息通知等资源隔离
## 权限（角色）组管理
权限可以分配给用户，也可以分配给权限组，支持对大多数操作进行限制，独立控制用户的审核、执行等操作权限
## 工作流   
工作流审批流程支持多层级多用户，并且隔离资源组，不同资源组不同的工单类型可以配置不同的审批层级
## 配置管理  
系统配置项、工作流审批流程可在前端页面动态修改，无需重启服务实时生效
## 实例管理
* 会话管理，支持查看和批量终止会话
* 用户管理，支持管理实例用户，目前仅支持查看
* Binlog2SQL，将Binlog2SQL模块可视化，从MySQL binlog解析出你要的SQL。
* SchemaSync，对比不同数据库的Schema信息，输出修改语句和回滚语句，SchemaSync不仅限于表结构，它可以处理的对象还有：视图、事件、存储过程、函数、触发器、外键。
## SQL审核
#### SQL工单自动审批 
* 支持正则判断工单是否需要人工审批，开启自动审批后，不在正则范围内的SQL语句无需审批，系统自动审核
* 自主控制SQL是否自动驳回，可自主配置对inception审核驳回的场景，支持警告驳回和异常驳回  
#### 跳过inception执行工单  
* 对于inception不支持的语法，如子查询更新，可以跳过inception直接执行，但目前无法生成回滚语句   
#### 快速上线其他实例  
* 在工单详情可快速提交相同SQL内容到其他实例，可适用于test>beta>ga等多套环境维护的需求  
## SQL查询
#### 授权管理
* 工作流控制SQL查询授权，支持库表级别的权限限制，以及授权时间，查询结果集的限制
* 支持部分语句的动态查询脱敏（有限的功能）
* 支持前台管理用户权限，对用户权限进行修改和维护
#### 页面体验
* 库、表、字段补全提示
* 多结果级展示
* 表结构查看
## SQL优化
#### 慢日志管理
#### SQL语句优化
## 消息通知
## 可视化
