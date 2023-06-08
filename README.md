# WebHosting-with-DigitalOcean
WebHosting with DigitalOcean
Hello Everyone today i am going to teach  you how you can upload a wordpress website to digital ocean website


First
1. Create an account on digitalocean 
I have already created 
2. Login into the account
3. Now you need to create a project
4. Now you have to create a droplet in it

Droplet is term used by digitalocean that simple means a server

Droplet can be configured

5. Click on the IP of the server

6. Now use terminal to access the droplet with SSH
7. Now you can see i have successfully logged in

8. Now install LAMP stack 

9. Digital ocean has very detail documentation on this

 apt: command not found
It mean that this is not a ubuntu machine

We are going to create a new droplet with Ubunto 22.x

Basic > PremiumAMD > 14$

Lets remove the previous droplet
Previous droplet is destroyed

Our new droplet is created

Let connect it with SSH
You can see i am successfuly logged in

Now lets follow the documentation

 systemctl status mysql.service

https://dmdailytricks.com/

sudo mkdir /var/www/dmdailytricks.com

sudo chown -R $USER:$USER /var/www/dmdailytricks.com

sudo nano /etc/apache2/sites-available/dmdailytricks.com.conf

sudo a2ensite dmdailytricks.com

nano /var/www/dmdailytricks.com/index.html

nano /var/www/dmdailytricks.com/info.php

sudo rm /var/www/dmdailytricks.com/info.php


CREATE DATABASE dmdailytricks_db;

CREATE USER 'dmdailytricks_user'@'%' IDENTIFIED BY 'password';

GRANT ALL ON dmdailytricks_db.* TO 'dmdailytricks_user'@'%';

now you have to flush the previleges
FLUSH PRIVILEGES;

Now its time to upload the zip of Wordpress installation to the server

My Zip is located at desktop



I will use SCP (Secure Copy Linux utility command to send the zip from my computer to the droplet

)

scp [OPTIONS] [[user@]src_host:]file1 [[user@]dest_host:]file2

scp ./dm.zip root@64.227.153.83:/var/www/dmdailytricks.com

Destination

/var/www/dmdailytricks.com

My Zip is getting uploaded to the server using SCP command

Now change permission to 755
    change ownwership to www-data:www-data (Ubuntu)

chown www-data:www-data /path/to/file_or_directory

Now configure the database credentials with new one

Lets check where https://dmdailytricks.com/ is pointing


we will use ping tool

It is currently pointing to old server i.e 159.89.168.150

we will point to new server i.e 64.227.153.83

We will use DNS panel for this

Login to your domain panell

We have successfully pointed to new server

Now it will take some time usually 1min to 48hr

So keep checking in time if it points to new server or not

Lets check again with new ip

Still it is pointing to old ip we will check after some time

I hope you like the video

Subsribe the channel

Thank you :)
