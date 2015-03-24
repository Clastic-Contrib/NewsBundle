NewsBundle
==========

News Module for [Clastic](https://github.com/Clastic/Clastic).

About
-----

This bundle currently provides a News Module for the Clastic CMF.

Installation
------------

Installation is a quick:

1. Download NewsBundle using composer
2. Enable the Bundle
3. Import NewsBundle routing files
4. Update your database schema

### Step 1: Download NewsBundle using composer

Add NewsBundle by running the command:

``` bash
$ composer require clastic/news-bundle "dev-master"
```
### Step 2: Enable the bundle

Enable the bundle in the kernel:

``` php
<?php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...
        new Clastic\NewsBundle\ClasticNewsBundle(),
    );
}
```

### Step 3: Import NewsBundle routing files

In YAML:

``` yaml
# app/config/routing_admin.yml
clastic_news:
    resource: "@ClasticNewsBundle/Resources/config/backoffice_routing.xml"
```

### Step 4: Update your database schema

Now that the bundle is configured, the last thing you need to do is update your
database schema because you need tables to store your News data.

For ORM run the following command.

``` bash
$ php app/console doctrine:schema:update --force
```

Contributing
------------

> All code contributions - including those of people having commit access - must
> go through a pull request and approved by a core developer before being
> merged. This is to ensure proper review of all the code.
>
> Fork the project, create a feature branch, and send us a pull request.
>
> To ensure a consistent code base, you should make sure the code follows
> the [Coding Standards](http://symfony.com/doc/2.0/contributing/code/standards.html)
> which we borrowed from Symfony.
> Make sure to check out [php-cs-fixer](https://github.com/fabpot/PHP-CS-Fixer) as this will help you a lot.

If you would like to help, take a look at the [list of issues](https://github.com/Clastic-Contrib/NewsBundle/issues).

Author and contributors
-----------------------

Dries De Peuter - <dries@nousefreak.be> - <http://nousefreak.be>

See also the list of [contributors](https://github.com/Clastic-Contrib/NewsBundle/contributors) who participated in this project.

License
-------

This project is licensed under the MIT license.
