# Drupal multi-site 

You can deploy your existing multi-site Drupal application as separate application instances. You will need to specify `Site directory` on the 2nd step of new application deployment form. For example if you have a directory `sites/my-drupal-site/*` you should specify `my-drupal-site`. This directory will be used to locate `settings.php` file and files directory. Also, [`sites.php` file](drupal-settings.md) will be created automatically inside `sites/` with mapping of all domains attached to this instance.
