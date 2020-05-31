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
 
