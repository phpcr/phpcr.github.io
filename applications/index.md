---
layout: default
title: Applications
---

This page tries to gather applications and libraries on top of PHPCR, as well as libraries that provide a PHPCR integration:

## Applications and Libraries

### Doctrine PHPCR-ODM

This variant of Doctrine provides an object-document mapper to store PHP 
objects in PHPCR. It provides built-in multilanguage support.

* Website: [www.doctrine-project.org](http://www.doctrine-project.org/projects/phpcr-odm.html)
* Vendor: [Doctrine Project](http://www.doctrine-project.org)
* Github: https://github.com/doctrine/phpcr-odm/

### Symfony Content Management Framework (CMF)

The CMF is built on top of Symfony2. It uses PHPCR-ODM as its default
persistence layer. It provides content editing, menu handling, a block system,
media management and utility functions such as a publish workflow.

* Website: [cmf.symfony.com](http://cmf.symfony.com)
* Vendor: [Symfony CMF](http://cmf.symfony.com)
* Github: https://github.com/symfony-cmf/

### Sulu 2.0

Sulu is an extensible CMS built directly on top of PHPCR. It comes with its own
editing concept inspired by the iOS finder.

* Website: [www.sulu.io](http://www.sulu.io)
* Vendor: [massiveart](http://www.massiveart.com)
* Github: https://github.com/sulu-cmf/sulu

### Togu

Togu is a new generation CMF built on top of Symfony CMF which allows to easily
create WYSIWYG websites. It uses PHPCR-ODM as its persistence layer.

* Website: [togu.io](http://togu.io)
* Github: https://github.com/togucms/ToguCMS

## Integrations

Hint: This list is not exhaustive. Check if your tools support PHPCR / 
PHPCR-ODM. If they don't, support is often simple to add, especially when
Doctrine ORM is already supported.

* [LiipImagineBundle](https://github.com/liip/LiipImagineBundle/)
* [PagerFanta](https://github.com/whiteoctober/pagerfanta)

## Framework Support

### Symfony2

The DoctrinePHPCRBundle integrates both PHPCR and PHPCR-ODM with the Symfony2
framework. It allows you to configure multiple sessions and can automatically
detect documents for PHPCR-ODM in bundles.

* Website: http://symfony.com/doc/master/cmf/bundles/phpcr_odm/introduction.html
* Vendor: [Doctrine Project](http://www.doctrine-project.org)
* Github: https://github.com/doctrine/DoctrinePHPCRBundle
