# 关于时间轴应用的设计

> 数据库字典  
  NODE_VALUE：节点时间戳  
  ID:一般表的主键  
  NODE_TYPE：img、md、video、txt 目前想到这么多类型  
  PARENT_ID：父叶子节点id  
  SPATIAL_LOCATION：空间位置 1.左，2.中，3.右
  IMG_URL：图片的地址  
  MD_VALUE：MD文档内容  
  VIDEO_URL：视频的地址  
  TXT_VALUE：文档内容  
   
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
PARENT_ID|bigint|父叶子节点id
SPATIAL_LOCATION|TINYINT(1)| 空间位置 1.左，2.中，3.右

### ImgInfo 图片表

字段|类型|说明
---- | ---- | ----
ID|bigint|叶子节点id
IMG_URL|VARCHAR(2000)|图片的地址

### MdInfo markdown 文档信息

字段|类型|说明
---- | ---- | ----
ID|bigint|叶子节点id
MD_VALUE|TEXT|MD文档内容

### VideoInfo 视频信息

字段|类型|说明
---- | ---- | ----
ID|bigint|叶子节点id
VIDEO_URL|VARCHAR(2000)|视频的地址


### TxtInfo  纯文档信息

字段|类型|说明
---- | ---- | ----
ID|bigint|叶子节点id
TXT_VALUE|TEXT|文档内容
