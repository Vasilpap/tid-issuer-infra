# TID Issuer Infrastructure (Docker Compose)

Containerized infrastructure for local TID Issuer environments.

## Services

- `quarkus-db` (PostgreSQL for API)
- `keycloak-db` (PostgreSQL for Keycloak)
- `keycloak` (OIDC provider)
- `minio` (object storage for article documents)

## Quick Start

1. Copy `.env.example` to `.env` and set values.
2. Start the stack:

```bash
docker compose up -d
```

3. Stop the stack:

```bash
docker compose down
```

## Default Host Ports

- PostgreSQL (API): `5432`
- PostgreSQL (Keycloak): `5433`
- Keycloak: `8180`
- MinIO API: `9000`
- MinIO Console: `9001`

## Realm Import

`realm-export.json` is mounted into Keycloak for bootstrap configuration and test users/roles.

## Notes

- `docker-compose.yml` expects sensitive values from `.env`.
- Do not commit real `.env` values.
