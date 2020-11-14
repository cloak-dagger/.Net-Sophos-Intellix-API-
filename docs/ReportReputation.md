# IO.Swagger.Model.ReportReputation
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Score** | **int?** | Reputation score 0 to 100   * 0-19: Malware   * 20-29: Potentially Unwanted   * 30: Unknown reputation   * ...   * 60-69: Prevalent   * 70-89: Clean   * 90-100 Trusted  | 
**ScoreString** | **string** | Reputation in string, as it is described under \&quot;score\&quot;  | 
**Prevalence** | **string** | Prevalence level string (e.g. rare, low, medium, common, popular) | 
**FirstSeen** | **DateTime?** | First-seen time/date timestamp (decimal representation of UNIX timestamp) | 
**LastSeen** | **DateTime?** | Last-seen time/date timestamp (decimal representation of UNIX timestamp) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

