# BASH

**_command  -params  arg1  arg2  arg3…_**  

.	    текуща директория  
..	   горна директория  
**_man  command_name_**	      - command help/manual  
**_mkdir  <dir_name>_**	- създава директория  
**_rmdir  <dir_name>_**	- трие директория  
**_cd_**  без аргумент	- отива в Home директорията  
**_cd <path/name>_** 	- смяна на директория (отиди на посоченото място)  
**_ls_**	- чете текущата директория  
**_ls -R_**	- листва текущата директория и поддиректориите ѝ  
**_ls <dir_name>_**      - чете друга директория  
**_ls -la_**	- чете директория с детайли  (list all)  
**_rm <file_name>_**     - трие файл  
**_rm  -fR  *_**          или         **_rm  -fR  ./*_**	- рекурсивно трие всички файлове, поддиректории и файловете в тях  
    (R – рекурсивно	f – не питай за потвърждение	)  
  
**_cp  -R  <what_dir_to_copy>  <where_to_copy>_**	      - копира директория и съдържанието ѝ  
**_cp  <file_name>  <dir_name>_**        - копира файл в директория dir_name  
**_mv <file_name>  <dir_name>_**       - мести файл в директория  dir_name  
**_touch  <file_name>_**	- създава такъв файл, ако го няма; ако го има – променя датата на модификация  
**_clear_**  ==  cls	?????  
**_echo_**	- отпечатва стринг или променлива  
**_>_**	- предай побитово данните  на дясно (<   наляво)  
Ex:	**_echo  $PATH  >  file_name_**	- предава побитово данните от първия аргумент на втория аргумент  

**_grep_**	- търси String в String
 Ex:	**_grep -R <some_string> ./*_** 	(   -v    Което не се съдържа  )  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  какво&nbsp;&nbsp;&nbsp;	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;         къде				

|	- pipe  
Ex:	**_ls  |  grep  <dir_name>_**	- втората команда (grep) се подава на изхода на изпълнение на първата команда (ls)  

**_cat  <file_name>_**	- чете файла file_name  
**_locate  <fale_name>_**   (or part of fole name)	- локализира файла  
**_history_**	- списък на използваните команди  
**_pwd_**	- показва текущо местоположение (full path)  
**_rsync_**	- инкрементално синхронизиране на две директории  
 Ex:	**_rsync  -avz  <от_къде_да_копира>  <къде_да_копира>_**  

Права:   собственик/група/всички останали					&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;7	- пълни права  
x  - изпълнение &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6	- четене, запис  
r  - четене	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;								5	- четене, изпълнение  
w  - запис	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4	- четене  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0	- никакви права  
**_chmod  777  <file_name>_**	- променя правата на <file_name>  
**_chmod  -R  <dir_name>_**  

**_chown  -R  root.root  <file_name>_**    (or  dir_name)	- сменя собственост на файл/директория  
**_su  - <another_user>_**	- сменя текущия потребител с друг за текущата сесия на терминала  
**_su -_**	- текущият потребител става root	OR: sudo  su -  
**_ctrl – d_**		- излизане от сесия  
**_sudo  apt-get  install  apache2_**		- инсталиране  (rpm)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;remove			/var/www/html  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/etc/apache2	- конфигурационни файлове  

**_which  <app_name>_**	- къде е инсталирано приложението  
**_ps  -ax_**		- дава процесите в системата  
**_kill  -9_**  <номер_на_процеса>	      - убива процеса  
**_ps  -ax  |  grep   <име_на_процеса>_**         - убива самия процес  
**_tar  -ZXVF  <име_на_файл_за_разархивиране>_**	- разархивира файл  
**_tar -xvf file_name_** - ???  
**_unzip file_name_** - 

**_scp_**	- като cp , но м/у две машини
Ex:	**_scp  -r  root@192.168.12.4_**    .	
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -  
**_crontab  -l_**	- list на задачите в crontab  
**_crontab  -e_**	- режим на редактиране  
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -  
GitLab…  
**_sh  cli/up.sh_**		- дърпам/pull  
**_sh  cli/push.sh  “some description”_**	- качвам/push  
**_ssh  root@192.168.5.15	<-_**  
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -  
Vi – текстов редактор  
**_esc_**	- излиза от редакция  
**_i_**	- влиза в редакция  
**_iq_**	- излиза от фала  
**_:qi_**	- излиза без запис на промяната  
**_:w_**	- запис на промените  
**_:qw_**	- запис и излизане  
**_:е  <file_name>_**		- отваряне на файл file_name  
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -  
Links:  
[Start a GUI Application on a Remote Computer using SSH](https://www.shellhacks.com/start-gui-application-remote-computer-ssh/)  
[An A-Z Index of the Linux command line: bash + utilities](https://ss64.com/bash/)  
[Crontab in Linux with 20 Useful Examples to Schedule Jobs](https://tecadmin.net/crontab-in-linux-with-20-examples-of-cron-schedule/)  
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -   
**_ip addr_** - показва IP подобно на netstat  
**_netstat -nat_** - съкратено показване  

**_iptables_** - чети  
**_ufw_** - чети  
**_ufw deny 80_** - чети  
**_ufw a_** - чети  

**_tail file_name_**   - чети  
**tail -f***    - чети  

**_lsblk_** - листва системата в text mode (в конзолата)  
**_wget http://server/dir/dir/file_name.tar.gz_** - сваля файл  
**_ln -s what_name  where_name_**  - създаване на твърди и символични връзки (ln - прави линк, -s - символичен)  
**_sudo dpkg -i deb_packet_name_**  - инсталира deb-пакети  
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -  
**Java install:**  
.profile  
Ex: /home/pi/.profile  
Добавяме:  
**_export JAVA_HOME=my_jdk_location_**  
**_PATH=$JAVA_HOME/bin:$PATH_**  
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -  
## PI 
**_ssh pi@192.168.20.199_**  
PI - GOT - open sources:  
gogs(http://gogs.io)  
gitea(http://gitea.io)  
./gogs web &  
& след отдалечено стартиране оставя приложението да работи и след излизане от ssh-сесията  





