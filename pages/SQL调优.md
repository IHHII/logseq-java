- 调优
	- sql调优
	- 表（结构）设计调优
	- 索引调优
	- 慢查询调优
	- 操作系统调优
	- 数据库参数调优
- 使用过哪些调优工具
	- 官方
		- EXPLAIN
		- mysqldumpslow
		- show profiles
		- ooptimizer_trace
	- 第三方
		- 性能诊断工具
		- 参数扫描提供建议
		- 参数辅助优化
- 如何监控慢sql，分析慢sql
	- 开启慢查询日志，收集sql
	- set global slow_query_log = 1
	- 查看slow.log
	- 日志分析工具mysqldumpslow
- 如何查看当前sql使用了哪个索引
	- 使用explain，选择索引过程可以使用optimizer_trace
	- DOING 补充资料
	  :LOGBOOK:
	  CLOCK: [2023-10-10 Tue 20:14:04]
	  CLOCK: [2023-10-10 Tue 20:14:07]
	  :END:
- 索引如何进行分析和调优
- explain关键字中的重要指标有哪些