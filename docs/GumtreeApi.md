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
| [**GumtreeListMarkets**](GumtreeApi.md#gumtreelistmarkets) | **GET** /v1/gumtree/markets | List markets |
| [**GumtreeLocationSuggestions**](GumtreeApi.md#gumtreelocationsuggestions) | **GET** /v1/gumtree/locations/autocomplete | Location suggestions |
| [**GumtreeSearchListings**](GumtreeApi.md#gumtreesearchlistings) | **GET** /v1/gumtree/search | Search listings |
| [**GumtreeSearchSuggestions**](GumtreeApi.md#gumtreesearchsuggestions) | **GET** /v1/gumtree/autocomplete | Search suggestions |

<a id="gumtreegetlisting"></a>
# **GumtreeGetListing**
> Object GumtreeGetListing (string listingId, string market = null)

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
            var listingId = "listingId_example";  // string | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one)
            var market = "uk";  // string | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional)  (default to uk)

            try
            {
                // Get listing
                Object result = apiInstance.GumtreeGetListing(listingId, market);
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
    ApiResponse<Object> response = apiInstance.GumtreeGetListingWithHttpInfo(listingId, market);
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
| **listingId** | **string** | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one) |  |
| **market** | **string** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] |

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
> Object GumtreeGetSearchFilters (string category = null, string location = null, string query = null, string filters = null, string market = null)

Get search filters

Filters, sort orders and radius options for a category, with live counts.  Feed a `key` and a `value` back into `/search` as `filters=key:value`.

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
            var category = "\"all\"";  // string | uk: category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs', 'bicycles'. au/za: numeric category id, e.g. '18320' (au cars) or '9077' (za cars). Use /categories to browse the tree. Default 'all'. (optional)  (default to "all")
            var location = "location_example";  // string | uk: location slug ('london'), town name or UK postcode ('SW1A 1AA'). au/za: numeric location id, e.g. '3003435' (au Sydney) or '3100003' (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. (optional) 
            var query = "query_example";  // string | Optional keywords to scope the counts (optional) 
            var filters = "filters_example";  // string | za only: filters already applied (e.g. 'ma:toyota' to list Toyota models) (optional) 
            var market = "uk";  // string | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional)  (default to uk)

            try
            {
                // Get search filters
                Object result = apiInstance.GumtreeGetSearchFilters(category, location, query, filters, market);
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
    ApiResponse<Object> response = apiInstance.GumtreeGetSearchFiltersWithHttpInfo(category, location, query, filters, market);
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
| **category** | **string** | uk: category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;, &#39;bicycles&#39;. au/za: numeric category id, e.g. &#39;18320&#39; (au cars) or &#39;9077&#39; (za cars). Use /categories to browse the tree. Default &#39;all&#39;. | [optional] [default to &quot;all&quot;] |
| **location** | **string** | uk: location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). au/za: numeric location id, e.g. &#39;3003435&#39; (au Sydney) or &#39;3100003&#39; (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. | [optional]  |
| **query** | **string** | Optional keywords to scope the counts | [optional]  |
| **filters** | **string** | za only: filters already applied (e.g. &#39;ma:toyota&#39; to list Toyota models) | [optional]  |
| **market** | **string** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] |

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
> Object GumtreeGetSellerListings (string listingId, int? page = null, string market = null)

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
            var listingId = "listingId_example";  // string | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one)
            var page = 1;  // int? |  (optional)  (default to 1)
            var market = "uk";  // string | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional)  (default to uk)

            try
            {
                // Get seller listings
                Object result = apiInstance.GumtreeGetSellerListings(listingId, page, market);
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
    ApiResponse<Object> response = apiInstance.GumtreeGetSellerListingsWithHttpInfo(listingId, page, market);
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
| **listingId** | **string** | Gumtree listing id — the number at the end of the listing URL (uk/au: ~10 digits; za: the full 26-digit ad id, not the short one) |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **market** | **string** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] |

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
> Object GumtreeListCategories (int? parentId = null, string market = null)

List categories

Browse Gumtree's category tree.  A node's `slug` (uk) or `id` (au/za) is the `/search` category.

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
            var parentId = 56;  // int? | Category id to list the children of (default: all) (optional) 
            var market = "uk";  // string | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional)  (default to uk)

            try
            {
                // List categories
                Object result = apiInstance.GumtreeListCategories(parentId, market);
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
    ApiResponse<Object> response = apiInstance.GumtreeListCategoriesWithHttpInfo(parentId, market);
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
| **parentId** | **int?** | Category id to list the children of (default: all) | [optional]  |
| **market** | **string** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] |

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
> Object GumtreeListLocations (int? parentId = null, string market = null)

List locations

Browse Gumtree's location tree.  uk: UK -> nations -> counties -> towns. au: states -> regions -> areas, each with its live ad count. za: provinces -> towns.

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
            var parentId = 56;  // int? | Location id to list the children of (default: the whole country) (optional) 
            var market = "uk";  // string | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional)  (default to uk)

            try
            {
                // List locations
                Object result = apiInstance.GumtreeListLocations(parentId, market);
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
    ApiResponse<Object> response = apiInstance.GumtreeListLocationsWithHttpInfo(parentId, market);
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
| **parentId** | **int?** | Location id to list the children of (default: the whole country) | [optional]  |
| **market** | **string** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] |

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

<a id="gumtreelistmarkets"></a>
# **GumtreeListMarkets**
> Object GumtreeListMarkets ()

List markets

The Gumtree sites this API covers (uk, au, za) with currency and id formats.

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
    public class GumtreeListMarketsExample
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
                // List markets
                Object result = apiInstance.GumtreeListMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GumtreeApi.GumtreeListMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GumtreeListMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<Object> response = apiInstance.GumtreeListMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GumtreeApi.GumtreeListMarketsWithHttpInfo: " + e.Message);
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

<a id="gumtreelocationsuggestions"></a>
# **GumtreeLocationSuggestions**
> Object GumtreeLocationSuggestions (string query, string market = null)

Location suggestions

Resolve a place name or postcode to Gumtree location ids (uk: with coordinates).  The `id` (au/za) or `name` (uk) is what `/search` takes as `location`.

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
            var query = "query_example";  // string | Town, area or postcode prefix, e.g. 'manch' or 'SW1A'
            var market = "uk";  // string | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional)  (default to uk)

            try
            {
                // Location suggestions
                Object result = apiInstance.GumtreeLocationSuggestions(query, market);
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
    ApiResponse<Object> response = apiInstance.GumtreeLocationSuggestionsWithHttpInfo(query, market);
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
| **query** | **string** | Town, area or postcode prefix, e.g. &#39;manch&#39; or &#39;SW1A&#39; |  |
| **market** | **string** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] |

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
> Object GumtreeSearchListings (string query = null, string category = null, string location = null, decimal? distance = null, int? minPrice = null, int? maxPrice = null, string sort = null, string sellerType = null, bool? urgentOnly = null, bool? withPhotos = null, string filters = null, int? page = null, string market = null)

Search listings

Search Gumtree listings in the UK, Australia or South Africa.  Up to 50 pages. Page size: uk 25, au 24 (plus up to 6 featured top ads), za 20.

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
            var category = "\"all\"";  // string | uk: category slug, e.g. 'cars', 'for-sale', 'property-to-rent', 'jobs', 'bicycles'. au/za: numeric category id, e.g. '18320' (au cars) or '9077' (za cars). Use /categories to browse the tree. Default 'all'. (optional)  (default to "all")
            var location = "location_example";  // string | uk: location slug ('london'), town name or UK postcode ('SW1A 1AA'). au/za: numeric location id, e.g. '3003435' (au Sydney) or '3100003' (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. (optional) 
            var distance = 8.14D;  // decimal? | Radius around `location`: miles (uk) or km (au). Not offered by za. (optional) 
            var minPrice = 56;  // int? | Minimum price in the market's currency (uk: needs a category, not 'all') (optional) 
            var maxPrice = 56;  // int? | Maximum price in the market's currency (uk: needs a category, not 'all') (optional) 
            var sort = "relevance";  // string | Result ordering (default relevance). 'distance' needs uk, or au with a location. (optional) 
            var sellerType = "private";  // string | uk/za: 'trade' covers dealers, agencies and recruiters. au: not supported — use a category filter such as 'cars.forsaleby_s:ownr'. (optional) 
            var urgentOnly = false;  // bool? | uk only: only ads marked urgent (optional)  (default to false)
            var withPhotos = false;  // bool? | uk only: only ads with photos (optional)  (default to false)
            var filters = "filters_example";  // string | Category-specific filters as comma-separated key:value pairs, e.g. 'vehicle_make:bmw,vehicle_fuel_type:petrol,min_vehicle_mileage:10000' (uk), 'cars.carmake_s:toyota,cars.forsaleby_s:ownr' (au) or 'ma:toyota,fu:petrol,max_km:100000' (za). Range filters take min_<key>/max_<key>. Discover keys and values with /search/filters for the same market. (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)
            var market = "uk";  // string | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional)  (default to uk)

            try
            {
                // Search listings
                Object result = apiInstance.GumtreeSearchListings(query, category, location, distance, minPrice, maxPrice, sort, sellerType, urgentOnly, withPhotos, filters, page, market);
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
    ApiResponse<Object> response = apiInstance.GumtreeSearchListingsWithHttpInfo(query, category, location, distance, minPrice, maxPrice, sort, sellerType, urgentOnly, withPhotos, filters, page, market);
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
| **category** | **string** | uk: category slug, e.g. &#39;cars&#39;, &#39;for-sale&#39;, &#39;property-to-rent&#39;, &#39;jobs&#39;, &#39;bicycles&#39;. au/za: numeric category id, e.g. &#39;18320&#39; (au cars) or &#39;9077&#39; (za cars). Use /categories to browse the tree. Default &#39;all&#39;. | [optional] [default to &quot;all&quot;] |
| **location** | **string** | uk: location slug (&#39;london&#39;), town name or UK postcode (&#39;SW1A 1AA&#39;). au/za: numeric location id, e.g. &#39;3003435&#39; (au Sydney) or &#39;3100003&#39; (za Gauteng). Use /locations/autocomplete to resolve one. Default: the whole country. | [optional]  |
| **distance** | **decimal?** | Radius around &#x60;location&#x60;: miles (uk) or km (au). Not offered by za. | [optional]  |
| **minPrice** | **int?** | Minimum price in the market&#39;s currency (uk: needs a category, not &#39;all&#39;) | [optional]  |
| **maxPrice** | **int?** | Maximum price in the market&#39;s currency (uk: needs a category, not &#39;all&#39;) | [optional]  |
| **sort** | **string** | Result ordering (default relevance). &#39;distance&#39; needs uk, or au with a location. | [optional]  |
| **sellerType** | **string** | uk/za: &#39;trade&#39; covers dealers, agencies and recruiters. au: not supported — use a category filter such as &#39;cars.forsaleby_s:ownr&#39;. | [optional]  |
| **urgentOnly** | **bool?** | uk only: only ads marked urgent | [optional] [default to false] |
| **withPhotos** | **bool?** | uk only: only ads with photos | [optional] [default to false] |
| **filters** | **string** | Category-specific filters as comma-separated key:value pairs, e.g. &#39;vehicle_make:bmw,vehicle_fuel_type:petrol,min_vehicle_mileage:10000&#39; (uk), &#39;cars.carmake_s:toyota,cars.forsaleby_s:ownr&#39; (au) or &#39;ma:toyota,fu:petrol,max_km:100000&#39; (za). Range filters take min_&lt;key&gt;/max_&lt;key&gt;. Discover keys and values with /search/filters for the same market. | [optional]  |
| **page** | **int?** |  | [optional] [default to 1] |
| **market** | **string** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] |

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
> Object GumtreeSearchSuggestions (string query, string market = null)

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
            var market = "uk";  // string | Which Gumtree: 'uk' (gumtree.com, GBP), 'au' (gumtree.com.au, AUD) or 'za' (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. (optional)  (default to uk)

            try
            {
                // Search suggestions
                Object result = apiInstance.GumtreeSearchSuggestions(query, market);
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
    ApiResponse<Object> response = apiInstance.GumtreeSearchSuggestionsWithHttpInfo(query, market);
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
| **market** | **string** | Which Gumtree: &#39;uk&#39; (gumtree.com, GBP), &#39;au&#39; (gumtree.com.au, AUD) or &#39;za&#39; (gumtree.co.za, ZAR). Separate sites — ids from one market mean nothing in another. | [optional] [default to uk] |

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

