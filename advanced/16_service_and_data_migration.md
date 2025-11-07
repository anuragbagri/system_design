# Service & Data Migration Strategies (Advanced)

## Overview

Service and data migrations are common during schema evolution, platform upgrades, and refactors. Proper strategies reduce downtime and data loss risk.

## Migration Patterns

- Blue/Green deployments for services
- Online schema migrations (expand/contract pattern)
- Dual writes with backfill and reconciliation
- Backwards-compatible API changes and versioning

## Data Migration Considerations

- Migrate in small batches and validate after each step
- Use idempotent backfill jobs and verify checksums
- Provide fallbacks and rollbacks in case of issues

## Tooling

- Migration frameworks (Flyway, Liquibase), custom backfill jobs, change-data-capture (CDC) tools

## Best Practices

- Test migrations in staging with production-like data
- Monitor migration progress and validation metrics
- Communicate changes to downstream consumers and provide deprecation timelines

## References

- Online schema migration patterns
