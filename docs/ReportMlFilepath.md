# IO.Swagger.Model.ReportMlFilepath
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Analyses** | [**ReportMlFilepathAnalyses**](ReportMlFilepathAnalyses.md) |  | 
**AnalyzedCounts** | [**ReportMlFilepathAnalyzedCounts**](ReportMlFilepathAnalyzedCounts.md) |  | 
**OverallScores** | [**ReportMlFilepathOverallScores**](ReportMlFilepathOverallScores.md) |  | 
**OverallScore** | [**decimal?**](BigDecimal.md) | The overall score for the filepath analyses. Currently just a weighted average of the ml_filepath.overall_scores values, heavily weighted in favor of the neighbor_maliciousness score (as this is what&#x27;s shown in the UI and has higher accuracy).  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

