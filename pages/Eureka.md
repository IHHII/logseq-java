- # 注册中心
- spring netfilx的核心组件之一
- 用于注册服务和地址，实现服务信息注册和查找
- 维护服务名称和服务实例对应关系
- 每个微服务都会向注册中心获取服务列表，汇报运行状态，当有其他服务调用是，可以从服务列表中获取实例地址调用
- 服务端配置
	- 启动类注解`@EnableEurekaServer`
	- ```yaml
	  spring:
	    application:
	      name: eureka-server # eureka-server,Server名字自定义
	  server:
	    port: 8761 # eureka-server port, default is 8761
	  
	  eureka:
	    client:
	    	service-url:
	        defaultZone: http://localhost:8761/eureka # eureka-server default zone 向Eureka Server注册时,注册中心地址
	      register-with-eureka: false # eureka-server register-with-eureka, false 不向注册中心注册
	      fetch-registry: false # eureka-server fetch-registry, false 是否获取注册信息
	  ```
- 客户端配置
	- 启动类注解
		- `@EnableDiscoveryClient`用于可能使用其它注册中心时
		- `@EnableEurekaClient`用于仅使用Eureka注册中心
	- ```yaml
	  spring:
	    application:
	      name: eureka-client # eureka-client 客户端向注册中心注册的服务ID
	  server:
	    port: 8080
	  eureka:
	    client:
	      service-url:
	        defaultZone: http://localhost:8761/eureka # 注册中心地址
	  ```
- 服务续约
	- 默认30s发送一次心跳，超时90s
- 自我保护机制
	- 因网络故障导致服务不可用时的一种保护机制
	- 网络异常，服务正常的
	- 开启后不剔除故障服务，等待修复网络正常
- 高可用
	- 注册中心集群，防止某个服务宕机
	- 注册中心相互注册，客户端同时在两个注册中心注册