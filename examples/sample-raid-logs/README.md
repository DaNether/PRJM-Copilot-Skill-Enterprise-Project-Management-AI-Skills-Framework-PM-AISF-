# Sample RAID Logs

Example RAID log data conforming to the RAID schema.

| File | Project | Items |
|------|---------|-------|
| beta-erp-raid-log.json | Beta ERP Migration | 4 items (1 Critical, 2 High) |

## Schema Validation

```bash
npx ajv validate -s ../../schemas/raid-schema/raid.schema.json -d beta-erp-raid-log.json
```
