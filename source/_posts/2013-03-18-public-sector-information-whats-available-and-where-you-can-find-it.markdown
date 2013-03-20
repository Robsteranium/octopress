---
layout: post
title: "Public Sector Information: what's available and where you can find it"
date: 2013-03-18 15:43
comments: true
categories: [open data, public sector information, API, statistics, data] 
---

This is the first in a pair of posts designed to provide a primer on sources of open data. This post focuses on open government data and the next focusses on [open data beyond the public sector](/news/blog/2013/03/20/open-data-sources-beyond-the-public-sector).

This post was prepared as part of my contribution to the [Business of Open Data Workshop](http://futureeverything.org/summit/conference/workshops-fringe-events/business-of-open-data-workshop/). This workshop is the first in a series organised by [Open Data Manchester](http://opendatamanchester.org.uk/) and [Future Everything](http://futureeverything.org).

To understand why public sector information is the main source of open data you may wish to read about the [economics of open data](/news/blog/2012/10/25/the-economics-of-open-data). 
<!-- more -->

## Who is publishing Public Sector Information - Where can I find it?

### data.gov.uk
{%img left /images/post_images/dgu-header.png %}
In 2009 [data.gov.uk](http://data.gov.uk) was established to provide a central catalogue of public sector information, covering over 9,000 sources (as I write this). It provides meta data, that is, it acts an index of other data rather than a respository itself. The site is built on the [Open Knowledge Foundation's](http://okfn.org) [CKAN](http://ckan.org/) platform. It provides a [SPARQL endpoint](http://data.gov.uk/sparql) for a [variety of Linked Open Data resources](http://data.gov.uk/linked-data/who-is-doing-what).
In theory, this site should cover most of what is available from Government. Although in the past, the coverage has been patchy in parts and duplicated in others, this has largely been resolved over the past few years. The main problem with data.gov.uk is that it's sometimes best to go direct to the horses' mouth particularly when what you're interested in is a delivery API, not metadata discovery. As such I'll go into a little more detail about the places you'll usually find yourself after you've explored data.gov.uk.

### The Office of National Statistics
{%img right /images/post_images/s300_NS_logo.jpg %}

The Office for National Statistics is the executive office of the UK Statistics Authority. The authority is a dedicated non-ministerial government department with responsibility for assessing *Official statistics* (i.e. "those produced by a government department or persons acting on behalf of the crown") against it's [Code of Practice](http://www.statisticsauthority.gov.uk/assessment/code-of-practice/) to ensure that only compliant publications are designated *National Statistics*.

The [ONS](http://www.ons.gov.uk) has long been providing data as both [datasets](http://www.ons.gov.uk/ons/datasets-and-tables/index.html) and [published reports](http://www.ons.gov.uk/ons/publications/index.html) (books, articles, bulletins) that include some narrative and interpretation. The most recent incarnation of the ONS site has convenient filters for discovering what available by theme, release date (including [forthcoming releases](http://www.ons.gov.uk/ons/release-calendar/index.html)), and geographic scope and precision (i.e. where is covers and with what breakdowns). While it's naturally tempting to rush to the raw data you should also bear in mind that the [methodological guidance](http://www.ons.gov.uk/ons/guide-method/index.html) is very important - there's many a time this has either saved me making a mistake in interpretation (fixed-capital investment figures used to be apportioned by jobs and so were no more informative for making regional comparisons) or suggested an alternate 'experimental' dataset that offered new insights (e.g. multiple approaches to measuring Gross Value Added).

Of particular note are:

- the ONS's site for labour market statistics - [nomis](http://www.nomisweb.co.uk) - they have a [RESTful API](http://www.nomisweb.co.uk/api/v01/help) which is compliant with the Statistical Data and Metadata eXchange (SMDX) ISO standard. The API offers both discovery and delivery services, URI resolution, and HTML, XML, json, and csv response formats.
- the [Neighbourhood Statistics Exchange (NeSS)](http://www.neighbourhood.statistics.gov.uk/) - with their [Neighbourhood Data Exchange (NDE) API](http://www.neighbourhood.statistics.gov.uk/dissemination/Info.do?page=nde.htm), version 2 of which is now RESTful (I've got some ruby bindings knocking around somewhere if you really want to use the SOAP interface instead).
- the [forthcoming ONS API](http://www.ons.gov.uk/ons/about-ons/what-we-do/programmes---projects/enhancing-access-to-ons-data/ons-api/index.html) which will operate under a similar principle and is designed with data from the 2011 Census in mind. 

### Central Government Departments
{%img left /images/post_images/govuk-crest.png %}
As part of their daily work and obligations for reporting, [Central Government Departments](https://www.gov.uk/government/organisations) produce great volumes of data that is publically available. This departments have gradually be brought out from a heterogenous collection of sites operating under a department.gov.uk sub domain to a consistent www.gov.uk/department arrangement. This has made it much easier to search across Government for [statistics](https://www.gov.uk/government/publications?publication_filter_option=statistics) or [research and analysis](https://www.gov.uk/government/publications?publication_filter_option=research-and-analysis). Indeed a convenient [index of statistical data sets](https://www.gov.uk/government/statistical-data-sets) is provided.

### data.gov.*
{%img right /images/post_images/datagm-beta.png %}
There is also a plethora of other PSI datastores from [Manchester](http://www.datagm.org.uk/) to [Moldova](http://data.gov.md/) and, indeed, [all over the world](http://datacatalogs.org).

## What's available? The Big Names in PSI
{%img /images/post_images/oslogo.png %}

- For transport, the main data sets are the [National Public Transport Access Nodes (NapTAN)](), which unique identifies public transport access points, and the [National Public Transport Data Repository](http://data.gov.uk/dataset/nptdr), which provides a snapshot of every GB journey in ATCO-CIF and TransXChange formats. Historically, the NPTDR has been taken annually in October but it is now being provided weekly as the [Traveline National Dataset](http://traveline.info/tnds.html) (requires registration for FTP access).
- The [Indicies of Multiple Deprivation](http://data.gov.uk/dataset/index-of-multiple-deprivation) - which ranks English neighbourhoods (or Lower-layer Super Output Areas - LSOAs) according to seven dimensions of deprivation. The IMD is often used as a means of allocating resources by need. NB: the publication is irregularly timed and has (historically at least) been subject to methodological changes between years making it difficult to use this dataset for trend analysis. It does, however, provide an incredible level of geographic precision.
- The [Combined Online Information System (COINS)](http://data.gov.uk/dataset/coins) - which is basically the governments central accounts, all 4.3Gb of them!
- The [ONS Postcode Directory and National Statistics Postcode Lookup](http://www.ons.gov.uk/ons/guide-method/geography/products/postcode-directories/-nspp-/index.html) - which provides a lookup for transforming postcodes into other geographic terms including statistical areas (e.g. LSOAs) and geocodes (i.e. Latitude-Longitude/ Northings-Eastings).
- [Ordnance Survey Open Data](http://www.ordnancesurvey.co.uk/oswebsite/products/os-opendata.html) including the 'tiles' of the map (raster), government administrative boundaries (vector ESRI shapefiles), code-points (a csv of postcode coordinates etc), and gazetteers of place and road names.
- [Legislation.gov.uk](http://legislation.gov.uk) publishes all UK legislation in both the original enacted form and with revisions that are made over time. The platform is managed by the [The National Archives](http://www.nationalarchives.gov.uk/) and provides Linked Data access (try adding /data.xml to the end of a URI).

If you're interested in more of the top datasets you might like to peruse [data.gov.uk's own list of popular datasets](http://data.gov.uk/data/site-usage/dataset) or read on to [find out about what's available outside of the public sector](/news/blog/2013/03/20/open-data-sources-beyond-the-public-sector).

Have I missed some major sources or data sets? Let me know in the comments...
