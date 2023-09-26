- [[Map]]集合中的一种实现
- 底层结构
	- JDK1.7前：[[数组]]+ [[链表]]
	- JDK1.7后：[[数组]]+[[链表]]+ [[红黑二叉树]]
- 用法
	- ```java
	  HashMap<String,String> datas = new HashMap<>();
	  ```
	- [[put]]
	- [[putAll]]
	- [[get]]
	- [[getOrDefault]]
	- 允许放[[null]]键null值
	- [[replace]]
	- [[remove]]
	- [[clear]]
	- [[keySet]]
	- [[values]]
- [[去重]]
	- 依靠Hashcode和equals
	- HashSet的底层是HashMap的key
	- Keys要重写equals和hashCode
- 遍历
	- [[forEach]]
		- ```java
		  datas.forEach(new BiConsumer<Girl, Boy>() {
		    @Override
		    public void accept(Girl key, Boy value) {
		      System.out.println("key=" + key + ",value" + value);
		    }
		  });
		  ```
	- 获得键的集合
		- ```java
		  Set<Girl> keys = datas.keySet(); 
		  for (Girl e : keys) {
		    System.out.println("key=" + e + ",value=" + datas.get(e));
		  }
		  ```
	- [[entrySet]]
		- ```java
		  Set<Map.Entry<Girl, Boy>> entries = datas.entrySet();
		  for (Map.Entry<Girl, Boy> e : entries  {
		    System.out.println("key=" + e.getKey() + ",value=" + e.getValue());
		  }
		  ```