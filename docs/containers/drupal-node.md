# Drupal Node

Drupal node is a container with a server app for the [Node.js Integration Drupal module](https://www.drupal.org/project/nodejs). Do not confuse with just [Node](node.md)

You can configure Node.js via environment variables that listed at https://github.com/wodby/drupal-node 

Usage:

1. Install [Node.js Integration Drupal module](https://www.drupal.org/project/nodejs) on your site
2. Visit the Node.js configuration page under the Configuration menu, and enter the connection information for your Node.js server application. Set host to `node` (or `drupal-node` for local environment) and service key can be found on `[Instance] > Stack > Node.js`
