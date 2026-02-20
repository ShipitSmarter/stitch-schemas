# Preparsers Schema Notes

## OVERVIEW
- JSON schemas for file pre-parser configurations.
- Small, strict schemas used before integration steps.

## STRUCTURE
```
./
├── csv.schema.json
├── fixedwidthreport.schema.json
├── multiheadercsv.schema.json
└── textdelimitedreport.schema.json
```

## WHERE TO LOOK
| Task | Location | Notes |
|------|----------|-------|
| CSV config | csv.schema.json | Delimiter/SkipFirstRow/Columns | 
| Fixed-width | fixedwidthreport.schema.json | RowDefinitions tree | 
| Multi-header CSV | multiheadercsv.schema.json | Header groups | 
| Text-delimited | textdelimitedreport.schema.json | Separator + columns | 

## CONVENTIONS
- draft-07 $schema, PascalCase properties.
- uniqueItems used for column arrays.

## ANTI-PATTERNS
- Adding new parser types without schema file.
- Removing required fields (consumers assume strict validation).
