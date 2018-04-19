# Solr

You can configure Solr via environment variables that listed at https://github.com/wodby/solr

You can find URL to Solr admin UI from under Domains tab. See [Solr for Drupal stack](https://cloud.wodby.com/stackhub/07a28bf6-6772-4ac2-9d3e-6b097e9038ff) for more details.

## Creating solr core

!!! tip "TIP"
    Since 4.4.0 we automatically create a default solr core named `default` when no cores found.

Go to `[Instance] > Stack > Search Engine` page, copy and execute `Access container` on your host server to access the container with Solr. Copy `Create Solr core` command (edit to change core name), execute it inside of the container. Response `200` means that the core has been successfully created.

## Integration 

### Drupal 8

Install [Search API Solr module](https://www.drupal.org/project/search_api_solr). Go to `Home » Administration » Configuration » Search and metadata » Search API`, create a new core or edit the default one. In expanded `CONFIGURE SOLR BACKEND` field set specify:

```
HTTP protocol: http
Solr host: solr
Solr port: 8983
Solr path: /solr
Solr core: [NAME OF YOUR CORE]
```

### Drupal 7

Install [Search API Solr module](https://www.drupal.org/project/search_api_solr). Go to `Configuration » Search and metadata » Search API` and select Service class to "Solr service". In expanded settings field set specify:

```
HTTP protocol: http
Solr host: solr
Solr port: 8983
Solr path: /solr/[NAME OF YOUR CORE]
```
