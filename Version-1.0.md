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

A document object identifier. Could a document have more than one?

languages
---------

A list of languages (three-letter-codes)

urls
----

A list of URLs.


RIS related properties (ris)
===========================

* ris.type

Open-URL related properties (rft)
=================================

* rft.atitle
* rft.btitle
* rft.date
* rft.eisbn []
* rft.eissn []
* rft.epage
* rft.genre
* rft.isbn []
* rft.issn []
* rft.issue
* rft.jtitle
* rft.pages
* rft.pub []
* rft.spage
* rft.tpages
* rft.volume

Other properties (x)
====================

* subjects []
* type
* fulltext
* tags [] (additional, source-dependent package identifiers)
* isils [] (explicit local information)

Tooling
=======

Specifying a new format would be useful, (only) if the tooling around it makes
tasks simpler that with other formats or tools.

Possible things to do with a single format:

* licensing (like span-tag)
* quality checks (graded records: A, B, C)
* exporters (like span-export, solr, formeta)

Imaginary documents
===================

```json
{
    "id": "abc-120-120912",
    "doi": "10.1023/12901.292921",
    "source": "120",
    "format": "ElectronicArticle",
    "collection": "The imaginare documents database (IDD)",
    "languages": ["eng", "deu"],
    "rft": {
        "atitle": "An example document",
        "date": "2000-02-28",
        "issn": "1281-1213",
        "pages": "X-XV",
    },
    "tags": ["FSI", "my-custom-tag"],
    "urls": [
        "http://example.com/120/123.html",
        "http://doi.org/10.1023/12901.292921"
    ],
    "subjects": ["History", "Databases", "],
    "version": "1.0"
}
```