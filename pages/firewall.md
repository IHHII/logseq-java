- 开端口
	- ```bash
	  firewall-cmd --permanent --add-port=8080/tcp --permanent
	  ```
	- ```
	  - --permanent 让端口配置永久生效
	  ```
- 重载防火墙
	- ```bash
	  firewall-cmd --reload
	  ```
- 重启防火墙服务
	- ```bash
	  systemctl restart firewalld
	  ```