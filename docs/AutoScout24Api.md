# ScrapeBadger.Api.AutoScout24Api

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**Autoscout24CheckAutoscout24Health**](AutoScout24Api.md#autoscout24checkautoscout24health) | **GET** /v1/autoscout24/health | Check AutoScout24 health |
| [**Autoscout24GetListing**](AutoScout24Api.md#autoscout24getlisting) | **GET** /v1/autoscout24/listing | Get listing |
| [**Autoscout24ListMarkets**](AutoScout24Api.md#autoscout24listmarkets) | **GET** /v1/autoscout24/markets | List markets |
| [**Autoscout24ListSearchFilters**](AutoScout24Api.md#autoscout24listsearchfilters) | **GET** /v1/autoscout24/filters | List search filters |
| [**Autoscout24SearchVehicles**](AutoScout24Api.md#autoscout24searchvehicles) | **GET** /v1/autoscout24/search | Search vehicles |

<a id="autoscout24checkautoscout24health"></a>
# **Autoscout24CheckAutoscout24Health**
> Object Autoscout24CheckAutoscout24Health ()

Check AutoScout24 health

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
    public class Autoscout24CheckAutoscout24HealthExample
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
            var apiInstance = new AutoScout24Api(httpClient, config, httpClientHandler);

            try
            {
                // Check AutoScout24 health
                Object result = apiInstance.Autoscout24CheckAutoscout24Health();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutoScout24Api.Autoscout24CheckAutoscout24Health: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the Autoscout24CheckAutoscout24HealthWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Check AutoScout24 health
    ApiResponse<Object> response = apiInstance.Autoscout24CheckAutoscout24HealthWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutoScout24Api.Autoscout24CheckAutoscout24HealthWithHttpInfo: " + e.Message);
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

<a id="autoscout24getlisting"></a>
# **Autoscout24GetListing**
> AutoScout24ListingResponse Autoscout24GetListing (string url = null, string listingId = null, string market = null)

Get listing

Full public vehicle specifications, equipment, photos, price and seller data.  Exactly one of url or listing_id is required. Supported markets match /markets. Successful detail costs 10 credits; removed or missing listings return an unbilled 404. Invalid inputs return 422 and source failures 503.

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
    public class Autoscout24GetListingExample
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
            var apiInstance = new AutoScout24Api(httpClient, config, httpClientHandler);
            var url = "url_example";  // string | Full HTTPS listing URL from search results. Supply url or listing_id, not both. (optional) 
            var listingId = "listingId_example";  // string | Listing UUID from search results; requires no SEO slug. (optional) 
            var market = "de";  // string | Inferred from URL, otherwise de. Explicit market must match the URL host. (optional) 

            try
            {
                // Get listing
                AutoScout24ListingResponse result = apiInstance.Autoscout24GetListing(url, listingId, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutoScout24Api.Autoscout24GetListing: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the Autoscout24GetListingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get listing
    ApiResponse<AutoScout24ListingResponse> response = apiInstance.Autoscout24GetListingWithHttpInfo(url, listingId, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutoScout24Api.Autoscout24GetListingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **url** | **string** | Full HTTPS listing URL from search results. Supply url or listing_id, not both. | [optional]  |
| **listingId** | **string** | Listing UUID from search results; requires no SEO slug. | [optional]  |
| **market** | **string** | Inferred from URL, otherwise de. Explicit market must match the URL host. | [optional]  |

### Return type

[**AutoScout24ListingResponse**](AutoScout24ListingResponse.md)

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

<a id="autoscout24listmarkets"></a>
# **Autoscout24ListMarkets**
> AutoScout24MarketsResponse Autoscout24ListMarkets ()

List markets

Verified marketplaces, domains, languages and currency. Free reference endpoint.

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
    public class Autoscout24ListMarketsExample
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
            var apiInstance = new AutoScout24Api(httpClient, config, httpClientHandler);

            try
            {
                // List markets
                AutoScout24MarketsResponse result = apiInstance.Autoscout24ListMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutoScout24Api.Autoscout24ListMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the Autoscout24ListMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<AutoScout24MarketsResponse> response = apiInstance.Autoscout24ListMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutoScout24Api.Autoscout24ListMarketsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**AutoScout24MarketsResponse**](AutoScout24MarketsResponse.md)

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

<a id="autoscout24listsearchfilters"></a>
# **Autoscout24ListSearchFilters**
> AutoScout24FiltersResponse Autoscout24ListSearchFilters (string market = null, string make = null)

List search filters

Current native make, model and vehicle filter options. Set make for its models.

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
    public class Autoscout24ListSearchFiltersExample
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
            var apiInstance = new AutoScout24Api(httpClient, config, httpClientHandler);
            var market = "de";  // string |  (optional)  (default to de)
            var make = "make_example";  // string |  (optional) 

            try
            {
                // List search filters
                AutoScout24FiltersResponse result = apiInstance.Autoscout24ListSearchFilters(market, make);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutoScout24Api.Autoscout24ListSearchFilters: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the Autoscout24ListSearchFiltersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List search filters
    ApiResponse<AutoScout24FiltersResponse> response = apiInstance.Autoscout24ListSearchFiltersWithHttpInfo(market, make);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutoScout24Api.Autoscout24ListSearchFiltersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **market** | **string** |  | [optional] [default to de] |
| **make** | **string** |  | [optional]  |

### Return type

[**AutoScout24FiltersResponse**](AutoScout24FiltersResponse.md)

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

<a id="autoscout24searchvehicles"></a>
# **Autoscout24SearchVehicles**
> AutoScout24SearchResponse Autoscout24SearchVehicles (string market = null, string make = null, string model = null, int? priceMin = null, int? priceMax = null, int? mileageMin = null, int? mileageMax = null, int? yearMin = null, int? yearMax = null, int? powerMin = null, int? powerMax = null, string fuelType = null, string transmission = null, string bodyType = null, string sellerType = null, string condition = null, string zip = null, int? radius = null, string sortBy = null, int? page = null)

Search vehicles

Search live vehicle cards, seller/location information and current filter taxonomy.  Browsing is capped at 200 pages (normally 20 cards each). Narrow the query to reach more inventory. Empty results cost zero credits. Pass a result's url or id to /listing for its full specifications and equipment.

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
    public class Autoscout24SearchVehiclesExample
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
            var apiInstance = new AutoScout24Api(httpClient, config, httpClientHandler);
            var market = "de";  // string |  (optional)  (default to de)
            var make = "make_example";  // string | Native make slug, e.g. volkswagen or bmw. (optional) 
            var model = "model_example";  // string | Native model slug, e.g. golf. Requires make. (optional) 
            var priceMin = 56;  // int? |  (optional) 
            var priceMax = 56;  // int? |  (optional) 
            var mileageMin = 56;  // int? | Kilometres. (optional) 
            var mileageMax = 56;  // int? |  (optional) 
            var yearMin = 56;  // int? |  (optional) 
            var yearMax = 56;  // int? |  (optional) 
            var powerMin = 56;  // int? | Engine power in kW. (optional) 
            var powerMax = 56;  // int? |  (optional) 
            var fuelType = "petrol";  // string |  (optional) 
            var transmission = "automatic";  // string |  (optional) 
            var bodyType = "compact";  // string |  (optional) 
            var sellerType = "dealer";  // string |  (optional) 
            var condition = "new";  // string |  (optional) 
            var zip = "zip_example";  // string | Postal code in the requested market. (optional) 
            var radius = 56;  // int? | Kilometres; requires zip. (optional) 
            var sortBy = "best_match";  // string |  (optional)  (default to best_match)
            var page = 1;  // int? |  (optional)  (default to 1)

            try
            {
                // Search vehicles
                AutoScout24SearchResponse result = apiInstance.Autoscout24SearchVehicles(market, make, model, priceMin, priceMax, mileageMin, mileageMax, yearMin, yearMax, powerMin, powerMax, fuelType, transmission, bodyType, sellerType, condition, zip, radius, sortBy, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AutoScout24Api.Autoscout24SearchVehicles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the Autoscout24SearchVehiclesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search vehicles
    ApiResponse<AutoScout24SearchResponse> response = apiInstance.Autoscout24SearchVehiclesWithHttpInfo(market, make, model, priceMin, priceMax, mileageMin, mileageMax, yearMin, yearMax, powerMin, powerMax, fuelType, transmission, bodyType, sellerType, condition, zip, radius, sortBy, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AutoScout24Api.Autoscout24SearchVehiclesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **market** | **string** |  | [optional] [default to de] |
| **make** | **string** | Native make slug, e.g. volkswagen or bmw. | [optional]  |
| **model** | **string** | Native model slug, e.g. golf. Requires make. | [optional]  |
| **priceMin** | **int?** |  | [optional]  |
| **priceMax** | **int?** |  | [optional]  |
| **mileageMin** | **int?** | Kilometres. | [optional]  |
| **mileageMax** | **int?** |  | [optional]  |
| **yearMin** | **int?** |  | [optional]  |
| **yearMax** | **int?** |  | [optional]  |
| **powerMin** | **int?** | Engine power in kW. | [optional]  |
| **powerMax** | **int?** |  | [optional]  |
| **fuelType** | **string** |  | [optional]  |
| **transmission** | **string** |  | [optional]  |
| **bodyType** | **string** |  | [optional]  |
| **sellerType** | **string** |  | [optional]  |
| **condition** | **string** |  | [optional]  |
| **zip** | **string** | Postal code in the requested market. | [optional]  |
| **radius** | **int?** | Kilometres; requires zip. | [optional]  |
| **sortBy** | **string** |  | [optional] [default to best_match] |
| **page** | **int?** |  | [optional] [default to 1] |

### Return type

[**AutoScout24SearchResponse**](AutoScout24SearchResponse.md)

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

