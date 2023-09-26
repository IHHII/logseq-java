- 特点
	- 互斥
		- 当某个线程获得对象锁之后，其它线程不能再次抢占同样对象锁
	- 重入
		- 当根线程获得对象锁之后，它的其它方法依旧可以抢占同样的对象锁
- Java对锁的支持
	- Synchronized关键字
		- 同步代码块
			- 放置在方法内部
			- 可以灵活控制加锁代码的区域
			- ```java
			  synchronized(对象){
			    //锁定的代码
			  }
			  ```
		- 同步方法
	- Lock接口
	- 对比
		- Lock可以通过tryLock()判断锁的状态，synchronized无法判断
		- synchronized自动释放锁，Lock需要手动unlock()，不释放变为死锁
		- synchronized线程间需要不断等待，Lock不一定
		- synchronized可重入，不可中断，非公平锁，Lock可重入，可中断，可公平与不公平
		- synchronized适合锁定代码量非常少，Lock适合锁定代码量非常多
- 锁升级
	- synchronized根据线程数量决定锁的力度
	- 无锁
		- 刚创建，未引用
	- 偏向锁
		- 1根线程操作该对象
	- 轻量级
		- 2根线程同时操作该对象
	- 重量级
		- 2根以上线程同时操作该对象
	- 锁只有升级，没有降级
- 面试题 #Java面试
	- ```java
	  synchronized(this){}
	  // 获得当前对象的锁
	  ```
	- ```java
	  synchronized(user){}
	  // 获得user对象的锁
	  ```
	- ```java
	  synchronized(Object.class){}
	  // 获得Object class 类对象的锁
	  ```
	- ```java
	  public synchronized boolean sell(){}
	  // 获得当前对象的锁
	  ```
	- ```java
	  public synchronized boolean sell(){}
	  // 获得当前类的Class对象的锁
	  ```