---
layout: "../../../../layouts/BlogPost.astro"
title: "Design Patterns"
pubDate: "2022-09-14"
---

## Authors

- Daniela García @dsgarcia8
- Jean Carlos Alarcón @jcalarcon98

## Topics

- [Authors](#authors)
- [Topics](#topics)
- [What are Design Patterns?](#what-are-design-patterns)
- [Difference between Design Pattern and an algorithm](#difference-between-design-pattern-and-an-algorithm)
- [What does the pattern consist of?](#what-does-the-pattern-consist-of)
- [Classification of patterns](#classification-of-patterns)
  - [Creational Patterns](#creational-patterns)
  - [Structural Patterns](#structural-patterns)
  - [Behavioral Patterns](#behavioral-patterns)
- [Why Should I Learn Patterns?](#why-should-i-learn-patterns)
- [Resources to learn design patterns](#resources-to-learn-design-patterns)

## What are Design Patterns?

Design patterns are typical solutions to commonly occurring problems in software design. They are like pre-made blueprints that you can customize to solve a recurring design problem in your code.

## Difference between Design Pattern and an algorithm

Patterns are often confused with algorithms, because both concepts describe typical solutions to some known problems. While an algorithm always defines a clear set of actions that can achieve some goal, a pattern is a more high-level description of a solution. The code of the same pattern applied to two different programs may be different.

## What does the pattern consist of?

Most patterns are described very formally so people can repro- duce them in many contexts. A pattern has the following common sections:

- **Intent of the pattern** briefly describes both the problem and the solution.

- **Motivation** further explains the problem and the solution the pattern makes possible.

- **Structure** of classes shows each part of the pattern and how they are related.

## Classification of patterns

Design patterns differ by their complexity, level of detail and scale of applicability to the entire system being designed.

The most universal and high-level patterns are architectural patterns. Developers can implement these patterns in virtually any language. Unlike other patterns, they can be used to design the architecture of an entire application. All patterns can be categorized by their intent, or purpose:

### Creational Patterns

**Creational patterns** provide object creation mechanisms that increase flexibility and reuse of existing code, list of creational patterns:

- Factory Method
- Abstract Factory
- Builder
- Prototype
- Singleton

### Structural Patterns

**Structural patterns** explain how to assemble objects and class- es into larger structures, while keeping the structures flexible and efficient, list of structural patterns:

- Adapter
- Bridge
- Composite
- Decorator
- Facade
- Flyweight
- Proxy

### Behavioral Patterns

**Behavioral patterns** take care of effective communication and the assignment of responsibilities between objects, list of behavioral patterns:

- Chain of responsibility
- Command
- Iterator
- Mediator
- Memento
- Observer
- State
- Strategy
- Template Method
- Visitor

## Why Should I Learn Patterns?

You can work as a programmer for many years, without knowing a single pattern. So why would you spend time learning them?

- Design patterns are a toolkit of tried and tested solutions to common problems in software design. Even if you never encounter these problems, knowing patterns is still useful because it teaches you how to solve all sorts of problems using principles of object-oriented design.

- Design patterns define a common language that you and your teammates can use to communicate more efficiently. You can say, “Oh, just use a Singleton for that,” and everyone will understand the idea behind your suggestion. No need to explain what a singleton is if you know the pattern and its name.

## Resources to learn design patterns

- [Java Design Patterns](https://github.com/iluwatar/java-design-patterns)
- [Desing Patterns for Humans](https://github.com/kamranahmedse/design-patterns-for-humans)
- [Design Patterns in ES6](https://github.com/ziyasal/design-patterns-and-idioms-in-es6)
- [Design Patterns in JS](https://github.com/fbeline/design-patterns-JS)
- [Python Design Patterns](https://github.com/faif/python-patterns)