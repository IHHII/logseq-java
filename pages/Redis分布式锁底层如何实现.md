- 利用setnx保证，key不存在才可以获得锁
- 利用lua脚本保证多个操作的原子性
- 利用看门狗监听锁过期时间
- 利用redlock保证节点挂了锁也不会被获取到