# Containers 

## Overview

The Drupal stack consist of the following containers:

| Container     | Versions           | Resources        | Image                              |
| ------------- | ------------------ | ---------------- | ---------------------------------- |
| [Apache]      | 2.4                | 4m               | [wodby/php-apache]                 |
| [AthenaPDF]   | 2.10.0             | 16m              | [arachnysdocker/athenapdf-service] |
| [Blackfire]   | latest             | 4m               | [blackfire/blackfire]              |
| [Crond]       | -//-               | 4m, 0.1; 512m, 1 | [wodby/drupal-php]                 |
| [Drupal node] | 1.0                | 32m              | [wodby/drupal-node]                |
| [Mailhog]     | latest             | 4m               | [mailhog/mailhog]                  |
| [MariaDB]     | 10.3, 10.2, 10.1   | 64m              | [wodby/mariadb]                    |
| [Memcached]   | 1.5                | 4m               | [wodby/memcached]                  |
| [Nginx]       | 1.15, 1.14, 1.13   | 4m               | [wodby/drupal-nginx]               |
| [Node.js]     | 9.11, 8.11, 6.14   |                  | [wodby/node]                       |
| [OpenSMTPD]   | 6.0                | 4m               | [wodby/opensmtpd]                  |
| [PHP]         | 7.x, 5.6, 5.3      | 32m              | [wodby/drupal-php]                 |
| [PostgreSQL]  | 10, 9.x            | 64m              | [wodby/postgres]                   |
| [Redis]       | 4.0, 3.2           | 4m               | [wodby/redis]                      |
| [Rsyslog]     | latest             | 4m               | [wodby/rsyslog]                    |
| [Solr]        | 7.x, 6.x, 5.5, 5.4 | 256m             | [wodby/drupal-solr]                |
| [SSHD]        | -//-               | 4m               | [wodby/drupal-php]                 |
| [Varnish]     | 4.1                | 8m               | [wodby/drupal-varnish]             |
| [Webgrind]    | 1.5                | 16m              | [wodby/webgrind]                   |
| Adminer       | 4.3                | 8m               | [wodby/adminer]                    |
| phpMyAdmin    | latest             | 32m              | [phpmyadmin/phpmyadmin]            |

!!! note "Resources"
    Default values specified. `4m, 0.1; 512m, 1` means 4m RAM and 0.1 CPU requests; 512m RAM and 1 CPU limits. For more details visit https://help.wodby.com/stacks/configuration#resources

!!! note "SSHD and Crond"
    For Wodby environments we additionally spin up copies of PHP services with overridden commands to run cron and ssh daemons. All environment variables added to PHP-FPM service will be automatically passed to [SSHD] and [Crond] services.

## Configuration

Every container provides a set of environment variables for its customization. You can add and edit environment variables of a service from `[Instance] > Stack` page. https://help.wodby.com/stacks/configuration

[Apache]: apache.md
[AthenaPDF]: athenapdf.md
[Blackfire]: blackfire.md
[Crond]: cron.md
[Drupal node]: drupal-node.md
[Mailhog]: mailhog.md
[MariaDB]: mariadb.md
[Memcached]: memcached.md
[Nginx]: nginx.md
[Node.js]: node.md
[OpenSMTPD]: opensmtpd.md
[PHP]: php.md
[PostgreSQL]: postgres.md
[Redis]: redis.md
[Rsyslog]: rsyslog.md
[Solr]: solr.md
[SSHD]: ssh.md
[Varnish]: varnish.md
[Webgrind]: webgrind.md

[_/node]: https://hub.docker.com/_/node
[_/traefik]: https://hub.docker.com/_/traefik
[arachnysdocker/athenapdf-service]: https://hub.docker.com/r/arachnysdocker/athenapdf-service
[blackfire/blackfire]: https://hub.docker.com/r/blackfire/blackfire
[mailhog/mailhog]: https://hub.docker.com/r/mailhog/mailhog
[phpmyadmin/phpmyadmin]: https://hub.docker.com/r/phpmyadmin/phpmyadmin
[portainer/portainer]: https://hub.docker.com/portainer/portainer
[wodby/adminer]: https://hub.docker.com/r/wodby/adminer
[wodby/drupal-nginx]: https://github.com/wodby/drupal-nginx
[wodby/drupal-node]: https://github.com/wodby/drupal-node
[wodby/drupal-php]: https://github.com/wodby/drupal-php
[wodby/drupal-solr]: https://github.com/wodby/drupal-solr
[wodby/drupal-varnish]: https://github.com/wodby/drupal-varnish
[wodby/drupal]: https://github.com/wodby/drupal
[wodby/mariadb]: https://github.com/wodby/mariadb
[wodby/memcached]: https://github.com/wodby/memcached
[wodby/node]: https://github.com/wodby/node
[wodby/opensmtpd]: https://github.com/wodby/opensmtpd
[wodby/php-apache]: https://github.com/wodby/php-apache
[wodby/postgres]: https://github.com/wodby/postgres
[wodby/redis]: https://github.com/wodby/redis
[wodby/rsyslog]: https://hub.docker.com/r/wodby/rsyslog
[wodby/webgrind]: https://hub.docker.com/r/wodby/webgrind
