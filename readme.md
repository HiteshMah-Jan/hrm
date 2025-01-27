<p align="right">Sponsored by</p>
<p align="right"><a href="https://adevait.com/"><img src="https://adevait.com/img/logo.svg" alt="Adeva - Exclusive Developers Network" width="105" ></a></p>

# HR Management System for SMEs

## Description

HRM is a web based HR management system that covers the needs of SMEs for managing their employees and the recruitment process. The system is built on [Laravel 5.3](https://laravel.com/docs/5.3).

Available functions:

* Settings (General settings related to features that will be used in the system. It includes setting up document templates for later use.)
* PIM (Personal information management for employees and candidates.)
* Leave (Managing leave and defining holidays.)
* Time (Managing time logs and projects.)
* Recruitment (Managing recruitment reports.)
* Discipline (Defining disciplinary cases for inadequate behaviours.)

## Installation

The system is built on top of Laravel 5.3, so to proceed with the installation you will need a machine that complies with [Laravel's requirements](https://laravel.com/docs/5.3/installation). Follow the steps below to quickly set up the application.

1. Dedicate a domain/subdomain to the project and set up the virtual host accordingly.
2. On the command line, run `composer install` to install all dependencies, and then `composer dump` to autoload the needed files.
3. Create a database that will be used for the application purposes.
4. Copy the .env.example file on the root of the app to a new file named .env. Update the database fields according to your local setup and set the APP_KEY.
5. On the command line, run `php artisan key:generate`
6. Still in the command line, run `php artisan migrate` to create the needed tables. 
7. Possible errors: if the app is not working at this point, there are probably some permission errors. 
    * Check `/storage` permissions - the storage folder on the root of the app should be writable by the application. Make sure the permissions are set correctly.
    * Check `/bootstrap/cache` permissions - this folder should also be writable. Make sure the permissions are set correctly. 
8. At this point you should have the app up and running. Hit `yourdomain/register` to open the registration screen for creating an admin user. This is a one time setup and the credentials set here will be used for authenticating before using the system.

#### Docker installation
1. Install Docker and Docker Compose for the operating system of your choice.
2. Get into your project directory (`cd hrm`)
3. Build the docker containers using `docker-compose build --no-cache --pull --force-rm`
4. Run the containers using `docker-compose up -d`
5. Access the PHP container using `docker exec -it hrm_phpfpm_1 bash`
6. Run `composer install` to install of the composer dependencies.
7. Rename the docker example `.env` file using `cp .env.docker.example .env`
8. Run `php artisan key:generate` to generate an application key (APP_KEY)
9. Run `php artisan migrate` to run all of the migration
10. Add `127.0.0.1 hrm.local:8080` to your `/etc/hosts` file
11. Access the site using `hrm.local:8080` in your browser

## Contributing

We encourage you to contribute to HRM! Please check out the [Contributing guide](contributing.md) for guidelines about how to proceed. 

## License

HRM is released under the GPL v3 (or later) license.

## Support

Please direct any feedback to trajchevska@adevait.com.

## Our supporters
#### [BrowserStack](https://www.browserstack.com/): Hassle free web-based browser testing 
![Testing made easy with BrowserStack](https://raw.githubusercontent.com/adevait/hrm/master/public/images/browserstack-logo.png)
Trigger 1
