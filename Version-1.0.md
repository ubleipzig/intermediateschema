Notes for Version 1.0
=====================

Version 1.0 should have a clearer description.

This is WIP.

Fields
======

id
--

Mandatory. Contains a unique identifier. Should be of the form

```
group-pool-id
```

Where group would be a processing entity or some arbitrary name. Alphanumeric and
short, not longer than 8 chars; a pool would subsume many ids. An id must be
uniq, but only within a pool.

The whole string must be useable as URL or filename. A base64 URL encoding is
suggested, if the IDs of the pool can contain URL unfriendly characters.

Examples:

```
ai-89-NzQxMjY4NQ
dswarm-105-MTAuMTAwNy81MjAuMTQzMy03MzM5
finc-99-1115
```

source
------

Name or id of the data source. Often the same as the pool part of the id. Alphanumeric.

format
------

Possible values:

* ElectronicArticle
* eBook
* ElectronicBookPart
* ElectronicJournal
* ElectronicProceeding
* ElectronicResourceRemoteAccess
* ElectronicSerial
* ElectronicThesis
* Unknown

collection
----------

Name of the collection. This value usually appears in a facet.

authors
-------

A list of authors.

doi
---

A document object identifier.

languages
---------

A list of languages (three-letter-codes)


RIS related properties (ris)
===========================

* ris.type

Open-URL related properties (rft)
=================================

* rft.atitle
* rft.epage
* rft.genre
* rft.issn []
* rft.issue
* rft.jtitle
* rft.tpages
* rft.pages
* rft.pub []
* rft.date
* rft.spage
* rft.volume

Other properties (x)
====================

* subjects
* type
