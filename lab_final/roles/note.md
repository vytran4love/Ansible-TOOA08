1. apt update
2. apt install -y nginx
3. systemctl start nginx.service
4. systemctl enable nginx.service
# Tạo thư mục lưu source web
5. mkdir -p /var/www/ten-domain
# Tạo nội dung file index
6. /var/www/ten_domain/index.html
# Tạo file vhost cho 2 website /etc/nginx/sites-available/ten_domain.conf
server {
       listen 80;
       listen [::]:80;
       server_name vinasupport-1.com;
       root /var/www/vinasupport_1;
       index index.html;
       location / {
               try_files $uri $uri/ =404;
       }
}
# Tạo symbolic link /etc/nginx/sites-enabled/
sudo ln -s /etc/nginx/sites-available/vinasupport-1.conf /etc/nginx/sites-enabled/vinasupport-1.conf
sudo ln -s /etc/nginx/sites-available/vinasupport-2.conf /etc/nginx/sites-enabled/vinasupport-2.conf
7. systemctl reload nginx