JSONLD-Java RDF2Go Integration module
=====================================

[![Build Status](https://travis-ci.org/jsonld-java/jsonld-java.svg?branch=master)](https://travis-ci.org/jsonld-java/jsonld-java) 
[![Coverage Status](https://coveralls.io/repos/jsonld-java/jsonld-java/badge.svg?branch=master)](https://coveralls.io/r/jsonld-java/jsonld-java?branch=master)

USAGE
=====

From Maven
----------

    <dependency>
        <groupId>com.github.jsonld-java</groupId>
        <artifactId>jsonld-java-rdf2go</artifactId>
        <version>0.7.0-SNAPSHOT</version>
    </dependency>

(Adjust for most recent <version>, as found in ``pom.xml``).


Serializing RDF into JSON-LD using RDF2GoRDFParser
--------------------------------------------------

    import com.github.jsonldjava.rdf2go.*;

    ModelSet modelSet = ...; // also works with a Model
    RDF2GoRDFParser parser = new RDF2GoRDFParser();
    Object json = JSONLD.fromRDF(modelSet, parser);

Parsing JSON-LD, and convert it into a ModelSet
-----------------------------------------------

    RDF2GoTripleCallback callback = new RDF2GoTripleCallback();
    ModelSet model = (ModelSet) JSONLD.toRDF(input, callback);
