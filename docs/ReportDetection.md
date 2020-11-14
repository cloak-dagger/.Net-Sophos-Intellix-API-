# IO.Swagger.Model.ReportDetection
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Sophos** | **string** | A detection name associated with a Sophos AV scan (may be empty string - also if the VT scan is old and we know we are now detecting the file, we will report detection despite a gap in the VT results - also if there is no VT scan we may still report a detection name if we know it)  | 
**SophosMl** | **string** | A detection name associated with a Sophos ML scan (may be empty string - also VT doesn&#x27;t differentiate ML detections from Reputation detections, we will attempt to do so in the back end - also if the VT scan is old and we know we are now detecting the file, we will report detection despite a gap in the VT results - also if there is no VT scan we may still report a detection name if we know it)  | 
**Positives** | **int?** | The total number of VT scanners which detected the file - excluding Sophos and Sophos ML which we will list explicitly - this may be zero for a given VT scan  | 
**Total** | **int?** | The total number of VT scanners run on the file (including non-detections) | 
**Permalink** | **string** | Web link to VT scan page (ie 3rd party website) for the file - NOTE if this is empty, there was no VT scan  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

