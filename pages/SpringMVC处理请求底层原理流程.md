- 请求发送到Tomcat内部，tomcat内部部署的应用程序会处理请求
- Tomcat只关注Servlet类，通过配置会扫描Servelet，会创建DispatchServlet来进行处理
- DispatchServlet根据请求路径来找到Spring容器内Controller Bean内的方法，DispatchServlet内部有一个WebApplicationContext的容器
-
- Tomcat启动
- 解析webapp下META-INFO的web.xml文件 ，listener，创建父容器
- DispatchServlet实例化
- DispatchServlet对象.init(),重写了init方法就拥有了自定义的初始化逻辑，init重写在HttpServletBean里面
	- initServletBean方法会初始化Servlet从而创建Spring容器
	- initWebApplicationContext() -> createWebapplicationContext()
	- 最终完成Spring容器的创建，建立factoryBean等
-