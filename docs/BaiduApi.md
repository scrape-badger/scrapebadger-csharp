# ScrapeBadger.Api.BaiduApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BaiduBaiduImageSearch**](BaiduApi.md#baidubaiduimagesearch) | **GET** /v1/baidu/images | Baidu image search |
| [**BaiduBaiduNewsSearch**](BaiduApi.md#baidubaidunewssearch) | **GET** /v1/baidu/news | Baidu news search |
| [**BaiduBaiduScraperHealthCheck**](BaiduApi.md#baidubaiduscraperhealthcheck) | **GET** /v1/baidu/health | Baidu scraper health check |
| [**BaiduBaiduScraperHealthCheckHead**](BaiduApi.md#baidubaiduscraperhealthcheckhead) | **HEAD** /v1/baidu/health | Baidu scraper health check |
| [**BaiduBaiduWebSearch**](BaiduApi.md#baidubaiduwebsearch) | **GET** /v1/baidu/search | Baidu web search |
| [**BaiduSearchSuggestions**](BaiduApi.md#baidusearchsuggestions) | **GET** /v1/baidu/autocomplete | Search suggestions |

<a id="baidubaiduimagesearch"></a>
# **BaiduBaiduImageSearch**
> Object BaiduBaiduImageSearch (string query, int? page = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Baidu image search

Baidu image search via the acjson JSON API.

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
    public class BaiduBaiduImageSearchExample
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
            var apiInstance = new BaiduApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords
            var page = 1;  // int? | 30 images per page (optional)  (default to 1)
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Baidu image search
                Object result = apiInstance.BaiduBaiduImageSearch(query, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BaiduApi.BaiduBaiduImageSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BaiduBaiduImageSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Baidu image search
    ApiResponse<Object> response = apiInstance.BaiduBaiduImageSearchWithHttpInfo(query, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BaiduApi.BaiduBaiduImageSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords |  |
| **page** | **int?** | 30 images per page | [optional] [default to 1] |
| **prefer** | **string** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional]  |
| **xCallbackURL** | **string** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional]  |
| **idempotencyKey** | **string** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional]  |
| **async** | **bool?** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional]  |
| **asyncWait** | **int?** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional]  |
| **callbackUrl** | **string** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional]  |
| **idempotencyKey2** | **string** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional]  |

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
| **202** | Accepted: the async call is still running (it outlived its wait, or a callback was given with no wait). Poll &#x60;next_action.url&#x60;. A repeat with the same &#x60;Idempotency-Key&#x60; answers what that poll answers, with &#x60;Idempotent-Replayed: true&#x60;. |  * Location - &#x60;/v1/requests/{request_id}&#x60;. <br>  * Retry-After - Seconds until the next poll. <br>  * Idempotent-Replayed - &#x60;true&#x60; when this answers an earlier call with the same key. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="baidubaidunewssearch"></a>
# **BaiduBaiduNewsSearch**
> Object BaiduBaiduNewsSearch (string query, int? page = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Baidu news search

Baidu news vertical — articles with source, publish date and real URLs.

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
    public class BaiduBaiduNewsSearchExample
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
            var apiInstance = new BaiduApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords
            var page = 1;  // int? |  (optional)  (default to 1)
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Baidu news search
                Object result = apiInstance.BaiduBaiduNewsSearch(query, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BaiduApi.BaiduBaiduNewsSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BaiduBaiduNewsSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Baidu news search
    ApiResponse<Object> response = apiInstance.BaiduBaiduNewsSearchWithHttpInfo(query, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BaiduApi.BaiduBaiduNewsSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **prefer** | **string** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional]  |
| **xCallbackURL** | **string** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional]  |
| **idempotencyKey** | **string** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional]  |
| **async** | **bool?** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional]  |
| **asyncWait** | **int?** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional]  |
| **callbackUrl** | **string** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional]  |
| **idempotencyKey2** | **string** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional]  |

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
| **202** | Accepted: the async call is still running (it outlived its wait, or a callback was given with no wait). Poll &#x60;next_action.url&#x60;. A repeat with the same &#x60;Idempotency-Key&#x60; answers what that poll answers, with &#x60;Idempotent-Replayed: true&#x60;. |  * Location - &#x60;/v1/requests/{request_id}&#x60;. <br>  * Retry-After - Seconds until the next poll. <br>  * Idempotent-Replayed - &#x60;true&#x60; when this answers an earlier call with the same key. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="baidubaiduscraperhealthcheck"></a>
# **BaiduBaiduScraperHealthCheck**
> Object BaiduBaiduScraperHealthCheck ()

Baidu scraper health check

