
<h1>Bắt đầu nhanh với Mysql-Server trên Linux</h1>

1. Cài đặt mysql-server

       sudo apt update
    
       sudo apt install mysql-server

3. Khởi động dịch vụ mysql

       sudo systemctl start mysql


4. Hoàn thành thiết lập bảo mật:

       sudo mysql_secure_installation


5. Mới cài đặt thì đăng nhập bằng lệnh với mật khẩu để trống:

       sudo mysql -u root -p

6. Đổi mật khẩu user root:

       ALTER USER 'root'@'localhost' IDENTIFIED BY 'V!7ASB)b3vu+eDDb';

7. Thao tác chạy, dừng, khởi động lại, xem trạng thái:

       sudo systemctl start mysql

       sudo systemctl stop mysql

       sudo systemctl restart mysql

       sudo systemctl status mysql

8. Tự động khởi động cùng hệ thống và tắt:

       sudo systemctl enable mysql

       sudo systemctl disable mysql

9. Xem danh sách cơ sở dữ liệu:

       SHOW DATABASES;

10. Sử dụng cơ sở dữ liệu:

        USE database_name;

11. Tạo cơ sở dữ liệu:

        CREATE DATABASE database_name;

12. Xóa cơ sở dữ liệu:

        DROP DATABASE database_name;

13. Thoát khỏi cơ sở dữ liệu:

        EXIT;

**Ngoài ra những câu query với cơ sở dữ liệu không nằm trong phạm vi của bài viết này**

<h1># Hướng dẫn cài đặt WordPress trên Ubuntu</h1>

1. Cài đặt Apache:

       sudo apt update
       sudo apt install apache2

2. Cài mysql như hướng dẫn trên:
3. 3 Cài đặt PHP:

       sudo apt install php libapache2-mod-php php-mysql


4. Khởi động lại Apache để áp dụng thay đổi

       sudo systemctl restart apache2

5. Đăng nhập vào mysql để tạo cơ sở dữ liệu cho wordpress

       sudo mysql -u root -p "password"

Tạo cơ sở dữ liệu:

    CREATE DATABASE mydatabase;
    CREATE USER 'myuser'@'localhost' IDENTIFIED BY 'mypassword';
    GRANT ALL PRIVILEGES ON mydatabase.* TO 'myuser'@'localhost';
    FLUSH PRIVILEGES;


6. Cài đặt wordpress:

       cd /tmp
       wget https://wordpress.org/latest.tar.gz
       tar -xzvf latest.tar.gz
       sudo mv wordpress /var/www/html/

7. Thay đổi quyền sở hữu thư mục cho người dùng và nhóm Apache:
  
       sudo chown -R www-data:www-data /var/www/html/wordpress

8. Sao chép tệp cấu hình mẫu và cài đặt cơ sở dữ liệu:

       cd /var/www/html/wordpress
       cp wp-config-sample.php wp-config.php
       nano wp-config.php

Ở bước này hãy sửa các thông tin về tên database, user, password, host cho phù hợp

Sau đó lưu lại tệp

Mở trình duyệt với địa chỉ là host vừa nhập, sau đó dùng giao diện trên web để tiến hành cấu hình tiếp

