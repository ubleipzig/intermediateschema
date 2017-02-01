Notes for Version 1.0
=====================

Version 1.0 should have a clearer description.

Fields
======

id
--

Mandatory. Contains a unique identifier. Should be of the form

```
group-pool-id
```

Where group would be a processing pool or some arbitrary name. Alphanumeric and
short, not longer than 8 chars; pool would subsume many ids. An id must be
uniq, but only within a pool.

The id must be useable as URL of filename. A base64 URL encoding is suggested, if the IDs of the pool can be anything. 

Examples:

```
finc-99-1115
ai-89-NzQxMjY4NQ
dswarm-105-MTAuMTAwNy81MjAuMTQzMy03MzM5
```

source
------

Name or id of the data source. Often the same as the pool part of the id.

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

authors
-------

A list of authors.

doi
---

A document object identifier.

languages
---------

A list of languages (three-letter-codes)



Name of the collection. This is usually displayed as a facet.

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
