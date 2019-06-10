# Oracle-Task
Oracle-Task Apache Haproxy


1. cd apache
2. docker build -t apache .
3. cd ../haproxy
4. docker build -t haproxy .
5. docker run -d --net=host --restart always haproxy  
6. docker run -d -p 8080:8080 --restart always apache


# The command for test a https URL of the web application 10 000 times, with 10 concurrent connections.

1. ab -n 10000 -c 10 https://127.0.0.1/
