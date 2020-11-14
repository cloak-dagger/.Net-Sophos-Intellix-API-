# IO.Swagger.Model.StaticAnalysisReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CorrelationId** | **string** | This is a unique ID for correlating logs and traces throughout the system provided by the caller in the X-Correlation-ID header.  It must match the regular expression: \&quot;[-._a-zA-Z0-9]{1,40}\&quot;:   * Only alphanumeric characters, hyphens, dots and underscores are allowed  * Min length of 1 character  * Max length of 40 characters  | [optional] 
**RequestId** | **string** | A unique identifier assigned by SophosLabs to the request.  | [optional] 
**JobStatus** | **string** | The status of the analysis job. Possible values:  * **IN_PROGRESS**: The analysis job is still running. No report provided. * **SUCCESS**: The analysis job has already finished. Report is provided. * **ERROR**: An error happend during the analysis. An AnalysisError object is provided.  | 
**Report** | [**Report**](Report.md) |  | 
**JobId** | **string** | The identifier assigned for this analysis job. Only present in case of GET /reports/{job_id} and POST / responses.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

