---
layout: page
title: Projects
subtitle: Architecture, culture and process
---

Each project has its own git repository. Repositories are hosted on Github within the ['ivans-innovation-lab' organziation](https://github.com/ivans-innovation-lab).

Apache Maven is used as a project management and comprehension tool. Maven supports project aggregation in addition to project inheritance. Maven processes projects with multiple modules so you can work with them more effectively.

Domain Driven Design is applied through Event Sourcing and CQRS. How Event Sourcing enables deployment flexibility - the monolithic application can be migrated and deployed as a microservices.

Please read the [Documentation](https://www.gitbook.com/read/book/ivans-innovation-lab/my-company).

![Dependiencies - tree](https://github.com/ivans-innovation-lab/ivans-innovation-lab.github.io/raw/master/img/my-company-dependencies.png)

# Monolith

This version of the application is deployed as a single monolithic application. It exposes a REST API consumed by [my-company-angular-fe](https://ivans-innovation-lab.github.io/my-company-angular-fe) application.

## [my-company-monolith](https://ivans-innovation-lab.github.io/my-company-monolith) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-monolith.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-monolith)
Spring Boot. CQRS. Eventsourcing. Axonframework. Event-driven. Docker. REST API.

### dependencies
- [my-company-blog-domain](https://ivans-innovation-lab.github.io/my-company-blog-domain)
- [my-company-blog-materialized-view](https://ivans-innovation-lab.github.io/my-company-blog-materialized-view)
- [my-company-project-domain](https://ivans-innovation-lab.github.io/my-company-project-domain)
- [my-company-project-materialized-view](https://ivans-innovation-lab.github.io/my-company-project-materialized-view)
- [my-company-team-domain](https://ivans-innovation-lab.github.io/my-company-team-domain)
- [my-company-team-materialized-view](https://ivans-innovation-lab.github.io/my-company-team-materialized-view)


##  [my-company-angular-fe](https://ivans-innovation-lab.github.io/my-company-angular-fe) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-angular-fe.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-angular-fe)
Angular 4. Atomic design methodology. Feature and presentational components. Consumes [my-company-monolith](https://ivans-innovation-lab.github.io/my-company-monolith)

# Microservices

This version of the application is deployed as a microservices.

This projects are intended to demonstrate end-to-end best practices for building a cloud native, event driven microservice architecture using Spring Cloud.

## [my-company-blog-domain-microservice](https://ivans-innovation-lab.github.io/my-company-blog-domain-microservice) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-blog-domain-microservice.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-blog-domain-microservice)

BlogPost, command side microservice.

### dependencies
- [my-company-blog-domain](https://ivans-innovation-lab.github.io/my-company-blog-domain)

## [my-company-blog-materialized-view-microservice](https://ivans-innovation-lab.github.io/my-company-blog-materialized-view-microservice) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-blog-materialized-view-microservice.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-blog-materialized-view-microservice)

BlogPost, query side microservice.

### dependencies
- [my-company-blog-materialized-view](https://ivans-innovation-lab.github.io/my-company-blog-materialized-view)

## [my-company-project-domain-microservice](https://ivans-innovation-lab.github.io/my-company-project-domain-microservice) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-project-domain-microservice.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-project-domain-microservice)

Project, command side microservice.

### dependencies
 - [my-company-project-domain](https://ivans-innovation-lab.github.io/my-company-project-domain)

## [my-company-project-materialized-view-microservice](https://ivans-innovation-lab.github.io/my-company-project-materialized-view-microservice) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-project-materialized-view-microservice.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-project-materialized-view-microservice)

Project, query side microservice.

### dependencies
- [my-company-project-materialized-view](https://ivans-innovation-lab.github.io/my-company-project-materialized-view)

## [my-company-registry-backingservice](https://ivans-innovation-lab.github.io/my-company-registry-backingservice) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-registry-backingservice.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-registry-backingservice)

Netflix Eureka is a service registry. It provides a REST API for service instance registration management and for querying available instances. Netflix Ribbon is an IPC client that works with Eureka to load balance(client side) requests across the available service instances.

## [my-company-configuration-backingservice](https://ivans-innovation-lab.github.io/my-company-configuration-backingservice) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-configuration-backingservice.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-configuration-backingservice)

The configuration service is a vital component of any microservices architecture. Based on the twelve-factor app methodology, configurations for your microservice applications should be stored in the environment and not in the project.

## [my-company-authserver-backingservice](https://ivans-innovation-lab.github.io/my-company-authserver-backingservice) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-authserver-backingservice.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-authserver-backingservice)

Authorization server for issuing tokens and authorize requests.

## [my-company-api-gateway-backingservice](https://ivans-innovation-lab.github.io/my-company-api-gateway-backingservice) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-api-gateway-backingservice.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-api-gateway-backingservice)

Implementation of an API gateway that is the single entry point for all clients. The API gateway handles requests in one of two ways. Some requests are simply proxied/routed to the appropriate service. It handles other requests by fanning out to multiple services.

## [my-company-adminserver-backingservice](https://ivans-innovation-lab.github.io/my-company-adminserver-backingservice) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-adminserver-backingservice.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-adminserver-backingservice)

A simple application to manage and monitor microservices.

# Libraries/Components

## [my-company-blog-domain](https://ivans-innovation-lab.github.io/my-company-blog-domain) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-blog-domain.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-blog-domain)  [![release](http://github-release-version.herokuapp.com/github/ivans-innovation-lab/my-company-blog-domain/release.svg?style=flat)](https://github.com/ivans-innovation-lab/my-company-blog-domain/releases/latest)
BlogPost aggregate. Command side. Spring Boot. CQRS. Eventsourcing. Axonframework.

## [my-company-blog-materialized-view](https://ivans-innovation-lab.github.io/my-company-blog-materialized-view) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-blog-materialized-view.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-blog-materialized-view) [![release](http://github-release-version.herokuapp.com/github/ivans-innovation-lab/my-company-blog-materialized-view/release.svg?style=flat)](https://github.com/ivans-innovation-lab/my-company-blog-materialized-view/releases/latest)
BlogPost. Query side - Materialized view. Spring Boot. CQRS. Eventsourcing. Axonframework.

## [my-company-project-domain](https://ivans-innovation-lab.github.io/my-company-project-domain) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-project-domain.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-project-domain) [![release](http://github-release-version.herokuapp.com/github/ivans-innovation-lab/my-company-project-domain/release.svg?style=flat)](https://github.com/ivans-innovation-lab/my-company-project-domain/releases/latest)
Project aggregate. Command side. Spring Boot. CQRS. Eventsourcing. Axonframework.

## [my-company-project-materialized-view](https://ivans-innovation-lab.github.io/my-company-project-materialized-view) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-project-materialized-view.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-project-materialized-view) [![release](http://github-release-version.herokuapp.com/github/ivans-innovation-lab/my-company-project-materialized-view/release.svg?style=flat)](https://github.com/ivans-innovation-lab/my-company-project-materialized-view/releases/latest)
Project. Query side - Materialized view. Spring Boot. CQRS. Eventsourcing. Axonframework.

## [my-company-team-domain](https://ivans-innovation-lab.github.io/my-company-team-domain) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-team-domain.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-team-domain) [![release](http://github-release-version.herokuapp.com/github/ivans-innovation-lab/my-company-team-domain/release.svg?style=flat)](https://github.com/ivans-innovation-lab/my-company-team-domain/releases/latest)
Team aggregate. Command side. Spring Boot. CQRS. Eventsourcing. Axonframework.

## [my-company-team-materialized-view](https://ivans-innovation-lab.github.io/my-company-team-materialized-view) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-team-materialized-view.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-team-materialized-view) [![release](http://github-release-version.herokuapp.com/github/ivans-innovation-lab/my-company-team-materialized-view/release.svg?style=flat)](https://github.com/ivans-innovation-lab/my-company-team-materialized-view/releases/latest)
Team. Query side - Materialized view. Spring Boot. CQRS. Eventsourcing. Axonframework.

## [my-company-common](https://ivans-innovation-lab.github.io/my-company-common) [![CircleCI](https://circleci.com/gh/ivans-innovation-lab/my-company-common.svg?style=svg)](https://circleci.com/gh/ivans-innovation-lab/my-company-common) [![release](http://github-release-version.herokuapp.com/github/ivans-innovation-lab/my-company-common/release.svg?style=flat)](https://github.com/ivans-innovation-lab/my-company-common/releases/latest)
Common and shared libraries. Domain events.

# Automation
[Atomist](https://www.atomist.com/) consumes your code (Java, C#, JavaScript, Scala, Python, Clojure, even Dockerfiles and Maven POMs), understanding your files, classes, variables, exceptions and more. This understanding is used to modify code directly and to connect code changes to runtime changes. 

Atomis is more then the code, it understands the relationship between your code, your tools, your environments, and your running services and brings this information to where you live: chat (Slack).


## [my-company-automations](https://ivans-innovation-lab.github.io/my-company-automations/) [![release](http://github-release-version.herokuapp.com/github/ivans-innovation-lab/my-company-automations/release.svg?style=flat)](https://github.com/ivans-innovation-lab/my-company-automations/releases/latest)
This Atomist project contains a command and event handlers for generating new modules/projects, editing existing projects,...


# Documentation
We use [Gitbook](https://www.gitbook.com/book/ivans-innovation-lab/my-company) to write the documentation.

## [my-company-documentation](https://github.com/ivans-innovation-lab/my-company-documentation) 
Gitbook documentation for the lab is saved in this repository. The documentaion is available for reading here: https://www.gitbook.com/read/book/ivans-innovation-lab/my-company

## [my-company-architecture-overview](https://github.com/ivans-innovation-lab/my-company-architecture-overview)
Visualize the architecture with [Structurizr](https://structurizr.com) ([4C model](https://c4model.com/))

 - [Monolithic](https://structurizr.com/share/36994#Context)
 - [Microservices](https://structurizr.com/share/22311#Context)

Need Help?  [Join our Slack team][slack].

[idugalic]: http://idugalic.pro
[lab]: http://lab.idugalic.pro
[slack]: https://communityinviter.com/apps/idugalic/idugalic