- for循环遍历
	- 从零开始
	- 不要超出范围
	- ```java
	  int[] numbers = {1,2,3}
	  int lnegth = numbers.length
	  for(int i = 0; i < length; i++){
	  	System.out.println(numbers[i]);
	  }
	  ```
- 增强for循环  for each循环
	- ```java
	  int[] numbers = {1,2,3}
	  for(int ele : numbers){
	  	System.out.println(ele);
	  }
	  ```
- 如果有针对下标的操作用第一种,否则第二种
- 使用Arrays.toString()
	- ```java
	  import java.util.Arrays;
	  
	  
	  int[] = {1,2,3,4,5,6,7};
	  System.out.println(Arrays.toString(ns))
	  ```