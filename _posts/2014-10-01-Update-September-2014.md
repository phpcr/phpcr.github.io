---
layout: default
title: Update September 2014
---

This month has been interesting, a new Jackalope PHPCR implementation has been started.
[Jackalope FS](https://github.com/dantleech/jackalope-fs) will eventually add
a new tool to the PHPCR developers kit, also there has been lots of activity on the phpcr-odm in
preparation for the forthcoming 1.2 release.

### Talks

- [@willemjanz](https://twitter.com/willemjanz) and
  ([@dantleech](https://twitter.com/dantleech)) talked about PHPCR at the great
  [EZ/PHP Summer Camp](http://2014.ezsummercamp.com/Programme) in Croatia.

### Jackalope

- Open [pull request](https://github.com/jackalope/jackalope/pull/245) for moving the implementation
  agnostic node validation code from the [doctrine-dbal](https://github.com/jackalope/jackalope-doctrine-dbal)
  implementation to the base package.
- Discussion about also moving the node normalization logic to the main Jackalope package.

### Jackalope FS

- Pure filesystem implementation of PHPCR
- Currently supports Reading and some Writing.
- Will initially aim to have feature parity with the [doctrine-dbal](https://github.com/jackalope/jackalope-doctrine-dbal) implementation.
- ETA: About 3 months :)

### Jackalope Jackrabbit

* [Alfusainey](https://github.com/Alfusainey) is working on implementing remoting for access control in Jackrabbit. Once this works, it will be possible to implement ACLs in jackalope-jackrabbit, allowing access control on nodes and subtrees. Check out the [Jackrabbit pull requests](https://github.com/apache/jackrabbit/pulls).

### PHPCR-Shell

- General minor improvements, including asking for confirmation on exit if there are unsaved changes.
- Open [pull request](https://github.com/phpcr/phpcr-shell/pull/90) for adding
  function mapping to UPDATE queries, with the particular goal of better
  supporting multi-value propoperties.

### PHPCR-ODM

- **Version 1.2** of the [PHPCR-ODM](https://github.com/doctrine/phpcr-odm) is just around the corner and we ask people to test the latest RC version ([1.2.0-rc4](https://packagist.org/packages/doctrine/phpcr-odm#1.2.0-rc4)) and provid feedback until next week when we hope to release it.
- Fixed some bugs related to [translation](https://github.com/doctrine/phpcr-odm/pull/566) handling.
