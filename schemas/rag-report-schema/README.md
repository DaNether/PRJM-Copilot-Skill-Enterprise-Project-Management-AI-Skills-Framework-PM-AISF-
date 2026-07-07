# RAG Report Schema

**Version:** 1.0.0 | **Standard:** JSON Schema Draft 2020-12

Defines the structure for weekly project status reports with RAG classification.

## Usage

Validate AI-generated status reports against this schema before distribution.

```bash
# Example: validate with ajv-cli
npx ajv validate -s rag-report.schema.json -d my-report.json
```

## Key Fields

| Field | Required | Description |
|-------|----------|-------------|
| project_name | Yes | Project name |
| rag_status | Yes | Red / Amber / Green |
| period | Yes | Reporting period (start/end dates) |
| key_messages | Yes | Top messages (1–5 items) |
| ai_content_warning | Yes | Must be true |
