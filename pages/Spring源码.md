- {{video https://www.bilibili.com/video/BV1rb4y147F2?p=2}}
- UserService类->无参构造方法->对象->依赖注入->初始化前->初始化->初始化后->放入单例池Map->Bean
- 通过@Autowired进行依赖注入
  判断属性上是否有@Autowired注解
- 初始化前要通过@PostConstruct注解来执行一个方法
  判断方法上是否有@PostConstruct注解
- 初始化通过实现InitializingBean接口的afterPropertiesSet方法
  通过InstanceOf来判断是否实现了这个接口
- 初始化后即AOP后置处理器
- 有多个构造方法时，Spring会使用无参构造方法，当有两个有参构造方法且没有无参构造方法时会报错，可以在想要的构造方法上面添加@Autowired注解
- 使用有参的构造方法时入参是有值的，有三种注入方法，setter注入，构造器注入，注解注入（@Autowire基于属性注入）
- 需要注入某个Bean时，先去单例池查询是否有这个Bean，没有就去创建