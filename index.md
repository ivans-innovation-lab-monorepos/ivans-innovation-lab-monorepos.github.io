---
layout: page
title: Lab - Monorepos
subtitle: Architecture, culture and process
bigimg:
  - "/img/architecture.jpg" : "Architecture"
  - "/img/innovate.jpg" : "Innovate"
  - "/img/digital-transformation.jpg" : "Digital transformation"
---

The intention of this open lab is to build information system of a **fictitious company**. We are going to use different architectural and design patterns to support this. 

This is a **mono-repo** version of the lab, and represents a predecessor of a [multi-repo version](http://ivans-innovation-lab.github.io/). Within this version of the lab we keep all related projects (apps & libs) in one repository.

We have one deployment pipeline for all projects within one repository. In addition, all projects in the repository share the same dependencies. Hence, there are no version conflicts because everyone has to use the same/the latest (SNAPSHOTS) version. And you don't need to deal with a private NPM (JavaScript) or Maven (Java) registry when you just want to use your own libraries.

![Monorepo](https://github.com/ivans-innovation-lab-monorepos/my-company-backend/raw/master/monorepo.png)

At this stage we are able to archive our modules in different packages, and we are making them more reusable. This will enable us to switch from monolithic architectural style to alternative microservices architectural style easier.
