# Containers 

## Overview

The Drupal stack consist of the following containers:

| Container    | Versions           | Resources        | Image                              |
| ------------ | ------------------ | ---------------- | ---------------------------------- |
| [Nginx]      | 1.15, 1.14, 1.13   | 4m               | [wodby/drupal-nginx]               |
| [Apache]     | 2.4                | 4m               | [wodby/php-apache]                 |
| [PHP-FPM]    | 7.x, 5.6, 5.3      | 32m              | [wodby/drupal-php]                 |
| [SSHD]       | -//-               | 4m               | [wodby/drupal-php]                 |
| [Crond]      | -//-               | 4m, 0.1; 512m, 1 | [wodby/drupal-php]                 |
| [MariaDB]    | 10.3, 10.2, 10.1   | 64m              | [wodby/mariadb]                    |
| [PostgreSQL] | 10, 9.x            | 64m              | [wodby/postgres]                   |
| [Redis]      | 4.0, 3.2           | 4m               | [wodby/redis]                      |
| [Memcached]  | 1.4                | 4m               | [wodby/memcached]                  |
| [Varnish]    | 4.1                | 8m               | [wodby/drupal-varnish]             |
| [Solr]       | 7.x, 6.x, 5.5, 5.4 | 256m             | [wodby/drupal-solr]                |
| [Node.js]    | 1.0                | 32m              | [wodby/drupal-node]                |
| [OpenSMTPD]  | 6.0                | 4m               | [wodby/opensmtpd]                  |
| [Webgrind]   | 1.5                | 16m              | [wodby/webgrind]                   |
| [Blackfire]  | latest             | 4m               | [blackfire/blackfire]              |
| [Rsyslog]    | latest             | 4m               | [wodby/rsyslog]                    |
| [AthenaPDF]  | 2.10.0             | 16m              | [arachnysdocker/athenapdf-service] |
| Mailhog      | latest             | 4m               | [mailhog/mailhog]                  |
| Adminer      | 4.3                | 8m               | [wodby/adminer]                    |
| phpMyAdmin   | latest             | 32m              | [phpmyadmin/phpmyadmin]            |

!!! note "Resources"
    Default values specified. `4m, 0.1; 512m, 1` means 4m RAM and 0.1 CPU requests; 512m RAM and 1 CPU limits. For more details visit https://help.wodby.com/stacks/configuration#resources

!!! note "SSHD and Crond"
    For Wodby environments we additionally spin up copies of PHP services with overridden commands to run cron and ssh daemons. All environment variables added to PHP-FPM service will be automatically passed to [SSHD] and [Crond] services.

## Configuration

Every container provides a set of environment variables for its customization. You can add and edit environment variables of a service from `[Instance] > Stack` page. https://help.wodby.com/stacks/configuration

[Apache]: apache.md
[AthenaPDF]: athenapdf.md
[Blackfire]: blackfire.md
[Mailhog]: mailhog.md
[MariaDB]: mariadb.md
[Memcached]: memcached.md
[Nginx]: nginx.md
[Node.js]: nodejs.md
[OpenSMTPD]: opensmtpd.md
[PHP-FPM]: php.md
[PostgreSQL]: postgres.md
[Redis]: redis.md
[Rsyslog]: rsyslog.md
[Solr]: solr.md
[Varnish]: varnish.md
[Webgrind]: webgrind.md

[SSHD]: ssh.md
[Crond]: cron.md

[wodby/drupal-nginx]: https://github.com/wodby/drupal-nginx
[wodby/php-apache]: https://github.com/wodby/php-apache
[wodby/drupal]: https://github.com/wodby/drupal
[wodby/drupal-php]: https://github.com/wodby/drupal-php
[wodby/mariadb]: https://github.com/wodby/mariadb
[wodby/postgres]: https://github.com/wodby/postgres
[wodby/redis]: https://github.com/wodby/redis
[wodby/drupal-varnish]: https://github.com/wodby/drupal-varnish
[wodby/drupal-solr]: https://github.com/wodby/drupal-solr
[wodby/drupal-node]: https://github.com/wodby/drupal-node
[wodby/opensmtpd]: https://github.com/wodby/opensmtpd
[wodby/memcached]: https://github.com/wodby/memcached
[wodby/webgrind]: https://hub.docker.com/r/wodby/webgrind
[blackfire/blackfire]: https://hub.docker.com/r/blackfire/blackfire
[wodby/rsyslog]: https://hub.docker.com/r/wodby/rsyslog
[arachnysdocker/athenapdf-service]: https://hub.docker.com/r/arachnysdocker/athenapdf-service
[mailhog/mailhog]: https://hub.docker.com/r/mailhog/mailhog
[wodby/adminer]: https://hub.docker.com/r/wodby/adminer
[phpmyadmin/phpmyadmin]: https://hub.docker.com/r/phpmyadmin/phpmyadmin
[portainer/portainer]: https://hub.docker.com/portainer/portainer
[_/node]: https://hub.docker.com/_/node
[_/traefik]: https://hub.docker.com/_/traefik
