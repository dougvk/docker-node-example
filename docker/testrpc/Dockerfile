FROM node:8.1

RUN apt-get update && apt-get -y upgrade

RUN apt-get install apt-transport-https

RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - \
      && echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list \
      && apt-get update && apt-get -y install yarn

WORKDIR /root
RUN npm install -g ethereumjs-testrpc

WORKDIR /app
