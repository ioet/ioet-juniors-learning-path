---
layout: "../../../../layouts/BlogPost.astro"
title: "What does CI/CD consist of?"
pubDate: "2022-09-14"
---

## Contributors

- [Josué Cando](https://github.com/JosueOb)

## Content

- [Contributors](#contributors)
- [Content](#content)
  - [Introduction](#introduction)
  - [What is CI/CD?](#what-is-cicd)
    - [Continuous integration](#continuous-integration)
    - [Continuous delivery](#continuous-delivery)
    - [Continuous deployment](#continuous-deployment)
  - [CI/CD benefits](#cicd-benefits)
  - [What are the differences between CI and CD?](#what-are-the-differences-between-ci-and-cd)
- [Conclusions](#conclusions)
- [References](#references)

### Introduction

Continuous integration (**CI**) and continuous deployment (**CD**) describe the key stages in an automated software
development and deployment flow. This flow typically includes design, coding, testing, integration, delivery, validation
and phased deployment activities before operation in a target environment.

**CI** is a software development practice where developers regularly merge their code changes into a central repository,
after which automated builds and tests are run. Their goals are to find and address bugs more quickly, improve software
quality, and reduce the time it takes to validate and release new software updates.

**CD** is a set of practices designed to optimize the process of taking changes from version control to
production. Its goal is to find ways to deliver high-quality, valuable software in an efficient, fast, and reliable
manner.

Therefore, the implementation of CI/CD has changed the way developers and testers ship software. In addition, code
quality is improved, and software updates are delivered quickly and with great confidence that there will be no breaking
changes.

### What is CI/CD?

CI and CD stand for **continuous integration** and **continuous delivery**/**continuous deployment**. Theses allow for
software developers to integrate their feature or service changes continuously and for IT and operations teams to
deliver with the standards, security, and confidence businesses need.

![ci-and-cd](https://assets.website-files.com/5feac9d1cc32ae279e536778/602a3b4cf516c0a3ba5ee3b5_continuous%20integration%20delivery%20deployment.jpeg)

#### Continuous integration

Continuous integration envisages a process under which developers implement incremental updates to a software product.
Initially, all the code written by individual developers gets combined. The CI process ensures that this integrated code
has passed all the essential checklists for business logic, coding and testing, and merged in a common repository
branch. The CI system automatically runs tests to catch quality issues, and developers get quick feedback and can fix
issues immediately.

CI greatly improves the quality and speed of software development. Teams can create more features that provide value to
users, and many organizations now release software every week, every day, or multiple times a day.

#### Continuous delivery

CD ensures that the code changes such as features, bug fixes, and configuration changes are prepared for release to the
production system in a quick, yet safe and sustainable manner.

The goal of continuous delivery is to deliver a packaged artifact into a production environment. Also, CD
responsibilities can include provisioning infrastructure, managing changes (ticketing), deploying artifacts, verifying
and monitoring those changes, and ensuring these changes do not happen if there are any issues.

#### Continuous deployment

The CD in the CI/CD process also stands for continuous deployment. As an extension of continuous delivery, which
automates the release of a production-ready build to a code repository, continuous deployment automates releasing an app
to production. In other words, no manual intervention required. With continuous deployment, DevOps teams set the
criteria for code releases ahead of time and when those criteria are met and validated, the code is deployed into the
production environment. Thanks to this type of automation, organizations are able to be more nimble and get new features
into the hands of users faster.

### CI/CD benefits

- Easier bug fixes
- Reduced project risk
- Improved software quality
- Automate the software release process
- Improve developer productivity
- Find and address bugs quicker
- Deliver updates faster
- Create workflows across the development, testing, and production environments
- Make deployments frictionless without compromising security.
- Automate the repetitive tasks and focus on actual testing.

### What are the differences between CI and CD?

Continuous integration is simply the process of integrating changes made to the code into a mainline code base. For
this, developers use platform specifically designed for this purpose.

In contrast, continuous delivery is the processes that happen after the changes have been integrated in the code base to
bring these changes to customers.

So, the difference between CI and CD is not as much a case that they’re two different approaches, but rather two
complimenting approaches.

The difference between continuous integration and continuous deployment is that continuous deployment deploys changes to
the customers automatically without any human intervention.

Finally, the difference between continuous delivery and continuous deployment is that Continuous delivery is a partly
manual process where developers can deploy any changes to customers by simply clicking a button, while continuous
deployment emphasizes automating the entire the process.

## Conclusions

- CI/CD is a practice that allows rapid changes to software while maintaining system stability and security.
- CI packages and tests software builds and alerts developers if their changes fail any unit tests.
- CD is the automation that delivers applications, services, and other technology deployments to the runtime
  infrastructure and may execute additional tests.

## References

- [What is CI/CD?](https://www.redhat.com/en/topics/devops/what-is-ci-cd#continuous-delivery)
- [What is CI/CD? Everything You Need To Know](https://harness.io/blog/what-is-ci-cd)
- [CI/CD: Continuous Integration & Delivery Explained](https://semaphoreci.com/cicd)
- [Explore CI/CD: Continuous software for continuous change](https://www.ericsson.com/en/ci-cd?gclid=Cj0KCQjwgO2XBhCaARIsANrW2X2i4XzGuAfwKOcaaA5Fuh8IX0UlaR5DXANmB3KAzAOLOa_38Tpw73waAtjMEALw_wcB&gclsrc=aw.ds)
