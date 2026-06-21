# Lab 1.2 — Microsoft Entra ID Role Assignment Validation  
Microsoft Entra ID | Identity & Access Management | Role-Based Access Control (RBAC)

---

## Overview

This lab validates Microsoft Entra ID role assignments for privileged access using the built-in **Global Administrator** role.

The focus is on verifying identity consistency, detecting apparent duplicate role entries in the portal UI, and confirming the actual underlying role assignment integrity.

---

## Objective

To validate Microsoft Entra ID privileged role assignment by:

- Identifying Global Administrator role assignments
- Confirming role definition consistency
- Validating principal identity mapping via Object ID
- Investigating apparent duplicate portal representations
- Confirming assignment integrity within Entra ID RBAC

---

## Steps Performed

### 1. Accessed Entra ID Role Management
- Opened Microsoft Entra admin centre
- Navigated to **Roles and administrators**
- Selected **Global Administrator**

---

### 2. Reviewed Role Assignments
Observed assigned identity:

- **Principal ID:** `e725c212-4d94-4ae4-9bf1-62422d7bac76`
- **Role Definition ID:** `62e90394-69f5-4237-9190-012177145e10`
- **Role Name:** Global Administrator
- **Scope:** Default Directory (Directory)

---

### 3. UI Observation
- Multiple entries appeared in the portal for the same role assignment view
- Entries were visually duplicated but shared identical backend identifiers

---

### 4. Validation
Confirmed consistency across:

- Principal ID
- Role Definition ID
- Directory scope

Conclusion: all entries represent the same underlying RBAC assignment.

---

## Evidence

- Global Administrator role assignment visible in Entra ID portal
- Principal ID: `e725c212-4d94-4ae4-9bf1-62422d7bac76`
- Role Definition ID: `62e90394-69f5-4237-9190-012177145e10`
- Single identity assignment confirmed
- No duplicate RBAC entries identified at backend level

---

## Outcome

The Global Administrator assignment was validated successfully.

Key findings:

- Only one actual privileged assignment exists
- Portal UI may display repeated representations of the same assignment
- No duplication exists in Entra ID RBAC data layer
- Identity mapping is consistent and stable

---

## Key Concepts Learned

- Microsoft Entra ID Role-Based Access Control (RBAC)
- Difference between UI representation vs backend identity model
- Role definition vs role assignment distinction
- Object ID as immutable identity anchor
- Importance of validation before assuming duplication

---

## Operational Significance

In enterprise identity environments:

- Global Administrator is the highest privilege role
- Misinterpretation of UI duplication can lead to false security assumptions
- Accurate RBAC validation depends on:
  - Role Definition ID
  - Principal ID
  - Scope

This ensures correct interpretation of identity data during audits or investigations.

---

## Next Lab

Lab 1.3 — Conditional Access Policy Introduction (planned)

Focus: enforcing identity-based access controls using policy-driven authentication rules.

---

## Repository Purpose

This repository documents structured progression in:

- Azure administration fundamentals
- Microsoft Entra ID identity governance
- RBAC validation and identity analysis
- SOC-style identity investigation methodology
