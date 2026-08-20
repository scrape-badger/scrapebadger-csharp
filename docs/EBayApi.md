# ScrapeBadger.Api.EBayApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**EbayBrowseACategory**](EBayApi.md#ebaybrowseacategory) | **GET** /v1/ebay/categories/{category_id}/items | Browse a category |
| [**EbayCompletedSoldListings**](EBayApi.md#ebaycompletedsoldlistings) | **GET** /v1/ebay/completed | Completed / sold listings |
| [**EbayEbayScraperHealthCheck**](EBayApi.md#ebayebayscraperhealthcheck) | **GET** /v1/ebay/health | eBay scraper health check |
| [**EbayEbayScraperHealthCheckHead**](EBayApi.md#ebayebayscraperhealthcheckhead) | **HEAD** /v1/ebay/health | eBay scraper health check |
| [**EbayGetItemDetail**](EBayApi.md#ebaygetitemdetail) | **GET** /v1/ebay/items/{item_id} | Get item detail |
| [**EbayGetItemReviews**](EBayApi.md#ebaygetitemreviews) | **GET** /v1/ebay/items/{item_id}/reviews | Get item reviews |
| [**EbayGetSellerFeedback**](EBayApi.md#ebaygetsellerfeedback) | **GET** /v1/ebay/sellers/{username}/feedback | Get seller feedback |
| [**EbayGetSellerListings**](EBayApi.md#ebaygetsellerlistings) | **GET** /v1/ebay/sellers/{username}/items | Get seller listings |
| [**EbayGetSellerProfile**](EBayApi.md#ebaygetsellerprofile) | **GET** /v1/ebay/sellers/{username} | Get seller profile |
| [**EbayKeywordSuggestions**](EBayApi.md#ebaykeywordsuggestions) | **GET** /v1/ebay/autocomplete | Keyword suggestions |
| [**EbayListCategories**](EBayApi.md#ebaylistcategories) | **GET** /v1/ebay/categories | List categories |
| [**EbayListMarkets**](EBayApi.md#ebaylistmarkets) | **GET** /v1/ebay/markets | List markets |
| [**EbaySearchListings**](EBayApi.md#ebaysearchlistings) | **GET** /v1/ebay/search | Search listings |

<a id="ebaybrowseacategory"></a>
# **EbayBrowseACategory**
> Object EbayBrowseACategory (string categoryId, string domain = null, int? page = null, int? perPage = null, string sortBy = null, decimal? minPrice = null, decimal? maxPrice = null)

Browse a category

List active listings within an eBay category.

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
    public class EbayBrowseACategoryExample
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
            var apiInstance = new EBayApi(httpClient, config, httpClientHandler);
            var categoryId = "categoryId_example";  // string | 
            var domain = "\"com\"";  // string |  (optional)  (default to "com")
            var page = 1;  // int? |  (optional)  (default to 1)
            var perPage = 56;  // int? |  (optional) 
            var sortBy = "\"best_match\"";  // string | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low (optional)  (default to "best_match")
            var minPrice = 8.14D;  // decimal? |  (optional) 
            var maxPrice = 8.14D;  // decimal? |  (optional) 

            try
            {
                // Browse a category
                Object result = apiInstance.EbayBrowseACategory(categoryId, domain, page, perPage, sortBy, minPrice, maxPrice);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EBayApi.EbayBrowseACategory: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbayBrowseACategoryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Browse a category
    ApiResponse<Object> response = apiInstance.EbayBrowseACategoryWithHttpInfo(categoryId, domain, page, perPage, sortBy, minPrice, maxPrice);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EBayApi.EbayBrowseACategoryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **categoryId** | **string** |  |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |
| **page** | **int?** |  | [optional] [default to 1] |
| **perPage** | **int?** |  | [optional]  |
| **sortBy** | **string** | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional] [default to &quot;best_match&quot;] |
| **minPrice** | **decimal?** |  | [optional]  |
| **maxPrice** | **decimal?** |  | [optional]  |

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

<a id="ebaycompletedsoldlistings"></a>
# **EbayCompletedSoldListings**
> Object EbayCompletedSoldListings (string query, string domain = null, string categoryId = null, int? page = null, int? perPage = null, string sortBy = null, string condition = null, decimal? minPrice = null, decimal? maxPrice = null)

Completed / sold listings

Search completed/sold listings — eBay's sold-price history.

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
    public class EbayCompletedSoldListingsExample
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
            var apiInstance = new EBayApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords
            var domain = "\"com\"";  // string | Marketplace domain (com, co.uk, de …) (optional)  (default to "com")
            var categoryId = "categoryId_example";  // string | Restrict to a category id (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)
            var perPage = 56;  // int? | 60, 120 or 240 (optional) 
            var sortBy = "\"best_match\"";  // string | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low (optional)  (default to "best_match")
            var condition = "condition_example";  // string | new|open_box|refurbished|used|for_parts (optional) 
            var minPrice = 8.14D;  // decimal? |  (optional) 
            var maxPrice = 8.14D;  // decimal? |  (optional) 

            try
            {
                // Completed / sold listings
                Object result = apiInstance.EbayCompletedSoldListings(query, domain, categoryId, page, perPage, sortBy, condition, minPrice, maxPrice);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EBayApi.EbayCompletedSoldListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbayCompletedSoldListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Completed / sold listings
    ApiResponse<Object> response = apiInstance.EbayCompletedSoldListingsWithHttpInfo(query, domain, categoryId, page, perPage, sortBy, condition, minPrice, maxPrice);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EBayApi.EbayCompletedSoldListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords |  |
| **domain** | **string** | Marketplace domain (com, co.uk, de …) | [optional] [default to &quot;com&quot;] |
| **categoryId** | **string** | Restrict to a category id | [optional]  |
| **page** | **int?** |  | [optional] [default to 1] |
| **perPage** | **int?** | 60, 120 or 240 | [optional]  |
| **sortBy** | **string** | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional] [default to &quot;best_match&quot;] |
| **condition** | **string** | new|open_box|refurbished|used|for_parts | [optional]  |
| **minPrice** | **decimal?** |  | [optional]  |
| **maxPrice** | **decimal?** |  | [optional]  |

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

<a id="ebayebayscraperhealthcheck"></a>
# **EbayEbayScraperHealthCheck**
> Object EbayEbayScraperHealthCheck ()

eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

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
    public class EbayEbayScraperHealthCheckExample
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
            var apiInstance = new EBayApi(httpClient, config, httpClientHandler);

            try
            {
                // eBay scraper health check
                Object result = apiInstance.EbayEbayScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EBayApi.EbayEbayScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbayEbayScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // eBay scraper health check
    ApiResponse<Object> response = apiInstance.EbayEbayScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EBayApi.EbayEbayScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="ebayebayscraperhealthcheckhead"></a>
# **EbayEbayScraperHealthCheckHead**
> Object EbayEbayScraperHealthCheckHead ()

eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

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
    public class EbayEbayScraperHealthCheckHeadExample
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
            var apiInstance = new EBayApi(httpClient, config, httpClientHandler);

            try
            {
                // eBay scraper health check
                Object result = apiInstance.EbayEbayScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EBayApi.EbayEbayScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbayEbayScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // eBay scraper health check
    ApiResponse<Object> response = apiInstance.EbayEbayScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EBayApi.EbayEbayScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="ebaygetitemdetail"></a>
# **EbayGetItemDetail**
> Object EbayGetItemDetail (string itemId, string domain = null)

Get item detail

Get a single eBay listing's full detail.

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
    public class EbayGetItemDetailExample
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
            var apiInstance = new EBayApi(httpClient, config, httpClientHandler);
            var itemId = "itemId_example";  // string | 
            var domain = "\"com\"";  // string |  (optional)  (default to "com")

            try
            {
                // Get item detail
                Object result = apiInstance.EbayGetItemDetail(itemId, domain);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EBayApi.EbayGetItemDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbayGetItemDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get item detail
    ApiResponse<Object> response = apiInstance.EbayGetItemDetailWithHttpInfo(itemId, domain);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EBayApi.EbayGetItemDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **itemId** | **string** |  |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |

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

<a id="ebaygetitemreviews"></a>
# **EbayGetItemReviews**
> Object EbayGetItemReviews (string itemId, string domain = null, int? page = null)

Get item reviews

Get catalog product reviews shown on an eBay listing.

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
    public class EbayGetItemReviewsExample
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
            var apiInstance = new EBayApi(httpClient, config, httpClientHandler);
            var itemId = "itemId_example";  // string | 
            var domain = "\"com\"";  // string |  (optional)  (default to "com")
            var page = 1;  // int? |  (optional)  (default to 1)

            try
            {
                // Get item reviews
                Object result = apiInstance.EbayGetItemReviews(itemId, domain, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EBayApi.EbayGetItemReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbayGetItemReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get item reviews
    ApiResponse<Object> response = apiInstance.EbayGetItemReviewsWithHttpInfo(itemId, domain, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EBayApi.EbayGetItemReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **itemId** | **string** |  |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |
| **page** | **int?** |  | [optional] [default to 1] |

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

<a id="ebaygetsellerfeedback"></a>
# **EbayGetSellerFeedback**
> Object EbayGetSellerFeedback (string username, string domain = null, int? page = null)

Get seller feedback

Get a seller's recent feedback comments.

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
    public class EbayGetSellerFeedbackExample
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
            var apiInstance = new EBayApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var domain = "\"com\"";  // string |  (optional)  (default to "com")
            var page = 1;  // int? |  (optional)  (default to 1)

            try
            {
                // Get seller feedback
                Object result = apiInstance.EbayGetSellerFeedback(username, domain, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EBayApi.EbayGetSellerFeedback: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbayGetSellerFeedbackWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get seller feedback
    ApiResponse<Object> response = apiInstance.EbayGetSellerFeedbackWithHttpInfo(username, domain, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EBayApi.EbayGetSellerFeedbackWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |
| **page** | **int?** |  | [optional] [default to 1] |

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

<a id="ebaygetsellerlistings"></a>
# **EbayGetSellerListings**
> Object EbayGetSellerListings (string username, string domain = null, string query = null, int? page = null, int? perPage = null)

Get seller listings

List the active listings of a single eBay seller.

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
    public class EbayGetSellerListingsExample
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
            var apiInstance = new EBayApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var domain = "\"com\"";  // string |  (optional)  (default to "com")
            var query = "query_example";  // string |  (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)
            var perPage = 56;  // int? |  (optional) 

            try
            {
                // Get seller listings
                Object result = apiInstance.EbayGetSellerListings(username, domain, query, page, perPage);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EBayApi.EbayGetSellerListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbayGetSellerListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get seller listings
    ApiResponse<Object> response = apiInstance.EbayGetSellerListingsWithHttpInfo(username, domain, query, page, perPage);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EBayApi.EbayGetSellerListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |
| **query** | **string** |  | [optional]  |
| **page** | **int?** |  | [optional] [default to 1] |
| **perPage** | **int?** |  | [optional]  |

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

<a id="ebaygetsellerprofile"></a>
# **EbayGetSellerProfile**
> Object EbayGetSellerProfile (string username, string domain = null)

Get seller profile

Get an eBay seller's public profile.

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
    public class EbayGetSellerProfileExample
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
            var apiInstance = new EBayApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var domain = "\"com\"";  // string |  (optional)  (default to "com")

            try
            {
                // Get seller profile
                Object result = apiInstance.EbayGetSellerProfile(username, domain);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EBayApi.EbayGetSellerProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbayGetSellerProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get seller profile
    ApiResponse<Object> response = apiInstance.EbayGetSellerProfileWithHttpInfo(username, domain);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EBayApi.EbayGetSellerProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |

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

<a id="ebaykeywordsuggestions"></a>
# **EbayKeywordSuggestions**
> Object EbayKeywordSuggestions (string query, string domain = null)

Keyword suggestions

Return eBay keyword autocomplete suggestions.

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
    public class EbayKeywordSuggestionsExample
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
            var apiInstance = new EBayApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Partial query prefix
            var domain = "\"com\"";  // string |  (optional)  (default to "com")

            try
            {
                // Keyword suggestions
                Object result = apiInstance.EbayKeywordSuggestions(query, domain);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EBayApi.EbayKeywordSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbayKeywordSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Keyword suggestions
    ApiResponse<Object> response = apiInstance.EbayKeywordSuggestionsWithHttpInfo(query, domain);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EBayApi.EbayKeywordSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Partial query prefix |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |

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

<a id="ebaylistcategories"></a>
# **EbayListCategories**
> Object EbayListCategories ()

List categories

List eBay's top-level category ids.

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
    public class EbayListCategoriesExample
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
            var apiInstance = new EBayApi(httpClient, config, httpClientHandler);

            try
            {
                // List categories
                Object result = apiInstance.EbayListCategories();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EBayApi.EbayListCategories: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbayListCategoriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List categories
    ApiResponse<Object> response = apiInstance.EbayListCategoriesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EBayApi.EbayListCategoriesWithHttpInfo: " + e.Message);
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

<a id="ebaylistmarkets"></a>
# **EbayListMarkets**
> Object EbayListMarkets ()

List markets

List all supported eBay marketplaces.

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
    public class EbayListMarketsExample
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
            var apiInstance = new EBayApi(httpClient, config, httpClientHandler);

            try
            {
                // List markets
                Object result = apiInstance.EbayListMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EBayApi.EbayListMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbayListMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<Object> response = apiInstance.EbayListMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EBayApi.EbayListMarketsWithHttpInfo: " + e.Message);
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

<a id="ebaysearchlistings"></a>
# **EbaySearchListings**
> Object EbaySearchListings (string query, string domain = null, string categoryId = null, int? page = null, int? perPage = null, string sortBy = null, string condition = null, string buyingFormat = null, decimal? minPrice = null, decimal? maxPrice = null, bool? freeShipping = null)

Search listings

Search an eBay marketplace for active listings.

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
    public class EbaySearchListingsExample
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
            var apiInstance = new EBayApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords
            var domain = "\"com\"";  // string | Marketplace domain (com, co.uk, de …) (optional)  (default to "com")
            var categoryId = "categoryId_example";  // string | Restrict to a category id (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)
            var perPage = 56;  // int? | 60, 120 or 240 (optional) 
            var sortBy = "\"best_match\"";  // string | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low (optional)  (default to "best_match")
            var condition = "condition_example";  // string | new|open_box|refurbished|used|for_parts (optional) 
            var buyingFormat = "buyingFormat_example";  // string | auction|buy_it_now|best_offer (optional) 
            var minPrice = 8.14D;  // decimal? |  (optional) 
            var maxPrice = 8.14D;  // decimal? |  (optional) 
            var freeShipping = false;  // bool? |  (optional)  (default to false)

            try
            {
                // Search listings
                Object result = apiInstance.EbaySearchListings(query, domain, categoryId, page, perPage, sortBy, condition, buyingFormat, minPrice, maxPrice, freeShipping);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EBayApi.EbaySearchListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EbaySearchListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search listings
    ApiResponse<Object> response = apiInstance.EbaySearchListingsWithHttpInfo(query, domain, categoryId, page, perPage, sortBy, condition, buyingFormat, minPrice, maxPrice, freeShipping);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EBayApi.EbaySearchListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords |  |
| **domain** | **string** | Marketplace domain (com, co.uk, de …) | [optional] [default to &quot;com&quot;] |
| **categoryId** | **string** | Restrict to a category id | [optional]  |
| **page** | **int?** |  | [optional] [default to 1] |
| **perPage** | **int?** | 60, 120 or 240 | [optional]  |
| **sortBy** | **string** | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional] [default to &quot;best_match&quot;] |
| **condition** | **string** | new|open_box|refurbished|used|for_parts | [optional]  |
| **buyingFormat** | **string** | auction|buy_it_now|best_offer | [optional]  |
| **minPrice** | **decimal?** |  | [optional]  |
| **maxPrice** | **decimal?** |  | [optional]  |
| **freeShipping** | **bool?** |  | [optional] [default to false] |

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

