# Home

Supported Drupal versions: 8 / 7 / 6

| Container | Description |
| --------- | ----------- |
| [Nginx] | Unlike traditional HTTP servers, [NGINX](http://nginx.org/) does not rely on threads to handle requests. Instead it uses a much more scalable event-driven (asynchronous) architecture. This architecture uses small, but more importantly, predictable amounts of memory under load. |
| [Apache] | [Apache HTTP server](https://httpd.apache.org/) is the most popular web server, developed and maintained by an open community of developers under the auspices of the Apache Software Foundation. |
| [PHP] | Only 7.x mainline supported. PHP container comes with a handful of most popular extensions and also includes [Drush](http://drush.org/) and [Drupal Console](https://drupalconsole.com/). |
| [MariaDB] | [MariaDB](http://mariadb.org/) is a [drop-in replacement](https://en.wikipedia.org/wiki/Drop-in_replacement) of MySQL and one of the most popular database servers in the world. It’s made by the original developers of MySQL and guaranteed to stay open source. |
| [PostgreSQL] | [PostgreSQL](http://postgres.org), often simply Postgres, is an object-relational database management system with an emphasis on extensibility and standards compliance.|
| [Redis] | [Redis](https://redis.io/) is an open source, in-memory data structure store, used as a database, cache and message broker. Also known as memcached on steroids. The easiest way to improve performance of Drupal is to connect an external in-memory cache storage. |
| [Memcached] | [Memcached](https://memcached.org) is a general-purpose distributed memory caching system. It is often used to speed up dynamic database-driven websites by caching data and objects in RAM to reduce the number of times an external data source must be read. |
| [OpenSMTPD] | [OpenSMTPD](https://www.opensmtpd.org/) is free and simple mail transfer agent, implementation of the server-side SMTP protocol as defined by RFC 5321, with some additional standard extensions. |
| [Varnish] | [Varnish](http://varnish-cache.org/) is a web application accelerator also known as a caching HTTP reverse proxy. You install it in front of any server that speaks HTTP and configure it to cache the contents. Varnish Cache is really, really fast. It typically speeds up delivery with a factor of 300 - 1000x, depending on your architecture. |
| [Solr] | [Solr](http://lucene.apache.org/solr/) is a search engine built on Apache Lucene. Its major features include full-text search, hit highlighting, faceted search, real-time indexing, dynamic clustering, database integration. |
| [Drupal node] | Server app for the Node.js Integration Drupal module. https://www.drupal.org/project/nodejs. |
| [Node] | Light-weight node container to build your application's frontend. |
| [Mailhog] | [MailHog](https://github.com/mailhog/MailHog) is an email testing tool for developers. All outbound emails will be catched by Mailhog, you can view messages in the web UI and optionally release messages to real SMTP servers for delivery |
| [AthenaPDF] | [AthenaPDF](http://www.athenapdf.com/) is a drop-in replacement for wkhtmltopdf using Electron and Go. |
| [Blackfire] | Agent for profiling via [blackfire.io](https://blackfire.io/docs/reference-guide/faq). |
| [Webgrind] | [Webgrind](https://github.com/jokkedk/webgrind) is a Xdebug profiling web frontend in PHP. |
| [Rsyslog] | [Rsyslog](http://www.rsyslog.com/) is an enhanced multi-threaded syslogd used to stream applications logs. |
| PhpMyAdmin | [phpMyAdmin](https://www.phpmyadmin.net/) is a free software tool written in PHP, intended to handle the administration of MySQL over the Web. |
| Adminer | [Adminer](https://www.adminer.org/) is a simplified alternative to PhpMyAdmin. |

[Apache]: containers/apache.md
[AthenaPDF]: containers/athenapdf.md
[Blackfire]: containers/blackfire.md
[Mailhog]: containers/mailhog.md
[MariaDB]: containers/mariadb.md
[Memcached]: containers/memcached.md
[Nginx]: containers/nginx.md
[Drupal node]: containers/drupal-node.md
[Node]: containers/node.md
[OpenSMTPD]: containers/opensmtpd.md
[PHP]: containers/php.md
[PostgreSQL]: containers/postgres.md
[Redis]: containers/redis.md
[Rsyslog]: containers/rsyslog.md
[Solr]: containers/solr.md
[Varnish]: containers/varnish.md
[Webgrind]: containers/webgrind.md
