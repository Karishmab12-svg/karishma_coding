Instructions to Deploy

Generate a Self-Signed SSL Certificate:
```
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/nginx-selfsigned.key -out /etc/ssl/certs/nginx-selfsigned.crt
sudo openssl dhparam -out /etc/nginx/dhparam.pem 2048
```

2.	Install Nginx:
```
sudo yum update -y
sudo amazon-linux-extras install nginx1 -y
sudo systemctl start nginx
sudo systemctl enable nginx
```

3.	Configure Nginx:

	•	Save the nginx.conf content to /etc/nginx/nginx.conf.
	•	Save the index.html content to /usr/share/nginx/html/index.html.

	4.	Restart Nginx:
```
sudo systemctl restart nginx
```
