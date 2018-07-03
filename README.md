# Bold  Review Analytics - Hub

This repository is just a hub to provide an environment for the project of the challenge, they are divided into 2 more repositories using git submodules

- [Bold Commerce - Code Challenge Reference](https://github.com/bold-commerce/review-syncer)
- [Backend](https://github.com/davibusanello/bold-analytics-api): api & job using (php, laravel, mysql)
- [Frontend](https://github.com/davibusanello/bold-analytics-app): SPA using Vue.js

## Stack

- PHP 7.0 - Laravel for API & Job Schedule
- Node.js - Vue.js 2
- MySQL 5.7
- Apache
- Docker
- docker-compose

## Requirements

- This repository & their submodules
- **[Docker](https://docs.docker.com/engine/installation)**
- **[docker-compose](https://docs.docker.com/compose/install)**

## How to use

- $ `git clone --recursive https://github.com/davibusanello/bold-analytics-hub.git`
- $ `cd bold-analytics-hub`
- $ `docker-compose build`
- $ `docker-compose up`  Use `-d` if wanna run in background and don't wanna see the log output.
- $ `docker-compose exec api composer install` It will install the php packages required
- $ `docker-compose exec api php artisan migrate:fresh` It will run migrations in the database
- $ `docker-compose exec api php artisan shopify:review-sync` (optional) For manually sync the reviews (Job is running every 30 minutes)
- Access: [http://localhost](http://localhost) If you haven't changed any ports map in docker-compose.yml

## How to completely clean the docker environment when you have finished

- $ `docker-compose down` Stop all environment
- $ `docker-compose rm` Remove stopped containers
- $ `docker volume rm bold-analytics-hub_mysql-data` Will remove volume used by MySQL container & all data in the database
