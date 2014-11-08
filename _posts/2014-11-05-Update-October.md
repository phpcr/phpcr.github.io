---
layout: default
title: Update October 2014
---

### Anouncements

The Jackalope team announces that upcoming version 1.2 will enter feature
freeze on the 19th of November and a beta is planned to be released before the
end of the month with the aim of a stable release before 2015. 

Any help would be greatly appreciated and there are issues with the label "1.2 Milestone"
open on the following trepositories:

- [jacaklope/jackalope](https://github.com/jackalope/jackalope/issues?q=is%3Aopen+is%3Aissue+milestone%3A1.2)
- [jackalope/jackalope-doctrine-dbal](https://github.com/jackalope/jackalope-doctrine-dbal/issues?q=is%3Aopen+is%3Aissue+milestone%3A1.2)
- [jackalope/jackalope-jackrabbit](https://github.com/jackalope/jackalope-jackrabbit/issues?q=is%3Aopen+is%3Aissue+milestone%3A1.2)

### Releases

The Symfony CMF had its third stable release this month, taking it to version 1.2, which included a new release of both
the [phpcr-odm](http://doctrine-phpcr-odm.readthedocs.org/en/latest) and the [DoctrinePHPCRBundle](https://github.com/doctrine/DoctrinePHPCRBundle).

- [PHPCR-ODM 1.2](http://www.doctrine-project.org/projects/phpcr-odm.html):
  Featuring improvements in handling transactions and collection performance.
- [DoctrinePHPCRBundle 1.2](https://github.com/doctrine/DoctrinePHPCRBundle):
  Including native support for the [phpcr
  shell](https://github.com/phpcr/phpcr-shell) as detailed in this [blog
  post](http://www.dantleech.com/post/2014/10/30/phpcr-shell-and-doctrinephpcrbundle-integration)
- [PHPCRShell alpha
  6](https://github.com/phpcr/phpcr-shell/releases/tag/1.0.0-alpha6): Full
  support for updating multi-value properties and minor fixes and improvements.

### Developments

- The [Jackalope FS](https://github.com/jackalope/jackalope-fs) is now an
  offical part of the Jackalope family and is edging closer to its first goal
  of feature parity with doctrine dbal, passing 90% of the
  [phpcr-api-tests](https://github.com/phpcr/phpcr-api-tests).
- [@danrot90](https://github.com/danrot) has confirmed that he will be implementing
  versioning on the [Jackalope Doctrine-Dbal](https://github.com/jackalope/jackalope-doctrine-dbal)
  PHPCR implementation as part of his thesis.
- A refactoring of Propel2 opens up the possiblity of PHPCR support: https://github.com/propelorm/Propel2/pull/795
