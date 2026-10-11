<div align="center">
  <img width="400" src="https://raw.githubusercontent.com/OurNeZt/.github/main/assets/OurNeZt-org-transparent-new.png" alt="OurNeZt logo">
</div>

<h1 align="center">OurNeZt</h1>

<p align="center">
  <strong>Plan household finances. Compare homes. Make decisions together.</strong>
</p>

<p align="center">
  A shared platform for household finance and home planning in Singapore.
</p>

<p align="center">
  <a href="https://ournezt.cyrostack.dev">Web app</a>
  &middot;
  <a href="https://github.com/OurNeZt/OurNeZt-deploy#readme">Self-hosting guide</a>
  &middot;
  <a href="https://github.com/orgs/OurNeZt/repositories">Repositories</a>
</p>

<p align="center">
  <a href="https://github.com/OurNeZt/OurNeZt-core/releases"><img src="https://img.shields.io/github/v/release/OurNeZt/OurNeZt-core?label=Core&style=flat-square" alt="Latest Core release"></a>
  <a href="https://github.com/OurNeZt/OurNeZt-web/releases"><img src="https://img.shields.io/github/v/release/OurNeZt/OurNeZt-web?label=Web&style=flat-square" alt="Latest Web release"></a>
  <a href="https://github.com/OurNeZt/OurNeZt-deploy/releases"><img src="https://img.shields.io/github/v/release/OurNeZt/OurNeZt-deploy?label=Deploy&style=flat-square" alt="Latest Deploy release"></a>
</p>

## About OurNeZt

A home decision involves more than its purchase price. Income, CPF, savings, upfront payments, monthly repayments, and everyday household expenses all shape what a family can afford. Location, layout, and viewing impressions matter too.

OurNeZt brings these inputs into a shared family workspace. Families can plan their finances, compare housing scenarios, organise a shortlist, and record evaluations together.

## What you can do

- **Plan household finances:** manage member profiles, income, CPF balances, cash savings, and expenses; review household summaries and projected surplus.
- **Compare housing affordability:** save BTO, resale HDB, EC, and private housing options; compare upfront costs, loan repayments, CPF usage, and cash requirements.
- **Explore future scenarios:** use housing-specific projected income inputs and payment timelines to understand how different plans affect affordability.
- **Organise your shortlist:** group homes by launch or planning category, control which appear on the dashboard, and show or hide an entire group while retaining individual overrides.
- **Evaluate homes consistently:** create a reusable family checklist with optional weights, rate each home, and compare evaluation scores and completion progress.
- **Keep shared observations:** save viewing feedback, agent details, concerns, and follow-up actions in each home's shared notepad, separate from ratings and financial calculations.

The Web application provides responsive dashboards, charts, forms, and comparison views for desktop and mobile. Family roles control access, and administrators manage user provisioning.

## Latest releases

The October 2026 releases add housing checklists, shared notes, and authentication protections across the platform.

| Component | Release | Highlights |
| --- | --- | --- |
| OurNeZt Core | [v1.6.0](https://github.com/OurNeZt/OurNeZt-core/releases/tag/v1.6.0) | Checklist APIs, evaluation scoring, shared notes, authentication limits, and admin authorization for all user creation. |
| OurNeZt Web | [v1.4.0](https://github.com/OurNeZt/OurNeZt-web/releases/tag/v1.4.0) | Checklist management, evaluation comparisons, a shared notes editor, and authentication throttling with retry responses. |
| OurNeZt Deploy | [v1.2.0](https://github.com/OurNeZt/OurNeZt-deploy/releases/tag/v1.2.0) | Pinned release images, authentication and trusted proxy settings, and a Compose override for local source builds. |

Deploy `v1.2.0` includes Helm chart `0.3.0`. Authentication limits recover automatically and are independent per process and replica.

## Repositories

| Repository | Responsibility |
| --- | --- |
| [OurNeZt-core](https://github.com/OurNeZt/OurNeZt-core) | Go gRPC backend: authentication, family access, profiles, financial calculations, housing planning, and PostgreSQL persistence. |
| [OurNeZt-web](https://github.com/OurNeZt/OurNeZt-web) | Browser application: Go and Gin routing, server-rendered templates, dashboards, forms, and responsive planning views. |
| [OurNeZt-deploy](https://github.com/OurNeZt/OurNeZt-deploy) | Docker Compose, the unified Kubernetes Helm chart, runtime configuration, and deployment validation and release packaging. |

## How it fits together

<p align="center">
  <a href="https://raw.githubusercontent.com/OurNeZt/.github/main/assets/OurNeZt-architecture-diag.png">
    <img src="https://raw.githubusercontent.com/OurNeZt/.github/main/assets/OurNeZt-architecture-diag.png" alt="OurNeZt architecture: runtime, API contracts, authentication, persistence, and delivery" width="100%">
  </a>
</p>

Core owns the financial calculations and stored planning data. Web provides the user interface and calls Core through gRPC. Deploy configures the three services for Docker Compose or Kubernetes with Helm.

The stack uses **Go, Gin, gRPC, Protocol Buffers, PostgreSQL, Tailwind CSS, DaisyUI, Docker, Helm, and GitHub Actions**.

## Get started

- **Use the application:** visit [OurNeZt Web](https://ournezt.cyrostack.dev). Accounts are provisioned by an administrator.
- **Run your own instance:** follow the [Deploy README](https://github.com/OurNeZt/OurNeZt-deploy#readme) for released images, local source builds, or Kubernetes installation.
- **Develop a component:** follow the [Core](https://github.com/OurNeZt/OurNeZt-core#readme) and [Web](https://github.com/OurNeZt/OurNeZt-web#readme) guides for setup, configuration, and testing.

For the current release, upgrade Core and complete migrations 6 and 7 before upgrading Web. Configure trusted proxies when Web sits behind an ingress or reverse proxy. The deployment guide covers these upgrade steps.

## Development and contributions

OurNeZt has released Core, Web, and deployment components and continues to evolve. Upcoming work includes [vehicle ownership and COE planning](https://github.com/OurNeZt/OurNeZt-core/issues/62) with a corresponding [Web interface](https://github.com/OurNeZt/OurNeZt-web/issues/66).

Bug reports, feature ideas, documentation improvements, and code contributions are welcome. Open an issue in the relevant repository, follow its contribution instructions, and submit application or deployment changes against `dev`.

## License

Core, Web, and Deploy are licensed under **Apache 2.0**. See the [Core](https://github.com/OurNeZt/OurNeZt-core/blob/stable/LICENSE), [Web](https://github.com/OurNeZt/OurNeZt-web/blob/stable/LICENSE), and [Deploy](https://github.com/OurNeZt/OurNeZt-deploy/blob/stable/LICENSE) licenses for details.

---

<p align="center">
  <sub>Built for clearer finances, organised home planning, and shared decisions.</sub>
</p>
