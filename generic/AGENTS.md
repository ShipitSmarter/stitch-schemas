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
| Airwaybill | classic/ShipmentAirwaybillResponse.xsd | Generated response |
| Print | classic/shipmentPrint_request.xsd | Request | 
| Print | classic/ShipmentPrintResponse.xsd | Generated response |
| Combined shipment | classic/combined_Request.xsd | Request |
| Combined shipment | classic/shipmentCombined_response_v1.xsd | Response |
| Shipment | classic/shipment.xsd | Request |
| Shipment | classic/ShipmentResponse.xsd | Generated response |
| Shipment rates | classic/shipmentRates_Request.xsd | Request |
| Shipment rates | classic/ShipmentRatesResponse.xsd | Generated response |
| Shipment documents | classic/uploadDocuments.xsd | Request |
| Shipment documents | classic/ShipmentDocumentUploadResponse.xsd | Generated response |
| Carrier label | classic/ShipmentCarrierLabelResponse.xsd | Generated response |
| Shipment delete | classic/ShipmentDeleteResponse.xsd | Generated response |
| Shipment rules | classic/shipmentRules.xsd | Request |
| Shipment rules | classic/ShipmentRulesResponse.xsd | Generated response |
| Shipment tracking | classic/ShipmentTrackingResponse.xsd | Generated response |

## CONVENTIONS
- XSD format, classic naming preserved.

## ANTI-PATTERNS
- Introducing non-classic schemas here (create new domain dir).
