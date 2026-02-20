# aalbertshfc Schema Notes

## OVERVIEW
- Single OpenAPI 3.0.4 document for Viya Shipping API.
- Very large file; treat as generated/authoritative spec.

## STRUCTURE
```
./
└── schema.json  # OpenAPI 3.0.4 (paths + components)
```

## WHERE TO LOOK
| Task | Location | Notes |
|------|----------|-------|
| API endpoints | paths | /v3/* operations | 
| Data models | components.schemas | OpenAPI schemas | 
| Auth/servers | servers | URL + variables | 
| Metadata | info | title/version/x-logo | 

## CONVENTIONS
- OpenAPI 3.0.4 format (openapi/info/servers/paths/components).
- Uses allOf for schema composition.

## ANTI-PATTERNS
- Manual reformatting (massive diff churn).
- Mixing JSON Schema draft-07 keywords here (stick to OpenAPI).
