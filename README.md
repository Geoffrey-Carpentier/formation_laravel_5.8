# laravel formation

channel youtube of creator : Nord Coders https://www.youtube.com/channel/UC36hi0WMeiR8HpUy-A2s4vQ

link playlist laravel class : https://www.youtube.com/watch?v=2m-A0PYuj6E&list=PLeeuvNW2FHVgvC-PdSfi309DbDMoEswiT

thanks to the youtuber "Nord Coders" ^^


first of all
--------------

- use windows 10
- install 1 text editor for coders (ex: vs code, sublime)
- install the "laragon" development stack : https://sourceforge.net/projects/laragon/files/releases/4.0/laragon-full.exe/download
- if you want another php version for windows (version 8) go : https://windows.php.net/download#php-8.0
	<br/>&emsp;. download the zip win32 x64 version if you are in 64 bits and prefere safe version
	<br/>&emsp;. go to laragon/bin/php and extract the zip in a folder with the zip name
	<br/>&emsp;. open laragon menu -> php/version/ choose the new one
	<br/>&emsp;. ! with php 8 you have to change 2 files : 
		<br/>&emsp;&emsp; laragon menu -> apache/dir:conf/mod_php.conf
			<br/>&emsp;&emsp;&emsp; change "php8_module" to "php_module"
		<br/>&emsp;&emsp; laragon menu -> php/php.ini/
			<br/>&emsp;&emsp;&emsp; active openssl mode -> find the line ";extension=openssl" and remove the ';'
- install the "composer" dependency manager for php  : https://getcomposer.org/
	<br/>&emsp;. select the good path with the php version you want to use -> laragon/bin/php/version you want/php.exe
- with composer v2 you have to active some extensions in the php.ini to install all the package when you create a laravel project
~~~
extension=fileinfo
extension=mbstring
~~~
- open laragon -> terminal
	<br/>&emsp;. tape command line : composer global require laravel/installer
	<br/>&emsp;. copy path generated on the console : C:/Users/username/AppData/Roaming/Composer (in this case)
- go to environment path
	<br/>&emsp;. on the top -> new
		<br/>&emsp;&emsp;variable name : LaravelInstaller
		<br/>&emsp;&emsp;variable value : paste the copied path with additional values on the end "/vendor/bin"
			<br/>&emsp;&emsp;&emsp;-> C:/Users/username/AppData/Roaming/Composer/vendor/bin
- close and reopen terminal
	<br/>&emsp;. tape command lines :
		<br/>&emsp;&emsp;- rm index.php
		<br/>&emsp;&emsp;- laravel new blog
- change the home page -> menu laragon/www/switch document root -> laragon/www/blog/public

infos
--------------
The formation consists to create chapter by chapter an application web with the "Laravel" framework.
So i created a repos that containts an empty "Laravel" project that will be completed gradually.
all the chapters are files.md in which you'll find the links of the modified files from the repos that containts the project "1st_laravel_project".
<br/>Files are linked with the commit i used to close the chapter. ("copy permalink" option) so the links don't' necessarily represent the actual state of the files... 
<br/> From the chapter 10, for easier understanding, all the instruction are noted in chronological order and the links that target the commits doesn't exist anymore.
<br/><br/> Warning ! if you download the repo and want to use it, the files ingored by the .gitignore files must be reinstalled or reconfigured :

- tip : create a new laravel project with the same name and copy the files from the downloaded project on it with overwrite duplicated data
- database.sqlite file -> need to be recreated and do "php artisan migrate" in the console
- .env file ->  reconfigure the db sqlite


