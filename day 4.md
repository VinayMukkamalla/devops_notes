VIM editor 



head



tail



45 mins



**user Management**



sudo su



current path as root



sudo su -  



/root path as root user



user and group creation



useradd suresh  --> when you create a user in Linux bydefault a group will be created with the username

groupadd devops



cat /etc/passwd

suresh:x:1001:1001::/home/suresh:/bin/bash



cat /etc/group  --> A user in Linux must have atleast 1 primary group and 1 secondary group

suresh:x:1001:

devops:x:1002:





password(encrypted)



cat /etc/shadow



ec2-user:!!:20342:0:99999:7:::

suresh:!!:20342:0:99999:7:::





usermod -g <groupname> <username>



id suresh

&nbsp;gid=1001(suresh) groups=1001(suresh)

usermod -g devops suresh

id suresh

gid=1002(devops) groups=1002(devops)



secondary group is used to give access to other teams temporarily



allow users to login using password 



vim /etc/ssh/sshd\_config  --> :/PasswordAuthentication  no --> yes



sshd -t to check after changing as the above file is very important



&nbsp;systemctl restart sshd   -->  restart to reflect changes



as we have given access to suresh to login to server through username and password he can login



by using ssh suresh@ipaddress



last -->  to check whoever logged in



remove user fromgroup



gpasswd -d suresh operations





&nbsp;      useradd suresh

&nbsp;  10  groupadd devops

&nbsp;  11  id suresh

&nbsp;  12  cat /etc/passwd/

&nbsp;  13  cat /etc/passwd

&nbsp;  14  cat /etc/group

&nbsp;  15  cat /etc/shadow

&nbsp;  16  clear

&nbsp;  17  id suresh

&nbsp;  18  usermod -g devops suresh

&nbsp;  19  id suresh

&nbsp;  20  history

&nbsp;  21  pwd

&nbsp;  22  sudo su -

&nbsp;  23  who

&nbsp;  24  groupadd operations

&nbsp;  25  cat /etc/group

&nbsp;  26  usemod -aG operations suresh

&nbsp;  27  usermod -aG operations suresh

&nbsp;  28  id suresh

&nbsp;  29  passwd suresh

&nbsp;  30  vim /etc/ssh/sshd\_config

&nbsp;  31  sshd -t

&nbsp;  32  history

&nbsp;  33  systemctl restart sshd

&nbsp;  34  exit

&nbsp;  35  pwd

&nbsp;  36  sudo su -

&nbsp;  37  exit

&nbsp;  38  gpasswd -d suresh devops

&nbsp;  39  id suresh

&nbsp;  40  gpasswd -d suresh operations

&nbsp;  41  id suresh







file permissions





@1:26 mins



download diagram and draw.io and existing diagram











