---
title: Write better documentation with Gherkin Syntax
description: Write better acceptance criteria and test cases with Gherkin, an
  indentation structured and line oriented language.
author: Mitch Wilston
date: 2022-06-27T00:05:52.262Z
tags:
  - tips
---
## What is Gherkin and why should I care?

Love it, hate it, or, *really* hate it - documentation is a critical part of software development. Gherkin comes in handy - especially when documenting user flows - as a way to standardize that documentation in an easy-to-read format that anyone can understand. At the beginning of a project it can help stakeholders, product and developers understand the expected behavior of a feature before a line of code is written. And, at the end of the development process it performs double duty as behavior-driven test cases.

## Gherkin's Syntax

One of the biggest benefits is that it uses standard English (or, your team's language of choice). The basic syntax requires almost no explanation:

*Feature: Title of the Scenario*
**Given** \[Preconditions]
**When** \[Action takes place]
**Then** \[Output]

An actual feature might be documented like this:

*Feature: Blog publish button*
**Given** User has populated rich text editor with content
**When** User clicks 'Publish' button in content management system
**Then** article is published and shows up on site

In reality, a little more context is generally needed, but the syntax is readily expandable with some common keywords (when, then, and, but).

*Feature: Blog publish button*
**Given** User has populated rich text editor with content
**When** User clicks 'Publish' button in content management system
   ** And** There are no errors
**Then** Article is published
   **And** Article's URL is added to sitemap
   **And** Article appears on recently published page
   **And** Modal appears to user and says 'Article has been published at \[timestamp]

## Additional Gherkin Resources

Any given feature might have several Gherkin snippets which provides a lot of utility in a test-driven development environment. If the documentation is done well, there shouldn't be any surprises at the end of the sprint because the team has been referring to and testing against the Gherkin scenarios during development.

There are handful of tools that are built around the general (but often modified) syntax, but the benefit of its simplicity is it can be used in whatever ticket tracking software you're using. If you do want to check out some of the solutions on the market, [Cucumber](https://cucumber.io/docs/gherkin/reference/) seems to be the most popular and has pretty good documentation that is useful even outside of their platform. [Behat ](https://docs.behat.org/en/latest/)is another good one, and [their documentation](https://docs.behat.org/en/v2.5/guides/1.gherkin.html) might be even better.