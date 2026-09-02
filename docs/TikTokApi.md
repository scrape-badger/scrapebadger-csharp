# ScrapeBadger.Api.TikTokApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**TiktokGeneralSearch**](TikTokApi.md#tiktokgeneralsearch) | **GET** /v1/tiktok/search | General search |
| [**TiktokGetCommentReplies**](TikTokApi.md#tiktokgetcommentreplies) | **GET** /v1/tiktok/comments/{comment_id}/replies | Get comment replies |
| [**TiktokGetComments**](TikTokApi.md#tiktokgetcomments) | **GET** /v1/tiktok/videos/{video_id}/comments | Get comments |
| [**TiktokGetFollowersDeprecated**](TikTokApi.md#tiktokgetfollowersdeprecated) | **GET** /v1/tiktok/users/{username}/followers | Get followers (deprecated) |
| [**TiktokGetFollowingDeprecated**](TikTokApi.md#tiktokgetfollowingdeprecated) | **GET** /v1/tiktok/users/{username}/following | Get following (deprecated) |
| [**TiktokGetHashtagDetail**](TikTokApi.md#tiktokgethashtagdetail) | **GET** /v1/tiktok/hashtags/{name} | Get hashtag detail |
| [**TiktokGetHashtagVideos**](TikTokApi.md#tiktokgethashtagvideos) | **GET** /v1/tiktok/hashtags/{name}/videos | Get hashtag videos |
| [**TiktokGetLikedVideosDeprecated**](TikTokApi.md#tiktokgetlikedvideosdeprecated) | **GET** /v1/tiktok/users/{username}/liked | Get liked videos (deprecated) |
| [**TiktokGetMusicSoundDetail**](TikTokApi.md#tiktokgetmusicsounddetail) | **GET** /v1/tiktok/music/{music_id} | Get music/sound detail |
| [**TiktokGetMusicVideos**](TikTokApi.md#tiktokgetmusicvideos) | **GET** /v1/tiktok/music/{music_id}/videos | Get music videos |
| [**TiktokGetOembedMetadata**](TikTokApi.md#tiktokgetoembedmetadata) | **GET** /v1/tiktok/oembed | Get oEmbed metadata |
| [**TiktokGetRelatedVideos**](TikTokApi.md#tiktokgetrelatedvideos) | **GET** /v1/tiktok/videos/{video_id}/related | Get related videos |
| [**TiktokGetReposts**](TikTokApi.md#tiktokgetreposts) | **GET** /v1/tiktok/users/{username}/reposts | Get reposts |
| [**TiktokGetTiktokAdDetail**](TikTokApi.md#tiktokgettiktokaddetail) | **GET** /v1/tiktok/ads/{ad_id} | Get TikTok ad detail |
| [**TiktokGetTranscript**](TikTokApi.md#tiktokgettranscript) | **GET** /v1/tiktok/videos/{video_id}/transcript | Get transcript |
| [**TiktokGetUserProfile**](TikTokApi.md#tiktokgetuserprofile) | **GET** /v1/tiktok/users/{username} | Get user profile |
| [**TiktokGetUserVideos**](TikTokApi.md#tiktokgetuservideos) | **GET** /v1/tiktok/users/{username}/videos | Get user videos |
| [**TiktokGetVideoDetail**](TikTokApi.md#tiktokgetvideodetail) | **GET** /v1/tiktok/videos/{video_id} | Get video detail |
| [**TiktokHealthCheck**](TikTokApi.md#tiktokhealthcheck) | **GET** /v1/tiktok/health | Health check |
| [**TiktokHealthCheckHead**](TikTokApi.md#tiktokhealthcheckhead) | **HEAD** /v1/tiktok/health | Health check |
| [**TiktokListRegions**](TikTokApi.md#tiktoklistregions) | **GET** /v1/tiktok/regions | List regions |
| [**TiktokSearchHashtags**](TikTokApi.md#tiktoksearchhashtags) | **GET** /v1/tiktok/search/hashtags | Search hashtags |
| [**TiktokSearchTheTiktokAdLibrary**](TikTokApi.md#tiktoksearchthetiktokadlibrary) | **GET** /v1/tiktok/ads/search | Search the TikTok Ad Library |
| [**TiktokSearchTiktokAdvertisers**](TikTokApi.md#tiktoksearchtiktokadvertisers) | **GET** /v1/tiktok/ads/advertisers | Search TikTok advertisers |
| [**TiktokSearchTiktokShopProducts**](TikTokApi.md#tiktoksearchtiktokshopproducts) | **GET** /v1/tiktok/shop/search | Search TikTok Shop products |
| [**TiktokSearchUsers**](TikTokApi.md#tiktoksearchusers) | **GET** /v1/tiktok/search/users | Search users |
| [**TiktokSearchVideos**](TikTokApi.md#tiktoksearchvideos) | **GET** /v1/tiktok/search/videos | Search videos |
| [**TiktokTiktokShopBestSellers**](TikTokApi.md#tiktoktiktokshopbestsellers) | **GET** /v1/tiktok/shop/ranking | TikTok Shop best sellers |
| [**TiktokTiktokShopCategorySubcategoriesTopProducts**](TikTokApi.md#tiktoktiktokshopcategorysubcategoriestopproducts) | **GET** /v1/tiktok/shop/categories/{category_id} | TikTok Shop category: subcategories + top products |
| [**TiktokTiktokShopDealsFeed**](TikTokApi.md#tiktoktiktokshopdealsfeed) | **GET** /v1/tiktok/shop/deals/{deal} | TikTok Shop deals feed |
| [**TiktokTiktokShopProductDetail**](TikTokApi.md#tiktoktiktokshopproductdetail) | **GET** /v1/tiktok/shop/products/{product_id} | TikTok Shop product detail |
| [**TiktokTiktokShopProductReviews**](TikTokApi.md#tiktoktiktokshopproductreviews) | **GET** /v1/tiktok/shop/products/{product_id}/reviews | TikTok Shop product reviews |
| [**TiktokTiktokShopRootCategories**](TikTokApi.md#tiktoktiktokshoprootcategories) | **GET** /v1/tiktok/shop/categories | TikTok Shop root categories |
| [**TiktokTiktokShopStoreProducts**](TikTokApi.md#tiktoktiktokshopstoreproducts) | **GET** /v1/tiktok/shop/stores/{seller_id} | TikTok Shop store + products |
| [**TiktokTrendingHashtags**](TikTokApi.md#tiktoktrendinghashtags) | **GET** /v1/tiktok/trending/hashtags | Trending hashtags |
| [**TiktokTrendingSongs**](TikTokApi.md#tiktoktrendingsongs) | **GET** /v1/tiktok/trending/songs | Trending songs |
| [**TiktokTrendingVideos**](TikTokApi.md#tiktoktrendingvideos) | **GET** /v1/tiktok/trending/videos | Trending videos |

<a id="tiktokgeneralsearch"></a>
# **TiktokGeneralSearch**
> Object TiktokGeneralSearch (string query, string region = null, int? count = null, string cursor = null)

General search

General TikTok search — video results from the Top feed.

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
    public class TiktokGeneralSearchExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keyword
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor (optional) 

            try
            {
                // General search
                Object result = apiInstance.TiktokGeneralSearch(query, region, count, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGeneralSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGeneralSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // General search
    ApiResponse<Object> response = apiInstance.TiktokGeneralSearchWithHttpInfo(query, region, count, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGeneralSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keyword |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string** | Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional]  |

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

<a id="tiktokgetcommentreplies"></a>
# **TiktokGetCommentReplies**
> Object TiktokGetCommentReplies (string commentId, string videoId, string region = null, int? count = null, string cursor = null)

Get comment replies

Get replies to a TikTok comment (best-effort).

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
    public class TiktokGetCommentRepliesExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var commentId = "commentId_example";  // string | 
            var videoId = "videoId_example";  // string | Parent video id
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string | Pagination cursor from a prior page's pagination.cursor (optional) 

            try
            {
                // Get comment replies
                Object result = apiInstance.TiktokGetCommentReplies(commentId, videoId, region, count, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetCommentReplies: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetCommentRepliesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get comment replies
    ApiResponse<Object> response = apiInstance.TiktokGetCommentRepliesWithHttpInfo(commentId, videoId, region, count, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetCommentRepliesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **commentId** | **string** |  |  |
| **videoId** | **string** | Parent video id |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string** | Pagination cursor from a prior page&#39;s pagination.cursor | [optional]  |

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

<a id="tiktokgetcomments"></a>
# **TiktokGetComments**
> Object TiktokGetComments (string videoId, string region = null, int? count = null, string cursor = null)

Get comments

Get top-level comments on a TikTok video.

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
    public class TiktokGetCommentsExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var videoId = "videoId_example";  // string | 
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string | Pagination cursor from a prior page's pagination.cursor (optional) 

            try
            {
                // Get comments
                Object result = apiInstance.TiktokGetComments(videoId, region, count, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetComments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetCommentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get comments
    ApiResponse<Object> response = apiInstance.TiktokGetCommentsWithHttpInfo(videoId, region, count, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetCommentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **videoId** | **string** |  |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string** | Pagination cursor from a prior page&#39;s pagination.cursor | [optional]  |

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

<a id="tiktokgetfollowersdeprecated"></a>
# **TiktokGetFollowersDeprecated**
> Object TiktokGetFollowersDeprecated (string username, string region = null, int? count = null)

Get followers (deprecated)

DEPRECATED — TikTok followers require an authenticated account session. Returns HTTP 410.

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
    public class TiktokGetFollowersDeprecatedExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 30;  // int? |  (optional)  (default to 30)

            try
            {
                // Get followers (deprecated)
                Object result = apiInstance.TiktokGetFollowersDeprecated(username, region, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetFollowersDeprecated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetFollowersDeprecatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get followers (deprecated)
    ApiResponse<Object> response = apiInstance.TiktokGetFollowersDeprecatedWithHttpInfo(username, region, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetFollowersDeprecatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 30] |

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

<a id="tiktokgetfollowingdeprecated"></a>
# **TiktokGetFollowingDeprecated**
> Object TiktokGetFollowingDeprecated (string username, string region = null, int? count = null)

Get following (deprecated)

DEPRECATED — TikTok following requires an authenticated account session. Returns HTTP 410.

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
    public class TiktokGetFollowingDeprecatedExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 30;  // int? |  (optional)  (default to 30)

            try
            {
                // Get following (deprecated)
                Object result = apiInstance.TiktokGetFollowingDeprecated(username, region, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetFollowingDeprecated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetFollowingDeprecatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get following (deprecated)
    ApiResponse<Object> response = apiInstance.TiktokGetFollowingDeprecatedWithHttpInfo(username, region, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetFollowingDeprecatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 30] |

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

<a id="tiktokgethashtagdetail"></a>
# **TiktokGetHashtagDetail**
> Object TiktokGetHashtagDetail (string name, string region = null)

Get hashtag detail

Get TikTok hashtag/challenge detail.

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
    public class TiktokGetHashtagDetailExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var name = "name_example";  // string | 
            var region = "\"US\"";  // string |  (optional)  (default to "US")

            try
            {
                // Get hashtag detail
                Object result = apiInstance.TiktokGetHashtagDetail(name, region);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetHashtagDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetHashtagDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get hashtag detail
    ApiResponse<Object> response = apiInstance.TiktokGetHashtagDetailWithHttpInfo(name, region);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetHashtagDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **name** | **string** |  |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |

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

<a id="tiktokgethashtagvideos"></a>
# **TiktokGetHashtagVideos**
> Object TiktokGetHashtagVideos (string name, string region = null, int? count = null, string cursor = null)

Get hashtag videos

Get videos tagged with a TikTok hashtag.

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
    public class TiktokGetHashtagVideosExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var name = "name_example";  // string | 
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 30;  // int? |  (optional)  (default to 30)
            var cursor = "cursor_example";  // string | Pagination cursor from a prior page's pagination.cursor (optional) 

            try
            {
                // Get hashtag videos
                Object result = apiInstance.TiktokGetHashtagVideos(name, region, count, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetHashtagVideos: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetHashtagVideosWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get hashtag videos
    ApiResponse<Object> response = apiInstance.TiktokGetHashtagVideosWithHttpInfo(name, region, count, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetHashtagVideosWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **name** | **string** |  |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 30] |
| **cursor** | **string** | Pagination cursor from a prior page&#39;s pagination.cursor | [optional]  |

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

<a id="tiktokgetlikedvideosdeprecated"></a>
# **TiktokGetLikedVideosDeprecated**
> Object TiktokGetLikedVideosDeprecated (string username, string region = null, int? count = null)

Get liked videos (deprecated)

DEPRECATED — TikTok liked videos require an authenticated account session. Returns HTTP 410.

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
    public class TiktokGetLikedVideosDeprecatedExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 30;  // int? |  (optional)  (default to 30)

            try
            {
                // Get liked videos (deprecated)
                Object result = apiInstance.TiktokGetLikedVideosDeprecated(username, region, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetLikedVideosDeprecated: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetLikedVideosDeprecatedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get liked videos (deprecated)
    ApiResponse<Object> response = apiInstance.TiktokGetLikedVideosDeprecatedWithHttpInfo(username, region, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetLikedVideosDeprecatedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 30] |

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

<a id="tiktokgetmusicsounddetail"></a>
# **TiktokGetMusicSoundDetail**
> Object TiktokGetMusicSoundDetail (string musicId, string region = null)

Get music/sound detail

Get TikTok sound/music detail.

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
    public class TiktokGetMusicSoundDetailExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var musicId = "musicId_example";  // string | 
            var region = "\"US\"";  // string |  (optional)  (default to "US")

            try
            {
                // Get music/sound detail
                Object result = apiInstance.TiktokGetMusicSoundDetail(musicId, region);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetMusicSoundDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetMusicSoundDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get music/sound detail
    ApiResponse<Object> response = apiInstance.TiktokGetMusicSoundDetailWithHttpInfo(musicId, region);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetMusicSoundDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **musicId** | **string** |  |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |

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

<a id="tiktokgetmusicvideos"></a>
# **TiktokGetMusicVideos**
> Object TiktokGetMusicVideos (string musicId, string region = null, int? count = null, string cursor = null)

Get music videos

Get videos using a given TikTok sound.

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
    public class TiktokGetMusicVideosExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var musicId = "musicId_example";  // string | 
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 30;  // int? |  (optional)  (default to 30)
            var cursor = "cursor_example";  // string | Pagination cursor from a prior page's pagination.cursor (optional) 

            try
            {
                // Get music videos
                Object result = apiInstance.TiktokGetMusicVideos(musicId, region, count, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetMusicVideos: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetMusicVideosWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get music videos
    ApiResponse<Object> response = apiInstance.TiktokGetMusicVideosWithHttpInfo(musicId, region, count, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetMusicVideosWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **musicId** | **string** |  |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 30] |
| **cursor** | **string** | Pagination cursor from a prior page&#39;s pagination.cursor | [optional]  |

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

<a id="tiktokgetoembedmetadata"></a>
# **TiktokGetOembedMetadata**
> Object TiktokGetOembedMetadata (string url, string region = null)

Get oEmbed metadata

Get cheap unauthenticated oEmbed metadata for a TikTok URL.

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
    public class TiktokGetOembedMetadataExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var url = "url_example";  // string | Full TikTok video or profile URL
            var region = "\"US\"";  // string |  (optional)  (default to "US")

            try
            {
                // Get oEmbed metadata
                Object result = apiInstance.TiktokGetOembedMetadata(url, region);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetOembedMetadata: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetOembedMetadataWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get oEmbed metadata
    ApiResponse<Object> response = apiInstance.TiktokGetOembedMetadataWithHttpInfo(url, region);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetOembedMetadataWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **url** | **string** | Full TikTok video or profile URL |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |

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

<a id="tiktokgetrelatedvideos"></a>
# **TiktokGetRelatedVideos**
> Object TiktokGetRelatedVideos (string videoId, string region = null, int? count = null)

Get related videos

Get TikTok's related videos for a given video.

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
    public class TiktokGetRelatedVideosExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var videoId = "videoId_example";  // string | 
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 16;  // int? |  (optional)  (default to 16)

            try
            {
                // Get related videos
                Object result = apiInstance.TiktokGetRelatedVideos(videoId, region, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetRelatedVideos: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetRelatedVideosWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get related videos
    ApiResponse<Object> response = apiInstance.TiktokGetRelatedVideosWithHttpInfo(videoId, region, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetRelatedVideosWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **videoId** | **string** |  |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 16] |

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

<a id="tiktokgetreposts"></a>
# **TiktokGetReposts**
> Object TiktokGetReposts (string username, string region = null, int? count = null)

Get reposts

Get videos a TikTok user has reposted.

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
    public class TiktokGetRepostsExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 30;  // int? |  (optional)  (default to 30)

            try
            {
                // Get reposts
                Object result = apiInstance.TiktokGetReposts(username, region, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetReposts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetRepostsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get reposts
    ApiResponse<Object> response = apiInstance.TiktokGetRepostsWithHttpInfo(username, region, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetRepostsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 30] |

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

<a id="tiktokgettiktokaddetail"></a>
# **TiktokGetTiktokAdDetail**
> Object TiktokGetTiktokAdDetail (string adId, string region = null)

Get TikTok ad detail

Get a single ad's advertiser, creatives, and targeting/impression breakdown.

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
    public class TiktokGetTiktokAdDetailExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var adId = "adId_example";  // string | 
            var region = "\"DE\"";  // string | EU region code (the Ad Library is EU-only) (optional)  (default to "DE")

            try
            {
                // Get TikTok ad detail
                Object result = apiInstance.TiktokGetTiktokAdDetail(adId, region);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetTiktokAdDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetTiktokAdDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get TikTok ad detail
    ApiResponse<Object> response = apiInstance.TiktokGetTiktokAdDetailWithHttpInfo(adId, region);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetTiktokAdDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **adId** | **string** |  |  |
| **region** | **string** | EU region code (the Ad Library is EU-only) | [optional] [default to &quot;DE&quot;] |

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

<a id="tiktokgettranscript"></a>
# **TiktokGetTranscript**
> Object TiktokGetTranscript (string videoId, string region = null)

Get transcript

Get subtitle/caption tracks for a TikTok video.

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
    public class TiktokGetTranscriptExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var videoId = "videoId_example";  // string | 
            var region = "\"US\"";  // string |  (optional)  (default to "US")

            try
            {
                // Get transcript
                Object result = apiInstance.TiktokGetTranscript(videoId, region);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetTranscript: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetTranscriptWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get transcript
    ApiResponse<Object> response = apiInstance.TiktokGetTranscriptWithHttpInfo(videoId, region);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetTranscriptWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **videoId** | **string** |  |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |

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

<a id="tiktokgetuserprofile"></a>
# **TiktokGetUserProfile**
> Object TiktokGetUserProfile (string username, string region = null)

Get user profile

Get a TikTok user's full profile.

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
    public class TiktokGetUserProfileExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var region = "\"US\"";  // string | Content region (ISO 3166-1 alpha-2) (optional)  (default to "US")

            try
            {
                // Get user profile
                Object result = apiInstance.TiktokGetUserProfile(username, region);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetUserProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetUserProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user profile
    ApiResponse<Object> response = apiInstance.TiktokGetUserProfileWithHttpInfo(username, region);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetUserProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **region** | **string** | Content region (ISO 3166-1 alpha-2) | [optional] [default to &quot;US&quot;] |

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

<a id="tiktokgetuservideos"></a>
# **TiktokGetUserVideos**
> Object TiktokGetUserVideos (string username, string region = null, int? count = null, string cursor = null)

Get user videos

Get a TikTok user's posted videos.

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
    public class TiktokGetUserVideosExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 30;  // int? |  (optional)  (default to 30)
            var cursor = "cursor_example";  // string | Pagination cursor from a prior page's `pagination.cursor` (signer path only). (optional) 

            try
            {
                // Get user videos
                Object result = apiInstance.TiktokGetUserVideos(username, region, count, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetUserVideos: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetUserVideosWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user videos
    ApiResponse<Object> response = apiInstance.TiktokGetUserVideosWithHttpInfo(username, region, count, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetUserVideosWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 30] |
| **cursor** | **string** | Pagination cursor from a prior page&#39;s &#x60;pagination.cursor&#x60; (signer path only). | [optional]  |

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

<a id="tiktokgetvideodetail"></a>
# **TiktokGetVideoDetail**
> Object TiktokGetVideoDetail (string videoId, string region = null, string username = null)

Get video detail

Get full metadata for a single TikTok video/post.

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
    public class TiktokGetVideoDetailExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var videoId = "videoId_example";  // string | 
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var username = "username_example";  // string | Author handle (skips oEmbed lookup) (optional) 

            try
            {
                // Get video detail
                Object result = apiInstance.TiktokGetVideoDetail(videoId, region, username);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokGetVideoDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokGetVideoDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get video detail
    ApiResponse<Object> response = apiInstance.TiktokGetVideoDetailWithHttpInfo(videoId, region, username);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokGetVideoDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **videoId** | **string** |  |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **username** | **string** | Author handle (skips oEmbed lookup) | [optional]  |

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

<a id="tiktokhealthcheck"></a>
# **TiktokHealthCheck**
> Object TiktokHealthCheck ()

Health check

Check health of the TikTok scraper service.

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
    public class TiktokHealthCheckExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);

            try
            {
                // Health check
                Object result = apiInstance.TiktokHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Health check
    ApiResponse<Object> response = apiInstance.TiktokHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokHealthCheckWithHttpInfo: " + e.Message);
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

<a id="tiktokhealthcheckhead"></a>
# **TiktokHealthCheckHead**
> Object TiktokHealthCheckHead ()

Health check

Check health of the TikTok scraper service.

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
    public class TiktokHealthCheckHeadExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);

            try
            {
                // Health check
                Object result = apiInstance.TiktokHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Health check
    ApiResponse<Object> response = apiInstance.TiktokHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="tiktoklistregions"></a>
# **TiktokListRegions**
> Object TiktokListRegions ()

List regions

List supported TikTok content regions.

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
    public class TiktokListRegionsExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);

            try
            {
                // List regions
                Object result = apiInstance.TiktokListRegions();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokListRegions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokListRegionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List regions
    ApiResponse<Object> response = apiInstance.TiktokListRegionsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokListRegionsWithHttpInfo: " + e.Message);
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

<a id="tiktoksearchhashtags"></a>
# **TiktokSearchHashtags**
> Object TiktokSearchHashtags (string query, string region = null, int? count = null, string cursor = null)

Search hashtags

Search TikTok hashtags by keyword.

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
    public class TiktokSearchHashtagsExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keyword
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor (optional) 

            try
            {
                // Search hashtags
                Object result = apiInstance.TiktokSearchHashtags(query, region, count, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokSearchHashtags: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokSearchHashtagsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search hashtags
    ApiResponse<Object> response = apiInstance.TiktokSearchHashtagsWithHttpInfo(query, region, count, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokSearchHashtagsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keyword |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string** | Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional]  |

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

<a id="tiktoksearchthetiktokadlibrary"></a>
# **TiktokSearchTheTiktokAdLibrary**
> Object TiktokSearchTheTiktokAdLibrary (string query = null, string advertiserId = null, string region = null, int? days = null, string sort = null, int? offset = null, string searchId = null, int? count = null)

Search the TikTok Ad Library

Search TikTok's Commercial Content Library (ad transparency) by keyword or advertiser.

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
    public class TiktokSearchTheTiktokAdLibraryExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var query = "\"\"";  // string | Keyword (ignored when advertiser_id is set) (optional)  (default to "")
            var advertiserId = "\"\"";  // string | Advertiser business id(s) for advertiser search (optional)  (default to "")
            var region = "\"DE\"";  // string | EU region code (the Ad Library is EU-only) (optional)  (default to "DE")
            var days = 30;  // int? |  (optional)  (default to 30)
            var sort = "\"last_shown_date,desc\"";  // string |  (optional)  (default to "last_shown_date,desc")
            var offset = 0;  // int? |  (optional)  (default to 0)
            var searchId = "\"\"";  // string |  (optional)  (default to "")
            var count = 20;  // int? |  (optional)  (default to 20)

            try
            {
                // Search the TikTok Ad Library
                Object result = apiInstance.TiktokSearchTheTiktokAdLibrary(query, advertiserId, region, days, sort, offset, searchId, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokSearchTheTiktokAdLibrary: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokSearchTheTiktokAdLibraryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search the TikTok Ad Library
    ApiResponse<Object> response = apiInstance.TiktokSearchTheTiktokAdLibraryWithHttpInfo(query, advertiserId, region, days, sort, offset, searchId, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokSearchTheTiktokAdLibraryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Keyword (ignored when advertiser_id is set) | [optional] [default to &quot;&quot;] |
| **advertiserId** | **string** | Advertiser business id(s) for advertiser search | [optional] [default to &quot;&quot;] |
| **region** | **string** | EU region code (the Ad Library is EU-only) | [optional] [default to &quot;DE&quot;] |
| **days** | **int?** |  | [optional] [default to 30] |
| **sort** | **string** |  | [optional] [default to &quot;last_shown_date,desc&quot;] |
| **offset** | **int?** |  | [optional] [default to 0] |
| **searchId** | **string** |  | [optional] [default to &quot;&quot;] |
| **count** | **int?** |  | [optional] [default to 20] |

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

<a id="tiktoksearchtiktokadvertisers"></a>
# **TiktokSearchTiktokAdvertisers**
> Object TiktokSearchTiktokAdvertisers (string query, string region = null, int? count = null)

Search TikTok advertisers

Look up TikTok advertiser business ids by name (feeds ads/search?advertiser_id=).

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
    public class TiktokSearchTiktokAdvertisersExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Advertiser name (or partial) to look up
            var region = "\"DE\"";  // string | EU region code (the Ad Library is EU-only) (optional)  (default to "DE")
            var count = 10;  // int? |  (optional)  (default to 10)

            try
            {
                // Search TikTok advertisers
                Object result = apiInstance.TiktokSearchTiktokAdvertisers(query, region, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokSearchTiktokAdvertisers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokSearchTiktokAdvertisersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search TikTok advertisers
    ApiResponse<Object> response = apiInstance.TiktokSearchTiktokAdvertisersWithHttpInfo(query, region, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokSearchTiktokAdvertisersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Advertiser name (or partial) to look up |  |
| **region** | **string** | EU region code (the Ad Library is EU-only) | [optional] [default to &quot;DE&quot;] |
| **count** | **int?** |  | [optional] [default to 10] |

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

<a id="tiktoksearchtiktokshopproducts"></a>
# **TiktokSearchTiktokShopProducts**
> Object TiktokSearchTiktokShopProducts (string q, string region = null, int? offset = null)

Search TikTok Shop products

Keyword search over TikTok Shop products: 30 per page with offset pagination (US); the first page also carries matching shops and related searches.

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
    public class TiktokSearchTiktokShopProductsExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Keyword, e.g. 'wireless earbuds'
            var region = "\"US\"";  // string | Market: US, GB, ID (optional)  (default to "US")
            var offset = 0;  // int? | Pass back next_offset for the next page (US) (optional)  (default to 0)

            try
            {
                // Search TikTok Shop products
                Object result = apiInstance.TiktokSearchTiktokShopProducts(q, region, offset);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokSearchTiktokShopProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokSearchTiktokShopProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search TikTok Shop products
    ApiResponse<Object> response = apiInstance.TiktokSearchTiktokShopProductsWithHttpInfo(q, region, offset);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokSearchTiktokShopProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Keyword, e.g. &#39;wireless earbuds&#39; |  |
| **region** | **string** | Market: US, GB, ID | [optional] [default to &quot;US&quot;] |
| **offset** | **int?** | Pass back next_offset for the next page (US) | [optional] [default to 0] |

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

<a id="tiktoksearchusers"></a>
# **TiktokSearchUsers**
> Object TiktokSearchUsers (string query, string region = null, int? count = null, string cursor = null)

Search users

Search TikTok users by keyword.

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
    public class TiktokSearchUsersExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keyword
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor (optional) 

            try
            {
                // Search users
                Object result = apiInstance.TiktokSearchUsers(query, region, count, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokSearchUsers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokSearchUsersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search users
    ApiResponse<Object> response = apiInstance.TiktokSearchUsersWithHttpInfo(query, region, count, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokSearchUsersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keyword |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string** | Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional]  |

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

<a id="tiktoksearchvideos"></a>
# **TiktokSearchVideos**
> Object TiktokSearchVideos (string query, string region = null, int? count = null, string cursor = null)

Search videos

Search TikTok videos by keyword.

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
    public class TiktokSearchVideosExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keyword
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 20;  // int? |  (optional)  (default to 20)
            var cursor = "cursor_example";  // string | Composite pagination cursor (offset.search_id) from a prior page's pagination.cursor (optional) 

            try
            {
                // Search videos
                Object result = apiInstance.TiktokSearchVideos(query, region, count, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokSearchVideos: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokSearchVideosWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search videos
    ApiResponse<Object> response = apiInstance.TiktokSearchVideosWithHttpInfo(query, region, count, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokSearchVideosWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keyword |  |
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 20] |
| **cursor** | **string** | Composite pagination cursor (offset.search_id) from a prior page&#39;s pagination.cursor | [optional]  |

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

<a id="tiktoktiktokshopbestsellers"></a>
# **TiktokTiktokShopBestSellers**
> Object TiktokTiktokShopBestSellers (string region = null, int? count = null)

TikTok Shop best sellers

TikTok Shop's own ranking of the best-selling products of the past 30 days (US only).

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
    public class TiktokTiktokShopBestSellersExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var region = "\"US\"";  // string | Market: US, GB, ID (optional)  (default to "US")
            var count = 20;  // int? | Max products to return (optional)  (default to 20)

            try
            {
                // TikTok Shop best sellers
                Object result = apiInstance.TiktokTiktokShopBestSellers(region, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopBestSellers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokTiktokShopBestSellersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // TikTok Shop best sellers
    ApiResponse<Object> response = apiInstance.TiktokTiktokShopBestSellersWithHttpInfo(region, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopBestSellersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **region** | **string** | Market: US, GB, ID | [optional] [default to &quot;US&quot;] |
| **count** | **int?** | Max products to return | [optional] [default to 20] |

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

<a id="tiktoktiktokshopcategorysubcategoriestopproducts"></a>
# **TiktokTiktokShopCategorySubcategoriesTopProducts**
> Object TiktokTiktokShopCategorySubcategoriesTopProducts (string categoryId, string region = null)

TikTok Shop category: subcategories + top products

A category's subcategories and its top products as TikTok Shop ranks them.

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
    public class TiktokTiktokShopCategorySubcategoriesTopProductsExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var categoryId = "categoryId_example";  // string | 
            var region = "\"US\"";  // string | Market: US, GB, ID (optional)  (default to "US")

            try
            {
                // TikTok Shop category: subcategories + top products
                Object result = apiInstance.TiktokTiktokShopCategorySubcategoriesTopProducts(categoryId, region);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopCategorySubcategoriesTopProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokTiktokShopCategorySubcategoriesTopProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // TikTok Shop category: subcategories + top products
    ApiResponse<Object> response = apiInstance.TiktokTiktokShopCategorySubcategoriesTopProductsWithHttpInfo(categoryId, region);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopCategorySubcategoriesTopProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **categoryId** | **string** |  |  |
| **region** | **string** | Market: US, GB, ID | [optional] [default to &quot;US&quot;] |

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

<a id="tiktoktiktokshopdealsfeed"></a>
# **TiktokTiktokShopDealsFeed**
> Object TiktokTiktokShopDealsFeed (string deal, string region = null)

TikTok Shop deals feed

A curated storefront feed: recommended-for-you, or premium-offers (US only).

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
    public class TiktokTiktokShopDealsFeedExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var deal = "deal_example";  // string | 
            var region = "\"US\"";  // string | Market: US, GB, ID (optional)  (default to "US")

            try
            {
                // TikTok Shop deals feed
                Object result = apiInstance.TiktokTiktokShopDealsFeed(deal, region);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopDealsFeed: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokTiktokShopDealsFeedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // TikTok Shop deals feed
    ApiResponse<Object> response = apiInstance.TiktokTiktokShopDealsFeedWithHttpInfo(deal, region);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopDealsFeedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deal** | **string** |  |  |
| **region** | **string** | Market: US, GB, ID | [optional] [default to &quot;US&quot;] |

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

<a id="tiktoktiktokshopproductdetail"></a>
# **TiktokTiktokShopProductDetail**
> Object TiktokTiktokShopProductDetail (string productId, string region = null)

TikTok Shop product detail

Full TikTok Shop product page: description, images, price, SKUs with stock, first reviews, shop and TikTok's AI summary.

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
    public class TiktokTiktokShopProductDetailExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | 
            var region = "\"US\"";  // string | Market: US, GB, ID (optional)  (default to "US")

            try
            {
                // TikTok Shop product detail
                Object result = apiInstance.TiktokTiktokShopProductDetail(productId, region);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopProductDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokTiktokShopProductDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // TikTok Shop product detail
    ApiResponse<Object> response = apiInstance.TiktokTiktokShopProductDetailWithHttpInfo(productId, region);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopProductDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** |  |  |
| **region** | **string** | Market: US, GB, ID | [optional] [default to &quot;US&quot;] |

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

<a id="tiktoktiktokshopproductreviews"></a>
# **TiktokTiktokShopProductReviews**
> Object TiktokTiktokShopProductReviews (string productId, string region = null, int? page = null, int? count = null, string sort = null, int? rating = null, bool? withMedia = null, bool? verified = null)

TikTok Shop product reviews

Paginated product reviews with the rating breakdown (US).

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
    public class TiktokTiktokShopProductReviewsExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | 
            var region = "\"US\"";  // string | Market: US, GB, ID (optional)  (default to "US")
            var page = 1;  // int? |  (optional)  (default to 1)
            var count = 20;  // int? |  (optional)  (default to 20)
            var sort = "\"recommended\"";  // string | recommended | recent (optional)  (default to "recommended")
            var rating = 56;  // int? | Only this star rating (optional) 
            var withMedia = false;  // bool? | Only reviews with photos/videos (optional)  (default to false)
            var verified = false;  // bool? | Only verified purchases (optional)  (default to false)

            try
            {
                // TikTok Shop product reviews
                Object result = apiInstance.TiktokTiktokShopProductReviews(productId, region, page, count, sort, rating, withMedia, verified);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopProductReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokTiktokShopProductReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // TikTok Shop product reviews
    ApiResponse<Object> response = apiInstance.TiktokTiktokShopProductReviewsWithHttpInfo(productId, region, page, count, sort, rating, withMedia, verified);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopProductReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** |  |  |
| **region** | **string** | Market: US, GB, ID | [optional] [default to &quot;US&quot;] |
| **page** | **int?** |  | [optional] [default to 1] |
| **count** | **int?** |  | [optional] [default to 20] |
| **sort** | **string** | recommended | recent | [optional] [default to &quot;recommended&quot;] |
| **rating** | **int?** | Only this star rating | [optional]  |
| **withMedia** | **bool?** | Only reviews with photos/videos | [optional] [default to false] |
| **verified** | **bool?** | Only verified purchases | [optional] [default to false] |

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

<a id="tiktoktiktokshoprootcategories"></a>
# **TiktokTiktokShopRootCategories**
> Object TiktokTiktokShopRootCategories (string region = null)

TikTok Shop root categories

Top-level TikTok Shop categories of a market. Drill down with /shop/categories/{id}.

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
    public class TiktokTiktokShopRootCategoriesExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var region = "\"US\"";  // string | Market: US, GB, ID (optional)  (default to "US")

            try
            {
                // TikTok Shop root categories
                Object result = apiInstance.TiktokTiktokShopRootCategories(region);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopRootCategories: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokTiktokShopRootCategoriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // TikTok Shop root categories
    ApiResponse<Object> response = apiInstance.TiktokTiktokShopRootCategoriesWithHttpInfo(region);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopRootCategoriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **region** | **string** | Market: US, GB, ID | [optional] [default to &quot;US&quot;] |

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

<a id="tiktoktiktokshopstoreproducts"></a>
# **TiktokTiktokShopStoreProducts**
> Object TiktokTiktokShopStoreProducts (string sellerId, string region = null, string cursor = null, int? count = null)

TikTok Shop store + products

A store's stats and its cursor-paginated product catalogue (US).

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
    public class TiktokTiktokShopStoreProductsExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var sellerId = "sellerId_example";  // string | 
            var region = "\"US\"";  // string | Market: US, GB, ID (optional)  (default to "US")
            var cursor = "\"\"";  // string | Pass back next_cursor for the next page (optional)  (default to "")
            var count = 20;  // int? |  (optional)  (default to 20)

            try
            {
                // TikTok Shop store + products
                Object result = apiInstance.TiktokTiktokShopStoreProducts(sellerId, region, cursor, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopStoreProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokTiktokShopStoreProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // TikTok Shop store + products
    ApiResponse<Object> response = apiInstance.TiktokTiktokShopStoreProductsWithHttpInfo(sellerId, region, cursor, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokTiktokShopStoreProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sellerId** | **string** |  |  |
| **region** | **string** | Market: US, GB, ID | [optional] [default to &quot;US&quot;] |
| **cursor** | **string** | Pass back next_cursor for the next page | [optional] [default to &quot;&quot;] |
| **count** | **int?** |  | [optional] [default to 20] |

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

<a id="tiktoktrendinghashtags"></a>
# **TiktokTrendingHashtags**
> Object TiktokTrendingHashtags (string region = null, int? period = null, int? count = null)

Trending hashtags

Get trending hashtags (mobile Discover surface — view_count + creators).

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
    public class TiktokTrendingHashtagsExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var period = 7;  // int? |  (optional)  (default to 7)
            var count = 20;  // int? |  (optional)  (default to 20)

            try
            {
                // Trending hashtags
                Object result = apiInstance.TiktokTrendingHashtags(region, period, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokTrendingHashtags: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokTrendingHashtagsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Trending hashtags
    ApiResponse<Object> response = apiInstance.TiktokTrendingHashtagsWithHttpInfo(region, period, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokTrendingHashtagsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **period** | **int?** |  | [optional] [default to 7] |
| **count** | **int?** |  | [optional] [default to 20] |

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

<a id="tiktoktrendingsongs"></a>
# **TiktokTrendingSongs**
> Object TiktokTrendingSongs (string region = null, int? period = null, int? count = null)

Trending songs

Get trending songs/sounds (mobile hot-music feed — ranked by usage).

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
    public class TiktokTrendingSongsExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var period = 7;  // int? |  (optional)  (default to 7)
            var count = 20;  // int? |  (optional)  (default to 20)

            try
            {
                // Trending songs
                Object result = apiInstance.TiktokTrendingSongs(region, period, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokTrendingSongs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokTrendingSongsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Trending songs
    ApiResponse<Object> response = apiInstance.TiktokTrendingSongsWithHttpInfo(region, period, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokTrendingSongsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **period** | **int?** |  | [optional] [default to 7] |
| **count** | **int?** |  | [optional] [default to 20] |

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

<a id="tiktoktrendingvideos"></a>
# **TiktokTrendingVideos**
> Object TiktokTrendingVideos (string region = null, int? count = null)

Trending videos

Get trending videos from the TikTok Explore feed.

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
    public class TiktokTrendingVideosExample
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
            var apiInstance = new TikTokApi(httpClient, config, httpClientHandler);
            var region = "\"US\"";  // string |  (optional)  (default to "US")
            var count = 20;  // int? |  (optional)  (default to 20)

            try
            {
                // Trending videos
                Object result = apiInstance.TiktokTrendingVideos(region, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TikTokApi.TiktokTrendingVideos: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TiktokTrendingVideosWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Trending videos
    ApiResponse<Object> response = apiInstance.TiktokTrendingVideosWithHttpInfo(region, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TikTokApi.TiktokTrendingVideosWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **region** | **string** |  | [optional] [default to &quot;US&quot;] |
| **count** | **int?** |  | [optional] [default to 20] |

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

