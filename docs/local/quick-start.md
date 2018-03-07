# Quick start

!!! danger "Persistence of database data":
    You will lose MariaDB / PostgreSQL data if you run `docker-compose down`. Instead use `docker-compose stop` to stop containers. Alternatively, you can use a manual volume for mariadb data (see compose file), this way your data will always persist. 

There are 2 options how to use docker4drupal – you can either run [vanilla](https://en.wikipedia.org/wiki/Vanilla_software) Drupal from the image or mount your own Drupal codebase:

## Option 1: Run Vanilla Drupal from Image

1. Clone [docker4drupal repository](https://github.com/wodby/docker4drupal) and switch to the [latest stable tag](https://github.com/wodby/docker4drupal/releases) or download/unpack the source code from the [latest release](https://github.com/wodby/docker4drupal/releases)
2. Optional: for Drupal 7 or 6 comment out corresponding `DRUPAL_TAG` and `NGINX_TAG` in `.env` file
4. [Configure domains](domains.md)
3. From project root directory run `docker-compose up -d` or `make up` to start containers 
5. That's it! Proceed with Drupal installation at http://drupal.docker.localhost:8000. Default database user, password and database name are all `drupal`, database host is `mariadb`
6. You can see status of your containers and their logs via portainer: http://portainer.drupal.docker.localhost:8000

## Option 2: Mount my Drupal Codebase

1. Download `docker-compose.yml`, `.env` and (optionally) `docker.mk` files from the [latest stable release](https://github.com/wodby/docker4drupal/releases) to your Drupal project root
2. Optional: for Drupal 7 or 6 comment out corresponding `PHP_TAG` and `NGINX_TAG` in your `.env` file
3. Optional: rename `docker.mk` to `Makefile` or include it in your existing Makefile, see available [make commands](make-commands.md) 
4. Ensure `NGINX_SERVER_ROOT` (or `APACHE_SERVER_ROOT`) is correct, by default set to `/var/www/html/web` for composer-based projects where Drupal is in `web` subdirectory
5. Ensure database credentials match in your `settings.php` as in `.env` file 
6. Optional: [import existing database](import-export.md)
7. Optional: uncomment lines in the compose file to run [redis](../containers/redis.md), [solr](../containers/solr.md), etc
8. [Configure domains](domains.md)
9. Optional: macOS users please read [this](docker-for-mac.md)
9. Optional: Windows users please read [this](permissions.md#windows)
9. Run containers: `docker-compose up -d` or `make up`
10. That's it! Your drupal website should be up and running at http://drupal.docker.localhost:8000
11. You can see status of your containers and their logs via portainer: http://portainer.drupal.docker.localhost:8000

You can stop containers by executing `docker-compose stop` or `make stop`

Have a problem? See [known issues](known-issues.md), submit a new issue on [GitHub](https://github.com/wodby/docker4drupal/issues) or ask [community on Slack](http://slack.wodby.com)

!!! tip "Permissions issues":
    To avoid potential problems with permissions between your host and containers please follow [these instructions](permissions.md)

!!! info "For macOS users":
    Docker for Mac volumes has poor performance. However there are workarounds, read more [here](docker-for-mac.md)

Feel free to adjust volumes and ports in the compose file for your convenience. 

