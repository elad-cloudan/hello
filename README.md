# Minimal Node.js Hello World example

This repo contains a minimal hello world application written in Node. This repo will document the many ways you can deploy this application.

## Run locally

```bash
npm install
npm start
```

## Run in a container

```bash
docker build -t node-hello-world:latest .
docker run -it -p 8080:8080 --name node-hello-world node-hello-world:latest
```

## Pull from DockerHub 

```bash
docker pull doneladio/node-hello-world:latest
```

## To run in Jenkins pipeline
Simply use jenkinsfile located in the repo 
It will perform the following: 
1. Repo clone
2. Build
3. Snyk monitor (SCA scan)
4. Docker build and docker push

Make sure to update ${SNYK_TOKEN} credentials. 
