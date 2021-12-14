---
layout: post
title: Integration of Graphs from Different Data Sources Using Crowdsourcing
categories:  
  - data integration
tags:
  - paper review
  - data integration
---

## Intro
*Younghoon Kim, Woohwan Jung, Kyuseok Shim, Integration of graphs from different data sources using crowdsourcing, Information Sciences, 2017*

This paper presents an efficient algorithm to integrate two graphs collected from different sources using crowdsourcing systems.

<!--more-->

![fig2](/assets/fig/integration-of-graphs/fig2.jpg)

## Problems to Think about
- Schema matching for graphs
- 

## Notions

### Graph Integration
- a type of entity resolution that merges at least two graphs obtained from different sources that concern the same real-world entities
- a general approach to graph integration is to select an object from a graph and determine its corresponding object appearing in the other graph that refers to the identical entity based on the attributes of nodes or the structural similarities in their neighborhood

### Network Alignment
- **Entity resolution** is the process of identifying distinct objects to merge databases or remove duplicates in a database.
- Network alignment is an entity resolution problem seeking isomorphisms using the neighborhood topology between different but similar graphs.
- Network alignment has attracted much attention because of its many potential applications including the integration of different movie databases IMDB and DBpedia, user linkage between different social media sites such as Facebook and Twitter, as well as the merging of the literature databases like DBLP and CiteULike.
- In this paper, **Network Alignment** and **Graph Integration** are used as a synonym.

### Active Learning
- Active learning is a kind of semi-supervised machine learning in which we interactively request new data to users for further training.

## Preliminaries

### Integration of graphs with different schemas
- schema matching has been extensively studied for relational database [8] and XML [29]
- [8] [P. Buneman , S.B. Davidson , A. Kosky , Theoretical aspects of schema merging, in: Proceedings of the International Conference on Extending Database Technology, 1992, pp. 152–167.](https://link.springer.com/chapter/10.1007%2FBFb0032429)
- [29] [E. Rahm , P.A. Bernstein , A survey of approaches to automatic schema matching, VLDB J. 10 (4) (2001) 334–350.](https://link.springer.com/chapter/10.1007%2FBFb0032429)
- assume that the graphs have identical schemas

### Problem Definition
- compute the most precise matches between two graphs by requesting annotators within a limited budget in a crowdsourcing system such as Amazon Mechanical Turk
- Assuming that we pay a fixed reward to annotators for each query, we must not only select the most informative query nodes to ask to annotators, but also match two graphs as accurately as possible with the available labels obtained from the crowd.

![fig3](/assets/fig/integration-of-graphs/fig3.jpg)
![fig3-2](/assets/fig/integration-of-graphs/fig3-2.jpg)
