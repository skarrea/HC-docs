# Data Treatment

## Overview

### Purpose

Describe how you should to treat and deal with the data on the Hunt Cloud environment.

### Scope

This guide covers guidelines for data treatment and handling.

### Audience

All users.

## Core Principles

### 1. Data Protection and Compliance

All data handling must follow relevant legal and institutional frameworks, including:

- **REC** approval.

- **GDPR** for processing personal and sensitive personal data.

- **Helseforskningsloven (Norwegian Health Research Act)**.

- Institutional data handling agreements and ethical approvals.

**Only users with authorized access may interact with datasets.**

### 2. Data Minimization

- Access and process only the data strictly necessary for approved project tasks.

- Direct identifiers should be removed or pseudonymized.

### 3. Secure Environment Usage

- All data processing must take place **within the HUNT Cloud environment**.

- Data must **not** be downloaded, copied, or transferred outside the cloud unless **explicitly approved by the lab leader or space leader**.

### 4. Structured Organization

Data should follow a clear and consistent directory structure, typically separating:

- **Raw data** – read-only, original files.

  > [NOTE] Raw data should be saved in the dedicated location under `/mnt/archive`.

- **Processed data** – intermediate outputs.

- **Results** – final outputs (e.g., models, statistics, figures).

### 5. Documentation and Traceability

All projects should maintain documentation (e.g., ReadME file) covering:

- Data sources.

- Processing workflows and scripts.

- Software versions.

- Storage locations.

- Access permissions.

This ensures transparency and reproducibility of all analyses.
