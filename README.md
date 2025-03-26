# kttkpm-lab7-dockercompose

## Part 2
### 1. Docker compose nginx 
- Tạo file `docker-compose.yml` gồm các thông tin về service nginx
![img.png](Evidences/Part2_nginx/img_nginx_yml.png)
- Tạo file `nginx.conf` chứa config của nginx
![img.png](Evidences/Part2_nginx/img_nginx_conf.png)
- Tạo file `index.html` cơ bản trong thư mục `html` `html/index.html`
![img.png](Evidences/Part2_nginx/img_html.png)
- `docker compose build -d`: build các services trong `docker-compose.yml`
![img.png](Evidences/Part2_nginx/img_docker-compose-build.png)
- Truy cập vào localhost với port 8080 [localhost:8080]()
![img.png](Evidences/Part2_nginx/img_result.png)
### 2. 
