FROM node:alpine as base

WORKDIR /app

COPY ./package.json .
COPY ./yarn.lock .

# tests env
# FROM base as test

# RUN yarn install --froozen-lockfile

# COPY . .
# CMD [ "yarn", "run", "dev" ]

# dev env
FROM base as dev

RUN yarn install
COPY . .

CMD [ "yarn", "start" ]