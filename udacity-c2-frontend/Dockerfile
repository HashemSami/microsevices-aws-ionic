## Build
FROM beevelop/ionic:latest AS ionic

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy app source
COPY . .

# RUN ionic build
RUN ionic build

# Bind the port that the image will run on
EXPOSE 8080

## Run
FROM nginx:alpine

#COPY www /usr/share/nginx/html
COPY --from=ionic  /usr/src/app/www /usr/share/nginx/html