# syntax=docker/dockerfile:1
FROM ubuntu:22.04 as builder

RUN apt update ; apt install -y curl git gnupg2 ; 
RUN curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list 
RUN curl -sL https://deb.nodesource.com/setup_18.x | bash - 
RUN apt update ; apt install -y yarn nodejs

RUN git clone https://github.com/spacebarchat/client.git -b legacy-v2 ; cd client
RUN cd client ; yarn install --network-timeout 100000 ; yarn build:web

FROM nginx:alpine

COPY --from=builder /client/web-build/ /usr/share/nginx/html/
