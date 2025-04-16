
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
  


  




