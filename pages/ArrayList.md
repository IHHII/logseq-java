- ```java
  Arraylist datas = new ArrayList<>();
  ```
- 是[[List]]的实现类
- 常用[[API]]
	- 添加元素[[add]](),[[addAll]]()
		- 不能添加 [[基本数据类型]] ,底层将[[int]]类型包装为 [[Integer]] 类型
		- ```java
		  ArrayList datas = new ArrayList();
		  datas.add("name");
		  datas.add(1)
		  ```
	- [[size]]()
	- [[get]]()
	- [[add]](int index，element e)
		- 将元素插入指定下标。后面的元素后移一位
	- [[set]]()
	- [[remove]]()
	- [[contains]]()
	- [[indexOf]]()
		- 返回元素出现在集合中第一个位置的下标
	- [[isEmpty]]()
		- 判断内部是否有元素
	- [[clear]]()
- 集合遍历
	- ((625782a9-64e5-4f9a-8d40-45ed6f9ddaf9))
	- ((625782a9-c1c2-413d-b1cf-255ecbea27d4))
	- [[迭代器]] [[Interator]] 遍历
	  id:: 625e1ecf-25a9-4b64-8eab-042fd889a062
		- ```java
		  //返回迭代器
		  Iterator its = datas.iterator();
		  while(its.hasNext()){
		    //获得的元素
		    Object ele = its.next;
		    System.out.println(ele);
		    //边取边删除
		    its.remove()
		  }
		  ```
- [[集合排序]] #排序
	- [[数组排序]] Arrays.sort
- 集合工具包[[Collections]]
	- [[addAll]]
		- 向集合中添加元素
		- Collecetions.addall(datas,"ele1","ele2","ele3",...)
	- [[sort]]
		- Collestions.sort(datas)
		- 自定义 [[引用数据类型]] 要用到使用到[[Comparable]]接口
			- [[重写]][[compareTo]]
			- 然后调用sort方法
		- [[自然排序]]
		- [[自定义排序]]
			- 自己定义比较器，完成排序规则
			- 不需要实现Comparable接口
			- sort(List,Comparator<T>)
			- 重写compare
- 底层结构
	- 底层是数组结构
	- 初始长度为0，加第一个元素长度变10，后面每次长度增加都是原来的1.5倍