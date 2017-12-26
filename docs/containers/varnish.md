# Varnish

You can configure Redis via environment variables that listed at https://github.com/wodby/varnish. 

Varnish ignores the following GET parameters for cache id generation:

```
utm_source
utm_medium
utm_campaign
utm_content
gclid
cx
ie
cof
siteurl
```

## Integration

### Drupal 8

Read [this article](https://wunderkraut.se/blogg/purge-cachetags-varnish) to learn how to use Varnish with Drupal 8.

### Drupal 7

1. Install and enable varnish module (use the dev version). All required configuration for this module already provided in [`wodby.settings.php` file](../drupal-settings.md)
2. Go to `Home » Administration » Configuration » Development` page of Drupal website and
3. Check Cache pages for anonymous users
4. Check Compress cached pages.
Check Aggregate and compress CSS files.
Check Aggregate JavaScript files.
Also, we recommend to install expire module to configure auto purge of pages when some content has been updated. After installation go to `Home » Administration » Configuration » System` and select External expiration at the "Module status" tab.
