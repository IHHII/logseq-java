- @SpringBootApplicaiton注解 #card
	- @SpringBootConfiguration，本质是一个@Configuration，表示启动类也是一个配置类
	- @EnableAutoConfiguration，先Spring容器导入一个Selector，用来加载ClassPath下SpringFactories文件中所定义的自动配置类，将这些自动加载为配置Bean
	- @ComponentScan，表示扫描路径，默认为启动类所在目录
- @Bean，定义Bean
- @Controller，@Service，@Autowire