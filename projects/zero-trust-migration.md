---
title: Zero Trust Migration
status: active
domain: IT
priority: high
created: 2026-03-05
updated: 2026-03-05
---

## Context

Migration to Zero Trust architecture for Caracal Corp M365 E5 tenant.
Phase 1: Identity. Phase 2: Endpoint. Phase 3: Network.

## Tasks

- [ ] Deploy MFA Conditional Access policy
  id: mfa-ca-policy
  priority: high
  label: identity
  dispatch: it-ops

- [ ] Configure device compliance policies
  id: device-compliance
  priority: medium
  label: endpoint

- [ ] Enable risk-based sign-in policies
  id: risk-sign-in
  priority: medium
  label: identity
  blocked-by: mfa-ca-policy

## Notes

- Baselines defined in ~/repos/it/baselines/target/ca-policies/
- Each dispatched task becomes a Change Request in the IT ops engine
