# Copilot Studio OpenAPI Manifests

**Version:** 1.0.0

## Overview

These OpenAPI 3.0 YAML manifests can be imported directly into Microsoft Copilot Studio as plugin action definitions.

## Import Instructions

1. Open **Microsoft Copilot Studio**.
2. Navigate to **Settings → AI Plugins**.
3. Select **Import Plugin** → **OpenAPI**.
4. Upload `pm-aisf-openapi.yaml`.
5. Configure the OAuth 2.0 security scheme with your Azure AD tenant ID.
6. Map the actions to the appropriate agent topics.

## Available Actions

| Operation | Path | Description |
|-----------|------|-------------|
| getProjectRagReport | GET /projects/{id}/rag-report | Latest weekly RAG report |
| getProjectHealth | GET /projects/{id}/health | Multi-dimension health score |
| getProjectRaid | GET /projects/{id}/raid | RAID log |
| getPortfolioDashboard | GET /portfolio/dashboard | Executive portfolio view |

## Security

All actions require OAuth 2.0 authentication via Azure AD. Scopes are least-privilege read-only by default.
