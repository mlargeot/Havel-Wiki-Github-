# Development Standards
--- 
## Purpose

This document defines the **development workflow standards** for the **Havel** project, ensuring:

- clear **traceability** of work
- consistent **naming and structure** across contributions
- smooth **integration** within the CI/CD pipeline

## Summary
- [Branch Naming Convention](#branch-naming-convention)
	- [Format](#format-1)
	- [Rules](#rules)
	- [Best Practices](#best-practices)
- [Pull Requests (PR)](#pull-requests-pr)
	- [Title](#title)
	- [PR Description (CPSE Format)](#pr-description-cpse-format)
	- [Merge Policy](#merge-policy)
- [Commits](#commits)
	- [Format](#format-2)
		- [Common Types](#common-types)
## Branch Naming Convention

Every development branch must follow a **consistent naming pattern** to make tracking and collaboration easier.
### **Format**

`dev/{developer}/{OpenProject_id}/{feature}`

Example:

`dev/EdiMalou/47/init_something`

### **Rules**

- **dev/** → required prefix indicating a development branch.
- **{developer}** → Github developer identifier.
- **{OpenProject\_id}** → corresponding task identifier from OpenProject (e.g. `47`).
- **{feature}** → short and descriptive feature name in `snake_case`.

### **Best Practices**

-  Always **branch off from** `dev`.
- Keep names **short, clear, and without special characters**.
- Avoid spaces and uppercase letters in the feature segment.

## Pull Requests (PR)

Each Pull Request should represent a **complete functional unit** tied to a OpenProject task.  
It must be **well-structured**, **documented**, and **review-ready**.

### Title

`{OpenProject_id} {feature}`

Example:

`47 init_something`

### PR Description (CPSE Format)

All PRs must follow the **CPSE** structure to clearly communicate context and intent.

<figure class="table op-uc-figure_align-center op-uc-figure"><table class="op-uc-table"><thead class="op-uc-table--head"><tr class="op-uc-table--row"><th class="op-uc-table--cell op-uc-table--cell_head"><p class="op-uc-p">Section</p></th><th class="op-uc-table--cell op-uc-table--cell_head"><p class="op-uc-p">Description</p></th></tr></thead><tbody><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>Context</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">Brief background about the business or technical context.</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>Problem</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">The problem or need that triggered this development.</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>Solution</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">Description of the implemented solution (technical choices, approach).</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>Expectation (Review)</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">What reviewers should check (expected behavior, tests, edge cases).</p></td></tr></tbody></table></figure>

Example:

```text
Context: Proxmox SDK development in TypeScript
Problem: Project not initialized
Solution: Initialize project & create first SDK tool (version)
Expectation: Complete feature review
```

### Merge Policy

- The **merge message keeps the original PR title**.
- A **merge is allowed only after**:
	- At least one reviewer’s approval
	- Successful CI-CD checks

## Commits

Although all branches are squashed into one commit before merging, local commits should still follow the [**Karma / Conventional Commits convention**](https://karma-runner.github.io/6.4/dev/git-commit-msg.html) for consistency and clarity.

### Format

`<type>(<scope>): <message>`

#### Common Types

<figure class="table op-uc-figure_align-center op-uc-figure"><table class="op-uc-table"><thead class="op-uc-table--head"><tr class="op-uc-table--row"><th class="op-uc-table--cell op-uc-table--cell_head"><p class="op-uc-p">Type</p></th><th class="op-uc-table--cell op-uc-table--cell_head"><p class="op-uc-p">Meaning</p></th></tr></thead><tbody><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>feat</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">New feature</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>fix</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">Bug fix</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>refactor</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">Code improvement without changing behavior</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>chore</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">Technical tasks, dependencies, configuration</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>test</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">Adding or updating tests</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>docs</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">Documentation updates</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>style</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">Code formatting, indentation, lint fixes</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>perf</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">Performance improvements</p></td></tr></tbody></table></figure>

Examples:

```text
feat(api): add endpoint for Proxmox VM deployment
fix(auth): correct token expiration issue
refactor(sdk): simplify Proxmox client initialization
chore(deps): update Docker base image version
```
