---
layout: post
title: "9 Tools Every Information Analyst Should Have"
date: 2013-01-30 12:15
comments: true
categories: [ analysis, data-visualisation, information, methodology, open-source, tools ] 
---

I was interested to read Rebecca Murphey's [Baseline for Front End Developers](http://rmurphey.com/blog/2012/04/12/a-baseline-for-front-end-developers/)  in which the author realizes that she has begun to take for granted a basic set of tools of the trade. She presents "a few things that [she] wants to start expecting people to be familiar with, along with some resources you can use if you feel like you need to get up to speed". I'd like to pay homage to that article and revise it in light of *the tools I believe are essential for an Information Analyst*. There is considerable overlap in the tools suggested although the application will differ.
<!--more -->
{% img http://imgs.xkcd.com/comics/regular_expressions.png 'Wait, forgot to escape a space.  Wheeeeee[taptaptap]eeeeee.' 'XKCD Regular Expressions Comic' %}

## GNU/ UNIX Command Line Tools

These tools are especially powerful because they don't require you to load the entire file into memory. This makes it possible to work with very large files efficiently.

- `head`, `tail`, `less`, `cat` etc for looking at files
- `awk`, `sed`, and `tr` for processing and altering files 
- `cut`, `paste`, and `join` again for editing and combining text files
- `sort` and `uniq`
- `wc` for counting lines/ words/ characters
- `iconv` for converting between different encodings

Some useful resources include:

- [Unix as an IDE](http://blog.sanctum.geek.nz/series/unix-as-ide/)
- [Simplify data extraction using Linux text utilities](http://www.ibm.com/developerworks/linux/library/l-textutils/index.html)
- [Text Processing Commands in the Advanced Bash-Scripting Guide](http://tldp.org/LDP/abs/html/textproc.html)
- [Replacing returns with commas in Sed](http://funarg.nfshost.com/r2/notes/sed-return-comma.html)
- [Oh my zsh](https://github.com/robbyrussell/oh-my-zsh) - zshell a replacement for bash


## Regular Expressions

Regexs are extremely powerful, if sometimes counter-intuitive. They are vital for defining patterns and replacements in text processing. Although some [debate](http://stackoverflow.com/questions/1732348/regex-match-open-tags-except-xhtml-self-contained-tags/1732454#1732454) exists a to whether they should be used to parse structured formats like XHTML, they are certainly a vital tool.

Having said which, I find this quote pretty amusing!
{% blockquote Jamie Zawinski http://regex.info/blog/2006-09-15/247 Jeffrey Friedl's Blog %}
Some people, when confronted with a problem, think “I know, I'll use regular expressions.” Now they have two problems.
{% endblockquote %}

- [RegExr](http://gskinner.com/RegExr/) - Regex building and testing tool
- [Regexper](http://www.regexper.com/) - visualisation tool
- [Reference Docs](http://www.regular-expressions.info/)
- An example for [validating credit card numbers](http://www.softwareprojects.com/resources/programming/t-validate-a-credit-card-1682.html) or [validating UK Postcodes](http://stackoverflow.com/a/164994/187009) 


## A Programming/ Scripting Language

If nothing else, these provide the glue to connect different sections of your data pipeline. The incredible range of libraries avavailable to most scripting languages will make quick work of many common information processing tasks: parsing, spidering, <abbr title="Extraction, Translation, and Loading">ETL</abbr> etc. The choice of language is down to personal preference or compatibility with the team.
It should suffice to say that knowledge of a scripting language is necessary and I don't feel the need to recommend a particular language. Having said which, I can't resist saying that I prefer `ruby` but have dabbled in `perl` and `python`. I find the following ruby gems indispensible: `mechanize`, `nokogiri`, `fastercsv` (now `CSV` in the 1.9 standard library), and `json`. I've also been using `javascript` and node for scripting outside of the browser as asynchronous processing has proved to be very quick (if a little peculiar to code at first).

- [Why The Lucky Stiff's (poignant) Guide to Ruby](http://mislav.uniqpath.com/poignant-guide/book/chapter-1.html)
- [A guide written by Matz (the original author of Ruby)](http://www.rubyist.net/~slagell/ruby/)
- [Github's Ruby Style Guide](https://github.com/styleguide/ruby)
- [Ruby Toolbox](https://www.ruby-toolbox.com/) - for finding and selecting gems
- John Ressig's [Learning Advanced Javascript](http://ejohn.org/apps/learn/)

## Text data files

Probably the most basic technology used in information analysis, the flat file is the lowest common denominator. You can almost guarantee that everyone will be able to cope with `csv` files (even if they need to be translated before loading into another tool). The expressiveness and rigour of `XML` makes it another vital tool although it's rapidly being superceded in bandwidth-conscious realm of http by the less verbose `json`.
Information analysts ought to be able to handle (read, understand, parse and translate) files in these all of formats even if they immediately convert them to a prefered type.

- [XSLT for CSV 2 XML](http://www.delicious.com/redirect?url=http%3A//andrewjwelch.com/code/xslt/csv/csv-to-xml_v2.html)
- [XPath Syntax](http://www.w3schools.com/xpath/xpath_syntax.asp)
- [Improving an XML feed through CSS and XSLT](http://www.evagoras.com/2011/02/10/improving-an-xml-feed-display-through-css-and-xslt/)
- [JSON reference with links to parsers](http://www.json.org/)


## Relational Databases, SQL, and NoSQL

This shouldn't really come as a surprise to anyone. If you're going to analyse information, you're going to need to deal with databases. An analyst ought to be able to write <abbr title="Structured Query Language">SQL</abbr>, understand normalisation/ denormalisation, and possibly also have some knowledge of <abbr title="Object-Relational Mapping">ORM</abbr>. NoSQL databases are also useful when the data structure is better represented by document, graph or key:value structures (and where tables would be very sparse).

- [MySQL](http://dev.mysql.com/)
- [MySQL Cheat Sheet](http://www.nparikh.org/unix/mysql.php)
- [SQLite](http://www.sqlite.org/)
- [database normalisation](http://en.wikipedia.org/wiki/Database_normalization) and [denormalisation](http://www.codinghorror.com/blog/2008/07/maybe-normalizing-isnt-normal.html)
- [NoSQL Guide](http://nosql-database.org/)
- [Mongodb](http://www.mongodb.org/) - document database
- [Neo4j](http://www.neo4j.org/) - graph database
- [CouchDB](http://couchdb.apache.org/) - json + map reduce + http


## Statistical Library

Unless you really want to code algorithms for every statistical process from scratch, you're going to want to adopt and familiarise yourself with a statistical library. I would strongly recommend `GNU-R` although other options include `Stata`, `SPSS`, and `Matlab` etc. Of course there is probably a library available for your prefered programming language. `scipy` and `numpy` are very popular choices for `python`.

- [The R Project](http://www.r-project.org/)
- [R Seek](http://rseek.org) - R-specific search engine
- [R tag on Stackoverflow](http://stackoverflow.com/tags/r) (bonus: [Cross Validated](http://stats.stackexchange.com/) - the stats-specific Stack Exchange Q&A site)
- [Revolution Analytics Blog](http://blog.revolutionanalytics.com/)
- [ggplot2](http://docs.ggplot2.org/current/)
- [gretl](gretl.sourceforge.net) - Gnu Regression, Econometrics and Time-series Library


## Visualisation Framework

Similarly you'll probably want to use some sort of framework for generating visualisations. I've tried many and have found myself coming back to a few:

- [d3 data driven documents](http://d3js.org) - A JavaScript library for manipulating documents based on data using HTML, SVG and CSS
- [ggplot2](http://docs.ggplot2.org/current/) - the tool that usually attracts people to R; excellent for quickly sketching out data graphics
- [processing](http://processing.org) - Processing is an electronic sketchbook for developing ideas - in Java and now Javascript too.

## Report Templating
Usually you're going to want to place your analysis in context with some commentary. If you're going to be repeating a given report - either in part or in full - they you stand to benefit greatly from using some form of template. Again this will depend upon your prefered programming languages. My favoured tools are listed below.

- [Sweave](http://www.stat.uni-muenchen.de/~leisch/Sweave/) - R + Latex and [Open Document Format](http://rss.acs.unt.edu/Rdoc/library/odfWeave/html/odfWeave.html). I've not tried it yet but [Knitr](http://yihui.name/knitr/) looks like it could be a useful package).
- [HAML - HTML abstraction markup language](http://haml.info/) - very clear markup with indentation (so you don't have to write out every tag twice), you're able to use ruby inline.
- [Sass - Syntactically Awesome Stylesheets](http://sass-lang.com) - an extension of CSS3, adding nested rules, variables, mixins, selector inheritance, and more.
- [Javascript Template Engine Chooser](http://garann.github.com/template-chooser/)
- [d3 data driven documents](http://d3js.org) - for programmatically creating html from data

## Version Management

Version management is vital for tracking progress, making experimental branches in your work, and coordinating across teams. The clear leader in this regard is [git](http://git-scm.com) and the amazing project hosting environment [github](https://github.com/). I've got in the habit of versioning everything - not just my code - but my home file configurations too.

## And the rest...

This is just a quick list I wrote off the top of my head. What have I missed? What else do you use?
