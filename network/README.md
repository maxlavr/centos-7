# NETWORK

you can use 2 ways edit network settings
* NMTUI (NetworkManager TUI)
* edit file /etc/sysconfig/network-scripts/ifcfg-enp0s3 <-- config file
	- enp0s3 my interface, your can diff
***

## Description
1. ### NMTUI (NetworkManger TUI)
	* edit a connection
	![img1](./imgs/1.png)  
	* <choose your interface> and press <Edit ...>
	![img2](./imgs/2.png)
	* IPv4 CONFIGURATION: choose your
		- if "automatic" scroll down and press <OK> 
		![img3](./imgs/3.png)  
		- else edit settings scroll down and press <OK>  
		![img4](./imgs/4.png)  
	* press <Back ...>  
	![img5](./imgs/5.png)  
	* press <Quit ...>  
	![img6](./imgs/6.png)  

#
2. ### edit config file
	* stop NetworkManger.service
	* nano vi "config file"
	* edit config file(my config is manual)  
		- add:  
			DEVICE=enp0s3  
			ONBOOT=yes  
			IPADDR=192.168.0.29  
			PREFIX=24  
			GATEWAY=192.168.0.1  
	* sudo systemctl restart NetworkManager.service
