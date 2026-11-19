# Classic Generic XSDs

## OVERVIEW
- Classic EDI/AWB/Print/Shipment XSDs shared across carriers.

## STRUCTURE
```
./
├── ShipitSmarterStandardEDISchema.xsd
├── shipmentAirwaybill_request.xsd
├── ShipmentAirwaybillResponse.xsd
├── shipmentPrint_request.xsd
├── ShipmentPrintResponse.xsd
├── combined_Request.xsd
├── shipmentCombined_response_v1.xsd
├── shipmentRates_Request.xsd
├── shipment.xsd
└── uploadDocuments.xsd
```

## WHERE TO LOOK
| Task | Location | Notes |
|------|----------|-------|
| Standard EDI | ShipitSmarterStandardEDISchema.xsd | Base schema | 
| Airwaybill request | shipmentAirwaybill_request.xsd | Request format | 
| Airwaybill response | ShipmentAirwaybillResponse.xsd | Response format | 
| Print request | shipmentPrint_request.xsd | Label/print | 
| Print response | ShipmentPrintResponse.xsd | Label/print | 
| Combined shipment request | combined_Request.xsd | Request |
| Combined shipment response | shipmentCombined_response_v1.xsd | Response |
| Shipment rates | shipmentRates_Request.xsd | Request |
| Shipment documents | uploadDocuments.xsd | Document upload |
| Updating Shipment | shipment.xsd | Request |

## CONVENTIONS
- XSDs kept as-is; filenames match legacy consumers.

## ANTI-PATTERNS
- Renaming files (breaks external references).
