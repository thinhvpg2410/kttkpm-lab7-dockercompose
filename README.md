# kttkpm-lab7-dockercompose

## Part 2
### 1. Docker compose nginx 
- Tạo file `docker-compose.yml` gồm các thông tin về service nginx
![img.png](Evidences/PART2/Part2_nginx/img_nginx_yml.png)
- Tạo file `nginx.conf` chứa config của nginx
![img.png](Evidences/PART2/Part2_nginx/img_nginx_conf.png)
- Tạo file `index.html` cơ bản trong thư mục `html` `html/index.html`
![img.png](Evidences/PART2/Part2_nginx/img_html.png)
- `docker compose up -d`: build các services trong `docker-compose.yml`
![img.png](Evidences/PART2/Part2_nginx/img_docker-compose-build.png)
- Truy cập vào localhost với port 8080 [localhost:8080]()
![img.png](Evidences/PART2/Part2_nginx/img_result.png)
### 2. Chạy MySQL với Docker Compose
- Tạo `docker-compose.yml`. 
  - Trong đó sử dụng mysql phiên bản 8.0
  - Gán các biến môi trường
    + MYSQL_ROOT_PASSWORD: sapassword | root password
    + MYSQL_DATABASE: mydb  tên database
    + MYSQL_USER: user | username
    + MYSQL_PASSWORD: password | password
  - Ánh xạ port 3309 của host vào 3306 (port măặc định cuủa mysql) trong container
![img.png](Evidences/PART2/Part2_mysql/img_mysql_yml.png)
- `docker compose up -d`: build các services trong `docker-compose.yml`
![img.png](Evidences/PART2/Part2_mysql/img_docker_compose_build.png)
- Sử dụng MySQL Workbench hoặc heidiSQL tạo connection với mysql. Như duưới hình sử dụng MySQL workbench để Test Connection đến db 
![img.png](Evidences/PART2/Part2_mysql/img_mysql_connection_test.png)
### 3. Chạy MySQL + PHPMyAdmin với Docker Compose
- Tạo `docker-compose.yml`. 
  -  Dựa vào docker-compose.yml của mysql phía trên, bổ sung thêm service PHPMyAdmin.
  - Trong đó có biến depends_on: mysql tức là phụ thuộc vào image mysql phía trên
  - Gán các biến môi trường
    + PMA_HOST: Giá trị `mysql` là tên của service/image MySQL trong file `docker-compose.yml`, phpMyAdmin sẽ kết nối đến MySQL thông qua tên này thay vì địa chỉ IP
    + MYSQL_ROOT_PASSWORD: Mật khẩu root của MySQL
![img.png](Evidences/PART2/Part2_mysql_phpmyadmin/img_pma_mysql_yml.png)
- `docker compose up -d`: build các services trong `docker-compose.yml`
![img.png](Evidences/PART2/Part2_mysql_phpmyadmin/img_docker_compose_build.png)
- 
![img.png](Evidences/PART2/Part2_mysql_phpmyadmin/img_result.png)

### 4. Chạy ứng dụng Node.js với Docker Compose

- `npm init -y`: khởi tạo 1 ứng dụng node.js
![img.png](Evidences/PART2/Part2_nodejs/img_nodejs_init.png)
- `npm i express`: cài đặt express
![img.png](Evidences/PART2/Part2_nodejs/img_install_express.png)
- Tạo 1 file server.js đơn giản
![img.png](Evidences/PART2/Part2_nodejs/img_serverjs.png)
- Tạo Dockerfile
![img_1.png](Evidences/PART2/Part2_nodejs/img_Dockerfile.png)
- `docker compose up -d`: build các services trong `docker-compose.yml`
![img.png](Evidences/PART2/Part2_nodejs/img_build.png)
-
![img.png](Evidences/PART2/Part2_nodejs/img_result.png)


