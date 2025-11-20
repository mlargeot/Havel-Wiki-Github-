# Technical Track - Objectives

## Summary

- [1. Introduction](#1.-introduction)
- [2. Purpose of the Document](#2.-purpose-of-the-document)
- [3. Mandatory Objective](#3.-mandatory-objective)
	- [3.1. Evaluating and Integrating New Technologies](#3.1.-evaluating-and-integrating-new-technologies)
	- [3.2. Structure, document, and harden the project’s technical architecture](#3.2.-structure,-document,-and-harden-the-project’s-technical-architecture)
	- [3.3. Planned solutions](#3.3.-planned-solutions)
- [4. Chosen Complementary Objectives](#4.-chosen-complementary-objectives)
	- [4.1. Collaborate with technical experts](#4.1.-collaborate-with-technical-experts)
	- [4.2. Measure, test, and optimize technical performance](#4.2.-measure,-test,-and-optimize-technical-performance)
	- [4.3. Planned solutions](#4.3.-planned-solutions)
- [5. Conclusion](#5.-conclusion)
## 1. Introduction

The Technical Track of the Epitech Innovative Project (EIP) ensures that students not only build functional solutions, but also develop strong engineering rigor, technical leadership, and mature architectural decision-making.

This document outlines the mandatory and optional objectives, the KPIs, and the expected deliverables students must achieve as part of the Technical Track for the Havel project, a cybersecurity-focused challenge deployment system designed to integrate CTF-like functionalities, Docker/VM provisioning, and advanced network scenarios.

## 2. Purpose of the Document

This document provides a formal reference for all obligations and KPIs required for Technical Track validation with mandatory and chosen objectives. It serves three main purposes:

- Guide the team in structuring technical work and prioritizing deep engineering topics.
- Support the mentor in monitoring progress and assessing maturity.
- Inform the evaluation jury during Go/No-Go decisions with clear evidence of rigor, analysis, and innovation.

## 3. Mandatory Objective

### 3.1. Evaluating and Integrating New Technologies

#### Evaluated skills

**Active technology watch**

- Set up a **regular watch** on topics linked to the project: languages, frameworks, protocols, tools, standards, architectures, etc.
- Use **varied, credible sources**: technical blogs, scientific publications, official documentation, GitHub repos, newsletters, Discord, X, etc.
- Identify **emerging trends/solutions** that are **useful** for the project (not merely curiosity)

**Documentation & analysis**

- Write **comparative briefs** or **analysis notes** on the explored tech: advantages, drawbacks, learning curve, project fit.
- Produce **one or more technical benchmarks** between approaches/solutions (performance, scalability, maintainability, ecosystem, etc.).
- Present a **reasoned decision** on choices made (or rejected).

**Concrete application**

- Carry out **1–2 concrete experiments** (POC, mini‑project, tested integration in the repo).
- **Integrate at least one new technology** into the project with working proof and justification.
- Update the project (docs, architecture, code) to reflect adopted evolutions.

**Sharing & openness**

- Participate actively in **tech communities**: exchanges on Discord, StackOverflow, GitHub, specialized forums, etc.
- Document your advances (**README, changelog, wiki, GitHub issues**), and share learnings within the team.

### 3.2. Structure, document, and harden the project’s technical architecture

#### Evaluated skills

**Clear, justified architecture**

- Present the project’s architecture: **components, services, dependencies, data flows, deployment, versioning**, etc.
- **Justify** structural choices: selected technologies, code organization, databases, APIs, frameworks, etc.

**Complete technical documentation**

- Provide a **structured README** including:
	- project purpose,
	- install/deploy,
	- folder/module structure,
	- key commands,
	- environment variables,
	- technical prerequisites.
- Create **at least one advanced document**: architecture diagram, technical use case, business logic, **technical roadmap**, etc.

**Quality, reliability & security**

- Enforce **code standards** (linting, conventions, naming, typing).
- Run **quality analysis tools** (SonarQube, ESLint, Pylint, etc.).
- Provide **unit or validation** tests on **at least one critical module**.
- Implement initial **error handling, logging, and minimal security** (auth, sanitization, backups, …).

### 3.3. Planned solutions

To meet the expectations related to the mandatory objectives, the Havel team plans to implement several measures:

- **To ensure an active technology watch**, regular research will be conducted on the selected technologies. Sources will be referenced and chosen for their relevance (community Discord servers, official documentation, experts, etc.). Each technology will be studied through Proofs of Concept (POCs) and benchmarks before being adopted into the project, with evaluation criteria including performance, usability, learning curve, and limitations.
- **The project will be continuously documented**, and the team intends to participate actively in Discord communities. Some of the identified technical communities include:
    
    - **SimianSec:** A cybersecurity and CTF-oriented server maintained by **[CvxFous](https://tryhackme.com/p/CvxFous)**. This community includes cybersecurity experts as well as junior profiles eager to learn through platforms such as HackTheBox. It is particularly relevant for gathering feedback from potential users (organizers/participants) and obtaining cybersécurity expert insights.
    - **Proxcord:** An unofficial Discord server dedicated to Proxmox. Since the project involves interacting with virtual machines, this community is a valuable source of expertise on virtualization technologies.

- **The project will include full functional and technical documentation**, covering specifications, architectural decisions, and all aspects related to installation, usage, and maintenance.
- **Given that the project revolves around cybersecurity and virtualized environments**, the team aims to build the safest platform possible. Standardization practices will be applied to ensure a stable, secure, and coherent development environment.

These measures may evolve or expand as the Havel project progresses. Any changes will be documented according to their relevance to the project’s development and organization.

## 4. Chosen Complementary Objectives

### 4.1. Collaborate with technical experts

**Identify & approach experts**

- Clearly define the **technical need** or topic to challenge: architecture choice, framework, security, performance, scalability, AI, etc.
- Proactively search for **relevant experts**: GitHub contributors, LinkedIn engineers, community leads, teachers, CTOs, alumni, etc.
- **Professional outreach**: clear message, precise question, appropriate channel

**Structured collaboration**

- Run a **documented exchange**: meeting, written feedback, Discord/GitHub thread, code review, etc.
- Optionally organize a **review session** with an external expert (pair programming, code review, light audit).
- Implement **concrete actions** from the exchange: structure adjustment, technical plan change, new resources, tool adoption, process improvement.

**Capitalize on the exchange**

- Write a **summary/memo**: discussed points, advice received, decisions taken.
- Add the collaboration to the **roadmap** or documentation.
- Valorize when possible: testimonial, mention, quote, public thanks.

### 4.2. Measure, test, and optimize technical performance

**Define key technical metrics**

- Choose 2–3 performance indicators relevant to the project (latency, response time, memory usage, load time, bundle size, CPU, API calls, etc.).
- Integrate these metrics into the dev cycle (dashboard, logs, third‑party tools, tests, etc.).

**Set up automated/manual tests**

- Run load tests, stress tests, and/or simulation scenarios.
- Run resilience tests: error handling, interruptions, unexpected behavior.
- Run comparative efficiency tests: optimized vs. initial version.

**Implement optimizations**

- Analyze bottlenecks and friction points.
- Modify one or more technical bricks (queries, processing, cache, code, …).
- Justify trade‑offs (quality vs. performance vs. cost vs. time).

### **4.3. Planned Solutions**

To meet the expectations related to the complementary objectives, the Havel team plans to implement several measures:

- **To provide a high-quality CTF-hosting solution**, the team intends to collaborate with experts who can offer feedback across multiple areas:

    - **Features:** Gain insight into the needs of organizers and participants regarding the functionalities offered by the platform and its API.
    - **Architecture:** Understand how large-scale CTF events are architected, particularly in relation to resource optimization, credit usage, uptime reliability, and efficient service management. These best practices will be analyzed and applied when relevant.

- The team has already received guidance from technical experts within the Epitech cybersecurity pedagogical team, and aims to collaborate with larger organizations—such as BreizhCTF—to gather high-quality insights. All interactions will be documented, including the feedback received, decisions made, and the contacts involved (who, when, and why).
- **To enable optimization of the platform**, key metrics such as **virtual machine response latency, uptime, deployment time, and resource consumption** will be taken into account when making architectural and technological decisions. These metrics will be measured, tracked, and evaluated over time.
- **The platform will follow a robust testing policy**, relying on both unit and functional tests. Test coverage will be extended across the main features to ensure functional correctness, stability, and code security.

These measures may evolve or expand as the Havel project progresses. Any changes will be documented according to their relevance to the project’s development and organization.

## **5. Conclusion**

The Technical Track defines a rigorous and structured framework that guides the Havel team toward achieving a high level of technical excellence. Through continuous technology monitoring, thoughtful architectural decisions, active community engagement, and collaboration with experts, the project commits to building a reliable, scalable, and security-oriented CTF-hosting platform.

The combination of mandatory and complementary objectives ensures both depth and breadth in the team’s technical approach. The measures outlined throughout this document—ranging from systematic documentation to performance evaluation, testing strategies, and expert contributions—form a coherent methodology that will support the project’s evolution.

As Havel progresses, the team remains committed to iterating, improving, and documenting every significant technical decision. This dynamic and evidence-driven approach will not only strengthen the platform but will also demonstrate the team’s capacity to produce a mature, robust, and well-engineered solution that meets the expectations of the EIP Technical Track.
