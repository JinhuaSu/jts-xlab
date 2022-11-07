# XXX函数 设计文档

| API名称 |	新增API名称 |
|  ----  | ----  |
| 提交作者 | 李强、张明 |
| 提交时间 | 2022-06-30 |
| 版本号 | 此设计文档的版本号，如V1.0 |
| 文件名	| 提交的markdown设计文档文件名称，如：20200301_cinn_api_design_clip.md |


## 一、函数功能

简要描述函数的用途或者使用场景，以ST_CLUSTERKMEANS为例
Takes a set of points as input and partitions them into clusters using the k-means algorithm. Returns an array of tuples with the cluster index for each of the input features and the input geometry.

## 二、业内方案调研

了解ST_CLUSTERKMEANS其他人的实现，比如可以看看JTS、Turf或者其他搜到library、paper里的实现

## 三、现状与对比分析

对调研的方案进行对比评价和对比分析，论述各种方案的优劣势。

## 四、设计思路与实现方案

原则是，换一个人看了这部分，他也能按照你这个设计完成实现。

## 五、命名与参数设计

命名：ST_CLUSTERKMEANS(geog, numberOfClusters)

入参：
- geog: ARRAY<GEOGRAPHY> points to be clustered.
- numberOfClusters: INT64|NULL numberOfClusters that will be generated. If NULL the default value Math.sqrt(<NUMBER OF POINTS>/2) is used.
- 
返回类型：

ARRAY<STRUCT<cluster INT64, geom GEOGRAPHY>>

## 六、实现思路：

文字描述清楚即可。

## 七、实现方案（伪代码）