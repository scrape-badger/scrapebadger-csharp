# ScrapeBadger.Api.GitHubApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GithubGetProfile**](GitHubApi.md#githubgetprofile) | **GET** /v1/github/profiles/{username} | Get profile |
| [**GithubGetRepository**](GitHubApi.md#githubgetrepository) | **GET** /v1/github/repositories/{owner}/{repo} | Get repository |

<a id="githubgetprofile"></a>
# **GithubGetProfile**
> GitHubProfileResponse GithubGetProfile (string username, string tab = null, int? year = null, int? page = null, string nextPageToken = null, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Get profile

Public user or organization profile, pins/popular repositories, README and contributions.  The overview preserves GitHub's public website sections, including organization-specific metadata. Compact displayed counts are approximate and marked with *_approximate. Unavailable or blocked data is an unbilled error, never an empty success.

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
    public class GithubGetProfileExample
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
            var apiInstance = new GitHubApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var tab = "overview";  // string | Profile section; stars is available for users only (optional)  (default to overview)
            var year = 56;  // int? | Overview only: 1970 through the current UTC year; activity is December or current month (optional) 
            var page = 56;  // int? | Repositories only: page number, 30 rows per page (optional) 
            var nextPageToken = "nextPageToken_example";  // string | Stars only: previous pagination.next_page_token (optional) 
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Get profile
                GitHubProfileResponse result = apiInstance.GithubGetProfile(username, tab, year, page, nextPageToken, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GitHubApi.GithubGetProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GithubGetProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get profile
    ApiResponse<GitHubProfileResponse> response = apiInstance.GithubGetProfileWithHttpInfo(username, tab, year, page, nextPageToken, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GitHubApi.GithubGetProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **tab** | **string** | Profile section; stars is available for users only | [optional] [default to overview] |
| **year** | **int?** | Overview only: 1970 through the current UTC year; activity is December or current month | [optional]  |
| **page** | **int?** | Repositories only: page number, 30 rows per page | [optional]  |
| **nextPageToken** | **string** | Stars only: previous pagination.next_page_token | [optional]  |
| **prefer** | **string** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional]  |
| **xCallbackURL** | **string** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional]  |
| **idempotencyKey** | **string** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional]  |
| **async** | **bool?** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional]  |
| **asyncWait** | **int?** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional]  |
| **callbackUrl** | **string** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional]  |
| **idempotencyKey2** | **string** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional]  |

### Return type

[**GitHubProfileResponse**](GitHubProfileResponse.md)

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

<a id="githubgetrepository"></a>
# **GithubGetRepository**
> GitHubRepositoryResponse GithubGetRepository (string owner, string repo, string prefer = null, string xCallbackURL = null, string idempotencyKey = null, bool? async = null, int? asyncWait = null, string callbackUrl = null, string idempotencyKey2 = null)

Get repository

