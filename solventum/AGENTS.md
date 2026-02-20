# Solventum Schemas

## OVERVIEW
- Carrier-specific XSDs for Solventum events.

## STRUCTURE
```
./
├── awb-update.xsd
└── milestone.xsd
```

## WHERE TO LOOK
| Task | Location | Notes |
|------|----------|-------|
| AWB updates | awb-update.xsd | Event schema | 
| Milestones | milestone.xsd | Event schema | 

## CONVENTIONS
- XSD naming aligned to event type.

## ANTI-PATTERNS
- Mixing generic schemas here (keep carrier-specific only).
