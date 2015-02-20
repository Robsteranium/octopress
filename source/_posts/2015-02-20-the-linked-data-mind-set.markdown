---
layout: post
title: "The Linked Data Mind Set"
date: 2015-02-20 17:13
comments: true
categories: [ linked data, open data, data, information ]
---

Linked Data is data that has been structured and published in such a way that it may be interlinked as part of the Semantic Web. In contrast to the traditional web, which is aimed at human readers, the semantic web is designed to be machine readable. It is built upon standard web technologies - <acronym title="Hypertext Transfer Protocol">HTTP</acronym>, <acronym title="Resource Description Framework">RDF<acronym>, and <acronym title="Uniform Resource Identifier">URI</acronym>s.

I've been working with Manchester-based Linked Data pioneers [Swirrl](http://www.swirrl.com/) to convert open data to linked data format. This experience has opened my eyes to the immense power of linked data. I thought it was simply a good, extensible structure with some nice web-oriented features. What I've actually found is some pretty fundamental differences that require quite a change in mind set.

<!--more-->

## Introduction to Linked Data

If you're already familiar with linked-data then jump down to read about the changes in perspective it's led me to see. If you're new to the topic or a bit rusty then you might want to read about the basic principles first.

The recently updated [RDF Primer 1.1](http://www.w3.org/TR/2014/NOTE-rdf11-primer-20140225/) provides an excellent introduction to RDF. A brief summary follows.

### Everything is a graph

Graphs, in the mathematical sense, are collections of nodes joined by edges. In linked-data this is described in terms of triples - statements which relate a subject to an object via a predicate:

    <subject> <predicate> <object>
    <Bob> <is a> <person>
    <Bob> <is a friend of> <Alice>
    <Bob> <is born on> <the 4th of July 1990>

These statements are typically grouped together into graphs or contexts. A quad statement has a subject, predicate, object, and context (or graph).

### URIs and Literal

The subjects and predicates are all identifiers symbolic representations that a supposed to be globally unique, called uniform resource identifiers (URIs). URIs are much like URLs (Uniform Resource Locators) that you may be familiar with using to find web pages (this "finding" process - requesting a URL in your browser to get a web page in response - is more technically known as "dereferencing"). URIs are a superset of URLs which also include URNs (Uniform Resource Names) such as ISBNs (International Standard Book Numbers).

The objects can also be URIs or they can take the form of literal values (like strings, numbers and dates).

### Turtle and SPARQL

There are a number of serialisation formats for RDF. By far the most readable is [Turtle](http://www.w3.org/TR/turtle/).

    BASE   <http://example.org/>
    PREFIX foaf: <http://xmlns.com/foaf/0.1/>
    PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
    PREFIX schema: <http://schema.org/>

    <bob#me>
        a foaf:Person ;
        foaf:knows <alice#me> ;
        schema:birthDate "1990-07-04"^^xsd:date ;

[SPAQRL](http://www.w3.org/TR/rdf-sparql-query/) is a query language for RDF. The query below selects Bob.

    SELECT ?person WHERE { ?person foaf:knows <http://example.org/alice#me> }


## Thinking with a Linked Data Mindset

Now that we've established the basics, we can go on to consider how this perspective can lead to a different mindset.

### There's no distinction between data and metadata

Metadata is data that describes data. For example, the date a dataset was published. In traditional spreadsheets there's not always an obvious place to put this information. It's recorded in the filename or on a "miscellanous details" sheet. This isn't ideal as a) it's not generally referenceable, and b) it is easily lost if it's not copied around with the data itself.

In RDF, metadata is stored in essentially the same way as data. It's triples all the way down! Certainly there are some vocabularies that are designed for metadata purposes ([Dublin Core](http://dublincore.org/), [VOID](http://www.w3.org/TR/void/), etc) but the content is described using the same structures and is amenable to the same sorts of interrogation techniques.

This makes a lot of sense when you think about it. Metadata serves two purposes: to enable discovery and to allow the recording of facts that wouldn't otherwise fit.

Discovery is the process of finding data relevant to your interests. Metadata summarises the scope of a dataset so that we can make requests like: "show me all of the datasets published since XXXX about YYYY available on a neighbourhood level". But this question could be answered with the data itself. The distinction between metadata and data exists in large part, because of the way we package data. That is to say we typically present data in spreadsheets where the content and scope cannot be accessed without the user first acquiring and then interpreting the data. Obviously this can't be done in bulk unless the spreadsheets follow a common schema (some human interaction is otherwise necessary to prepare the data). If we remove the data from these packages, and allow deep inspection of it's content, then discovery can be acheived without resorting to a separate metadata index (although metadata descriptions can still make the process more efficient).

The recording of facts that don't fit is usually a problem for metadata because it doesn't vary along the dimensions of the dataset in the traditional (tabular) way it's usually present. This isn't a problem for linked data.


### The entity-relationship model doesn't (always) fit

The capacity of entity-relationship models is demonstrated by the popularity of object-oriented programming and relational-databases. Linked-data too can represent entity-relationship very naturally. The typically problem with the ER approach is that there's so often an exception to the rule. A given entity doesn't fit with the others and has a few odd properties that don't apply to everything else. Different relationships between instances of the same two types (typically recorded with primary/ foreign keys) are qualitatively different. Since in ER, information about an object is stored within it, the data model can become brittle. In linked-data, properties can be defined quite apart from objects.


### There's no schema: arbitrary data can be added anywhere

In a traditional table representation, it's awkward to add arbitrary data. If you want to add a datum that doesn't fit into the schema then the schema must be modified. Adding new columns for a single datum is wasteful, and quickly leads to a bloated and confusing list of seldom-used fields.

In part, this frustration gave rise to the Schemaless/ NoSQL databases. These systems sit at the other end of the scale. Without any structure it can be complex to make queries and maintain data integrity. These problems are shifted from the database to the application layer.

In a graph representation, anything can be added anywhere. The schema is in the data itself and we can decide how much structure (like constraints and datatypes) we want to add.


### The data is self-describing

This flexibility - the ability to add arbitrary facts without the constriction of a schema - can certainly seem daunting. Without a schema what is going to prevent errors, provide guarantees, or ensure consistency? In fact linked-data does have a schema of sorts. Vocabularies are used to describe the data. A few popular ontologies are worth mentioning:

- [RDFS](http://www.w3.org/TR/rdf-schema/): the RDF Schema extends the basic RDF vocabulary to include a class and property system.
- [OWL](http://www.w3.org/TR/owl-primer/): the Web Ontology Language is designed to represent rich and complex knowledge about things, groups of things, and relations between things
- [SKOS](http://www.w3.org/TR/skos-primer): provides a model for expressing the basic structure and content of concept schemes such as thesauri, classification schemes, subject heading lists, taxonomies, folksonomies, and other similar types of controlled vocabulary.


### There's no one right way to do things

The flexibility of the data format means that there are often several ways to model the same dataset. This can lead to a sort of options-paralysis! It often pays to make a choice for the sake of progress, then review it later once more of the pieces of the puzzle are in place. Realising that it doesn't need to be perfect first time is certainly liberating.


### Naming is hard

Naming is one of the hardest problems in programming. Linked data modelling is 90% naming. The [Linked Data Patterns book](http://patterns.dataincubator.org/book/) provides some useful suggestions for how to approach naming (URI design) in a range of contexts.

[Identifiers have value](http://thomsonreuters.com/corporate/pdf/creating-value-with-identifiers-in-an-open-data-world.pdf): clarifying ambiguity, promoting consensus, providing reliability, ensuring stability, and facilitating integration.


### Vocabularies aren't settled

When developing a linked-data model, it's vital to understand the work done by others before you. After all, you need to adopt other vocabularies and URIs in order to link your data to the rest of the semantic web. There are lots of alternatives. The [Linked Open Vocabularies](http://lov.okfn.org) site provides a way to search and compare vocabularies to help you decide which to use.


## The Linked-Data Mind Set

In summary:

- Metadata can be data too, don't treat it as a second class citizen
- Use entities if it helps, but don't get too hung-up on them
- Let your schema grow and change over time as you learn more about the domain
- Use the core vocabularies to bring commonly understood structure to your data
- Experiment with different models to see what works best for your data and applications
- Create identifiers - it might be hard to start with, but everybody benefits in the long-term
- Stand on the shoulders of giants - follow patterns and adopt vocabularies
