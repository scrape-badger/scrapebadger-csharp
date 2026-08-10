# ScrapeBadger.Api.RedfinApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**RedfinGetAgentProfileListings**](RedfinApi.md#redfingetagentprofilelistings) | **GET** /v1/redfin/agent | Get agent profile + listings |
| [**RedfinGetPropertyDetail**](RedfinApi.md#redfingetpropertydetail) | **GET** /v1/redfin/property/{property_id} | Get property detail |
| [**RedfinGetPropertyDetailByUrl**](RedfinApi.md#redfingetpropertydetailbyurl) | **GET** /v1/redfin/property | Get property detail by URL |
| [**RedfinListCoverageMarkets**](RedfinApi.md#redfinlistcoveragemarkets) | **GET** /v1/redfin/markets | List coverage markets |
| [**RedfinRedfinScraperHealthCheck**](RedfinApi.md#redfinredfinscraperhealthcheck) | **GET** /v1/redfin/health | Redfin scraper health check |
| [**RedfinRedfinScraperHealthCheckHead**](RedfinApi.md#redfinredfinscraperhealthcheckhead) | **HEAD** /v1/redfin/health | Redfin scraper health check |
| [**RedfinRegionAddressSuggestions**](RedfinApi.md#redfinregionaddresssuggestions) | **GET** /v1/redfin/autocomplete | Region/address suggestions |
| [**RedfinSearchProperties**](RedfinApi.md#redfinsearchproperties) | **GET** /v1/redfin/search | Search properties |

<a id="redfingetagentprofilelistings"></a>
# **RedfinGetAgentProfileListings**
> Object RedfinGetAgentProfileListings (string url = null, string agentId = null)

Get agent profile + listings

Get a Redfin real-estate agent's profile and their active listings.

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
    public class RedfinGetAgentProfileListingsExample
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
            var apiInstance = new RedfinApi(httpClient, config, httpClientHandler);
            var url = "url_example";  // string | Full Redfin /realestateagents/ URL (optional) 
            var agentId = "agentId_example";  // string | Redfin agent id (optional) 

            try
            {
                // Get agent profile + listings
                Object result = apiInstance.RedfinGetAgentProfileListings(url, agentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedfinApi.RedfinGetAgentProfileListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedfinGetAgentProfileListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get agent profile + listings
    ApiResponse<Object> response = apiInstance.RedfinGetAgentProfileListingsWithHttpInfo(url, agentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedfinApi.RedfinGetAgentProfileListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **url** | **string** | Full Redfin /realestateagents/ URL | [optional]  |
| **agentId** | **string** | Redfin agent id | [optional]  |

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

<a id="redfingetpropertydetail"></a>
# **RedfinGetPropertyDetail**
> Object RedfinGetPropertyDetail (string propertyId)

Get property detail

Get a single Redfin property's full detail by its numeric propertyId.

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
    public class RedfinGetPropertyDetailExample
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
            var apiInstance = new RedfinApi(httpClient, config, httpClientHandler);
            var propertyId = "propertyId_example";  // string | 

            try
            {
                // Get property detail
                Object result = apiInstance.RedfinGetPropertyDetail(propertyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedfinApi.RedfinGetPropertyDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedfinGetPropertyDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get property detail
    ApiResponse<Object> response = apiInstance.RedfinGetPropertyDetailWithHttpInfo(propertyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedfinApi.RedfinGetPropertyDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **propertyId** | **string** |  |  |

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

<a id="redfingetpropertydetailbyurl"></a>
# **RedfinGetPropertyDetailByUrl**
> Object RedfinGetPropertyDetailByUrl (string url)

Get property detail by URL

Get a single Redfin property's full detail by its home URL.

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
    public class RedfinGetPropertyDetailByUrlExample
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
            var apiInstance = new RedfinApi(httpClient, config, httpClientHandler);
            var url = "url_example";  // string | Full Redfin property URL (/CA/City/.../home/12345678)

            try
            {
                // Get property detail by URL
                Object result = apiInstance.RedfinGetPropertyDetailByUrl(url);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedfinApi.RedfinGetPropertyDetailByUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedfinGetPropertyDetailByUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get property detail by URL
    ApiResponse<Object> response = apiInstance.RedfinGetPropertyDetailByUrlWithHttpInfo(url);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedfinApi.RedfinGetPropertyDetailByUrlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **url** | **string** | Full Redfin property URL (/CA/City/.../home/12345678) |  |

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

<a id="redfinlistcoveragemarkets"></a>
# **RedfinListCoverageMarkets**
> Object RedfinListCoverageMarkets ()

List coverage markets

List Redfin coverage regions (US).

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
    public class RedfinListCoverageMarketsExample
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
            var apiInstance = new RedfinApi(httpClient, config, httpClientHandler);

            try
            {
                // List coverage markets
                Object result = apiInstance.RedfinListCoverageMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedfinApi.RedfinListCoverageMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedfinListCoverageMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List coverage markets
    ApiResponse<Object> response = apiInstance.RedfinListCoverageMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedfinApi.RedfinListCoverageMarketsWithHttpInfo: " + e.Message);
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

<a id="redfinredfinscraperhealthcheck"></a>
# **RedfinRedfinScraperHealthCheck**
> Object RedfinRedfinScraperHealthCheck ()

Redfin scraper health check

Check health of the Redfin scraper service (accepts HEAD for UptimeRobot).

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
    public class RedfinRedfinScraperHealthCheckExample
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
            var apiInstance = new RedfinApi(httpClient, config, httpClientHandler);

            try
            {
                // Redfin scraper health check
                Object result = apiInstance.RedfinRedfinScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedfinApi.RedfinRedfinScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedfinRedfinScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Redfin scraper health check
    ApiResponse<Object> response = apiInstance.RedfinRedfinScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedfinApi.RedfinRedfinScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="redfinredfinscraperhealthcheckhead"></a>
# **RedfinRedfinScraperHealthCheckHead**
> Object RedfinRedfinScraperHealthCheckHead ()

Redfin scraper health check

Check health of the Redfin scraper service (accepts HEAD for UptimeRobot).

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
    public class RedfinRedfinScraperHealthCheckHeadExample
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
            var apiInstance = new RedfinApi(httpClient, config, httpClientHandler);

            try
            {
                // Redfin scraper health check
                Object result = apiInstance.RedfinRedfinScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedfinApi.RedfinRedfinScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedfinRedfinScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Redfin scraper health check
    ApiResponse<Object> response = apiInstance.RedfinRedfinScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedfinApi.RedfinRedfinScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="redfinregionaddresssuggestions"></a>
# **RedfinRegionAddressSuggestions**
> Object RedfinRegionAddressSuggestions (string query)

Region/address suggestions

Resolve a search term to Redfin regions/addresses.

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
    public class RedfinRegionAddressSuggestionsExample
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
            var apiInstance = new RedfinApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Partial location — city, ZIP, address, neighborhood

            try
            {
                // Region/address suggestions
                Object result = apiInstance.RedfinRegionAddressSuggestions(query);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedfinApi.RedfinRegionAddressSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedfinRegionAddressSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Region/address suggestions
    ApiResponse<Object> response = apiInstance.RedfinRegionAddressSuggestionsWithHttpInfo(query);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedfinApi.RedfinRegionAddressSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Partial location — city, ZIP, address, neighborhood |  |

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

<a id="redfinsearchproperties"></a>
# **RedfinSearchProperties**
> Object RedfinSearchProperties (string location, int? page = null, string sort = null, int? priceMin = null, int? priceMax = null, int? bedsMin = null, decimal? bathsMin = null, string homeType = null, int? sqftMin = null, int? sqftMax = null, int? lotMin = null, int? lotMax = null, int? yearBuiltMin = null, int? yearBuiltMax = null, int? maxDaysOnMarket = null, decimal? north = null, decimal? south = null, decimal? east = null, decimal? west = null)

Search properties

Search Redfin for for-sale / for-rent / recently-sold properties.

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
    public class RedfinSearchPropertiesExample
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
            var apiInstance = new RedfinApi(httpClient, config, httpClientHandler);
            var location = "location_example";  // string | City/state, ZIP, address or neighborhood
            var page = 1;  // int? |  (optional)  (default to 1)
            var sort = "sort_example";  // string | relevant|newest|price_high_to_low|price_low_to_high|square_feet|lot_size|price_per_sqft|beds|baths (optional) 
            var priceMin = 56;  // int? |  (optional) 
            var priceMax = 56;  // int? |  (optional) 
            var bedsMin = 56;  // int? |  (optional) 
            var bathsMin = 8.14D;  // decimal? |  (optional) 
            var homeType = "homeType_example";  // string | house|condo|townhouse|multi_family|land|mobile|coop|other (optional) 
            var sqftMin = 56;  // int? |  (optional) 
            var sqftMax = 56;  // int? |  (optional) 
            var lotMin = 56;  // int? |  (optional) 
            var lotMax = 56;  // int? |  (optional) 
            var yearBuiltMin = 56;  // int? |  (optional) 
            var yearBuiltMax = 56;  // int? |  (optional) 
            var maxDaysOnMarket = 56;  // int? |  (optional) 
            var north = 8.14D;  // decimal? | Map bounds for tiling past the cap (optional) 
            var south = 8.14D;  // decimal? |  (optional) 
            var east = 8.14D;  // decimal? |  (optional) 
            var west = 8.14D;  // decimal? |  (optional) 

            try
            {
                // Search properties
                Object result = apiInstance.RedfinSearchProperties(location, page, sort, priceMin, priceMax, bedsMin, bathsMin, homeType, sqftMin, sqftMax, lotMin, lotMax, yearBuiltMin, yearBuiltMax, maxDaysOnMarket, north, south, east, west);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RedfinApi.RedfinSearchProperties: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RedfinSearchPropertiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search properties
    ApiResponse<Object> response = apiInstance.RedfinSearchPropertiesWithHttpInfo(location, page, sort, priceMin, priceMax, bedsMin, bathsMin, homeType, sqftMin, sqftMax, lotMin, lotMax, yearBuiltMin, yearBuiltMax, maxDaysOnMarket, north, south, east, west);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RedfinApi.RedfinSearchPropertiesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **location** | **string** | City/state, ZIP, address or neighborhood |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **sort** | **string** | relevant|newest|price_high_to_low|price_low_to_high|square_feet|lot_size|price_per_sqft|beds|baths | [optional]  |
| **priceMin** | **int?** |  | [optional]  |
| **priceMax** | **int?** |  | [optional]  |
| **bedsMin** | **int?** |  | [optional]  |
| **bathsMin** | **decimal?** |  | [optional]  |
| **homeType** | **string** | house|condo|townhouse|multi_family|land|mobile|coop|other | [optional]  |
| **sqftMin** | **int?** |  | [optional]  |
| **sqftMax** | **int?** |  | [optional]  |
| **lotMin** | **int?** |  | [optional]  |
| **lotMax** | **int?** |  | [optional]  |
| **yearBuiltMin** | **int?** |  | [optional]  |
| **yearBuiltMax** | **int?** |  | [optional]  |
| **maxDaysOnMarket** | **int?** |  | [optional]  |
| **north** | **decimal?** | Map bounds for tiling past the cap | [optional]  |
| **south** | **decimal?** |  | [optional]  |
| **east** | **decimal?** |  | [optional]  |
| **west** | **decimal?** |  | [optional]  |

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

