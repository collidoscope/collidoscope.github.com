---
published: false
layout: post
title: W3IDs for ISIL
abstract: persistent and secure identifier for ISIL
description: persistent and secure identifier for ISIL
author: Carsten Klee
categories: isil, identifier, library
tags: isil, w3id, identifier
comments: true
sharing: false
---

#W3IDs for ISIL

The International Standard Identifier for Libraries and Related Organisations (ISIL / ISO 15511) identifies an organization, i.e. a library, an archive, a museum or a related organization, or one of its subordinate units. The registration of ISILs takes place at the [National ISIL Allocation Agencies (see list)](http://biblstandard.dk/isil/).

Todays identification is best expressed through HTTP URIs because of their uniqueness. Unfortunately the distributed maintenance of ISILs in the different national agencies makes it yery hard or impossible to reference cultural heritage organizations by ISIL through URIs.

However some agencies provide ISIL-URIs or even linked data services (see [Code List for Cultural Heritage Organizations](http://id.loc.gov/vocabulary/organizations) or [Linked Data Service Adressdaten](http://sigel.staatsbibliothek-berlin.de/en/suche/linked-data-service/)). But wouldn't it be nice to access cultural heritage organizations within a single domain?

[Permanent Identifiers for the Web (w3id.org)](https://w3id.org/) provides a secure, permanent URL re-direction service for Web applications. And this gives us the opportunity to provide a single access point to organization information identified by ISIL.

One can now reference an organization identified by an ISIL through

    https://w3id.org/isil/<ISIL>

Such an URI may be not dereferenceable (no data for lookup). E.g. https://w3id.org/isil/CH-000015-0 will not return any organization data but may be used as an identifier for the "Schweizerisches Literaturarchiv, Bern".

Current ISILs that are supported for dereferencing are:
- US-* (e.g. https://w3id.org/isil/US-NNM)
- DE-* (e.g. https://w3id.org/isil/DE-1a)
- IT-* (e.g. https://w3id.org/isil/IT-BO0001)
- ZDB-* (e.g. https://w3id.org/isil/ZDB-1-TDA)

