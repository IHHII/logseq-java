- [[Set]]接口的实现类
- 底层是 [[HashMap]] 的key
- 遍历
	- ((625782a9-c1c2-413d-b1cf-255ecbea27d4))
	- {{embed  ((625e1ecf-25a9-4b64-8eab-042fd889a062))}}
	- forEach遍历
	  id:: 625f6ab4-5bf2-40bf-a258-8d3d5765361f
	  {{embed ((625e5ddf-aa2d-4567-8531-3ccc94628ef7)) }}
- [[排序]]
	- 借助ArrayList的排序
	- ```java
	  Arraylist<String> arrs = new ArrayList<String>(datas);
	  Collections.sort(arrs);//升序排序
	  Collections.reverse(arrs);//反转降序
	  ```
- 去重原理
	- 计算hashcode值，看集合内是否存在
	- 如果存在，调用元素上的equals()与对应hash链表上每个元素比较，相同则不添加，不同就添加
- Java对象特点
	- 相同的[[Hash]]值，可能对象不同 Aa和BB
	- 相同对象，Hash值相同
- HashSet去重
	- 元素类重写 [[equals]]和[[hashCode]]