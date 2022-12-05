# Docker & Symfony + MySQL  
Install a dockerized dev environnement based on: PHP8, Apache / Nginx, NodeJS & Yarn, MailDev, PHPMyAdmin / PGAdmin, MySQL / PostgreSQL, and Symfony CLI.   
Additional services : PHPMyAdmin / PGAdmin, MailDev  

---  

## Installation  
  1. Clone this Git repository :  
  `git clone https://github.com/stuntmanmike87/docker_sf6.git`  

  2. Duplicate file .env-sample then rename it to .env :  
  `cd docker_sf`  
  `cp .env-sample .env`  
  Change this file by typing your own settings  

  3. Build the Docker containers :  
  `docker-compose up -d --build`  

  4. Open a new tab on your terminal, then get the console of your main container :  
  `docker-compose exec php /bin/bash`  

  5. Test Symfony CLI :  
  `symfony check:requirements`  

---  

## Install a Symfony project :  
Every command is executed in your main container terminal :  
- `php bin/console […]`  
- `git […]`  
- `npm […]`  
- `yarn […]`  

**Note : remove file delete-me.txt before init a SF project **  
`rm delete-me.txt`  

- Latest : `symfony new --full .`  
- LTS : `composer create-project symfony/website-skeleton:"^5.4" .`  
