# Documentation Guide

This is a brief guide on how to document different types of information within software projects. Every project has different key aspect. So build your own toolbox out of it. This guide covers general technical and non technical documentation. It does not deal with documentation in code.

First of all writing documentation is more kind of a mindset than everything else. It is about you and your work and less how your (team’s) workflows are or which tools you use. Starting a documentation is the easy part. The hard part comes with maintenance. No doubt you get the easy part on yourself. This guide takes you on the journey to get the hard part easy too.

## Where to put the documentation

Ask yourself who should read the documentation. For technical people the readme is the perfect entry point. Which can be expanded to a simple file system based structure of markdown files.  
For non technical people confluence (or project wiki) should fit your needs. Keep in mind that you can start where you are. If there is a Readme.md take it. You can move the contents later within a documentation (or readme) day.

Feel free to use our [readme template as a starter.](../doc-templates/README.md)

## How to maintain a documentation

To keep your documentation right, make it part of your personal and your team's development process and mindset. Create rules that fit your and your team’s needs: No feature merge without documentation, organize documentation days, etc. 
Adapt your team's workflows and take information that still exists when starting the documentation. User stories and tickets are a good starting point. You just have to move them to your documentation place and give them a review when development has finished.
Everyone who is developing software does some kind of technical concept. Write it down and give it a review when development has finished.

Keep in mind that your documentation does not have to be perfect. Your documentation has to be good or at least okay. It should be good to read. It may be fun to read. It never has to be wrong over a period of time.

**Focus on the content. _Always_.**

## Who and How

Everyone who's involved in project development should participate. As a rule of thumb every code change should be accompanied by a documentation change.

## When

The most important rule is to document regularly. Every project has many suitable possibilities when documentation can happen. Or at least when to check if a documentation is needed.

- Code changes
- Sprint reviews
- Start of feature development
- End of feature development

The best choice you can make is to take what you already have. As mentioned in section [How to maintain a documentation](#how-to-maintain-a-documentation), documenting is more a task of collecting existing information as producing content from scratch. Use what you have: User stories, task descriptions, estimations.

When you start documenting, we recommend that you nominate a responsible person. 

## What to document

### Project setup

The goal is to get every new developer to run the project setup on its own. We highly recommend documenting the project setup within the Readme file of your project and [applying the Readme Day](https://github.com/avenga/coding-guidelines/blob/master/general/readme-day.md).

### System and Software Architecture

The documentation of the software and system architecture describes the big picture of an application. You don’t need to go too much into detail. The goal is to give the viewer an idea of which systems are involved. The system architecture could be a good starting point to dive deeper.

> **Tip:** Use flow charts to visualize the system architecture.

- Containers & Volumes
- Environments
- Deployment pipeline
- Services
- 3rd party dependencies

### APIs

We highly recommend describing your APIs with an OpenAPI (former Swagger) specification. The specification acts as a single source of truth for your system APIs and technical dependencies outside of the project too.

### Features Over Time

Feature documentation should reflect the current state of requirements from a technical perspective. And how these requirements are fullfilled. You should extend the topics by actual examples and exceptions. Especially when no unit tests exists.

The feature documentation acts as single source of truth.

### Contributing

Tell the people how to contribute to the project. The contribution documentation usually consists of several topics. Best place to store the contribution documentation is the `CONTRIBUTING.md.`

- [git branch model and workflow](./avenga-git-guidelines.md)
)
- [merge request/code review rules](./Code-review-rules.md)
- definition of done
- the ticket workflow
- [coding tools config](./coding-tools-configs.md)
- handover rules to other project participants like QA oder UI/UX
- etc.

### Project Sheet

Use the [project sheet template](../doc-templates/PROJECT_SHEET.md) as a starting point. Where participants get the big picture of your project.
