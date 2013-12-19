---
published: "true"
layout: post
title: MARC spec as string
abstract: Introsuction to MARC spec as string
description: Specification for encoding a MARC field spec as string
author: Carsten Klee
categories: lld
tags: "rdf, marc"
comments: "true"
sharing: "true"
---
# MARC spec as string

*MARC spec as string* is a specification for a MARC 21 field specification (short MARC spec) encoded as string. A MARC spec defines the reference to a data set derived from a MARC 21 record. A MARC spec normally consits of the field tag, a character position or range or subfield tags and indicators. Since there are a variety of mapping tools using MARC specifications in different encodings and forms, I thought it is time to standardize the form of a MARC spec encoded as string.

Therefor I've written a proposal for a MARC 21 spec as string specification. You can find it at <a href="http://cklee.github.io/marc-spec/marc-spec.html">http://cklee.github.io/marc-spec/marc-spec.html</a>.

Comments are welcome at <a href="https://github.com/cKlee/marc-spec/issues">https://github.com/cKlee/marc-spec/issues</a>

## What is a MARC spec as string good for?

The specification aims for the possibility of exchanging MARC mappings. More specific it aims for exchange of MARC mappings via RDF. A MARC spec as string can be easily described by RDF through literals or URIs.

Here is an imaginary example on how a MARC mapping could be described by RDF:

```
$mapping ex:maps [
    a ex:MappingRule ;
    ex:from [
        ex:form <http://cklee.github.io/marc-spec/marc-spec.html> ;
        rdf:value "245a"^^ex:MarcSpec
    ] ;
    ex:to <http://purl.org/dc/terms/title>
] .
```

Or maybe more easy

```
$mapping ex:maps [
    a ex:MappingRule ;
    ex:from <http://example.org/marcspec/245a> ;
    ex:to <http://purl.org/dc/terms/title>
] .
```

## Usage of MARC spec as string

Besides the specification I've written a PHP MARC spec as string parser and validator. It's available at [Github](https://github.com/cKlee/php-marc-spec). This parser is now included in [easyM2R](https://github.com/cKlee/easyM2R). With the use of MARC spec as string in the mapping configuration of easyM2R it makes configuring more easy and more powerful.
