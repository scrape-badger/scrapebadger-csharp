# ScrapeBadger.Api.DuckDuckGoApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DuckduckgoDuckduckgoScraperHealthCheck**](DuckDuckGoApi.md#duckduckgoduckduckgoscraperhealthcheck) | **GET** /v1/duckduckgo/health | DuckDuckGo scraper health check |
| [**DuckduckgoDuckduckgoScraperHealthCheckHead**](DuckDuckGoApi.md#duckduckgoduckduckgoscraperhealthcheckhead) | **HEAD** /v1/duckduckgo/health | DuckDuckGo scraper health check |
| [**DuckduckgoImageSearch**](DuckDuckGoApi.md#duckduckgoimagesearch) | **GET** /v1/duckduckgo/images | Image search |
| [**DuckduckgoInstantAnswer**](DuckDuckGoApi.md#duckduckgoinstantanswer) | **GET** /v1/duckduckgo/instant | Instant Answer |
| [**DuckduckgoListSupportedRegions**](DuckDuckGoApi.md#duckduckgolistsupportedregions) | **GET** /v1/duckduckgo/regions | List supported regions |
| [**DuckduckgoNewsSearch**](DuckDuckGoApi.md#duckduckgonewssearch) | **GET** /v1/duckduckgo/news | News search |
| [**DuckduckgoSearchSuggestions**](DuckDuckGoApi.md#duckduckgosearchsuggestions) | **GET** /v1/duckduckgo/autocomplete | Search suggestions |
| [**DuckduckgoVideoSearch**](DuckDuckGoApi.md#duckduckgovideosearch) | **GET** /v1/duckduckgo/videos | Video search |
| [**DuckduckgoWebSearch**](DuckDuckGoApi.md#duckduckgowebsearch) | **GET** /v1/duckduckgo/search | Web search |

<a id="duckduckgoduckduckgoscraperhealthcheck"></a>
# **DuckduckgoDuckduckgoScraperHealthCheck**
> Object DuckduckgoDuckduckgoScraperHealthCheck ()

DuckDuckGo scraper health check

Check health of the DuckDuckGo scraper service (accepts HEAD for UptimeRobot).

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
    public class DuckduckgoDuckduckgoScraperHealthCheckExample
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
            var apiInstance = new DuckDuckGoApi(httpClient, config, httpClientHandler);

            try
            {
                // DuckDuckGo scraper health check
                Object result = apiInstance.DuckduckgoDuckduckgoScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoDuckduckgoScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuckduckgoDuckduckgoScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // DuckDuckGo scraper health check
    ApiResponse<Object> response = apiInstance.DuckduckgoDuckduckgoScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoDuckduckgoScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="duckduckgoduckduckgoscraperhealthcheckhead"></a>
# **DuckduckgoDuckduckgoScraperHealthCheckHead**
> Object DuckduckgoDuckduckgoScraperHealthCheckHead ()

DuckDuckGo scraper health check

Check health of the DuckDuckGo scraper service (accepts HEAD for UptimeRobot).

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
    public class DuckduckgoDuckduckgoScraperHealthCheckHeadExample
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
            var apiInstance = new DuckDuckGoApi(httpClient, config, httpClientHandler);

            try
            {
                // DuckDuckGo scraper health check
                Object result = apiInstance.DuckduckgoDuckduckgoScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoDuckduckgoScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuckduckgoDuckduckgoScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // DuckDuckGo scraper health check
    ApiResponse<Object> response = apiInstance.DuckduckgoDuckduckgoScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoDuckduckgoScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="duckduckgoimagesearch"></a>
# **DuckduckgoImageSearch**
> Object DuckduckgoImageSearch (string query, string region = null, string safesearch = null, int? page = null, string size = null, string color = null, string imageType = null, string layout = null, string license = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Image search

DuckDuckGo image search with size/color/type/layout/license filters.

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
    public class DuckduckgoImageSearchExample
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
            var apiInstance = new DuckDuckGoApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search query
            var region = "\"wt-wt\"";  // string | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. (optional)  (default to "wt-wt")
            var safesearch = "\"moderate\"";  // string | on | moderate | off (optional)  (default to "moderate")
            var page = 1;  // int? | 100 results per page (optional)  (default to 1)
            var size = "\"\"";  // string | Small | Medium | Large | Wallpaper (optional)  (default to "")
            var color = "\"\"";  // string | color | Monochrome | Red | Blue | … (optional)  (default to "")
            var imageType = "\"\"";  // string | photo | clipart | gif | transparent | line (optional)  (default to "")
            var layout = "\"\"";  // string | Square | Tall | Wide (optional)  (default to "")
            var license = "\"\"";  // string | Any | Public | Share | ShareCommercially | Modify (optional)  (default to "")
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Image search
                Object result = apiInstance.DuckduckgoImageSearch(query, region, safesearch, page, size, color, imageType, layout, license, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoImageSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuckduckgoImageSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Image search
    ApiResponse<Object> response = apiInstance.DuckduckgoImageSearchWithHttpInfo(query, region, safesearch, page, size, color, imageType, layout, license, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoImageSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search query |  |
| **region** | **string** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &quot;wt-wt&quot;] |
| **safesearch** | **string** | on | moderate | off | [optional] [default to &quot;moderate&quot;] |
| **page** | **int?** | 100 results per page | [optional] [default to 1] |
| **size** | **string** | Small | Medium | Large | Wallpaper | [optional] [default to &quot;&quot;] |
| **color** | **string** | color | Monochrome | Red | Blue | … | [optional] [default to &quot;&quot;] |
| **imageType** | **string** | photo | clipart | gif | transparent | line | [optional] [default to &quot;&quot;] |
| **layout** | **string** | Square | Tall | Wide | [optional] [default to &quot;&quot;] |
| **license** | **string** | Any | Public | Share | ShareCommercially | Modify | [optional] [default to &quot;&quot;] |
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

<a id="duckduckgoinstantanswer"></a>
# **DuckduckgoInstantAnswer**
> Object DuckduckgoInstantAnswer (string query, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Instant Answer

DuckDuckGo Instant Answer — abstract, definition, direct answer, related topics.

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
    public class DuckduckgoInstantAnswerExample
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
            var apiInstance = new DuckDuckGoApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Query for the Instant Answer API
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Instant Answer
                Object result = apiInstance.DuckduckgoInstantAnswer(query, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoInstantAnswer: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuckduckgoInstantAnswerWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Instant Answer
    ApiResponse<Object> response = apiInstance.DuckduckgoInstantAnswerWithHttpInfo(query, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoInstantAnswerWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Query for the Instant Answer API |  |
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

<a id="duckduckgolistsupportedregions"></a>
# **DuckduckgoListSupportedRegions**
> Object DuckduckgoListSupportedRegions (string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

List supported regions

The full DuckDuckGo region (kl) code list.

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
    public class DuckduckgoListSupportedRegionsExample
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
            var apiInstance = new DuckDuckGoApi(httpClient, config, httpClientHandler);
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // List supported regions
                Object result = apiInstance.DuckduckgoListSupportedRegions(prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoListSupportedRegions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuckduckgoListSupportedRegionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List supported regions
    ApiResponse<Object> response = apiInstance.DuckduckgoListSupportedRegionsWithHttpInfo(prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoListSupportedRegionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
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
| **202** | Accepted: the async call is still running (it outlived its wait, or a callback was given with no wait). Poll &#x60;next_action.url&#x60;. A repeat with the same &#x60;Idempotency-Key&#x60; answers what that poll answers, with &#x60;Idempotent-Replayed: true&#x60;. |  * Location - &#x60;/v1/requests/{request_id}&#x60;. <br>  * Retry-After - Seconds until the next poll. <br>  * Idempotent-Replayed - &#x60;true&#x60; when this answers an earlier call with the same key. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="duckduckgonewssearch"></a>
# **DuckduckgoNewsSearch**
> Object DuckduckgoNewsSearch (string query, string region = null, string safesearch = null, string timelimit = null, int? page = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

News search

DuckDuckGo news search — headline, source, excerpt, unix + ISO date, image.

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
    public class DuckduckgoNewsSearchExample
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
            var apiInstance = new DuckDuckGoApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search query
            var region = "\"wt-wt\"";  // string | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. (optional)  (default to "wt-wt")
            var safesearch = "\"moderate\"";  // string | on | moderate | off (optional)  (default to "moderate")
            var timelimit = "\"\"";  // string | day | week | month | year (optional)  (default to "")
            var page = 1;  // int? | 30 results per page (optional)  (default to 1)
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // News search
                Object result = apiInstance.DuckduckgoNewsSearch(query, region, safesearch, timelimit, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoNewsSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuckduckgoNewsSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // News search
    ApiResponse<Object> response = apiInstance.DuckduckgoNewsSearchWithHttpInfo(query, region, safesearch, timelimit, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoNewsSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search query |  |
| **region** | **string** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &quot;wt-wt&quot;] |
| **safesearch** | **string** | on | moderate | off | [optional] [default to &quot;moderate&quot;] |
| **timelimit** | **string** | day | week | month | year | [optional] [default to &quot;&quot;] |
| **page** | **int?** | 30 results per page | [optional] [default to 1] |
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

<a id="duckduckgosearchsuggestions"></a>
# **DuckduckgoSearchSuggestions**
> Object DuckduckgoSearchSuggestions (string query, string region = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Search suggestions

DuckDuckGo search-box suggestions.

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
    public class DuckduckgoSearchSuggestionsExample
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
            var apiInstance = new DuckDuckGoApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Partial query to complete
            var region = "\"wt-wt\"";  // string | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. (optional)  (default to "wt-wt")
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
                Object result = apiInstance.DuckduckgoSearchSuggestions(query, region, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoSearchSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuckduckgoSearchSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search suggestions
    ApiResponse<Object> response = apiInstance.DuckduckgoSearchSuggestionsWithHttpInfo(query, region, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoSearchSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Partial query to complete |  |
| **region** | **string** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &quot;wt-wt&quot;] |
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

<a id="duckduckgovideosearch"></a>
# **DuckduckgoVideoSearch**
> Object DuckduckgoVideoSearch (string query, string region = null, string safesearch = null, int? page = null, string duration = null, string resolution = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Video search

DuckDuckGo video search — title, publisher, uploader, duration, views, thumbnails.

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
    public class DuckduckgoVideoSearchExample
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
            var apiInstance = new DuckDuckGoApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search query
            var region = "\"wt-wt\"";  // string | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. (optional)  (default to "wt-wt")
            var safesearch = "\"moderate\"";  // string | on | moderate | off (optional)  (default to "moderate")
            var page = 1;  // int? | 60 results per page (optional)  (default to 1)
            var duration = "\"\"";  // string | short | medium | long (optional)  (default to "")
            var resolution = "\"\"";  // string | high | standard (optional)  (default to "")
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Video search
                Object result = apiInstance.DuckduckgoVideoSearch(query, region, safesearch, page, duration, resolution, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoVideoSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuckduckgoVideoSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Video search
    ApiResponse<Object> response = apiInstance.DuckduckgoVideoSearchWithHttpInfo(query, region, safesearch, page, duration, resolution, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoVideoSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search query |  |
| **region** | **string** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &quot;wt-wt&quot;] |
| **safesearch** | **string** | on | moderate | off | [optional] [default to &quot;moderate&quot;] |
| **page** | **int?** | 60 results per page | [optional] [default to 1] |
| **duration** | **string** | short | medium | long | [optional] [default to &quot;&quot;] |
| **resolution** | **string** | high | standard | [optional] [default to &quot;&quot;] |
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

<a id="duckduckgowebsearch"></a>
# **DuckduckgoWebSearch**
> Object DuckduckgoWebSearch (string query, string region = null, string safesearch = null, string timelimit = null, int? page = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Web search

DuckDuckGo web SERP — organic results, the zero-click abstract box, ads flagged.

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
    public class DuckduckgoWebSearchExample
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
            var apiInstance = new DuckDuckGoApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search query
            var region = "\"wt-wt\"";  // string | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions. (optional)  (default to "wt-wt")
            var safesearch = "\"moderate\"";  // string | on | moderate | off (optional)  (default to "moderate")
            var timelimit = "\"\"";  // string | day | week | month | year (optional)  (default to "")
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
                // Web search
                Object result = apiInstance.DuckduckgoWebSearch(query, region, safesearch, timelimit, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoWebSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuckduckgoWebSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Web search
    ApiResponse<Object> response = apiInstance.DuckduckgoWebSearchWithHttpInfo(query, region, safesearch, timelimit, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DuckDuckGoApi.DuckduckgoWebSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search query |  |
| **region** | **string** | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to &quot;wt-wt&quot;] |
| **safesearch** | **string** | on | moderate | off | [optional] [default to &quot;moderate&quot;] |
| **timelimit** | **string** | day | week | month | year | [optional] [default to &quot;&quot;] |
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

