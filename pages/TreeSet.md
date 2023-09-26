- 一种树形结构的集合
	- [[二叉树]]结构
		- 每一个节点下最多两个分支
	- TreeSet结构为[[红黑二叉树]]
		- 通过红黑二叉数可提升操作和查询效率
- 特点
  id:: 625fe239-5548-4c66-ba66-f6fb1629b682
	- 元素存储有序
	- 元素不能重复
	- 没有下标
- [[API]]与HashSet一致
- 排序
	- 借助 [[ArrayList]]排序
- [[去重]]原理
  id:: 625fa874-b218-4044-ac16-b9de892cd9d2
	- 不依靠[[Hash]]Code及 [[equals]]
	- 依靠[[比较器]] [[Comparable]]
	- Key上一定要实现Comparable
	- ```java
	  public class Girl implements Comparable<Girl> {
	      private String name;
	      private String id; 
	  	@Override
	    	public int compareTo(Girl o) {
	      if (this.equals(o)) {
	        return 0;
	      }
	      if (this.name.equals(o.name)) {
	        return this.id.compareTo(o.id);
	      } else {
	        return this.name.compareTo(o.name);
	      }
	    }
	  }
	  ```
- 和 [[HashSet]]的区别