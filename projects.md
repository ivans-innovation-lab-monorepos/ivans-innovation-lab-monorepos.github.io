---
layout: page
title: Projects
subtitle: Architecture, culture and process
---

The source code of this lab is open, and hosted on Github within the ['ivans-innovation-lab-monorepos' organziation](https://github.com/ivans-innovation-lab-monorepos). 

Github organization is structured in two repos:
- [Backend](https://ivans-innovation-lab-monorepos.github.io/my-company-backend)
- [Frontend](https://ivans-innovation-lab-monorepos.github.io/my-company-frontend)

## [Backend](https://ivans-innovation-lab-monorepos.github.io/my-company-backend)
Exposes a REST API to be consumed by [internal employees or partners](http://idugalic.pro/2017-12-26-API-Strategy/).

Apache Maven is used as a project management and comprehension tool. Maven supports project aggregation in addition to project inheritance. Maven processes projects with multiple modules so you can work with them more effectively.

![Dependiencies - tree](https://github.com/ivans-innovation-lab/ivans-innovation-lab.github.io/raw/master/img/my-company-dependencies.png)


## [Frontend](https://ivans-innovation-lab-monorepos.github.io/my-company-frontend)
It conusumes a [REST API](https://ivans-innovation-lab-monorepos.github.io/my-company-backend).

This application is generated with Angular CLI and [Nrwl](https://nrwl.io/nx) extensions for Angular. 

Instead of having a large monolith, we have dozens of small libraries with well-defined public APIs (and an Nx Workspace ensures you only use your libraries’ public APIs). The libraries are hosting Angular modules.
