# ScrapeBadger.Api.ZillowApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ZillowGetAgentProfileListings**](ZillowApi.md#zillowgetagentprofilelistings) | **GET** /v1/zillow/agent | Get agent profile + listings |
| [**ZillowGetPropertyDetail**](ZillowApi.md#zillowgetpropertydetail) | **GET** /v1/zillow/property/{zpid} | Get property detail |
| [**ZillowGetPropertyDetailByUrl**](ZillowApi.md#zillowgetpropertydetailbyurl) | **GET** /v1/zillow/property | Get property detail by URL |
| [**ZillowListCoverageMarkets**](ZillowApi.md#zillowlistcoveragemarkets) | **GET** /v1/zillow/markets | List coverage markets |
| [**ZillowRegionAddressSuggestions**](ZillowApi.md#zillowregionaddresssuggestions) | **GET** /v1/zillow/autocomplete | Region/address suggestions |
| [**ZillowSearchProperties**](ZillowApi.md#zillowsearchproperties) | **GET** /v1/zillow/search | Search properties |
| [**ZillowZillowScraperHealthCheck**](ZillowApi.md#zillowzillowscraperhealthcheck) | **GET** /v1/zillow/health | Zillow scraper health check |
| [**ZillowZillowScraperHealthCheckHead**](ZillowApi.md#zillowzillowscraperhealthcheckhead) | **HEAD** /v1/zillow/health | Zillow scraper health check |

<a id="zillowgetagentprofilelistings"></a>
# **ZillowGetAgentProfileListings**
> Object ZillowGetAgentProfileListings (string username = null, string url = null)

Get agent profile + listings

Get a Zillow professional's profile and their active listings.

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
    public class ZillowGetAgentProfileListingsExample
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
            var apiInstance = new ZillowApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | Zillow profile username (optional) 
            var url = "url_example";  // string | Full Zillow /profile/... URL (optional) 

            try
            {
                // Get agent profile + listings
                Object result = apiInstance.ZillowGetAgentProfileListings(username, url);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ZillowApi.ZillowGetAgentProfileListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ZillowGetAgentProfileListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get agent profile + listings
    ApiResponse<Object> response = apiInstance.ZillowGetAgentProfileListingsWithHttpInfo(username, url);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ZillowApi.ZillowGetAgentProfileListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** | Zillow profile username | [optional]  |
| **url** | **string** | Full Zillow /profile/... URL | [optional]  |

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

<a id="zillowgetpropertydetail"></a>
# **ZillowGetPropertyDetail**
> Object ZillowGetPropertyDetail (string zpid)

Get property detail

Get a single Zillow property's full detail by zpid.

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
    public class ZillowGetPropertyDetailExample
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
            var apiInstance = new ZillowApi(httpClient, config, httpClientHandler);
            var zpid = "zpid_example";  // string | 

            try
            {
                // Get property detail
                Object result = apiInstance.ZillowGetPropertyDetail(zpid);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ZillowApi.ZillowGetPropertyDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ZillowGetPropertyDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get property detail
    ApiResponse<Object> response = apiInstance.ZillowGetPropertyDetailWithHttpInfo(zpid);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ZillowApi.ZillowGetPropertyDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **zpid** | **string** |  |  |

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

<a id="zillowgetpropertydetailbyurl"></a>
# **ZillowGetPropertyDetailByUrl**
> Object ZillowGetPropertyDetailByUrl (string url)

Get property detail by URL

Get a single Zillow property's full detail by its homedetails URL.

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
    public class ZillowGetPropertyDetailByUrlExample
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
            var apiInstance = new ZillowApi(httpClient, config, httpClientHandler);
            var url = "url_example";  // string | Full Zillow /homedetails/... URL

            try
            {
                // Get property detail by URL
                Object result = apiInstance.ZillowGetPropertyDetailByUrl(url);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ZillowApi.ZillowGetPropertyDetailByUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ZillowGetPropertyDetailByUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get property detail by URL
    ApiResponse<Object> response = apiInstance.ZillowGetPropertyDetailByUrlWithHttpInfo(url);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ZillowApi.ZillowGetPropertyDetailByUrlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **url** | **string** | Full Zillow /homedetails/... URL |  |

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

<a id="zillowlistcoveragemarkets"></a>
# **ZillowListCoverageMarkets**
> Object ZillowListCoverageMarkets ()

List coverage markets

List Zillow coverage regions (US + Canada).

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
    public class ZillowListCoverageMarketsExample
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
            var apiInstance = new ZillowApi(httpClient, config, httpClientHandler);

            try
            {
                // List coverage markets
                Object result = apiInstance.ZillowListCoverageMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ZillowApi.ZillowListCoverageMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ZillowListCoverageMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List coverage markets
    ApiResponse<Object> response = apiInstance.ZillowListCoverageMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ZillowApi.ZillowListCoverageMarketsWithHttpInfo: " + e.Message);
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

<a id="zillowregionaddresssuggestions"></a>
# **ZillowRegionAddressSuggestions**
> Object ZillowRegionAddressSuggestions (string query)

Region/address suggestions

Resolve a search term to Zillow regions/addresses.

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
    public class ZillowRegionAddressSuggestionsExample
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
            var apiInstance = new ZillowApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Partial location — city, ZIP, address, neighborhood

            try
            {
                // Region/address suggestions
                Object result = apiInstance.ZillowRegionAddressSuggestions(query);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ZillowApi.ZillowRegionAddressSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ZillowRegionAddressSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Region/address suggestions
    ApiResponse<Object> response = apiInstance.ZillowRegionAddressSuggestionsWithHttpInfo(query);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ZillowApi.ZillowRegionAddressSuggestionsWithHttpInfo: " + e.Message);
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

<a id="zillowsearchproperties"></a>
# **ZillowSearchProperties**
> Object ZillowSearchProperties (string location, string status = null, int? page = null, string sort = null, int? priceMin = null, int? priceMax = null, int? bedsMin = null, decimal? bathsMin = null, string homeType = null, int? sqftMin = null, int? sqftMax = null, int? lotMin = null, int? lotMax = null, int? yearBuiltMin = null, int? yearBuiltMax = null, int? hoaMax = null, string keywords = null, string daysOn = null, decimal? north = null, decimal? south = null, decimal? east = null, decimal? west = null)

Search properties

Search Zillow for for-sale / for-rent / recently-sold properties.

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
    public class ZillowSearchPropertiesExample
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
            var apiInstance = new ZillowApi(httpClient, config, httpClientHandler);
            var location = "location_example";  // string | City/state, ZIP, address or neighborhood
            var status = "\"for_sale\"";  // string | for_sale|for_rent|sold (optional)  (default to "for_sale")
            var page = 1;  // int? |  (optional)  (default to 1)
            var sort = "sort_example";  // string | homes_for_you|newest|price_high_to_low|price_low_to_high|bedrooms|bathrooms|square_feet|lot_size|year_built (optional) 
            var priceMin = 56;  // int? |  (optional) 
            var priceMax = 56;  // int? |  (optional) 
            var bedsMin = 56;  // int? |  (optional) 
            var bathsMin = 8.14D;  // decimal? |  (optional) 
            var homeType = "homeType_example";  // string | houses|condos|townhomes|apartments|manufactured|lots|multi_family (optional) 
            var sqftMin = 56;  // int? |  (optional) 
            var sqftMax = 56;  // int? |  (optional) 
            var lotMin = 56;  // int? |  (optional) 
            var lotMax = 56;  // int? |  (optional) 
            var yearBuiltMin = 56;  // int? |  (optional) 
            var yearBuiltMax = 56;  // int? |  (optional) 
            var hoaMax = 56;  // int? |  (optional) 
            var keywords = "keywords_example";  // string |  (optional) 
            var daysOn = "daysOn_example";  // string |  (optional) 
            var north = 8.14D;  // decimal? | Map bounds for tiling past the 820 cap (optional) 
            var south = 8.14D;  // decimal? |  (optional) 
            var east = 8.14D;  // decimal? |  (optional) 
            var west = 8.14D;  // decimal? |  (optional) 

            try
            {
                // Search properties
                Object result = apiInstance.ZillowSearchProperties(location, status, page, sort, priceMin, priceMax, bedsMin, bathsMin, homeType, sqftMin, sqftMax, lotMin, lotMax, yearBuiltMin, yearBuiltMax, hoaMax, keywords, daysOn, north, south, east, west);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ZillowApi.ZillowSearchProperties: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ZillowSearchPropertiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search properties
    ApiResponse<Object> response = apiInstance.ZillowSearchPropertiesWithHttpInfo(location, status, page, sort, priceMin, priceMax, bedsMin, bathsMin, homeType, sqftMin, sqftMax, lotMin, lotMax, yearBuiltMin, yearBuiltMax, hoaMax, keywords, daysOn, north, south, east, west);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ZillowApi.ZillowSearchPropertiesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **location** | **string** | City/state, ZIP, address or neighborhood |  |
| **status** | **string** | for_sale|for_rent|sold | [optional] [default to &quot;for_sale&quot;] |
| **page** | **int?** |  | [optional] [default to 1] |
| **sort** | **string** | homes_for_you|newest|price_high_to_low|price_low_to_high|bedrooms|bathrooms|square_feet|lot_size|year_built | [optional]  |
| **priceMin** | **int?** |  | [optional]  |
| **priceMax** | **int?** |  | [optional]  |
| **bedsMin** | **int?** |  | [optional]  |
| **bathsMin** | **decimal?** |  | [optional]  |
| **homeType** | **string** | houses|condos|townhomes|apartments|manufactured|lots|multi_family | [optional]  |
| **sqftMin** | **int?** |  | [optional]  |
| **sqftMax** | **int?** |  | [optional]  |
| **lotMin** | **int?** |  | [optional]  |
| **lotMax** | **int?** |  | [optional]  |
| **yearBuiltMin** | **int?** |  | [optional]  |
| **yearBuiltMax** | **int?** |  | [optional]  |
| **hoaMax** | **int?** |  | [optional]  |
| **keywords** | **string** |  | [optional]  |
| **daysOn** | **string** |  | [optional]  |
| **north** | **decimal?** | Map bounds for tiling past the 820 cap | [optional]  |
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

<a id="zillowzillowscraperhealthcheck"></a>
# **ZillowZillowScraperHealthCheck**
> Object ZillowZillowScraperHealthCheck ()

Zillow scraper health check

Check health of the Zillow scraper service (accepts HEAD for UptimeRobot).

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
    public class ZillowZillowScraperHealthCheckExample
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
            var apiInstance = new ZillowApi(httpClient, config, httpClientHandler);

            try
            {
                // Zillow scraper health check
                Object result = apiInstance.ZillowZillowScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ZillowApi.ZillowZillowScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ZillowZillowScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Zillow scraper health check
    ApiResponse<Object> response = apiInstance.ZillowZillowScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ZillowApi.ZillowZillowScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="zillowzillowscraperhealthcheckhead"></a>
# **ZillowZillowScraperHealthCheckHead**
> Object ZillowZillowScraperHealthCheckHead ()

Zillow scraper health check

Check health of the Zillow scraper service (accepts HEAD for UptimeRobot).

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
    public class ZillowZillowScraperHealthCheckHeadExample
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
            var apiInstance = new ZillowApi(httpClient, config, httpClientHandler);

            try
            {
                // Zillow scraper health check
                Object result = apiInstance.ZillowZillowScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ZillowApi.ZillowZillowScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ZillowZillowScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Zillow scraper health check
    ApiResponse<Object> response = apiInstance.ZillowZillowScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ZillowApi.ZillowZillowScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

