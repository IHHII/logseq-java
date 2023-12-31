- [[Tomcat]]是轻量级的服务器，处理的并发请求低，无法处理高并发请求
	- 使用Tomcat服务器[[集群]]可提高处理请求的能力
- 负载均衡服务器
	- Apache服务器
	- Nginx服务器
		- 更加轻量，容易配置
		- 采用异步非阻塞式，性能较高
- 负载均衡
	- 算法
		- 轮询
			- 轮流分配请求
		- 随机
			- 随机分配请求
		- 最少连接
			- 当前那一台服务器处理请求少，分配给谁
		- 权重
			- 分配的请求的占比
		- 地址粘贴
			- 相同的IP地址请求发送到同一台服务器
- 反向代理
	- **代理服务器来接受Internet上的连接请求，然后将请求转发给内部网络上的服务器**
	- 正向代理：内网中的设备需要访问外部网络需要利用正向代理上网
	- 好处：可以在服务器上做负载均衡，也可做动静分离
- [[Docker]] 实现
	- 运行nginx镜像
	- 配置nginx的nginx.conf
- 动静分离
	- 静态资源请求量远大于动态资源
	- 修改nginx.conf配置文件