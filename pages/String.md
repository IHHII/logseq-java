- 长度固定，内容固定
- ```java
  private final char value[]
  ```
- [[数组]]导致长度不能变，[[final]]导致内容不能变
- 写法
	- 字面量写法
		- ```java
		  String name = "Kelly" //在全局字符串常量池
		  ```
	- 使用对象[[new]]
		- ```java
		  String tel = new String("123")
		  ```
- 常见方法
	- [[indexOf]]
	- [[charAt]]
	- [[concat]]
	- [[contains]]
	- [[equals]]
		- 判断两字符串内容是否相同
	- [[equalsIgnoreCase]]
	- [[startWith]]
	- [[endWith]]
	- [[getBytes]]
	- [[toCharArry]]
	- [[isEmpty]]
	- [[trim]]
	- [[split]]
	- [[substring]]
	- [[replace]]
	- [[lastIndexOf]]
	- [[toUpperCase]]
	- [[toLowerCase]]
	- [[valueOf]]
	- [[intern]]
	- [[length]]
- 字符串合并创建 #Java面试
	- ```java
	  "Hello"和"Hel"+"lo"是同一个对象
	  ```
	- ```java
	  "Hel""lo"",World"
	  a = "Hel" + "lo" + ",World"
	  Hello，world
	  共创建了5个字符串对象
	  "Hel" + "lo" 时会创建一个
	  ```
	- ```java
	  String a = "Hello"
	  String b = new String("Hello")
	  创建了两个对象
	  ```