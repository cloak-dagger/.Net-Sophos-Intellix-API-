# IO.Swagger.Model.ErrorResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CorrelationId** | **string** | This is a unique ID for correlating logs and traces throughout the system provided by the caller in the X-Correlation-ID header.  It must match the regular expression: \&quot;[-._a-zA-Z0-9]{1,40}\&quot;:   * Only alphanumeric characters, hyphens, dots and underscores are allowed  * Min length of 1 character  * Max length of 40 characters  | [optional] 
**RequestId** | **string** | A unique identifier assigned by SophosLabs to the request.  | [optional] 
**Error** | **string** | A camelCase identifier for the error condition.  | [optional] 
**Message** | **string** | An English string explaining the error.  | [optional] 
**CreatedAt** | **string** | The ISO 8601 UTC timestamp for when the error object was created.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

