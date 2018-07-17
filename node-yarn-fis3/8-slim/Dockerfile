FROM node:8-slim

MAINTAINER Nimo Chu <nimo.jser@gmail.com>

RUN apt-get update && apt-get install -y curl apt-transport-https && \
    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
    apt-get update && apt-get install -y yarn

RUN yarn config set registry https://registry.npm.taobao.org
RUN yarn global add fis3

WORKDIR /app
