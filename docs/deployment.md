# Deployment 

## Vanilla Drupal (no deployment)

For demo purposes and simple Drupal installations you can use Vanilla Drupal deployment option. In this case Drupal code that comes with the Docker image will be used. In case of changes all data made to your codebase will persist but there will be no versions control.

## Deployment with git

We recommend using [Composer](https://getcomposer.org/) to manage dependencies in your repository:

1. Fork [our boilerplate](https://github.com/wodby/drupal-composer) or use the original [composer template for Drupal](https://github.com/drupal-composer/drupal-project)
2. Create `wodby.yml` in repository root (our boilerplate already has it) with the following content:
  ```yml
  pipeline:
    - name: Install dependencies
      type: command
      command: composer install --no-interaction --optimize-autoloader
      directory: $APP_ROOT
  ```
3. On the 3rd step of new application deployment form:
    * Specify `web` in `Codebase dir` (default name of subdir with Drupal's codebase) 
    * Make sure git branch matches to your Drupal version

## Deployment from CI tool

See https://help.wodby.com/deployment/cicd

## Post-deployment scripts

You can perform some actions such as run a drush command after deployment by using [post-deployment scripts](https://help.wodby.com/deployment/post-deployment-scripts)

## Auto deployment via git hooks

See https://help.wodby.com/deployment/auto-deployment-from-git