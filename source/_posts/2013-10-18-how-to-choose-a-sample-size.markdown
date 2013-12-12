---
layout: post
title: "How to choose a Sample Size"
date: 2013-10-18 09:26
comments: true
categories: [ analysis, data, econometrics, statistics, methodology, research ]
---

I'm often asked to provide advice on this question. The short answer is usually "it depends". This is the longer answer that explains what it depends on!

The size of a sample doesn't need to be as large people usually think. The sample size doesn't actually depend upon the population size (i.e. the things - individuals, organisations, or projects - that the sample is supposed to represent). Indeed National opinion polls usually include no more than 1,000 responses (although they do require an [unbiased sample](http://en.wikipedia.org/wiki/Sampling_bias#Historical_examples)).

So what does sample size depend upon..?
<!-- more -->

## Why choosing a sample size is important

A sample is a subset of a population that you wish to study. A sample is typically chosen for research because it is too difficult or expensive to talk to the whole population. Fortunately statistical theory demonstrates that it is possible for responses taken from a sample to represent a wider population.

This post explains some of things to consider when choosing a representative sample.

## Total sample size

The choice of overall sample size is driven by three statistical considerations

* what effect size you want to capture (i.e. the expected difference between the things you're comparing), 
* how willing you are to miss effects that are present, and 
* how willing you are to mistakenly identify effects that aren't present. 

We can set the latter two according to statistical convention (significance level of 95%, and a statistical power of 80%). Effect size really depends upon the context.

The main unknown here will be the standard deviation - that is to say the extent to which the things you're measuring vary from case-to-case. This, of course, determines the degree to which we can draw conclusions about the whole population by looking at a sample.

We define the effect size relative to the standard deviation. The larger the effect size, the smaller the sample needed to detect it. Drawing on social research, Cohen suggests that 20%, 50%, and 80% (of the standard deviation) represent small, medium, and large effect sizes respectively.


## Representativeness of sub-groups

There are a couple of issues here. First, the overall results should be representative (you don't want to miss-out certain groups) and unbiased (if the sample structure doesn't match the proportion of the overall population the results will need to be weighted). Second, you might want to compare the results of the sub-groups (e.g. treatment vs control groups, cohorts by gender/ age/ ethncitiy, or to see if results change over time/ by location).

Bear in mind the above discussion on sample sizes. The rule of thumb value for sub-samples is to have 30 responses - is consistent with an effect size of 73%. This would, of course, be exhaustive for some of the smaller sub-groups. You may need to combine sub-groups or deal with this variability in the analysis rather than in the sample design - e.g. removing outliers after the responses have been gathered). You might aim for 30 responses among the larger groups but relax this for smaller ones.


## Response rates

This depends on how and who contacts the projects. Fortunately, as a funder you're likely to have their attention! In my experience of contacting beneficiaries on behalf of public/ social projects, a 30% response rate is good going. Don't be surprised if you receive a response rate lower than 1% for an email survey (although the ease of contacting a wide range should mean this is still an effective method). I'd aim to contact about 5 times as many people as you need responses.

The overall decision on sample size ought to take into account the cost and difficulty of acquiring responses and the observed variability of responses. You might want to bootstrap the process by running an initial small sample that would serve to identify whether further booster samples are required (e.g. "the overall result is satisfactory but we're concerned about the apparent discrepancy among very large projects so they'll be the subject of further research"). Bear in mind that this is by no means a precise science and this guidance should be considered in the context of practical concerns. Perhaps the most useful contribution of statistical advice - rather than identifying a magic number - is to help you to understand the overall patterns (variability matters, diminishing returns apply, very large/ small projects might need to be considered separately).
