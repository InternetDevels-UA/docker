# Selenium standalone server with Chrome browser
## To run this container with docker-compose.yml:
- copy docker-compose.yml 
- run next command inside folder with docker-compose.yml :
```bash
docker_compose up
```
## Additional settings 
### Memory limit
```bash
mem_limit: 2048m
```
If you need to set specific memory limit just uncomment this line and set value that you want.
By default container is able to use all machine memory.
### CPUs
```bash
cpuset: 0,1
```
You can additionally set what CPUs container will use. First CPU is 0, second is 1 and so on.
## Alternative way to run this container
Run next command:
```bash
docker run --restart=always --name=selenium_chrome -d -p 4444:4444 -v /dev/shm:/dev/shm selenium/standalone-chrome:2.52.0
```

