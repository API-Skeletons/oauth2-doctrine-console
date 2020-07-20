Console Management of an Apigility Doctrine OAuth2 server
=========================================================

[![Gitter](https://badges.gitter.im/api-skeletons/open-source.svg)](https://gitter.im/api-skeletons/open-source)
[![Patreon](https://img.shields.io/badge/patreon-donate-yellow.svg)](https://www.patreon.com/apiskeletons)
[![Total Downloads](https://poser.pugx.org/api-skeletons/oauth2-doctrine-console/downloads)](https://packagist.org/packages/api-skeletons/oauth2-doctrine-console)


About
-----

This repository provides console routes to manage an [OAuth2 for Doctrine](https://github.com/API-Skeletons/oauth2-doctrine) server.


Installation
------------

Installation of this module uses composer. For composer documentation, please refer to [getcomposer.org](http://getcomposer.org/).

```sh
$ php composer.phar require api-skeletons/oauth2-doctrine-console "*"
```

Add this module to your application's configuration:

```php
'modules' => array(
   ...
   'ApiSkeletons\OAuth2\Doctrine\Console',
),
```

Console Routes
------------------

* `oauth2:client:create` Create a new client with or without a user.

* `oauth2:client:update` Update a client.

* `oauth2:client:delete` Delete a client.

* `oauth2:client:list` List all clients.

* `oauth2:scope:create` Create a scope.

* `oauth2:scope:update` Update a scope.

* `oauth2:scope:delete` Delete a scope.

* `oauth2:scope:list` List all scopes.

* `oauth2:public-key:create` Create the public/private key record for the given client.  This data is used to sign JWT access tokens.  Each client may have only one key pair.

* `oauth2:public-key:delete` Remove the key pair public key from a client.

* `oauth2:jwt:create` Create a new JWT for a given client.  This JWT will be used by an oauth2 connection requesting a grant_type of `urn:ietf:params:oauth:grant-type:jwt-bearer`.  Creating the JWT puts the oauth2 connection request's public key in place in the OAuth2 tables.

* `oauth2:jwt:delete` Delete a JWT.

* `oauth2:jwt:list` List all JWT.

For the connecting side of JWT see http://bshaffer.github.io/oauth2-server-php-docs/grant-types/jwt-bearer/

