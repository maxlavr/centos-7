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

		#output will print some params, you can know about them by follow link  


	#### 1.2 locale

	#### THIS LINK CAN HELP YOU [MAN-LOCALE-OFFICIAL](https://jlk.fjfi.cvut.cz/arch/manpages/man/locale.1.en "man locale official")  

		#you need the mean some of 'locale' params (about anothers you can know follow the link):  
		- LANG (LANGUAGE)  
		- LS_MESSAGES (This category affects the language in which messages are displayed and what an affirmative or negative answer looks like)  
		- LC_ALL (All for above)  

		# locale have flags -a | -m  
		# locale -a (--all-locales) display a list of all of available locales (cat /usr/lib/locale/locale-archive)  
		# locale -m (--charmaps) display all of avalable charmaps 

		# for more info:  

	> locale -a -v  

		# infomations of this output located in /usr/lib/locale/locale-archive  

	#### 1.3 localectl  


	### 2.1  Change Language and Encoding Temporarily  
		# for a few time (after reboot will change)  
		# you should set value for global param LANG  
		# before print current value

	> echo $LANG

		# to change for rus for example type:  

	> LANG=ru_RU.utf-8  

		# after type to check:  

	> echo $LANG  

	### Change Language and Encoding Permanently  
		# if you don’t want to manually change the language and encoding each time  
		# you connect, you can set the locale on an ongoing basis  
		# edit ./bash_profile and add LANG='value' in  
