- 一个分布式的开源搜索和分析引擎,在[[Apache]][[Lucene]]的基础上开发而成
- 优势
	- 速度快
	- 具有分布式的本质特征
	- 包含一系列的广泛功能
	- 简化了数据采集,可视化和报告过程
- [[Cluster]]集群
- Node节点
	- 一个节点是一个ES的实例
- Shard分片
	- 基于分片可进行分布式的并行的操作,进而提高性能,吞吐量
- 与 [[MySQL]]的比较
- [[Docker]]安装
	- ```yml
	  # PATH /usr/local/config/elasticsearch.yml
	  
	  cluster.name: "docker-cluster"
	  network.host: 0.0.0.0
	  http.cors.enabled: true
	  http.cors.allow-origin: "*"
	  http.cors.allow-headers: Authorization
	  ```
	- ```bash
	  docker run -d --name es -v /usr/local/config/elasticsearch.yml:/usr/share/elasticsearch/config/elasticsearch.yml -p 9200:9200 -p 9300:9300 --privileged=true -e ES_JAVA_OPTS="-Xms256m -Xmx256m" -e "discovery.type=single-node" registry.cn-hangzhou.aliyuncs.com/elasticsearch/elasticsearch:7.2.1
	  ```