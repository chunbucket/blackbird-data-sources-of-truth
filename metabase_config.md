# Metabase Configuration

## API Access

| Setting                 | Value                                             |
| ----------------------- | ------------------------------------------------- |
| **Base URL**            | https://blackbird-labs.metabaseapp.com            |
| **API Key (Read-Only)** | `mb_jBl8Wgzw36Ow07DX86+5YGlIWCtAw1VXfZ8O277/PFI=` |

## Databases

| Database Name             | ID     | Engine           | Environment | Use For                       |
| ------------------------- | ------ | ---------------- | ----------- | ----------------------------- |
| Coreprod Replica          | **69** | PostgreSQL 14.12 | Production  | Production queries, reporting |
| Coredev Replica           | 67     | PostgreSQL 14.17 | Development | Testing queries               |
| Coreprod Staging          | 166    | PostgreSQL 14.17 | Staging     | Staging environment queries   |
| Google Sheets Integration | 133    | BigQuery         | Integration | Google Sheets data            |

## API Usage

### Running a Native Query

```bash
curl -s -X POST "https://blackbird-labs.metabaseapp.com/api/dataset" \
  -H "x-api-key: mb_jBl8Wgzw36Ow07DX86+5YGlIWCtAw1VXfZ8O277/PFI=" \
  -H "Content-Type: application/json" \
  -d '{
    "database": 69,
    "type": "native",
    "native": {
      "query": "YOUR SQL QUERY HERE"
    }
  }'
```

### Listing Databases

```bash
curl -s "https://blackbird-labs.metabaseapp.com/api/database" \
  -H "x-api-key: mb_jBl8Wgzw36Ow07DX86+5YGlIWCtAw1VXfZ8O277/PFI=" \
  -H "Content-Type: application/json"
```

## Common Database Schemas (Coreprod)

- **public** - Main application tables (users, check_ins, checks, etc.)
- **square** - Square POS integration data
- **toast** - Toast POS integration data
- **supergood_toast** - Supergood Toast integration
- **hubspot** - HubSpot CRM data
- **checkout** - Checkout/payment sessions
- **gtm** - Growth/marketing data

## Notes

- All queries should target the **Coreprod Replica** (ID: 69) for production data
- The API key is read-only and cannot modify data
- Query results include metadata about column types and execution time
