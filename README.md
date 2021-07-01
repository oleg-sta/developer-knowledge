# Useful knowledge for the backend software developer

# Table of Contents
* [Introduction](#introduction)
* [Algorithms and Data Structure](#algorithms)
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

Here is my knowledge for backend software developer. Please use it.   

## Algorithms and Data Structure
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

## Version Control
* [git](https://git-scm.com/)
* svn


## Databases
In order to store files you could use files, think about format, solve issues with multiple using. And other things, but it's better to use ready for this products for storing - databases.
It's considered that NoSQL databases could be horizontally scaled, SQL only vertically. 
### Relational database
* [postgres](https://www.postgresql.org/)
* [mysql](https://www.mysql.com/)
* oracle
### Non-relational(NoSQL)
#### key-value
 * redis
 * memcache
#### document
 * mongodb
#### columns
 * cassandra
#### graph
 * neo4j
#### search
 * elastic
 * solr

## Interactive Development Environment
Integrated development environment is software that gives you possibility to write code easily. Literally they help you to do it.
### Intelij DEA
### Eclipse

## Frameworks
- Spring, beans, DI/IC

## Streaming
* [kafka](https://kafka.apache.org/)
* [rabbitMQ](https://www.rabbitmq.com/)

## Observability
* [SLO/SLI/SLA](https://sre.google/sre-book/service-level-objectives/)
* latency/throughput
* opentracing jaeger
* monitoring
* grafana
* kibana

## Microservices
### microservices vs monolith
- you need good reason to use microservices
- in monolith hard to establish borders between components, all the teams work in should use the same libraries
- by microservices you could split on independent supported by separate teams
### Docker
Lightweight version of virtual machine, but it doesn't. It works at first on linux, on windows it just started to be implemented. Main idea it uses core of the linux, because it's stable enough and create isolate environment from other processes.
### Kubernetes
Orchestration for a lot of services. Uses pods as minimal thing. On Pods could be several container, but usually one.
Type of services:
* Stateful
* Stateless
### Openshift
Red Had implementation that uses Kubernetes under the hood. It includes UI, aggregated command line, images stores and other features. 
### service mesh
#### Embedded proxy
Proxy as a library. Hard to implement because for each different language required their own library. But fastest.
#### Sidecar proxy
Proxy that started near service, e.g. on the same pod. Service sends request to sidecard proxy, then proxy reroute it.
#### Envoy
Sidecar proxy written on C++. Supports http, http2, grpc, databases connections.
Could also be used as edge proxy.
#### Istio
Control for traffic, secure, rules, circuit braking.
#### Edge proxy
Proxy before service mesh, something like reverse proxy.

## Service communications
### gRPC
uses two main things:
* protobuf
* http/2

Protobuf is way for describe api.
http2 use the same channel for bidirectional requests.

built in features:
* timeouts, you could always set timeouts in the request

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
[OSI(Open Systems Interconnection Model)](https://en.wikipedia.org/wiki/OSI_model) conceptual model that shows the levels of system interaction.

## Continuous Integration
Helps to automate building
* [circleci](https://circleci.com/)
* [jenkins](https://www.jenkins.io/)
* [teamcity](https://www.jetbrains.com/teamcity/)

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