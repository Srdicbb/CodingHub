# Multi-Tenancy

**Phase:** 2.1 - Architecture
**Status:** [ ] In Progress
**Priority:** Senior Level / SaaS Architecture

---

## Current Knowledge

<!-- Fill in what you learn about multi-tenancy -->

### What is Multi-Tenancy?

### Isolation Strategies

| Approach | Description | Pros | Cons |
|---|---|---|---|
| Shared DB, shared schema | Single table with `TenantId` column on every row | Cheapest, simplest | Lowest isolation |
| Shared DB, separate schema | Each tenant has own schema in same DB | Medium isolation | More complex migrations |
| Separate DB per tenant | Each tenant has own database | Highest isolation | Expensive, harder to manage |

### Identifying the Current Tenant

<!-- How does the app know which tenant is making the request? -->
<!-- e.g. subdomain, JWT claim, header, route -->

### Data Isolation

<!-- How do you make sure tenant A never sees tenant B's data? -->

---

## Examples / Notes

<!-- Code examples, config, EF Core filters, middleware, etc. -->

---

## Questions / Confusions

<!-- Anything you're not 100% sure about yet -->
