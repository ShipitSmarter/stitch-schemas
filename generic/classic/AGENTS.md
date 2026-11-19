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
├── Shipment.xsd
├── ShipmentResponse.xsd
├── shipmentRates_Request.xsd
├── ShipmentRatesResponse.xsd
├── ShipmentDocuments.xsd
├── ShipmentDocumentUploadResponse.xsd
├── ShipmentCarrierLabelResponse.xsd
├── ShipmentDeleteResponse.xsd
├── ShipmentRulesResponse.xsd
└── ShipmentTrackingResponse.xsd
```

## WHERE TO LOOK
| Task | Location | Notes |
|------|----------|-------|
| Standard EDI | ShipitSmarterStandardEDISchema.xsd | Base schema | 
| Airwaybill request | shipmentAirwaybill_request.xsd | Request format | 
| Airwaybill response | ShipmentAirwaybillResponse.xsd | Generated response |
| Print request | shipmentPrint_request.xsd | Label/print | 
| Print response | ShipmentPrintResponse.xsd | Generated response |
| Combined shipment request | combined_Request.xsd | Request |
| Combined shipment response | shipmentCombined_response_v1.xsd | Response |
| Shipment request | Shipment.xsd | Generated request |
| Shipment response | ShipmentResponse.xsd | Generated response |
| Shipment rates | shipmentRates_Request.xsd | Request |
| Shipment rates response | ShipmentRatesResponse.xsd | Generated response |
| Shipment documents | ShipmentDocuments.xsd | Generated document upload |
| Document upload response | ShipmentDocumentUploadResponse.xsd | Generated response |
| Carrier label response | ShipmentCarrierLabelResponse.xsd | Generated response |
| Shipment delete response | ShipmentDeleteResponse.xsd | Generated response |
| Shipment rules response | ShipmentRulesResponse.xsd | Generated response |
| Shipment tracking response | ShipmentTrackingResponse.xsd | Generated response |

## CONVENTIONS
- XSDs preserve their source schema definitions; retain established filenames unless requested.
- Generated files that declared UTF-16 but contained UTF-8 bytes have their declaration corrected to `utf-8`.
- `Shipment.xsd` uses a lax XML Schema namespace wildcard instead of the generated `ref="xs:schema"` so it compiles standalone.

## ANTI-PATTERNS
- Renaming files (breaks external references).
