# 数据库设计规范
1. 所有数据库均需要先修改pdm再修改数据库脚本
2. 数据库表名称、字段名称均采用Pascal命名规范,字段均需要进行备注
3. 所有表名称、字段均采用英文或通用英文单词缩写进行命名，禁止采用汉语拼音或是不通用的大写字母缩写等不规范的名称进行命名
4. 所有表均必须要有逻辑主键`Id`,且不带任何前缀
5. 所有表均需要包含CreateBy、CreateTime、UpdateBy、UpdateTime等审计字段。实体表还需要包含软删除相关字段(IsDeleted、DeleteBy、DeleteTime)，关系表不包含软删除相关字段
6. 所有表均不设置物理外键，通过逻辑外键进行关联
7. 不允许写存储过程和触发器