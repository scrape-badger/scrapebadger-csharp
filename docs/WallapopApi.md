# ScrapeBadger.Api.WallapopApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**WallapopAutocomplete**](WallapopApi.md#wallapopautocomplete) | **GET** /v1/wallapop/autocomplete | Autocomplete |
| [**WallapopGetListingDetail**](WallapopApi.md#wallapopgetlistingdetail) | **GET** /v1/wallapop/items/{item_id} | Get listing detail |
| [**WallapopGetUserListings**](WallapopApi.md#wallapopgetuserlistings) | **GET** /v1/wallapop/users/{user_id}/items | Get user listings |
| [**WallapopGetUserProfile**](WallapopApi.md#wallapopgetuserprofile) | **GET** /v1/wallapop/users/{user_id} | Get user profile |
| [**WallapopGetUserReviews**](WallapopApi.md#wallapopgetuserreviews) | **GET** /v1/wallapop/users/{user_id}/reviews | Get user reviews |
| [**WallapopListCategories**](WallapopApi.md#wallapoplistcategories) | **GET** /v1/wallapop/categories | List categories |
| [**WallapopListFilterOptions**](WallapopApi.md#wallapoplistfilteroptions) | **GET** /v1/wallapop/filters/{filter_id}/options | List filter options |
| [**WallapopListMarkets**](WallapopApi.md#wallapoplistmarkets) | **GET** /v1/wallapop/markets | List markets |
| [**WallapopListSearchFilters**](WallapopApi.md#wallapoplistsearchfilters) | **GET** /v1/wallapop/filters | List search filters |
| [**WallapopSearchListings**](WallapopApi.md#wallapopsearchlistings) | **GET** /v1/wallapop/search | Search listings |
| [**WallapopWallapopScraperHealthCheck**](WallapopApi.md#wallapopwallapopscraperhealthcheck) | **GET** /v1/wallapop/health | Wallapop scraper health check |
| [**WallapopWallapopScraperHealthCheckHead**](WallapopApi.md#wallapopwallapopscraperhealthcheckhead) | **HEAD** /v1/wallapop/health | Wallapop scraper health check |

<a id="wallapopautocomplete"></a>
# **WallapopAutocomplete**
> Object WallapopAutocomplete (string query, string market = null)

Autocomplete

Wallapop's search-box suggestions for a partial query.

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
    public class WallapopAutocompleteExample
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
            var apiInstance = new WallapopApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Partial search text, e.g. 'bici'
            var market = "\"es\"";  // string | Market: es (Spain), it (Italy), pt (Portugal) (optional)  (default to "es")

            try
            {
                // Autocomplete
                Object result = apiInstance.WallapopAutocomplete(query, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WallapopApi.WallapopAutocomplete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WallapopAutocompleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Autocomplete
    ApiResponse<Object> response = apiInstance.WallapopAutocompleteWithHttpInfo(query, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WallapopApi.WallapopAutocompleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Partial search text, e.g. &#39;bici&#39; |  |
| **market** | **string** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;] |

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

<a id="wallapopgetlistingdetail"></a>
# **WallapopGetListingDetail**
> Object WallapopGetListingDetail (string itemId, string market = null)

Get listing detail

Full listing detail by id (e.g. nzxeknm5x562) or listing slug.

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
    public class WallapopGetListingDetailExample
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
            var apiInstance = new WallapopApi(httpClient, config, httpClientHandler);
            var itemId = "itemId_example";  // string | 
            var market = "\"es\"";  // string | Market: es (Spain), it (Italy), pt (Portugal) (optional)  (default to "es")

            try
            {
                // Get listing detail
                Object result = apiInstance.WallapopGetListingDetail(itemId, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WallapopApi.WallapopGetListingDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WallapopGetListingDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get listing detail
    ApiResponse<Object> response = apiInstance.WallapopGetListingDetailWithHttpInfo(itemId, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WallapopApi.WallapopGetListingDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **itemId** | **string** |  |  |
| **market** | **string** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;] |

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

<a id="wallapopgetuserlistings"></a>
# **WallapopGetUserListings**
> Object WallapopGetUserListings (string userId, string market = null, string nextPage = null)

Get user listings

A seller's live listings, 40 per page.

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
    public class WallapopGetUserListingsExample
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
            var apiInstance = new WallapopApi(httpClient, config, httpClientHandler);
            var userId = "userId_example";  // string | 
            var market = "\"es\"";  // string | Market: es (Spain), it (Italy), pt (Portugal) (optional)  (default to "es")
            var nextPage = "nextPage_example";  // string | Cursor from the previous page's next_page (optional) 

            try
            {
                // Get user listings
                Object result = apiInstance.WallapopGetUserListings(userId, market, nextPage);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WallapopApi.WallapopGetUserListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WallapopGetUserListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user listings
    ApiResponse<Object> response = apiInstance.WallapopGetUserListingsWithHttpInfo(userId, market, nextPage);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WallapopApi.WallapopGetUserListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userId** | **string** |  |  |
| **market** | **string** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;] |
| **nextPage** | **string** | Cursor from the previous page&#39;s next_page | [optional]  |

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

<a id="wallapopgetuserprofile"></a>
# **WallapopGetUserProfile**
> Object WallapopGetUserProfile (string userId, string market = null)

Get user profile

Seller profile with ratings, sales counters, response rate and verifications.

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
    public class WallapopGetUserProfileExample
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
            var apiInstance = new WallapopApi(httpClient, config, httpClientHandler);
            var userId = "userId_example";  // string | 
            var market = "\"es\"";  // string | Market: es (Spain), it (Italy), pt (Portugal) (optional)  (default to "es")

            try
            {
                // Get user profile
                Object result = apiInstance.WallapopGetUserProfile(userId, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WallapopApi.WallapopGetUserProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WallapopGetUserProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user profile
    ApiResponse<Object> response = apiInstance.WallapopGetUserProfileWithHttpInfo(userId, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WallapopApi.WallapopGetUserProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userId** | **string** |  |  |
| **market** | **string** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;] |

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

<a id="wallapopgetuserreviews"></a>
# **WallapopGetUserReviews**
> Object WallapopGetUserReviews (string userId, string market = null, string nextPage = null)

Get user reviews

Reviews a seller received, newest first, 40 per page.

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
    public class WallapopGetUserReviewsExample
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
            var apiInstance = new WallapopApi(httpClient, config, httpClientHandler);
            var userId = "userId_example";  // string | 
            var market = "\"es\"";  // string | Market: es (Spain), it (Italy), pt (Portugal) (optional)  (default to "es")
            var nextPage = "nextPage_example";  // string | Cursor from the previous page's next_page (optional) 

            try
            {
                // Get user reviews
                Object result = apiInstance.WallapopGetUserReviews(userId, market, nextPage);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WallapopApi.WallapopGetUserReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WallapopGetUserReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user reviews
    ApiResponse<Object> response = apiInstance.WallapopGetUserReviewsWithHttpInfo(userId, market, nextPage);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WallapopApi.WallapopGetUserReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userId** | **string** |  |  |
| **market** | **string** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;] |
| **nextPage** | **string** | Cursor from the previous page&#39;s next_page | [optional]  |

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

<a id="wallapoplistcategories"></a>
# **WallapopListCategories**
> Object WallapopListCategories (string market = null)

List categories

The full category tree; ids are usable as the search category_id.

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
    public class WallapopListCategoriesExample
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
            var apiInstance = new WallapopApi(httpClient, config, httpClientHandler);
            var market = "\"es\"";  // string | Market: es (Spain), it (Italy), pt (Portugal) (optional)  (default to "es")

            try
            {
                // List categories
                Object result = apiInstance.WallapopListCategories(market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WallapopApi.WallapopListCategories: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WallapopListCategoriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List categories
    ApiResponse<Object> response = apiInstance.WallapopListCategoriesWithHttpInfo(market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WallapopApi.WallapopListCategoriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **market** | **string** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;] |

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

<a id="wallapoplistfilteroptions"></a>
# **WallapopListFilterOptions**
> Object WallapopListFilterOptions (string filterId, int? categoryId = null, string query = null, string market = null)

List filter options

Long option lists (e.g. brand, model) for filters flagged options_endpoint.

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
    public class WallapopListFilterOptionsExample
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
            var apiInstance = new WallapopApi(httpClient, config, httpClientHandler);
            var filterId = "filterId_example";  // string | 
            var categoryId = 56;  // int? | Category to scope options to (optional) 
            var query = "query_example";  // string | Search text to scope options to (optional) 
            var market = "\"es\"";  // string | Market: es (Spain), it (Italy), pt (Portugal) (optional)  (default to "es")

            try
            {
                // List filter options
                Object result = apiInstance.WallapopListFilterOptions(filterId, categoryId, query, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WallapopApi.WallapopListFilterOptions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WallapopListFilterOptionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List filter options
    ApiResponse<Object> response = apiInstance.WallapopListFilterOptionsWithHttpInfo(filterId, categoryId, query, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WallapopApi.WallapopListFilterOptionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **filterId** | **string** |  |  |
| **categoryId** | **int?** | Category to scope options to | [optional]  |
| **query** | **string** | Search text to scope options to | [optional]  |
| **market** | **string** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;] |

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

<a id="wallapoplistmarkets"></a>
# **WallapopListMarkets**
> Object WallapopListMarkets ()

List markets

Supported Wallapop markets and their default search location.

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
    public class WallapopListMarketsExample
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
            var apiInstance = new WallapopApi(httpClient, config, httpClientHandler);

            try
            {
                // List markets
                Object result = apiInstance.WallapopListMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WallapopApi.WallapopListMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WallapopListMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<Object> response = apiInstance.WallapopListMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WallapopApi.WallapopListMarketsWithHttpInfo: " + e.Message);
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

<a id="wallapoplistsearchfilters"></a>
# **WallapopListSearchFilters**
> Object WallapopListSearchFilters (int? categoryId = null, string query = null, string market = null)

List search filters

The filters Wallapop offers for a category or query, with option ids.

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
    public class WallapopListSearchFiltersExample
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
            var apiInstance = new WallapopApi(httpClient, config, httpClientHandler);
            var categoryId = 56;  // int? | Category the filters apply to (optional) 
            var query = "query_example";  // string | Search text the filters apply to (optional) 
            var market = "\"es\"";  // string | Market: es (Spain), it (Italy), pt (Portugal) (optional)  (default to "es")

            try
            {
                // List search filters
                Object result = apiInstance.WallapopListSearchFilters(categoryId, query, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WallapopApi.WallapopListSearchFilters: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WallapopListSearchFiltersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List search filters
    ApiResponse<Object> response = apiInstance.WallapopListSearchFiltersWithHttpInfo(categoryId, query, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WallapopApi.WallapopListSearchFiltersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **categoryId** | **int?** | Category the filters apply to | [optional]  |
| **query** | **string** | Search text the filters apply to | [optional]  |
| **market** | **string** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;] |

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

<a id="wallapopsearchlistings"></a>
# **WallapopSearchListings**
> Object WallapopSearchListings (string query = null, string market = null, decimal? latitude = null, decimal? longitude = null, int? distanceKm = null, int? categoryId = null, decimal? minPrice = null, decimal? maxPrice = null, string condition = null, string brand = null, string model = null, string color = null, string timeFilter = null, bool? shippable = null, bool? hasWarranty = null, bool? refurbished = null, int? minYear = null, int? maxYear = null, int? minKm = null, int? maxKm = null, string gearbox = null, int? minHorsepower = null, int? maxHorsepower = null, string orderBy = null, string nextPage = null)

Search listings

Search Wallapop listings (40 per page). Needs a query, a category_id, or both.

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
    public class WallapopSearchListingsExample
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
            var apiInstance = new WallapopApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search text, e.g. 'iphone 14' (optional) 
            var market = "\"es\"";  // string | Market: es (Spain), it (Italy), pt (Portugal) (optional)  (default to "es")
            var latitude = 8.14D;  // decimal? | Search centre latitude (defaults to the market capital) (optional) 
            var longitude = 8.14D;  // decimal? | Search centre longitude (optional) 
            var distanceKm = 56;  // int? | Search radius (optional) 
            var categoryId = 56;  // int? | Category id from /categories (optional) 
            var minPrice = 8.14D;  // decimal? | Minimum price (EUR) (optional) 
            var maxPrice = 8.14D;  // decimal? | Maximum price (EUR) (optional) 
            var condition = "condition_example";  // string | Comma-separated: un_opened, in_box, new, as_good_as_new, good, fair, has_given_it_all (optional) 
            var brand = "brand_example";  // string | Brand, e.g. Apple (optional) 
            var model = "model_example";  // string | Model, e.g. iPhone 14 (optional) 
            var color = "color_example";  // string | Colour id, e.g. black (optional) 
            var timeFilter = "today";  // string | Only listings published within this window (optional) 
            var shippable = false;  // bool? | Only listings that ship (optional)  (default to false)
            var hasWarranty = false;  // bool? | Only listings with a warranty (optional)  (default to false)
            var refurbished = false;  // bool? | Only refurbished listings (optional)  (default to false)
            var minYear = 56;  // int? | Cars: earliest model year (optional) 
            var maxYear = 56;  // int? | Cars: latest model year (optional) 
            var minKm = 56;  // int? | Cars: minimum mileage (optional) 
            var maxKm = 56;  // int? | Cars: maximum mileage (optional) 
            var gearbox = "manual";  // string | Cars (optional) 
            var minHorsepower = 56;  // int? | Cars: minimum power (optional) 
            var maxHorsepower = 56;  // int? | Cars: maximum power (optional) 
            var orderBy = "most_relevance";  // string | Sort order (optional)  (default to most_relevance)
            var nextPage = "nextPage_example";  // string | Cursor from the previous page's next_page; other parameters are then ignored (optional) 

            try
            {
                // Search listings
                Object result = apiInstance.WallapopSearchListings(query, market, latitude, longitude, distanceKm, categoryId, minPrice, maxPrice, condition, brand, model, color, timeFilter, shippable, hasWarranty, refurbished, minYear, maxYear, minKm, maxKm, gearbox, minHorsepower, maxHorsepower, orderBy, nextPage);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WallapopApi.WallapopSearchListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WallapopSearchListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search listings
    ApiResponse<Object> response = apiInstance.WallapopSearchListingsWithHttpInfo(query, market, latitude, longitude, distanceKm, categoryId, minPrice, maxPrice, condition, brand, model, color, timeFilter, shippable, hasWarranty, refurbished, minYear, maxYear, minKm, maxKm, gearbox, minHorsepower, maxHorsepower, orderBy, nextPage);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WallapopApi.WallapopSearchListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search text, e.g. &#39;iphone 14&#39; | [optional]  |
| **market** | **string** | Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to &quot;es&quot;] |
| **latitude** | **decimal?** | Search centre latitude (defaults to the market capital) | [optional]  |
| **longitude** | **decimal?** | Search centre longitude | [optional]  |
| **distanceKm** | **int?** | Search radius | [optional]  |
| **categoryId** | **int?** | Category id from /categories | [optional]  |
| **minPrice** | **decimal?** | Minimum price (EUR) | [optional]  |
| **maxPrice** | **decimal?** | Maximum price (EUR) | [optional]  |
| **condition** | **string** | Comma-separated: un_opened, in_box, new, as_good_as_new, good, fair, has_given_it_all | [optional]  |
| **brand** | **string** | Brand, e.g. Apple | [optional]  |
| **model** | **string** | Model, e.g. iPhone 14 | [optional]  |
| **color** | **string** | Colour id, e.g. black | [optional]  |
| **timeFilter** | **string** | Only listings published within this window | [optional]  |
| **shippable** | **bool?** | Only listings that ship | [optional] [default to false] |
| **hasWarranty** | **bool?** | Only listings with a warranty | [optional] [default to false] |
| **refurbished** | **bool?** | Only refurbished listings | [optional] [default to false] |
| **minYear** | **int?** | Cars: earliest model year | [optional]  |
| **maxYear** | **int?** | Cars: latest model year | [optional]  |
| **minKm** | **int?** | Cars: minimum mileage | [optional]  |
| **maxKm** | **int?** | Cars: maximum mileage | [optional]  |
| **gearbox** | **string** | Cars | [optional]  |
| **minHorsepower** | **int?** | Cars: minimum power | [optional]  |
| **maxHorsepower** | **int?** | Cars: maximum power | [optional]  |
| **orderBy** | **string** | Sort order | [optional] [default to most_relevance] |
| **nextPage** | **string** | Cursor from the previous page&#39;s next_page; other parameters are then ignored | [optional]  |

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

<a id="wallapopwallapopscraperhealthcheck"></a>
# **WallapopWallapopScraperHealthCheck**
> Object WallapopWallapopScraperHealthCheck ()

Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

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
    public class WallapopWallapopScraperHealthCheckExample
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
            var apiInstance = new WallapopApi(httpClient, config, httpClientHandler);

            try
            {
                // Wallapop scraper health check
                Object result = apiInstance.WallapopWallapopScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WallapopApi.WallapopWallapopScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WallapopWallapopScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Wallapop scraper health check
    ApiResponse<Object> response = apiInstance.WallapopWallapopScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WallapopApi.WallapopWallapopScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="wallapopwallapopscraperhealthcheckhead"></a>
# **WallapopWallapopScraperHealthCheckHead**
> Object WallapopWallapopScraperHealthCheckHead ()

Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

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
    public class WallapopWallapopScraperHealthCheckHeadExample
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
            var apiInstance = new WallapopApi(httpClient, config, httpClientHandler);

            try
            {
                // Wallapop scraper health check
                Object result = apiInstance.WallapopWallapopScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WallapopApi.WallapopWallapopScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WallapopWallapopScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Wallapop scraper health check
    ApiResponse<Object> response = apiInstance.WallapopWallapopScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WallapopApi.WallapopWallapopScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

