# Udagram Image Filtering Microservices Application

## Generel info

This project for the Udacity Cloud Devoleper Nanodegree. Where we took an existing monolith application (developed by Udacity), and deploy it as microservices in Kubernetes on AWS. Each microservice is running in its own Docker container, CI/CD pipeline was set up to deploy the containers to Kubernetes.

## Technologies

- nodejs
- express.js
- aws
- docker
- travis CI
- Kubernetes
- Ionic

## Setup

### Installation requirments

- If you don't have Nodejs installed yet. you'll need to [download Node.js](https://nodejs.org/en/download/) to be able to use this application.
- You'll also need to [install Ionic](https://ionicframework.com/docs/intro/cli) framework
- [Install docker](https://docs.docker.com/install/) to setup your docker environment.

### Installing project dependencies

- Clone this repo and install the dependencies by running `npm i` for the frontend and backend projects.
- Example:
  ```bash
   cd ./udacity-c3-restapi-feed
   npm install
  ```

### Setup the development server

- Configure your backend Endpoint by changing the apiHost value located in `./src/enviornments/enviornment.ts` to mach your server host.
- Open a terminal and run `ionic serve` on the frontend code, and another terminal for each backend service and run `npm run dev` on them.

### Setup Docker Environment

- Build the images: `docker-compose -f docker-compose-build.yaml build --parallel`
- Push the images: `docker-compose -f docker-compose-build.yaml push`
- Run the container: `docker-compose up`
