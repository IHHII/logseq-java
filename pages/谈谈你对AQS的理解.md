- AQS是抽象队列同步器，java并发包下的很多API都是基于AQS来是实现加锁以及释放锁的功能的，AQS是java并发包的基础类
- AQS内部有一个state变量，0变1表示加锁了，同时还有一个变量exclusiveOwnerThread用于记录加锁的线程，加锁时会tongguoCAS操作来改变state的值从而改变加锁的状态
- 由此可以实现可重入锁以及互斥锁，释放锁就是将state状态变为0，同时将加锁线程变为null，同时等待队列里的另外一个线程就可以重新加锁，从而从队列中出来