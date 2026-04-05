# Governance and LGPD Baseline

## Purpose

This repository is a portfolio platform and analytics scaffold, not a production system handling customer records.
Even so, the project now documents a governance and privacy baseline so future integrations can evolve from a defined control surface instead of ad hoc decisions.

## Current Position

- the root sample dataset contains portfolio metadata only
- no personal data is required for the current root-level runtime
- the current LGPD assessment for the root scaffold is `not applicable for the current sample`
- privacy and retention controls are still documented because the platform is designed to be extensible

## Current Control Surface

- data inventory in `config/data_governance.json`
- dataset classification and retention metadata
- explicit statement of whether personal or sensitive personal data is present
- runtime policy checks covering inventory, retention, and LGPD positioning
- sanitized governance summary exposed in Streamlit and API

## Minimum Governance Standard

Each dataset integrated into this scaffold should define:

- business owner
- classification
- whether personal data is present
- whether sensitive personal data is present
- lawful basis or explicit `not_applicable`
- retention period in days
- intended sharing scope

## LGPD Guardrails

Before onboarding personal data into this root scaffold:

1. update `config/data_governance.json`
2. document lawful basis and the data subject request process
3. validate whether external GenAI providers remain allowed
4. confirm retention and deletion expectations
5. review whether the sample or demo surface still needs anonymization or pseudonymization

## Why This Matters In The Portfolio

This is not a claim of legal certification.
It is evidence that the project treats privacy, minimization, retention, and governance as design concerns rather than afterthoughts.
