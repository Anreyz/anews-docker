FROM node:16.6.2-alpine3.14

# Not available for linux
# RUN apk add --no-cache libc6-compat

RUN npm i -g npm && npm -v

ENV NODE_ENV development
ENV PORT 3000

EXPOSE 3000

# Create app directory
RUN mkdir -p /client/src/app
WORKDIR /client/src/app

# Installing dependencies
COPY package*.json /client/src/app/
RUN npm install

# Copying source files
COPY . /client/src/app

# Building app
RUN npm run build
EXPOSE 3000

# Running the app
CMD "npm" "run" "dev"