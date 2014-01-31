---
layout: post
title: "Open Data Sources - Beyond the Public Sector"
date: 2013-03-20 09:40
comments: true
categories: [open data, API, statistics, data] 
---

This is the second in a pair of posts designed to provide a primer on sources of open data. This post focuses on non-public sector sources, the previous one looked at [where to go for open government data](/blog/2013/03/18/public-sector-information-whats-available-and-where-you-can-find-it/).

This post was prepared as part of my contribution to the [Business of Open Data Workshop](http://futureeverything.org/summit/conference/workshops-fringe-events/business-of-open-data-workshop/). This workshop is the first in a series organised by [Open Data Manchester](http://opendatamanchester.org.uk/) and [Future Everything](http://futureeverything.org).
<!-- more -->

## The Social Web
{%img /images/post_images/circles-bird.png %}

As you might expect, there's a tremendous amount of data being generated across social networking platforms. These businesses thrive on having porous walls (from a data perspective at least). It's little surprise then that they all come with a suite of developer tools to help you build functionality into their offering. This approach wouldn't be considered by all to constitute openness (and indeed some are [completely resistant to the prospect of Facebook owning their identity](http://www.fsf.org/facebook)) but it is worth mentioning as these resources contain a wealth of information. Typically permission must be given by a user for you to access their perspective on the social network using protocols such as open auth

  - [Twitter's Developer APIs](https://dev.twitter.com/) provide programmatic access to what they call 'platform objects': Tweets, Users, Entities (#hashtags, media, urls, and @mentions), and Places.
  - [Facebook for Developers](https://developers.facebook.com) includes the Graph API for reading from and writing to Facebook platform: Users, Pages, Groups, Photos, Videos, and the actions between objects. They've even got their [own query language](https://developers.facebook.com/docs/technical-guides/fql/)!
  - [Linked-in APIs](https://developer.linkedin.com/) for People, Groups, Companies, and Jobs.
  - [The Google+ Platform](https://developers.google.com/+/) for People, Activities, Comments and Moments

## Open Corporates
{% img /images/post_images/mapping-tesco.png %}

[OpenCorporates](http://opencorporates.com/) has a straightforward (though big) ambition: to have a URL for every company in the world. The project combines data collected from official registries (such as Companies House in the UK) with crowd-sourced data (e.g. from unparseable filings etc). The [blog](http://blog.opencorporates.com/) reveals some of the fascinating analyses that are possible (such as [this network graph of directors and companies](http://blog.opencorporates.com/2012/12/17/guest-post-data-sketching-with-the-opencorporates-api/)) and issues that exist in this area ([are DUNS numbers the crack cocaine of business identification?](http://blog.opencorporates.com/2012/07/24/are-duns-numbers-the-crack-cocaine-of-id-systems-and-is-the-uk-the-latest-addict/)).

## Princeton Wordnet
The [Princeton WordNet](http://wordnet.princeton.edu/) is a lexical database of English - a catalogue of words.
{% blockquote %}
Nouns, verbs, adjectives and adverbs are grouped into sets of cognitive synonyms (synsets), each expressing a distinct concept. Synsets are interlinked by means of conceptual-semantic and lexical relations. The resulting network of meaningfully related words and concepts can be navigated with the browser. WordNet is also freely and publicly available for download. WordNet's structure makes it a useful tool for computational linguistics and natural language processing.
{% endblockquote %}
If you're interested in text analysis then I highly recommend that you check out [Gate](http://gate.ac.uk/) which of course has a Wordnet plugin.

## OPTA MCFC-Analytics
{% img /images/post_images/Opta.png %}

Opta - a sports data company - has released data as part of the MCFC-Analytics project. There are two datasets:
- The "Lite" Dataset which has an entry for every player's appearance in each match (10,370 in total) from the 2011-12 Premier League Season. The 185 fields cover a handful of contextual details (name of player and team etc) and counts for all of the "on ball" events in some detail (e.g. "Total Successful Passes Excl Crosses Corners"). The data is provided in csv.
- The "Advanced" data provides a time and space (x, y, and z!) coded feed of events, codified by type. The initial set of open data covers only Manchester City players although more is promised if you can demonstrate some interesting developments...

## DBpedia
{% img /images/post_images/dbpedia_logo.png %}

[DBpedia](http://dbpedia.org/)...
{% blockquote %}
...is a crowd-sourced community effort to extract structured information from Wikipedia and to make this information available on the Web. DBpedia allows you to make sophisticated queries against Wikipedia, and to link other data sets on the Web to Wikipedia data. We hope this will make it easier for the amazing amount of information in Wikipedia to be used in new and interesting ways, and that it might inspire new mechanisms for navigating, linking, and improving the encyclopedia itself.
{% endblockquote %}

## Freebase
{% img /images/post_images/freebase-logo.png %}

[Freebase](http://freebase.org/) is a free, open knowledge graph covering 37 million topics, 2000 types, and 30,000 properties. Topics (e.g. [Leonardo da Vinci](http://www.freebase.com/m/04lg6)) can have types (e.g. Visual Artists) and types contain properties (e.g. his [artworks](http://www.freebase.com/query?autorun=1&q=%5B%7B%22id%22:%22/m/04lg6%22,%22name%22:null,%22/visual_art/visual_artist/artworks%22:%5B%5D%7D%5D)).




Hopefully that gives you a flavour of what is out there. I'd welcome any additional suggestions in the comments...
