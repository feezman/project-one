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