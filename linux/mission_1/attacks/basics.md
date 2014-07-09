


Mission Linux
==========
1->How does the directory structure look like in a linux file system?
------------------------------------------------------------------------------------


		“/” (root) is the directory is parent of all the other directory of system. / contains following directories {bin    dev   initrd.img  lost+found  opt   run   sys  var
 boot   etc   lib   media       proc  sbin  tmp  vmlinuz
 cdrom  home  lib64       mnt         root  srv   usr
}. /Home is a directiory which contains a child directory per user. Linux is designed for Multiuser systems, so when standerd user logs in, that user can access only own directory of home. There are some files that are with “s” version, say “bin” and “sbin” both are available. “sbin” is accessible to administarators. 
The purpose of all directory is explained below:
 http://www.tecmint.com/linux-directory-structure-and-important-files-paths-explained/


2->What are executables & how do we get access to executables in the command promt.
----------------------------------------------------------------------------------------------------------


	  Executable files are those which can be executed by machine directly. They are in a form that human can not read/understand.
	To get the file executed from any where in machin, the file's parent directory must be included in $PATH. So now ultimatly two options are there to make file executable from any where 1) Put the file in the directory which is already exist in $PATH.
	$PATH will enlist the directories in environment variable, Put the file in any of them.
2) Include the file's parent directory in $PATH.
	.bashrc is executed each time when non-login terminal is launched. so those path which we want to set as variable path can be included in this file. 
	.bash_profile or .profile are the files which are executed when user logged in. The scope for this is "session". 

3->What are users &  groups in linux and how are they used while assiging permissions for files and folders.
------------------------------------------------------------------------------------------------------------------------


	User is logically an account in linux. When ever user created, a directory with user_name is created under /Home and . This directory will contain user specific data. One user do not have access rights over other users Home directory.  Group is collaction of Users. Say there are 50 student users, and somebody want to grant permission of some file to all students. Instead of giving access individually , give access to “student group” which contains all 50 students account in it. 

