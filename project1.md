## Step1 

## Installing Apache and updating firewall

`sudo apt update`

![apt update](./images/apt-update.PNG)

`sudo apt install apache2`
![apache2 install](./images/apache2_install.PNG)

`sudo systemctl status apache2`
![apache status](./images/apache_status.PNG)

`curl -s http://169.254.169.254/latest/meta-data/public-ipv4`
![server-ip](./images/serverip.PNG)

`http://3.141.23.3:80`
![php staus](./images/apache_page.PNG)

## Step2  

## Installing mysql

`sudo apt install mysql-server`
![sql server](./images/mysql-server.PNG)

`sudo mysql`
![sql status](./images/sql-status.PNG)


`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';`
![security check](./images/security-check.PNG)

`mysql> exit`
![sql exit](./images/exit-sql.PNG)

`sudo mysql_secure_installation`
![secure sql](./images/secure-sql.PNG)

`mysql> exit`
![sql exit](./images/exit-sql.PNG)

## Step 3

## INSTALLING PHP

`sudo apt install php libapache2-mod-php php-mysql`
![sql exit](./images/install-php.PNG)

`php -v`
![sql exit](./images/php-status.PNG)



## Step 4

##  CREATING A VIRTUAL HOST FOR YOUR WEBSITE USING APACHE

`sudo mkdir /var/www/projectlamp`
![mkdir project lamp](./images/mkdir-projectlamp.PNG)

 `sudo chown -R $USER:$USER /var/www/projectlamp`
 ![chown project lamp](./images/chown-projectlamp.PNG)

 `sudo vi /etc/apache2/sites-available/projectlamp.conf`
 ![vi project lamp](./images/vi-projectlamp.PNG)

 `sudo ls /etc/apache2/sites-available`
 ![project lamp avalability](./images/projectlamp-ava.PNG)

 `sudo a2ensite projectlamp`
  ![ a2ensite project lamp](./images/a2ensite.PNG)

  `sudo apache2ctl configtest`
  ![ apachectl config](./images/apachectl-status.PNG)

  `sudo systemctl reload apache2`
   ![ reload ouput](./images/edit-vim.PNG)

   ## STEP 5 
   
   ##  ENABLE PHP ON THE WEBSITE

   `sudo vim /etc/apache2/mods-enabled/dir.conf`
   ![ vim apache](./images/edit-vim.PNG)

   `sudo systemctl reload apache2`
   ![ reload ouput](./images/edit-vim.PNG)

   `vim /var/www/projectlamp/index.php`
   ![ vim index](./images/vim-index.PNG)

   `sudo rm /var/www/projectlamp/index.php`
   ![ rm index](./images/rm-index.PNG)


