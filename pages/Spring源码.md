- UserService类->无参构造方法->对象->依赖注入->初始化前->初始化->初始化后->放入单例池Map->Bean
- 通过@Autowired进行依赖注入
  判断属性上是否有@Autowired注解
- 初始化前要通过@PostConstruct注解来执行一个方法
  判断方法上是否有@PostConstruct注解
- 初始化通过实现InitializingBean接口的afterPropertiesSet方法
  通过InstanceOf来判断是否实现了这个接口
- 初始化AOP后置处理器
-
-