# sub-web-modify
肥羊的订阅转换前端，直接在vercel.com部署即可
## 效果预览：
![avatar](https://raw.githubusercontent.com/youshandefeiyang/webcdn/main/sub-web-modify.GIF)
### 使用方法：
建议使用Docker一键部署:
```
docker run -d --restart always -p 8090:80 --name sub-web-modify youshandefeiyang/sub-web-modify
```
或使用docker compose
```yaml
name: sub-web-modify
services:
    sub-web-modify:
        restart: always
        privileged: false
        ports:
            - 8090:80
        container_name: sub-web-modify
        image: youshandefeiyang/sub-web-modify
```
运行docker compose: `docker compose up -d`

访问地址举例:
```
http://192.168.10.1:8090/?backend=https://url.v1.mk
```
