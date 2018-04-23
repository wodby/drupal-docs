# Domains Configuration

[Traefik](https://hub.docker.com/_/traefik) container used for routing. By default, we use port `8000` to avoid potential conflicts but if port `80` is free on your host machine just replace traefik's ports definition in the compose file.

By default `BASE_URL` set to `drupal.docker.localhost`, you can change it in `.env` file.

Add `127.0.0.1 drupal.docker.localhost` to your `/etc/hosts` file (some browsers like Chrome may work without it). Do the same for other default domains you might need from listed below:

| Service      | Domain                                          |
| ------------ | ----------------------------------------------- |
| nginx/apache | `http://drupal.docker.localhost:8000`           |
| pma          | `http://pma.drupal.docker.localhost:8000`       |
| adminer      | `http://adminer.drupal.docker.localhost:8000`   |
| mailhog      | `http://mailhog.drupal.docker.localhost:8000`   |
| solr         | `http://solr.drupal.docker.localhost:8000`      |
| nodejs       | `http://nodejs.drupal.docker.localhost:8000`    |
| node         | `http://front.drupal.docker.localhost:8000`     |
| varnish      | `http://varnish.drupal.docker.localhost:8000`   |
| portainer    | `http://portainer.drupal.docker.localhost:8000` |
| webgrind     | `http://webgrind.drupal.docker.localhost:8000`  |
