# ScrapeBadger.Api.NaverApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**NaverNaverBlogSearch**](NaverApi.md#navernaverblogsearch) | **GET** /v1/naver/blog | Naver blog search |
| [**NaverNaverDatalabShoppingKeywordInsight**](NaverApi.md#navernaverdatalabshoppingkeywordinsight) | **GET** /v1/naver/shopping/insight | Naver DataLab shopping keyword insight |
| [**NaverNaverNewsSearch**](NaverApi.md#navernavernewssearch) | **GET** /v1/naver/news | Naver news search |
| [**NaverNaverPlaceDetail**](NaverApi.md#navernaverplacedetail) | **GET** /v1/naver/place/{place_id} | Naver place detail |
| [**NaverNaverPlaceLocalSearch**](NaverApi.md#navernaverplacelocalsearch) | **GET** /v1/naver/local | Naver Place/Local search |
| [**NaverNaverPlaceVisitorReviews**](NaverApi.md#navernaverplacevisitorreviews) | **GET** /v1/naver/place/{place_id}/reviews | Naver place visitor reviews |
| [**NaverNaverScraperHealthCheck**](NaverApi.md#navernaverscraperhealthcheck) | **GET** /v1/naver/health | Naver scraper health check |
| [**NaverNaverScraperHealthCheckHead**](NaverApi.md#navernaverscraperhealthcheckhead) | **HEAD** /v1/naver/health | Naver scraper health check |
| [**NaverNaverShoppingBestsellerRankings**](NaverApi.md#navernavershoppingbestsellerrankings) | **GET** /v1/naver/shopping/bestsellers | Naver Shopping bestseller rankings |
| [**NaverNaverShoppingCategoryReference**](NaverApi.md#navernavershoppingcategoryreference) | **GET** /v1/naver/shopping/categories | Naver Shopping category reference |
| [**NaverNaverShoppingTrendingKeywordRankings**](NaverApi.md#navernavershoppingtrendingkeywordrankings) | **GET** /v1/naver/shopping/keywords | Naver Shopping trending keyword rankings |
| [**NaverNaverWebSearch**](NaverApi.md#navernaverwebsearch) | **GET** /v1/naver/search | Naver web search |
| [**NaverSearchSuggestions**](NaverApi.md#naversearchsuggestions) | **GET** /v1/naver/autocomplete | Search suggestions |

<a id="navernaverblogsearch"></a>
# **NaverNaverBlogSearch**
> Object NaverNaverBlogSearch (string query, int? page = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Naver blog search

Naver blog vertical — post title, blog name and real post URLs.

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
    public class NaverNaverBlogSearchExample
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
            var apiInstance = new NaverApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | 검색어
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
                // Naver blog search
                Object result = apiInstance.NaverNaverBlogSearch(query, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NaverApi.NaverNaverBlogSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the NaverNaverBlogSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Naver blog search
    ApiResponse<Object> response = apiInstance.NaverNaverBlogSearchWithHttpInfo(query, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NaverApi.NaverNaverBlogSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | 검색어 |  |
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

<a id="navernaverdatalabshoppingkeywordinsight"></a>
# **NaverNaverDatalabShoppingKeywordInsight**
> Object NaverNaverDatalabShoppingKeywordInsight (string categoryId, string startDate, string endDate, string timeUnit = null, int? count = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Naver DataLab shopping keyword insight

DataLab Shopping Insight — top search keywords in a category over a window.

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
    public class NaverNaverDatalabShoppingKeywordInsightExample
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
            var apiInstance = new NaverApi(httpClient, config, httpClientHandler);
            var categoryId = "categoryId_example";  // string | DataLab category id (cid), e.g. 50000000
            var startDate = "startDate_example";  // string | YYYY-MM-DD
            var endDate = "endDate_example";  // string | YYYY-MM-DD
            var timeUnit = "\"date\"";  // string | date | week | month (optional)  (default to "date")
            var count = 20;  // int? | Keywords to return (optional)  (default to 20)
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Naver DataLab shopping keyword insight
                Object result = apiInstance.NaverNaverDatalabShoppingKeywordInsight(categoryId, startDate, endDate, timeUnit, count, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NaverApi.NaverNaverDatalabShoppingKeywordInsight: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the NaverNaverDatalabShoppingKeywordInsightWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Naver DataLab shopping keyword insight
    ApiResponse<Object> response = apiInstance.NaverNaverDatalabShoppingKeywordInsightWithHttpInfo(categoryId, startDate, endDate, timeUnit, count, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NaverApi.NaverNaverDatalabShoppingKeywordInsightWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **categoryId** | **string** | DataLab category id (cid), e.g. 50000000 |  |
| **startDate** | **string** | YYYY-MM-DD |  |
| **endDate** | **string** | YYYY-MM-DD |  |
| **timeUnit** | **string** | date | week | month | [optional] [default to &quot;date&quot;] |
| **count** | **int?** | Keywords to return | [optional] [default to 20] |
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

<a id="navernavernewssearch"></a>
# **NaverNaverNewsSearch**
> Object NaverNaverNewsSearch (string query, int? page = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Naver news search

Naver news vertical — publisher, age string and real article URLs.

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
    public class NaverNaverNewsSearchExample
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
            var apiInstance = new NaverApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | 검색어
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
                // Naver news search
                Object result = apiInstance.NaverNaverNewsSearch(query, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NaverApi.NaverNaverNewsSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the NaverNaverNewsSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Naver news search
    ApiResponse<Object> response = apiInstance.NaverNaverNewsSearchWithHttpInfo(query, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NaverApi.NaverNaverNewsSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | 검색어 |  |
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

<a id="navernaverplacedetail"></a>
# **NaverNaverPlaceDetail**
> Object NaverNaverPlaceDetail (string placeId, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Naver place detail

Naver Place detail by place id.

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
    public class NaverNaverPlaceDetailExample
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
            var apiInstance = new NaverApi(httpClient, config, httpClientHandler);
            var placeId = "placeId_example";  // string | 
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Naver place detail
                Object result = apiInstance.NaverNaverPlaceDetail(placeId, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NaverApi.NaverNaverPlaceDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the NaverNaverPlaceDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Naver place detail
    ApiResponse<Object> response = apiInstance.NaverNaverPlaceDetailWithHttpInfo(placeId, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NaverApi.NaverNaverPlaceDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **placeId** | **string** |  |  |
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

<a id="navernaverplacelocalsearch"></a>
# **NaverNaverPlaceLocalSearch**
> Object NaverNaverPlaceLocalSearch (string query, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Naver Place/Local search

Naver Place/Local search — name, category, rating, hours status.

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
    public class NaverNaverPlaceLocalSearchExample
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
            var apiInstance = new NaverApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Place query, e.g. '성남 카페'
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Naver Place/Local search
                Object result = apiInstance.NaverNaverPlaceLocalSearch(query, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NaverApi.NaverNaverPlaceLocalSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the NaverNaverPlaceLocalSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Naver Place/Local search
    ApiResponse<Object> response = apiInstance.NaverNaverPlaceLocalSearchWithHttpInfo(query, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NaverApi.NaverNaverPlaceLocalSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Place query, e.g. &#39;성남 카페&#39; |  |
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

<a id="navernaverplacevisitorreviews"></a>
# **NaverNaverPlaceVisitorReviews**
> Object NaverNaverPlaceVisitorReviews (string placeId, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Naver place visitor reviews

Visitor reviews for a Naver place — rating, body, reviewer, voted keywords, photos.

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
    public class NaverNaverPlaceVisitorReviewsExample
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
            var apiInstance = new NaverApi(httpClient, config, httpClientHandler);
            var placeId = "placeId_example";  // string | 
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Naver place visitor reviews
                Object result = apiInstance.NaverNaverPlaceVisitorReviews(placeId, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NaverApi.NaverNaverPlaceVisitorReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the NaverNaverPlaceVisitorReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Naver place visitor reviews
    ApiResponse<Object> response = apiInstance.NaverNaverPlaceVisitorReviewsWithHttpInfo(placeId, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NaverApi.NaverNaverPlaceVisitorReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **placeId** | **string** |  |  |
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

<a id="navernaverscraperhealthcheck"></a>
# **NaverNaverScraperHealthCheck**
> Object NaverNaverScraperHealthCheck ()

Naver scraper health check

Check health of the Naver scraper service (accepts HEAD for UptimeRobot).

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
    public class NaverNaverScraperHealthCheckExample
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
            var apiInstance = new NaverApi(httpClient, config, httpClientHandler);

            try
            {
                // Naver scraper health check
                Object result = apiInstance.NaverNaverScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NaverApi.NaverNaverScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the NaverNaverScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Naver scraper health check
    ApiResponse<Object> response = apiInstance.NaverNaverScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NaverApi.NaverNaverScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="navernaverscraperhealthcheckhead"></a>
# **NaverNaverScraperHealthCheckHead**
> Object NaverNaverScraperHealthCheckHead ()

Naver scraper health check

Check health of the Naver scraper service (accepts HEAD for UptimeRobot).

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
    public class NaverNaverScraperHealthCheckHeadExample
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
            var apiInstance = new NaverApi(httpClient, config, httpClientHandler);

            try
            {
                // Naver scraper health check
                Object result = apiInstance.NaverNaverScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NaverApi.NaverNaverScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the NaverNaverScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Naver scraper health check
    ApiResponse<Object> response = apiInstance.NaverNaverScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NaverApi.NaverNaverScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="navernavershoppingbestsellerrankings"></a>
# **NaverNaverShoppingBestsellerRankings**
> Object NaverNaverShoppingBestsellerRankings (string categoryId = null, string ageType = null, string sortType = null, string periodType = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Naver Shopping bestseller rankings

Naver Shopping bestseller rankings — ranked products with price, review score, mall.

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
    public class NaverNaverShoppingBestsellerRankingsExample
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
            var apiInstance = new NaverApi(httpClient, config, httpClientHandler);
            var categoryId = "\"ALL\"";  // string | Naver shopping category id, or ALL (optional)  (default to "ALL")
            var ageType = "\"ALL\"";  // string | ALL | MEN_20 | WOMEN_20 | ... (optional)  (default to "ALL")
            var sortType = "\"PRODUCT_CLICK\"";  // string | PRODUCT_CLICK | PRODUCT_BUY (optional)  (default to "PRODUCT_CLICK")
            var periodType = "\"DAILY\"";  // string | DAILY | WEEKLY (optional)  (default to "DAILY")
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Naver Shopping bestseller rankings
                Object result = apiInstance.NaverNaverShoppingBestsellerRankings(categoryId, ageType, sortType, periodType, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NaverApi.NaverNaverShoppingBestsellerRankings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the NaverNaverShoppingBestsellerRankingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Naver Shopping bestseller rankings
    ApiResponse<Object> response = apiInstance.NaverNaverShoppingBestsellerRankingsWithHttpInfo(categoryId, ageType, sortType, periodType, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NaverApi.NaverNaverShoppingBestsellerRankingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **categoryId** | **string** | Naver shopping category id, or ALL | [optional] [default to &quot;ALL&quot;] |
| **ageType** | **string** | ALL | MEN_20 | WOMEN_20 | ... | [optional] [default to &quot;ALL&quot;] |
| **sortType** | **string** | PRODUCT_CLICK | PRODUCT_BUY | [optional] [default to &quot;PRODUCT_CLICK&quot;] |
| **periodType** | **string** | DAILY | WEEKLY | [optional] [default to &quot;DAILY&quot;] |
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

<a id="navernavershoppingcategoryreference"></a>
# **NaverNaverShoppingCategoryReference**
> Object NaverNaverShoppingCategoryReference (string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Naver Shopping category reference

Naver Shopping top-level category ids (for bestsellers/keywords/insight). Free.

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
    public class NaverNaverShoppingCategoryReferenceExample
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
            var apiInstance = new NaverApi(httpClient, config, httpClientHandler);
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Naver Shopping category reference
                Object result = apiInstance.NaverNaverShoppingCategoryReference(prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NaverApi.NaverNaverShoppingCategoryReference: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the NaverNaverShoppingCategoryReferenceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Naver Shopping category reference
    ApiResponse<Object> response = apiInstance.NaverNaverShoppingCategoryReferenceWithHttpInfo(prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NaverApi.NaverNaverShoppingCategoryReferenceWithHttpInfo: " + e.Message);
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

<a id="navernavershoppingtrendingkeywordrankings"></a>
# **NaverNaverShoppingTrendingKeywordRankings**
> Object NaverNaverShoppingTrendingKeywordRankings (string categoryId, string ageType = null, string sortType = null, string periodType = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Naver Shopping trending keyword rankings

Trending Naver Shopping keywords for a category (snxbest keyword rankings).

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
    public class NaverNaverShoppingTrendingKeywordRankingsExample
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
            var apiInstance = new NaverApi(httpClient, config, httpClientHandler);
            var categoryId = "categoryId_example";  // string | Naver shopping category id (see /shopping/categories)
            var ageType = "\"ALL\"";  // string | ALL | MEN_20 | WOMEN_20 | ... (optional)  (default to "ALL")
            var sortType = "\"KEYWORD_POPULAR\"";  // string |  (optional)  (default to "KEYWORD_POPULAR")
            var periodType = "\"WEEKLY\"";  // string | DAILY | WEEKLY (optional)  (default to "WEEKLY")
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Naver Shopping trending keyword rankings
                Object result = apiInstance.NaverNaverShoppingTrendingKeywordRankings(categoryId, ageType, sortType, periodType, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NaverApi.NaverNaverShoppingTrendingKeywordRankings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the NaverNaverShoppingTrendingKeywordRankingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Naver Shopping trending keyword rankings
    ApiResponse<Object> response = apiInstance.NaverNaverShoppingTrendingKeywordRankingsWithHttpInfo(categoryId, ageType, sortType, periodType, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NaverApi.NaverNaverShoppingTrendingKeywordRankingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **categoryId** | **string** | Naver shopping category id (see /shopping/categories) |  |
| **ageType** | **string** | ALL | MEN_20 | WOMEN_20 | ... | [optional] [default to &quot;ALL&quot;] |
| **sortType** | **string** |  | [optional] [default to &quot;KEYWORD_POPULAR&quot;] |
| **periodType** | **string** | DAILY | WEEKLY | [optional] [default to &quot;WEEKLY&quot;] |
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

<a id="navernaverwebsearch"></a>
# **NaverNaverWebSearch**
> Object NaverNaverWebSearch (string query, int? page = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Naver web search

Naver integrated SERP — organic results plus the inline Place pack.

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
    public class NaverNaverWebSearchExample
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
            var apiInstance = new NaverApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | 검색어, e.g. '성남 카페'
            var page = 1;  // int? | Result page (optional)  (default to 1)
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Naver web search
                Object result = apiInstance.NaverNaverWebSearch(query, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NaverApi.NaverNaverWebSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the NaverNaverWebSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Naver web search
    ApiResponse<Object> response = apiInstance.NaverNaverWebSearchWithHttpInfo(query, page, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NaverApi.NaverNaverWebSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | 검색어, e.g. &#39;성남 카페&#39; |  |
| **page** | **int?** | Result page | [optional] [default to 1] |
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

<a id="naversearchsuggestions"></a>
# **NaverSearchSuggestions**
> Object NaverSearchSuggestions (string query, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Search suggestions

Naver search-box suggestions.

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
    public class NaverSearchSuggestionsExample
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
            var apiInstance = new NaverApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Partial search term
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
                Object result = apiInstance.NaverSearchSuggestions(query, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NaverApi.NaverSearchSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the NaverSearchSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search suggestions
    ApiResponse<Object> response = apiInstance.NaverSearchSuggestionsWithHttpInfo(query, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NaverApi.NaverSearchSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Partial search term |  |
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

