# TODO:

Use https://github.com/zeromq/pyzmq with FastAPI to create distributed applicaation montitoring. This is just an exercise - DO NOT use in production.


1. Create multiple docker images with "microservices" and one docker compose file to run them all [DONE].
2. Send CPU and MEM usage data to one central service which will display received data [DONE].

Check out receiver service here: https://github.com/dghy/zeromq_sockets_receiver


<img width="1790" alt="Screenshot 2021-03-25 at 10 53 18" src="https://user-images.githubusercontent.com/16268031/112456193-ccf34480-8d5a-11eb-9e5c-0a88999e1ff5.png">


## To start the senders:
0. Docker and docker-compose are required.
1. Create .env file in the same dir as docker-compose.yaml
2. Type commands:
```
docker-compose up -d backend_1

docker-compose up -d backend_2

docker-compose up -d backend_3
```

3. After services build, make sure that receiver service is running (https://github.com/dghy/zeromq_sockets_receiver) then access http://localhost:8000/stats for performance graph. 
