# 业务路线图

* 1.0: 无车共乘业务
* 2.0: 顺风车业务
* 3.0: 共享巴士业务

# 1.0 无车共乘

无车共乘是最简单的共乘模式，不需要复杂的运营。

通过无车共乘，提供特定场景的便利，积累初始用户，同时建立基础运营数据（如上车点）。

## 阶段1-1： 能够在特定场景下拼车（车站机场），用户自行结算。

* 每个“共乘”最多包含2个出行计划。
* 用户默认5-5支付。不涉及支付链路，用户会合视作拼车成功。
* 每个用户只能有一个活动的预约单
* 具有通知机制
* 最简化的撮合算法
* 有限区域运营， 系统设定上车点，静态上车点引导信息
* 不考虑撮合的性能和时效性要求

## 阶段1-1'：体验优化
* 根据用户定位，推荐上车点 （案例目的：增加上车点服务）
* 优化撮合算法 （案例目的：TDD）
* 优化距离计算，使用外部服务 （案例目的：依赖外部服务）
* 超时撮合失败通知


## 阶段2: 普通场景下的拼车

* 每个“共乘”可以包含多个出行计划。（案例目的：推动领域模型的演进）
* 根据共乘的人数计算费用 （案例目的：增加价格计算服务，练习设计契约和接口）
* 增加上车点管理能力 （案例目的：1. 增加管理前端，2. 为后续数据驱动的业务运营做准备）

# 2.0 顺风车

## 阶段2-1: 基础顺风车业务能力支持

* 乘客发起出行计划时可声明”我是车主“
* 支持不同的车型，可以管理车辆信息
* 仅匹配同起点（中间无上车）出行
* 增加顺风车计价策略

## 阶段2-2: 顺风车运营优化
* 增加可中途上车拼车能力
* 增加行程反馈功能
* 预测抵达时间和地点，显示对方位置
* 常用路线推荐：综合当前位置和历史数据，推荐起点和终点


# 3.0 共享巴士
* 通过管理界面规划周期性共乘
* 静态线路管理
* 固定费用策略
