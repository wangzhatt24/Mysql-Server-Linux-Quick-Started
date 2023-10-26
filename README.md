<h1>Bắt đầu nhanh với Mysql-Server trên Linux</h1>

1. Cài đặt mysql-server:
	   
	<code>sudo apt update</code>
	<code>sudo apt install mysql-server</code>

3. Khởi động dịch vụ mysql

	<code>sudo systemctl start mysql</code>

4. Hoàn thành thiết lập bảo mật:

	   <code>sudo mysql_secure_installation</code>


5. Mới cài đặt thì đăng nhập bằng lệnh với mật khẩu để trống:
	
	<code>sudo mysql -u root -p</code>

6. Đổi mật khẩu user root:

	 <code>ALTER USER 'root'@'localhost' IDENTIFIED BY 'V!7ASB)b3vu+eDDb';</code>

7. Thao tác chạy, dừng, khởi động lại, xem trạng thái:
	
	<code>sudo systemctl start mysql</code>
	<code>sudo systemctl stop mysql</code>
	<code> sudo systemctl restart mysql</code>
	<code>sudo systemctl status mysql</code>
	    
8. Tự động khởi động cùng hệ thống và tắt:

   <code>sudo systemctl enable mysql</code>
   <code>sudo systemctl disable mysql</code>

9. Xem danh sách cơ sở dữ liệu:

        <code>SHOW DATABASES;</code>

10. Sử dụng cơ sở dữ liệu:

         <code>USE database_name;</code>

11. Tạo cơ sở dữ liệu:
       
         <code>CREATE DATABASE database_name;</code>

12. Xóa cơ sở dữ liệu:

         <code>DROP DATABASE database_name;</code>

13. Thoát khỏi cơ sở dữ liệu:

         <code>EXIT;</code>

**Ngoài ra những câu query với cơ sở dữ liệu không nằm trong phạm vi của bài viết này**
