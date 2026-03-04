# ADR-INDEX.md

## Architecture Decision Record Index

### ADR-001: Repository Strategy for Multi-Tenant AEMaaCS — Multi-Repo + Aggregator (Program-Wide)
Defines the program-wide repository topology.  
Each tenant maintains its own Git repository for autonomy and ownership clarity, while a central **Aggregator repository** composes the deployable codebase and hosts shared platform modules. This strategy balances team independence with the requirement that AEMaaCS deployments occur as a single composite artifact.

---

### ADR-002: Release Train Model for Multi-Tenant AEMaaCS (Aggregator-Based)
Defines the **release operating model** for the multi-tenant platform.  
A **time-boxed release train** anchored in the Aggregator repository governs how tenant changes are integrated, stabilized, and promoted across environments (**Dev → SIT → Stage → Prod**). The model ensures predictable releases, deterministic rollback, and a controlled hotfix path in a shared runtime.

---

### ADR-003: Multi-Tenant AEMaaCS Build, Versioning, and Runtime Identity Strategy (Shell Aggregator)
Defines how the platform preserves **tenant identity, traceability, and release composition** despite Cloud Manager’s automatic Maven version rewriting.  
The strategy introduces a **Shell Aggregator build pattern**, explicit **tenant semantic versioning**, runtime identity via **OSGi bundle metadata**, and a **release manifest** that records the exact tenant revisions included in each deployment.