# Generic Schemas Overview

## OVERVIEW
- Container for generic carrier schemas.
- Current focus is classic EDI/AWB/Print/Shipment XSDs under classic/.

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
| Combined shipment | classic/combined_Request.xsd | Request |
| Combined shipment | classic/shipmentCombined_response_v1.xsd | Response |
| Shipment rates | classic/shipmentRates_Request.xsd | Request |
| Shipment documents | classic/uploadDocuments.xsd | Document upload |
| Updating Shipment Shipment | classic/shipment.xsd | Request |

## CONVENTIONS
- XSD format, classic naming preserved.

## ANTI-PATTERNS
- Introducing non-classic schemas here (create new domain dir).
