# NETWORK

## YOU CAN USE 2 WAYS EDIT NETWORK SETTING
1. ## NMTUI (NetworkManager TUI)
2. ## EDIT CONFIG FILES:
	### /etc/sysconfig/network-scripts/ifcfg-enp0s3  
		# enp0s3 my interface, your can diff
		# here you should know some params:
			TYPE 		- Ethernet/Wired
			BOOTPROTO	- how to get IP: static/dhcp/none
			NAME		- "name of connection"
			DEVICE		- "name of interface"
			ONBOOT		- "tell machine to start this interface when your system start": yes/no
			IPADDR		- IP address that this machine will be use
			GATEWAY		- network access GATEWAY
			NETMASK		- network NETMASK
			DNS		- server for resolving DNS domain names
***

## Description
1. ### NMTUI (NetworkManger TUI)
	![img1](./imgs/1.png)  
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
		- ![img10](./imgs/10.png)  
		- ![img11](./imgs/11.png)  
		- ![img12](./imgs/12.png)  
	* sudo vi "config file"
		- ![img13](./imgs/13.png)  
	* edit config file(my config is manual)  
		![img14](./imgs/14.png)  
		- add / or edit some params(you should adapt your machine):  
			TYPE=Ethernet  
			DEVICE=enp0s3    
			ONBOOT=yes  
			IPADDR=192.168.0.29  
			PREFIX=24  
			NETMASK=255.255.255.0
			GATEWAY=192.168.0.1  
			DNS1=8.8.8.8
	* sudo systemctl restart network services  
		![img15](./imgs/15.png)  
		- "ping" or "nmctl d"
		![img16](./imgs/16.png)
