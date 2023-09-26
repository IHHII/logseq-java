- [[ElasticSearch]]的可视化管理工具
- [[Docker]]安装
	- ```yml
	  # PATH /usr/local/config/kibana.yml
	  #
	  # ** THIS IS AN AUTO-GENERATED FILE **
	  #
	  # Default Kibana configuration for docker target
	  server.name: kibana
	  xpack.monitoring.ui.container.elasticsearch.enabled: true
	  server.port: 5601
	  server.host: 0.0.0.0
	  elasticsearch.hosts: ["http://es:9200"]
	  i18n.locale: "zh-CN"
	  ```
	- ```bash
	  docker run --name kibana --privileged=true -v /usr/local/config/kibana.yml:/usr/share/kibana/config/kibana.yml  --link es:es -p 5601:5601 -d kibana:7.2.1
	  ```