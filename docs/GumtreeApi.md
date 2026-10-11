# ScrapeBadger.Api.GumtreeApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GumtreeGetListing**](GumtreeApi.md#gumtreegetlisting) | **GET** /v1/gumtree/listings/{listing_id} | Get listing |
| [**GumtreeGetSearchFilters**](GumtreeApi.md#gumtreegetsearchfilters) | **GET** /v1/gumtree/search/filters | Get search filters |
| [**GumtreeGetSellerListings**](GumtreeApi.md#gumtreegetsellerlistings) | **GET** /v1/gumtree/listings/{listing_id}/seller-listings | Get seller listings |
| [**GumtreeGumtreeScraperHealthCheck**](GumtreeApi.md#gumtreegumtreescraperhealthcheck) | **GET** /v1/gumtree/health | Gumtree scraper health check |
| [**GumtreeGumtreeScraperHealthCheckHead**](GumtreeApi.md#gumtreegumtreescraperhealthcheckhead) | **HEAD** /v1/gumtree/health | Gumtree scraper health check |
| [**GumtreeListCategories**](GumtreeApi.md#gumtreelistcategories) | **GET** /v1/gumtree/categories | List categories |
| [**GumtreeListLocations**](GumtreeApi.md#gumtreelistlocations) | **GET** /v1/gumtree/locations | List locations |
| [**GumtreeLocationSuggestions**](GumtreeApi.md#gumtreelocationsuggestions) | **GET** /v1/gumtree/locations/autocomplete | Location suggestions |
| [**GumtreeSearchListings**](GumtreeApi.md#gumtreesearchlistings) | **GET** /v1/gumtree/search | Search listings |
| [**GumtreeSearchSuggestions**](GumtreeApi.md#gumtreesearchsuggestions) | **GET** /v1/gumtree/autocomplete | Search suggestions |

<a id="gumtreegetlisting"></a>
# **GumtreeGetListing**
> Object GumtreeGetListing (string listingId)

Get listing

Full listing — description, attributes, images, seller, similar listings.

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
    public class GumtreeGetListingExample
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
            var apiInstance = new GumtreeApi(httpClient, config, httpClientHandler);
            var listingId = "listingId_example";  // string | Gumtree listing id — the number at the end of a gumtree.com/p/... URL

            try
            {
                // Get listing
                Object result = apiInstance.GumtreeGetListing(listingId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GumtreeApi.GumtreeGetListing: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GumtreeGetListingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get listing
    ApiResponse<Object> response = apiInstance.GumtreeGetListingWithHttpInfo(listingId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GumtreeApi.GumtreeGetListingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listingId** | **string** | Gumtree listing id — the number at the end of a gumtree.com/p/... URL |  |

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

<a id="gumtreegetsearchfilters"></a>
# **GumtreeGetSearchFilters**
> Object GumtreeGetSearchFilters (string category = null, string location = null, string query = null)

Get search filters

Filters, sort orders and radius options for a category, with live counts.

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
    public class GumtreeGetSearchFiltersExample
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
            var apiInstance = new GumtreeApi(httpClient, config, httpClientHandler);
            var category = "\"all\"";  // string | Category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs'. Default 'all'. (optional)  (default to "all")
            var location = "\"uk\"";  // string | Location slug ('london'), town name or UK postcode ('SW1A 1AA'). Default 'uk'. (optional)  (default to "uk")
            var query = "query_example";  // string |  (optional) 

            try
            {
                // Get search filters
                Object result = apiInstance.GumtreeGetSearchFilters(category, location, query);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GumtreeApi.GumtreeGetSearchFilters: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GumtreeGetSearchFiltersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get search filters
    ApiResponse<Object> response = apiInstance.GumtreeGetSearchFiltersWithHttpInfo(category, location, query);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GumtreeApi.GumtreeGetSearchFiltersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **category** | **string** | Category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;. Default &#39;all&#39;. | [optional] [default to &quot;all&quot;] |
| **location** | **string** | Location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). Default &#39;uk&#39;. | [optional] [default to &quot;uk&quot;] |
| **query** | **string** |  | [optional]  |

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

<a id="gumtreegetsellerlistings"></a>
# **GumtreeGetSellerListings**
> Object GumtreeGetSellerListings (string listingId, int? page = null)

Get seller listings

Every live listing by the seller of the given listing.

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
    public class GumtreeGetSellerListingsExample
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
            var apiInstance = new GumtreeApi(httpClient, config, httpClientHandler);
            var listingId = "listingId_example";  // string | Gumtree listing id — the number at the end of a gumtree.com/p/... URL
            var page = 1;  // int? |  (optional)  (default to 1)

            try
            {
                // Get seller listings
                Object result = apiInstance.GumtreeGetSellerListings(listingId, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GumtreeApi.GumtreeGetSellerListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GumtreeGetSellerListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get seller listings
    ApiResponse<Object> response = apiInstance.GumtreeGetSellerListingsWithHttpInfo(listingId, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GumtreeApi.GumtreeGetSellerListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listingId** | **string** | Gumtree listing id — the number at the end of a gumtree.com/p/... URL |  |
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

<a id="gumtreegumtreescraperhealthcheck"></a>
# **GumtreeGumtreeScraperHealthCheck**
> Object GumtreeGumtreeScraperHealthCheck ()

Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

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
    public class GumtreeGumtreeScraperHealthCheckExample
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
            var apiInstance = new GumtreeApi(httpClient, config, httpClientHandler);

            try
            {
                // Gumtree scraper health check
                Object result = apiInstance.GumtreeGumtreeScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GumtreeApi.GumtreeGumtreeScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GumtreeGumtreeScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gumtree scraper health check
    ApiResponse<Object> response = apiInstance.GumtreeGumtreeScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GumtreeApi.GumtreeGumtreeScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="gumtreegumtreescraperhealthcheckhead"></a>
# **GumtreeGumtreeScraperHealthCheckHead**
> Object GumtreeGumtreeScraperHealthCheckHead ()

Gumtree scraper health check

Check health of the Gumtree scraper service (accepts HEAD for UptimeRobot).

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
    public class GumtreeGumtreeScraperHealthCheckHeadExample
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
            var apiInstance = new GumtreeApi(httpClient, config, httpClientHandler);

            try
            {
                // Gumtree scraper health check
                Object result = apiInstance.GumtreeGumtreeScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GumtreeApi.GumtreeGumtreeScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GumtreeGumtreeScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gumtree scraper health check
    ApiResponse<Object> response = apiInstance.GumtreeGumtreeScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GumtreeApi.GumtreeGumtreeScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="gumtreelistcategories"></a>
# **GumtreeListCategories**
> Object GumtreeListCategories (int? parentId = null)

List categories

Browse Gumtree's category tree. A node's `slug` is the `/search` category.

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
    public class GumtreeListCategoriesExample
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
            var apiInstance = new GumtreeApi(httpClient, config, httpClientHandler);
            var parentId = 1;  // int? | Parent category id (default: all) (optional)  (default to 1)

            try
            {
                // List categories
                Object result = apiInstance.GumtreeListCategories(parentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GumtreeApi.GumtreeListCategories: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GumtreeListCategoriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List categories
    ApiResponse<Object> response = apiInstance.GumtreeListCategoriesWithHttpInfo(parentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GumtreeApi.GumtreeListCategoriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **parentId** | **int?** | Parent category id (default: all) | [optional] [default to 1] |

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

<a id="gumtreelistlocations"></a>
# **GumtreeListLocations**
> Object GumtreeListLocations (int? parentId = null)

List locations

Browse Gumtree's location tree.

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
    public class GumtreeListLocationsExample
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
            var apiInstance = new GumtreeApi(httpClient, config, httpClientHandler);
            var parentId = 10000392;  // int? | Parent location id (default: UK) (optional)  (default to 10000392)

            try
            {
                // List locations
                Object result = apiInstance.GumtreeListLocations(parentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GumtreeApi.GumtreeListLocations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GumtreeListLocationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List locations
    ApiResponse<Object> response = apiInstance.GumtreeListLocationsWithHttpInfo(parentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GumtreeApi.GumtreeListLocationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **parentId** | **int?** | Parent location id (default: UK) | [optional] [default to 10000392] |

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

<a id="gumtreelocationsuggestions"></a>
# **GumtreeLocationSuggestions**
> Object GumtreeLocationSuggestions (string query)

Location suggestions

Resolve a place name or postcode to Gumtree locations with coordinates.

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
    public class GumtreeLocationSuggestionsExample
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
            var apiInstance = new GumtreeApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Town or postcode prefix, e.g. 'manch'

            try
            {
                // Location suggestions
                Object result = apiInstance.GumtreeLocationSuggestions(query);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GumtreeApi.GumtreeLocationSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GumtreeLocationSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Location suggestions
    ApiResponse<Object> response = apiInstance.GumtreeLocationSuggestionsWithHttpInfo(query);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GumtreeApi.GumtreeLocationSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Town or postcode prefix, e.g. &#39;manch&#39; |  |

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

<a id="gumtreesearchlistings"></a>
# **GumtreeSearchListings**
> Object GumtreeSearchListings (string query = null, string category = null, string location = null, decimal? distance = null, int? minPrice = null, int? maxPrice = null, string sort = null, string sellerType = null, bool? urgentOnly = null, bool? withPhotos = null, string filters = null, int? page = null)

Search listings

Search gumtree.com listings. ~25-30 per page, up to 50 pages.

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
    public class GumtreeSearchListingsExample
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
            var apiInstance = new GumtreeApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords, e.g. 'mountain bike' (optional) 
            var category = "\"all\"";  // string | Category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs'. Default 'all'. (optional)  (default to "all")
            var location = "\"uk\"";  // string | Location slug ('london'), town name or UK postcode ('SW1A 1AA'). Default 'uk'. (optional)  (default to "uk")
            var distance = 8.14D;  // decimal? | Radius in miles (optional) 
            var minPrice = 56;  // int? | GBP; needs a category (optional) 
            var maxPrice = 56;  // int? | GBP; needs a category (optional) 
            var sort = "relevance";  // string |  (optional) 
            var sellerType = "private";  // string |  (optional) 
            var urgentOnly = false;  // bool? |  (optional)  (default to false)
            var withPhotos = false;  // bool? |  (optional)  (default to false)
            var filters = "filters_example";  // string | Category filters as key:value pairs, e.g. 'vehicle_make:bmw,vehicle_fuel_type:petrol' (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)

            try
            {
                // Search listings
                Object result = apiInstance.GumtreeSearchListings(query, category, location, distance, minPrice, maxPrice, sort, sellerType, urgentOnly, withPhotos, filters, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GumtreeApi.GumtreeSearchListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GumtreeSearchListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search listings
    ApiResponse<Object> response = apiInstance.GumtreeSearchListingsWithHttpInfo(query, category, location, distance, minPrice, maxPrice, sort, sellerType, urgentOnly, withPhotos, filters, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GumtreeApi.GumtreeSearchListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords, e.g. &#39;mountain bike&#39; | [optional]  |
| **category** | **string** | Category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;. Default &#39;all&#39;. | [optional] [default to &quot;all&quot;] |
| **location** | **string** | Location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). Default &#39;uk&#39;. | [optional] [default to &quot;uk&quot;] |
| **distance** | **decimal?** | Radius in miles | [optional]  |
| **minPrice** | **int?** | GBP; needs a category | [optional]  |
| **maxPrice** | **int?** | GBP; needs a category | [optional]  |
| **sort** | **string** |  | [optional]  |
| **sellerType** | **string** |  | [optional]  |
| **urgentOnly** | **bool?** |  | [optional] [default to false] |
| **withPhotos** | **bool?** |  | [optional] [default to false] |
| **filters** | **string** | Category filters as key:value pairs, e.g. &#39;vehicle_make:bmw,vehicle_fuel_type:petrol&#39; | [optional]  |
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

<a id="gumtreesearchsuggestions"></a>
# **GumtreeSearchSuggestions**
> Object GumtreeSearchSuggestions (string query)

Search suggestions

Gumtree search-box keyword suggestions with their categories.

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
    public class GumtreeSearchSuggestionsExample
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
            var apiInstance = new GumtreeApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Partial search term, e.g. 'iph'

            try
            {
                // Search suggestions
                Object result = apiInstance.GumtreeSearchSuggestions(query);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GumtreeApi.GumtreeSearchSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GumtreeSearchSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search suggestions
    ApiResponse<Object> response = apiInstance.GumtreeSearchSuggestionsWithHttpInfo(query);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GumtreeApi.GumtreeSearchSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Partial search term, e.g. &#39;iph&#39; |  |

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

