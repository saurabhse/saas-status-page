# saas-status-page

-- Application Prerequisites
You'll need at least the following installed on your server:

PHP 5.5.9, you'll also need ext-gd, ext-simplexml, mcrypt and ext-xml installed.
Composer and ext-mbstring,ext-tokenizer
APC or Redis for caching.
A database driver for your DB, such as MySQL, PostgreSQL or SQLite.
Git


-- Set the application key
Before going any further, we need to set the APP_KEY config. This is used for all encryption used in Cachet.

Shell
$ php artisan key:generate



-- Clone the repository:
Shell
$ git clone https://github.com/cachethq/Docker.git cachet-docker
$ cd cachet-docker
Edit the docker-compose.yml file to specify your ENV variables.

To build an image containing a specific Cachet release, change the cachet_ver ARG in the docker-compose.yml file:

YAML
cachet:
    build:
      context: .
      args:
        - cachet_ver=v2.3.10
Build and run the image:
Shell
$ docker-compose build
$ docker-compose up
Continue to configure Cachet in your web browser by navigating to your Docker host's IP address.
