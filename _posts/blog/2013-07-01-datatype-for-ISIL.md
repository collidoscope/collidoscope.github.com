---
published: 
  - false
  - "true"
layout: post
title: Datatype for ISIL
abstract: Definition of a datatype for ISILs
description: Definition of a datatype for ISILs
author: Carsten Klee
categories: lld
tags: "rdf, isil"
comments: "true"
sharing: "true"
---

# Datatype for ISIL
Jakob wrote about [ Identifiers in RDF considered harmful ](http://jakoblog.de/2013/06/18/identifier-in-rdf-considered-harmful/). He shows that the common practice describing [ ISILs ](http://biblstandard.dk/isil/) in RDF as Literals is problematic.

Since there are no standard way to encode ISILs in an URI there are only to possibilities left: Using a property like Adrian suggested http://purl.org/lobid/lv#isil or defining a datatype for ISILs.

I'm not sure, what is the best way to proceed, but here is my proposal for a ISIL-datatype:

```
<http://example.org/ISIL>
	a rdfs:Datatype ;
	rdfs:comment "String representing an ISIL - International Standard Identifier for Libraries and Related Organizations" ;
	owl:onDatatype xsd:string ;
	owl:withRestrictions (
		[
			xsd:pattern "[A-Z]{1,4}-[0-9a-zA-Z:\-/]{1,11}"
		]
	) .```
    
So one could state now

```
$BIB
  dc11:identifier "DE-1a"^^<http://example.org/ISIL> .
```

Maybe the combination of both is a good solution too?

```
$BIB
  lobid:isil "DE-1a"^^<http://example.org/ISIL> .
```


