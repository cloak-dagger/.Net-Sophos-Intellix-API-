# SophosLabs.Intellix.Api.AuthenticationApi

All URIs are relative to *https://api.labs.sophos.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Oauth2TokenPost**](AuthenticationApi.md#oauth2tokenpost) | **POST** /oauth2/token | Authentication endpoint

<a name="oauth2tokenpost"></a>
# **Oauth2TokenPost**
> AuthenticationResponse Oauth2TokenPost (string authorization, string contentType)

Authentication endpoint

The user must get an access token to call the SophosLabs APIs.  * Example call   ```bash   $ curl \\       -X POST \\       -H 'Authorization: Basic MXJxbmR1ODBpOWR2ZGwwN28zNGdrYTA2azoxM2h2Y2wxY3FqOG5lNWNnN2VlMGU3Z2ppNmszNms3OXNyMjAyamE2YTVraWZnNWd0ZTlx' \\       -H 'Content-Type: application/x-www-form-urlencoded' \\       -i https://api.labs.sophos.com/oauth2/token \\       -d 'grant_type=client_credentials'   HTTP/2 200   content-type: application/json;charset=UTF-8    {\"access_token\":\"eyJraWQiOiIxZmhWUmt0VmNLRW1xVmhDV1 ... 3FVIPrC3ruPAcuTSN_MN9FtMvSrSMA\",\"expires_in\":3600,\"token_type\":\"Bearer\"}   ``` 

### Example
```csharp
using System;
using System.Diagnostics;
using SophosLabs.Intellix.Api;
using SophosLabs.Intellix.Client;
using SophosLabs.Intellix.Model;

namespace Example
{
    public class Oauth2TokenPostExample
    {
        public void main()
        {
            var apiInstance = new AuthenticationApi();
            var authorization = authorization_example;  // string | The authorization header. The secret is [Basic](https://en.wikipedia.org/wiki/Basic_access_authentication#Client_side): Base64Encode(client_id:client_secret). 
            var contentType = contentType_example;  // string | The content type for the request body.  Must be **application/x-www-form-urlencoded** 

            try
            {
                // Authentication endpoint
                AuthenticationResponse result = apiInstance.Oauth2TokenPost(authorization, contentType);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling AuthenticationApi.Oauth2TokenPost: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**| The authorization header. The secret is [Basic](https://en.wikipedia.org/wiki/Basic_access_authentication#Client_side): Base64Encode(client_id:client_secret).  | 
 **contentType** | **string**| The content type for the request body.  Must be **application/x-www-form-urlencoded**  | 

### Return type

[**AuthenticationResponse**](AuthenticationResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
