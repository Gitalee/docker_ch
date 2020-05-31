# docker_ch
 Default bridge network 
 This folder contains Dockerfile of flask and redis. 
 Command to run : 
 docker build -t redisimage /redis 
 docker build -t  flaskiamge . 
 docker run --name redis-server -it -d redisimage 
 docker run --name flaskapp -it -d flaskimage 
 
 Change app.py 
 replace host value with ip address of redis container 
 cache = redis.Redis(host='172.17.0.2', port=6379) 
 
