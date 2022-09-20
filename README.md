## Dockerized Jira 8.7.1 + MySQL 5.7 + Caddy HTTPS

Docker-Compose setup for running Atlassian Jira on Docker

* Jira 8.7.1
* MySQL 5.7
* Caddy 1.0.3

[Based on Atlassian's Base Jira Image](https://hub.docker.com/r/atlassian/jira-software)

### Setup

* Create .env file based on .env.example to configure enviroment variables
* Update Caddyfile in /config/caddy with your domain for SSL to work
* Launch docker-compose.yaml
* Enjoy :)

#### MySQL Config

MySQL Settings can be edited in /config/mysql/my.cnf
