# docker_ch
 Default bridge network<br />
 This folder contains Dockerfile of flask and redis.<br />
 Command to run :<br />
 docker build -t redisimage /redis<br /> 
 docker build -t  flaskiamge .<br /> 
 docker run --name redis-server -it -d redisimage<br /> 
 docker run --name flaskapp -it -d flaskimage<br />
 
 Change app.py<br />
 replace host value with ip address of redis container<br /> 
 cache = redis.Redis(host='172.17.0.2', port=6379)<br />
 
User Defined bridge network<br />
 This folder contains Dockerfile of flask and redis.<br />
 Command to run :<br />
 Create User Defined bridge :<br />
 docker network create my-app-bridge-net<br />
 Give replace value of name in docker-compose.yml with network name<br />
 name: my-app-bridge-net<br />
 docker-compose up -d .<br />
 docker build -t  flaskimage .<br /> 
 docker run --name flaskapp -it -d --network my-app-bridge-net flaskimage<br />
 
mysql and phpmyadmin<br /> 
mysql : Contains dockerfile of mysql<br /> 
Change password in Dockerfile<br /> 
Build image<br /> 
docker build -t mysqlimage .<br /> 
phpmyadmin: Contains dockerfile of phpmyadmin<br /> 
Build image<br /> 
docker build -t phpmyadmin_image .<br /> 
Run command<br /> 
docker run -it -d --name mysql-server mysqlimage<br /> 
docker run -it -d --name phpmyadmin-server --link mysql-server:db phpmyadmin_image<br /> 
