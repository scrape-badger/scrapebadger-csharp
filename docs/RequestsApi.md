# ScrapeBadger.Api.RequestsApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**RequestsCallbackStatus**](RequestsApi.md#requestscallbackstatus) | **GET** /v1/requests/{request_id}/callback | Callback status |
| [**RequestsPollAnAsyncRequest**](RequestsApi.md#requestspollanasyncrequest) | **GET** /v1/requests/{request_id} | Poll an async request |

<a id="requestscallbackstatus"></a>
# **RequestsCallbackStatus**
> AsyncCallbackStatus RequestsCallbackStatus (string requestId)

Callback status

Webhook delivery state of a call submitted with `X-Callback-URL` / `callback_url`: kept for 24 h. Free. `404 callback_not_found` for a request without a callback, of another account, or older than 24 h.

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
    public class RequestsCallbackStatusExample
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
            var apiInstance = new RequestsApi(httpClient, config, httpClientHandler);
            var requestId = "requestId_example";  // string | 

            try
            {
                // Callback status
                AsyncCallbackStatus result = apiInstance.RequestsCallbackStatus(requestId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RequestsApi.RequestsCallbackStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RequestsCallbackStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Callback status
    ApiResponse<AsyncCallbackStatus> response = apiInstance.RequestsCallbackStatusWithHttpInfo(requestId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RequestsApi.RequestsCallbackStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **requestId** | **string** |  |  |

### Return type

[**AsyncCallbackStatus**](AsyncCallbackStatus.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **404** | &#x60;callback_not_found&#x60;. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="requestspollanasyncrequest"></a>
# **RequestsPollAnAsyncRequest**
> Object RequestsPollAnAsyncRequest (string requestId)

Poll an async request

Status or final response of a call made with ``Prefer: respond-async``. While it runs: 202. When done: the original status, headers and body.  The final response carries `X-Callback-Status`, `X-Callback-Attempts` and `X-Callback-Error` for a call submitted with a callback; while it runs, the `202` body has a `callback` object. Full delivery state: `GET /v1/requests/{request_id}/callback`.

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
    public class RequestsPollAnAsyncRequestExample
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
            var apiInstance = new RequestsApi(httpClient, config, httpClientHandler);
            var requestId = "requestId_example";  // string | 

            try
            {
                // Poll an async request
                Object result = apiInstance.RequestsPollAnAsyncRequest(requestId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RequestsApi.RequestsPollAnAsyncRequest: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RequestsPollAnAsyncRequestWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Poll an async request
    ApiResponse<Object> response = apiInstance.RequestsPollAnAsyncRequestWithHttpInfo(requestId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RequestsApi.RequestsPollAnAsyncRequestWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **requestId** | **string** |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |
| **202** | The call is still running. |  * Location - &#x60;/v1/requests/{request_id}&#x60;. <br>  * Retry-After - Seconds until the next poll. <br>  |
| **404** | &#x60;request_not_found&#x60;: unknown, another account&#39;s, or expired. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

