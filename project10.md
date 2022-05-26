# LOAD BALANCER SOLUTION WITH NGINX AND SSL/TLS

For this project,I created a domain using AWS and I connected the public IP of my load balancer in the domain record.

![DOMAIN](./images/DOMAIN.PNG)

`sudo apt update && sudo apt install nginx -y`

`sudo systemctl enable nginx && sudo systemctl start nginx`

`sudo systemctl status nginx`

![nginx](./project10/images/nginx.PNG)

Configure Nginx LB using Web Servers’ names defined in /etc/hosts

![localip](./project10/images/localip.PNG)


 `sudo vi /etc/nginx/sites-available/load_balancer.conf`

![config](./images/config.PNG)

`sudo systemctl restart nginx`

![zainion](./project10/images/zainion.PNG)

`sudo systemctl status snapd`

![snapd](./project10/images/snapd.PNG)

`sudo snap install --classic certbot`

![certboot](https://user-images.githubusercontent.com/102236877/170505331-3dfd6924-618a-426f-83ab-47bb5a4896e5.PNG)


`sudo certbot --nginx -d zainion.click -d www.zainion.click`

![cert](./project10/images/certbot%20cert.PNG)

`sudo ln -s /snap/bin/certbot /usr/bin/certbot`

![secured](./project10/images/secured.PNG)

`crontab -e`

![crontab](https://user-images.githubusercontent.com/102236877/170504517-26e9fec3-cd33-4e72-9a45-c6efd71d4b5f.PNG)






































