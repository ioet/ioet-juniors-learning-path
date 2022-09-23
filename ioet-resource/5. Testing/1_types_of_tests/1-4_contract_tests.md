# Contract testing

## Authors

- Daniela García @dsgarcia8
- Jean Carlos Alarcón @jcalarcon98

## Topics

- [What is Contract Testing?](#what-is-contract-testing)
- [When to use Contract Testing?](#when-to-use-contract-testing)
- [Basic concepts](#basic-concepts)
- [Contract testing types](#contract-testing-types)
  - [Consumer-driven](#consumer-driven)
  - [Producer-driven](#producer-driven)
- [Benefits of contract testing](#benefits-of-contract-testing)
- [Contract testing tools](#contract-testing-tools)
- [References and Additional Resources](#references-and-additional-resources)

## What is Contract Testing?

Contract testing is a way for validating that two distinct systems (such as two microservices) are compatible and can communicate with one another. It captures the interactions that are exchanged between each service, storing them in a contract, which can then be used to verify that both parties adhere to it. [What is contract testing and why should I try it?](https://pactflow.io/blog/what-is-contract-testing/)

![Contract testing](https://s3-ap-southeast-2.amazonaws.com/content-prod-529546285894/2021/03/Screen-Shot-2021-03-29-at-1.04.29-pm.png)

## When to use Contract Testing?

Contract testing is frequently used to test an integration point between various services. They are used in APIs, microservices, and other applications.

It is mostly used for:

- Detecting irregularities in a consumer workflow
- Detecting any service configuration defects
- Keeping the connections safe even when the producer changes any service configuration

## Basic concepts

- Isolated service: An isolated service typically consists of a consumer and a producer. To complete a task, these isolated services may need to interact. A successful interaction would indicate that a consumer and a producer are adhering to a common contract.
- Consumer:  This service is reliant on a producer to do their work.
- Producer: It provides relevant info to the consumer, assisting the consumer in completing their task.

## Contract testing types

### Consumer-driven

Consumer driven contract testing is a type of contract testing that ensures that a provider is compatible with the expectations that the consumer has of it. For an HTTP API (and other synchronous protocols), this would involve checking that the provider accepts the expected requests, and that it returns the expected responses. For a system that uses message queues, this would involve checking that the provider generates the expected message.

### Producer-driven

Producer-driven contract testing is infrequently employed in comparison to consumer-driven contract testing.
A producer is in responsible of constructing a contract between them and the consumer in this testing. The producer then runs multiple build tests to ensure that the contract is met.
If the producer passes all of the test cases, the results are saved in a central repository.
The build and test cases are subsequently executed by the consumer. Both parties interact only after all of the test cases have been passed.

## Benefits of contract testing

Contract tests belong in the "Service Tests" layer since they run rapidly and do not require integration with external systems. Their role is to ensure that the systems with which you integrate are compatible with your code before you deploy it.
![ Practical Test Pyramid ](https://s3-ap-southeast-2.amazonaws.com/content-prod-529546285894/2019/07/image.png)

Contract tests have the inverse qualities of e2e integrated tests:

- They are quick since they do not need to communicate with different systems.
- They are simpler to manage because you do not need to comprehend the complete ecosystem in order to build your tests.
- They are simple to debug and repair because the issue is always limited to the component being tested, thus you usually get a line number or a specific API endpoint that is failing.
- They can be repeated
- They scale: because each component may be verified independently, build pipelines do not grow linearly or exponentially in time.
- They discover problems on developer machines: Prior to publishing code, contract tests can and should be done on development machines.

## Contract Testing Tools

### Pack

[Pack](https://docs.pact.io/) is a command-line tool. This tool has a faster feedback time. It helps with better communication between the consumer and the producer.

### Spring Cloud Contract

[Spring Cloud Contract](https://spring.io/projects/spring-cloud-contract) is primarily suitable for the JVM environment but can be easily extended to a non-JVM environment. This tool is suitable for producer-driven contract testing.

### JOI

[JOI](https://github.com/sideway/joi) allows us to create API contracts for consuming APIs.

[Here](https://www.qentelli.com/thought-leadership/insights/test-automation-age-microservices-strategies-and-challenges) you can check more tools available in the market

## References and Additional Resources

- [What is Contract Testing, and Why Should You Try it?](https://www.qentelli.com/thought-leadership/insights/what-contract-testing-and-why-should-you-try-it#when-to-use-contract-testing)
- [What is contract testing and why should I try it?](https://pactflow.io/blog/what-is-contract-testing/)
- [Consumer-driven contract testing](https://bluesoft.com/blog/consumer-driven-contract-testing-and-mock-testing-meaning/)
- [API contract testing with Joi](https://circleci.com/blog/api-contract-testing-with-joi/)
- [API Contract Testing, Tools and Impressions: REST](https://medium.com/adidoescode/api-contract-testing-tools-and-impressions-1eaa18bc2bda)
- [Testing microservices with consumer-driven contracts](https://openliberty.io/guides/contract-testing.html)
- [Introduction To Contract Testing With Examples](https://www.softwaretestinghelp.com/contract-testing/)
