- 错误日志error log
- 慢查询日志slow query log
	- 默认10s
	- 手动开启
	- 支持将日志写入文件
- 一般查询日志generallog
- 重写日志redolog
	- 基于磁盘的数据结构，用来宕机时恢复不完整的数据
	- 用于恢复更新了内存但是还没有刷入硬盘的数据
- 回滚日志undolog
	- 回滚到某一版本，是一种逻辑数据
	- 记录修改之前的数据，delete对应一条insert数据
	- 提供mvcc下的读取
- 二进制日志binlog
	- 记录增删改时的sql（当前时间，系统相关）记录的日志，修改了内容就会产生一条bin log
	- 进行主从复制，数据库的恢复
- 是否实时写入磁盘
	- binlog
		- sync_binlog
		- 0,写入页缓存，操作系统决定刷盘，有丢失日志风险
		- 1，每次提交事务都写入磁盘
		- N，N个事务后写入磁盘
	- redolog
	- undolog
	- **innodb_flush_log_at_trx_commit**
		- 0：每秒写入磁盘
		- 1：每次提交调用fsync刷新IO缓存
		- 2：每次都把redolog写入page cache，由系统接管什么时候写入磁盘
- 时机顺序
	- DOING 补充笔记
	  :LOGBOOK:
	  CLOCK: [2023-10-10 Tue 17:58:30]
	  CLOCK: [2023-10-10 Tue 17:58:34]
	  CLOCK: [2023-10-10 Tue 17:58:34]
	  :END:
- redolog和binlog的两阶段提交
- binlog有几种录入格式
	- statement
		- 不记录数据变更，只记录sql语句和每一行数据变化
	- row
		- 不记录sql语句上下文信息，记录数据被修改，修改成什么样
	- mixed
		- 有函数用row，没函数用statement，无法识别系统变量
- 集群同步为什么使用binglog
	- binglog是mysql提供的日志，所有存储引擎都可以使用
	- 支持增量同步
	- 可以供其他中间件读取，hdfs
	- 复制表数据
		- 不支持某个阶段回放
		- 复制过程中断很难确定复制的offset