Symfony Entity Application
============

The "Symfony Entity Application" is a simple application to show how to create 
entity following the [Symfony Best Practices][1].

Requirements
------------

Require the [usual Symfony application requirements][2].

  * PHP 7.2.9 or higher
  * Mysql 8.0.21 or higher
  * Some PHP extensions
  * Composer
  * Symfony CLI

Installation
------------

Clone the [repository][3] on your computer:

```bash
$ git clone https://github.com/mickaelbober/symfony-entity.git symfony-entity
```

Configuring your `.env` file:

```bash
DATABASE_URL=mysql://symfony_entity:Azerty12@127.0.0.1:3306/symfony_entity?serverVersion=8.0
```

Create the database:

```bash
$ cd symfony-entity/
$ php bin/console doctrine:database:create
```

Apply migrations:

```bash
$ cd symfony-entity/
$ php bin/console doctrine:migrations:migrate
```

Composer
------------

[Download Composer][4] to install the `composer` binary on your computer and install
dependencies to the `./vendor` directory.

```bash
$ cd symfony-entity/
$ composer install
```

Symfony CLI
------------

[Download Symfony][5] to install the `symfony` binary on your computer. 

```bash
$ wget https://get.symfony.com/cli/installer -O - | bash
```

Run this command and access the application in your
browser at the given URL (<https://localhost:8000> by default):

```bash
$ cd symfony-entity/
$ symfony server:start
```

If you don't have the Symfony binary installed, run `php -S localhost:8000 -t public/`
to use the built-in PHP web server or [configure a web server][6] like Nginx or
Apache to run the application.

References
------------

 * [Data Mapper][7]
 * [Unit of Work][8]
 * [Annotations Reference][9]
 * [Types][10]
 * [Relation : Many-To-One][11]
 * [Relation : One-To-One][12]
 * [Relation : One-To-Many][13]
 * [Relation : Many-To-Many][14] 
 * [Databases and the Doctrine ORM][15]
 * [Openclassrooms : Tutorial][16]

[1]: https://symfony.com/doc/current/best_practices.html
[2]: https://symfony.com/doc/current/setup.html
[3]: https://github.com/mickaelbober/symfony-entity
[4]: https://getcomposer.org/download/
[5]: https://symfony.com/download
[6]: https://symfony.com/doc/current/setup/web_server_configuration.html
[7]: https://martinfowler.com/eaaCatalog/dataMapper.html
[8]: https://martinfowler.com/eaaCatalog/unitOfWork.html
[9]: https://www.doctrine-project.org/projects/doctrine-orm/en/2.6/reference/annotations-reference.html#annotations-reference
[10]: https://www.doctrine-project.org/projects/doctrine-dbal/en/2.6/reference/types.html#types
[11]: https://www.doctrine-project.org/projects/doctrine-orm/en/2.6/reference/association-mapping.html#many-to-one-unidirectional
[12]: https://www.doctrine-project.org/projects/doctrine-orm/en/2.6/reference/association-mapping.html#one-to-one-unidirectional
[13]: https://www.doctrine-project.org/projects/doctrine-orm/en/2.6/reference/association-mapping.html#one-to-many-bidirectional
[14]: https://www.doctrine-project.org/projects/doctrine-orm/en/2.6/reference/association-mapping.html#many-to-many-unidirectional
[15]: https://symfony.com/doc/current/doctrine.html#querying-for-objects-the-repository
[16]: https://openclassrooms.com/fr/courses/5489656-construisez-un-site-web-a-l-aide-du-framework-symfony-4/5517031-gerez-vos-donnees-avec-doctrine-orm