Check health of the Baidu scraper service (accepts HEAD for UptimeRobot).

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
    public class BaiduBaiduScraperHealthCheckExample
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
            var apiInstance = new BaiduApi(httpClient, config, httpClientHandler);

            try
            {
                // Baidu scraper health check
                Object result = apiInstance.BaiduBaiduScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BaiduApi.BaiduBaiduScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BaiduBaiduScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Baidu scraper health check
    ApiResponse<Object> response = apiInstance.BaiduBaiduScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BaiduApi.BaiduBaiduScraperHealthCheckWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="baidubaiduscraperhealthcheckhead"></a>
# **BaiduBaiduScraperHealthCheckHead**
> Object BaiduBaiduScraperHealthCheckHead ()

Baidu scraper health check

Check health of the Baidu scraper service (accepts HEAD for UptimeRobot).

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
    public class BaiduBaiduScraperHealthCheckHeadExample
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
            var apiInstance = new BaiduApi(httpClient, config, httpClientHandler);

            try
            {
                // Baidu scraper health check
                Object result = apiInstance.BaiduBaiduScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BaiduApi.BaiduBaiduScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BaiduBaiduScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Baidu scraper health check
    ApiResponse<Object> response = apiInstance.BaiduBaiduScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BaiduApi.BaiduBaiduScraperHealthCheckHeadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="baidubaiduwebsearch"></a>
# **BaiduBaiduWebSearch**
> Object BaiduBaiduWebSearch (string query, int? page = null, int? num = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Baidu web search

Baidu web SERP — organic results with real target URLs, related searches, total count.

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
    public class BaiduBaiduWebSearchExample
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
            var apiInstance = new BaiduApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords, e.g. '咖啡机' or 'coffee machine'
            var page = 1;  // int? | Result page (10 results per page) (optional)  (default to 1)
            var num = 10;  // int? | Results per page (rn) (optional)  (default to 10)
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Baidu web search
                Object result = apiInstance.BaiduBaiduWebSearch(query, page, num, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BaiduApi.BaiduBaiduWebSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BaiduBaiduWebSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Baidu web search
    ApiResponse<Object> response = apiInstance.BaiduBaiduWebSearchWithHttpInfo(query, page, num, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BaiduApi.BaiduBaiduWebSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords, e.g. &#39;咖啡机&#39; or &#39;coffee machine&#39; |  |
| **page** | **int?** | Result page (10 results per page) | [optional] [default to 1] |
| **num** | **int?** | Results per page (rn) | [optional] [default to 10] |
| **prefer** | **string** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional]  |
| **xCallbackURL** | **string** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional]  |
| **idempotencyKey** | **string** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional]  |
| **async** | **bool?** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional]  |
| **asyncWait** | **int?** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional]  |
| **callbackUrl** | **string** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional]  |
| **idempotencyKey2** | **string** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional]  |

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
| **202** | Accepted: the async call is still running (it outlived its wait, or a callback was given with no wait). Poll &#x60;next_action.url&#x60;. A repeat with the same &#x60;Idempotency-Key&#x60; answers what that poll answers, with &#x60;Idempotent-Replayed: true&#x60;. |  * Location - &#x60;/v1/requests/{request_id}&#x60;. <br>  * Retry-After - Seconds until the next poll. <br>  * Idempotent-Replayed - &#x60;true&#x60; when this answers an earlier call with the same key. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="baidusearchsuggestions"></a>
# **BaiduSearchSuggestions**
> Object BaiduSearchSuggestions (string query, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Search suggestions

Baidu search-box suggestions.

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
    public class BaiduSearchSuggestionsExample
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
            var apiInstance = new BaiduApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Partial search term, e.g. '咖啡' or 'coff'
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Search suggestions
                Object result = apiInstance.BaiduSearchSuggestions(query, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BaiduApi.BaiduSearchSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BaiduSearchSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search suggestions
    ApiResponse<Object> response = apiInstance.BaiduSearchSuggestionsWithHttpInfo(query, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BaiduApi.BaiduSearchSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Partial search term, e.g. &#39;咖啡&#39; or &#39;coff&#39; |  |
| **prefer** | **string** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional]  |
| **xCallbackURL** | **string** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional]  |
| **idempotencyKey** | **string** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional]  |
| **async** | **bool?** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional]  |
| **asyncWait** | **int?** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional]  |
| **callbackUrl** | **string** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional]  |
| **idempotencyKey2** | **string** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional]  |

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
| **202** | Accepted: the async call is still running (it outlived its wait, or a callback was given with no wait). Poll &#x60;next_action.url&#x60;. A repeat with the same &#x60;Idempotency-Key&#x60; answers what that poll answers, with &#x60;Idempotent-Replayed: true&#x60;. |  * Location - &#x60;/v1/requests/{request_id}&#x60;. <br>  * Retry-After - Seconds until the next poll. <br>  * Idempotent-Replayed - &#x60;true&#x60; when this answers an earlier call with the same key. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

