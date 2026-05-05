# AI Use Case Evaluation Portal

A governance portal for prioritizing AI use cases with security, privacy, ethics, value, and feasibility evidence.

This repository provides a production-minded PHP 8.x and MySQL 8.0 portal aligned with themes from Musaab Hasan's book, [Artificial Intelligence for Security Culture Transformation](https://www.amazon.com/Artificial-Intelligence-Security-Culture-Transformation/dp/3639876954). It translates the book's security culture transformation concepts into a working application foundation that can be extended for institutional, enterprise, and professional development contexts.

## Book Alignment

- Primary reference: **Appendix B: AI Implementation Resources**
- Transformation theme: AI use case evaluation, data readiness, ethical controls, security value, and implementation feasibility.
- Broader framing: moving from compliance-centered activity to measurable security culture, adaptive learning, and organizational resilience.

## Core Capabilities

- Role or unit assessment intake with CSRF protection and server-side validation.
- Weighted scoring model with maturity bands.
- MySQL schema for assessments, dimension scores, initiatives, evidence, and audit records.
- Dashboard view with maturity score, assessment volume, initiative tracking, and dimension cards.
- Roadmap view for implementation workflows and improvement planning.
- JSON summary endpoint for integration with reporting tools.
- Docker-based local development environment.
- Lint and self-test scripts for maintainability.

## Assessment Dimensions

- **Strategic Alignment**: Measures fit with security culture and business outcomes.
- **Value Potential**: Assesses expected risk reduction, learning improvement, or efficiency gain.
- **Data Readiness**: Measures quality, availability, minimization, and governance of required data.
- **Implementation Feasibility**: Assesses technical, operational, and integration feasibility.
- **Privacy and Ethics**: Tracks fairness, transparency, consent, explainability, and oversight.
- **Operational Resilience**: Measures monitoring, fallback, accountability, and support readiness.

## Operating Workflow

- Register a proposed AI use case with owner, purpose, data needs, and expected value.
- Score the use case across strategic, technical, ethical, and operational dimensions.
- Route high-value and high-risk use cases for deeper governance review.
- Track approved pilots through evidence, controls, and post-implementation outcomes.

## Quick Start

```bash
cp .env.example .env
docker compose up --build
```

Then open:

- Application: `http://localhost:8080`
- Health endpoint: `http://localhost:8080/health`
- JSON summary: `http://localhost:8080/api/summary`

## Local Checks

```bash
php bin/lint.php
php bin/test.php
```

## Repository Structure

```text
public/              Web entry point and assets
src/                 PHP application services, repository, and support classes
config/              Portal configuration and scoring dimensions
database/            MySQL migration and seed data
docs/                Architecture, security, testing, and extension documentation
bin/                 Developer and release checks
```

## Production Notes

- Store database credentials and application secrets outside source control.
- Enforce HTTPS at the reverse proxy or load balancer.
- Use least-privilege database users.
- Route logs and audit records to approved monitoring systems.
- Review assessment data retention rules before collecting identifiable responses.

## License

MIT License. See [LICENSE](LICENSE).
