# Useful knowledge for the backend software developer

# Table of Contents
* [Introduction](#introduction)
* [Algorithms](#algorithms)
* [Languages](#languages)
* [CVS](#cvs)
* [Databases](#databases)
* [IDE](#ide)
* [Frameworks](#frameworks)
* [Observability](#observability)
* [Microservices](#microservices)
* [Service communications](#service-communications)
* [Balancer](#balancer)
* [Continuous Integration](#continuous-integration)
* [Architecture](#architecture)
* [Responsibilities](#responsibilities)
* [Methodology of Development](#methodology-of-development)

## Introduction
Software development is relatively new profession. It's hard to say when exactly it born, but we could say certainly that it evolves constantly like our big world. New technologies and concepts are constantly being born, some of them evolving, some is dying, in end up we have huge diversity of different technologies.

Here is my knowledge on backend developer. It's not everything I know, but tried to emphasize most important thing need to be known by modern backend java developer. Not all the contents is filled yet, i'll fill it with time.   

## Algorithms
### Structure Data
#### DFS
#### BFS
#### Sliding Window
#### Tree
#### LinkedList
#### HashMap
### complexity
### sorting

## Languages
Language of development in the most starting point of software development. There are huge number of languages. They have different properties like syntax, on which operation system it works, or on which hardware it works.
    
### java
It's one of the most popular languages for software development.
The most rival feature is build once then run anywhere. Java compiler creates byte code from source code. This byte code looks like machine code, i.e. instructions for the processors, but there are no physical processor, in runs on Java Virtual Machine, that exists for almost any popular Operation System(Windows, Linux).

Other things that make it's so popular - the huge number of libraries and technologies with java could be used. 
### scala

## CVS
- git github, ....
- mercury
- svn

## Databases
In order to store files you could use files, think about format, solve issues with multiple using. And other things, but it's better to use ready for this products for storing - databases.
### Relational database
Relational means there is relations between table. E.g. you have client and orders of this client. You could create something like this:

| Client      | cell phone  | Order     |
| ----------- | ----------- | --------- |
| Alex        | 11123       | order1    |
| Alex        | 11123       | order2    |
| Bob         | 33433       | order1    |

in relation world it could consist of two tables: Clients and Orders

Client table

| Id   | Client | cell phone |
| -----| ------ | ---------- |
| 1    | Alex   | 11123      |
| 2    | Bob    | 33433      |

Order table 

| Id | client_id | Order  |
| ---| --------- | ------ |
| 1  | 1         | order1 |
| 2  | 1         | order2 |
| 3  | 2         | order1 |

So here is relation, Order reference to Client by client id.


The commonly used databases:
* posgres
* mysql
* oracle

### key-value
 * redis
 * memcache
### document
 * mongodb
### columns
 * cassandra
### graph
 * neo4j
### search
 * elastic
 * solr

## IDE
Integrated development environment is software that gives you possibility to write code easily. Literally they help you to do it.
### Intelij DEA
### Eclipse

## Frameworks
- Spring, beans, DI/IC

## Streaming
- kafka
- rabbitMQ

## Observability
- SLO/SLI/SLA
- latency/throughput
- opentracing jaeger
- monitoring
- grafana
- kibana

## Microservices
- microservices vs monolith
- you need good reason to use microservices
- in monolith hard to establish borders between components, all the teams work in should use the same libraries
- by microservices you could split on independent supported by separate teams
- docker
- kubernetes, openshift
- stateful, stateless services
- service mesh
- embedded proxy
- sidecar proxy
- envoy, istio
- edge proxy

## Service communications
### gRPC
### rest, soap, ..
### http2
### webservice...
### balancer
In order to spread workload more equally between services [balancer](#balancer) could be used
- ssl, tls, ...

## Balancer
### L4/L7
In general balancer could be divided in two groups: L4 and L7, which connected to the level of OSI model where they used.

L4 on the transport layer, i.e. TCP level. Mostly such balancer are hardware. It doesn't know anything of context of traffic it knows only source and destination, but there are features like ssl that hardly could be fit only in L4 model.

L7 balance relies on application layer so, they could decide balancing strategy based on the traffic.
### Proxy
If you want to hide client from server you use proxy.
### Reverse proxy
If you want to hide server from client, you use reverse proxy. In some situation reverse proxy could be general case for balancer.

## Network
### OSI model
7  layers

## Continuous Integration
- circleci
- jenkins
- teamcity

## Architecture

## Responsibilities
- architecture, provides pros and cons
- writing info about features, discussion on it
- understand domain
- communications

## Tools
- Confluence
- Bugtracking - jira
- plantUML

## Methodology of Development
- Agile
- Waterfall