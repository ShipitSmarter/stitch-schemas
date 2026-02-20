# Classic Generic XSDs

## OVERVIEW
- Classic EDI/AWB/Print XSDs shared across carriers.

## STRUCTURE
```
./
├── ShipitSmarterStandardEDISchema.xsd
├── shipmentAirwaybill_request.xsd
├── ShipmentAirwaybillResponse.xsd
├── shipmentPrint_request.xsd
└── ShipmentPrintResponse.xsd
```

## WHERE TO LOOK
| Task | Location | Notes |
|------|----------|-------|
| Standard EDI | ShipitSmarterStandardEDISchema.xsd | Base schema | 
| Airwaybill request | shipmentAirwaybill_request.xsd | Request format | 
| Airwaybill response | ShipmentAirwaybillResponse.xsd | Response format | 
| Print request | shipmentPrint_request.xsd | Label/print | 
| Print response | ShipmentPrintResponse.xsd | Label/print | 

## CONVENTIONS
- XSDs kept as-is; filenames match legacy consumers.

## ANTI-PATTERNS
- Renaming files (breaks external references).
