Items Needed to complete the project
Windows Subsystem for Linux- WSl
Docker


Step by step process
Pull ubuntu image from docker
Optional but confirm img has been successfully pulled.
Create a directory to host the ubuntu containers
Run first container with the name "container1" 
Install ssh in the container(apt-get update)
Install openssh (pat-get install openssh-server)
Install nano (apt-get install nano)
Enter the sshd config mode to permit password access
**  Find authentication permitRootLogin to "yes"and remove the "#"(nano /etc/ssh/sshd_config)
Start the ssh (service ssh start)/(service --status-all)
Create the second container 
Install ssh (apt-get update)
Install ssh client(apt-get install openssh-client)
Start/enter container1 (docker exec -it container1 bash)
Identify the root password. (cat /etc/shadow | grep root)
Update password (passwd root)
Identify ip address of cont1 by exiting the cont1(docker inspect container1 | grep IPAddress )
Start/enter container2 (docker exec -it container2 bash) 
Ssh into the container1 (ssh root@172.17.0.2)
