# LOAD BALANCER SOLUTION WITH NGINX AND SSL/TLS

For this project,I created a domain using AWS and I connected the public IP of my load balancer in the domain record.

![DOMAIN](./images/DOMAIN.PNG)

`sudo apt update && sudo apt install nginx -y`

`sudo systemctl enable nginx && sudo systemctl start nginx`

`sudo systemctl status nginx`

![nginx](https://user-images.githubusercontent.com/102236877/170506579-2dd04f3c-dc92-4fa7-832b-6f38c089c0c8.PNG)


Configure Nginx LB using Web Servers’ names defined in /etc/hosts

![localip](https://user-images.githubusercontent.com/102236877/170506805-6825ee8c-c056-4cfa-b54e-7b8bb22a18eb.PNG)



 `sudo vi /etc/nginx/sites-available/load_balancer.conf`


![config](https://user-images.githubusercontent.com/102236877/170508026-90c2890d-a947-4e0c-af0b-e240d0bb9ce8.PNG)



`sudo systemctl restart nginx`

![zainion](https://user-images.githubusercontent.com/102236877/170506999-7291a2d9-b140-4a2d-befa-cb39dcb7da18.PNG)


`sudo systemctl status snapd`

![snapd](https://user-images.githubusercontent.com/102236877/170507370-a5e8bf0d-67c5-4074-84e8-9949c04d407c.PNG)


`sudo snap install --classic certbot`

![certboot](https://user-images.githubusercontent.com/102236877/170505331-3dfd6924-618a-426f-83ab-47bb5a4896e5.PNG)


`sudo certbot --nginx -d zainion.click -d www.zainion.click`

![certbot cert](https://user-images.githubusercontent.com/102236877/170507167-e05ed404-2e12-4ff1-bd68-b73ed72e19d2.PNG)


`sudo ln -s /snap/bin/certbot /usr/bin/certbot`

![secured](https://user-images.githubusercontent.com/102236877/170507555-d09ef23e-4667-42d4-bd44-af4dfdc0e570.PNG)


`crontab -e`

![crontab](https://user-images.githubusercontent.com/102236877/170504517-26e9fec3-cd33-4e72-9a45-c6efd71d4b5f.PNG)






































