# INNHOUSE

Canonical INNHOUSE product architecture.

## Status

Architecture foundation under active development.

## Canonical model

- Multiple creators per House
- Three membership roles: Creator, Admin, Member
- Explicit ownership semantics
- Atomic ownership transfer
- Application-level authorization
- Supabase/PostgreSQL RLS as defense in depth
- Tenant isolation
- Concurrency-safe membership and ownership operations

## Production safety

The existing production Supabase schema is being reconciled against this canonical model.

No destructive production migration should be executed until:

1. The canonical schema is validated in an isolated environment.
2. Existing production data is mapped safely.
3. Existing RLS policies are reconciled.
4. Migration and rollback procedures are prepared.
5. All required authorization, RLS, ownership, concurrency, and tenant-isolation tests pass.

See `docs/` for the architecture and migration decisions.
