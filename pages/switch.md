- 也是一种多分支结构 #多分支
- 与IF相比较,判断条件更多是几个固定的值
- **语法**
	- ```java
	  int num = 值;
	  switch(num){
	  	case 值1:
	      	//代码块1
	  		break;
	  	case 值2:
	      	//代码块2
	  		break;
	   	case 值3:
	      	//代码块3
	   		break;
	      ......
	  	default:
	      	//默认语句代码块
	  		break;
	  }
	  
	  ```
- switch中支持的数据类型
	- JDK1.7
		- byte,short,int,long
	- JDK1.8
		- 增加String,枚举