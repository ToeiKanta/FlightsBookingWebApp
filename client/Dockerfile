FROM node:12

COPY . /client
WORKDIR /client

RUN yarn install
ENTRYPOINT ["yarn","serve"]
