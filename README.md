# Docker Compose file for EFK with static website

Simple demo of a static website running in a container with logs collected by Fluentd and accessible in Kibana

Use this docker-compose as template for ElasticSearch - Fluentd - Kibana stack.

## EFK version

- ElasticSearch 7.8.1
- Kibana 7.8.1
- Fluentd 1.11

## Requirements
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## How to run
- Run `docker-compose build`
- Run `docker-compose up`

# How to access
Go to these sites:
- Demo site: [localhost:80](http://localhost:80) or [localhost](http://localhost)
- Kibana: [localhost:5601](http://localhost:5601)

# Kibana index pattern setup
Kibana need to setup an index pattern on first run. 
To do that, make sure you've generated some logs for Kibana to have a data to get. 

Then, create the index pattern referencing from the available indexes in the list.

Normally, there should be a **'fluent_xxxx'** index. Just type **'fluent'** and continue with the steps. 

Then you may now go to the **Discover** tab to view the logs.

Reload the app and see the updated results in Kibana. 

## How to quit
Run `docker-compose down`
