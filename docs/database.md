# Database Schema

The portal uses MySQL 8.0 with `utf8mb4` collation.

## Tables

- `dimensions`: scoring dimensions and weights.
- `assessments`: assessment subject, weighted score, maturity band, and notes.
- `assessment_scores`: per-dimension scoring evidence.
- `initiatives`: improvement initiatives linked to impact areas.
- `evidence_items`: examples and supporting evidence records.
- `audit_events`: system activity trail.

## Portal Dimensions

- `strategic_alignment`: Strategic Alignment - Measures fit with security culture and business outcomes.
- `value_potential`: Value Potential - Assesses expected risk reduction, learning improvement, or efficiency gain.
- `data_readiness`: Data Readiness - Measures quality, availability, minimization, and governance of required data.
- `implementation_feasibility`: Implementation Feasibility - Assesses technical, operational, and integration feasibility.
- `privacy_ethics`: Privacy and Ethics - Tracks fairness, transparency, consent, explainability, and oversight.
- `operational_resilience`: Operational Resilience - Measures monitoring, fallback, accountability, and support readiness.

## Seeded Initiatives

- AI use case intake workflow (Governance, high)
- Data readiness checklist (Data Office, high)
- Ethical review board cadence (Risk and Compliance, high)
