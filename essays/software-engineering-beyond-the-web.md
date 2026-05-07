---
layout: essay
type: essay
title: "Two Languages, One Codebase: What ICS 314 Taught Me About Software Engineering"
date: 2026-05-06
published: true
labels:
  - Agile Project Management
  - Configuration Management
  - Software Engineering
  - Reflection
---

## Learning Two Languages at Once

Coming to the University of Hawaii as an international student meant I was simultaneously learning two new languages: English and software engineering. While I had some programming experience before ICS 314, the vocabulary of professional software development — pull requests, configuration drift, sprint planning, version pinning — was as foreign to me as English academic writing. What I did not expect was that both challenges would reinforce each other. Learning to communicate precisely in code taught me to communicate more precisely in English, and vice versa.

This essay reflects on two concepts from ICS 314 that I believe extend well beyond web application development: **Agile Project Management** and **Configuration Management**. Both of these disciplines shaped how I think about software engineering as a craft, and both apply equally well to embedded systems, mobile applications, data pipelines, or any collaborative technical project.

## Agile Project Management: A Framework for Uncertainty

**Agile Project Management** is an iterative approach to planning and executing software projects. Rather than specifying every requirement upfront and building toward a fixed endpoint, Agile teams work in short cycles called **sprints** — typically one to three weeks long — and deliver working software incrementally. After each sprint, the team reflects, re-prioritizes, and adjusts. The underlying premise is that requirements change, understanding deepens over time, and flexibility produces better outcomes than rigid up-front planning.

ICS 314 introduced a specific flavor of Agile called **Issue Driven Project Management (IDPM)**, where every unit of work is represented as a GitHub Issue. Each issue is assigned to a team member, associated with a milestone, and tracked on a project board. When work begins, a branch is created from the issue. When it is complete, a pull request is merged and the issue is closed. The board itself — with columns like "Backlog," "In Progress," and "Done" — gives the entire team a live picture of project state at any moment.

During our final project, StudyViser, I found IDPM genuinely valuable — but perhaps not in the way I expected. What surprised me was how much it reduced the communication overhead between teammates. When English is not your first language, team meetings can be exhausting. You process the conversation a beat behind, worry about misunderstanding a task, and sometimes walk away unsure exactly what you agreed to do. The GitHub Issues board sidestepped a significant portion of that friction. I could read an issue description at my own pace, look up unfamiliar vocabulary, and ask clarifying questions in writing rather than in a fast-moving conversation. The written, asynchronous nature of IDPM was, unexpectedly, an accessibility feature.

But the broader point is that Agile is not a web development tool — it is a general framework for managing complexity under uncertainty. A team building firmware for a medical device faces uncertainty just as real as a team building a web app. A group maintaining a data science pipeline with shifting research requirements benefits from sprint planning just as much as a startup building a mobile product. The core insight of Agile — deliver something working, reflect, and adjust — applies wherever humans build software together.

## Configuration Management: Controlling What You Cannot See

**Configuration Management** is the discipline of systematically tracking and controlling changes to software systems, including the code, its dependencies, its environment settings, and its build and deployment configuration. The goal is reproducibility: given the same inputs, the system should behave identically regardless of who runs it, on which machine, or at what point in time.

In ICS 314, configuration management showed up in several concrete forms. We used **Git** for version control, which is the most visible layer: every change to the codebase is recorded, attributed, and reversible. We used **package.json** and a lockfile to pin exact dependency versions, so that running `npm install` on any machine produces the same set of packages. We stored sensitive values — database connection strings, API keys — in `.env` files that were excluded from version control and documented in `.env.example`, so the application could be configured differently for local development and production without leaking credentials into the repository.

Each of these practices is solving the same underlying problem: the gap between "it works on my machine" and "it works everywhere." Without version control, two teammates editing the same file simultaneously produces chaos. Without a lockfile, a dependency update that one person pulls in silently breaks another person's build. Without environment variable management, secrets end up committed to a public repository, and production behavior becomes impossible to reproduce locally.

For me as an international student, configuration management also had a more personal dimension. When I encountered a cryptic error message — often in dense English technical prose — having a reproducible environment meant I could isolate the problem. I knew the error was not caused by a difference in my local setup. I could share the exact error with a teammate or paste it into a documentation search and trust that the context was consistent. Configuration management, in other words, made debugging legible across a language barrier.

Beyond web development, configuration management is essential in virtually every software domain. In machine learning engineering, reproducibility of training runs — pinning dataset versions, model architecture configurations, and library versions — is so critical that entire frameworks like MLflow and DVC exist specifically to address it. In infrastructure engineering, tools like Terraform and Ansible apply configuration management principles to entire server environments, treating infrastructure as code rather than as something administrators configure manually. In embedded systems development, knowing exactly which firmware version is running on which device is a safety requirement, not just a best practice.

## Software Engineering Is a Universal Language

What ICS 314 ultimately taught me is that software engineering — at its best — is a discipline of structured communication. Agile Project Management is a communication protocol for teams navigating uncertainty. Configuration Management is a communication protocol between developers, machines, and time. Both reduce ambiguity and increase shared understanding.

As an international student who spent this semester writing code in TypeScript and prose in English, I found that getting better at one made me better at the other. Precision matters in both. Structure reduces miscommunication in both. And in both, the reader — whether a teammate or a compiler — benefits from clarity over cleverness.

I came into this course thinking I was learning how to build web applications. I am leaving it with something more durable: a vocabulary and a set of practices for building software collaboratively, whatever form that software takes.

### Use of AI
AI tools (Claude) were used to assist with structure, phrasing, and grammar. The core ideas, project context, and personal reflections are my own and are based on my experience during ICS 314.
