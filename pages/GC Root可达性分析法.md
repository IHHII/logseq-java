- 将GC Root对象作为起点，从这些节点开始向下搜索引用的对象，找到的对象标记为非垃圾，其它为垃圾
- 根节点：线程栈的本地变量，静态变量，本地方法栈的变量