- CAS就是比较并交换，通过CAS可以实现乐观锁机制，在每一次对数据进行操作的时候都会对值进行校对，从而判断是否有其他线程修改过这个值，没有修改过才会更新这个值
- 存在ABA问题，这个问题可以通过加一个版本号来解决