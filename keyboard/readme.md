# This is guide aboute configuration keyborad in centos-7

### Notice
	I recommended first of all to configure the basic/minimal tools in your system,  
	but you can to do it later. This is your choice, this is your life)  



#### HELPER LINK: [TO INSTALL MINIMAL CENTOS](../minimal/ "FOLLOW THIS LINK TO MINIMAL")  


1. ### Lets talk about 'localectl' and 'locale'  

	#### 1.1 localectl & locale  

		# localectl is util that control system locale and keyboard layout settings  
		# locale is perl programm to use or avoid POSIX locales for built-in operations  

	> man localectl  
	> man locale  

		# the configuration file named locale.conf  

	> man locale.conf  

		# it's located in /etc/locale.conf  
		# to know more about your configuration now type:  

	> locale  
	> locale -v  
	> localectl  

	### this link can help you [man-locale-officail](https://jlk.fjfi.cvut.cz/arch/manpages/man/locale.1.en "man locale official")