# docker_ch
 Default bridge network_
 This folder contains Dockerfile of flask and redis._
 Command to run :_
 docker build -t redisimage /redis_
 docker build -t  flaskiamge ._
 docker run --name redis-server -it -d redisimage_
 docker run --name flaskapp -it -d flaskimage_
 
 Change app.py_
 replace host value with ip address of redis container_
 cache = redis.Redis(host='172.17.0.2', port=6379)_
 
