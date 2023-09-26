- Universally Unique Identifier
- [通用唯一识别码](https://zh.wikipedia.org/wiki/%E9%80%9A%E7%94%A8%E5%94%AF%E4%B8%80%E8%AF%86%E5%88%AB%E7%A0%81)
- UUID的标准型式包含32个16进制数字，以连字号分为五段，形式为 8-4-4-4-12 的32个字符。
- ![通用唯一识别码.pdf](../assets/通用唯一识别码_1649925769559_0.pdf)
- 使用
	- ```java
	  String str = UUID.randomUUID().toString();
	  System.out.println(str);
	  ```