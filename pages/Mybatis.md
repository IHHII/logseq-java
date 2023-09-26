- ```java
  //读取Mybat配置文件
  InputStream mybatisConfigInputStream = Resources.getResourceAsStream("mybatis-config.xml");
  //创建sqlsession会话工厂
  SqlSessionFactoryBuilder factoryBuilder = new SqlSessionFactoryBuilder();
  //一个数据库 对应一个会话工厂
  SqlSessionFactory factory = factoryBuilder.build(mybatisConfigInputStream);
  //获取会话 会话用来执行sql语句,提交,回滚事务
  SqlSession sqlSession = factory.openSession();
  //关闭session
  sqlSession.close();
  ```