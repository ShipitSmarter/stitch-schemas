# Generic Schemas Overview

## OVERVIEW
- Container for generic carrier schemas.
- Current focus is classic EDI/AWB/Print XSDs under classic/.

## STRUCTURE
```
./
└── classic/  # EDI/AWB/Print XSDs
```

## WHERE TO LOOK
| Task | Location | Notes |
|------|----------|-------|
| EDI standard | classic/ShipitSmarterStandardEDISchema.xsd | Base format | 
| Airwaybill | classic/shipmentAirwaybill_request.xsd | Request | 
| Airwaybill | classic/ShipmentAirwaybillResponse.xsd | Response | 
| Print | classic/shipmentPrint_request.xsd | Request | 
| Print | classic/ShipmentPrintResponse.xsd | Response | 

## CONVENTIONS
- XSD format, classic naming preserved.

## ANTI-PATTERNS
- Introducing non-classic schemas here (create new domain dir).
