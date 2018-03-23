# Quick start

!!! danger "Persistence of database data":
    You will lose MariaDB / PostgreSQL data if you run `docker-compose down`. Instead use `docker-compose stop` to stop containers. Alternatively, you can use a manual volume for mariadb data (see compose file), this way your data will always persist. 

There are 2 options how to use docker4drupal – you can either run [vanilla](https://en.wikipedia.org/wiki/Vanilla_software) Drupal from the image or mount your own Drupal codebase:

## Option 1: Run Vanilla Drupal from Image

1. Clone [docker4drupal repository](https://github.com/wodby/docker4drupal) and switch to the [latest stable tag](https://github.com/wodby/docker4drupal/releases) or download/unpack the source code from the [latest release](https://github.com/wodby/docker4drupal/releases)
2. Optional: for Drupal 7 or 6 comment out corresponding `DRUPAL_TAG` and `NGINX_TAG` in `.env` file
4. [Configure domains](domains.md)
3. From project root directory run `docker-compose up -d` or `make up` to start containers. Give it 10-20 seconds to initialize after the start
5. That's it! Proceed with Drupal installation at http://drupal.docker.localhost:8000. Default database user, password and database name are all `drupal`, database host is `mariadb`
6. You can see status of your containers and their logs via portainer: http://portainer.drupal.docker.localhost:8000

## Option 2: Mount my Drupal Codebase

1. Download `docker4drupal.tar.gz` from the [latest stable release](https://github.com/wodby/docker4drupal/releases) and unpack to your Drupal project root. If you choose to clone [the repository](https://github.com/wodby/docker4drupal) delete `docker-compose.override.yml` as it's used to deploy vanilla Drupal
2. Ensure `NGINX_SERVER_ROOT` (or `APACHE_SERVER_ROOT`) is correct, by default set to `/var/www/html/web` for composer-based projects where Drupal is in `web` subdirectory
3. Ensure database credentials match in your `settings.php` as in `.env` file 
4. [Configure domains](domains.md)
5. Optional: for Drupal 7 or 6 comment out corresponding `PHP_TAG` and `NGINX_TAG` in your `.env` file
6. Optional: [import existing database](import-export.md)
7. Optional: uncomment lines in the compose file to run [redis](../containers/redis.md), [solr](../containers/solr.md), [varnish](../containers/varnish.md), etc
8. Optional: macOS users please read [this](docker-for-mac.md)
9. Optional: Windows users please read [this](permissions.md#windows)
10. Run containers: `docker-compose up -d` or `make up` (see all [make commands](make-commands.md))
11. That's it! Your drupal website should be up and running at http://drupal.docker.localhost:8000
12. You can see status of your containers and their logs via portainer: http://portainer.drupal.docker.localhost:8000

!!! info "Optional files":
    If you don't need to [run multiple projects](multiple-projects.md) and don't use [docker-sync to improve volumes performance on macOS](docker-for-mac.md) feel free to delete `traefik.yml` and `docker-sync.yml` that come with the `docker4drupal.tar.gz`

You can stop containers by executing `docker-compose stop` or `make stop`

Have a problem? See [known issues](known-issues.md), submit a new issue on [GitHub](https://github.com/wodby/docker4drupal/issues) or ask [community on Slack](http://slack.wodby.com)

Feel free to adjust volumes and ports in the compose file for your convenience. 
