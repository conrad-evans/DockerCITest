FROM node:alpine as base

WORKDIR /app

COPY ./package.json .
COPY ./yarn.lock .

# tests env
FROM base as test

RUN yarn test
CMD [ "echo", "DONE" ]

# dev env
FROM base as dev

CMD [ "npm", "start" ]