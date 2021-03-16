[TOC]

#  Mysql编程语句

## 一、更新语句

### 1、新增联合唯一索引

通用表达式：

```sql
ALTER TABLE (表名) ADD UNIQUE KEY (唯一索引名) (联合字段)
```

举例：

```sql
ALTER TABLE `user` ADD UNIQUE KEY `uk_u_uid_uname` (`user_id`, `user_name`);
```



### 2、新增列

通用表达式：

```sql
ALTER TABLE (表名) ADD COLUMN (列名) (类型) (DEFAULT [可选]默认值) (COMMENT [可选]备注)
```

举例：

```sql
ALTER TABLE `user` ADD COLUMN `user_name` VARCHAR(50) NOT NULL COMMENT '用户名字'
```



### 3、删除索引

通用表达式：

```sql
ALTER TABLE (表名) DROP INDEX (索引名)
```

举例：

```sql
ALTER TABLE `user` DROP INDEX `uk_u_uid_uname`
```



