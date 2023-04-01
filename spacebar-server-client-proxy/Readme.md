## With NGINX and client (Which is under WIP)

Under spacebar-server-client-proxy there is a small project in experimental state. Which run the spacebar server, the spacebar client with an reverse proxy and ssl in it.
You need to clone the repo.
`git clone https://github.com/spacebarchat/docker.git`
And then go to `spacebar-server-client-proxy`
Please adapt the following env variables to your need:

```
export POSTGRES_USER=postgres
export POSTGRES_PASSWORD=your-password
export POSTGRES_DATABASE=spacebar
export MAIL_CERTBOT=your-email
export NGINX_HOST=your-domain
```

To run it you need docker and docker-compose
`sudo docker-compose -f docker-compose.prod.yaml up` or `sudo docker-compose -f docker-compose.prod.yaml up -d`
