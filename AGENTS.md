# Stitch-Schemas Knowledge Base

## OVERVIEW
- Schema-only repo for Stitch integration definitions.
- JSON Schema (draft-07), YAML schema, XSD, and OpenAPI 3.0.4 live together.

## STRUCTURE
```
./
├── integration.schema.json                 # Core integration workflow schema
├── integration-set.schema.yaml             # Integration-set metadata (YAML)
├── integration.metadata.schema.json        # UI instruction metadata
├── integration-set.services.translation.en.yaml  # Service label translations
├── carrier-gateway-xml-*-schema.xsd        # Cross-carrier ordering/tracking XSD
├── aalbertshfc/schema.json                 # OpenAPI 3.0.4 (very large)
├── preparsers/                             # CSV/fixed-width/text parsers
├── generic/classic/                        # Generic EDI/AWB/Print XSDs
└── solventum/                              # Carrier-specific XSDs
```

## WHERE TO LOOK
| Task | Location | Notes |
|------|----------|-------|
| Integration workflow steps | integration.schema.json | $type discriminator + anyOf refs | 
| Carrier integration metadata | integration-set.schema.yaml | YAML schema, strict additionalProperties | 
| UI instruction metadata | integration.metadata.schema.json | Small, form-facing schema | 
| Cross-carrier XML | carrier-gateway-xml-ordering-schema.xsd | Ordering schema | 
| Tracking XML | carrier-gateway-xml-tracking-schema.xsd | Tracking schema | 
| Large API surface | aalbertshfc/schema.json | OpenAPI 3.0.4 | 
| Input preparsers | preparsers/*.schema.json | CSV/fixed-width/text | 
| Generic classic EDI | generic/classic/*.xsd | Standard formats | 
| Solventum events | solventum/*.xsd | AWB + milestone | 

## CONVENTIONS
- JSON schemas use draft-07 ($schema at root).
- Strict models use additionalProperties: false (expect failures on unknown fields).
- integration.schema.json uses $type discriminator strings (C# type names).
- YAML schema starts with yaml-language-server $schema directive.
- OpenAPI 3.0.4 spec lives under aalbertshfc/schema.json.

## ANTI-PATTERNS (REPO-SPECIFIC)
- Dropping $schema or $type in integration.schema.json (breaks validation/serialization).
- Adding fields without updating required/additionalProperties rules.
- Editing integration-set.schema.yaml as JSON (keep YAML semantics).
- Reformatting aalbertshfc/schema.json with different JSON style (huge file; diff noise).

## COMMANDS
```bash
# No build/test/CI commands in this repo.
```

## NOTES
- Line counts are large (20k+ total); expect large diffs.
- No AGENTS.md existed previously.
