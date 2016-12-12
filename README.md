# ExoGameWebsite
Website for COMP204P project.
Working with ATOS on project Gamification.

	
Dear students,

To make your project website be accessible by the URL http://students.cs.ucl.ac.uk/2016/groupXX/index.html, your website files under /cs/student/www/2016/groupXX need (at the minimum) read access for others. Here others mean users who are neither the file's owner nor members of your COMP204P group. I use group1 as the example to demonstrate the steps to change the access permissions to all the files and directories under your project directory. 

1. Assess your web hosting directory by booting a Linux machine in a CS lab or using Thinlinc Client to connect thinlinc.cs.ucl.ac.uk. 

2. Open a terminal and navigate to your project directory. 

cd /cs/student/www/2016/group1

3. Change all the files to access permissions 664 (-rw-rw--r--). It means the files owner has the read and write permission for all the files; your team members have the read and write permission for all the files; the public can only read the file.

find . -type f -exec chmod 664 {} \;

4. Change all the directories to access permissions 775 (-rwxr-wsr-x).  It means the owner has the read, write and execute permission on all the child directories; your team members have the read, write and execute permission; the public has the execute permission.

find *  -type d -exec chmod 775 {} \;

5. Test your website by accessing the URL http://students.cs.ucl.ac.uk/2016/group1/index.html

Please click this link to learn more about Unix file access permissions. If you have any questions, please let me know. 
