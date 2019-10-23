# This is guide aboute configuration keyborad in centos-7

### Notice
	I recommended first of all to configure the basic/minimal tools in your system,  
	but you can to do it later. This is your choice, this is your life)  



#### HELPER LINK: [TO INSTALL MINIMAL CENTOS](../minimal/ "FOLLOW THIS LINK TO MINIMAL")  


1. ### Lets talk about localectl

	#### 1.1 localectl
		# localectl is util that control system locale and keyboard layout settings  
	> man localectl
		# the configuration file named locale.conf  
	> man locale.conf
		# it's place in /etc/locale.conf  
		# your can learn more after type  
	> man locale.conf
		# we need some params, but before configure we need to know virtual
		# console keyboard mapping(simple: what languages we can use?)
		# lets type:  
	> localectl list-keymaps
		# there is all available for you
		# very big output i think, make shorter, I need only macintosh and lets type:  
	> localectl list-keymaps | grep mac
		# this is all available for me(your can diff)
		# and now we can configure keyboead by
		# 1. open /etc/lcoalectl.conf or 2. use util localectl
		# lets use both
