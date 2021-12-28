FROM node:14

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

# Running the app
CMD "npm" "run" "dev"
