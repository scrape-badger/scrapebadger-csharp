# ScrapeBadger.Api.TwitterApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**TwitterAdvancedTweetSearch**](TwitterApi.md#twitteradvancedtweetsearch) | **GET** /v1/twitter/tweets/advanced_search | Advanced tweet search |
| [**TwitterBatchGetUsersByIds**](TwitterApi.md#twitterbatchgetusersbyids) | **GET** /v1/twitter/users/batch_by_ids | Batch get users by IDs |
| [**TwitterBatchGetUsersByUsernames**](TwitterApi.md#twitterbatchgetusersbyusernames) | **GET** /v1/twitter/users/batch_by_usernames | Batch get users by usernames |
| [**TwitterConfigureWebhookOnAMonitor**](TwitterApi.md#twitterconfigurewebhookonamonitor) | **POST** /v1/twitter/stream/webhooks | Configure webhook on a monitor |
| [**TwitterCreateFilterRule**](TwitterApi.md#twittercreatefilterrule) | **POST** /v1/twitter/stream/filter-rules | Create filter rule |
| [**TwitterCreateStreamMonitor**](TwitterApi.md#twittercreatestreammonitor) | **POST** /v1/twitter/stream/monitors | Create stream monitor |
| [**TwitterDeleteFilterRule**](TwitterApi.md#twitterdeletefilterrule) | **DELETE** /v1/twitter/stream/filter-rules/{rule_id} | Delete filter rule |
| [**TwitterDeleteStreamMonitor**](TwitterApi.md#twitterdeletestreammonitor) | **DELETE** /v1/twitter/stream/monitors/{monitor_id} | Delete stream monitor |
| [**TwitterGetArticleById**](TwitterApi.md#twittergetarticlebyid) | **GET** /v1/twitter/tweets/article/{article_id} | Get article by ID |
| [**TwitterGetBroadcastDetails**](TwitterApi.md#twittergetbroadcastdetails) | **GET** /v1/twitter/spaces/broadcast/{broadcast_id} | Get broadcast details |
| [**TwitterGetCommunityDetails**](TwitterApi.md#twittergetcommunitydetails) | **GET** /v1/twitter/communities/{community_id} | Get community details |
| [**TwitterGetCommunityNotes**](TwitterApi.md#twittergetcommunitynotes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/community_notes | Get community notes |
| [**TwitterGetCommunityTweets**](TwitterApi.md#twittergetcommunitytweets) | **GET** /v1/twitter/communities/{community_id}/tweets | Get community tweets |
| [**TwitterGetFilterRule**](TwitterApi.md#twittergetfilterrule) | **GET** /v1/twitter/stream/filter-rules/{rule_id} | Get filter rule |
| [**TwitterGetFilterRulePerPollRates**](TwitterApi.md#twittergetfilterruleperpollrates) | **GET** /v1/twitter/stream/filter-rules-pricing | Get filter rule per-poll rates |
| [**TwitterGetListDetails**](TwitterApi.md#twittergetlistdetails) | **GET** /v1/twitter/lists/{list_id}/detail | Get list details |
| [**TwitterGetListTweets**](TwitterApi.md#twittergetlisttweets) | **GET** /v1/twitter/lists/{list_id}/tweets | Get list tweets |
| [**TwitterGetPlaceDetails**](TwitterApi.md#twittergetplacedetails) | **GET** /v1/twitter/geo/places/{place_id} | Get place details |
| [**TwitterGetSimilarTweets**](TwitterApi.md#twittergetsimilartweets) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/similar | Get similar tweets |
| [**TwitterGetSpaceDetails**](TwitterApi.md#twittergetspacedetails) | **GET** /v1/twitter/spaces/{space_id} | Get Space details |
| [**TwitterGetStreamMonitor**](TwitterApi.md#twittergetstreammonitor) | **GET** /v1/twitter/stream/monitors/{monitor_id} | Get stream monitor |
| [**TwitterGetTrendingTopics**](TwitterApi.md#twittergettrendingtopics) | **GET** /v1/twitter/trends/ | Get trending topics |
| [**TwitterGetTrendsByLocation**](TwitterApi.md#twittergettrendsbylocation) | **GET** /v1/twitter/trends/place/{woeid} | Get trends by location |
| [**TwitterGetTweetDetails**](TwitterApi.md#twittergettweetdetails) | **GET** /v1/twitter/tweets/tweet/{tweet_id} | Get tweet details |
| [**TwitterGetTweetEditHistory**](TwitterApi.md#twittergettweetedithistory) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/edit_history | Get tweet edit history |
| [**TwitterGetTweetFavoriters**](TwitterApi.md#twittergettweetfavoriters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/favoriters | Get tweet favoriters |
| [**TwitterGetTweetQuotes**](TwitterApi.md#twittergettweetquotes) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/quotes | Get tweet quotes |
| [**TwitterGetTweetReplies**](TwitterApi.md#twittergettweetreplies) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/replies | Get tweet replies |
| [**TwitterGetTweetRetweeters**](TwitterApi.md#twittergettweetretweeters) | **GET** /v1/twitter/tweets/tweet/{tweet_id}/retweeters | Get tweet retweeters |
| [**TwitterGetTweetsByIds**](TwitterApi.md#twittergettweetsbyids) | **GET** /v1/twitter/tweets/ | Get tweets by IDs |
| [**TwitterGetUserArticles**](TwitterApi.md#twittergetuserarticles) | **GET** /v1/twitter/users/{user_id}/articles | Get user articles |
| [**TwitterGetUserById**](TwitterApi.md#twittergetuserbyid) | **GET** /v1/twitter/users/{user_id}/by_id | Get user by ID |
| [**TwitterGetUserByUsername**](TwitterApi.md#twittergetuserbyusername) | **GET** /v1/twitter/users/{username}/by_username | Get user by username |
| [**TwitterGetUserFollowers**](TwitterApi.md#twittergetuserfollowers) | **GET** /v1/twitter/users/{username}/followers | Get user followers |
| [**TwitterGetUserFollowing**](TwitterApi.md#twittergetuserfollowing) | **GET** /v1/twitter/users/{username}/followings | Get user following |
| [**TwitterGetUserMentions**](TwitterApi.md#twittergetusermentions) | **GET** /v1/twitter/users/{username}/mentions | Get user mentions |
| [**TwitterGetUserSubscriptions**](TwitterApi.md#twittergetusersubscriptions) | **GET** /v1/twitter/users/{user_id}/subscriptions | Get user subscriptions |
| [**TwitterGetUserTweets**](TwitterApi.md#twittergetusertweets) | **GET** /v1/twitter/users/{username}/latest_tweets | Get user tweets |
| [**TwitterListBillingLogs**](TwitterApi.md#twitterlistbillinglogs) | **GET** /v1/twitter/stream/billing-logs | List billing logs |
| [**TwitterListDeliveryLogsForAFilterRule**](TwitterApi.md#twitterlistdeliverylogsforafilterrule) | **GET** /v1/twitter/stream/filter-rules/{rule_id}/logs | List delivery logs for a filter rule |
| [**TwitterListFilterRules**](TwitterApi.md#twitterlistfilterrules) | **GET** /v1/twitter/stream/filter-rules | List filter rules |
| [**TwitterListStreamMonitors**](TwitterApi.md#twitterliststreammonitors) | **GET** /v1/twitter/stream/monitors | List stream monitors |
| [**TwitterListTweetDeliveryLogs**](TwitterApi.md#twitterlisttweetdeliverylogs) | **GET** /v1/twitter/stream/logs | List tweet delivery logs |
| [**TwitterListWebhooks**](TwitterApi.md#twitterlistwebhooks) | **GET** /v1/twitter/stream/webhooks | List webhooks |
| [**TwitterRemoveWebhookFromMonitor**](TwitterApi.md#twitterremovewebhookfrommonitor) | **DELETE** /v1/twitter/stream/webhooks/{webhook_id} | Remove webhook from monitor |
| [**TwitterSearchCommunities**](TwitterApi.md#twittersearchcommunities) | **GET** /v1/twitter/communities/search | Search communities |
| [**TwitterSearchListTweets**](TwitterApi.md#twittersearchlisttweets) | **GET** /v1/twitter/lists/{list_id}/search_tweets | Search list tweets |
| [**TwitterSearchPlaces**](TwitterApi.md#twittersearchplaces) | **GET** /v1/twitter/geo/search | Search places |
| [**TwitterSearchUsers**](TwitterApi.md#twittersearchusers) | **GET** /v1/twitter/users/search_users | Search users |
| [**TwitterTestWebhookDelivery**](TwitterApi.md#twittertestwebhookdelivery) | **POST** /v1/twitter/stream/webhooks/test | Test webhook delivery |
| [**TwitterTwitterScraperHealthCheck**](TwitterApi.md#twittertwitterscraperhealthcheck) | **GET** /v1/twitter/health | Twitter scraper health check |
| [**TwitterTwitterScraperHealthCheckHead**](TwitterApi.md#twittertwitterscraperhealthcheckhead) | **HEAD** /v1/twitter/health | Twitter scraper health check |
| [**TwitterUpdateFilterRule**](TwitterApi.md#twitterupdatefilterrule) | **PATCH** /v1/twitter/stream/filter-rules/{rule_id} | Update filter rule |
| [**TwitterUpdateStreamMonitor**](TwitterApi.md#twitterupdatestreammonitor) | **PATCH** /v1/twitter/stream/monitors/{monitor_id} | Update stream monitor |
| [**TwitterValidateSearchQuery**](TwitterApi.md#twittervalidatesearchquery) | **POST** /v1/twitter/stream/filter-rules/validate | Validate search query |

<a id="twitteradvancedtweetsearch"></a>
# **TwitterAdvancedTweetSearch**
> Object TwitterAdvancedTweetSearch (string query, string queryType = null, int? count = null, string cursor = null)

Advanced tweet search

Search tweets with advanced options.

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
    public class TwitterAdvancedTweetSearchExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | 
            var queryType = "queryType_example";  // string |  (optional) 
            var count = 56;  // int? |  (optional) 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Advanced tweet search
                Object result = apiInstance.TwitterAdvancedTweetSearch(query, queryType, count, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterAdvancedTweetSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterAdvancedTweetSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Advanced tweet search
    ApiResponse<Object> response = apiInstance.TwitterAdvancedTweetSearchWithHttpInfo(query, queryType, count, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterAdvancedTweetSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** |  |  |
| **queryType** | **string** |  | [optional]  |
| **count** | **int?** |  | [optional]  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twitterbatchgetusersbyids"></a>
# **TwitterBatchGetUsersByIds**
> Object TwitterBatchGetUsersByIds (string userIds)

Batch get users by IDs

Get multiple user profiles by their numeric IDs (comma-separated).

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
    public class TwitterBatchGetUsersByIdsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var userIds = "userIds_example";  // string | 

            try
            {
                // Batch get users by IDs
                Object result = apiInstance.TwitterBatchGetUsersByIds(userIds);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterBatchGetUsersByIds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterBatchGetUsersByIdsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Batch get users by IDs
    ApiResponse<Object> response = apiInstance.TwitterBatchGetUsersByIdsWithHttpInfo(userIds);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterBatchGetUsersByIdsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userIds** | **string** |  |  |

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

<a id="twitterbatchgetusersbyusernames"></a>
# **TwitterBatchGetUsersByUsernames**
> Object TwitterBatchGetUsersByUsernames (string usernames)

Batch get users by usernames

Get multiple user profiles by their usernames (comma-separated).

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
    public class TwitterBatchGetUsersByUsernamesExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var usernames = "usernames_example";  // string | 

            try
            {
                // Batch get users by usernames
                Object result = apiInstance.TwitterBatchGetUsersByUsernames(usernames);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterBatchGetUsersByUsernames: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterBatchGetUsersByUsernamesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Batch get users by usernames
    ApiResponse<Object> response = apiInstance.TwitterBatchGetUsersByUsernamesWithHttpInfo(usernames);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterBatchGetUsersByUsernamesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **usernames** | **string** |  |  |

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

<a id="twitterconfigurewebhookonamonitor"></a>
# **TwitterConfigureWebhookOnAMonitor**
> WebhookResponse TwitterConfigureWebhookOnAMonitor (WebhookCreate webhookCreate)

Configure webhook on a monitor

Configure a webhook delivery URL on a stream monitor.  The secret is returned only once on creation. Subsequent calls show secret_set: bool. If monitor already has a webhook, delete it first (409 is returned).

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
    public class TwitterConfigureWebhookOnAMonitorExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var webhookCreate = new WebhookCreate(); // WebhookCreate | 

            try
            {
                // Configure webhook on a monitor
                WebhookResponse result = apiInstance.TwitterConfigureWebhookOnAMonitor(webhookCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterConfigureWebhookOnAMonitor: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterConfigureWebhookOnAMonitorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Configure webhook on a monitor
    ApiResponse<WebhookResponse> response = apiInstance.TwitterConfigureWebhookOnAMonitorWithHttpInfo(webhookCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterConfigureWebhookOnAMonitorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookCreate** | [**WebhookCreate**](WebhookCreate.md) |  |  |

### Return type

[**WebhookResponse**](WebhookResponse.md)

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

<a id="twittercreatefilterrule"></a>
# **TwitterCreateFilterRule**
> FilterRuleResponse TwitterCreateFilterRule (FilterRuleCreate filterRuleCreate)

Create filter rule

Create a new query-based tweet filter rule.  The rule starts in 'active' status immediately. Credits must be positive. The (api_key_id, tag) pair must be unique.

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
    public class TwitterCreateFilterRuleExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var filterRuleCreate = new FilterRuleCreate(); // FilterRuleCreate | 

            try
            {
                // Create filter rule
                FilterRuleResponse result = apiInstance.TwitterCreateFilterRule(filterRuleCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterCreateFilterRule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterCreateFilterRuleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create filter rule
    ApiResponse<FilterRuleResponse> response = apiInstance.TwitterCreateFilterRuleWithHttpInfo(filterRuleCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterCreateFilterRuleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **filterRuleCreate** | [**FilterRuleCreate**](FilterRuleCreate.md) |  |  |

### Return type

[**FilterRuleResponse**](FilterRuleResponse.md)

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

<a id="twittercreatestreammonitor"></a>
# **TwitterCreateStreamMonitor**
> StreamMonitorResponse TwitterCreateStreamMonitor (StreamMonitorCreate streamMonitorCreate)

Create stream monitor

Create a new stream monitor to watch Twitter accounts in real-time.

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
    public class TwitterCreateStreamMonitorExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var streamMonitorCreate = new StreamMonitorCreate(); // StreamMonitorCreate | 

            try
            {
                // Create stream monitor
                StreamMonitorResponse result = apiInstance.TwitterCreateStreamMonitor(streamMonitorCreate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterCreateStreamMonitor: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterCreateStreamMonitorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create stream monitor
    ApiResponse<StreamMonitorResponse> response = apiInstance.TwitterCreateStreamMonitorWithHttpInfo(streamMonitorCreate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterCreateStreamMonitorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **streamMonitorCreate** | [**StreamMonitorCreate**](StreamMonitorCreate.md) |  |  |

### Return type

[**StreamMonitorResponse**](StreamMonitorResponse.md)

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

<a id="twitterdeletefilterrule"></a>
# **TwitterDeleteFilterRule**
> void TwitterDeleteFilterRule (string ruleId)

Delete filter rule

Delete a filter rule and all its logs.

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
    public class TwitterDeleteFilterRuleExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var ruleId = "ruleId_example";  // string | 

            try
            {
                // Delete filter rule
                apiInstance.TwitterDeleteFilterRule(ruleId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterDeleteFilterRule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterDeleteFilterRuleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete filter rule
    apiInstance.TwitterDeleteFilterRuleWithHttpInfo(ruleId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterDeleteFilterRuleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ruleId** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="twitterdeletestreammonitor"></a>
# **TwitterDeleteStreamMonitor**
> void TwitterDeleteStreamMonitor (string monitorId)

Delete stream monitor

Delete a stream monitor and all its logs.

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
    public class TwitterDeleteStreamMonitorExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var monitorId = "monitorId_example";  // string | 

            try
            {
                // Delete stream monitor
                apiInstance.TwitterDeleteStreamMonitor(monitorId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterDeleteStreamMonitor: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterDeleteStreamMonitorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete stream monitor
    apiInstance.TwitterDeleteStreamMonitorWithHttpInfo(monitorId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterDeleteStreamMonitorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **monitorId** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="twittergetarticlebyid"></a>
# **TwitterGetArticleById**
> Object TwitterGetArticleById (string articleId)

Get article by ID

Get a long-form article by its ID.

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
    public class TwitterGetArticleByIdExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var articleId = "articleId_example";  // string | 

            try
            {
                // Get article by ID
                Object result = apiInstance.TwitterGetArticleById(articleId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetArticleById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetArticleByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get article by ID
    ApiResponse<Object> response = apiInstance.TwitterGetArticleByIdWithHttpInfo(articleId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetArticleByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **articleId** | **string** |  |  |

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

<a id="twittergetbroadcastdetails"></a>
# **TwitterGetBroadcastDetails**
> Object TwitterGetBroadcastDetails (string broadcastId)

Get broadcast details

Get details of a live video broadcast.

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
    public class TwitterGetBroadcastDetailsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var broadcastId = "broadcastId_example";  // string | 

            try
            {
                // Get broadcast details
                Object result = apiInstance.TwitterGetBroadcastDetails(broadcastId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetBroadcastDetails: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetBroadcastDetailsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get broadcast details
    ApiResponse<Object> response = apiInstance.TwitterGetBroadcastDetailsWithHttpInfo(broadcastId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetBroadcastDetailsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **broadcastId** | **string** |  |  |

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

<a id="twittergetcommunitydetails"></a>
# **TwitterGetCommunityDetails**
> Object TwitterGetCommunityDetails (string communityId)

Get community details

Get details of a specific community.

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
    public class TwitterGetCommunityDetailsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var communityId = "communityId_example";  // string | 

            try
            {
                // Get community details
                Object result = apiInstance.TwitterGetCommunityDetails(communityId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetCommunityDetails: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetCommunityDetailsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get community details
    ApiResponse<Object> response = apiInstance.TwitterGetCommunityDetailsWithHttpInfo(communityId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetCommunityDetailsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **communityId** | **string** |  |  |

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

<a id="twittergetcommunitynotes"></a>
# **TwitterGetCommunityNotes**
> Object TwitterGetCommunityNotes (string tweetId)

Get community notes

Get community notes (Birdwatch) for a specific tweet.

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
    public class TwitterGetCommunityNotesExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var tweetId = "tweetId_example";  // string | 

            try
            {
                // Get community notes
                Object result = apiInstance.TwitterGetCommunityNotes(tweetId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetCommunityNotes: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetCommunityNotesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get community notes
    ApiResponse<Object> response = apiInstance.TwitterGetCommunityNotesWithHttpInfo(tweetId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetCommunityNotesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tweetId** | **string** |  |  |

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

<a id="twittergetcommunitytweets"></a>
# **TwitterGetCommunityTweets**
> Object TwitterGetCommunityTweets (string communityId, string tweetType = null, string cursor = null)

Get community tweets

Get tweets from a specific community.

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
    public class TwitterGetCommunityTweetsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var communityId = "communityId_example";  // string | 
            var tweetType = "tweetType_example";  // string |  (optional) 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Get community tweets
                Object result = apiInstance.TwitterGetCommunityTweets(communityId, tweetType, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetCommunityTweets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetCommunityTweetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get community tweets
    ApiResponse<Object> response = apiInstance.TwitterGetCommunityTweetsWithHttpInfo(communityId, tweetType, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetCommunityTweetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **communityId** | **string** |  |  |
| **tweetType** | **string** |  | [optional]  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittergetfilterrule"></a>
# **TwitterGetFilterRule**
> FilterRuleResponse TwitterGetFilterRule (string ruleId)

Get filter rule

Get a single filter rule by ID.

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
    public class TwitterGetFilterRuleExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var ruleId = "ruleId_example";  // string | 

            try
            {
                // Get filter rule
                FilterRuleResponse result = apiInstance.TwitterGetFilterRule(ruleId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetFilterRule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetFilterRuleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get filter rule
    ApiResponse<FilterRuleResponse> response = apiInstance.TwitterGetFilterRuleWithHttpInfo(ruleId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetFilterRuleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ruleId** | **string** |  |  |

### Return type

[**FilterRuleResponse**](FilterRuleResponse.md)

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

<a id="twittergetfilterruleperpollrates"></a>
# **TwitterGetFilterRulePerPollRates**
> PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse TwitterGetFilterRulePerPollRates ()

Get filter rule per-poll rates

Current per-poll rates (auth required — used by SDK + dashboard).

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
    public class TwitterGetFilterRulePerPollRatesExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);

            try
            {
                // Get filter rule per-poll rates
                PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse result = apiInstance.TwitterGetFilterRulePerPollRates();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetFilterRulePerPollRates: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetFilterRulePerPollRatesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get filter rule per-poll rates
    ApiResponse<PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse> response = apiInstance.TwitterGetFilterRulePerPollRatesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetFilterRulePerPollRatesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse**](PortalApiRoutersV1TwitterFilterRulesFilterRulePricingResponse.md)

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

<a id="twittergetlistdetails"></a>
# **TwitterGetListDetails**
> Object TwitterGetListDetails (string listId)

Get list details

Get details of a specific list.

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
    public class TwitterGetListDetailsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var listId = "listId_example";  // string | 

            try
            {
                // Get list details
                Object result = apiInstance.TwitterGetListDetails(listId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetListDetails: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetListDetailsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get list details
    ApiResponse<Object> response = apiInstance.TwitterGetListDetailsWithHttpInfo(listId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetListDetailsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listId** | **string** |  |  |

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

<a id="twittergetlisttweets"></a>
# **TwitterGetListTweets**
> Object TwitterGetListTweets (string listId, string cursor = null)

Get list tweets

Get tweets from a specific list.

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
    public class TwitterGetListTweetsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var listId = "listId_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Get list tweets
                Object result = apiInstance.TwitterGetListTweets(listId, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetListTweets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetListTweetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get list tweets
    ApiResponse<Object> response = apiInstance.TwitterGetListTweetsWithHttpInfo(listId, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetListTweetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listId** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittergetplacedetails"></a>
# **TwitterGetPlaceDetails**
> Object TwitterGetPlaceDetails (string placeId)

Get place details

Get details of a specific place.

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
    public class TwitterGetPlaceDetailsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var placeId = "placeId_example";  // string | 

            try
            {
                // Get place details
                Object result = apiInstance.TwitterGetPlaceDetails(placeId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetPlaceDetails: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetPlaceDetailsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get place details
    ApiResponse<Object> response = apiInstance.TwitterGetPlaceDetailsWithHttpInfo(placeId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetPlaceDetailsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **placeId** | **string** |  |  |

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

<a id="twittergetsimilartweets"></a>
# **TwitterGetSimilarTweets**
> Object TwitterGetSimilarTweets (string tweetId)

Get similar tweets

Get tweets similar to a specific tweet.

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
    public class TwitterGetSimilarTweetsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var tweetId = "tweetId_example";  // string | 

            try
            {
                // Get similar tweets
                Object result = apiInstance.TwitterGetSimilarTweets(tweetId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetSimilarTweets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetSimilarTweetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get similar tweets
    ApiResponse<Object> response = apiInstance.TwitterGetSimilarTweetsWithHttpInfo(tweetId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetSimilarTweetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tweetId** | **string** |  |  |

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

<a id="twittergetspacedetails"></a>
# **TwitterGetSpaceDetails**
> Object TwitterGetSpaceDetails (string spaceId)

Get Space details

Get details of a Twitter Space.

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
    public class TwitterGetSpaceDetailsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var spaceId = "spaceId_example";  // string | 

            try
            {
                // Get Space details
                Object result = apiInstance.TwitterGetSpaceDetails(spaceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetSpaceDetails: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetSpaceDetailsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Space details
    ApiResponse<Object> response = apiInstance.TwitterGetSpaceDetailsWithHttpInfo(spaceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetSpaceDetailsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **spaceId** | **string** |  |  |

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

<a id="twittergetstreammonitor"></a>
# **TwitterGetStreamMonitor**
> StreamMonitorResponse TwitterGetStreamMonitor (string monitorId)

Get stream monitor

Get a single stream monitor by ID.

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
    public class TwitterGetStreamMonitorExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var monitorId = "monitorId_example";  // string | 

            try
            {
                // Get stream monitor
                StreamMonitorResponse result = apiInstance.TwitterGetStreamMonitor(monitorId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetStreamMonitor: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetStreamMonitorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get stream monitor
    ApiResponse<StreamMonitorResponse> response = apiInstance.TwitterGetStreamMonitorWithHttpInfo(monitorId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetStreamMonitorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **monitorId** | **string** |  |  |

### Return type

[**StreamMonitorResponse**](StreamMonitorResponse.md)

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

<a id="twittergettrendingtopics"></a>
# **TwitterGetTrendingTopics**
> Object TwitterGetTrendingTopics (string category = null, int? count = null)

Get trending topics

Get trending topics.

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
    public class TwitterGetTrendingTopicsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var category = "category_example";  // string |  (optional) 
            var count = 56;  // int? |  (optional) 

            try
            {
                // Get trending topics
                Object result = apiInstance.TwitterGetTrendingTopics(category, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetTrendingTopics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetTrendingTopicsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get trending topics
    ApiResponse<Object> response = apiInstance.TwitterGetTrendingTopicsWithHttpInfo(category, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetTrendingTopicsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **category** | **string** |  | [optional]  |
| **count** | **int?** |  | [optional]  |

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

<a id="twittergettrendsbylocation"></a>
# **TwitterGetTrendsByLocation**
> Object TwitterGetTrendsByLocation (string woeid)

Get trends by location

Get trending topics for a specific location (WOEID).

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
    public class TwitterGetTrendsByLocationExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var woeid = "woeid_example";  // string | 

            try
            {
                // Get trends by location
                Object result = apiInstance.TwitterGetTrendsByLocation(woeid);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetTrendsByLocation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetTrendsByLocationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get trends by location
    ApiResponse<Object> response = apiInstance.TwitterGetTrendsByLocationWithHttpInfo(woeid);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetTrendsByLocationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **woeid** | **string** |  |  |

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

<a id="twittergettweetdetails"></a>
# **TwitterGetTweetDetails**
> Object TwitterGetTweetDetails (string tweetId, string cursor = null)

Get tweet details

Get detailed information about a specific tweet.

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
    public class TwitterGetTweetDetailsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var tweetId = "tweetId_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Get tweet details
                Object result = apiInstance.TwitterGetTweetDetails(tweetId, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetTweetDetails: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetTweetDetailsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get tweet details
    ApiResponse<Object> response = apiInstance.TwitterGetTweetDetailsWithHttpInfo(tweetId, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetTweetDetailsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tweetId** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittergettweetedithistory"></a>
# **TwitterGetTweetEditHistory**
> Object TwitterGetTweetEditHistory (string tweetId)

Get tweet edit history

Get the edit history of a tweet.

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
    public class TwitterGetTweetEditHistoryExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var tweetId = "tweetId_example";  // string | 

            try
            {
                // Get tweet edit history
                Object result = apiInstance.TwitterGetTweetEditHistory(tweetId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetTweetEditHistory: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetTweetEditHistoryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get tweet edit history
    ApiResponse<Object> response = apiInstance.TwitterGetTweetEditHistoryWithHttpInfo(tweetId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetTweetEditHistoryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tweetId** | **string** |  |  |

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

<a id="twittergettweetfavoriters"></a>
# **TwitterGetTweetFavoriters**
> Object TwitterGetTweetFavoriters (string tweetId, string cursor = null)

Get tweet favoriters

Get users who favorited a specific tweet.

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
    public class TwitterGetTweetFavoritersExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var tweetId = "tweetId_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Get tweet favoriters
                Object result = apiInstance.TwitterGetTweetFavoriters(tweetId, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetTweetFavoriters: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetTweetFavoritersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get tweet favoriters
    ApiResponse<Object> response = apiInstance.TwitterGetTweetFavoritersWithHttpInfo(tweetId, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetTweetFavoritersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tweetId** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittergettweetquotes"></a>
# **TwitterGetTweetQuotes**
> Object TwitterGetTweetQuotes (string tweetId, string cursor = null)

Get tweet quotes

Get tweets that quote a specific tweet.

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
    public class TwitterGetTweetQuotesExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var tweetId = "tweetId_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Get tweet quotes
                Object result = apiInstance.TwitterGetTweetQuotes(tweetId, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetTweetQuotes: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetTweetQuotesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get tweet quotes
    ApiResponse<Object> response = apiInstance.TwitterGetTweetQuotesWithHttpInfo(tweetId, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetTweetQuotesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tweetId** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittergettweetreplies"></a>
# **TwitterGetTweetReplies**
> Object TwitterGetTweetReplies (string tweetId, string cursor = null)

Get tweet replies

Get replies to a specific tweet.

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
    public class TwitterGetTweetRepliesExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var tweetId = "tweetId_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Get tweet replies
                Object result = apiInstance.TwitterGetTweetReplies(tweetId, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetTweetReplies: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetTweetRepliesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get tweet replies
    ApiResponse<Object> response = apiInstance.TwitterGetTweetRepliesWithHttpInfo(tweetId, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetTweetRepliesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tweetId** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittergettweetretweeters"></a>
# **TwitterGetTweetRetweeters**
> Object TwitterGetTweetRetweeters (string tweetId, string cursor = null)

Get tweet retweeters

Get users who retweeted a specific tweet.

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
    public class TwitterGetTweetRetweetersExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var tweetId = "tweetId_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Get tweet retweeters
                Object result = apiInstance.TwitterGetTweetRetweeters(tweetId, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetTweetRetweeters: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetTweetRetweetersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get tweet retweeters
    ApiResponse<Object> response = apiInstance.TwitterGetTweetRetweetersWithHttpInfo(tweetId, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetTweetRetweetersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tweetId** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittergettweetsbyids"></a>
# **TwitterGetTweetsByIds**
> Object TwitterGetTweetsByIds (string tweets)

Get tweets by IDs

Get multiple tweets by their IDs.

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
    public class TwitterGetTweetsByIdsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var tweets = "tweets_example";  // string | 

            try
            {
                // Get tweets by IDs
                Object result = apiInstance.TwitterGetTweetsByIds(tweets);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetTweetsByIds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetTweetsByIdsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get tweets by IDs
    ApiResponse<Object> response = apiInstance.TwitterGetTweetsByIdsWithHttpInfo(tweets);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetTweetsByIdsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tweets** | **string** |  |  |

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

<a id="twittergetuserarticles"></a>
# **TwitterGetUserArticles**
> Object TwitterGetUserArticles (string userId, string cursor = null)

Get user articles

Get long-form articles written by a user.

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
    public class TwitterGetUserArticlesExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var userId = "userId_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Get user articles
                Object result = apiInstance.TwitterGetUserArticles(userId, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetUserArticles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetUserArticlesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user articles
    ApiResponse<Object> response = apiInstance.TwitterGetUserArticlesWithHttpInfo(userId, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetUserArticlesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userId** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittergetuserbyid"></a>
# **TwitterGetUserById**
> Object TwitterGetUserById (string userId)

Get user by ID

Get user profile by user ID.

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
    public class TwitterGetUserByIdExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var userId = "userId_example";  // string | 

            try
            {
                // Get user by ID
                Object result = apiInstance.TwitterGetUserById(userId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetUserById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetUserByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user by ID
    ApiResponse<Object> response = apiInstance.TwitterGetUserByIdWithHttpInfo(userId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetUserByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userId** | **string** |  |  |

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

<a id="twittergetuserbyusername"></a>
# **TwitterGetUserByUsername**
> Object TwitterGetUserByUsername (string username)

Get user by username

Get user profile by username.

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
    public class TwitterGetUserByUsernameExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 

            try
            {
                // Get user by username
                Object result = apiInstance.TwitterGetUserByUsername(username);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetUserByUsername: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetUserByUsernameWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user by username
    ApiResponse<Object> response = apiInstance.TwitterGetUserByUsernameWithHttpInfo(username);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetUserByUsernameWithHttpInfo: " + e.Message);
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

<a id="twittergetuserfollowers"></a>
# **TwitterGetUserFollowers**
> Object TwitterGetUserFollowers (string username, string cursor = null)

Get user followers

Get followers of a specific user.

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
    public class TwitterGetUserFollowersExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Get user followers
                Object result = apiInstance.TwitterGetUserFollowers(username, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetUserFollowers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetUserFollowersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user followers
    ApiResponse<Object> response = apiInstance.TwitterGetUserFollowersWithHttpInfo(username, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetUserFollowersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittergetuserfollowing"></a>
# **TwitterGetUserFollowing**
> Object TwitterGetUserFollowing (string username, string cursor = null)

Get user following

Get users that a specific user is following.

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
    public class TwitterGetUserFollowingExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Get user following
                Object result = apiInstance.TwitterGetUserFollowing(username, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetUserFollowing: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetUserFollowingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user following
    ApiResponse<Object> response = apiInstance.TwitterGetUserFollowingWithHttpInfo(username, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetUserFollowingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittergetusermentions"></a>
# **TwitterGetUserMentions**
> Object TwitterGetUserMentions (string username, int? count = null, string cursor = null)

Get user mentions

Get tweets mentioning a specific user.

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
    public class TwitterGetUserMentionsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var count = 56;  // int? |  (optional) 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Get user mentions
                Object result = apiInstance.TwitterGetUserMentions(username, count, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetUserMentions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetUserMentionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user mentions
    ApiResponse<Object> response = apiInstance.TwitterGetUserMentionsWithHttpInfo(username, count, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetUserMentionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **count** | **int?** |  | [optional]  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittergetusersubscriptions"></a>
# **TwitterGetUserSubscriptions**
> Object TwitterGetUserSubscriptions (string userId, string cursor = null)

Get user subscriptions

Get subscriptions of a specific user.

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
    public class TwitterGetUserSubscriptionsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var userId = "userId_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Get user subscriptions
                Object result = apiInstance.TwitterGetUserSubscriptions(userId, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetUserSubscriptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetUserSubscriptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user subscriptions
    ApiResponse<Object> response = apiInstance.TwitterGetUserSubscriptionsWithHttpInfo(userId, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetUserSubscriptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userId** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittergetusertweets"></a>
# **TwitterGetUserTweets**
> Object TwitterGetUserTweets (string username, string cursor = null)

Get user tweets

Get latest tweets from a specific user.

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
    public class TwitterGetUserTweetsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Get user tweets
                Object result = apiInstance.TwitterGetUserTweets(username, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterGetUserTweets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterGetUserTweetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user tweets
    ApiResponse<Object> response = apiInstance.TwitterGetUserTweetsWithHttpInfo(username, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterGetUserTweetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twitterlistbillinglogs"></a>
# **TwitterListBillingLogs**
> BillingLogListResponse TwitterListBillingLogs (string monitorId = null, int? page = null, int? pageSize = null)

List billing logs

List billing activity logs for the authenticated API key's monitors.

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
    public class TwitterListBillingLogsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var monitorId = "monitorId_example";  // string |  (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)
            var pageSize = 20;  // int? |  (optional)  (default to 20)

            try
            {
                // List billing logs
                BillingLogListResponse result = apiInstance.TwitterListBillingLogs(monitorId, page, pageSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterListBillingLogs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterListBillingLogsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List billing logs
    ApiResponse<BillingLogListResponse> response = apiInstance.TwitterListBillingLogsWithHttpInfo(monitorId, page, pageSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterListBillingLogsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **monitorId** | **string** |  | [optional]  |
| **page** | **int?** |  | [optional] [default to 1] |
| **pageSize** | **int?** |  | [optional] [default to 20] |

### Return type

[**BillingLogListResponse**](BillingLogListResponse.md)

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

<a id="twitterlistdeliverylogsforafilterrule"></a>
# **TwitterListDeliveryLogsForAFilterRule**
> FilterRuleDeliveryLogListResponse TwitterListDeliveryLogsForAFilterRule (string ruleId, string deliveryStatus = null, string authorUsername = null, int? page = null, int? pageSize = null, string sort = null)

List delivery logs for a filter rule

List tweet delivery logs for a specific filter rule.

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
    public class TwitterListDeliveryLogsForAFilterRuleExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var ruleId = "ruleId_example";  // string | 
            var deliveryStatus = "deliveryStatus_example";  // string |  (optional) 
            var authorUsername = "authorUsername_example";  // string |  (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)
            var pageSize = 20;  // int? |  (optional)  (default to 20)
            var sort = "asc";  // string |  (optional)  (default to desc)

            try
            {
                // List delivery logs for a filter rule
                FilterRuleDeliveryLogListResponse result = apiInstance.TwitterListDeliveryLogsForAFilterRule(ruleId, deliveryStatus, authorUsername, page, pageSize, sort);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterListDeliveryLogsForAFilterRule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterListDeliveryLogsForAFilterRuleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List delivery logs for a filter rule
    ApiResponse<FilterRuleDeliveryLogListResponse> response = apiInstance.TwitterListDeliveryLogsForAFilterRuleWithHttpInfo(ruleId, deliveryStatus, authorUsername, page, pageSize, sort);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterListDeliveryLogsForAFilterRuleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ruleId** | **string** |  |  |
| **deliveryStatus** | **string** |  | [optional]  |
| **authorUsername** | **string** |  | [optional]  |
| **page** | **int?** |  | [optional] [default to 1] |
| **pageSize** | **int?** |  | [optional] [default to 20] |
| **sort** | **string** |  | [optional] [default to desc] |

### Return type

[**FilterRuleDeliveryLogListResponse**](FilterRuleDeliveryLogListResponse.md)

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

<a id="twitterlistfilterrules"></a>
# **TwitterListFilterRules**
> FilterRuleListResponse TwitterListFilterRules (string status = null, int? page = null, int? pageSize = null)

List filter rules

List all filter rules for the authenticated API key.

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
    public class TwitterListFilterRulesExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var status = "status_example";  // string |  (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)
            var pageSize = 20;  // int? |  (optional)  (default to 20)

            try
            {
                // List filter rules
                FilterRuleListResponse result = apiInstance.TwitterListFilterRules(status, page, pageSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterListFilterRules: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterListFilterRulesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List filter rules
    ApiResponse<FilterRuleListResponse> response = apiInstance.TwitterListFilterRulesWithHttpInfo(status, page, pageSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterListFilterRulesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **status** | **string** |  | [optional]  |
| **page** | **int?** |  | [optional] [default to 1] |
| **pageSize** | **int?** |  | [optional] [default to 20] |

### Return type

[**FilterRuleListResponse**](FilterRuleListResponse.md)

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

<a id="twitterliststreammonitors"></a>
# **TwitterListStreamMonitors**
> StreamMonitorListResponse TwitterListStreamMonitors (string status = null, int? page = null, int? pageSize = null)

List stream monitors

List all stream monitors for the authenticated API key.

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
    public class TwitterListStreamMonitorsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var status = "status_example";  // string |  (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)
            var pageSize = 20;  // int? |  (optional)  (default to 20)

            try
            {
                // List stream monitors
                StreamMonitorListResponse result = apiInstance.TwitterListStreamMonitors(status, page, pageSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterListStreamMonitors: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterListStreamMonitorsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List stream monitors
    ApiResponse<StreamMonitorListResponse> response = apiInstance.TwitterListStreamMonitorsWithHttpInfo(status, page, pageSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterListStreamMonitorsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **status** | **string** |  | [optional]  |
| **page** | **int?** |  | [optional] [default to 1] |
| **pageSize** | **int?** |  | [optional] [default to 20] |

### Return type

[**StreamMonitorListResponse**](StreamMonitorListResponse.md)

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

<a id="twitterlisttweetdeliverylogs"></a>
# **TwitterListTweetDeliveryLogs**
> TweetDeliveryLogListResponse TwitterListTweetDeliveryLogs (string monitorId = null, string authorUsername = null, string deliveryStatus = null, int? page = null, int? pageSize = null, string sort = null)

List tweet delivery logs

List tweet delivery logs for the authenticated API key's monitors.

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
    public class TwitterListTweetDeliveryLogsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var monitorId = "monitorId_example";  // string |  (optional) 
            var authorUsername = "authorUsername_example";  // string |  (optional) 
            var deliveryStatus = "deliveryStatus_example";  // string |  (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)
            var pageSize = 20;  // int? |  (optional)  (default to 20)
            var sort = "asc";  // string |  (optional)  (default to desc)

            try
            {
                // List tweet delivery logs
                TweetDeliveryLogListResponse result = apiInstance.TwitterListTweetDeliveryLogs(monitorId, authorUsername, deliveryStatus, page, pageSize, sort);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterListTweetDeliveryLogs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterListTweetDeliveryLogsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List tweet delivery logs
    ApiResponse<TweetDeliveryLogListResponse> response = apiInstance.TwitterListTweetDeliveryLogsWithHttpInfo(monitorId, authorUsername, deliveryStatus, page, pageSize, sort);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterListTweetDeliveryLogsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **monitorId** | **string** |  | [optional]  |
| **authorUsername** | **string** |  | [optional]  |
| **deliveryStatus** | **string** |  | [optional]  |
| **page** | **int?** |  | [optional] [default to 1] |
| **pageSize** | **int?** |  | [optional] [default to 20] |
| **sort** | **string** |  | [optional] [default to desc] |

### Return type

[**TweetDeliveryLogListResponse**](TweetDeliveryLogListResponse.md)

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

<a id="twitterlistwebhooks"></a>
# **TwitterListWebhooks**
> WebhookListResponse TwitterListWebhooks (string monitorId = null)

List webhooks

List all webhook-configured monitors for the authenticated API key.

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
    public class TwitterListWebhooksExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var monitorId = "monitorId_example";  // string |  (optional) 

            try
            {
                // List webhooks
                WebhookListResponse result = apiInstance.TwitterListWebhooks(monitorId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterListWebhooks: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterListWebhooksWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List webhooks
    ApiResponse<WebhookListResponse> response = apiInstance.TwitterListWebhooksWithHttpInfo(monitorId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterListWebhooksWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **monitorId** | **string** |  | [optional]  |

### Return type

[**WebhookListResponse**](WebhookListResponse.md)

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

<a id="twitterremovewebhookfrommonitor"></a>
# **TwitterRemoveWebhookFromMonitor**
> void TwitterRemoveWebhookFromMonitor (string webhookId)

Remove webhook from monitor

Remove webhook configuration from a monitor. webhook_id is the monitor_id.

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
    public class TwitterRemoveWebhookFromMonitorExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var webhookId = "webhookId_example";  // string | 

            try
            {
                // Remove webhook from monitor
                apiInstance.TwitterRemoveWebhookFromMonitor(webhookId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterRemoveWebhookFromMonitor: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterRemoveWebhookFromMonitorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove webhook from monitor
    apiInstance.TwitterRemoveWebhookFromMonitorWithHttpInfo(webhookId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterRemoveWebhookFromMonitorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookId** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="twittersearchcommunities"></a>
# **TwitterSearchCommunities**
> Object TwitterSearchCommunities (string query, string cursor = null)

Search communities

Search for communities by query.

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
    public class TwitterSearchCommunitiesExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Search communities
                Object result = apiInstance.TwitterSearchCommunities(query, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterSearchCommunities: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterSearchCommunitiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search communities
    ApiResponse<Object> response = apiInstance.TwitterSearchCommunitiesWithHttpInfo(query, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterSearchCommunitiesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittersearchlisttweets"></a>
# **TwitterSearchListTweets**
> Object TwitterSearchListTweets (string listId, string query, string cursor = null)

Search list tweets

Search tweets within a specific list.

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
    public class TwitterSearchListTweetsExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var listId = "listId_example";  // string | 
            var query = "query_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Search list tweets
                Object result = apiInstance.TwitterSearchListTweets(listId, query, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterSearchListTweets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterSearchListTweetsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search list tweets
    ApiResponse<Object> response = apiInstance.TwitterSearchListTweetsWithHttpInfo(listId, query, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterSearchListTweetsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listId** | **string** |  |  |
| **query** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittersearchplaces"></a>
# **TwitterSearchPlaces**
> Object TwitterSearchPlaces (string query = null, decimal? lat = null, decimal? varLong = null)

Search places

Search for places by query or coordinates.

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
    public class TwitterSearchPlacesExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string |  (optional) 
            var lat = 8.14D;  // decimal? |  (optional) 
            var varLong = 8.14D;  // decimal? |  (optional) 

            try
            {
                // Search places
                Object result = apiInstance.TwitterSearchPlaces(query, lat, varLong);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterSearchPlaces: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterSearchPlacesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search places
    ApiResponse<Object> response = apiInstance.TwitterSearchPlacesWithHttpInfo(query, lat, varLong);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterSearchPlacesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** |  | [optional]  |
| **lat** | **decimal?** |  | [optional]  |
| **varLong** | **decimal?** |  | [optional]  |

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

<a id="twittersearchusers"></a>
# **TwitterSearchUsers**
> Object TwitterSearchUsers (string query, string cursor = null)

Search users

Search for users by query.

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
    public class TwitterSearchUsersExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | 
            var cursor = "cursor_example";  // string |  (optional) 

            try
            {
                // Search users
                Object result = apiInstance.TwitterSearchUsers(query, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterSearchUsers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterSearchUsersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search users
    ApiResponse<Object> response = apiInstance.TwitterSearchUsersWithHttpInfo(query, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterSearchUsersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** |  |  |
| **cursor** | **string** |  | [optional]  |

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

<a id="twittertestwebhookdelivery"></a>
# **TwitterTestWebhookDelivery**
> WebhookTestResponse TwitterTestWebhookDelivery (WebhookTestRequest webhookTestRequest)

Test webhook delivery

Send a test payload to a monitor's webhook URL.  The test payload has type=\"test\" instead of type=\"tweet\". Makes a synchronous HTTP POST and returns the delivery result.

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
    public class TwitterTestWebhookDeliveryExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var webhookTestRequest = new WebhookTestRequest(); // WebhookTestRequest | 

            try
            {
                // Test webhook delivery
                WebhookTestResponse result = apiInstance.TwitterTestWebhookDelivery(webhookTestRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterTestWebhookDelivery: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterTestWebhookDeliveryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Test webhook delivery
    ApiResponse<WebhookTestResponse> response = apiInstance.TwitterTestWebhookDeliveryWithHttpInfo(webhookTestRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterTestWebhookDeliveryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookTestRequest** | [**WebhookTestRequest**](WebhookTestRequest.md) |  |  |

### Return type

[**WebhookTestResponse**](WebhookTestResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="twittertwitterscraperhealthcheck"></a>
# **TwitterTwitterScraperHealthCheck**
> Object TwitterTwitterScraperHealthCheck ()

Twitter scraper health check

Check health of the Twitter scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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
    public class TwitterTwitterScraperHealthCheckExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);

            try
            {
                // Twitter scraper health check
                Object result = apiInstance.TwitterTwitterScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterTwitterScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterTwitterScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Twitter scraper health check
    ApiResponse<Object> response = apiInstance.TwitterTwitterScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterTwitterScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="twittertwitterscraperhealthcheckhead"></a>
# **TwitterTwitterScraperHealthCheckHead**
> Object TwitterTwitterScraperHealthCheckHead ()

Twitter scraper health check

Check health of the Twitter scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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
    public class TwitterTwitterScraperHealthCheckHeadExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);

            try
            {
                // Twitter scraper health check
                Object result = apiInstance.TwitterTwitterScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterTwitterScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterTwitterScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Twitter scraper health check
    ApiResponse<Object> response = apiInstance.TwitterTwitterScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterTwitterScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="twitterupdatefilterrule"></a>
# **TwitterUpdateFilterRule**
> FilterRuleResponse TwitterUpdateFilterRule (string ruleId, FilterRuleUpdate filterRuleUpdate)

Update filter rule

Partially update a filter rule.  Setting status='active' on a paused rule performs a credit check.

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
    public class TwitterUpdateFilterRuleExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var ruleId = "ruleId_example";  // string | 
            var filterRuleUpdate = new FilterRuleUpdate(); // FilterRuleUpdate | 

            try
            {
                // Update filter rule
                FilterRuleResponse result = apiInstance.TwitterUpdateFilterRule(ruleId, filterRuleUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterUpdateFilterRule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterUpdateFilterRuleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update filter rule
    ApiResponse<FilterRuleResponse> response = apiInstance.TwitterUpdateFilterRuleWithHttpInfo(ruleId, filterRuleUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterUpdateFilterRuleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **ruleId** | **string** |  |  |
| **filterRuleUpdate** | [**FilterRuleUpdate**](FilterRuleUpdate.md) |  |  |

### Return type

[**FilterRuleResponse**](FilterRuleResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="twitterupdatestreammonitor"></a>
# **TwitterUpdateStreamMonitor**
> StreamMonitorResponse TwitterUpdateStreamMonitor (string monitorId, StreamMonitorUpdate streamMonitorUpdate)

Update stream monitor

Partially update a stream monitor.

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
    public class TwitterUpdateStreamMonitorExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var monitorId = "monitorId_example";  // string | 
            var streamMonitorUpdate = new StreamMonitorUpdate(); // StreamMonitorUpdate | 

            try
            {
                // Update stream monitor
                StreamMonitorResponse result = apiInstance.TwitterUpdateStreamMonitor(monitorId, streamMonitorUpdate);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterUpdateStreamMonitor: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterUpdateStreamMonitorWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update stream monitor
    ApiResponse<StreamMonitorResponse> response = apiInstance.TwitterUpdateStreamMonitorWithHttpInfo(monitorId, streamMonitorUpdate);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterUpdateStreamMonitorWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **monitorId** | **string** |  |  |
| **streamMonitorUpdate** | [**StreamMonitorUpdate**](StreamMonitorUpdate.md) |  |  |

### Return type

[**StreamMonitorResponse**](StreamMonitorResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="twittervalidatesearchquery"></a>
# **TwitterValidateSearchQuery**
> FilterRuleValidateResponse TwitterValidateSearchQuery (FilterRuleValidateRequest filterRuleValidateRequest)

Validate search query

Validate a Twitter search query string.  Performs basic structural validation without making a live Twitter request. Returns valid=True if the query passes syntax checks.

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
    public class TwitterValidateSearchQueryExample
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
            var apiInstance = new TwitterApi(httpClient, config, httpClientHandler);
            var filterRuleValidateRequest = new FilterRuleValidateRequest(); // FilterRuleValidateRequest | 

            try
            {
                // Validate search query
                FilterRuleValidateResponse result = apiInstance.TwitterValidateSearchQuery(filterRuleValidateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TwitterApi.TwitterValidateSearchQuery: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TwitterValidateSearchQueryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Validate search query
    ApiResponse<FilterRuleValidateResponse> response = apiInstance.TwitterValidateSearchQueryWithHttpInfo(filterRuleValidateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TwitterApi.TwitterValidateSearchQueryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **filterRuleValidateRequest** | [**FilterRuleValidateRequest**](FilterRuleValidateRequest.md) |  |  |

### Return type

[**FilterRuleValidateResponse**](FilterRuleValidateResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

