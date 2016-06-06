##Grandet是什么？
Grandet是一组面向QUANTS的Python工具库

##Grandet的历史
* Grandet前身是由北京正民惠浩投资管理有限公司面向内部开发的量化投资工具库
* 由2016年6月6日起，公司开发团队决定将其陆续开源，定名Grandet
* 公司开发团队将积极地开发和维护它

##Grandet库工具简介

Grandet由一系列工具组成，旨在提高QUANTS的工作效率
##### 基础工具：
* Grandet_base: 由交易日数据api、有效证券代码api等一系列基础api

##### tick数据工具：
* Grandet_tickORM: 高频tick数据ORM，将证券高频tick数据映射为class
* Grandet_DB： tick数据库接口及回调函数，
可将tick数据固化在elasticsearch、mysql、redis等数据库中
* Grandet_tickToBar： 基于tick数据生成bar数据
* Grandet_barToTick： 基于bar数据模拟tick数据

##### 回测及模拟工具：
* Grandet_algoTrade: 基于tick数据的策略回测及模拟分析

##### 基差交易工具：
* Grandet_basisCalcu: 基于tick数据，实时计算basket基差，并将其映射为class
* Grandet_basisPDF: 基于连续tick数据生成basket基差概率密度曲线，
    同时可分层叠加不同分布概率密度函数曲线
* Grandet_basisTrade: 基于不同分布概率密度函数（PDF）模型，实时生成基差交易模型风险数据

##### 基于久期的债券交易工具：
* Grandet_durationCalcu: 基于tick数据生成债券连续久期（duration）数据
* Grandet_durationCurve: 基于连续久期（duration）数据生成久期曲线，并作回归分析和曲线拟合
* Grandet_durationTrade: 实时扫描市场偏离拟合久期曲线的交易或报价

陆续还将开源可转债、分级基金、期权等工具

