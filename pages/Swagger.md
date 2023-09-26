- [[前后端分离]]开发模式中前后端需要同步开发，开发过程中需要提供接口说明
- 接口说明文档
	- 接口说明
	- 请求路径
	- 请求方法
	- 请求参数
	- 响应参数
	- 错误状态码
	- 请求模板
	- 响应模板
- 使用
	- import springfox-swagger2 springfox-swagger-ui dependency
	- configrue Class SwaggerConfigure
- @Api
	- 接口类的上方，描述，接口
- @ApiOperation
	- 方法上方，描述方法的用途
- @Apiparam
	- 方法传递的参数前，描述传递的参数
- @ApiModel
	- JavaBean上方，描述JavaBean含义
- @ApiModelProperty
- 拦截器放行Swagger
	- SpringMVC配置类中写addInterceptors
	- ```java
	   @Override
	  public void addInterceptors(InterceptorRegistry registry) {
	      // 创建拦截器类
	      HandlerInterceptor interceptor = new TokenInterceptor();
	      // 不必拦截的路径
	      List<String> excludePatterns = new ArrayList();
	      excludePatterns.add("/sys/login");
	      excludePatterns.add("/sys/register");
	      excludePatterns.add("/static/**");
	      // 放行Swagger
	      excludePatterns.add("/webjars/**");
	      excludePatterns.add("/swagger-resources/**");
	      excludePatterns.add("/v2/**");
	      excludePatterns.add("/swagger-ui.html/**");
	      // 注册拦截器类，添加黑名单 /* 只拦截一个层级 /** 拦截所有层级
	      // 和白名单excludePathPatterns(pattens)
	      registry.addInterceptor(interceptor)
	              .addPathPatterns("/**")
	              .excludePathPatterns(excludePatterns);
	  }
	  ```