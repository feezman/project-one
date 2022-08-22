## Step1 

## Installing Apache and updating firewall

`sudo apt update`
![apt update](./images/apt-update.png)

`sudo apt install apache2`
![apache2 install](./images/apache2_install.png)

`sudo systemctl status apache2`
![apache status](./images/apache_status.png)

`curl -s http://169.254.169.254/latest/meta-data/public-ipv4`
![server-ip](./images/serverip.png)

`http://3.141.23.3:80`
![php staus](./images/apache_page.png)

## Step2  

## Installing mysql

`sudo apt install mysql-server`
![sql server](./images/mysql-server.png)

`sudo mysql`
![sql status](./images/sql-status.png)


`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';`
![security check](./images/security-check.png)

`mysql> exit`
![sql exit](./images/exit-sql.png)

`sudo mysql_secure_installation`
![secure sql](./images/secure-sql.png)

`mysql> exit`
![sql exit](./images/exit-sql.png)

## Step 3

## INSTALLING PHP

`sudo apt install php libapache2-mod-php php-mysql`
![sql exit](./images/install-php.png)

`php -v`
![sql exit](./images/php-status.png)



## Step 4

##  CREATING A VIRTUAL HOST FOR YOUR WEBSITE USING APACHE

`sudo mkdir /var/www/projectlamp`
![mkdir project lamp](./images/mkdir-projectlamp.png)

 `sudo chown -R $USER:$USER /var/www/projectlamp`
 ![chown project lamp](./images/chown-projectlamp.png)

 `sudo vi /etc/apache2/sites-available/projectlamp.conf`
 ![vi project lamp](./images/vi-projectlamp.png)

 `sudo ls /etc/apache2/sites-available`
 ![project lamp avalability](./images/projectlamp-ava.png)

 `sudo a2ensite projectlamp`
  ![ a2ensite project lamp](./images/a2ensite.png)

  `sudo apache2ctl configtest`
  ![ apachectl config](./images/apachectl-status.png)

  `sudo systemctl reload apache2`
   ![ reload ouput](./images/edit-vim.png)

   ## STEP 5 
   
   ##  ENABLE PHP ON THE WEBSITE

   `sudo vim /etc/apache2/mods-enabled/dir.conf`
   ![ vim apache](./images/edit-vim.png)

   `sudo systemctl reload apache2`
   ![ reload ouput](./images/edit-vim.png)

   `vim /var/www/projectlamp/index.php`
   ![ vim index](./images/vim-index.png)

   `sudo rm /var/www/projectlamp/index.php`
   ![ rm index](./images/rm-index.png)


