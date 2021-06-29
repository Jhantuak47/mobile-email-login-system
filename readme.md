<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>


## Laravel App Login with mobile no and OTP

This is a simple Application to Demonstrate How we can implement login functionality without using a password. 

- git clone https://github.com/ajay04/Laravel_login_otp.git
- cd Laravel_login_otp/
- composer install
- cp .env.example .env
- update Database name , username and password
- php artison migrate
- php artison serve  

## Laravel App Login with mobile no and OTP Using Docker

This Application can also run using docker.

Step-1: Install Docker and Docker-compose
- check version of docker and docker compose 
- use `docker -v` to check docker version {Docker version 20.10.2, build 20.10.2-0ubuntu1~18.04.2}
- use `docker-compose -v` to check docker-compose version {docker-compose version 1.21.2, build a133471}

Step-2: Go inside root directory. path/to/laravel_otp_docker/

Step-3: Run `docker-compose build`

Step-4: Run `docker-compose up -d`

Till now your composer is up and running.

Step-5: Go inside terminal or open terminal/cmd in root directory i,e. path/to/laravel_otp_docker/

Step-6: Run `docker-compose exec app /bin/bash`

Step-7: Run `composer install`.

- If you getting any error 
- Run `composer update`

Step-8: inside /bin/bash (at your present location wehre you are now) Run `php artisan key:gen`

Step-9: Run `php artisan migrate`
- If you getting any error
- Run `composer install`

## To Acess the application while running using docker.
- Open Web browser (chrome/firefox etc) and type http://localhost:9100/

## To install or run any command.
- If you wish to install any package. Go inside bash, path/to/your/laravel_otp_docker/ 
- Run `docker-compose exec app /bin/bash` 
- Then run composer require {package name}
- Running any command. Either you can go inside bash or you can run from terminal using below command
- Run `docker-compose exec app php artisan migrate:status` --> docker-compose exec app php artisan {any command}

## Stop/Down the running container.
- Run `docker-composer down`

## License

The project is open-source software licensed under the [MIT license](https://opensource.org/licenses/MIT).
