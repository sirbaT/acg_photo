# 关于时间轴应用的设计

> 数据库字典  
  NODE_VALUE：节点时间戳  
  ID:一般表的主键 
  
### Timeline 表设计

字段|类型|说明
---- | ---- | ----
NODE_VALUE|TIMESTAMP|节点时间戳，主键

### TreeNode 表设计

字段|类型|说明
---- | ---- | ----
ID|bigint|叶子节点id
NODE_TYPE|char(8)|img、md、video、txt 目前想到这么多类型
NODE_VALUE|TIMESTAMP|所挂在的时间轴节点

### ImgInfo 图片表

字段|类型|说明
---- | ---- | ----
ID
