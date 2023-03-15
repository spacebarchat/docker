## With NGINX and client (Which is under WIP)

Under fosscord-server-client-proxy there is a small project in experimental state. Which run the fosscord server, the fosscord-client with an reverse proxy and ssl in it.
You need to clone the repo.
`git clone https://github.com/fosscord/docker.git`
And then go to `fosscord-server-client-proxy`
Please adapt the following env variables to your need:

```
export POSTGRES_USER=postgres
export POSTGRES_PASSWORD=your-password
export POSTGRES_DATABASE=fosscord
export MAIL_CERTBOT=your-email
export NGINX_HOST=your-domain
```

To run it you need docker and docker-compose
`sudo docker-compose -f docker-compose.prod.yaml up` or `sudo docker-compose -f docker-compose.prod.yaml up -d`
