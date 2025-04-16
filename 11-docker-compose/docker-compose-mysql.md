
# Docker compose example .

## 1. create a docker-compose.yml file for redis server   used to create caching 
      
   ``` bash
    docker-compose up -d
  ```
  ``` bash 
    docker exec -it my-redis-server redis-cli
  ``` 
  Connect to Redis CLI
    Run the Redis CLI inside the container:
  
  ``` bash 
  docker exec -it my-redis-server redis-cli
  ```
  Then, test it by running:
  ``` bash 
  PING
  ```
  If Redis is running, it should respond with:
   ``` bash
    PONG
  ```

## 2. apache server on rhel 9 - create a docker compose file for apache server  
  
  create a container with docker compose 
  ``` bash 
  docker compose up -d dcoker-compose.yml 
  ```

  access the apache server 
  ``` bash 
  curl localhost:8080
  ```

## 3. create mysql server with docker compose file 

1. Run the following command to access the MySQL CLI inside the container:
``` bash 
docker exec -it my-mysql-server mysql -u root -p
Then enter the root password (as defined in MYSQL_ROOT_PASSWORD in your docker-compose.yml file).
```
2. Using mysql CLI from Host Machine
If you have MySQL installed on your host, connect to the containerized MySQL:
``` bash 
mysql -h 127.0.0.1 -P 3306 -u root -p
```
Then enter the password.

3. Using docker-compose run (Alternative)
``` bash 
docker-compose run mysql mysql -u root -p
```
This starts a one-time MySQL session inside the container.
  
  




