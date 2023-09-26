- XML
	- Extensible Markup Language 可扩展标记语言
		- 用于标记电子文件使其具有结构性的标记语言，可以用来标记数据、定义数据类型，是一种允许用户对自己的标记语言进行定义的源语言。 XML使用DTD(document type definition)文档类型定义来组织数据;格式统一，跨平台和语言，早已成为业界公认的标准。
		  XML是标准通用标记语言 (SGML) 的子集，非常适合 Web 传输。XML 提供统一的方法来描述和交换独立于应用程序或供应商的结构化数据。
	- 用途
		- 存储数据
		- 配置文件
		- 跨平台数据传输
- JSON
	- JavaScript Object Notation
	- 一种轻量级的数据交换格式，具有良好的可读和便于快速编写的特性。可在不同平台之间进行数据交换。JSON采用兼容性很高的、完全独立于语言文本格式，同时也具备类似于C语言的习惯(包括C, C++, C#, Java, JavaScript, Perl, Python等)体系的行为。这些特性使JSON成为理想的数据交换语言。
	  JSON基于JavaScript Programming Language , Standard ECMA-262 3rd Edition - December 1999 的一个子集。
- 对比
	- 可读性方面。
		- JSON和XML的 数据可读性基本相同，JSON和XML的可读性可谓不相上下，一边是建议的 语法，一边是规范的标签形式，XML可读性较好些。
		- 可扩展性方面。
	- XML天生有很好的扩展性，JSON当然也有，没有什么是XML能扩展，JSON不能的。
	  (3).编码难度方面。
	- XML有丰富的编码 工具，比如Dom4j、JDom等，JSON也有json.org提供的 工具，但是JSON的编码明显比XML容易许多，即使不借助 工具也能写出JSON的 代码，可是要写好XML就不太容易了。
	  (4).解码难度方面。
	- XML的解析得考虑子节点父节点，让人头昏眼花，而JSON的解析难度几乎为0。这一点XML输的真是没话说。
	  (5).流行度方面。
	- XML已经被业界广泛的使用，而JSON才刚刚开始，但是在Ajax这个特定的领域，未来的发展一定是XML让位于JSON。到时Ajax应该变成Ajaj(Asynchronous  JavaScript and JSON)了。
	  (6).解析手段方面。
	- JSON和XML同样拥有丰富的解析手段。
	  (7).数据体积方面。
	- JSON相对于XML来讲， 数据的体积小，传递的速度更快些。
	  (8).数据交互方面。
	- JSON与 JavaScript的交互更加方便，更容易解析处理，更好的数据交互。
	  (9).数据描述方面。
	- JSON对数据的描述性比XML较差。
	  (10).传输速度方面。
	- JSON的速度要远远快于XML。