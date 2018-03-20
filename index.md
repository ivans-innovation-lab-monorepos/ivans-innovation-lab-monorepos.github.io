---
layout: page
title: Lab - Monorepo
subtitle: Architecture, culture and process
bigimg:
  - "/img/architecture.jpg" : "Architecture"
  - "/img/innovate.jpg" : "Innovate"
  - "/img/digital-transformation.jpg" : "Digital transformation"
---

The intention of this open lab is to build information system of a **fictitious company**. We are going to use different architectural and design patterns to support this. 

This lab is a mono-repo version of the [lab (multi-repo version)](http://ivans-innovation-lab.github.io/), and it represents its predecessor. We keep all our libraries and applications in one/two repo/s, and this make our build/deployment pipeline and release management simpler then in a multi-repo environemnt. 

![Monorepo](https://github.com/ivans-innovation-lab-monorepos/my-company-backend/raw/master/monorepo.png)

At this stage we are decoupling our components and modules in different packages and we are making them more reusable. This enables us to switch from monolithic architectural style to alternative microservices architectural style.