Public default-branch repository detail, native README, files and latest commit.  Use owner.login and name from a profile repository summary. Root file and contributor previews are not exhaustive recursive trees or membership lists. No GitHub token, market, ref, search or pagination parameter is accepted.

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
    public class GithubGetRepositoryExample
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
            var apiInstance = new GitHubApi(httpClient, config, httpClientHandler);
            var owner = "owner_example";  // string | 
            var repo = "repo_example";  // string | 
            var prefer = respond-async, wait=25;  // string | `respond-async[, wait=N]` (RFC 7240): run the call async. If it has not finished after `wait` seconds (0-120, default 25) the answer is `202` with a `request_id`; poll `GET /v1/requests/{request_id}`. Its `wait=` wins over `async_wait`; without one, `async_wait` sets the wait. (optional) 
            var xCallbackURL = "xCallbackURL_example";  // string | An `https` URL that receives the signed `request.completed` webhook when the call finishes. Implies async: on its own (no `Prefer`, `async` or `async_wait`) the answer is an immediate `202`; with `Prefer: respond-async` or `async=true` the call still waits 25 s unless a wait is given. Wins over `callback_url`. (optional) 
            var idempotencyKey = "idempotencyKey_example";  // string | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call's current state (`Idempotent-Replayed: true`) without running or billing it again; on a different call it is `409 idempotency_key_reused`. Applies to async calls only; on a synchronous call it is ignored. Wins over `idempotency_key`. (optional) 
            var async = true;  // bool? | Query form of `Prefer: respond-async`: `true` or `1` (also `yes`, `on`; `false`, `0`, `no`, `off` leave the call synchronous). Waits 25 s unless `async_wait` is given. Not sent to the scraper. (optional) 
            var asyncWait = 56;  // int? | Seconds (0-120; values outside are clamped) to wait for the result before answering `202`. Implies async. Not sent to the scraper. (optional) 
            var callbackUrl = "callbackUrl_example";  // string | Query form of `X-Callback-URL` (URL-encode it). Implies async; on its own the answer is an immediate `202` (wait 0). Not sent to the scraper. (optional) 
            var idempotencyKey2 = "idempotencyKey_example";  // string | Query form of `Idempotency-Key`. Not sent to the scraper. (optional) 

            try
            {
                // Get repository
                GitHubRepositoryResponse result = apiInstance.GithubGetRepository(owner, repo, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GitHubApi.GithubGetRepository: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GithubGetRepositoryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get repository
    ApiResponse<GitHubRepositoryResponse> response = apiInstance.GithubGetRepositoryWithHttpInfo(owner, repo, prefer, xCallbackURL, idempotencyKey, async, asyncWait, callbackUrl, idempotencyKey2);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GitHubApi.GithubGetRepositoryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **owner** | **string** |  |  |
| **repo** | **string** |  |  |
| **prefer** | **string** | &#x60;respond-async[, wait&#x3D;N]&#x60; (RFC 7240): run the call async. If it has not finished after &#x60;wait&#x60; seconds (0-120, default 25) the answer is &#x60;202&#x60; with a &#x60;request_id&#x60;; poll &#x60;GET /v1/requests/{request_id}&#x60;. Its &#x60;wait&#x3D;&#x60; wins over &#x60;async_wait&#x60;; without one, &#x60;async_wait&#x60; sets the wait. | [optional]  |
| **xCallbackURL** | **string** | An &#x60;https&#x60; URL that receives the signed &#x60;request.completed&#x60; webhook when the call finishes. Implies async: on its own (no &#x60;Prefer&#x60;, &#x60;async&#x60; or &#x60;async_wait&#x60;) the answer is an immediate &#x60;202&#x60;; with &#x60;Prefer: respond-async&#x60; or &#x60;async&#x3D;true&#x60; the call still waits 25 s unless a wait is given. Wins over &#x60;callback_url&#x60;. | [optional]  |
| **idempotencyKey** | **string** | 1-200 visible ASCII characters, per account, kept as long as the result (about 15 minutes). The same key on the same call returns that call&#39;s current state (&#x60;Idempotent-Replayed: true&#x60;) without running or billing it again; on a different call it is &#x60;409 idempotency_key_reused&#x60;. Applies to async calls only; on a synchronous call it is ignored. Wins over &#x60;idempotency_key&#x60;. | [optional]  |
| **async** | **bool?** | Query form of &#x60;Prefer: respond-async&#x60;: &#x60;true&#x60; or &#x60;1&#x60; (also &#x60;yes&#x60;, &#x60;on&#x60;; &#x60;false&#x60;, &#x60;0&#x60;, &#x60;no&#x60;, &#x60;off&#x60; leave the call synchronous). Waits 25 s unless &#x60;async_wait&#x60; is given. Not sent to the scraper. | [optional]  |
| **asyncWait** | **int?** | Seconds (0-120; values outside are clamped) to wait for the result before answering &#x60;202&#x60;. Implies async. Not sent to the scraper. | [optional]  |
| **callbackUrl** | **string** | Query form of &#x60;X-Callback-URL&#x60; (URL-encode it). Implies async; on its own the answer is an immediate &#x60;202&#x60; (wait 0). Not sent to the scraper. | [optional]  |
| **idempotencyKey2** | **string** | Query form of &#x60;Idempotency-Key&#x60;. Not sent to the scraper. | [optional]  |

### Return type

[**GitHubRepositoryResponse**](GitHubRepositoryResponse.md)

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

