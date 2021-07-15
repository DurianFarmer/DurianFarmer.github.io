---
layout: post
title: Markdown Cookbook
categories:  
  - data integration
tags:
  - paper review
  - data integration
---

# Intro
This paper presents an efficient algorithm to integrate two graphs collected from different sources using crowdsourcing systems.

<!--more-->

![fig2](/assets/fig/2021-07-15-integration-of-graphs/fig2.jpg)

# Notions

### Graph Integration
- a type of entity resolution that merges at least two graphs obtained from different sources that concern the same real-world entities
- a general approach to graph integration is to select an object from a graph and determine its corresponding object appearing in the other graph that refers to the identical entity based on the attributes of nodes or the structural similarities in their neighborhood

### Network Alignment
- **Entity resolution** is the process of identifying distinct objects to merge databases or remove duplicates in a database.
- Network alignment is an entity resolution problem seeking isomorphisms using the neighborhood topology between different but similar graphs.
- Network alignment has attracted much attention because of its many potential applications including the integration of different movie databases IMDB and DBpedia, user linkage between different social media sites such as Facebook and Twitter, as well as the merging of the literature databases like DBLP and CiteULike.

### Active Learning
- Active learning is a kind of semi-supervised machine learning in which we interactively request new data to users for further training.


