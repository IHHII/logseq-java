- ### 执行步骤
	- Hello代码
	  ```java
	  public class HelloWorld{
	  	public static void main(String[] args) {
	  		System.out.println("Hello World");
	  	}
	  }
	  ```
- 编译步骤
- > [[编译]]:相当于英文书籍的中文翻译,一定会出来一个新的文件
- > [[解释]]:国家领导人参与国际会议,戴的同声传译
- Java是一种半编译,半解释性语言
- [[字节码]]信息,配合JVM虚拟机,就可以做到[[跨平台]]
- Java源代码文件基本结构
	- Java程序依靠类来组织自己的代码
	- [[类]][[class]]
		- **类的类名要跟源代码的文件名保持一致**
	- ```java
	  public class 类的类名{
	    /*
	    Java程序中主函数/主入口
	    一个程序要跑起来,一定要有一个主入口
	    主函数的结构是固定的
	    */
	      public static void main(String[] arg){
	        
	        //其它代码
	        
	      }
	  }
	  ```
- 比如
	- ```java
	  public class SelfIntroduce{
	  	public static void main(String[] args){
	        
	      System.out.println("My name is ***")
	      
	  	}
	  }
	  ```
	- **SelfIntroduce** 类名,和文件名保持一致
	- **main** 函数方法
	- **System.out.println("")** 程序输出方法