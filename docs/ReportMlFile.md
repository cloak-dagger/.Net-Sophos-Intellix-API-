# IO.Swagger.Model.ReportMlFile
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Analyses** | [**ReportMlFileAnalyses**](ReportMlFileAnalyses.md) |  | 
**AnalyzedCounts** | [**ReportMlFileAnalyzedCounts**](ReportMlFileAnalyzedCounts.md) |  | 
**OverallScore** | [**decimal?**](BigDecimal.md) | The overall score for the file analyses. Currently just a weighted average of the ml_file.overall_scores values, heavily (4x1) weighted in favor of the genetic_analysis score (higher accuracy).  | 
**OverallScores** | [**ReportMlFileOverallScores**](ReportMlFileOverallScores.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

