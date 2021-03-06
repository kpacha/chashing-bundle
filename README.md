Consistent hashing Symfony 2 bundle
=============================

[![Latest Stable Version](https://poser.pugx.org/eso/chashing-bundle/v/stable.png)](https://packagist.org/packages/eso/chashing-bundle) [![Build Status](https://api.travis-ci.org/entering/chashing-bundle.png?branch=master)](https://travis-ci.org/entering/chashing-bundle) [![Scrutinizer Quality Score](https://scrutinizer-ci.com/g/entering/chashing-bundle/badges/quality-score.png?s=0cda11526319371e090f2650570c13f361a95c52)](https://scrutinizer-ci.com/g/entering/chashing-bundle/)

What does this bundle do?
------------

Simple Symfony 2 bundle that implements consistent hashing, one of the most know use case is in distributed caching, but can be used in other cases like shard data across multiple databases/servers.

The source code of this bundle is base Flexihash (https://github.com/pda/flexihash/).

You can read more about consistent hashing in: http://www.tomkleinpeter.com/2008/03/17/programmers-toolbox-part-3-consistent-hashing/

Pull requests are welcome (see Developing section).

Improves/changes
------------

There are some improves/changes to Flexihash:
* Used PHPunit instead of Simpletest;
* Added several validations on adding/removing targets;
* Improved performance of lookup:
  * Used isset instead of in_array (https://github.com/pda/flexihash/blob/master/classes/Flexihash.php#L190);
  * Removed unecessary count's (https://github.com/pda/flexihash/blob/master/classes/Flexihash.php#L196);
  * Simplified the if's inside foreach leading to huge performance improvements  (https://github.com/pda/flexihash/blob/master/classes/Flexihash.php#L181);
* Break the main class in two, one main class and one holding data and methods related to tagerts;
* 100% code coverage;

Documentation
------------

[Index](https://github.com/entering/chashing-bundle/blob/master/Resources/doc/index.md)

Installation
------------

Installation instructions are located in [documentation](https://github.com/entering/chashing-bundle/blob/master/Resources/doc/installation.md).

License
------------

This bundle is under the MIT license. See the complete license in:

```
Resources/meta/LICENSE
```
