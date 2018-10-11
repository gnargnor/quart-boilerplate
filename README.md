# Quart App Boilerplate

This is boilerplate to get a Quart app up and running with docker-compose using hypercorn to serve and nginx as a 
reverse proxy.

## Prerequisites:
* Docker / Docker cli

## Getting Started:
To run locally:
* Clone the repo
* Create a `.env` file in the project root (you can leave it empty for now or put environment variables you want passed 
into your local environment inside for fun and profit)
* `> docker-compose build && docker-compose up`

## Dependencies
* [Quart](https://gitlab.com/pgjones/quart) - async flask replacement api
* [Hypercorn](https://hypercorn.org/) - async production server
* [nginx](https://nginx.org/en/) - reverse proxy

