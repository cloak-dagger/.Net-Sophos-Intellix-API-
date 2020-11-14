# IO.Swagger.Api.StaticFileAnalysisApi

All URIs are relative to *https://de.api.labs.sophos.com/analysis/file/static/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ReportsGet**](StaticFileAnalysisApi.md#reportsget) | **GET** /reports | Get a report by file hash.
[**ReportsJobIdGet**](StaticFileAnalysisApi.md#reportsjobidget) | **GET** /reports/{job_id} | Get a report by job id.
[**RootPost**](StaticFileAnalysisApi.md#rootpost) | **POST** / | Submit a file for static analysis.

<a name="reportsget"></a>
# **ReportsGet**
> StaticAnalysisReport ReportsGet (string sha256, string authorization, string reportFormat = null, string xCorrelationID = null)

Get a report by file hash.

Get a report by file hash. Currently only sha256 hashes are supported.  The caller is billed if SophosLabs returns a report for the file with status code 200. The server returns with status code 404 in case of no report found for the requested file hash. 

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class ReportsGetExample
    {
        public void main()
        {
            // Configure OAuth2 access token for authorization: oAuthScheme
            Configuration.Default.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new StaticFileAnalysisApi();
            var sha256 = sha256_example;  // string | The SHA256 hash of the file. 
            var authorization = authorization_example;  // string | The access token obtained from the token endpoint to authenticate towards a specific SophosLabs API.  You can learn more about authentication towards SophosLabs APIs [here](/doc/authentication.html). 
            var reportFormat = reportFormat_example;  // string | The requested report format. Either 'json' (default) or 'html'.  HTML response may only be received in case of the jobStatus is SUCCESS. Otherwise the response format is always JSON, even if HTML requested.  The 'Content-Type' response header is always set accordingly:   * application/json  * text/html  (optional) 
            var xCorrelationID = xCorrelationID_example;  // string | An optional caller-provided identifier which will be included in the response object. It must match the following regular expression: \"[-._a-zA-Z0-9]{1,40}\":  * Only alphanumeric characters, hyphens, dots and underscores are allowed * Min length of 1 character * Max length of 40 characters  (optional) 

            try
            {
                // Get a report by file hash.
                StaticAnalysisReport result = apiInstance.ReportsGet(sha256, authorization, reportFormat, xCorrelationID);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling StaticFileAnalysisApi.ReportsGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sha256** | **string**| The SHA256 hash of the file.  | 
 **authorization** | **string**| The access token obtained from the token endpoint to authenticate towards a specific SophosLabs API.  You can learn more about authentication towards SophosLabs APIs [here](/doc/authentication.html).  | 
 **reportFormat** | **string**| The requested report format. Either &#x27;json&#x27; (default) or &#x27;html&#x27;.  HTML response may only be received in case of the jobStatus is SUCCESS. Otherwise the response format is always JSON, even if HTML requested.  The &#x27;Content-Type&#x27; response header is always set accordingly:   * application/json  * text/html  | [optional] 
 **xCorrelationID** | **string**| An optional caller-provided identifier which will be included in the response object. It must match the following regular expression: \&quot;[-._a-zA-Z0-9]{1,40}\&quot;:  * Only alphanumeric characters, hyphens, dots and underscores are allowed * Min length of 1 character * Max length of 40 characters  | [optional] 

### Return type

[**StaticAnalysisReport**](StaticAnalysisReport.md)

### Authorization

[oAuthScheme](../README.md#oAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json SUCCESS, text/html SUCCESS, application/json ERROR, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="reportsjobidget"></a>
# **ReportsJobIdGet**
> StaticAnalysisReport ReportsJobIdGet (string jobId, string authorization, string reportFormat = null, string xCorrelationID = null)

Get a report by job id.

Get a report by job id.  In case of IN_PROGRESS jobStatus the client has to continue polling this endpoint to retrieve the report with either SUCCES or ERROR jobStatus. The proposed polling interval is 5 seconds. The proposed analysis timeout on the client side is 15 minutes. If the server does not provide either SUCCESS or ERROR report within this time, most probably it faces with an unexpected error.  The caller is not billed for this call.  Example call to get report by Job ID:   ```bash   $ curl \\         -X GET \\         -H \"Authorization: ${TOKEN}\" \\         -s https://de.api.labs.sophos.com/analysis/file/static/v1/reports/${JOBID}?report_format=html`   ``` 

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class ReportsJobIdGetExample
    {
        public void main()
        {
            // Configure OAuth2 access token for authorization: oAuthScheme
            Configuration.Default.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new StaticFileAnalysisApi();
            var jobId = jobId_example;  // string | The job id obtained in the submit call. 
            var authorization = authorization_example;  // string | The access token obtained from the token endpoint to authenticate towards a specific SophosLabs API.  You can learn more about authentication towards SophosLabs APIs [here](/doc/authentication.html). 
            var reportFormat = reportFormat_example;  // string | The requested report format. Either 'json' (default) or 'html'.  HTML response may only be received in case of the jobStatus is SUCCESS. Otherwise the response format is always JSON, even if HTML requested.  The 'Content-Type' response header is always set accordingly:   * application/json  * text/html  (optional) 
            var xCorrelationID = xCorrelationID_example;  // string | An optional caller-provided identifier which will be included in the response object. It must match the following regular expression: \"[-._a-zA-Z0-9]{1,40}\":  * Only alphanumeric characters, hyphens, dots and underscores are allowed * Min length of 1 character * Max length of 40 characters  (optional) 

            try
            {
                // Get a report by job id.
                StaticAnalysisReport result = apiInstance.ReportsJobIdGet(jobId, authorization, reportFormat, xCorrelationID);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling StaticFileAnalysisApi.ReportsJobIdGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jobId** | **string**| The job id obtained in the submit call.  | 
 **authorization** | **string**| The access token obtained from the token endpoint to authenticate towards a specific SophosLabs API.  You can learn more about authentication towards SophosLabs APIs [here](/doc/authentication.html).  | 
 **reportFormat** | **string**| The requested report format. Either &#x27;json&#x27; (default) or &#x27;html&#x27;.  HTML response may only be received in case of the jobStatus is SUCCESS. Otherwise the response format is always JSON, even if HTML requested.  The &#x27;Content-Type&#x27; response header is always set accordingly:   * application/json  * text/html  | [optional] 
 **xCorrelationID** | **string**| An optional caller-provided identifier which will be included in the response object. It must match the following regular expression: \&quot;[-._a-zA-Z0-9]{1,40}\&quot;:  * Only alphanumeric characters, hyphens, dots and underscores are allowed * Min length of 1 character * Max length of 40 characters  | [optional] 

### Return type

[**StaticAnalysisReport**](StaticAnalysisReport.md)

### Authorization

[oAuthScheme](../README.md#oAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json SUCCESS, text/html SUCCESS, application/json ERROR, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
<a name="rootpost"></a>
# **RootPost**
> StaticAnalysisReport RootPost (string authorization, string xCorrelationID = null)

Submit a file for static analysis.

Submit a file for static analysis.  Supported file types:  * PE /32-bit & 64-bit, EXE & DLL/  * Office documents /OLE & Open XML formats/  * RTF documents  * PDF documents  * Archive or compression types:    * zip archive  After successfully submitting a file for static analysis the server responds with jobStatus IN_PROGRESS or SUCCESS or ERROR. In case of IN_PROGRESS jobStatus the client has to poll (periodically call) the /reports/{job_id} endpoint to retrieve the report. The proposed polling interval is 5 seconds.  In case of SUCCESS or ERROR jobStatus the report is responded immediatelly. No need to call /reports/{job_id} endpoint.  All successful file submissions are billed.  Example call to submit file:   ```bash   $ curl \\       -X POST \\       -H \"Authorization: ${TOKEN}\" \\       -s https://de.api.labs.sophos.com/analysis/file/static/v1/ \\       -F file=@${file} \\   ``` 

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class RootPostExample
    {
        public void main()
        {
            // Configure OAuth2 access token for authorization: oAuthScheme
            Configuration.Default.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new StaticFileAnalysisApi();
            var authorization = authorization_example;  // string | The access token obtained from the token endpoint to authenticate towards a specific SophosLabs API.  You can learn more about authentication towards SophosLabs APIs [here](/doc/authentication.html). 
            var xCorrelationID = xCorrelationID_example;  // string | An optional caller-provided identifier which will be included in the response object. It must match the following regular expression: \"[-._a-zA-Z0-9]{1,40}\":  * Only alphanumeric characters, hyphens, dots and underscores are allowed * Min length of 1 character * Max length of 40 characters  (optional) 

            try
            {
                // Submit a file for static analysis.
                StaticAnalysisReport result = apiInstance.RootPost(authorization, xCorrelationID);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling StaticFileAnalysisApi.RootPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| The access token obtained from the token endpoint to authenticate towards a specific SophosLabs API.  You can learn more about authentication towards SophosLabs APIs [here](/doc/authentication.html).  | 
 **xCorrelationID** | **string**| An optional caller-provided identifier which will be included in the response object. It must match the following regular expression: \&quot;[-._a-zA-Z0-9]{1,40}\&quot;:  * Only alphanumeric characters, hyphens, dots and underscores are allowed * Min length of 1 character * Max length of 40 characters  | [optional] 

### Return type

[**StaticAnalysisReport**](StaticAnalysisReport.md)

### Authorization

[oAuthScheme](../README.md#oAuthScheme)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json SUCCESS, text/html SUCCESS, application/json ERROR, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
