- 解决[[基本数据类型]]浮点数[[float]][[double]]在参与运算时存在丢失精度的问题
- ```java
  //使用字符串作为参数，最精准
  BigDecimal a = new BigDecimal("0.1");
  ```
- 加减乘除
	- ```java
	  a.add(b);
	  a.subtract(b);
	  a.multiply(b);
	  a.divde(b);
	  ```
	- 收尾规则
		- ROUND_DOWN去尾模式
			- 直接去掉后面的数
		- ROUND_UP收尾模式
			- 判断最后舍弃的那个位置是否为0,非0则加1
		- ROUND_HALF_UP
			- [[四舍五入]]