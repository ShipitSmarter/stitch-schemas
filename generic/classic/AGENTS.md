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
├── shipment.xsd
├── ShipmentResponse.xsd
├── shipmentRates_Request.xsd
├── ShipmentRatesResponse.xsd
├── uploadDocuments.xsd
├── ShipmentDocumentUploadResponse.xsd
├── ShipmentCarrierLabelResponse.xsd
├── shipmentRules.xsd
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
| Shipment request | shipment.xsd | Request |
| Shipment response | ShipmentResponse.xsd | Generated response |
| Shipment rates | shipmentRates_Request.xsd | Request |
| Shipment rates response | ShipmentRatesResponse.xsd | Generated response |
| Shipment documents | uploadDocuments.xsd | Request |
| Document upload response | ShipmentDocumentUploadResponse.xsd | Generated response |
| Carrier label response | ShipmentCarrierLabelResponse.xsd | Generated response |
| Shipment rules request | shipmentRules.xsd | Request |
| Shipment rules response | ShipmentRulesResponse.xsd | Generated response |
| Shipment tracking response | ShipmentTrackingResponse.xsd | Generated response |

## CONVENTIONS
- XSDs preserve their source schema definitions; retain established filenames unless requested.
- Generated files that declared UTF-16 but contained UTF-8 bytes have their declaration corrected to `utf-8`.
- Request XSDs are copies of the Catch API validation schemas (`SiS.Validations/v1/InsertShipment` and `v1/PrintShipment`); Catch validates incoming requests against these, not against generated XSDs.
- Response XSDs are generated from the Catch response classes (Catch does not validate responses). Properties serialized via `XmlNode` (e.g. AWB `Error/Message`) must be `type="xs:string"`, as the actual output is plain text.

## ANTI-PATTERNS
- Renaming files (breaks external references).
