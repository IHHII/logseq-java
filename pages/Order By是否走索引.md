- 没有过滤条件时不会走索引，需要有过滤条件
- 通过索引排序内部流程是什么
	- select name,id from user where name like '%明' order by name;
	- select name,id,age from user where name like '%明'
	- sort_buffer可供排序的内存缓冲区大小
	- max_length_for_sort_data单行所有字段总和限制，超过启动双路排序
	- 通过索引检测过滤筛选条件需要用到的排序字段+其他字段
	  logseq.order-list-type:: number
	- 判断索引内容是否覆盖select字段
	  logseq.order-list-type:: number
		- 如果覆盖索引，select字段和排序都在索引上，在内存中进行排序，排序后输出结果
		  logseq.order-list-type:: number
		- 如果索引没有覆盖查询字段，接下来计算select的字段是否超过max_length_for_sort_data限制，超过使用双路排序
		  logseq.order-list-type:: number
- 单双路排序
	- DOING 找相关资料学习
	  :LOGBOOK:
	  CLOCK: [2023-10-10 Tue 16:25:32]
	  CLOCK: [2023-10-10 Tue 16:25:34]
	  :END:
	- 单路排序
		- 一次性取出所有字段排序，内存不够用时会使用硬盘
	- 双路排序
		- 取出排序字段进行排序，排序完成后再次回表查询其他需要的字段
	-
- group by 和order by在索引使用上有什么区别
	- group by先排序再分组，遵循最左前缀原则
	- group by没有索引也可以用上索引，order by必须有过滤字段才能用上索引
- 有字段为null，是否要创建索引
	- null值比较高的时候会显示range
	- is null会走索引，is not null只有在大部分都是null值才会走索引
- 有字段为null索引是否会失效
	- 不一定会失效
	- 最好还是给上默认值0或""