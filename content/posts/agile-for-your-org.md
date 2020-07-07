---
title: "Agile for Your Org"
tldr: "Practical methods for orchestrating remote, agile development."
date: 2020-07-01T17:04:24-07:00
draft: true
toc: false
images:
tags:
  - development
  - agile
  - linux
  - tools
  - onboarding
---

## What is Agile?
Agile is a methodology for doing work - in my case that work is building Software. I'm
sure at this point, millions of words have been written about Agile development - most by
people much smarter and more credentialed than me! I encourage you to read some of the
[sacred texts](https://agilemanifesto.org/), but I'm going to tell you what works for
*me*.

## The 4 Values
* Individuals and interactions over processes and tools
* Working software over comprehensive documentation
* Customer collaboration over contract negotiation
* Responding to change over following a plan

tl;dr be *proactive*, *open-minded*, and *dedicated* to a creative journey that may not
progress in a straight line!

From a development standpoint, this is where I start:
1. What are we building?
2. Why are we building it?
3. How do we do it without going insane?

Few people who *use* software ever have to grapple with the philosophical ramifications
of codifying obscure incantations and etching them onto millions of devices. Most people
who *make* it understand perfectly well how coercing a machine into performing for humans
proves hazardous to the ego. So, we benefit in the long run by asking a lot of questions
up front. Not *all* the questions - the client is a living, breathing, opinion-changing
beast, but just the bare necessities to give the idea corporeal form. This is called an
MVP - or Minimum Viable Product - and represents the absolute dinkiest version of the
product that can *still provide value* to the users. 

## How to Form Your MVP
I like to think of generating an MVP like a police sketch artist drawing from a witness'
testimony. In an ideal world, you'd be able to just build the product from an exact set of
requirements. Unfortunately, we rarely get a complete & accurate picture from a single
source - a witness spots a tall man wearing a shirt - how many tall men wearing shirts
exist in the world? Likewise, clients may not have a clear or concise vision for the
product they need. It is your job (as a developer, product manager, or other agile
stakeholder) to help extract the vital functions of the would-be application and glue
them together in a pleasant, coherent manner.

- Collect requirements in markdown format
- Create mockups
- Share mockups with client
- Collect feedback

TODO: create cycle diagram above

Things that facilitate your rapid iteration:
- Version Control System (git)
- Kanban (trello, jira)
- Collaboration (slack, teams, jitsi)
- Continuous Delivery/Integration (netlify, github, jenkins)
- KISS documentation (readme, [mdbook](https://rust-lang.github.io/mdBook/))
