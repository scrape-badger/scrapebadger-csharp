# ScrapeBadger.Api.IdealistaApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**IdealistaAgencyByPhone**](IdealistaApi.md#idealistaagencybyphone) | **GET** /v1/idealista/agency/by-phone/{phone} | Agency by phone |
| [**IdealistaAgencyProfileListings**](IdealistaApi.md#idealistaagencyprofilelistings) | **GET** /v1/idealista/agency/{short_name} | Agency profile + listings |
| [**IdealistaGetListingEngagementStats**](IdealistaApi.md#idealistagetlistingengagementstats) | **GET** /v1/idealista/properties/{property_code}/stats | Get listing engagement stats |
| [**IdealistaGetPropertyDetail**](IdealistaApi.md#idealistagetpropertydetail) | **GET** /v1/idealista/properties/{property_code} | Get property detail |
| [**IdealistaIdealistaScraperHealthCheck**](IdealistaApi.md#idealistaidealistascraperhealthcheck) | **GET** /v1/idealista/health | Idealista scraper health check |
| [**IdealistaIdealistaScraperHealthCheckHead**](IdealistaApi.md#idealistaidealistascraperhealthcheckhead) | **HEAD** /v1/idealista/health | Idealista scraper health check |
| [**IdealistaListMarkets**](IdealistaApi.md#idealistalistmarkets) | **GET** /v1/idealista/markets | List markets |
| [**IdealistaResolveLocations**](IdealistaApi.md#idealistaresolvelocations) | **GET** /v1/idealista/suggest | Resolve locations |
| [**IdealistaSearchAllBeatsResultCap**](IdealistaApi.md#idealistasearchallbeatsresultcap) | **GET** /v1/idealista/search/all | Search all (beats result cap) |
| [**IdealistaSearchListings**](IdealistaApi.md#idealistasearchlistings) | **GET** /v1/idealista/search | Search listings |

<a id="idealistaagencybyphone"></a>
# **IdealistaAgencyByPhone**
> Object IdealistaAgencyByPhone (string phone, string market = null, string operation = null, string propertyType = null, int? page = null, int? maxItems = null, bool? includeListings = null)

Agency by phone

Reverse-lookup the agency behind a contact phone (national number), with its listings.

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
    public class IdealistaAgencyByPhoneExample
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
            var apiInstance = new IdealistaApi(httpClient, config, httpClientHandler);
            var phone = "phone_example";  // string | 
            var market = "\"es\"";  // string | es|it|pt (optional)  (default to "es")
            var operation = "operation_example";  // string | sale|rent (optional) 
            var propertyType = "propertyType_example";  // string | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)
            var maxItems = 30;  // int? |  (optional)  (default to 30)
            var includeListings = true;  // bool? |  (optional)  (default to true)

            try
            {
                // Agency by phone
                Object result = apiInstance.IdealistaAgencyByPhone(phone, market, operation, propertyType, page, maxItems, includeListings);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IdealistaApi.IdealistaAgencyByPhone: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the IdealistaAgencyByPhoneWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Agency by phone
    ApiResponse<Object> response = apiInstance.IdealistaAgencyByPhoneWithHttpInfo(phone, market, operation, propertyType, page, maxItems, includeListings);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IdealistaApi.IdealistaAgencyByPhoneWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **phone** | **string** |  |  |
| **market** | **string** | es|it|pt | [optional] [default to &quot;es&quot;] |
| **operation** | **string** | sale|rent | [optional]  |
| **propertyType** | **string** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional]  |
| **page** | **int?** |  | [optional] [default to 1] |
| **maxItems** | **int?** |  | [optional] [default to 30] |
| **includeListings** | **bool?** |  | [optional] [default to true] |

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

<a id="idealistaagencyprofilelistings"></a>
# **IdealistaAgencyProfileListings**
> Object IdealistaAgencyProfileListings (string shortName, string market = null, string operation = null, string propertyType = null, int? page = null, int? maxItems = null, bool? includeListings = null)

Agency profile + listings

An agency's microsite profile plus a page of its listings (by URL-slug shortName).

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
    public class IdealistaAgencyProfileListingsExample
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
            var apiInstance = new IdealistaApi(httpClient, config, httpClientHandler);
            var shortName = "shortName_example";  // string | 
            var market = "\"es\"";  // string | es|it|pt (optional)  (default to "es")
            var operation = "operation_example";  // string | sale|rent (optional) 
            var propertyType = "propertyType_example";  // string | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)
            var maxItems = 30;  // int? |  (optional)  (default to 30)
            var includeListings = true;  // bool? |  (optional)  (default to true)

            try
            {
                // Agency profile + listings
                Object result = apiInstance.IdealistaAgencyProfileListings(shortName, market, operation, propertyType, page, maxItems, includeListings);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IdealistaApi.IdealistaAgencyProfileListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the IdealistaAgencyProfileListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Agency profile + listings
    ApiResponse<Object> response = apiInstance.IdealistaAgencyProfileListingsWithHttpInfo(shortName, market, operation, propertyType, page, maxItems, includeListings);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IdealistaApi.IdealistaAgencyProfileListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **shortName** | **string** |  |  |
| **market** | **string** | es|it|pt | [optional] [default to &quot;es&quot;] |
| **operation** | **string** | sale|rent | [optional]  |
| **propertyType** | **string** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional]  |
| **page** | **int?** |  | [optional] [default to 1] |
| **maxItems** | **int?** |  | [optional] [default to 30] |
| **includeListings** | **bool?** |  | [optional] [default to true] |

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

<a id="idealistagetlistingengagementstats"></a>
# **IdealistaGetListingEngagementStats**
> Object IdealistaGetListingEngagementStats (string propertyCode, string market = null, string locale = null)

Get listing engagement stats

Engagement counters for a listing: views, email contacts, sent-to-friend, favourites.

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
    public class IdealistaGetListingEngagementStatsExample
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
            var apiInstance = new IdealistaApi(httpClient, config, httpClientHandler);
            var propertyCode = "propertyCode_example";  // string | 
            var market = "\"es\"";  // string | es|it|pt (optional)  (default to "es")
            var locale = "\"en\"";  // string | Language for stat labels (optional)  (default to "en")

            try
            {
                // Get listing engagement stats
                Object result = apiInstance.IdealistaGetListingEngagementStats(propertyCode, market, locale);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IdealistaApi.IdealistaGetListingEngagementStats: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the IdealistaGetListingEngagementStatsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get listing engagement stats
    ApiResponse<Object> response = apiInstance.IdealistaGetListingEngagementStatsWithHttpInfo(propertyCode, market, locale);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IdealistaApi.IdealistaGetListingEngagementStatsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **propertyCode** | **string** |  |  |
| **market** | **string** | es|it|pt | [optional] [default to &quot;es&quot;] |
| **locale** | **string** | Language for stat labels | [optional] [default to &quot;en&quot;] |

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

<a id="idealistagetpropertydetail"></a>
# **IdealistaGetPropertyDetail**
> Object IdealistaGetPropertyDetail (string propertyCode, string market = null, string locale = null)

Get property detail

Get a single Idealista listing's full detail (energy cert, characteristics, media).

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
    public class IdealistaGetPropertyDetailExample
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
            var apiInstance = new IdealistaApi(httpClient, config, httpClientHandler);
            var propertyCode = "propertyCode_example";  // string | 
            var market = "\"es\"";  // string | es|it|pt (optional)  (default to "es")
            var locale = "\"en\"";  // string | Response language (en, es, it, pt) (optional)  (default to "en")

            try
            {
                // Get property detail
                Object result = apiInstance.IdealistaGetPropertyDetail(propertyCode, market, locale);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IdealistaApi.IdealistaGetPropertyDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the IdealistaGetPropertyDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get property detail
    ApiResponse<Object> response = apiInstance.IdealistaGetPropertyDetailWithHttpInfo(propertyCode, market, locale);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IdealistaApi.IdealistaGetPropertyDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **propertyCode** | **string** |  |  |
| **market** | **string** | es|it|pt | [optional] [default to &quot;es&quot;] |
| **locale** | **string** | Response language (en, es, it, pt) | [optional] [default to &quot;en&quot;] |

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

<a id="idealistaidealistascraperhealthcheck"></a>
# **IdealistaIdealistaScraperHealthCheck**
> Object IdealistaIdealistaScraperHealthCheck ()

Idealista scraper health check

Check health of the Idealista scraper service (accepts HEAD for UptimeRobot).

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
    public class IdealistaIdealistaScraperHealthCheckExample
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
            var apiInstance = new IdealistaApi(httpClient, config, httpClientHandler);

            try
            {
                // Idealista scraper health check
                Object result = apiInstance.IdealistaIdealistaScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IdealistaApi.IdealistaIdealistaScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the IdealistaIdealistaScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Idealista scraper health check
    ApiResponse<Object> response = apiInstance.IdealistaIdealistaScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IdealistaApi.IdealistaIdealistaScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="idealistaidealistascraperhealthcheckhead"></a>
# **IdealistaIdealistaScraperHealthCheckHead**
> Object IdealistaIdealistaScraperHealthCheckHead ()

Idealista scraper health check

Check health of the Idealista scraper service (accepts HEAD for UptimeRobot).

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
    public class IdealistaIdealistaScraperHealthCheckHeadExample
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
            var apiInstance = new IdealistaApi(httpClient, config, httpClientHandler);

            try
            {
                // Idealista scraper health check
                Object result = apiInstance.IdealistaIdealistaScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IdealistaApi.IdealistaIdealistaScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the IdealistaIdealistaScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Idealista scraper health check
    ApiResponse<Object> response = apiInstance.IdealistaIdealistaScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IdealistaApi.IdealistaIdealistaScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="idealistalistmarkets"></a>
# **IdealistaListMarkets**
> Object IdealistaListMarkets ()

List markets

List supported Idealista markets (ES, IT, PT).

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
    public class IdealistaListMarketsExample
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
            var apiInstance = new IdealistaApi(httpClient, config, httpClientHandler);

            try
            {
                // List markets
                Object result = apiInstance.IdealistaListMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IdealistaApi.IdealistaListMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the IdealistaListMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<Object> response = apiInstance.IdealistaListMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IdealistaApi.IdealistaListMarketsWithHttpInfo: " + e.Message);
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

<a id="idealistaresolvelocations"></a>
# **IdealistaResolveLocations**
> Object IdealistaResolveLocations (string query, string operation = null, string propertyType = null, string market = null, string locale = null)

Resolve locations

Resolve a free-text query into Idealista location codes for a search.

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
    public class IdealistaResolveLocationsExample
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
            var apiInstance = new IdealistaApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Free-text location, e.g. 'sagrada familia'
            var operation = "\"sale\"";  // string | sale|rent (optional)  (default to "sale")
            var propertyType = "\"homes\"";  // string | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms (optional)  (default to "homes")
            var market = "\"es\"";  // string | es|it|pt (optional)  (default to "es")
            var locale = "locale_example";  // string | Response language (en, es, it, pt) (optional) 

            try
            {
                // Resolve locations
                Object result = apiInstance.IdealistaResolveLocations(query, operation, propertyType, market, locale);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IdealistaApi.IdealistaResolveLocations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the IdealistaResolveLocationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resolve locations
    ApiResponse<Object> response = apiInstance.IdealistaResolveLocationsWithHttpInfo(query, operation, propertyType, market, locale);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IdealistaApi.IdealistaResolveLocationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Free-text location, e.g. &#39;sagrada familia&#39; |  |
| **operation** | **string** | sale|rent | [optional] [default to &quot;sale&quot;] |
| **propertyType** | **string** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] [default to &quot;homes&quot;] |
| **market** | **string** | es|it|pt | [optional] [default to &quot;es&quot;] |
| **locale** | **string** | Response language (en, es, it, pt) | [optional]  |

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

<a id="idealistasearchallbeatsresultcap"></a>
# **IdealistaSearchAllBeatsResultCap**
> Object IdealistaSearchAllBeatsResultCap (string location, string operation = null, string propertyType = null, string market = null, int? maxResults = null, decimal? minPrice = null, decimal? maxPrice = null, decimal? minSize = null, decimal? maxSize = null, int? minRooms = null, int? maxRooms = null, string locale = null)

Search all (beats result cap)

Full inventory for a location, beating Idealista's ~1800 per-search cap via price-range tiling (deduped). Billed per page fetched.

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
    public class IdealistaSearchAllBeatsResultCapExample
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
            var apiInstance = new IdealistaApi(httpClient, config, httpClientHandler);
            var location = "location_example";  // string | Idealista location code (from /suggest)
            var operation = "\"sale\"";  // string | sale|rent (optional)  (default to "sale")
            var propertyType = "\"homes\"";  // string | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms (optional)  (default to "homes")
            var market = "\"es\"";  // string | es|it|pt (optional)  (default to "es")
            var maxResults = 500;  // int? |  (optional)  (default to 500)
            var minPrice = 8.14D;  // decimal? |  (optional) 
            var maxPrice = 8.14D;  // decimal? |  (optional) 
            var minSize = 8.14D;  // decimal? |  (optional) 
            var maxSize = 8.14D;  // decimal? |  (optional) 
            var minRooms = 56;  // int? |  (optional) 
            var maxRooms = 56;  // int? |  (optional) 
            var locale = "locale_example";  // string | Response language (en, es, it, pt) (optional) 

            try
            {
                // Search all (beats result cap)
                Object result = apiInstance.IdealistaSearchAllBeatsResultCap(location, operation, propertyType, market, maxResults, minPrice, maxPrice, minSize, maxSize, minRooms, maxRooms, locale);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IdealistaApi.IdealistaSearchAllBeatsResultCap: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the IdealistaSearchAllBeatsResultCapWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search all (beats result cap)
    ApiResponse<Object> response = apiInstance.IdealistaSearchAllBeatsResultCapWithHttpInfo(location, operation, propertyType, market, maxResults, minPrice, maxPrice, minSize, maxSize, minRooms, maxRooms, locale);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IdealistaApi.IdealistaSearchAllBeatsResultCapWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **location** | **string** | Idealista location code (from /suggest) |  |
| **operation** | **string** | sale|rent | [optional] [default to &quot;sale&quot;] |
| **propertyType** | **string** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] [default to &quot;homes&quot;] |
| **market** | **string** | es|it|pt | [optional] [default to &quot;es&quot;] |
| **maxResults** | **int?** |  | [optional] [default to 500] |
| **minPrice** | **decimal?** |  | [optional]  |
| **maxPrice** | **decimal?** |  | [optional]  |
| **minSize** | **decimal?** |  | [optional]  |
| **maxSize** | **decimal?** |  | [optional]  |
| **minRooms** | **int?** |  | [optional]  |
| **maxRooms** | **int?** |  | [optional]  |
| **locale** | **string** | Response language (en, es, it, pt) | [optional]  |

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

<a id="idealistasearchlistings"></a>
# **IdealistaSearchListings**
> Object IdealistaSearchListings (string location, string operation = null, string propertyType = null, string market = null, int? page = null, int? maxItems = null, string sortBy = null, string sortOrder = null, decimal? minPrice = null, decimal? maxPrice = null, decimal? minSize = null, decimal? maxSize = null, int? minRooms = null, int? maxRooms = null, string locale = null)

Search listings

Search Idealista real-estate listings by location code.

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
    public class IdealistaSearchListingsExample
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
            var apiInstance = new IdealistaApi(httpClient, config, httpClientHandler);
            var location = "location_example";  // string | Idealista location code (from /suggest)
            var operation = "\"sale\"";  // string | sale|rent (optional)  (default to "sale")
            var propertyType = "\"homes\"";  // string | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms (optional)  (default to "homes")
            var market = "\"es\"";  // string | es|it|pt (optional)  (default to "es")
            var page = 1;  // int? |  (optional)  (default to 1)
            var maxItems = 30;  // int? |  (optional)  (default to 30)
            var sortBy = "sortBy_example";  // string | distance|size|rooms|floor|ratioeurm2|price|street|photos|modificationDate|publicationDate|weigh|priceDown|preservationTypeAndPrice|privateAds (optional) 
            var sortOrder = "\"desc\"";  // string | asc|desc (optional)  (default to "desc")
            var minPrice = 8.14D;  // decimal? |  (optional) 
            var maxPrice = 8.14D;  // decimal? |  (optional) 
            var minSize = 8.14D;  // decimal? |  (optional) 
            var maxSize = 8.14D;  // decimal? |  (optional) 
            var minRooms = 56;  // int? |  (optional) 
            var maxRooms = 56;  // int? |  (optional) 
            var locale = "locale_example";  // string | Response language (en, es, it, pt) (optional) 

            try
            {
                // Search listings
                Object result = apiInstance.IdealistaSearchListings(location, operation, propertyType, market, page, maxItems, sortBy, sortOrder, minPrice, maxPrice, minSize, maxSize, minRooms, maxRooms, locale);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling IdealistaApi.IdealistaSearchListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the IdealistaSearchListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search listings
    ApiResponse<Object> response = apiInstance.IdealistaSearchListingsWithHttpInfo(location, operation, propertyType, market, page, maxItems, sortBy, sortOrder, minPrice, maxPrice, minSize, maxSize, minRooms, maxRooms, locale);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling IdealistaApi.IdealistaSearchListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **location** | **string** | Idealista location code (from /suggest) |  |
| **operation** | **string** | sale|rent | [optional] [default to &quot;sale&quot;] |
| **propertyType** | **string** | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] [default to &quot;homes&quot;] |
| **market** | **string** | es|it|pt | [optional] [default to &quot;es&quot;] |
| **page** | **int?** |  | [optional] [default to 1] |
| **maxItems** | **int?** |  | [optional] [default to 30] |
| **sortBy** | **string** | distance|size|rooms|floor|ratioeurm2|price|street|photos|modificationDate|publicationDate|weigh|priceDown|preservationTypeAndPrice|privateAds | [optional]  |
| **sortOrder** | **string** | asc|desc | [optional] [default to &quot;desc&quot;] |
| **minPrice** | **decimal?** |  | [optional]  |
| **maxPrice** | **decimal?** |  | [optional]  |
| **minSize** | **decimal?** |  | [optional]  |
| **maxSize** | **decimal?** |  | [optional]  |
| **minRooms** | **int?** |  | [optional]  |
| **maxRooms** | **int?** |  | [optional]  |
| **locale** | **string** | Response language (en, es, it, pt) | [optional]  |

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

