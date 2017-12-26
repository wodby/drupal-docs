# Quick start

!!! danger "Persistence of database data":
    You will lose MariaDB / PostgreSQL data if you run `docker-compose down`. Instead use `docker-compose stop` to stop containers. Alternatively, you can use a manual volume for mariadb data (see compose file), this way your data will always persist. 

There are 2 options how to use docker4drupal – you can either run [vanilla](https://en.wikipedia.org/wiki/Vanilla_software) Drupal from the image or mount your own Drupal codebase:

## Option 1: Run Vanilla Drupal from Image (default)

1. Download `docker-compose.yml` file from the [latest stable release](https://github.com/wodby/docker4drupal/releases)
2. Optional: update _php_ and _nginx_ images tags if you want to run Drupal 7 or 6 (by default Drupal 8)
3. Run containers: `docker-compose up -d` (it may take some time for them to initialize) 
4. [Configure domains](domains.md)
5. That's it! Proceed with Drupal installation at http://drupal.docker.localhost:8000. Default database user, password and database name are all `drupal`, database host is `mariadb`
6. You can see status of your containers and their logs via portainer: http://portainer.drupal.docker.localhost:8000

## Option 2: Mount my Drupal Codebase

1. Download `docker-compose.yml` file from the [latest stable release](https://github.com/wodby/docker4drupal/releases) to your Drupal project root
2. Replace php image from `wodby/drupal` (PHP + vanilla Drupal) to `wodby/drupal-php` (just PHP)
3. Depending on your Drupal version use appropriate tags for _php_ and _nginx_ images
4. Update _nginx_ and _php_ volumes to `- ./:/var/www/html` to mount your codebase
4. Update `NGINX_SERVER_ROOT` (or `APACHE_SERVER_ROOT`) to `/var/www/html` unless your project is based on [composer template](https://github.com/drupal-composer/drupal-project)
5. Ensure your settings.php uses the same credentials as _mariadb_ service 
6. Optional: [import existing database](import-export.md)
7. Optional: uncomment lines in the compose file to run _redis_, _solr_, etc
8. [Configure domains](domains.md) 
9. Run containers: `docker-compose up -d`
10. That's it! Your drupal website should be up and running at http://drupal.docker.localhost:8000
11. You can see status of your containers and their logs via portainer: http://portainer.drupal.docker.localhost:8000

You can stop containers by executing:
```bash
docker-compose stop
```

Have a problem? See [known issues](known-issues.md), submit a new issue on [GitHub](https://github.com/wodby/docker4drupal/issues) or ask [community on Slack](http://slack.wodby.com)

!!! tip "Permissions issues":
    To avoid potential problems with permissions between your host and containers please follow [these instructions](permissions.md)

!!! info "For macOS users":
    Docker for Mac volumes has poor performance. However there are workarounds, read more [here](docker-for-mac.md)

Feel free to adjust volumes and ports in the compose file for your convenience. 

