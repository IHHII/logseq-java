- Java中所有[[类]]都是Class类型的[[对象]]
- 类加载器负责加载所有的类,class字节码文载入到内存中，载入到内存的类[[JVM]]会创建一个Java.lang.Class对象
- 通过该class对象可以访问该类的所有方法
- 获取该类的class对象
	- 1. 访问类的class属性
	  2. 调用对象的getClass(）方法
	  3. 通过类的全限定名字符串加载
- java.lang.reflect包
- 通过[[反射]]调用该类的构造方法
	- 通过getConstructor()
		- 1. 获取该类的Classdu