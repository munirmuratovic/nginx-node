# Nginx - Node
## With SSL from Letsencrypt dockerized - done right way

Go to folder and run:
```sh
docker-compose up --build -d
```

To see all the processes running:
```sh
docker ps -a
```
On the left side find container_id of nginx, and enter bash:
```sh
docker exec -it <container_id> bash
```

Finally, run certbot once to get SSL (change domain.com with your own domain name):
```sh
certbot --nginx -d domain.com -d www.domain.com
```

Via browser access your domain link like this:
```sh
domain.com/api
```

You will have SSL certificates now on your VPS hosting.