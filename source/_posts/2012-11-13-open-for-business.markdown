---
layout: post
title: "Open For Business"
date: 2012-11-13 13:28
comments: true
categories: [open source, business model]
---

This post outlines some business considerations for open source. It follows [advice Infonomics provided to the World Wildlife Fund](/../portfolio_project/14) in collaboration with [Ribble Consultants](http://www.ribble-consultants.co.uk).
<!--more-->

Open Source Definitions
-----------------------
The term _open source_ denotes software for which the original source code is made available and may be redistributed with or without modification. In practice this is typically coupled with a peer-production development model although code can be open-sourced without providing any means of re-integrated changes back into the code base.
Note that:

* **Free software is not necessarily open-source (closed-source software may be free)**.  [Here ‘free’ refers to the freedom (to run, modify, and redistribute) not the price](http://www.gnu.org/philosophy/selling.html).
* **Open-source software is not necessarily free of charge**.  There are a variety of business models for generating revenue from an open-source project including: ‘freemium’ (premium features must be paid for), consulting (selling services related to the product), support (paid-for training), subscriptions (original is free, updates require a fee), proprietary add-ons (fees for implementing/ developing bespoke features), and dual licenses (whereby only those earning money from the tool must pay).
*	**Open-sourcing does not necessarily involve any loss of control over the quality or integrity of the product** (or intellectual property); multiple versions (internal and external) may exist concurrently.  Typically derivatives and modifications are made upon ‘forked’ copies (or branches).  The lead maintainer (person managing the code) takes responsibility for the core (trunk) version.  Changes contributed by the community (in branches) may be applied (used to patch) the original (trunk) or they may be pursued independently.  Moreover forks may pursue entirely different objectives without ever being integrated (e.g. a version is developed for a different software platform or only small portions of the code taken for use elsewhere).  See below for some real-world examples.

Advantages and Disadvantages
----------------------------
The advantages of open source include:

*	**Bug/ defect correction**: with more people exploring and testing the code there is a greater chance that problems will be identified and solved (improving stability and reliability);
*	**Improvements/ new feature**: there are more people to contribute ideas and code to enhance the product and integrate it with other developments;
*	**Credibility**: greater transparency lends credibility (‘auditability’) and the product’s sustainability depends less on the original developer.
The disadvantages include:
*	**Price ceiling**: the original developer may not be able to charge as much for software licenses.  We might expect that the fee could be no greater than is the cost of deploying/ implementing/ maintaining the code that is provided.
*	**Intellectual property**: other developers may be able to implement competing versions (this is typically dealt with via licensing restrictions).

Open Source Business Models
---------------------------
The table below describes how some of the larger businesses make money while releasing open-source versions of their software.
Typically there is:

*	a distinction between a limited-spec version which is released open-source and a fully-featured version which is sold commercially; and/ or
*	a fundamental division of functionality along the lines of free to use, pay to develop/ sell;
*	a set of complementary services that are provided at a fee (training, support, consultancy).

| Company          | Open Source                                                                              | Commercial                                                                 |
|------------------|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Adobe            | Flex platform for rich internet applications                                             | Flash Builder integrated development environment
| Apple            | Darwin: core unix compatible operating system released under Apple Public Source License | Mac OSX, Apple TV, iOS (iPhone/ iPad/ iPod platform)
| Canonical        | Ubuntu: linux operating system                                                           | Technical support contracts 
| Mozilla          | Firefox: web browser                                                                     | Partnership with google and others for including search engines in Firefox
| MySQL            | Database: community edition                                                              | Enterprise/ Cluster editions, training and consultancy
| Sun Microsystems | Open Office: office productivity suite                                                   | Star Office
  
What to consider before going Open Source
-----------------------------------------
* **Release the code**: the source will be made available online (i.e. the code not necessarily the data)
* **Release data**: some example data may be provided
* **Provide facility for commits**: developers may ‘commit’ changes or ‘fork’ new versions of the software (otherwise developers are responsible for maintain their own – external – versions)
* **Allow derivative works**: software developed from the tool can be sold commercially (there may be dual licenses – i.e. one for users and another for re-sellers)
* **Modifications must distribute source**: Licensee must include the source with any modifications (i.e. cannot create a closed-source derivative)
* **Derivatives subject to same license (copy-left)**: require that the same rights be preserved in modified versions
* **Provide user support**: for example, via training courses/ email/ telephone/ issue tracking/ webchat to end-users
* **Provide development support**: as above but for developers
* **Facility for community discussions**: a popular alternative to one-to-one support, this allows users to guide one-another (typically moderated by trust users or employees)
* **What aspects are free of charge?**
* **What aspects require a fee?**
 
Comparison of Open Source Licenses
----------------------------------
The decicions you reach on the above considerations will help to determine which license is most suitable.

<table>
 <tr>
  <td>
  <p align="center"><span>License</span></p>
  </td>
  <td>
  <p align="center"><span>Attribution</span></p>
  </td>
  <td>
  <p align="center"><span>Non-Commercial</span></p>
  </td>
  <td>
  <p align="center"><span>Registration</span></p>
  </td>
  <td>
  <p align="center"><span>Distribution</span></p>
  </td>
  <td>
  <p align="center"><span>Combinations</span></p>
  </td>
  <td>
  <p align="center"><span>Transformation</span></p>
  </td>
  <td>
  <p align="center"><span>Linking</span></p>
  </td>
  <td>
  <p align="center"><span>Copyleft</span></p>
  </td>
 </tr>
 <tr>
  <td>
  <p align="center"><span>&nbsp;</span></p>
  </td>
  <td>
  <p align="center"><span>&nbsp;</span></p>
  </td>
  <td>
  <p align="center"><span>&nbsp;</span></p>
  </td>
  <td>
  <p align="center"><span>&nbsp;</span></p>
  </td>
  <td>
  <p align="center"><span>Licensee must include the source with any
  modifications</span></p>
  </td>
  <td>
  <p align="center"><span>with other code</span></p>
  </td>
  <td>
  <p align="center"><span>edit/ rewrite</span></p>
  </td>
  <td>
  <p align="center"><span>with code under different license</span></p>
  </td>
  <td>
  <p align="center"><span>Derivates subject to same license</span></p>
  </td>
 </tr>
 <tr>
  <td nowrap valign="bottom">
  <p><span>All-rights-reserved</span></p>
  </td>
  <td nowrap>
  <p align="center"><span>n/a</span></p>
  </td>
  <td nowrap>
  <p align="center"><span>n/a</span></p>
  </td>
  <td nowrap>
  <p align="center"><span>n/a</span></p>
  </td>
  <td nowrap>
  <p align="center"><span>n/a</span></p>
  </td>
  <td nowrap>
  <p align="center"><span>n/a</span></p>
  </td>
  <td nowrap>
  <p align="center"><span>n/a</span></p>
  </td>
  <td nowrap>
  <p align="center"><span>n/a</span></p>
  </td>
  <td nowrap>
  <p align="center"><span>n/a</span></p>
  </td>
 </tr>
 <tr>
  <td nowrap valign="bottom">
  <p><span>Public-domain</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Allowed</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Allowed</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
 </tr>
 <tr>
  <td nowrap valign="bottom">
  <a href="http://three.org/openart/license/"><p><span>Open-art</span></p></a>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FFFFBF">
  <p align="center"><span>Share alike</span></p>
  </td>
  <td nowrap style="background: #FFFFBF">
  <p align="center"><span>Share alike</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
 </tr>
 <tr>
  <td nowrap valign="bottom">
  <a href="http://www.gnu.org/licenses/gpl.html"><p><span><acronym title="General Public License">GPL</acronym></span></p></a>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FFFFBF">
  <p align="center"><span>Share alike</span></p>
  </td>
  <td nowrap style="background: #FFFFBF">
  <p align="center"><span>Share alike</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
 </tr>
 <tr>
  <td nowrap valign="bottom">
  <a href="http://www.gnu.org/copyleft/lesser.html"><p><span><acronym title="Lesser General Public License">LGPL</acronym></span></p></a>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Allowed</span></p>
  </td>
  <td nowrap style="background: #FFFFBF">
  <p align="center"><span>Share alike</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
 </tr>
 <tr>
  <td nowrap valign="bottom">
  <a href="http://www.apache.org/licenses/LICENSE-2.0.html"><p><span>Apache 2.0</span></p></a>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Allowed</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Allowed</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
 </tr>
 <tr>
  <td nowrap valign="bottom">
  <a href="http://www.linfo.org/bsdlicense.html"><p><span><acronym title="Berkley Software Distribution">BSD</acronym></span></p></a>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Allowed</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Allowed</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
 </tr>
 <tr>
  <td nowrap valign="bottom">
  <a href="http://mit-license.org"><p><span><acronym title="Massachusetts Institute of Technology">MIT<acronym></span></p></a>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Allowed</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Allowed</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
 </tr>
 <tr>
  <td nowrap valign="bottom">
  <a href="http://creativecommons.org/licenses/by/3.0"><p><span><acronym title="Creative Commons Attribution">CC by</acronym></span></p></a>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Allowed</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Allowed</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
 </tr>
 <tr>
  <td nowrap valign="bottom">
  <a href="http://creativecommons.org/licenses/by-sa/3.0"><p><span><acronym title="Creative Commons Attribution ShareAlike">CC by-sa</acronym></span></p></a>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FFFFBF">
  <p align="center"><span>Share alike</span></p>
  </td>
  <td nowrap style="background: #FFFFBF">
  <p align="center"><span>Share alike</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
 </tr>
 <tr>
  <td nowrap valign="bottom">
  <a href="http://creativecommons.org/licenses/by-nc-nd/3.0"><p><span><acronym title="Creative Commons Attribution Non-Commerical No-Derivatives">CC by-nc-nd</acronym></span></p></a>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
  <td nowrap style="background: #91CF60">
  <p align="center"><span>Yes</span></p>
  </td>
  <td nowrap style="background: #FC8D59">
  <p align="center"><span>No</span></p>
  </td>
 </tr>
</table>


The GPL and LGPL Version 3 prohibits DRM, locked-down firmware, and patent lawsuits.

The BSD license prohibits the use of copyright holder's name for promotion.

The Apache license requires that every file must contain all information about changes, copyrights and patent protection.

The [Black Duck Knowledge Base](http://osrc.blackducksoftware.com/data/licenses/#top20) suggests that GPL2 is the most popular choice.


