<h1>Bắt đầu nhanh với Mysql-Server trên Linux</h1>

1. Cài đặt mysql-server

    sudo apt update

    sudo apt install mysql-server

2. Khởi động dịch vụ mysql

    sudo systemctl start mysql


3. Hoàn thành thiết lập bảo mật:

    sudo mysql_secure_installation


4. Mới cài đặt thì đăng nhập bằng lệnh với mật khẩu để trống:

    sudo mysql -u root -p

5. Đổi mật khẩu user root:

    ALTER USER 'root'@'localhost' IDENTIFIED BY 'V!7ASB)b3vu+eDDb';

6. Thao tác chạy, dừng, khởi động lại, xem trạng thái:

    sudo systemctl start mysql

    sudo systemctl stop mysql

    sudo systemctl restart mysql

    sudo systemctl status mysql

7. Tự động khởi động cùng hệ thống và tắt:

    sudo systemctl enable mysql

    sudo systemctl disable mysql

8. Xem danh sách cơ sở dữ liệu:

    SHOW DATABASES;

9. Sử dụng cơ sở dữ liệu:

    USE database_name;

10. Tạo cơ sở dữ liệu:

    CREATE DATABASE database_name;

11. Xóa cơ sở dữ liệu:

    DROP DATABASE database_name;

12. Thoát khỏi cơ sở dữ liệu:

    EXIT;

**Ngoài ra những câu query với cơ sở dữ liệu không nằm trong phạm vi của bài viết này**




