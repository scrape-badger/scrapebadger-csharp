# ScrapeBadger.Api.RedditApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**RedditGetCrossPosts**](RedditApi.md#redditgetcrossposts) | **GET** /v1/reddit/posts/{post_id}/duplicates | Get cross-posts |
| [**RedditGetPostComments**](RedditApi.md#redditgetpostcomments) | **GET** /v1/reddit/posts/{post_id}/comments | Get post comments |
| [**RedditGetPostDetail**](RedditApi.md#redditgetpostdetail) | **GET** /v1/reddit/posts/{post_id} | Get post detail |
| [**RedditGetPostsByDomain**](RedditApi.md#redditgetpostsbydomain) | **GET** /v1/reddit/domains/{domain}/posts | Get posts by domain |
| [**RedditGetSubredditInfo**](RedditApi.md#redditgetsubredditinfo) | **GET** /v1/reddit/subreddits/{subreddit} | Get subreddit info |
| [**RedditGetSubredditPosts**](RedditApi.md#redditgetsubredditposts) | **GET** /v1/reddit/subreddits/{subreddit}/posts | Get subreddit posts |
| [**RedditGetSubredditRules**](RedditApi.md#redditgetsubredditrules) | **GET** /v1/reddit/subreddits/{subreddit}/rules | Get subreddit rules |
| [**RedditGetTrendingPosts**](RedditApi.md#redditgettrendingposts) | **GET** /v1/reddit/posts/trending | Get trending posts |
| [**RedditGetUserProfile**](RedditApi.md#redditgetuserprofile) | **GET** /v1/reddit/users/{username} | Get user profile |
| [**RedditGetUserSComments**](RedditApi.md#redditgetuserscomments) | **GET** /v1/reddit/users/{username}/comments | Get user&#39;s comments |
| [**RedditGetUserSModeratedSubreddits**](RedditApi.md#redditgetusersmoderatedsubreddits) | **GET** /v1/reddit/users/{username}/moderated | Get user&#39;s moderated subreddits |
| [**RedditGetUserSPosts**](RedditApi.md#redditgetusersposts) | **GET** /v1/reddit/users/{username}/posts | Get user&#39;s posts |
| [**RedditGetUserSTrophies**](RedditApi.md#redditgetuserstrophies) | **GET** /v1/reddit/users/{username}/trophies | Get user&#39;s trophies |
| [**RedditGetWikiPageContent**](RedditApi.md#redditgetwikipagecontent) | **GET** /v1/reddit/subreddits/{subreddit}/wiki/{page} | Get wiki page content |
| [**RedditListWikiPages**](RedditApi.md#redditlistwikipages) | **GET** /v1/reddit/subreddits/{subreddit}/wiki | List wiki pages |
| [**RedditNewSubreddits**](RedditApi.md#redditnewsubreddits) | **GET** /v1/reddit/subreddits/new | New subreddits |
| [**RedditPopularSubreddits**](RedditApi.md#redditpopularsubreddits) | **GET** /v1/reddit/subreddits/popular | Popular subreddits |
| [**RedditRedditScraperHealthCheck**](RedditApi.md#redditredditscraperhealthcheck) | **GET** /v1/reddit/health | Reddit scraper health check |
| [**RedditRedditScraperHealthCheckHead**](RedditApi.md#redditredditscraperhealthcheckhead) | **HEAD** /v1/reddit/health | Reddit scraper health check |
| [**RedditSearchRedditPosts**](RedditApi.md#redditsearchredditposts) | **GET** /v1/reddit/search/posts | Search Reddit posts |
| [**RedditSearchSubreddits**](RedditApi.md#redditsearchsubreddits) | **GET** /v1/reddit/search/subreddits | Search subreddits |
| [**RedditSearchUsers**](RedditApi.md#redditsearchusers) | **GET** /v1/reddit/search/users | Search users |

<a id="redditgetcrossposts"></a>
# **RedditGetCrossPosts**
> Object RedditGetCrossPosts (string postId, int? limit = null, string after = null)

Get cross-posts

Get cross-posts and duplicates of a Reddit post.

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
    public class RedditGetCrossPostsExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var postId = "postId_example";  // string | 
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string |  (optional) 

            try
            {
                // Get cross-posts
                Object result = apiInstance.RedditGetCrossPosts(postId, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetCrossPosts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetCrossPostsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get cross-posts
    ApiResponse<Object> response = apiInstance.RedditGetCrossPostsWithHttpInfo(postId, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetCrossPostsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **postId** | **string** |  |  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string** |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditgetpostcomments"></a>
# **RedditGetPostComments**
> Object RedditGetPostComments (string postId, string sort = null, int? limit = null, int? depth = null)

Get post comments

Get comment tree for a Reddit post.

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
    public class RedditGetPostCommentsExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var postId = "postId_example";  // string | 
            var sort = "\"confidence\"";  // string | Sort: confidence, top, new, controversial, old, qa (optional)  (default to "confidence")
            var limit = 25;  // int? |  (optional)  (default to 25)
            var depth = 56;  // int? |  (optional) 

            try
            {
                // Get post comments
                Object result = apiInstance.RedditGetPostComments(postId, sort, limit, depth);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetPostComments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetPostCommentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get post comments
    ApiResponse<Object> response = apiInstance.RedditGetPostCommentsWithHttpInfo(postId, sort, limit, depth);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetPostCommentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **postId** | **string** |  |  |
| **sort** | **string** | Sort: confidence, top, new, controversial, old, qa | [optional] [default to &quot;confidence&quot;] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **depth** | **int?** |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditgetpostdetail"></a>
# **RedditGetPostDetail**
> Object RedditGetPostDetail (string postId)

Get post detail

Get detailed information about a Reddit post.

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
    public class RedditGetPostDetailExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var postId = "postId_example";  // string | 

            try
            {
                // Get post detail
                Object result = apiInstance.RedditGetPostDetail(postId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetPostDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetPostDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get post detail
    ApiResponse<Object> response = apiInstance.RedditGetPostDetailWithHttpInfo(postId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetPostDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **postId** | **string** |  |  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditgetpostsbydomain"></a>
# **RedditGetPostsByDomain**
> Object RedditGetPostsByDomain (string domain, string sort = null, string t = null, int? limit = null, string after = null)

Get posts by domain

Get Reddit posts linking to a specific domain.

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
    public class RedditGetPostsByDomainExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var domain = "domain_example";  // string | 
            var sort = "\"hot\"";  // string |  (optional)  (default to "hot")
            var t = "\"all\"";  // string |  (optional)  (default to "all")
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string |  (optional) 

            try
            {
                // Get posts by domain
                Object result = apiInstance.RedditGetPostsByDomain(domain, sort, t, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetPostsByDomain: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetPostsByDomainWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get posts by domain
    ApiResponse<Object> response = apiInstance.RedditGetPostsByDomainWithHttpInfo(domain, sort, t, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetPostsByDomainWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **domain** | **string** |  |  |
| **sort** | **string** |  | [optional] [default to &quot;hot&quot;] |
| **t** | **string** |  | [optional] [default to &quot;all&quot;] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string** |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditgetsubredditinfo"></a>
# **RedditGetSubredditInfo**
> Object RedditGetSubredditInfo (string subreddit)

Get subreddit info

Get detailed information about a subreddit.

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
    public class RedditGetSubredditInfoExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var subreddit = "subreddit_example";  // string | 

            try
            {
                // Get subreddit info
                Object result = apiInstance.RedditGetSubredditInfo(subreddit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetSubredditInfo: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetSubredditInfoWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get subreddit info
    ApiResponse<Object> response = apiInstance.RedditGetSubredditInfoWithHttpInfo(subreddit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetSubredditInfoWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **subreddit** | **string** |  |  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditgetsubredditposts"></a>
# **RedditGetSubredditPosts**
> Object RedditGetSubredditPosts (string subreddit, string sort = null, string t = null, int? limit = null, string after = null)

Get subreddit posts

Get posts from a subreddit with sorting options.

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
    public class RedditGetSubredditPostsExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var subreddit = "subreddit_example";  // string | 
            var sort = "\"hot\"";  // string | Sort: hot, new, top, rising, controversial (optional)  (default to "hot")
            var t = "\"all\"";  // string | Time filter (optional)  (default to "all")
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string |  (optional) 

            try
            {
                // Get subreddit posts
                Object result = apiInstance.RedditGetSubredditPosts(subreddit, sort, t, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetSubredditPosts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetSubredditPostsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get subreddit posts
    ApiResponse<Object> response = apiInstance.RedditGetSubredditPostsWithHttpInfo(subreddit, sort, t, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetSubredditPostsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **subreddit** | **string** |  |  |
| **sort** | **string** | Sort: hot, new, top, rising, controversial | [optional] [default to &quot;hot&quot;] |
| **t** | **string** | Time filter | [optional] [default to &quot;all&quot;] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string** |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditgetsubredditrules"></a>
# **RedditGetSubredditRules**
> Object RedditGetSubredditRules (string subreddit)

Get subreddit rules

Get the rules of a subreddit.

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
    public class RedditGetSubredditRulesExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var subreddit = "subreddit_example";  // string | 

            try
            {
                // Get subreddit rules
                Object result = apiInstance.RedditGetSubredditRules(subreddit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetSubredditRules: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetSubredditRulesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get subreddit rules
    ApiResponse<Object> response = apiInstance.RedditGetSubredditRulesWithHttpInfo(subreddit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetSubredditRulesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **subreddit** | **string** |  |  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditgettrendingposts"></a>
# **RedditGetTrendingPosts**
> Object RedditGetTrendingPosts (string sort = null, string t = null, int? limit = null, string after = null)

Get trending posts

Get trending posts from Reddit's front page.

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
    public class RedditGetTrendingPostsExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var sort = "\"hot\"";  // string | Sort: hot, new, top, rising, controversial, best (optional)  (default to "hot")
            var t = "\"day\"";  // string | Time filter (optional)  (default to "day")
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string |  (optional) 

            try
            {
                // Get trending posts
                Object result = apiInstance.RedditGetTrendingPosts(sort, t, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetTrendingPosts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetTrendingPostsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get trending posts
    ApiResponse<Object> response = apiInstance.RedditGetTrendingPostsWithHttpInfo(sort, t, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetTrendingPostsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sort** | **string** | Sort: hot, new, top, rising, controversial, best | [optional] [default to &quot;hot&quot;] |
| **t** | **string** | Time filter | [optional] [default to &quot;day&quot;] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string** |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditgetuserprofile"></a>
# **RedditGetUserProfile**
> Object RedditGetUserProfile (string username)

Get user profile

Get a Reddit user's profile.

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
    public class RedditGetUserProfileExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 

            try
            {
                // Get user profile
                Object result = apiInstance.RedditGetUserProfile(username);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetUserProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetUserProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user profile
    ApiResponse<Object> response = apiInstance.RedditGetUserProfileWithHttpInfo(username);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetUserProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditgetuserscomments"></a>
# **RedditGetUserSComments**
> Object RedditGetUserSComments (string username, string sort = null, string t = null, int? limit = null, string after = null)

Get user's comments

Get comments by a Reddit user.

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
    public class RedditGetUserSCommentsExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var sort = "\"new\"";  // string |  (optional)  (default to "new")
            var t = "\"all\"";  // string |  (optional)  (default to "all")
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string |  (optional) 

            try
            {
                // Get user's comments
                Object result = apiInstance.RedditGetUserSComments(username, sort, t, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetUserSComments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetUserSCommentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user's comments
    ApiResponse<Object> response = apiInstance.RedditGetUserSCommentsWithHttpInfo(username, sort, t, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetUserSCommentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **sort** | **string** |  | [optional] [default to &quot;new&quot;] |
| **t** | **string** |  | [optional] [default to &quot;all&quot;] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string** |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditgetusersmoderatedsubreddits"></a>
# **RedditGetUserSModeratedSubreddits**
> Object RedditGetUserSModeratedSubreddits (string username)

Get user's moderated subreddits

Get subreddits moderated by a user.

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
    public class RedditGetUserSModeratedSubredditsExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 

            try
            {
                // Get user's moderated subreddits
                Object result = apiInstance.RedditGetUserSModeratedSubreddits(username);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetUserSModeratedSubreddits: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetUserSModeratedSubredditsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user's moderated subreddits
    ApiResponse<Object> response = apiInstance.RedditGetUserSModeratedSubredditsWithHttpInfo(username);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetUserSModeratedSubredditsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditgetusersposts"></a>
# **RedditGetUserSPosts**
> Object RedditGetUserSPosts (string username, string sort = null, string t = null, int? limit = null, string after = null)

Get user's posts

Get posts submitted by a Reddit user.

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
    public class RedditGetUserSPostsExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var sort = "\"new\"";  // string |  (optional)  (default to "new")
            var t = "\"all\"";  // string |  (optional)  (default to "all")
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string |  (optional) 

            try
            {
                // Get user's posts
                Object result = apiInstance.RedditGetUserSPosts(username, sort, t, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetUserSPosts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetUserSPostsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user's posts
    ApiResponse<Object> response = apiInstance.RedditGetUserSPostsWithHttpInfo(username, sort, t, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetUserSPostsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **sort** | **string** |  | [optional] [default to &quot;new&quot;] |
| **t** | **string** |  | [optional] [default to &quot;all&quot;] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string** |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditgetuserstrophies"></a>
# **RedditGetUserSTrophies**
> Object RedditGetUserSTrophies (string username)

Get user's trophies

Get a user's trophy case.

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
    public class RedditGetUserSTrophiesExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 

            try
            {
                // Get user's trophies
                Object result = apiInstance.RedditGetUserSTrophies(username);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetUserSTrophies: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetUserSTrophiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user's trophies
    ApiResponse<Object> response = apiInstance.RedditGetUserSTrophiesWithHttpInfo(username);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetUserSTrophiesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditgetwikipagecontent"></a>
# **RedditGetWikiPageContent**
> Object RedditGetWikiPageContent (string subreddit, string page)

Get wiki page content

Get the content of a specific wiki page.

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
    public class RedditGetWikiPageContentExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var subreddit = "subreddit_example";  // string | 
            var page = "page_example";  // string | 

            try
            {
                // Get wiki page content
                Object result = apiInstance.RedditGetWikiPageContent(subreddit, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditGetWikiPageContent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditGetWikiPageContentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get wiki page content
    ApiResponse<Object> response = apiInstance.RedditGetWikiPageContentWithHttpInfo(subreddit, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditGetWikiPageContentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **subreddit** | **string** |  |  |
| **page** | **string** |  |  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditlistwikipages"></a>
# **RedditListWikiPages**
> Object RedditListWikiPages (string subreddit)

List wiki pages

List all wiki pages in a subreddit.

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
    public class RedditListWikiPagesExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var subreddit = "subreddit_example";  // string | 

            try
            {
                // List wiki pages
                Object result = apiInstance.RedditListWikiPages(subreddit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditListWikiPages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditListWikiPagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List wiki pages
    ApiResponse<Object> response = apiInstance.RedditListWikiPagesWithHttpInfo(subreddit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditListWikiPagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **subreddit** | **string** |  |  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditnewsubreddits"></a>
# **RedditNewSubreddits**
> Object RedditNewSubreddits (int? limit = null, string after = null)

New subreddits

Get recently created subreddits.

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
    public class RedditNewSubredditsExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string |  (optional) 

            try
            {
                // New subreddits
                Object result = apiInstance.RedditNewSubreddits(limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditNewSubreddits: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditNewSubredditsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // New subreddits
    ApiResponse<Object> response = apiInstance.RedditNewSubredditsWithHttpInfo(limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditNewSubredditsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string** |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditpopularsubreddits"></a>
# **RedditPopularSubreddits**
> Object RedditPopularSubreddits (int? limit = null, string after = null)

Popular subreddits

Get popular subreddits by subscriber count.

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
    public class RedditPopularSubredditsExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string |  (optional) 

            try
            {
                // Popular subreddits
                Object result = apiInstance.RedditPopularSubreddits(limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditPopularSubreddits: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditPopularSubredditsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Popular subreddits
    ApiResponse<Object> response = apiInstance.RedditPopularSubredditsWithHttpInfo(limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditPopularSubredditsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string** |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditredditscraperhealthcheck"></a>
# **RedditRedditScraperHealthCheck**
> Object RedditRedditScraperHealthCheck ()

Reddit scraper health check

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
    public class RedditRedditScraperHealthCheckExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);

            try
            {
                // Reddit scraper health check
                Object result = apiInstance.RedditRedditScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditRedditScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditRedditScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reddit scraper health check
    ApiResponse<Object> response = apiInstance.RedditRedditScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditRedditScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="redditredditscraperhealthcheckhead"></a>
# **RedditRedditScraperHealthCheckHead**
> Object RedditRedditScraperHealthCheckHead ()

Reddit scraper health check

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
    public class RedditRedditScraperHealthCheckHeadExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);

            try
            {
                // Reddit scraper health check
                Object result = apiInstance.RedditRedditScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditRedditScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditRedditScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reddit scraper health check
    ApiResponse<Object> response = apiInstance.RedditRedditScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditRedditScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="redditsearchredditposts"></a>
# **RedditSearchRedditPosts**
> Object RedditSearchRedditPosts (string q, string subreddit = null, string sort = null, string t = null, int? limit = null, string after = null)

Search Reddit posts

Search Reddit posts globally or within a subreddit.

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
    public class RedditSearchRedditPostsExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search query
            var subreddit = "subreddit_example";  // string | Restrict to subreddit (optional) 
            var sort = "\"relevance\"";  // string | Sort: relevance, hot, top, new, comments (optional)  (default to "relevance")
            var t = "\"all\"";  // string | Time: hour, day, week, month, year, all (optional)  (default to "all")
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string |  (optional) 

            try
            {
                // Search Reddit posts
                Object result = apiInstance.RedditSearchRedditPosts(q, subreddit, sort, t, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditSearchRedditPosts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditSearchRedditPostsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Reddit posts
    ApiResponse<Object> response = apiInstance.RedditSearchRedditPostsWithHttpInfo(q, subreddit, sort, t, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditSearchRedditPostsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search query |  |
| **subreddit** | **string** | Restrict to subreddit | [optional]  |
| **sort** | **string** | Sort: relevance, hot, top, new, comments | [optional] [default to &quot;relevance&quot;] |
| **t** | **string** | Time: hour, day, week, month, year, all | [optional] [default to &quot;all&quot;] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string** |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditsearchsubreddits"></a>
# **RedditSearchSubreddits**
> Object RedditSearchSubreddits (string q, int? limit = null, string after = null)

Search subreddits

Search for subreddits by keyword.

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
    public class RedditSearchSubredditsExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search query
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string |  (optional) 

            try
            {
                // Search subreddits
                Object result = apiInstance.RedditSearchSubreddits(q, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditSearchSubreddits: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditSearchSubredditsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search subreddits
    ApiResponse<Object> response = apiInstance.RedditSearchSubredditsWithHttpInfo(q, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditSearchSubredditsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search query |  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string** |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="redditsearchusers"></a>
# **RedditSearchUsers**
> Object RedditSearchUsers (string q, int? limit = null, string after = null)

Search users

Search for Reddit users.

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
    public class RedditSearchUsersExample
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
            var apiInstance = new RedditApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search query
            var limit = 25;  // int? |  (optional)  (default to 25)
            var after = "after_example";  // string |  (optional) 

            try
            {
                // Search users
                Object result = apiInstance.RedditSearchUsers(q, limit, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedditApi.RedditSearchUsers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedditSearchUsersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search users
    ApiResponse<Object> response = apiInstance.RedditSearchUsersWithHttpInfo(q, limit, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedditApi.RedditSearchUsersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search query |  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **after** | **string** |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

