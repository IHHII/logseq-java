- 通过@Scope注解可修改Bean的作用域
- prototype作用域，每次都是生成一个新的对象，不存在线程安全问题
- singleton作用域，默认线程不安全，日常开发大部分Bean是无状态的Bean，不需要保证线程安全
	- controller，service，dao线程安全
	- pojo线程不安全
	- 需要保证线程安全可以将作用域声明为ptototype，也可以采用ThreadLocal
	- 如果需要在多个线程间共享，那么就只能使用synchronized、lock、CAS