# Documentation Guide

This is a brief guide on how to document different types of information within software projects. Every project has different key aspects so build your own toolbox out of it. This guide covers general technical and non technical documentation. It does not deal with documentation in code.

First of all writing documentation is more kind of a mindset than everything else. It is about you and your work and less how your (team’s) workflows are or which tools you use. Starting a documentation is the easy part. The hard part comes with maintenance. No doubt you get the easy part on yourself. This guide takes you on the journey to get the hard part easy too.

### Where to put the documentation

Ask yourself who should read the documentation. For technical people the readme should be okay. For non technical people Confluence (or project wiki) should fit your needs. Keep in mind that you can start where you are. If there is a Readme.md take it. You can move the contents later within a documentation (or readme) day.

### How to maintain a documentation

To keep your documentation right, make it part of your personal and your team's development process and mindset. Create rules that fit your and your team’s needs: No feature merge without documentation, organize documentation days, etc. 
Adapt your team's workflows and take information that still exists when starting the documentation. User stories and tickets are a good starting point. You just have to move them to your documentation place and give them a review when development has finished.
Everyone who is developing software does some kind of technical concept. Write it down and give it a review when development has finished.

Keep in mind that your documentation does not have to be perfect. Your documentation has to be good or at least okay. It should be good to read. It may be fun to read. It never has to be wrong over a period of time.

**Focus on the content. Always.**

## Who and How

Assigning all involved developers to execute a Documentation Day, one after another, is a good idea. Introducing new developers by having them execute the Documentation Day will provide great insight and valuable feedback, as well as asking developers who are not involved in the project.

The following steps are one possible way for the Documentation Day:

tbd

If possible, fix all identified problems directly and update the documentation regardingly. Otherwise try to schedule the issues to have them fixed at least until the next Documentation Day.

## When

The most important rule is to document regularly. Every project has many suitable possibilities when documentation can happen. Or at least when to check if a documentation is needed.

Sprint Reviews
Start of feature development
End of feature development
etc.

The best choice you can make is to take what you already have. As mentioned in section [How to maintain a documentation](#how-to-maintain-a-documentation), documenting is more a task of collecting existing information as producing content from scratch. Use what you have: User stories, task descriptions, estimations.

When you start documenting, we recommend that you nominate a responsible person. 

### What to document

#### Project setup

The goal is to get every new developer to run the project setup on its own. We highly recommend documenting the project setup within the Readme file of your project and [applying the Readme Day](https://github.com/avenga/coding-guidelines/blob/master/general/readme-day.md).

#### (System) Architecture and Infrastructure

The documentation of the system architecture and infrastructure describes the big picture of an application. You don’t need to go too much into detail. The goal is to give the viewer an idea of which systems are involved. The system architecture could be a good starting point to dive deeper.

> **Tip:** Use flow charts to visualize the system architecture.

Containers & Volumes
Environments
Deployment pipeline
Services
3rd party dependencies

#### APIs 

We highly recommend describing your APIs with an OpenAPI (former Swagger) specification. The specification acts as a single source of truth for your system APIs and technical dependencies outside of the project too.

#### Features Over Time 

tbd

(one single point of truth where anybody can see the current requirements for a given feature. Should solve problem that requirements are spread across JIRA-Tickets)

#### Git

 (contribution.md in repo? Confluence?)

Branche Model, e.g. [GitFlow]()
[Reviews](https://github.com/avenga/coding-guidelines/blob/master/general/Code-review-rules.md)
[Git Guidelines](https://github.com/avenga/coding-guidelines/blob/master/general/avenga-git-guidelines.md)

#### Ticket-Flow?

QA
UX Handover and Review
DEV

#### Definition of Done?

Describe your team's definition of done.

#### Project Sheet 

[Project Sheet](https://github.com/avenga/coding-guidelines/blob/master/doc-templates/PROJECT_SHEET.md)
