- synchronized和ReentrantLock
- jvm，接口
- 自动释放，手动释放
- 阻塞会一直等待，可以通过tryLock判断是否获取锁
- 不可判断锁状态，可以判断
- 可重入，不可中断，非公平、可重入，可判断，可公平非公平
-
- 性能不一样，竟争激烈情况lock性能好
- lock只能写在方法里
- lock有tryLock，lockInterrupiblty可以中断争抢锁
- ReentrantReadWriteLock实现读写锁
- 支持Condition