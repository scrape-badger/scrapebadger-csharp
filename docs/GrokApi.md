# ScrapeBadger.Api.GrokApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GrokAskGrokAQuestion**](GrokApi.md#grokaskgrokaquestion) | **GET** /v1/grok/ask | Ask Grok a question |
| [**GrokAskGrokAQuestionPost**](GrokApi.md#grokaskgrokaquestionpost) | **POST** /v1/grok/ask | Ask Grok a question (POST) |
| [**GrokGetAGrokConversation**](GrokApi.md#grokgetagrokconversation) | **GET** /v1/grok/conversations/{conversation_id} | Get a Grok conversation |
| [**GrokGrokScraperHealthCheck**](GrokApi.md#grokgrokscraperhealthcheck) | **GET** /v1/grok/health | Grok scraper health check |
| [**GrokGrokScraperHealthCheckHead**](GrokApi.md#grokgrokscraperhealthcheckhead) | **HEAD** /v1/grok/health | Grok scraper health check |
| [**GrokListGrokAssistantModes**](GrokApi.md#groklistgrokassistantmodes) | **GET** /v1/grok/models | List Grok assistant modes |
| [**GrokMeasureBrandVisibilityInGrok**](GrokApi.md#grokmeasurebrandvisibilityingrok) | **GET** /v1/grok/brand-visibility | Measure brand visibility in Grok |
| [**GrokMeasureBrandVisibilityInGrokPost**](GrokApi.md#grokmeasurebrandvisibilityingrokpost) | **POST** /v1/grok/brand-visibility | Measure brand visibility in Grok (POST) |

<a id="grokaskgrokaquestion"></a>
# **GrokAskGrokAQuestion**
> Object GrokAskGrokAQuestion (string prompt, string conversationId = null, string mode = null, string webSearch = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Ask Grok a question

Ask the real Grok assistant and get its answer, web sources, and X post references.

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
    public class GrokAskGrokAQuestionExample
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
            var apiInstance = new GrokApi(httpClient, config, httpClientHandler);
            var prompt = "prompt_example";  // string | Prompt to send to Grok (max 4000 characters).
            var conversationId = "conversationId_example";  // string | Existing Grok conversation to continue. (optional) 
            var mode = "\"auto\"";  // string | Assistant mode: auto, fast, or expert. (optional)  (default to "auto")
            var webSearch = "\"auto\"";  // string | Web and X search: auto, force, or off. (optional)  (default to "auto")
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Ask Grok a question
                Object result = apiInstance.GrokAskGrokAQuestion(prompt, conversationId, mode, webSearch, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GrokApi.GrokAskGrokAQuestion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GrokAskGrokAQuestionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ask Grok a question
    ApiResponse<Object> response = apiInstance.GrokAskGrokAQuestionWithHttpInfo(prompt, conversationId, mode, webSearch, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GrokApi.GrokAskGrokAQuestionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **prompt** | **string** | Prompt to send to Grok (max 4000 characters). |  |
| **conversationId** | **string** | Existing Grok conversation to continue. | [optional]  |
| **mode** | **string** | Assistant mode: auto, fast, or expert. | [optional] [default to &quot;auto&quot;] |
| **webSearch** | **string** | Web and X search: auto, force, or off. | [optional] [default to &quot;auto&quot;] |
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

<a id="grokaskgrokaquestionpost"></a>
# **GrokAskGrokAQuestionPost**
> Object GrokAskGrokAQuestionPost (string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Ask Grok a question (POST)

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
    public class GrokAskGrokAQuestionPostExample
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
            var apiInstance = new GrokApi(httpClient, config, httpClientHandler);
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Ask Grok a question (POST)
                Object result = apiInstance.GrokAskGrokAQuestionPost(prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GrokApi.GrokAskGrokAQuestionPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GrokAskGrokAQuestionPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ask Grok a question (POST)
    ApiResponse<Object> response = apiInstance.GrokAskGrokAQuestionPostWithHttpInfo(prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GrokApi.GrokAskGrokAQuestionPostWithHttpInfo: " + e.Message);
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

<a id="grokgetagrokconversation"></a>
# **GrokGetAGrokConversation**
> Object GrokGetAGrokConversation (string conversationId, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Get a Grok conversation

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
    public class GrokGetAGrokConversationExample
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
            var apiInstance = new GrokApi(httpClient, config, httpClientHandler);
            var conversationId = "conversationId_example";  // string | 
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Get a Grok conversation
                Object result = apiInstance.GrokGetAGrokConversation(conversationId, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GrokApi.GrokGetAGrokConversation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GrokGetAGrokConversationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a Grok conversation
    ApiResponse<Object> response = apiInstance.GrokGetAGrokConversationWithHttpInfo(conversationId, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GrokApi.GrokGetAGrokConversationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **conversationId** | **string** |  |  |
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

<a id="grokgrokscraperhealthcheck"></a>
# **GrokGrokScraperHealthCheck**
> Object GrokGrokScraperHealthCheck ()

Grok scraper health check

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
    public class GrokGrokScraperHealthCheckExample
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
            var apiInstance = new GrokApi(httpClient, config, httpClientHandler);

            try
            {
                // Grok scraper health check
                Object result = apiInstance.GrokGrokScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GrokApi.GrokGrokScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GrokGrokScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Grok scraper health check
    ApiResponse<Object> response = apiInstance.GrokGrokScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GrokApi.GrokGrokScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="grokgrokscraperhealthcheckhead"></a>
# **GrokGrokScraperHealthCheckHead**
> Object GrokGrokScraperHealthCheckHead ()

Grok scraper health check

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
    public class GrokGrokScraperHealthCheckHeadExample
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
            var apiInstance = new GrokApi(httpClient, config, httpClientHandler);

            try
            {
                // Grok scraper health check
                Object result = apiInstance.GrokGrokScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GrokApi.GrokGrokScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GrokGrokScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Grok scraper health check
    ApiResponse<Object> response = apiInstance.GrokGrokScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GrokApi.GrokGrokScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="groklistgrokassistantmodes"></a>
# **GrokListGrokAssistantModes**
> Object GrokListGrokAssistantModes (string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

List Grok assistant modes

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
    public class GrokListGrokAssistantModesExample
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
            var apiInstance = new GrokApi(httpClient, config, httpClientHandler);
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // List Grok assistant modes
                Object result = apiInstance.GrokListGrokAssistantModes(prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GrokApi.GrokListGrokAssistantModes: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GrokListGrokAssistantModesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Grok assistant modes
    ApiResponse<Object> response = apiInstance.GrokListGrokAssistantModesWithHttpInfo(prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GrokApi.GrokListGrokAssistantModesWithHttpInfo: " + e.Message);
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

<a id="grokmeasurebrandvisibilityingrok"></a>
# **GrokMeasureBrandVisibilityInGrok**
> Object GrokMeasureBrandVisibilityInGrok (string prompt, string brand, List<string> competitors = null, string brandDomain = null, string mode = null, string webSearch = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Measure brand visibility in Grok

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
    public class GrokMeasureBrandVisibilityInGrokExample
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
            var apiInstance = new GrokApi(httpClient, config, httpClientHandler);
            var prompt = "prompt_example";  // string | Buyer or category prompt to send to Grok.
            var brand = "brand_example";  // string | Brand name to measure.
            var competitors = new List<string>(); // List<string> | Competitor brand names. (optional) 
            var brandDomain = "brandDomain_example";  // string | Brand domain for citation rank. (optional) 
            var mode = "\"auto\"";  // string | Assistant mode: auto, fast, or expert. (optional)  (default to "auto")
            var webSearch = "\"force\"";  // string | Web and X search mode. (optional)  (default to "force")
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Measure brand visibility in Grok
                Object result = apiInstance.GrokMeasureBrandVisibilityInGrok(prompt, brand, competitors, brandDomain, mode, webSearch, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GrokApi.GrokMeasureBrandVisibilityInGrok: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GrokMeasureBrandVisibilityInGrokWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Measure brand visibility in Grok
    ApiResponse<Object> response = apiInstance.GrokMeasureBrandVisibilityInGrokWithHttpInfo(prompt, brand, competitors, brandDomain, mode, webSearch, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GrokApi.GrokMeasureBrandVisibilityInGrokWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **prompt** | **string** | Buyer or category prompt to send to Grok. |  |
| **brand** | **string** | Brand name to measure. |  |
| **competitors** | [**List&lt;string&gt;**](string.md) | Competitor brand names. | [optional]  |
| **brandDomain** | **string** | Brand domain for citation rank. | [optional]  |
| **mode** | **string** | Assistant mode: auto, fast, or expert. | [optional] [default to &quot;auto&quot;] |
| **webSearch** | **string** | Web and X search mode. | [optional] [default to &quot;force&quot;] |
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

<a id="grokmeasurebrandvisibilityingrokpost"></a>
# **GrokMeasureBrandVisibilityInGrokPost**
> Object GrokMeasureBrandVisibilityInGrokPost (string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Measure brand visibility in Grok (POST)

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
    public class GrokMeasureBrandVisibilityInGrokPostExample
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
            var apiInstance = new GrokApi(httpClient, config, httpClientHandler);
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Measure brand visibility in Grok (POST)
                Object result = apiInstance.GrokMeasureBrandVisibilityInGrokPost(prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GrokApi.GrokMeasureBrandVisibilityInGrokPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GrokMeasureBrandVisibilityInGrokPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Measure brand visibility in Grok (POST)
    ApiResponse<Object> response = apiInstance.GrokMeasureBrandVisibilityInGrokPostWithHttpInfo(prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GrokApi.GrokMeasureBrandVisibilityInGrokPostWithHttpInfo: " + e.Message);
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

