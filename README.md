BLTed powered by Docksal
====
A base or sample Drupal 10 project defined by Acquia BLT and powered by Docksal.

## Getting Started

You must first have [Docksal installed](https://docs.docksal.io/getting-started/) and setup on your computer.

If you are using an Acquia Cloud production environment, follow instructions for [adding your Acquia Cloud API key](https://docs.docksal.io/tools/acquia-drush/) to the Docksal environment.

To use this project as a starter, clone this repo to your local machine.

From your terminal, go to the directory where you have cloned the repo and enter the following command:
```
fin init
```

A `composer.lock` file and a `salt.txt` file will be generated. These files, along with the docroot directory
should be committed to your repository. When complete, you can access the site by running:

```
fin drush uli
```

Additional [BLT documentation](https://docs.acquia.com/blt/) may be useful. You may also access a list of BLT commands by running:
```
fin blt
```

Additional [Docksal documentation](http://docs.docksal.io) may also be helpful. You can access a list of commands simply by running:
```
fin
```

## Working With a BLT Project

BLT projects are designed to instill software development best practices (including git workflows).

Acquia BLT Developer documentation includes an [example workflow](https://docs.acquia.com/blt/developer/dev-workflow/).

### Important Configuration Files

BLT uses a number of configuration (.yml or .json) files to define and customize behaviors. Some examples of these are:

* blt/blt.yml (formerly blt/project.yml prior to BLT 9.x)
* blt/local.blt.yml
* box/config.yml (if using Drupal VM)
* drush/sites (contains Drush aliases for this project)
* composer.json (includes required components, including Drupal Modules, for this project)

## Resources

* [BLT Documentation](https://docs.acquia.com/blt/)
* [BLT GitHub](https://github.com/acquia/blt)
* [Docksal Documentation](http://docs.docksal.io)
* [Docksal GitHub](https://github.com/docksal/docksal)

## Acquia Drupal Recommended Project

This is a project template providing a great out-of-the-box experience for new Drupal 10 projects hosted on Acquia. It is based on the [Drupal Recommended Project](https://github.com/drupal/recommended-project/tree/9.0.x), with the principal difference being the addition of several modules and packages that provide the best possible out-of-the-box experience for Acquia customers.

This project includes the following packages and configuration:
* [Drupal core](https://www.drupal.org/project/drupal)
* [Drupal core scaffold](https://www.drupal.org/docs/develop/using-composer/using-drupals-composer-scaffold)
* [Acquia CMS](https://github.com/acquia/acquia-cms-starterkit) (Starter kit)
* [Drush](https://github.com/drush-ops/drush) (Drupal CLI and development tool)
* [Asset Packagist](https://asset-packagist.org/) repository, package, and configuration
* [Acquia environment detection](https://github.com/acquia/drupal-environment-detector)
* [Acquia platform memcache settings](https://github.com/acquia/memcache-settings)
* Best practices for Drupal development, testing and project architecture

The Acquia CMS starter kit allows you to install Drupal for a given style of CMS:

| Name  | Description |
| ------------- | ------------- |
| Acquia CMS Enterprise Low-code  | The low-code starter kit will install Acquia CMS with Site Studio and a UIkit. It provides drag and drop content authoring and low-code site building. An optional content model can be added in the installation process.  |
| Acquia CMS Community  | The community starter kit will install Acquia CMS. An optional content model can be added in the installation process.  |
| Acquia CMS Headless  | The headless starter kit preconfigures Drupal for serving structured, RESTful content to 3rd party content displays such as mobile apps, smart displays and frontend driven websites (e.g. React or Next.js).  |

For instance, you can remove a provided package by running the following command and committing the changed `composer.json` and `composer.lock` to Git:
```
composer remove acquia/mysql56
```

## Next steps

After creating your project, you can add additional BLT plugins:

* [BLT Behat](https://github.com/acquia/blt-behat)
* [Acquia Drupal Spec Tool](https://github.com/acquia/drupal-spec-tool)

## Usage

To use the Acquia CMS run the command:
```
fin exec /var/www/vendor/bin/acms acms:install
```


# License

Copyright (C) 2020 Acquia, Inc.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License version 2 as published by the Free Software Foundation.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.

**BLT v13.0.0**
