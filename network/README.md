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
	* choose your interface and press <Edit ...>
	![img2](./imgs/2.png)
	![img3](./imgs/3.png)  
	* IPv4 CONFIGURATION: choose your
		- if "automatic" scroll down and press <OK...> 
		![img4](./imgs/4.png)  
		- else edit settings scroll down and press <OK...>  
		![img5](./imgs/5.png)  
		![img6](./imgs/6.png)  
	* press <Back ...>  
	![img7](./imgs/7.png)  
	* press <Quit ...>  
	![img8](./imgs/8.png)  
	* result  
	![img9](./imgs/9.png)  

#
2. ### edit config file
	* type: stop all network services
		- img10  
		- img11  
		- img12  
	* sudo vi "config file"
		- img13  
	* edit config file(my config is manual)  
		img14  
		- add:  
			DEVICE=enp0s3  
			ONBOOT=yes  
			IPADDR=192.168.0.29  
			PREFIX=24  
			GATEWAY=192.168.0.1  
	* sudo systemctl restart network services  
		img15  
		- ping  
		img16
