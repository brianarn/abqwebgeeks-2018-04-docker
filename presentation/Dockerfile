# Choosing the Alpine-based image will usually be smaller
# See https://hub.docker.com/_/node/ for a full list!
FROM node:9.10.1-alpine

# it me
MAINTAINER brianarn@gmail.com

# Set up a directory in which we'll work
WORKDIR /app

# Bring over our package file(s) and install modules first
# as it will improve image caching
COPY package*.json ./
RUN npm install

# Bring in the rest of the code
COPY . ./

# Start the main process!
CMD ["npm", "start"]
