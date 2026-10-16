# ScrapeBadger.Api.EtsyApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**EtsyGetCategories**](EtsyApi.md#etsygetcategories) | **GET** /v1/etsy/categories | Get categories |
| [**EtsyGetListingDetail**](EtsyApi.md#etsygetlistingdetail) | **GET** /v1/etsy/listings/{listing_id} | Get listing detail |
| [**EtsyGetListingReviews**](EtsyApi.md#etsygetlistingreviews) | **GET** /v1/etsy/listings/{listing_id}/reviews | Get listing reviews |
| [**EtsyGetSearchSuggestions**](EtsyApi.md#etsygetsearchsuggestions) | **GET** /v1/etsy/autocomplete | Get search suggestions |
| [**EtsyGetShopListings**](EtsyApi.md#etsygetshoplistings) | **GET** /v1/etsy/shops/{shop_name}/listings | Get shop listings |
| [**EtsyGetShopProfile**](EtsyApi.md#etsygetshopprofile) | **GET** /v1/etsy/shops/{shop_name} | Get shop profile |
| [**EtsyGetShopReviews**](EtsyApi.md#etsygetshopreviews) | **GET** /v1/etsy/shops/{shop_name}/reviews | Get shop reviews |
| [**EtsySearchListings**](EtsyApi.md#etsysearchlistings) | **GET** /v1/etsy/search | Search listings |

<a id="etsygetcategories"></a>
# **EtsyGetCategories**
> Object EtsyGetCategories (string country = null, string currency = null, string language = null)

Get categories

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
    public class EtsyGetCategoriesExample
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
            var apiInstance = new EtsyApi(httpClient, config, httpClientHandler);
            var country = "\"US\"";  // string |  (optional)  (default to "US")
            var currency = "\"USD\"";  // string |  (optional)  (default to "USD")
            var language = "\"en-US\"";  // string |  (optional)  (default to "en-US")

            try
            {
                // Get categories
                Object result = apiInstance.EtsyGetCategories(country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EtsyApi.EtsyGetCategories: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EtsyGetCategoriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get categories
    ApiResponse<Object> response = apiInstance.EtsyGetCategoriesWithHttpInfo(country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EtsyApi.EtsyGetCategoriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |
| **currency** | **string** |  | [optional] [default to &quot;USD&quot;] |
| **language** | **string** |  | [optional] [default to &quot;en-US&quot;] |

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

<a id="etsygetlistingdetail"></a>
# **EtsyGetListingDetail**
> Object EtsyGetListingDetail (string listingId, string country = null, string currency = null, string language = null)

Get listing detail

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
    public class EtsyGetListingDetailExample
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
            var apiInstance = new EtsyApi(httpClient, config, httpClientHandler);
            var listingId = "listingId_example";  // string | 
            var country = "\"US\"";  // string |  (optional)  (default to "US")
            var currency = "\"USD\"";  // string |  (optional)  (default to "USD")
            var language = "\"en-US\"";  // string |  (optional)  (default to "en-US")

            try
            {
                // Get listing detail
                Object result = apiInstance.EtsyGetListingDetail(listingId, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EtsyApi.EtsyGetListingDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EtsyGetListingDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get listing detail
    ApiResponse<Object> response = apiInstance.EtsyGetListingDetailWithHttpInfo(listingId, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EtsyApi.EtsyGetListingDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listingId** | **string** |  |  |
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |
| **currency** | **string** |  | [optional] [default to &quot;USD&quot;] |
| **language** | **string** |  | [optional] [default to &quot;en-US&quot;] |

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

<a id="etsygetlistingreviews"></a>
# **EtsyGetListingReviews**
> Object EtsyGetListingReviews (string listingId, int? page = null, string sort = null, string country = null, string currency = null, string language = null)

Get listing reviews

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
    public class EtsyGetListingReviewsExample
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
            var apiInstance = new EtsyApi(httpClient, config, httpClientHandler);
            var listingId = "listingId_example";  // string | 
            var page = 1;  // int? |  (optional)  (default to 1)
            var sort = "Relevancy";  // string |  (optional)  (default to Relevancy)
            var country = "\"US\"";  // string |  (optional)  (default to "US")
            var currency = "\"USD\"";  // string |  (optional)  (default to "USD")
            var language = "\"en-US\"";  // string |  (optional)  (default to "en-US")

            try
            {
                // Get listing reviews
                Object result = apiInstance.EtsyGetListingReviews(listingId, page, sort, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EtsyApi.EtsyGetListingReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EtsyGetListingReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get listing reviews
    ApiResponse<Object> response = apiInstance.EtsyGetListingReviewsWithHttpInfo(listingId, page, sort, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EtsyApi.EtsyGetListingReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listingId** | **string** |  |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **sort** | **string** |  | [optional] [default to Relevancy] |
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |
| **currency** | **string** |  | [optional] [default to &quot;USD&quot;] |
| **language** | **string** |  | [optional] [default to &quot;en-US&quot;] |

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

<a id="etsygetsearchsuggestions"></a>
# **EtsyGetSearchSuggestions**
> Object EtsyGetSearchSuggestions (string query, string country = null, string currency = null, string language = null)

Get search suggestions

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
    public class EtsyGetSearchSuggestionsExample
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
            var apiInstance = new EtsyApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | 
            var country = "\"US\"";  // string |  (optional)  (default to "US")
            var currency = "\"USD\"";  // string |  (optional)  (default to "USD")
            var language = "\"en-US\"";  // string |  (optional)  (default to "en-US")

            try
            {
                // Get search suggestions
                Object result = apiInstance.EtsyGetSearchSuggestions(query, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EtsyApi.EtsyGetSearchSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EtsyGetSearchSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get search suggestions
    ApiResponse<Object> response = apiInstance.EtsyGetSearchSuggestionsWithHttpInfo(query, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EtsyApi.EtsyGetSearchSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** |  |  |
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |
| **currency** | **string** |  | [optional] [default to &quot;USD&quot;] |
| **language** | **string** |  | [optional] [default to &quot;en-US&quot;] |

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

<a id="etsygetshoplistings"></a>
# **EtsyGetShopListings**
> Object EtsyGetShopListings (string shopName, int? page = null, string country = null, string currency = null, string language = null)

Get shop listings

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
    public class EtsyGetShopListingsExample
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
            var apiInstance = new EtsyApi(httpClient, config, httpClientHandler);
            var shopName = "shopName_example";  // string | 
            var page = 1;  // int? |  (optional)  (default to 1)
            var country = "\"US\"";  // string |  (optional)  (default to "US")
            var currency = "\"USD\"";  // string |  (optional)  (default to "USD")
            var language = "\"en-US\"";  // string |  (optional)  (default to "en-US")

            try
            {
                // Get shop listings
                Object result = apiInstance.EtsyGetShopListings(shopName, page, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EtsyApi.EtsyGetShopListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EtsyGetShopListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get shop listings
    ApiResponse<Object> response = apiInstance.EtsyGetShopListingsWithHttpInfo(shopName, page, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EtsyApi.EtsyGetShopListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **shopName** | **string** |  |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |
| **currency** | **string** |  | [optional] [default to &quot;USD&quot;] |
| **language** | **string** |  | [optional] [default to &quot;en-US&quot;] |

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

<a id="etsygetshopprofile"></a>
# **EtsyGetShopProfile**
> Object EtsyGetShopProfile (string shopName, string country = null, string currency = null, string language = null)

Get shop profile

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
    public class EtsyGetShopProfileExample
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
            var apiInstance = new EtsyApi(httpClient, config, httpClientHandler);
            var shopName = "shopName_example";  // string | 
            var country = "\"US\"";  // string |  (optional)  (default to "US")
            var currency = "\"USD\"";  // string |  (optional)  (default to "USD")
            var language = "\"en-US\"";  // string |  (optional)  (default to "en-US")

            try
            {
                // Get shop profile
                Object result = apiInstance.EtsyGetShopProfile(shopName, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EtsyApi.EtsyGetShopProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EtsyGetShopProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get shop profile
    ApiResponse<Object> response = apiInstance.EtsyGetShopProfileWithHttpInfo(shopName, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EtsyApi.EtsyGetShopProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **shopName** | **string** |  |  |
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |
| **currency** | **string** |  | [optional] [default to &quot;USD&quot;] |
| **language** | **string** |  | [optional] [default to &quot;en-US&quot;] |

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

<a id="etsygetshopreviews"></a>
# **EtsyGetShopReviews**
> Object EtsyGetShopReviews (string shopName, int? page = null, string country = null, string currency = null, string language = null)

Get shop reviews

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
    public class EtsyGetShopReviewsExample
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
            var apiInstance = new EtsyApi(httpClient, config, httpClientHandler);
            var shopName = "shopName_example";  // string | 
            var page = 1;  // int? |  (optional)  (default to 1)
            var country = "\"US\"";  // string |  (optional)  (default to "US")
            var currency = "\"USD\"";  // string |  (optional)  (default to "USD")
            var language = "\"en-US\"";  // string |  (optional)  (default to "en-US")

            try
            {
                // Get shop reviews
                Object result = apiInstance.EtsyGetShopReviews(shopName, page, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EtsyApi.EtsyGetShopReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EtsyGetShopReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get shop reviews
    ApiResponse<Object> response = apiInstance.EtsyGetShopReviewsWithHttpInfo(shopName, page, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EtsyApi.EtsyGetShopReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **shopName** | **string** |  |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |
| **currency** | **string** |  | [optional] [default to &quot;USD&quot;] |
| **language** | **string** |  | [optional] [default to &quot;en-US&quot;] |

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

<a id="etsysearchlistings"></a>
# **EtsySearchListings**
> Object EtsySearchListings (string query, int? page = null, string country = null, string currency = null, string language = null, string sort = null, decimal? minPrice = null, decimal? maxPrice = null)

Search listings

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
    public class EtsySearchListingsExample
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
            var apiInstance = new EtsyApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | 
            var page = 1;  // int? |  (optional)  (default to 1)
            var country = "\"US\"";  // string |  (optional)  (default to "US")
            var currency = "\"USD\"";  // string |  (optional)  (default to "USD")
            var language = "\"en-US\"";  // string |  (optional)  (default to "en-US")
            var sort = "most_relevant";  // string |  (optional)  (default to most_relevant)
            var minPrice = 8.14D;  // decimal? |  (optional) 
            var maxPrice = 8.14D;  // decimal? |  (optional) 

            try
            {
                // Search listings
                Object result = apiInstance.EtsySearchListings(query, page, country, currency, language, sort, minPrice, maxPrice);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EtsyApi.EtsySearchListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the EtsySearchListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search listings
    ApiResponse<Object> response = apiInstance.EtsySearchListingsWithHttpInfo(query, page, country, currency, language, sort, minPrice, maxPrice);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EtsyApi.EtsySearchListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** |  |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |
| **currency** | **string** |  | [optional] [default to &quot;USD&quot;] |
| **language** | **string** |  | [optional] [default to &quot;en-US&quot;] |
| **sort** | **string** |  | [optional] [default to most_relevant] |
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

