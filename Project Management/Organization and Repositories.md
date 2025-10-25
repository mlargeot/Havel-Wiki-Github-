# Organization and Repositories

## Summary

- [Organization - Havel](#organization---havel)
- [Repositories](#repositories-1)
	- [Roles](#roles)
	- [Branch Protection Policy](#branch-protection-policy)
		- [Protected Branches](#protected-branches)
		- [Protection Rules](#protection-rules)
- [Best practices](#best-practices)
	- [Repositories](#repositories-2)
- [Enforcement Responsibility](#enforcement-responsibility)
## Organization - Havel

The **[Havel](https://github.com/HavelCTF)** GitHub organization centralizes all code, components, documentation, and tooling related to the Havel project.  
Its goals are:

- To provide a **single source of truth** for all project modules and integrations
- To **encapsulate separation of concerns** via dedicated repositories for frontend, backend, infrastructure, etc.
- To enforce **consistent structure, standards, and workflows** across repositories
- To facilitate **collaboration, code sharing, modular growth, and deployment automation**

## Repositories

### Roles

<figure class="table op-uc-figure_align-center op-uc-figure"><table class="op-uc-table"><thead class="op-uc-table--head"><tr class="op-uc-table--row"><th class="op-uc-table--cell op-uc-table--cell_head"><p class="op-uc-p">Repository</p></th><th class="op-uc-table--cell op-uc-table--cell_head"><p class="op-uc-p">Purpose / Description</p></th></tr></thead><tbody><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>ProxmoxSDK</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">SDK bridging the interface with the Proxmox API for VM management and orchestration.</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>epitech-monorepo</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">A monolithic repository that <strong>mirrors</strong> various project repositories for the <i>Epitech</i> framework/integration, used in the EIP project context.</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>frontend</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">The user-facing interface of the Havel platform.</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>docs</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">User documentation, technical documentation, and technology watch / research (i.e. monitoring new tech) on GitHub.</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>functions</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">Collection of serverless / backend-as-a-service (BaaS) functions, utilities, and glue code (e.g., custom logic, API endpoints).</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>landing-page</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">The showcase / marketing / public presentation site for Havel.</p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>PoC-CTFd</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">A plugin / extension for CTFd to deploy challenge instances via Docker, integrating with Havel’s infrastructure <strong>developed before project validation by EPITECH as a PoC to demonstrate our ability to deploy instances such as containers.</strong></p></td></tr><tr class="op-uc-table--row"><td class="op-uc-table--cell"><p class="op-uc-p"><strong>backend</strong></p></td><td class="op-uc-table--cell"><p class="op-uc-p">Core backend services, APIs, business logic, authentication, data storage, orchestration of modules.</p></td></tr></tbody></table></figure>

### Branch Protection Policy

The following **branch protection rules** apply to all repositories within the **Havel** organization to maintain consistency, prevent accidental merges, and ensure code quality across all projects.

#### Protected Branches

| Branch    | Description                                                                |
| --------- | -------------------------------------------------------------------------- |
| `main`    | Production-ready branch. Used for stable releases and public deployments.  |
| `develop` | Integration branch. Contains tested and validated features before release. |

#### Protection rules

1. **Require Pull Request Reviews**
	- All changes must go through a Pull Request (PR).
	- At least **1 reviewer approval** is required before merging.
	- Reviewers must verify:
		- Code quality and naming conventions.
		- Test success and CI pipeline status.
		- PR description follows [**CPSE** format](https://github.com/mlargeot/Havel-Wiki-Github-/blob/main/Project%20Management/Development%20Standards.md#pr-description-cpse-format)

2. **Require Status Checks to Pass**
	- CI/CD workflows must complete successfully before merge.
	- Minimum checks:
		- Linting
		- Unit / Integration Tests
		- Build Success
	- Repositories using Docker or SDKs must also pass **integration tests**

3. **Require Up-to-Date Branches**
	- Feature branches must be **rebased or merged** with the latest `develop` before merge.
	- Prevents outdated code or conflicts on `main` and `develop`.

4. **Restrict Force Pushes & Deletions**
	- Force pushes are **disabled** on all protected branches.
	- Deletion of `main` or `develop` branches is **forbidden**.

## Best Practices

#### Repositories

**Modularity & Decoupling**
- Each repository should focus on a single responsibility (e.g. UI, API).
- Avoid tight coupling; expose well-defined interfaces (SDKs, APIs).

**Shared Dependencies & Versioning**
- Use [semantic versioning](https://semver.org/) where applicable.
- Treat **ProxmoxSDK** as a shared library—changes must maintain backward compatibility when possible.

**Documentation & README**
- Each repo must include a `README.md` with purpose, setup, usage, and contributor instructions.
- Link to **docs** for deeper architectural explanations, API references, and design decisions.

**CI / CD & Automation**
- Use GitHub Actions (or equivalent) in each repo to run tests, linting, builds, deployments.
- Automate publishing, version tagging, and inter-repo integration where necessary.

**Code Ownership & Access**
- Use branch protection, required reviews, and enforce merging standards.

## Enforcement Responsibility

- **Organization admins** enforce and review protection settings monthly.
- **Repository maintainers** ensure compliance within their scope.
- Violations (e.g., direct commits, bypassing CI) must be documented and justified.

