# Bold  Review Analytics - Hub

This repository is just a hub to provide an environment for the project of the challenge, they are divided into 2 more repositories using git submodules
- (Backend)[https://github.com/davibusanello/bold-analytics-api]: api & job using (php, laravel, mysql)
- (Frontend)[https://github.com/davibusanello/bold-analytics-app]: SPA using Vue.js

## Stack
* PHP 7.0 - Laravel for API & Job Schedule
* Node.js - Vue.js 2
* MySQL 5.7
* Apache
* Docker
* docker-compose


## Requirements
- Git Submodules of repository
- *(Docker)[https://docs.docker.com/engine/installation]
- *(docker-compose)[https://docs.docker.com/compose/install]

## How to use
- $ `git clone --recursive https://github.com/davibusanello/bold-analytics-hub.git`
- $ `cd bold-analytics-hub`
- $ `docker-compose build`
- $ `docker-compose up`  Use `-d` if wanna run in background and don't wanna see the log output.
