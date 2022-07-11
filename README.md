# inception

### Introduction

This project aims to broaden your knowledge of system administration by using Docker. You will virtualize several Docker images, creating them in your new personal virtual machine.

### General guidelines

- This project need to be done on a Virtual Machine.
- Also, it is strongly recommended to use a .env file to store environment variables. 

### CHECK:

1. clone git repo to shared folder in VM (virtual machine)

In a VM:

2. go to the shared folder -> open terminal -> drag "commands" file to the terminal -> inside terminal press Enter button

3. go to the shared folder -> in terminal

> make

Check containers:

> docker ps
> make ps
> docker images -a

4. check nginx

> docker logs nginx

5. check mariadb

> docker exec -it mariadb bash
> mysql -utrurgot -ptrurgot
> status
> show databases;
> exit
> exit

Оpen browser in VM

6. check Adminer:

go to the localhost/adminer

(A self-signed certificate may appear. You must accept)

> server: mariadb
> user name: trurgot
> password: trurgot
> database: wordpress

You can see the structure of db

7. check SSL certificate:

go to the https://trurgot.42.fr/

(A self-signed certificate may appear. You must accept)

In address bar click padlock icon and examine the certificate (TLS v1.3)

8. go to the trurgot.42.fr/wp-admin

> user trurgotwa
> password trurgotwa

in left vertical bar: 

examine quantities of users (2: adm and subscriber)

examine plugins -> Redis

examine posts -> edit -> upgrade -> check changes

9. check stats

go to the localhost:8080

10. check static site

go to the localhost:4000

11. check ftp

In terminal:

> sudo apt install -y filezilla

Click: applications -> Internet -> filezilla

Make connections (localhost, trurgot, trurgot, 21) and examine the folder

12. you can reboot vm and check if the changes are stored

> sudo reboot
