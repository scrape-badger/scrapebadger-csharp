# ScrapeBadger.Api.FeedbackApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FeedbackReportABugOrSendFeedback**](FeedbackApi.md#feedbackreportabugorsendfeedback) | **POST** /v1/feedback | Report a bug or send feedback |

<a id="feedbackreportabugorsendfeedback"></a>
# **FeedbackReportABugOrSendFeedback**
> Object FeedbackReportABugOrSendFeedback (FeedbackRequest feedbackRequest)

Report a bug or send feedback

File a bug (wrong/empty result for valid input, misleading error, price mismatch) or feedback (an API or field you needed and couldn't find). Free, never billed. Pass the failing call's X-Request-ID so we can find it.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using ScrapeBadger.Api;
using ScrapeBadger.Client;
using ScrapeBadger.Model;

namespace Example
{
    public class FeedbackReportABugOrSendFeedbackExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://scrapebadger.com";
            // Configure API key authorization: ApiKeyAuth
            config.AddApiKey("X-API-Key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-API-Key", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new FeedbackApi(httpClient, config, httpClientHandler);
            var feedbackRequest = new FeedbackRequest(); // FeedbackRequest | 

            try
            {
                // Report a bug or send feedback
                Object result = apiInstance.FeedbackReportABugOrSendFeedback(feedbackRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling FeedbackApi.FeedbackReportABugOrSendFeedback: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FeedbackReportABugOrSendFeedbackWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Report a bug or send feedback
    ApiResponse<Object> response = apiInstance.FeedbackReportABugOrSendFeedbackWithHttpInfo(feedbackRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling FeedbackApi.FeedbackReportABugOrSendFeedbackWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **feedbackRequest** | [**FeedbackRequest**](FeedbackRequest.md) |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

