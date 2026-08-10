# ScrapeBadger.Api.RealtorApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**RealtorGetFullPropertyDetail**](RealtorApi.md#realtorgetfullpropertydetail) | **GET** /v1/realtor/properties/{property_id} | Get full property detail |
| [**RealtorListMarkets**](RealtorApi.md#realtorlistmarkets) | **GET** /v1/realtor/markets | List markets |
| [**RealtorLocationAutocomplete**](RealtorApi.md#realtorlocationautocomplete) | **GET** /v1/realtor/autocomplete | Location autocomplete |
| [**RealtorRealtorScraperHealthCheck**](RealtorApi.md#realtorrealtorscraperhealthcheck) | **GET** /v1/realtor/health | Realtor scraper health check |
| [**RealtorRealtorScraperHealthCheckHead**](RealtorApi.md#realtorrealtorscraperhealthcheckhead) | **HEAD** /v1/realtor/health | Realtor scraper health check |
| [**RealtorSearchPropertyListings**](RealtorApi.md#realtorsearchpropertylistings) | **GET** /v1/realtor/search | Search property listings |

<a id="realtorgetfullpropertydetail"></a>
# **RealtorGetFullPropertyDetail**
> Object RealtorGetFullPropertyDetail (string propertyId, string market = null)

Get full property detail

Full listing detail: features, tax & price history, schools, photos, agents.

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
    public class RealtorGetFullPropertyDetailExample
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
            var apiInstance = new RealtorApi(httpClient, config, httpClientHandler);
            var propertyId = "propertyId_example";  // string | 
            var market = "\"us\"";  // string | us (realtor.com) | ca (realtor.ca) (optional)  (default to "us")

            try
            {
                // Get full property detail
                Object result = apiInstance.RealtorGetFullPropertyDetail(propertyId, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RealtorApi.RealtorGetFullPropertyDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RealtorGetFullPropertyDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get full property detail
    ApiResponse<Object> response = apiInstance.RealtorGetFullPropertyDetailWithHttpInfo(propertyId, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RealtorApi.RealtorGetFullPropertyDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **propertyId** | **string** |  |  |
| **market** | **string** | us (realtor.com) | ca (realtor.ca) | [optional] [default to &quot;us&quot;] |

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

<a id="realtorlistmarkets"></a>
# **RealtorListMarkets**
> Object RealtorListMarkets ()

List markets

List supported Realtor markets (US = realtor.com, CA = realtor.ca).

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
    public class RealtorListMarketsExample
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
            var apiInstance = new RealtorApi(httpClient, config, httpClientHandler);

            try
            {
                // List markets
                Object result = apiInstance.RealtorListMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RealtorApi.RealtorListMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RealtorListMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<Object> response = apiInstance.RealtorListMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RealtorApi.RealtorListMarketsWithHttpInfo: " + e.Message);
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

<a id="realtorlocationautocomplete"></a>
# **RealtorLocationAutocomplete**
> Object RealtorLocationAutocomplete (string query, string market = null, int? limit = null)

Location autocomplete

Resolve a location query into candidate places to feed /search.

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
    public class RealtorLocationAutocompleteExample
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
            var apiInstance = new RealtorApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Freetext location (city, ZIP/postal, address…)
            var market = "\"us\"";  // string | us (realtor.com) | ca (realtor.ca) (optional)  (default to "us")
            var limit = 10;  // int? |  (optional)  (default to 10)

            try
            {
                // Location autocomplete
                Object result = apiInstance.RealtorLocationAutocomplete(query, market, limit);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RealtorApi.RealtorLocationAutocomplete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RealtorLocationAutocompleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Location autocomplete
    ApiResponse<Object> response = apiInstance.RealtorLocationAutocompleteWithHttpInfo(query, market, limit);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RealtorApi.RealtorLocationAutocompleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Freetext location (city, ZIP/postal, address…) |  |
| **market** | **string** | us (realtor.com) | ca (realtor.ca) | [optional] [default to &quot;us&quot;] |
| **limit** | **int?** |  | [optional] [default to 10] |

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

<a id="realtorrealtorscraperhealthcheck"></a>
# **RealtorRealtorScraperHealthCheck**
> Object RealtorRealtorScraperHealthCheck ()

Realtor scraper health check

Check health of the realtor scraper service (accepts HEAD for UptimeRobot).

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
    public class RealtorRealtorScraperHealthCheckExample
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
            var apiInstance = new RealtorApi(httpClient, config, httpClientHandler);

            try
            {
                // Realtor scraper health check
                Object result = apiInstance.RealtorRealtorScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RealtorApi.RealtorRealtorScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RealtorRealtorScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Realtor scraper health check
    ApiResponse<Object> response = apiInstance.RealtorRealtorScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RealtorApi.RealtorRealtorScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="realtorrealtorscraperhealthcheckhead"></a>
# **RealtorRealtorScraperHealthCheckHead**
> Object RealtorRealtorScraperHealthCheckHead ()

Realtor scraper health check

Check health of the realtor scraper service (accepts HEAD for UptimeRobot).

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
    public class RealtorRealtorScraperHealthCheckHeadExample
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
            var apiInstance = new RealtorApi(httpClient, config, httpClientHandler);

            try
            {
                // Realtor scraper health check
                Object result = apiInstance.RealtorRealtorScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RealtorApi.RealtorRealtorScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RealtorRealtorScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Realtor scraper health check
    ApiResponse<Object> response = apiInstance.RealtorRealtorScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RealtorApi.RealtorRealtorScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="realtorsearchpropertylistings"></a>
# **RealtorSearchPropertyListings**
> Object RealtorSearchPropertyListings (string location = null, string market = null, string status = null, decimal? priceMin = null, decimal? priceMax = null, int? bedsMin = null, int? bathsMin = null, int? sqftMin = null, int? sqftMax = null, string propertyType = null, string sort = null, int? page = null, int? limit = null, decimal? latMin = null, decimal? latMax = null, decimal? lngMin = null, decimal? lngMax = null)

Search property listings

Search for-sale/for-rent/sold listings with rich filters.

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
    public class RealtorSearchPropertyListingsExample
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
            var apiInstance = new RealtorApi(httpClient, config, httpClientHandler);
            var location = "location_example";  // string | 'Austin, TX', a ZIP, 'Toronto, ON'… (optional) 
            var market = "\"us\"";  // string | us (realtor.com) | ca (realtor.ca) (optional)  (default to "us")
            var status = "\"for_sale\"";  // string | for_sale | for_rent | sold | pending (optional)  (default to "for_sale")
            var priceMin = 8.14D;  // decimal? |  (optional) 
            var priceMax = 8.14D;  // decimal? |  (optional) 
            var bedsMin = 56;  // int? |  (optional) 
            var bathsMin = 56;  // int? |  (optional) 
            var sqftMin = 56;  // int? | US only (optional) 
            var sqftMax = 56;  // int? | US only (optional) 
            var propertyType = "propertyType_example";  // string | US only, CSV of property types (optional) 
            var sort = "\"relevant\"";  // string | relevant | newest | price_low | price_high | photo_count (optional)  (default to "relevant")
            var page = 1;  // int? |  (optional)  (default to 1)
            var limit = 56;  // int? |  (optional) 
            var latMin = 8.14D;  // decimal? | CA bbox south (optional) 
            var latMax = 8.14D;  // decimal? | CA bbox north (optional) 
            var lngMin = 8.14D;  // decimal? | CA bbox west (optional) 
            var lngMax = 8.14D;  // decimal? | CA bbox east (optional) 

            try
            {
                // Search property listings
                Object result = apiInstance.RealtorSearchPropertyListings(location, market, status, priceMin, priceMax, bedsMin, bathsMin, sqftMin, sqftMax, propertyType, sort, page, limit, latMin, latMax, lngMin, lngMax);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RealtorApi.RealtorSearchPropertyListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RealtorSearchPropertyListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search property listings
    ApiResponse<Object> response = apiInstance.RealtorSearchPropertyListingsWithHttpInfo(location, market, status, priceMin, priceMax, bedsMin, bathsMin, sqftMin, sqftMax, propertyType, sort, page, limit, latMin, latMax, lngMin, lngMax);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RealtorApi.RealtorSearchPropertyListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **location** | **string** | &#39;Austin, TX&#39;, a ZIP, &#39;Toronto, ON&#39;… | [optional]  |
| **market** | **string** | us (realtor.com) | ca (realtor.ca) | [optional] [default to &quot;us&quot;] |
| **status** | **string** | for_sale | for_rent | sold | pending | [optional] [default to &quot;for_sale&quot;] |
| **priceMin** | **decimal?** |  | [optional]  |
| **priceMax** | **decimal?** |  | [optional]  |
| **bedsMin** | **int?** |  | [optional]  |
| **bathsMin** | **int?** |  | [optional]  |
| **sqftMin** | **int?** | US only | [optional]  |
| **sqftMax** | **int?** | US only | [optional]  |
| **propertyType** | **string** | US only, CSV of property types | [optional]  |
| **sort** | **string** | relevant | newest | price_low | price_high | photo_count | [optional] [default to &quot;relevant&quot;] |
| **page** | **int?** |  | [optional] [default to 1] |
| **limit** | **int?** |  | [optional]  |
| **latMin** | **decimal?** | CA bbox south | [optional]  |
| **latMax** | **decimal?** | CA bbox north | [optional]  |
| **lngMin** | **decimal?** | CA bbox west | [optional]  |
| **lngMax** | **decimal?** | CA bbox east | [optional]  |

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

