- 进行扫描，得到所有的[[BeanDefination]]对象，存在一个Map中
- 筛选出非懒加载的单例BeanDefination创建Bean，多例的Bean会在获取Bean的时候再利用BeanDefination创建
- 利用BeanDefination创建Bean，其中包括合并BeanDefination、推断构造方法，实例化，属性填充，初始化前，初始化，初始化后（AOP）等步骤，
- 创建完成单例Bean后Spring发布一个容器启动事件