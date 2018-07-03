# Local environment with Docker4Drupal

Docker4Drupal is an open-source project ([GitHub page](https://github.com/wodby/docker4drupal)) that provides pre-configured `docker-compose.yml` file from to spin up local environment on Linux, Mac OS X and Windows. 

## Requirements

* [Install Docker Compose](https://docs.docker.com/compose/install)

The Drupal stack consist of the following containers:

| Container     | Versions                | Service name    | Image                              |
| ------------- | ----------------------- | --------------- | ---------------------------------- |
| [Nginx]       | 1.15, 1.14, 1.13        | `nginx`         | [wodby/drupal-nginx]               |
| [Apache]      | 2.4                     | `apache`        | [wodby/php-apache]                 |
| [Drupal]      | 8, 7, 6                 | `php`           | [wodby/drupal]                     |
| [PHP-FPM]     | 7.x, 5.6, 5.3           | `php`           | [wodby/drupal-php]                 |
| [MariaDB]     | 10.3, 10.2, 10.1        | `mariadb`       | [wodby/mariadb]                    |
| [PostgreSQL]  | 10, 9.x                 | `postgres`      | [wodby/postgres]                   |
| [Redis]       | 4.0, 3.2                | `redis`         | [wodby/redis]                      |
| [Varnish]     | 4.1                     | `varnish`       | [wodby/drupal-varnish]             |
| [Node]        | 9, 8                    | `node`          | [wodby/node]                       |
| [Drupal node] | 1.0                     | `nodejs`        | [wodby/drupal-node]                |
| [Solr]        | 7.x, 6.x, 5.5, 5.4      | `solr`          | [wodby/drupal-solr]                |
| Elasticsearch | 6.x, 5.6, 5.5, 5.4      | `elasticsearch` | [wodby/elasticsearch]              |
| Kibana        | 6.x, 5.6, 5.5, 5.4      | `kibana`        | [wodby/kibana]                     |
| [Memcached]   | 1.5                     | `memcached`     | [wodby/memcached]                  |
| [Webgrind]    | 1.5                     | `webgrind`      | [wodby/webgrind]                   |
| [Blackfire]   | latest                  | `blackfire`     | [blackfire/blackfire]              |
| [Rsyslog]     | latest                  | `rsyslog`       | [wodby/rsyslog]                    |
| [AthenaPDF]   | 2.10.0                  | `athenapdf`     | [arachnysdocker/athenapdf-service] |
| [Mailhog]     | latest                  | `mailhog`       | [mailhog/mailhog]                  |
| [OpenSMTPD]   | 6.0                     | `opensmtpd`     | [wodby/opensmtpd]                  |
| Adminer       | 4.3                     | `adminer`       | [wodby/adminer]                    |
| phpMyAdmin    | latest                  | `pma`           | [phpmyadmin/phpmyadmin]            |
| Portainer     | latest                  | `portainer`     | [portainer/portainer]              |
| Traefik       | latest                  | `traefik`       | [_/traefik]                        |

Supported Drupal versions: 8 / 7 / 6

[Apache]: ../containers/apache.md
[AthenaPDF]: ../containers/athenapdf.md
[Blackfire]: ../containers/blackfire.md
[Drupal node]: ../containers/drupal-node.md
[Drupal]: ../containers/php.md
[Mailhog]: ../containers/mailhog.md
[MariaDB]: ../containers/mariadb.md
[Memcached]: ../containers/memcached.md
[Nginx]: ../containers/nginx.md
[Node]: ../containers/node.md
[OpenSMTPD]: ../containers/opensmtpd.md
[PHP-FPM]: ../containers/php.md
[PostgreSQL]: ../containers/postgres.md
[Redis]: ../containers/redis.md
[Rsyslog]: ../containers/rsyslog.md
[Solr]: ../containers/solr.md
[Varnish]: ../containers/varnish.md
[Webgrind]: ../containers/webgrind.md

[wodby/drupal-nginx]: https://github.com/wodby/drupal-nginx
[wodby/php-apache]: https://github.com/wodby/php-apache
[wodby/drupal]: https://github.com/wodby/drupal
[wodby/drupal-php]: https://github.com/wodby/drupal-php
[wodby/mariadb]: https://github.com/wodby/mariadb
[wodby/postgres]: https://github.com/wodby/postgres
[wodby/redis]: https://github.com/wodby/redis
[wodby/drupal-varnish]: https://github.com/wodby/drupal-varnish
[wodby/drupal-solr]: https://github.com/wodby/drupal-solr
[wodby/elasticsearch]: https://github.com/wodby/elasticsearch
[wodby/kibana]: https://github.com/wodby/kibana
[wodby/node]: https://github.com/wodby/node
[wodby/drupal-node]: https://github.com/wodby/drupal-node
[wodby/memcached]: https://github.com/wodby/memcached
[wodby/opensmtpd]: https://github.com/wodby/opensmtpd
[wodby/webgrind]: https://hub.docker.com/r/wodby/webgrind
[blackfire/blackfire]: https://hub.docker.com/r/blackfire/blackfire
[wodby/rsyslog]: https://hub.docker.com/r/wodby/rsyslog
[arachnysdocker/athenapdf-service]: https://hub.docker.com/r/arachnysdocker/athenapdf-service
[mailhog/mailhog]: https://hub.docker.com/r/mailhog/mailhog
[wodby/adminer]: https://hub.docker.com/r/wodby/adminer
[phpmyadmin/phpmyadmin]: https://hub.docker.com/r/phpmyadmin/phpmyadmin
[portainer/portainer]: https://hub.docker.com/r/portainer/portainer
[_/traefik]: https://hub.docker.com/_/traefik
