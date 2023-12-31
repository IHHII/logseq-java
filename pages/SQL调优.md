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
		  id:: 65252de4-1039-4af2-bcc6-c0f5d67074eb
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
  id:: 65253f94-6e42-488a-9f9f-510ee1d340d7
	- table
	- id
	- select_type
	- partitions
	- type
		- all全表扫描
		- index，索引
		- range，范围查询
		- ref，通过普通二级索引列与常量进行等值匹配
		- const
		- system
		- index_subquery
		- unique_subquery
		- index_merge
		- ref_or_null
	- possible_keys,可能使用的索引
	- keys，使用的索引
	- key_len，索引使用的字节数
	- ref
	- rows，查询时必须检查的行数
	- filtered
	- extra