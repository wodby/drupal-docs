# Redis

You can configure Redis via environment variables that listed at https://github.com/wodby/redis. See [Redis stack](https://cloud.wodby.com/stackhub/7548eb5a-c61b-4480-9f36-2501917692b3) for more details.

## Integration

### Drupal 8

Install [redis module](https://www.drupal.org/project/redis) and enable redis integration under `[Instance] > Cache > Settings` page of Wodby dashboard to use it as an internal cache storage for Drupal. All required configuration already provided in [`wodby.settings.php` file](../drupal-settings.md).

### Drupal 7

Install [redis module](https://www.drupal.org/project/redis) to use it as an internal cache storage for Drupal. All required configuration already provided in [`wodby.settings.php` file](../drupal-settings.md).
