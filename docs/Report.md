# IO.Swagger.Model.Report
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Submission** | **string** | The file submission date in UTC. | 
**AnalysisType** | **string** | The type of the file analysis.  It&#x27;s always **static**.  | 
**AnalysisSubject** | [**AnalysisSubject**](AnalysisSubject.md) |  | 
**Score** | **int?** | Maliciousness score of the analyzed file (0 &#x3D; malicious, 100 &#x3D; benign). | [optional] 
**AnalysisSummary** | [**List&lt;ReportAnalysisSummary&gt;**](ReportAnalysisSummary.md) | Array of matched rules from detailed file analysis of EDR analyzer output | [optional] 
**ContainerAnalysis** | [**ReportContainerAnalysis**](ReportContainerAnalysis.md) |  | [optional] 
**Detection** | [**ReportDetection**](ReportDetection.md) |  | [optional] 
**DocumentAnalysis** | [**ReportDocumentAnalysis**](ReportDocumentAnalysis.md) |  | [optional] 
**MlAggregateResults** | [**ReportMlAggregateResults**](ReportMlAggregateResults.md) |  | [optional] 
**MlFile** | [**ReportMlFile**](ReportMlFile.md) |  | [optional] 
**MlFilepath** | [**ReportMlFilepath**](ReportMlFilepath.md) |  | [optional] 
**MlInputs** | [**ReportMlInputs**](ReportMlInputs.md) |  | [optional] 
**PeAnalysis** | [**ReportPeAnalysis**](ReportPeAnalysis.md) |  | [optional] 
**Reputation** | [**ReportReputation**](ReportReputation.md) |  | [optional] 
**Target** | [**ReportTarget**](ReportTarget.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

