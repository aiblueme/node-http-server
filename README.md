# node-http-server

Minimal Node.js HTTP health-check server. Returns `OK` on any request.

## Stack

- Node.js 22 Alpine
- Ghost VPS / Docker

## Run Locally

    docker build -t node-http-server .
    docker run -p 3000:3000 node-http-server

## Deploy

    docker context use ghost
    docker build -t node-http-server .
    docker run -d --name node-http-server \
      -p 3000:3000 \
      --restart unless-stopped \
      node-http-server
