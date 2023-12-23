# SQLi Lab 靶场Docker化

基于:
- SQLi Labs https://github.com/Audi-1/sqli-labs
- Alpine-based LAP Server with PHP extensions https://github.com/EvilFreelancer/alpine-apache-php5 


## 文件位置

- MySQL数据库 Dump -> dump/
- 靶场 php 文件位置 -> html/public

提示:  数据库文件存储在 ./database

## 靶场配置

靶场的http端口为**63520**

靶场的mysql端口为**63521**

数据库账号**root**

数据库密码**toor**

靶场的关键参数在https://github.com/muyuanlove/sqli-lab/blob/main/docker-compose.yml 和 https://github.com/muyuanlove/sqli-lab/blob/main/html/public/sql-connections/db-creds.inc **非必要不建议修改**。

如果你不想让靶场的数据库端口可以被远程访问请更改**docker-compose.yml**文件的第10行为

```
    - 127.0.0.1:63521:3306
```



### 启动靶场

```
git clone https://github.com/muyuanlove/sqli-lab.git
cd sqli-lab
docker-compose up -d
```

启动之后**等一分钟**连接服务器的63520端口 例如 http://49.0.240.90:63520/ 


### 停止靶场
如果您想停止容器而不将其从 docker 中删除： 
```
docker compose down
```
如果您想停止容器并将其从 docker 中删除： 

```
docker-compose rm -fsv
```

### 我的blog

www.muyuanhuck.cn
