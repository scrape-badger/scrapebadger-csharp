# ScrapeBadger.Api.GitHubApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GithubGetProfile**](GitHubApi.md#githubgetprofile) | **GET** /v1/github/profiles/{username} | Get profile |
| [**GithubGetRepository**](GitHubApi.md#githubgetrepository) | **GET** /v1/github/repositories/{owner}/{repo} | Get repository |

<a id="githubgetprofile"></a>
# **GithubGetProfile**
> GitHubProfileResponse GithubGetProfile (string username, string tab = null, int? year = null, int? page = null, string nextPageToken = null)

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

            try
            {
                // Get profile
                GitHubProfileResponse result = apiInstance.GithubGetProfile(username, tab, year, page, nextPageToken);
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
    ApiResponse<GitHubProfileResponse> response = apiInstance.GithubGetProfileWithHttpInfo(username, tab, year, page, nextPageToken);
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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="githubgetrepository"></a>
# **GithubGetRepository**
> GitHubRepositoryResponse GithubGetRepository (string owner, string repo)

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

            try
            {
                // Get repository
                GitHubRepositoryResponse result = apiInstance.GithubGetRepository(owner, repo);
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
    ApiResponse<GitHubRepositoryResponse> response = apiInstance.GithubGetRepositoryWithHttpInfo(owner, repo);
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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

