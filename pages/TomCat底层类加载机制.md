- Tomcat Web容器需要部署多个程序，不同应用程序会依赖同一个第三方类库的不同版本
- DOING 补充类加载器
  :LOGBOOK:
  CLOCK: [2023-10-16 Mon 14:57:28]
  CLOCK: [2023-10-16 Mon 14:57:34]
  :END:
- commonLoader：最基本类加载器，可以被Tomcat容器本身和各个webapp访问