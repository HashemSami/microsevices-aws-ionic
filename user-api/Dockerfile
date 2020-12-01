# We reduced many lines of code to set up NodeJS by abstracting all of it into a base image
FROM hashemfay/base-image-node:latest

# Create app directory
WORKDIR /user/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy app source
COPY . .

RUN npm build

# Bind the port that the image will run on
EXPOSE 8080

# Define the Docker image's behavior at runtime
CMD ["node", "./www/server.js"]