# Domains

All domains attached to an HTTP server (Nginx or Apache) or Varnish will be added to Drupal's trusted hosts patterns. The domain marked as primary will be used as `-l` for drush cron run and will be used in drush aliases. Additionally, in Drupal 6 and 7 `$base_url` set to primary domain. The primary domain is available via environment variables `$WODBY_HOST_PRIMARY` and `$WODBY_URL_PRIMARY`. 

For more details please see Wodby documentation:

* [Domains management](https://help.wodby.com/apps/domains)
* [SSL](https://help.wodby.com/apps/ssl)
* [HSTS](https://help.wodby.com/infrastructure/hsts)